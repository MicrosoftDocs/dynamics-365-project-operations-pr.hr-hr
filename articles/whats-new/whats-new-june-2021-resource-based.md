---
title: Novosti u lipnju 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovoj temi nalaze se informacije o ažuriranjima kvalitete dostupnim u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za lipanj 2021. godine.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c6a40335df89cc6b2bb35e54832140aac6eb9ac6
ms.sourcegitcommit: 03414a74ddf1f2d63043d734ebdee7485f1aadd2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/25/2021
ms.locfileid: "7679200"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u lipnju 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

- Project Operations u okruženju sustava Dynamics 365 Dataverse verzije 4.11.0.156 ili 4.11.0.164.
- Upravljanje projektima i računovodstvo u aplikacijama Finance and Operations okruženja verzije 10.0.19.

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Mogućnost brisanja [Redci prijedloga fakture za projekt za scenarije prilagodbe](../invoicing/correct-project-invoice-proposals.md).
- Specificirani redci troškova odražavaju nazive potkategorija u izvješću o troškovima [Izmijenjena izvješća o troškovima – nove značajke](../expense/expense-reports-reimagined.md#new-features).
- Način plaćanja dostupan je u novom oknu s troškovima tijekom stvaranja novog troška.
- Opća dostupnost API-ja rasporeda projekta. Ova nova funkcionalnost omogućuje korisnicima da programski izvršavaju operacije stvaranja, ažuriranja i brisanja u projektnim zadacima, dodjelama resursa, ovisnostima zadataka i zapisima članova projektnog tima. Dodatne informacija potražite u odjeljku [Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. 

Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućiti sve povezane karte tablice dok ažurirate svoje verzije rješenja aplikacije Project Operations platforme Dataverse i aplikacija Finance and Operations. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti na stranici **Dvostruko pisanje** u stupcu **Verzija**. Aktivirajte novu verziju karte odabirom mogućnosti **Verzije tabličnih karata**, odabirom najnovije verzije, a zatim spremanjem odabrane verzije. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem s nedostatkom stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Naplata i određivanje cijene | 2281417 | Ispravljen je problem u vezi s neuspjehom radnje automatskog stvaranja fakture putem rasporeda faktura. |
| Naplata i određivanje cijene | 2287835 | Poboljšana je učinkovitost potvrde računa. |
| Upravljanje prilikama | 2222555 | Naplativost procjena materijala mora se ispravno kopirati u pojedinosti retka ponude pri uporabi mogućnosti **Uvoz iz procjene projekta**. |
| Upravljanje prilikama | 2223427 | Prilagodbe su sada dozvoljene za radnju **GenerateRetainersFromRetainerScheduleOptions**. |
| Upravljanje prilikama | 2277528 | Popravljen je izračun vrijednosti kontrolne točke za naplatu za retke ugovora o projektu s više klijenata. |
| Planiranje i praćenje projekta | 2226110 | Popravljen je problem s prekidima funkcije **Generiraj zahtjev** u rešetki **Projektni tim**. |
| Planiranje i praćenje projekta | 2208109 | Korisnici ne mogu stvoriti projekt u jednoj valuti s povezanim zadacima u drugoj valuti. |
| Planiranje i praćenje projekta | 2258228 | Ažuriran je popis polja kojima je dozvoljeno mijenjati entitete **Zakazivanje** koji upotrebljavaju API rasporeda. |
| Planiranje i praćenje projekta | 2293989 | Ispravni jezik i regionalne postavke moraju se proslijediti rešetki **Projektni zadaci**. |
| Upravljanje resursima | 2220493 | Popravljeno je korisničko iskustvo u rešetki **Zadatak** kada se zahtjev za resursom brzo označavao kao završen. |
| Upravljanje resursima | 2330496 | Popravljen je problem s učitavanjem **Ploče s rasporedom**. (Ažuriranje kvalitete dostupno je u verziji 4.11.0.164) |
| Vrijeme i trošak | 2194431 | Rešetka **Vremenski unos** mora poštivati početak tjedna kako je postavljeno u stavci **Postavke sustava**. |
| Vrijeme i trošak | 2277311 | Nakon što izbrišete vrijednost u ćeliji u rešetki **Vremenski unos**, pokazivač ostaje u rešetki. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Bilješke na obrascu** i **Postavljanje obrasca** nisu vidljivi pod stavkom **Postavke upravljanja projektom** u financijskim pravnim osobama koje su integrirane s aplikacijom Project Operations. |
| Upravljanje projektom i računovodstvo | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Zadani je opis za PDV prazan kada je **Vrsta knjiženja** = **Porez na promet** za vaučere fakture za projekt. |
| Upravljanje projektom i računovodstvo | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Knjiže se dvostruke transakcije kada se naplata koja se temelji na zadatku upotrebljava na platformi Dataverse s integriranom aplikacijom Project Operations. |
| Upravljanje projektom i računovodstvo | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Postotak dovršenosti za priznavanje prihoda nije točan tijekom uporabe integracije aplikacije Project Operations. |
| Upravljanje projektom i računovodstvo | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Akumulacija prihoda udvostručuje se na fakturi dobavljača koja je na čekanju u scenariju integrirane aplikacije Project Operations. |
| Upravljanje projektom i računovodstvo | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Dnevnik integracije nije moguće knjižiti kada je pravilo profila prihoda postavljeno na postavke **Grupa**. |
| Upravljanje projektom i računovodstvo | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Račun za kupnju nije moguće knjižiti za narudžbe za projekt koje imaju retke s više mjernih jedinica. |
| Upravljanje projektom i računovodstvo | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Zadana financijska veličina za projekt ne može se ažurirati s pomoću podatkovnog entiteta projekta **V2**. |
| Upravljanje projektom i računovodstvo | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Izvršenje skupnog postupka za stvaranje procjene projekta predugo traje. |
| Upravljanje projektom i računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Brisanjem ugovora briše se i adresa povezana s klijentom. |
| Putovanje i trošak | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Uvjet tijeka rada odobrenja izvješća o troškovima nije pravilno procijenjen. |
| Putovanje i trošak | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Politika izvješća o troškovima ne procjenjuje ispravno ID projekta. |
| Putovanje i trošak | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Radnja **Razdijeli na osobno za transakcije troškova među poduzećima unutar iste tvrtke** ne funkcionira ispravno. |
| Putovanje i trošak | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Opravdanja retka izvješća o troškovima slučajno se brišu tijekom brisanja određenih putnih naloga. To se događa kada su ID zapisa izvješća o troškovima i putnog naloga isti. |
| Putovanje i trošak | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Postoji problem u mobilnoj aplikaciji za troškove kada je polje **ID projekta** obvezno u pravilima izvješća o troškovima. |
| Putovanje i trošak | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Troškovi ostvareni između poduzeća unutar iste tvrtke koji su povezani s projektom ne mogu se uređivati. Umjesto toga, prikazuje se sljedeća poruka o pogrešci: „Referenca objekta nije postavljena na instancu objekta.” |
| Putovanje i trošak | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Nakon knjiženja izvješća o troškovima, u sporednoj knjizi banke navodi se pogrešna valuta i iznos. |
| Putovanje i trošak | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Poboljšanja su napravljena u značajci *Brisanje transakcija ostvarenih kreditnom karticom*.  |
| Putovanje i trošak | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Porez na promet uključen u izvješće o troškovima ne izračunava se dosljedno kada je u pravnoj osobi navedena druga valuta za izvješće. |
| Putovanje i trošak | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Na izvedbu utječe dodavanje novog gotovinskog putnog troška. |
| Putovanje i trošak | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravila politike troškova ne pokreću se u izvješću o troškovima. |
| Putovanje i trošak | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Prijenos nove dijeljene kategorije s pomoću Okvira za upravljanje podacima uklanja sve potkategorije za sve dijeljene kategorije. |
| Putovanje i trošak | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Kada stvarate redak troška i zatim odaberete kategoriju, prikazuje se sljedeća pogreška: „Kombinacija grupe poreza na promet DOM i grupe poreza na promet stavki STD nije valjana.” |
| Putovanje i trošak | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Postoje problemi sinkronizacije u mobilnoj aplikaciji za troškove. |
