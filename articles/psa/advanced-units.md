---
title: Grupe jedinica i jedinice
description: Ova tema pruža informacije o grupama jedinica i jedinicama.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 78f154856acf796f408491c5873cb29da8ac55bb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073404"
---
# <a name="unit-groups-and-units"></a>Grupe jedinica i jedinice

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Grupe jedinica i jedinice osnovni su entiteti u Microsoft Dynamics 365. Jedinica je pojedinačna jedinica mjere, a više jedinica može se grupirati u grupe jedinica. Grupa jedinica ponekad se naziva jediničnim rasporedom u korisničkom sučelju sustava Dynamics 365 (UI). 

Evo nekoliko primjera jedinica i grupa jedinica:
 
- **Grupa jedinica** : Udaljenost 
    - **Jedinice** : milja, kilometar, i tako dalje.
- **Grupa jedinica** : Vrijeme
    - **Jedinice** : sat, dan, tjedan, i tako dalje. 

Kada postavite više jedinica u grupi jedinica, također morate postaviti faktor konverzije između njih tako da odredite prvu jedinicu koju ste postavili kao zadanu ili primarnu jedinicu za grupu jedinica. 

Na primjer, u grupi jedinica **Vrijeme** , ako postavite **Sat** kao prvu jedinicu, sustav označava **Sat** kao zadanu jedinicu. Ako je sljedeća jedinica koju postavljate **Dan** , morate postaviti faktor konverzije za **Dan** u **Sat.** Ako zatim dodate **Tjedan** kao treću jedinicu, morate postaviti faktor konverzije za **Tjedan** u smislu **Dana** ili **Sata**. 

Sljedeća slika prikazuje primjer postavljanja za jedinicu **Dan** , gdje polje **Količina** prikazuje broj sati koji su u danu i **Tjednu** , gdje polje **Količina** prikazuje broj dana u tjednu.

> ![Grupa jedinica: informacijska stranica](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Korištenje jedinica i grupa jedinica

Dynamics 365 Project Service Automation koristi jedinice i grupe jedinica za obradu procjena i unosa za troškove i vrijeme. 

Za troškove, svaka kategorija troška ima zadanu grupu jedinica i jedinicu. Te se vrijednosti unose kao zadane vrijednosti u unosima cjenika za kategorije troškova. 

Na primjer, imate kategoriju troška koja se zove **Kilometraža**. Ima grupu jedinica koja se zove **Udaljenost** i zadanu jedinicu koja se zove **Milja.** Ako postavite grupu jedinica **Udaljenost** tako da ima dvije jedinice ( **Milja** i **Kilometar** ), možete postaviti dvije cijene za kategoriju **Kilometraža** na jednom cjeniku: cijena po milji i cijena po kilometru.

| Kategorija troška  | Grupa jedinica  | Jedinica      | Način određivanja cijena  | Jedin. cijena  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometraža           | Udaljenost      | Milja      | Jedin. cijena    | 10 USD            |
| Kilometraža           | Udaljenost      | kilometar | Jedin. cijena    |  6 USD            |

Kada unesete trošak u projekt, sustav određuje cijenu kroz kombinaciju kategorije i jedinice za trošak. 

| Opis troška        | Kategorija troška  | Jedinica  | Količina  | Jedinična cijena   |
|----------------------------|---------------------|-------|-----------|----------------|
| Vozi do lokacije klijenta | Kilometraža             | Milja  | 1,0        | 10 USD         |

Za vrijeme, svako zaglavlje cjenika ima polje **Zadana vremenska jedinica**. Vrijednost se postavlja kada izradite zaglavlje cjenika. Ta se jedinica zatim koristi za postavljanje svih cijena koje se temelje na ulozi na tom cjeniku.

Reci procjene za polje **Vrijeme na ponudi** mogu se izraziti u bilo kojoj jedinici vremena. Međutim, reci procjene projekata i unosa vremena za projekte mogu koristiti samo jedinicu vremena **Sat**. Ako jedinica unosa vremena ili procjene ne odgovara jedinici u retku cjenika za tu ulogu, sustav pretvara cijenu u jedinice koje su definirane u procjeni projekta ili stvarnoj transakciji projekta.

Sljedeći primjer pokazuje kako sustav PSA koristi grupu jedinica, jedinice i čimbenike konverzije.
- Jedinice

   - **Grupa jedinica** : Vrijeme 
   - **Jedinice** : Sat 
    
    - **Dan** - Faktor konverzije: 8 sati       
    - **Tjedan** - Faktor konverzije: 40 sati  
        
- Postavljanje cjenika na projektu A:

    - **Naziv** : Prodajne cijene u UK-u za 2016. 
    - **Zadana vremenska jedinica** : Dan 
    - **Valuta** : GBP

| Uloga      | Grupa jedinica | Jedinica | Organizacijska jedinica | Cijena   |
|-----------|------------|------|---------------------|---------|
| Razvojni inženjer | Vrijeme       | Dan  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Unos vremena

Sljedeća tablica prikazuje dobivenu transakciju na strani prodaje koju je izradio sustav PSA za trosatni projekt.


| Projekt   | Zadatak    | Uloga      | Količina | Jedinica  | Jedinična cijena | Nenaplaćeni iznos prodaje |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projekt A | Dizajn  | Razvojni inženjer | 3        | Sat  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Često postavljena pitanja za jedinicu vremena

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Pretvara li PSA u različite jedinice u slučaju troškova?
Ne. Konverzija jedinica radi samo za vrijeme. Za troškove, ako sustav ne može pronaći cijenu za kombinaciju kategorije troška i jedinice, cijena je postavljena na 0,00 prema zadanim postavkama.

### <a name="why-does-psa-convert-time-units"></a>Zašto PSA pretvara vremenske jedinice?
U nekim zemljama ili regijama postoji pravna obveza da se stope naplaćivanja postavljaju u danima. Pregovaranje o cijenama i disceniranje tijekom ciklusa ponude izvodi se koristeći dnevne stope za svaku naplativu ulogu. Procjena rasporeda i unos vremena izvode se u satima. Za podršku ove razlike u vremenskim jedinicama, PSA pretvara vremenske jedinice.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Mogu li se vremenske jedinice promijeniti na procjenama projekta?
Ne. Procjena rasporeda trenutačno je ograničena na sate i ne može se mijenjati.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Mogu li se jedinice i grupe jedinica uređivati, brisati i dodavati?
Da. Uz iznimku grupe jedinica **Vrijeme** i jedinice **Sat** , sve jedinice mogu se brisati ili uređivati, a mogu se dodati i nove jedinice. U sustavu PSA, grupa jedinica **Vrijeme** i jedinica **Sat** ne mogu se brisati. Međutim, oni se mogu ažurirati s prevedenim tekstom za polje **Naziv**.
