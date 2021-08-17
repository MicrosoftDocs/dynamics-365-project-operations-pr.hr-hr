---
title: Procjena prodaje i troškova projekta kada resurs koji se bože rezervirati ispunjava više uloga na projektu
description: U ovoj se temi objašnjava način uporabe veličina za određivanje cijena za potporu procjenama cijena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28a67e79b03dfbc38e9786350c931838ef27891a3d26787fc0334e0572528228
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990127"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Procjena prodaje i troškova projekta kada resurs koji se bože rezervirati ispunjava više uloga na projektu 

_**Odnosi se na:** Project Operations za scenarije koji se temelje na resursima / bez zaliha, jednostavne implementacije – od sklapanja posla do predračuna, Project Operations za scenarije koji se temelje na zalihama/proizvodnji_ 

Tvrtke koje se temelje na projektu često imaju potrebu za jednim resursom koji bi ispunjavao više uloga u projektu. Za svaku se ulogu može različito odrediti cijena i trošak. To znači da bi vrijeme istog resursa na projektu moglo dobiti drugačiju financijsku procjenu, ovisno o naplati i cijenama koštanja svake uloge. Možete postaviti vrijednosti u zapisu člana tima za imenovani resurs s drugačijim nadjačavanjima za svaki od zadataka kojem je član tima dodijeljen.

Sljedeći primjer vodi vas kroz način na koji jednostavno poništavanje vrijednosti omogućuje resursu da ima više uloga na projektu s drugačijim cijenama koštanja i naplate.

## <a name="create-tasks"></a>Stvaranje zadatka
Kako biste stvorili zadatke, morate dodati zadatke, kao i sažetke zadataka, nakon čega morate dodijeliti zadatak prije nego što dodate njegovo trajanje. 

### <a name="add-tasks-and-summary-tasks"></a>Dodavanje zadataka i sažetaka zadataka
Kako biste dodali zadatak, poduzmite sljedeće korake.

1. Idite na mogućnost **Projekti** i otvorite projekt kojem želite dodati zadatke.
2. Odaberite **Dodaj novi zadatak**. Dajte naziv zadatku, a zatim pritisnite **Unos**.
3. Unesite naziv sljedećeg zadatka i pritisnite **Unos**. Ponavljajte ovo dok ne dobijete cjelovit popis zadataka.
3. Za uvlačenje zadataka pod **Sažetak** zadataka, odaberite tri okomite točke uz naziv zadatka, a zatim odaberite **Napravi podzadatak**. 

  > [!TIP]
  > Kako biste odabrali više zadataka, odaberite zadatak, pritisnite i držite tipku **Ctrl**, a zatim odaberite drugi zadatak.
  >
  > Možete odabrati i mogućnost **Unaprijedi podzadatak** kako biste zadatke izbacili iz **Sažetka** zadataka.

### <a name="assign-tasks"></a>Dodjeljivanje zadataka

Kako biste dodijelili zadatak, poduzmite sljedeće korake.

1. U stupcu **Dodijeljeno** za zadatak, odaberite ikonu osobe.
2. Odaberite člana tima s popisa ili unesite tekst za traženje imena.

### <a name="add-task-duration-and-columns"></a>Dodajte trajanje zadatka i stupce

Često je najlakše započeti izgradnju projekta s trajanjem. Kako biste zadatku dodali trajanje, poduzmite sljedeće korake.

1. U stupcu **Trajanje** za zadatak unesite broj dana koji će prema vašem mišljenju trebati za dovršetak zadatka. Ako želite upotrijebiti drugu vremensku jedinicu, unesite broj i riječ **sati**, **tjedni** ili **mjeseci**.
2. Ako želite da se vaš zadatak prikaže kao kontrolna točka u obliku dijamanta u prikazu **Vremenska traka**, u stupac **Trajanje** , unesite **0 dana**.
3. Pritisnite mogućnost **Unos** kako biste prešli na sljedeći polje mogućnosti **Trajanje** za zadatak i nastavite unositi trajanja.

  > [!NOTE]
  > Ne možete unijeti trajanje sažetim zadacima.

U svoj projekt možete dodati stupce kako biste omogućili više pojedinosti. Kako biste to učinili, odaberite mogućnost **Dodaj stupac**. 

Dodatne informacije potražite u članku [Izrada projekta](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Postavljanje uloge i organizacijske jedinice za generičkog člana projektnog tima
Poduzmite sljedeće korake kako biste postavili uloge i organizacijske jedinice za generičkog člana tima.

1. Na stranici **Zadaci** odaberite red **Zadatak** za **Zadatak A**. 
2. U stavci **Dodijeljeno** odaberite mogućnost **Dodaj generički resurs**. Ovo otvara stranicu **Brzo stvaranje člana tima**.
3. Na stranici **Brzo stvaranje člana tima** navedite atribute generičkog člana tima koji može izvršiti taj zadatak.
4. Odaberite odgovarajuću ulogu i organizacijsku jedinicu, a zatim odaberite mogućnost **Spremi i zatvori**. Stvara se generički član tima koji se dodjeljuje ovom zadatku. 
5. Ponovite korake 1 – 4 za **Zadatak B**. Međutim, **Zadatak B** mora imati drugačiju ulogu i organizacijsku jedinicu dodijeljenu generičkom članu tima od **Zadatka A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Postavljanje uloge i organizacijske jedinice za projektni zadatak
Poduzmite sljedeće korake kako biste postavili uloge i organizacijske jedinice za zadatak.

1. Nakon što stvorite **Zadatak A**, odaberite zadatak, a zatim odaberite ikonu **i** kako biste otvorili okno **Pojedinosti zadatka**. 
2. U oknu **Pojedinosti zadatka** pomaknite se na dno i odaberite **Prikaži pojedinosti** kako biste otvorili stranicu **Pojedinosti zadatka**.
3. Na stranici **Pojedinosti zadatka**, u stavkama **Uloga** i **Organizacijska jedinica**, dodajte vrijednosti potrebne za izvršavanje ovog zadatka za resurs. 

  > [!NOTE]
  > Ako ovaj scenarij dovršite s pomoću pokaznih podataka aplikacije Project Operations, za ulogu odaberite **Voditelj savjetovanja**, a kao organizacijsku jedinicu **Fabrikam US**.

4. Odaberite **Zadatak B** i zatim zadatak.
5. Odaberite ikonu **i** kako biste otvorili okno **Pojedinosti zadatka**. 
6. U oknu **Pojedinosti zadatka** pomaknite se na dno i odaberite **Prikaži pojedinosti** kako biste otvorili stranicu **Pojedinosti zadatka**.
7. Na stranici **Pojedinosti zadatka**, u stavkama **Uloga** i **Organizacijska jedinica**, dodajte vrijednosti potrebne resursu koji bi trebao izvršiti ovaj zadatak. Vrijednosti u stavkama **Uloga** i **Organizacijska jedinica** za **Zadatak B** moraju se razlikovati od onih za **Zadatak A**. 

  > [!NOTE]
  > Ako ovaj scenarij dovršite s pomoću pokaznih podataka aplikacije Project Operations, za ulogu odaberite **Tehničar za mrežu**, a kao organizacijsku jedinicu **Fabrikam US**.

8. Spremite i zatvorite stranicu **Pojedinosti zadatka**. 

## <a name="team-member-and-estimates-behavior"></a>Član tima i procjene ponašanja 
Kako biste razumjeli ponašanje u rešetki **Član tima** i procjene, poduzmite sljedeće korake.

1. U rešetki **Član tima** odaberite dva generička člana tima, a zatim mogućnost **Generiraj zahtjeve**. To će generirati zahtjeve za resurs. 
2. Odaberite redak člana tima za stavku **Voditelj savjetovanja**, a zatim **Rezerviraj**. Otvara se ploča s rasporedom na kojoj se nalazi popis resursa. Odaberite resurs, a zatim odaberite **Rezerviraj** kako biste za taj zahtjev rezervirali resurs.
3. Odaberite redak člana tima za stavku **Tehničar za mrežu**, a zatim **Rezerviraj**. Otvara se ploča s rasporedom na kojoj se nalazi popis resursa. Odaberite isti resurs kao i gore, a zatim odaberite **Rezerviraj** kako biste za taj zahtjev rezervirali resurs.

### <a name="team-member-grid"></a>Rešetka člana tima 

U rešetki **Član tima** dva zapisa generičkog člana tima brišu se i zamjenjuju sa samo jednim resursom. Postoji jedan skup vrijednosti za taj resurs, koji je zadani skup vrijednosti za stavke **Uloga** i **Organizacijska jedinica**.

Kada proširite redak za taj zapis člana tima, na zapisu člana tima možete vidjeti različite zadatke za oba zadatka. Svaki redak zadatka ima vrijednosti specifične za mogućnosti **Uloga** i **Organizacijska jedinica**. 

### <a name="estimates-grid"></a>Rešetka procjena 

U rešetki **Procjene** oba zadatka za isti resurs imaju različite cijene. Cijena zadaka resursa u **Zadatku A** određuje se s pomoću vrijednost atributa **Uloga** stavke **Voditelj savjetovanja**. Cijena zadaka istog resursa u **Zadatku B** određuje se s pomoću vrijednost atributa **Uloga** stavke **Tehničar za mrežu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]