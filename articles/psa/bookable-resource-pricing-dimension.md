---
title: Koristi resurs koji je moguće rezervirati kao dimenziju određivanja cijena
description: Ova tema pruža informacije o korištenju resursa koji je moguće rezervirati kao dimenzije određivanja cijena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d9b25a768f892d83c09d37ce76291d6c8e75b1be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144989"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Koristi resurs koji je moguće rezervirati kao dimenziju određivanja cijena

[!include [banner](../includes/psa-now-project-operations.md)]

Ova tema pruža informacije o korištenju resursa koji je moguće rezervirati kao dimenzije određivanja cijena. Prije nego što započnete, ako još niste izradili rješenje dimenzije cijena, morat ćete stvoriti novu. Ako već imate rješenje dimenzije cijena, možete uvesti promjene u tom rješenju. Ako niste izradili novo rješenje dimenzije cijena za svoju organizaciju, provedite postupke u temi [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Dodaj resurs koji je moguće rezervirati obrascima i prikazima
Da bi polja bila vidljiva u korisničkom sučelju u rješenju dimenzije određivanja cijena, morat ćete proći kroz sve obrasce i prikaze ključnih entiteta programa Project Service i dodati ta polja obrascima i prikazima tih entiteta.
Sljedeća tablica je sveobuhvatan popis gotovih obrazaca i prikaza koji su navedeni po entitetu, a koji će se trebati ažurirati. Ako u prilagodbama tih entiteta postoje dodatni prikazi ili obrasci, njima također dodajte nova polja.
Otvorite Istraživač rješenja za rješenje dimenzije određivanja cijena, a zatim kliknite **Objavi sve prilagodbe**.


|   Entitet        | Obrasci   |Prikazi        |
| ------------------------------|---------------------------------|----------------------------------|
|  Cijena uloge|• Informacije |• Cijene kategorije aktivnog resursa<br> • Pridruženi prikaz cijene kategorije resursa|
|  Provizija cijene uloge|• Informacije|• Aktivna provizija cijene uloge<br>• Pridruženi prikaz provizije cijene uloge|
|  Pojedinost retka ponude|• Informacije o projektu<br>• Brzo stvaranje projekta|• Pojedinost retka aktivne ponude<br>• Kombinirane pojedinosti retka ponude<br>• Pridruženi prikaz pojedinosti retka ponude|
|  Pojedinost retka ugovora projekta|• Informacije o projektu<br>• Brzo stvaranje projekta|• Kombinirane pojedinosti retka ugovora<br>• Pojedinosti aktivnog retka ugovora<br>• Pridruženi prikaz pojedinosti retka ugovora|
|  Projektni zadatak|• Informacije<br>• Novi obrazac||
|  Članov projektnog tima|• Informacije<br>• Novi obrazac|• Aktivni članovi projektnog tima<br>• Članovi projektnog tima<br>• Pridruženi prikaz članova projektnog tima|
|  Unos vremena|• Informacije<br>• Stvaranje unosa vremena|• Moji Unosi vremena po datumu<br>• Moji Unosi vremena za ovaj tjedan<br>• Unos vremena za odobrenje|
|  Redak u dnevniku|• Informacije<br>• Brzo stvaranje|• Reci u aktivnom dnevniku<br>• Pridruženi prikaz retka u dnevniku|
|  Pojedinost retka fakture|• Informacije<br>• Brzo stvaranje|• Pojedinosti retka aktivne fakture<br>• Naplative transakcije fakture<br>• Besplatne transakcije fakture<br>• Pridruženi prikaz pojedinosti retka fakture<br>• Nenaplative transakcije fakture|
|  Stvarni posao|• Informacije<br>• Aktivni stvarni podaci|• Pridruženi prikaz stvarnih podataka|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Postavi resurs koji je moguće rezervirati kao dimenziju određivanja cijena

1. Na web-sučelju otvorite **Project Service** > **Postavke** > **Parametri**. Na stranici **Parametar**, na kartici **Dimenzije određivanja cijena koje se temelje na iznosu**, primijetite da rešetka na kartici prikazuje zapise u entitetu dimenzija određivanja cijena. 
2. Dodajte **Resurs koji je moguće rezervirati** na ovaj popis dimenzija određivanja cijena kao **kao msdyn_bookableresource**. 
3. Naznačite kontekst u kojem resurs koji je moguće rezervirati ima dimenziju određivanja cijena i postavite vrijednosti **Primjenjivo na troškove** i **Primjenjivo na prodaju**.
4. U polju **Vrsta dimenzije**, odaberite **Koja se temelji na iznosu**. 
5. Odaberite prioritet troškova i prodaje za resurs koji je moguće rezervirati. Obično, kada je uključen kao dimenzija određivanja cijena, resurs koji je moguće rezervirati ima najviši prioritet, tako da će postavljanje na **1** (ili **0** ovisno o tome kako računate prioritet) osigurati to ponašanje.

## <a name="set-up-pricing-dimension-field-names"></a>Postavi nazive polja dimenzije određivanja cijena

Kada se naziv polja dimenzije određivanja cijena u tablici **Cijena uloge** razlikuje od naziva polja u bilo kojem od drugih entiteta gdje je nužno da postoji zadana postavka za cijene, zapis dimenzije određivanja cijena mora prepoznati različite nazive.    
Za resurs koji je moguće rezervirati, entitet **Članovi tima projekta** ima malo drugačiji naziv polja (**msdyn_bookableresourceid**) od naziva na entitetu **Cijena uloga** (**msdyn_bookableresource**). Zapis dimenzije određivanja cijena za **msydn_bookableresource** mora to prepoznati. 
1. Da biste to učinili, dvaput kliknite redak u rešetki **Dimenzije određivanja cijena** da biste otvorili stranicu dimenzije **msdyn_bookableresource.**
2. Na stranici dimenzije, na kartici **Povezano** kliknite **Nazivi polja dimenzije određivanja cijena**.

 ![Kartica Nazivi polja dimenzije određivanja cijena](media/PD-fieldname.png)

4. Na povezanom prikazu koji se otvori, kliknite **Dodaj novi naziv polja dimenzije određivanja cijena**.

 ![Dodaj nove nazive polja dimenzije određivanja cijena](media/Add-NewPD-fieldname.png)


To otvara stranicu **Novi naziv polja dimenzije određivanja cijena** za **msdyn_bookableresource**. 

5. **msdyn_projectteam** dodaj polju **Logični naziv entiteta**, a **msdyn_bookableresourceid** polju **Naziv polja**. Spremite zapis.

 ![Obrazac novog naziva polja dimenzije određivanja cijena](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]