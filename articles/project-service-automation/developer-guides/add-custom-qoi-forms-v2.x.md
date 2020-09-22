---
title: Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)
description: Ova tema pruža informacije o tome kako dodati obrasce prilagođenih entiteta za prilike, ponude, narudžbe ili fakture u sustavu Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750036"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="b4e83-103">Dodavanje novih obrazaca prilagođenih entiteta (Project Service Automation 2. x)</span><span class="sxs-lookup"><span data-stu-id="b4e83-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="b4e83-104">Polje Vrsta</span><span class="sxs-lookup"><span data-stu-id="b4e83-104">Type field</span></span> 

<span data-ttu-id="b4e83-105">Dynamics 365 Project Service Automation oslanja se na polje **Vrsta** (**msdyn\_ordertype**) entiteta Prilika, Ponuda, Narudžba i Fakture za raspoznavanje verzija tih entiteta **koje se temelje na radu** od verzija **koje se temelje na artiklu** i verzija koje se **temelje na usluzi**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="b4e83-106">Verzije tih entiteta koje se temelje na radu obrađuje aplikacija PSA.</span><span class="sxs-lookup"><span data-stu-id="b4e83-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="b4e83-107">Mnoštvo poslovne logike rješenja na strani klijenta i na strani poslužitelja ovisi o polju **Vrsta**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="b4e83-108">Stoga je važno da se polje inicijalizira s ispravnom vrijednošću kada se izrađuju entiteti.</span><span class="sxs-lookup"><span data-stu-id="b4e83-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="b4e83-109">Neispravna vrijednost može uzrokovati neispravan odaziv, a neka poslovna logika možda se neće ispravno izvoditi.</span><span class="sxs-lookup"><span data-stu-id="b4e83-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="b4e83-110">Automatsko prebacivanje obrazaca</span><span class="sxs-lookup"><span data-stu-id="b4e83-110">Automatic form switching</span></span>

<span data-ttu-id="b4e83-111">Da bi se izbjeglo potencijalno oštećenje podataka i neočekivani odazivi koji su uzrokovani neispravnom inicijalizacijom i uređivanjem zapisa entiteta prodaje, PSA sada uključuje logiku za automatsko prebacivanje obrazaca u gotovim obrascima.</span><span class="sxs-lookup"><span data-stu-id="b4e83-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="b4e83-112">Ova logika vodi korisnike u ispravan obrazac za rad s verzijom koja se temelji na radu ili bilo u koju drugu vrstu entiteta Prilika, Ponuda, Narudžba ili Faktura.</span><span class="sxs-lookup"><span data-stu-id="b4e83-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="b4e83-113">Kada korisnik otvori verziju entiteta Prilika, Ponuda, Narudžba ili Faktura koja se temelji na radu, obrazac se prebacuje na **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="b4e83-114">Logika automatskog prebacivanja obrazaca oslanja se na mapiranje između vrijednosti **formId** i polja **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="b4e83-115">Svi gotovi obrasci dodani su tom mapiranju.</span><span class="sxs-lookup"><span data-stu-id="b4e83-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="b4e83-116">Međutim, prilagođeni obrasci moraju se ručno dodati da bi se naznačilo koja je verzija entiteta namijenjena za obradu.</span><span class="sxs-lookup"><span data-stu-id="b4e83-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="b4e83-117">To se temelji na polju **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="b4e83-118">Ako u mapiranju nedostaje prebacivanje obrazaca, logika će se prebaciti na gotovi obrazac na temelju vrijednosti koja je spremljena u polju **msdyn\_ordertype** entiteta.</span><span class="sxs-lookup"><span data-stu-id="b4e83-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="b4e83-119">Dodavanje prilagođenih obrazaca i uključivanje logike prebacivanja obrazaca</span><span class="sxs-lookup"><span data-stu-id="b4e83-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="b4e83-120">Sljedeći primjer pokazuje kako dodati prilagođeni obrazac, **Moje informacije o projektu**, tako da radi s prilikama koje se temelje na radu.</span><span class="sxs-lookup"><span data-stu-id="b4e83-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="b4e83-121">Isti se postupak koristi za dodavanje prilagođenih obrazaca tako da rade s ponudama, narudžbama i fakturama.</span><span class="sxs-lookup"><span data-stu-id="b4e83-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="b4e83-122">Slijedite ove korake da biste izradili prilagođenu verziju obrasca **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="b4e83-123">U entitetu Prilika, otvorite obrazac **Informacije o projektu** i spremite kopiju pod nazivom **Moje informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="b4e83-124">Otvorite novi obrazac, a zatim, u svojstvima, provjerite jesu li prisutne skripte za inicijalizaciju obrasca iz obrasca **Informacije o projektu**.</span><span class="sxs-lookup"><span data-stu-id="b4e83-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="b4e83-125">Nemojte ukloniti skripte.</span><span class="sxs-lookup"><span data-stu-id="b4e83-125">Don't remove the scripts.</span></span> <span data-ttu-id="b4e83-126">U protivnom se neki podaci mogu neispravno inicijalizirati.</span><span class="sxs-lookup"><span data-stu-id="b4e83-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="b4e83-127">Provjerite je li polje **Vrsta** (**msdyn\_ordertype**) prisutno u obrascu.</span><span class="sxs-lookup"><span data-stu-id="b4e83-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="b4e83-128">Nemojte ukloniti ovo polje.</span><span class="sxs-lookup"><span data-stu-id="b4e83-128">Don't remove this field.</span></span> <span data-ttu-id="b4e83-129">U protivnom skripte za inicijalizaciju neće ispuniti zadatak.</span><span class="sxs-lookup"><span data-stu-id="b4e83-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="b4e83-130">Pronađite vrijednost **formId** novog obrasca.</span><span class="sxs-lookup"><span data-stu-id="b4e83-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="b4e83-131">Možete dovršiti ovaj korak na dva načina:</span><span class="sxs-lookup"><span data-stu-id="b4e83-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="b4e83-132">Izvezite obrazac **Moje informacije o projektu** kao dio neupravljanog rješenja, a zatim potražite vrijednost **formId** u datoteci customization.xml izvezenog rješenja.</span><span class="sxs-lookup"><span data-stu-id="b4e83-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="b4e83-133">Otvorite obrazac **Moje infomacije o projektu** u uređivaču obrazaca, a zatim potražite globalni jedinstveni identifikator (GUID) pored parametra **fromId** u URL-u, kao što je prikazano na sljedećoj ilustraciji.</span><span class="sxs-lookup"><span data-stu-id="b4e83-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Vrijednost formId novog obrasca u URL-u](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="b4e83-135">Izradite mapiranje **msdyn\_ordertype** za vrijednost **formId** uređivanjem web-resursa msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="b4e83-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="b4e83-136">Uklonite kȏd iz resursa i zamijenite ga sljedećim kȏdom.</span><span class="sxs-lookup"><span data-stu-id="b4e83-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="b4e83-137">Spremite i potom objavite prilagodbe.</span><span class="sxs-lookup"><span data-stu-id="b4e83-137">Save and then publish the customizations.</span></span>
