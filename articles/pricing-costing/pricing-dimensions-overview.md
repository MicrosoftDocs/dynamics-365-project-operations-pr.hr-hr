---
title: Pregled cjenovnih veličina
description: U ovoj se temi nalaze informacije o dimenzijama određivanja cijena u aplikaciji Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073495"
---
# <a name="pricing-dimensions-overview"></a>Pregled cjenovnih veličina

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_

Dimenzije koje se koriste u ljudskim resursima za postavljanje cijena i troškova spadaju u dvije kategorije:

- Osobe
- Planirani rad

Zbog toga postoje dvije vrste dostupnih vrijednosti dimenzija za određivanje cijena:

- **Skupovi mogućnosti** : dimenzije koje su fiksne enumeracije za skup vrijednosti.
- **Vrijednosti temeljene na entitetima** : dimenzije koje mogu biti različiti skup vrijednosti.

## <a name="pricing-dimensions"></a>Cjenovne veličine

Dynamics 365 Project Operations isporučuje se sa zadanim skupom dimenzija za određivanje cijena. Te dimenzije za određivanje cijena možete pregledati tako da odete na **Project Operations** > **Parametri**. U zapisu parametra na kartici **Dimenzije cijena temeljene na iznosu** potvrdite da uloga **msdyn_resourcecategory** i organizacijska jedinica za resurse **msdyn_organizationalunit** sadrže polja **Primjenjivo na prodaju** i **Primjenjivo na trošak** postavljena na **Da**. Ako su ta polja omogućena, možete postaviti cijenu i trošak za svaku kombinaciju uloge i organizacijske jedinice.

Ako trebate odrediti cijenu ili trošak resursa pomoću dodatnih atributa, možete stvoriti prilagođena polja, entitete i dimenzije.

## <a name="pricing-human-resource-time"></a>Određivanje cijene vremena ljudskog resursa
Način na koji tvrtka ili ustanova određuje cijenu vremena ljudskog resursa često je važno strateško razmatranje koje izravno utječe na profitabilnost tvrtke ili ustanove. Surađujte s financijskim timovima i voditeljima kada je vaša tvrtka ili ustanova spremna identificirati način na koji želi postaviti naplatu i stope troškova za vrijeme ljudskog resursa.

Druga razmatranja za određivanje cijena uključuju želite li ponovno koristiti polja ili entitete koji trenutačno ne određuju cijene dimenzija, ali se primjenjuju kao dimenzija cijena za vašu tvrtku ili ustanovu. Polja kao što su **Kategorija transakcije** ( **msdyn_transactioncategory** ) i **Resurs koji je moguće rezervirati** ( **bookableresource** ) primjeri su dimenzija kandidata. 

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
