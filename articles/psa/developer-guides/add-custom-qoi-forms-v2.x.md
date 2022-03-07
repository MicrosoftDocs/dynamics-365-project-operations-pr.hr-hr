---
title: Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)
description: Ova tema pruža informacije o tome kako dodati obrasce prilagođenih entiteta za prilike, ponude, narudžbe ili fakture u sustavu Dynamics 365 Project Service Automation 2.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 400d817ee7cbae6f6da95db4286ad6c4d6ff349a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6007987"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Polje Vrsta 

Dynamics 365 Project Service Automation oslanja se na polje **Vrsta** (**msdyn\_ordertype**) entiteta Prilika, Ponuda, Narudžba i Fakture za raspoznavanje verzija tih entiteta **koje se temelje na radu** od verzija **koje se temelje na artiklu** i verzija koje se **temelje na usluzi**. Verzije tih entiteta koje se temelje na radu obrađuje aplikacija PSA. Mnoštvo poslovne logike rješenja na strani klijenta i na strani poslužitelja ovisi o polju **Vrsta**. Stoga je važno da se polje inicijalizira s ispravnom vrijednošću kada se izrađuju entiteti. Neispravna vrijednost može uzrokovati neispravan odaziv, a neka poslovna logika možda se neće ispravno izvoditi.

## <a name="automatic-form-switching"></a>Automatsko prebacivanje obrazaca

Da bi se izbjeglo potencijalno oštećenje podataka i neočekivani odazivi koji su uzrokovani neispravnom inicijalizacijom i uređivanjem zapisa entiteta prodaje, PSA sada uključuje logiku za automatsko prebacivanje obrazaca u gotovim obrascima. Ova logika vodi korisnike u ispravan obrazac za rad s verzijom koja se temelji na radu ili bilo u koju drugu vrstu entiteta Prilika, Ponuda, Narudžba ili Faktura. Kada korisnik otvori verziju entiteta Prilika, Ponuda, Narudžba ili Faktura koja se temelji na radu, obrazac se prebacuje na **Informacije o projektu**.

Logika automatskog prebacivanja obrazaca oslanja se na mapiranje između vrijednosti **formId** i polja **msdyn\_ordertype**. Svi gotovi obrasci dodani su tom mapiranju. Međutim, prilagođeni obrasci moraju se ručno dodati da bi se naznačilo koja je verzija entiteta namijenjena za obradu. To se temelji na polju **msdyn\_ordertype**. Ako u mapiranju nedostaje prebacivanje obrazaca, logika će se prebaciti na gotovi obrazac na temelju vrijednosti koja je spremljena u polju **msdyn\_ordertype** entiteta.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Dodavanje prilagođenih obrazaca i uključivanje logike prebacivanja obrazaca

Sljedeći primjer pokazuje kako dodati prilagođeni obrazac, **Moje informacije o projektu**, tako da radi s prilikama koje se temelje na radu. Isti se postupak koristi za dodavanje prilagođenih obrazaca tako da rade s ponudama, narudžbama i fakturama.

Slijedite ove korake da biste izradili prilagođenu verziju obrasca **Informacije o projektu**.

1. U entitetu Prilika, otvorite obrazac **Informacije o projektu** i spremite kopiju pod nazivom **Moje informacije o projektu**.
2. Otvorite novi obrazac, a zatim, u svojstvima, provjerite jesu li prisutne skripte za inicijalizaciju obrasca iz obrasca **Informacije o projektu**. 

    > [!IMPORTANT]
    > Nemojte ukloniti skripte. U protivnom se neki podaci mogu neispravno inicijalizirati.

3. Provjerite je li polje **Vrsta** (**msdyn\_ordertype**) prisutno u obrascu. 

    > [!IMPORTANT]
    > Nemojte ukloniti ovo polje. U protivnom skripte za inicijalizaciju neće ispuniti zadatak.

4. Pronađite vrijednost **formId** novog obrasca. Možete dovršiti ovaj korak na dva načina:

    - Izvezite obrazac **Moje informacije o projektu** kao dio neupravljanog rješenja, a zatim potražite vrijednost **formId** u datoteci customization.xml izvezenog rješenja.
    - Otvorite obrazac **Moje infomacije o projektu** u uređivaču obrazaca, a zatim potražite globalni jedinstveni identifikator (GUID) pored parametra **fromId** u URL-u, kao što je prikazano na sljedećoj ilustraciji.

    ![Vrijednost formId novog obrasca u URL-u](media/how-to-add-custom-forms-in-v2.0.png)

5. Izradite mapiranje **msdyn\_ordertype** za vrijednost **formId** uređivanjem web-resursa msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Uklonite kȏd iz resursa i zamijenite ga sljedećim kȏdom.

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. Spremite i potom objavite prilagodbe.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]