---
title: Početna stranica Dimenzije cijena i troškova
description: Ova tema pruža pregled dimenzija cijena.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d17939777a6670bafc41b372adc922f8bdcc0411f3fdb399e7c9ab01eca87dd0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998452"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Početna stranica Dimenzije cijena i troškova

[!include [banner](../includes/psa-now-project-operations.md)]

Na dimenzije koje se upotrebljavaju za određivanje cijena i troškova rada u tvrtkama i ustanovama koje se temelje na projektu utječu sljedeći atributi:

- Ljudi koji rade posao sličan svojem iskustvu, ulozi ili zemljopisnom području
- Posao koji treba odraditi slično složenosti ili dobu dana

S obzirom na tipičnu prirodu ovih atributa posla i ljudi koji su potrebni za obavljanje posla, u aplikaciji Project Service Automation dostupne su dvije vrste vrijednosti dimenzija za određivanje cijena: 

- **Skupovi mogućnosti** – Atributi koji su fiksni popisi skupa vrijednosti.
- **Entitetne vrijednosti** – Atributi koji mogu imati različit skup vrijednosti koji je konačan, ali se može mijenjati tijekom vremena.

## <a name="pricing-dimensions"></a>Cjenovne veličine

PSA se isporučuje sa zadanim skupom dimenzija cijena. Možete ih pregledati tako da idete na **Project Service** > **Parametri**. U zapisu parametra na kartici **Dimenzije cijena temeljene na iznosu** potvrdite da uloga **msdyn_resourcecategory** i organizacijska jedinica za resurse **msdyn_organizationalunit** sadrže polja **Primjenjivo na prodaju** i **Primjenjivo na trošak** postavljena na **Da**. To će vam omogućiti da postavite cijenu i trošak za svaku kombinaciju uloge i organizacijske jedinice.

![Snimka zaslona parametara rješenja Project Service s istaknutom mogućnosti „Primjenjivo na prodaju”.](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Ako ste upotrebljavali gotova polja uloge i organizacijske jedinice kao dimenzije cijena prije verzije 3 sustava PSA, neće biti vidljivih promjena. Možete nastaviti uobičajeno koristiti aplikaciju Project Service. 

Ako trebate odrediti cijenu ili trošak resursa pomoću dodatnih atributa, možete stvoriti prilagođena polja, entitete i dimenzije. Za više informacija pogledajte sljedeće teme, međutim, napominjemo da morate dovršiti postupke redoslijedom navedenim u nastavku:

- [Stvaranje prilagođenih polja i entiteta](create-custom-fields-entities.md)
- [Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima](field-references.md)
- [Postavljanje prilagođenih polja kao cjenovnih veličina](set-up-pricing-dimensions.md)
- [Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Određivanje cijene vremena ljudskog resursa
Način na koji tvrtka ili ustanova određuje cijenu vremena ljudskog resursa često je važno strateško razmatranje koje izravno utječe na profitabilnost tvrtke ili ustanove. Surađujte s financijskim timovima i voditeljima kada je vaša tvrtka ili ustanova spremna identificirati način na koji želi postaviti naplatu i stope troškova za vrijeme ljudskog resursa.

Druga razmatranja za određivanje cijena uključuju želite li ponovno koristiti polja ili entitete koji trenutačno ne određuju cijene dimenzija, ali se primjenjuju kao dimenzija cijena za vašu tvrtku ili ustanovu. Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji je moguće rezervirati** (**bookableresource**) primjeri su dimenzija kandidata. 

Razmotrite treba li dimenzija određivanja cijena biti tablica ili skup mogućnosti. Ako predviđate promjene vrijednosti dimenzije koja će premašiti 10 ili 12, a potrebni su vam dodatni atributi tih vrijednosti, možete stvoriti entitet umjesto skupa mogućnosti. Održavanje skupa mogućnosti, kao što je dodavanje ili uklanjanje vrijednosti, zahtijeva administratora ili razvojnog programera dok dodavanje novih redaka u tablicu može izvršiti većina poslovnih korisnika.

Sljedeći primjer prikazuje stope naplate postavljene na temelju uloge i organizacijske jedinice za resurse kojoj resurs pripada. Stope troškova obično se temelje na platnom razredu zaposlenika i organizacijskoj jedinici kojoj pripadaju. U ovom primjeru tablice stopa naplate i stopa troškovaa izgledat će kao sljedeće.

**Primjeri stopa naplate**

| Uloga        | Organizacijska jedinica    |Jedinica      |Cijena      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Razvojni inženjer   | Contoso US  |h | 200|USD     |
| Razvojni inženjer   | Contoso Indija |h|   112|USD     |


**Primjeri stopa troškova**

| Platni razred     | Organizacijska jedinica    |Jedinica      |Cijena      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| My company_Band1 | Contoso US  |h | 145|USD     |
| My company_Band2 | Contoso Indija |h|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]