---
title: Novosti u studenom 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u studenome 2021. za scenarije temeljene na resursima/neutemeljenim sredstvima.
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

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.22

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Sučelja za programiranje aplikacija za planiranje projekata (API-ji) sada podržavaju mogućnost stvaranja i brisanja projektnih grupa.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dataverse"></a>Projektne operacije u programu Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2240080 | Polje Uvjeti **plaćanja** ne smije se duplicirati na predračunu. |
| Naplata i određivanje cijene | 2358236 | Ispravak fakture mora dopustiti ispravke koji imaju retke nulte cijene. |
| Upravljanje resursima | 2410072 | Dopusti postavljanje resursa koji je dodijeljen zadatku kao voditelj projekta. |
| Naplata i određivanje cijene | 2430234 | Riješite problem s izračunom performansi troškova. |
| Vrijeme i trošak | 2436978 | Dopustite unos vremena u hh:mm formatu. |
| Naplata i određivanje cijene | 2448623 | Dopustite ažuriranje cjenika nakon povezivanja s organizacijskom jedinicom. |
| Vrijeme i trošak | 2460396 | Dopustite brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cijene | 2467386 | Dopusti brisanje projekta koji ima zadatak, čak i kada je zadatak povezan s osvojenom ponudom. |
| Vrijeme i trošak | 2461744 | Prikaz **Moje neuspjelo odobrenje** sadrži samo odobrenja projekta u **fazi Poslano**. |
| Vrijeme i trošak | 2464082 | Uklonite vezu iz odobrenja projekta na odobrenje postavljeno kada se podudara ciljni status. |
| Vrijeme i trošak | 2468108 | Zadatak Raspored ne bi trebao postaviti **status Obrade** za skup odobravanja. |
| Vrijeme i trošak | 2471503 | Izbrišite skupove odobrenja stare sedam dana. |
| Naplata i određivanje cijene | 2480687 | Referenca retka ponude ne smije se ukloniti prilikom stvaranja prekretnice retka ponude. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani iznosi dobavljača u transakcijama troškova projekta nisu prikazani na popisu transakcija. |
| Upravljanje projektom i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača prekinuta je kada je uključena integracija fakture dobavljača. |
| Upravljanje projektom i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uvjeti plaćanja na računima projekta ne funkcioniraju kako se očekivalo. |
| Upravljanje projektom i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se oslobodi zadržavanje dobavljača, knjiženje vaučera sadrži dodatne retke koji nisu točni. |
| Upravljanje projektom i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kada se temeljnica integracije s operacijama projekta proknjiži, ona ne uspijeva zbog dimenzija koje nedostaju za račun na koji se ne knjiži. |
| Upravljanje projektom i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Projekt** ne može se uređivati na fakturi dobavljača na čekanju kada je kategorija nabave dodijeljena artiklu. |
| Upravljanje projektom i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko okno nedostaje ako niste prijavljeni u projektne operacije Dataverse. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kada knjižite prihod od fakture projekta u zatvorenom slučaju akontacije, pojavljuje se problem jer transakcije na vaučeru ne saldaju. |
| Upravljanje projektom i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procjene nakon knjiženja prijedloga fakture blokira retke ispravljanja od uvoza. |
| Upravljanje projektom i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmjena potpuno fakturiranog zapisa ključne etape ne bi trebala biti moguća. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Sva izvješća o troškovima vidljiva su kada tražite kategoriju u mobilnoj aplikaciji Expense. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netočni iznosi transakcija dobavljača i transakcija poreza na promet knjiže se iz troška kreiranog iz transakcije kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Nevažno upozorenje pojavljuje se kada osvježite **stranicu izvješća** Trošak. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešan privremeni odobravatelj koristi se kada izbrišete privremenog odobravatelja, a zatim ponovno pošaljete izvješće o troškovima putem tijeka rada. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavljuje se pogreška knjiženja povezana s postavljanjem kilometraže. |
