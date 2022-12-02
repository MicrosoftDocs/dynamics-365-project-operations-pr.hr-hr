---
title: Pregled veličina za određivane cijena
description: U ovom članku nalaze se informacije o veličinama za određivanje cijena u aplikaciji Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 294dcff8e9717aaa3a0459daf87cb7d608c96106
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918027"
---
# <a name="pricing-dimensions-overview"></a>Pregled veličina za određivane cijena

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_

Dimenzije koje se koriste u ljudskim resursima za postavljanje cijena i troškova spadaju u dvije kategorije:

- Osobe
- Planirani rad

Zbog toga postoje dvije vrste dostupnih vrijednosti dimenzija za određivanje cijena:

- **Skupovi mogućnosti**: dimenzije koje su fiksne enumeracije za skup vrijednosti.
- **Vrijednosti temeljene na entitetima**: dimenzije koje mogu biti različiti skup vrijednosti.

## <a name="pricing-dimensions"></a>Veličine za određivanje cijena

Dynamics 365 Project Operations isporučuje se sa zadanim skupom veličina za određivanje cijena. Te dimenzije za određivanje cijena možete pregledati tako da odete na **Project Operations** > **Parametri**. U zapisu parametra na kartici **Dimenzije cijena temeljene na iznosu** potvrdite da uloga **msdyn_resourcecategory** i organizacijska jedinica za resurse **msdyn_organizationalunit** sadrže polja **Primjenjivo na prodaju** i **Primjenjivo na trošak** postavljena na **Da**. Ako su ta polja omogućena, možete postaviti cijenu i trošak za svaku kombinaciju uloge i organizacijske jedinice.

![Snimka zaslona parametara rješenja Project Service s istaknutom mogućnosti „Primjenjivo na prodaju”.](media/PS-OOB-parameters.png)

Ako trebate odrediti cijenu ili trošak resursa pomoću dodatnih atributa, možete stvoriti prilagođena polja, entitete i dimenzije. Dodatne informacije potražite u sljedećim člancima. 
  
  > [!NOTE]
  > Postupci moraju biti dovršeni redoslijedom kojim su navedeni.

1. [Stvaranje rješenja za prilagođene veličine određivanja cijena](../sales/create-solution-custompd.md)
2. [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities-pricing-dimensions.md)
3. [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](add-custom-fields-price-setup-transactional-entities.md)
4. [Postavljanje prilagođenih polja kao cjenovnih veličina](set-up-custom-fields-pricing-dimensions.md)
5. [Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Određivanje cijene vremena ljudskog resursa
Način na koji tvrtka ili ustanova određuje cijenu vremena ljudskog resursa često je važno strateško razmatranje koje izravno utječe na profitabilnost tvrtke ili ustanove. Surađujte s financijskim timovima i voditeljima kada je vaša tvrtka ili ustanova spremna identificirati način na koji želi postaviti naplatu i stope troškova za vrijeme ljudskog resursa.

Druga razmatranja za određivanje cijena uključuju želite li ponovno koristiti polja ili entitete koji trenutačno ne određuju cijene dimenzija, ali se primjenjuju kao dimenzija cijena za vašu tvrtku ili ustanovu. Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji je moguće rezervirati** (**bookableresource**) primjeri su dimenzija kandidata. 

Razmotrite treba li dimenzija određivanja cijena biti tablica ili skup mogućnosti. Ako predviđate promjene vrijednosti dimenzije koja će premašiti 10 ili 12, a potrebni su vam dodatni atributi tih vrijednosti, možete stvoriti entitet umjesto skupa mogućnosti. Održavanje skupa mogućnosti, kao što je dodavanje ili uklanjanje vrijednosti, zahtijeva administratora ili razvojnog programera dok dodavanje novih redaka u tablicu može izvršiti većina korisnika.

Sljedeći primjer prikazuje stope naplate postavljene na temelju uloge i organizacijske jedinice za resurse kojoj resurs pripada. Stope troškova obično se temelje na platnom razredu zaposlenika i organizacijskoj jedinici kojoj pripadaju. U ovom primjeru tablice stopa naplate i stopa troškovaa izgledat će kao sljedeće.

**Primjeri stopa naplate**

| Uloga        | Organizacijska jedinica    |Jedinica      |Cijena      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Razvojni inženjer   | Contoso US  |Hour | 200|USD     |
| Razvojni inženjer   | Contoso, Indija |Hour|   112|USD     |


**Primjeri stopa troškova**

| Platni razred     | Organizacijska jedinica    |Jedinica      |Cijena      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |Hour | 145|USD     |
| My company_Band2 | Contoso, Indija |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]