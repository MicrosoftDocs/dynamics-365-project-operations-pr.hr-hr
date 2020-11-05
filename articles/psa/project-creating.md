---
title: Rasporedi projekta
description: Ova tema pruža informacije o tome kako izraditi raspored.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a6b27050a19d8a7f2ed35f74b42bb4f371ad069
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073423"
---
# <a name="project-schedules"></a>Rasporedi projekta 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Raspored projekta objašnjava koji posao treba dovršiti, koji će resursi izvesti posao i koji je vremenski okvir u kojem posao treba biti dovršen. Raspored projekta odražava sve poslove povezane s pravovremenom isporukom projekta. U sustavu Dynamics 365 Project Service Automation izrađujete raspored projekta tako da raščlanite posao na zadatke kojima se može upravljati, procijenite vrijeme potrebno za obavljanje svakog zadatka, postavite ovisnosti zadataka, postavite trajanje zadataka i procjenite generičke resurse koji će obaviti zadatke. Raspored projekta izrađuje se na kartici **Raspored** na stranici projekta.
 
## <a name="tasks"></a>Zadaci

Prvi korak izrade rasporeda projekta jest raščlamba posla na dijelove kojima je moguće upravljati. Raspored u PSA-u podržava sljedeće značajke:

- Korijenski čvor projekta
- Zadaci sažetka ili spremnika
- Zadaci lisnog čvora

### <a name="project-root-node"></a>Korijenski čvor projekta

Korijenski čvor projekta jest zadatak sažetka najviše razine za projekt. Svi drugi zadaci projekta stvaraju se ispod njega. Naziv korijenskog zadatka uvijek se postavlja na naziv projekta. Sažeti podaci o radu, datumima i trajanju korijenskog čvora temelje se na vrijednostima u hijerarhiji ispod njega. Ne možete uređivati svojstva korijenskog čvora. Također ne možete izbrisati korijenski čvor.

### <a name="summary-or-container-tasks"></a>Zadaci sažetka ili spremnika 

Zadaci sažetka imaju podzadatke ili zadatke spremnika ispod njih. Ne sadrže rad ni vlastiti trošak. Umjesto toga, njihov rad i trošak skupna su vrijednost rada i troškova njihovih zadataka spremnika. Datum početka zadatka sažetka datum je početka zadataka spremnika, a datum završetka datum je završetka zadataka spremnika. Naziv zadatka sažetka može se urediti, no svojstva zakazivanja (rad, datumi i trajanje) ne mogu se urediti. Ako izbrišete zadatak sažetka, izbrisat ćete i sve njegove zadatke spremnika.

### <a name="leaf-node-tasks"></a>Zadaci lisnog čvora

Zadaci lisnog čvora predstavljaju najgranularniji rad na projektu. Sadrže procijenjeni rad, resurse, planirane datume početka i završtka te trajanje.
 
## <a name="creating-a-task-hierarchy"></a>Izrada hijerarhije zadataka

Hijerarhiju zadataka možete izraditi pomoću sljedećih mogućnosti:

- Gumb **Dodaj zadatak**
- Gumb **Uvuci zadatak**
- Gumb **Izvuci zadatak**
- Gumbi **Premjesti gore** i **Premjesti dolje**
- Tipkovni prečaci i pristupačnost

### <a name="add-task"></a>Dodavanje zadatka

Gumb **Dodaj zadatak** omogućuje izradu novog zadatka u hijerarhiji. Ako ne odaberete položaj, zadatak se umeće na kraju. 

Svakom zadatku dodjeljuje se ID rasporeda. ID rasporeda predstavlja dubinu i položaj zadatka u hijerarhiji. Koristi numeriranje strukture. Za zadatke na prvoj razini ispod korijenskog čvora projekta koristi se shema numeriranja od 1, 2, 3 itd. Za zadatke ispod prve razine koristi se shema numeriranja od 1.1, 1.2, 1.3 itd.

### <a name="indent-task"></a>Uvlačenje zadatka

Kada se zadatak uvuče, postaje podređen zadatku koji je izravno iznad njega. ID rasporeda zadatka zatim se ponovno izračunava tako da se temelji na ID-u rasporeda novog nadređenog zadatka i prati shemu numeriranja strukture. Nadređeni zadatak sada je zadatak sažetka ili zadatak spremnika. Stoga on postaje skupna vrijednost svojih podređenih zadataka.

### <a name="outdent-task"></a>Izvlačenje zadatka 

Kada se zadatak izvuče, više nije podređeni zadatak nadređenog zadatka. ID rasporeda zatim se ponovno izračunava tako da odražava ažuriranu dubinu i položaj u hijerarhiji. Rad, trošak i datumi prethodnog nadređenog zadatka ponovno se izračunavaju tako da ne uključuju taj zadatak.

### <a name="move-up-and-move-down"></a>Premještanje gore i premještanje dolje 

Gumbi **Premjesti gore** i **Premjesti dolje** mijenjaju položaj zadatka unutar nadređene hijerarhije. Promjene navedene vrste ne utječu na rad, trošak, datume ili trajanje zadatka. Zahvaćen je samo ID rasporeda zadatka. ID rasporeda ponovno se izračunava tako da odražava novi položaj na popisu podređenih zadataka nadređenog zadatka.

### <a name="accessibility-and-keyboard-shortcuts"></a>Tipkovni prečaci i pristupačnost

Rešetka **Raspored** potpuno je dostupna i može se koristiti s čitačima zaslona kao što su Narrator, JAWS ili NVDA. Možete se kretati područjem rešetke pomoću tipki sa strelicama (kao u programu Microsoft Excel), možete koristiti tipku Tab za kretanje interaktivnim elementima korisničkog sučelja i možete koristiti tipku sa strelicom dolje, tipku Enter ili razmaknicu za odabir i aktiviranje padajućih izbornika. Zaglavlja stupaca također su interaktivna. Možete sakriti i prikazati stupce, koristiti tipku Tab i tipke sa strelicama za kretanje zaglavljima stupaca te koristiti gumbe radnji na alatnoj traci. Osim toga, možete koristiti sljedeće tipkovne prečace:

- **Osvježi** : ALT+SHIFT+F5
- **Dodaj** : ALT+SHIFT+Insert
- **Izbriši** : ALT+SHIFT+Delete
- **Premjesti gore/dolje** :ALT+SHIFT+Up/strelice gore/dolje
- **Uvuci/izvuci** : ALT_SHIFT+ strelice lijevo/desno
- **Proširi/sažmi hijerarhije** : ALT+SHIFT+tipkeplus/minus

## <a name="task-attributes"></a>Atributi zadatka

Naziv zadatka opisuje posao koji treba dovršiti. U PSA-u atributi povezani sa zadatkom opisuju raspored zadatka i zahtjeve za broj djelatnika.

> ![Atributi zadatka](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atributi rasporeda

Atributi **Rad** , **Datum početka** , **Datum završetka** i **Trajanje** određuju raspored zadatka.

Dodatni atributi rasporeda uključuju sljedeće:

- **Sati rada** : unesite procjenu sati potrebnih za dovršetak zadatka. 
- **Trajanje** : navedite broj radnih dana potrebnih za dovršetak zadatka.
- **ID rasporeda** : ovaj automatski generirani ID koristi se za raspoređivanje zadataka u hijerarhiji. Ovisnosti između zadataka upravljaju stvarnim redoslijedom kojim se zadaci obavljaju.
 
### <a name="staffing-attributes"></a>Atributi broja djelatnika

Atributima broja djelatnika pristupa se putem polja **Resursi** u rasporedu. Možete pretražiti postojeći resurs ili kliknuti **Stvori** i u oknu **Brzo stvaranje** dodati člana projektnog tima kao novi resurs.

Polja **Uloga** , **Jedinica za resurse** i **Naziv položaja** koriste se za opisivanje zahtjeva za broj djelatnika za zadatak. Ti atributi broja djelatnika zajedno s rasporedom zadataka koriste se za pronalaženje dostupnih resursa za taj zadatak.

**Uloga** – odredite vrstu resursa koji je potreban za izvršavanje zadatka.

**Jedinica za resurse** – navedite jedinicu iz koje je potrebno dodijeliti resurse za zadatak. Taj atribut utječe na procjenu troška i prodaje za zadatak ako su troškovi i stopa naplate za resurs postavljeni na temelju jedinica za resurse.

**Naziv položaja** – unesite neslužbeni naziv za generički resurs koji služi kao rezervirano mjesto za resurs koji će u konačnici obaviti posao.

Polje **Resursi** sadrži naziv položaja generičkog resursa ili imenovanog resursa kada se pronađe takav resurs.

Polje **Kategorija** sadrži vrijednosti koje označavaju širu vrstu posla u koju se zadatak može grupirati. To polje ne utječe na zakazivanje ili broj djelatnika. Koristi se samo za izvješćivanje.

### <a name="task-dependencies"></a>Zavisnosti zadatka 

Raspored u PSA-a možete koristiti za stvaranje odnosa prethodnika između zadataka. Polje **Prethodnik** u odjeljku **Zadaci** uzima jednu ili više vrijednosti da bi se označili zadaci o kojima zadatak ovisi. Kada se zadatku dodijele vrijednosti prethodnika, zadatak može započeti tek nakon dovršetka svih zadataka prethodnika. Zbog ovisnosti planirani početni datum zadatka vraća se na datum dovršetka zadataka prethodnika.

Način zadatka ne utječe na ažuriranja izvršena na datum početka i datum završetka zadataka prethodnika/ovisnih zadataka.

## <a name="task-mode"></a>Način zadatka 

Način zadatka određuje zakazivanje zadataka lisnog čvora. PSA podržava dva načina zadatka za svaki zadatak: automatsko zakazivanje i ručno zakazivanje.

### <a name="auto-scheduling"></a>Automatsko zakazivanje 
 
Ako je način zadatka postavljen na **Automatsko zakazano** , modul zakazivanja zadataka koristi pravila za zakazivanje za atribute zadatka kako bi se odredio raspored za zadatak:

#### <a name="scheduling-rules"></a>Pravila zakazivanja

Prema zadanim postavkama, ako lisni čvor nema prethodnike, datum početka postavlja se na zakazani datum početka. Trajanje zadatka lisnog čvora uvijek se izračunava kao broj radnih dana između njegovog početnog i završnog datuma. Ako je zadatak automatski zakazan, modul zakazivanja uvijek slijedi ova pravila:

- Datumi početka i završetka zadatka uvijek moraju biti radni dani prema kalendaru za zakazivanje projekta. 
- Za bilo koji zadatak koji sadrži zadatke prethodnika datum početka automatski se postavlja na najnoviji datum završetka prethodnika.
- Rad se izračunava pomoću ove formule: broj osoba × trajanje × sati u standardnom radnom danu u kalendaru projekta.

### <a name="manual-scheduling"></a>Ručno zakazivanje

Ako pravila automatskog zakazivanja ne ispunjavaju vaše zahtjeve, možete postaviti način zadatka za zadatak na **Ručno zakazano**. Ta postavka zaustavlja modul zakazivanja u izračunu vrijednosti za druge atribute zakazivanja. Bez obzira na način zadatka, ako postavite prethodnike za zadatke, to će se uvijek odraziti na datum početka ovisnog zadatka.
