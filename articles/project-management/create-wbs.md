---
title: Stvaranje strukturne analize rada
description: U ovoj se temi objašnjava način stvaranja strukturna analize rada (WBS, work breakdown structure) koja uključuje osnovne kontrole u novom sučelju za planiranje.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3b8162d256aa145301fc64bee9682caa8737496f
ms.sourcegitcommit: d3f66dfb5978c5c6b7fd51363c7f9278737c49c1
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2021
ms.locfileid: "7928606"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Stvaranje strukturne analize rada (WBS)

Raspored projekta objašnjava koji posao treba dovršiti, koji će resursi izvesti posao i koji je vremenski okvir u kojem posao treba biti dovršen. Raspored odražava sve poslove povezane s pravovremenom isporukom projekta. U aplikaciji Dynamics 365 Project Operations stvarate raspored projekata na sljedeći način:

  - Raščlanjivanjem posla na zadatke kojima se može upravljati.
  - Procjenom vremena potrebnog za izvršavanje svakog zadatka.
  - Postavljanjem ovisnosti zadataka.
  - Postavljanjem trajanja zadataka.
  - Procjenom generičkih resursa koji će izvršavati zadatke. 

Raspored projekta izrađuje se na kartici **Raspored**, na stranici **Projekt**.

## <a name="tasks"></a>Zadaci

Prvi korak izrade rasporeda projekta jest raščlamba posla na dijelove kojima je moguće upravljati. Raspored u aplikaciji Project Operations podržava sljedeće značajke:

- Zadaci sažetka ili spremnika
- Zadaci lisnog čvora

### <a name="summary-tasks"></a>Sumarni zadaci

Sumarni zadaci mogu pohraniti druge sumarne zadatke ili zadatke lisnog čvora. Ne sadrže rad ni vlastiti trošak. Umjesto toga, njihov rad i trošak skupna su vrijednost rada i troškova njihovih zadataka spremnika. Datum početka zadatka sažetka datum je početka zadataka spremnika, a datum završetka datum je završetka zadataka spremnika. Naziv sumarnog zadatka može se urediti, no svojstva planiranja, uključujući rad, datume i trajanje, ne mogu se urediti. Ako izbrišete zadatak sažetka, izbrisat ćete i sve njegove zadatke spremnika.

### <a name="leaf-node-tasks"></a>Zadaci lisnog čvora

Zadaci lisnog čvora predstavljaju najgranularniji rad na projektu. Sadrže procijenjeni rad, resurse, planirane datume početka i završtka te trajanje.

## <a name="create-a-task-hierarchy"></a>Stvaranje hijerarhije zadataka

### <a name="add-a-task"></a>Dodavanje zadatka

Kako biste dodali jedan ili više zadataka, poduzmite sljedeće korake.

1. Idite na **Projekti** te odaberite i otvorite projektni zapis za koji želite stvoriti raspored. 
2. Odaberite karticu **Zadaci**. 
3. Odaberite **Dodaj novi zadatak**, unesite naziv zadatka, a zatim pritisnite Unos.
2. Unesite drugi naziv zadatka i ponovo pritisnite Unos dok ne dobijete cjelovit popis zadataka.

### <a name="manage-hierarchy-of-a-task"></a>Upravljanje hijerarhijom zadatka

Kada se zadatak uvuče, postaje podređen zadatku koji je izravno iznad njega. ID rasporeda zadatka zatim se ponovno izračunava tako da se temelji na ID-u rasporeda novog nadređenog zadatka i prati shemu numeriranja strukture. Nadređeni zadatak sada je sumarni zadatak. Stoga on postaje skupna vrijednost svojih podređenih zadataka. Kada se zadatak promakne, više nije podređeni zadatak nadređenog zadatka. ID rasporeda zatim se ponovno izračunava tako da odražava ažuriranu dubinu i položaj u hijerarhiji. Rad, trošak i datumi prethodnog nadređenog zadatka ponovno se izračunavaju tako da ne uključuju taj zadatak.

Kako biste uvukli ili promakli zadatak, poduzmite sljedeće korake.

1. Na stranici **Projekt**, na kartici **Zadaci**, pod stavkom **Sumarni zadaci**, odaberite tri okomite točke uz naziv zadatka, a zatim odaberite **Napravi podzadatak**. 
2. Odaberite zadatak za uvlačenje ili promaknuće. Kako biste odabrali više zadataka, odaberite zadatak, pritisnite i držite tipku Ctrl, a zatim odaberite dodatni zadatak.
2. Odaberite **Uvuci** ili **Promakni podzadatak** kako biste zadatke maknuli ili izbacili iz sumarnih zadataka.

### <a name="move-tasks-up-and-down"></a>Pomicanje zadataka gore i dolje

Zadaci se mogu premjestiti na bilo koju razinu u strukturnoj analizi rada na jedan od dva načina:

- Odaberite još jedan zadatak i povucite ga na željeno mjesto.
- Odaberite jedan ili više zadataka, kliknite desnom tipkom miša i odaberite **Izreži**, odaberite odredišnu ćeliju u rasporedu, a zatim desnom tipkom miša kliknite i odaberite **Zalijepi**.

## <a name="task-attributes"></a>Atributi zadatka

Naziv zadatka opisuje posao koji treba dovršiti. Atributi povezani sa zadatkom u aplikaciji Project Operations opisuju raspored zadatka i njihove preduvjete za broj djelatnika.

## <a name="schedule-attributes"></a>Atributi rasporeda

Atributi **Rad**, **Datum početka**, **Datum završetka** i **Trajanje** određuju raspored zadatka.

Sljedeća tablica prikazuje dodatne atribute rasporeda.

| **Konačni naziv zaslona** | **Konačni opis** |
| --- | --- |
| Dovršeni rad (sati) | Rad za dovršenje zadatka u satima. |
| Trajanje | Prikazuje trajanje zadatka u danima. |
| Ukupan rad | Ukupan rad na zadatku u satima. |
| Završi | Datum i vrijeme završetka. |
| Dovršeno: % | Postotak dovršenosti zadatka. |
| Grupa projekta | Ploča sa zadacima može se grupirati po grupi tako da svaka grupa ima svoj stupac. |
| Preostali rad (sati) | Preostali rad na zadatku u satima. |
| Početak | Datum i vrijeme početka. |
| Ime | Naziv zadatka. |
| ID | ID zadatka u strukturnoj analizi rada. |

Kao administrator možete definirati prilagođena polja na entitetu zadatka. Međutim, polja se ne mogu prikazati na rešetki rasporeda. Kako biste vidjeli svoja prilagođena polja, dodajte ih na stranicu s pojedinostima **Projektni zadatak**.

## <a name="staffing-attributes"></a>Atributi broja djelatnika

Atributima broja djelatnika pristupa se putem polja **Resursi** u rasporedu. Možete pretražiti postojeći resurs ili odabrati **Stvori** i u oknu **Brzo stvaranje** dodati člana projektnog tima kao novi resurs.  Kada tražite resurs pomoću birača resursa u rešetki zadatka, prikazu ploče ili ganttu, pretraživanje vraća postojeće članove projektnog tima ili aktivne resurse koje je moguće rezervirati.

Polja **Uloga**, **Jedinica za resurse** i **Naziv položaja** koriste se za opisivanje zahtjeva za broj djelatnika za zadatak. Ti atributi broja djelatnika zajedno s rasporedom zadataka koriste se za pronalaženje dostupnih resursa za taj zadatak.

   - **Uloga** : Navedite vrstu resursa koja je potrebna za obavljanje zadatka.,
   - **Jedinica za resurse**: Navedite jedinicu iz koje je potrebno dodijeliti resurse za zadatak. Taj atribut utječe na procjenu troška i prodaje za zadatak ako su troškovi i stopa naplate za resurs postavljeni na temelju jedinica za resurse.
   - **Naziv položaja**: Unesite naziv za generički resurs koji služi kao rezervirano mjesto za resurs koji će u konačnici obaviti posao.

Polje **Resursi** sadrži naziv položaja generičkog resursa ili imenovanog resursa kada se pronađe takav resurs.

Polje **Kategorija** sadrži vrijednosti koje označavaju širu vrstu posla u koju se zadatak može grupirati. To polje ne utječe na zakazivanje ili broj djelatnika. Umjesto toga, polje se upotrebljava samo za izvješćivanje.

## <a name="task-dependencies"></a>Zavisnosti zadatka

Raspored u aplikaciji Project Operations-a možete upotrebljavati za stvaranje odnosa prethodnika između zadataka. Polje **Prethodnik** upotrebljava jednu ili više vrijednosti kako bi se označili zadaci o kojima zadatak ovisi. Kada se zadatku dodijele vrijednosti prethodnika, zadatak može započeti tek nakon dovršetka svih zadataka prethodnika. Zbog ovisnosti planirani početni datum zadatka vraća se na datum dovršetka zadataka prethodnika.

Način zadatka ne utječe na ažuriranja izvršena na datum početka i datum završetka zadataka prethodnika/ovisnih zadataka.

## <a name="accessibility-and-keyboard-shortcuts"></a>Tipkovni prečaci i pristupačnost

Rešetka **Raspored** potpuno je dostupna i može se koristiti s čitačima zaslona kao što su Narrator, JAWS ili NVDA. Možete se kretati područjem rešetke s pomoću tipki sa strelicama (kao u programu Microsoft Excel), možete upotrebljavati tipku Tab za kretanje interaktivnim elementima korisničkog sučelja i možete upotrebljavati tipku sa strelicom dolje, tipku Unos ili razmaknicu za odabir i otvaranje padajućih izbornika.

## <a name="project-limitations"></a>Ograničenja projekta 
Ako upotrebljavate strukturna analizu rada u aplikaciji Project Operations, trebali biste biti svjesni ograničenja u nastavku. Ova ograničenja vrijede za projekte i zadatke. Dodatne informacija potražite u odjeljku [Project for the web – ograničenja i granice](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Polje**                                          |  **Ograničenje**           |
|----------------------------------------------------|----------------------|
| Maksimalan ukupan broj zadataka projekta                  | 500                  |
| Maksimalno ukupno trajanje projekta               | 3650 dana (10 godina) |
| Maksimalni ukupni resursi projekta              | 150                  |
| Maksimalan broj veza (samo slijednik) za projekt | 600                  |
| Maksimalna ukupna prilagođena polja za projekt          | 1,0                   |
| Maksimalan broj stavki kontrolnog popisa po zadatku                   | 20                   |

**Ograničenja zadatka**

| **Polje**                               |   **Ograničenje**           |
|-----------------------------------------|-----------------------|
| Maksimalna razina hijerarhije                 | 10 razina             |
| Maksimalan broj veza (slijednik + prednik) | 20                    |
| Maksimalno trajanje zadatka lista           | 1250 dana             |
| Maksimalno trajanje sažetog zadatka      | 3650 dana (10 godina)  |
| Maksimalni resursi dodijeljeni zadatku    | 20 resursa          |
| Podržani datumski raspon za zadatak         | 01. 01. 2000. – 31. 12. 2149. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
