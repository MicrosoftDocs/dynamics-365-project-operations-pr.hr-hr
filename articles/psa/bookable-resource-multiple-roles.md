---
title: Procjena prodaju i troškove projekta kada resurs koji može rezervirati ispunjava više uloga u projektu
description: U ovoj se temi nalaze informacije o načinu na koji se dimenzije mogu upotrebljavati za podršku određivanju cijena i troškova za resurs koji ispunjava višestruke uloge u projektu.
author: rumant
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
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073440"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Procjena prodaju i troškove projekta kada resurs koji može rezervirati ispunjava više uloga u projektu 

Tvrtke temeljene na projektu često imaju potrebu za jednim resursom za obavljanje više uloga u projektu. Svaka od ovih uloga može imati različitu cijenu i troškove, što znači da vrijeme istog resursa na projektu može dobiti različitu financijsku procjenu, ovisno o računu i troškovima za svaku od uloga. Project Service Automation omogućuje postavljanje vrijednosti u zapisu o članu tima za imenovani resurs i omogućuje različite izmjene svakog zadatka kojem je član tima dodijeljen.

Sljedeći primjer objašnjava kako jednostavna izmjena ove vrijednosti omogućuje resursu da ima više uloga na projektu s različitim cijenama troška i računa.

## <a name="create-tasks"></a>Stvaranje zadatka
Stvorite dva projektna zadatka, svaki po 40 sati, Zadatak A i Zadatak B. Odaberite Zadatak A kao prethodnika Zadataka B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Postavljanje jedinice za generičkog člana projektnog tima za ulogu i tvrtku ili ustanovu

1. Na stranici **Raspored** odaberite redak **Zadatak** za zadatak A. 
2. S padajućeg popisa u polju **Resursi** odaberite **Stvori**.
3. Na stranici **Brzo stvaranje člana tima** navedite atribute generičkog člana tima koji može izvršiti taj zadatak.
4. Odaberite odgovarajuću ulogu i organizacijsku jedinicu, a zatim odaberite mogućnost **Spremi i zatvori**. Stvara se generički član tima koji se dodjeljuje ovom zadatku. 

Ponovite ove korake za zadatak B i provjerite da se uloga i organizacijska jedinica generičkog člana tima stvorenog za zadatak B razlikuje od onog za zadatak A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Postavljanje uloge i organizacijske jedinice za projektni zadatak

1. Nakon što stvorite zadatak A, odaberite zadatak, a zatim odaberite mogućnost **Uredi zadatak**.
2. Na stranici **Pojedinosti zadatka** pronađite polja **Uloga** i **Organizacijska jedinica** i dodajte vrijednosti potrebne za resurs koji bi trebao izvršiti ovaj zadatak. 

  > [!NOTE]
  > Ako dovršavate ovaj scenarij s pomoću pokaznih podataka aplikacije Project Service Automation, odaberite stavku **Voditelj savjetovanja** za ulogu, a **Fabrikam US** kao organizacijsku jedinicu.

3. Odaberite Zadatak B, a zatim odaberite mogućnost **Uredi zadatak**.
4. Na stranici **Pojedinosti zadatka** pronađite polja **Uloga** i **Organizacijska jedinica** i dodajte vrijednosti potrebne za resurs koji bi trebao izvršiti ovaj zadatak. Provjerite razlikuju li se vrijednosti u poljima **Uloga** i **Organizacijska jedinica** za zadatak B od onih u poljima za zadatak A. 

  > [!NOTE]
  > Ako dovršavate ovaj scenarij s pomoću pokaznih podataka aplikacije Project Service Automation, odaberite stavku **Tehničar za mrežu** za ulogu, a **Fabrikam US** kao organizacijsku jedinicu.

5. Spremite i zatvorite stranicu **Pojedinosti zadatka**. 

## <a name="team-member-and-estimates-behaviour"></a>Član tima i procjena ponašanja 

1. Na stranici **Pojedinosti zadatka** , na stavci **Član tima** , odaberite dva člana generičkog tima, a zatim odaberite **Generiraj zahtjeve**. To će generirati zahtjeve za resurs. 
2. Odaberite redak člana tima za stavku **Voditelj savjetovanja** a zatim odaberite **Rezerviraj**. Otvara se ploča s rasporedom i rezervira resurs za taj zahtjev.
3. Odaberite redak člana tima za stavku **Tehničar za mrežu** a zatim odaberite **Rezerviraj**. Otvara se ploča s rasporedom i rezervira isti resurs za taj zahtjev.

### <a name="team-member-grid"></a>Rešetka člana tima 
Na rešetki **Član tima** primijetit ćete kako su dva zapisa o članu generičkog tima izbrisana i zamijenjene jednim resursom. Postoji jedan skup vrijednosti za taj resurs koji prikazuje zadani skup vrijednosti za stavke **Uloga** i **Organizacijska jedinica**.
Kada proširite red tog zapisa o članu tima, na tom zapisu možete vidjeti različite zadatke za oba ta zadatka. Svaki redak zadatka ima vrijednosti specifične za mogućnosti **Uloga** i **Organizacijska jedinica**. 

### <a name="estimates-grid"></a>Rešetka procjena 
Kada prijeđete na rešetku **Procjene** , primijetit ćete kako oba zadatka za isti resurs imaju različitu cijenu.
Cijena zadaka resursa u Zadatku A određuje se s pomoću vrijednost atributa **Uloga** stavke **Voditelj savjetovanja**. Cijena zadaka istog resursa u Zadatku B određuje se s pomoću vrijednost atributa **Uloga** stavke **Tehničar za mrežu**.





