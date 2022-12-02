---
title: Novosti u studenom 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha za studeni 2021.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932885"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Upravljanje projektima i računovodstvo u verziji 10.0.22 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Sučelja za programiranje (API-ji) aplikacije Project Scheduling sada podržavaju mogućnost stvaranja i brisanja spremnika projekta.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2240080 | Polje **Uvjeti plaćanja** ne smije se duplicirati na predračunu. |
| Naplata i određivanje cijene | 2358236 | Ispravak fakture mora omogućiti ispravke koji imaju retke s nultom cijenom. |
| Upravljanje resursima | 2410072 | Dopušta postavljanje resursa koji je dodijeljen zadatku kao voditelj projekata. |
| Naplata i određivanje cijene | 2430234 | Rješava problem s izračunom performansi. |
| Vrijeme i trošak | 2436978 | Dopušta da se vrijeme unese u formatu hh:mm. |
| Naplata i određivanje cijene | 2448623 | Omogućuje ažuriranje cjenika nakon povezivanja s organizacijskom jedinicom. |
| Vrijeme i trošak | 2460396 | Dopušta brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cijene | 2467386 | Dopušta brisanje projekta koji ima zadatak, čak i kada je zadatak povezan s osvojenom ponudom. |
| Vrijeme i trošak | 2461744 | Prikaz **Moja neuspjela odobrenja** sadrži samo odobrenja projekta u fazi **Poslano**. |
| Vrijeme i trošak | 2464082 | Uklanja vezu s odobrenja projekta na skup odobrenja kada se ciljni status podudara. |
| Vrijeme i trošak | 2468108 | Posao rasporeda ne bi trebao postaviti status **Obrada** za skup odobrenja. |
| Vrijeme i trošak | 2471503 | Briše skupove odobrenja stare sedam dana. |
| Naplata i određivanje cijene | 2480687 | Referenca retka ponude ne smije se ukloniti kada se kreira ključna točka retka ponude. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani iznosi dobavljača u transakcijama troškova projekta nisu prikazani na popisu transakcija. |
| Upravljanje projektom i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača prekinuta je kada je uključena integracija fakture dobavljača. |
| Upravljanje projektom i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uvjeti plaćanja na projektnim fakturama ne funkcioniraju prema očekivanjima. |
| Upravljanje projektom i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se otpusti zadržavanje dobavljača, knjiženje vaučera ima dodatne retke koji su netočni. |
| Upravljanje projektom i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kada se knjiži dnevnik integracije Project Operations, ne uspijeva jer nedostaju dimenzije za račun na koji se ne knjiži. |
| Upravljanje projektom i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Project** ne može se uređivati na fakturi dobavljača na čekanju kada je kategorija nabave dodijeljena stavci. |
| Upravljanje projektom i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko okno nedostaje ako niste prijavljeni u Project Operations Dataverse. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kada knjižite prihod iz fakture projekta u primijenjenom slučaju zadržavanja, dolazi do problema jer transakcije vaučera nisu pravilno uravnotežene. |
| Upravljanje projektom i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Stvaranje procjene nakon što knjižite prijedlog fakture blokira uvoz redaka korekcije. |
| Upravljanje projektom i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmjena potpuno fakturiranog ključnog zapisa ne bi trebala biti moguća. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Sva izvješća o troškovima vidljiva su kada tražite kategoriju u mobilnoj aplikaciji Expense. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netočni iznosi transakcija dobavljača i transakcija poreza na promet koji su knjiženi iz troškova nastalih transakcijom kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Nevažno upozorenje pojavljuje se kada osvježite stranicu **Izvješće o troškovima**. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešan privremeni odobravatelj koristi se kada izbrišete privremenog odobravatelja i ponovno pošaljete izvješće o troškovima kroz tijek rada. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do pogreške knjiženja povezane s postavljanjem kilometraže. |
