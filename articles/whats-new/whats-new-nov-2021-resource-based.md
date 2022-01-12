---
title: Novosti u studenom 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: Ovaj tema pruža informacije o ažuriranjima kvalitete koja su dostupna u izdanju projektnih operacija u studenom 2021. za scenarije temeljene na resursima / nesuglađenima.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942876"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2021. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ovaj tema primjenjuje se na sljedeće Microsoftove komponente i verzije Dynamics 365 Project Operations:

- Projektne operacije u Dataverse okruženju verzije 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.22

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

U ovo izdanje uključene su sljedeće značajke:

- Sučelja za programiranje aplikacija za planiranje projekata (API-je) sada podržavaju mogućnost stvaranja i brisanja grupa projekata.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Uvijek pokrenite najnoviju verziju karte u okruženju i omogućite sve povezane karte tablica prilikom ažuriranja rješenja Operacije projekta Dataverse i verzije financijskog rješenja. Neke značajke i mogućnosti možda neće ispravno funkcionirati ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako prilikom pokretanja karte naiđete na problem, slijedite upute u [odjeljku Stupci tablice koji nedostaju u odjeljku Karte](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-in-dataverse"></a>Projektne operacije u programu Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2240080 | **Polje Uvjeti plaćanja ne smije se** duplicirati na pro forma fakturi. |
| Naplata i određivanje cijene | 2358236 | Ispravak fakture mora omogućiti ispravke koji imaju retke nulte cijene. |
| Upravljanje resursima | 2410072 | Dopustite postavljanje resursa koji je zadatku dodijeljen kao voditelj projekta. |
| Naplata i određivanje cijene | 2430234 | Riješite problem izračuna troškova i performansi. |
| Vrijeme i trošak | 2436978 | Dopusti unos vremena u obliku hh:mm. |
| Naplata i određivanje cijene | 2448623 | Dopustite ažuriranje cjenika nakon povezivanja s organizacijskom jedinicom. |
| Vrijeme i trošak | 2460396 | Dopustite brisanje unosa vremena čišćenjem ćelije. |
| Naplata i određivanje cijene | 2467386 | Dopustite brisanje projekta koji ima zadatak, čak i kada je zadatak povezan s osvojenom ponudom. |
| Vrijeme i trošak | 2461744 | **Prikaz Moje neuspjelo odobrenje sadrži samo** odobrenja projekta u fazi **Poslano**. |
| Vrijeme i trošak | 2464082 | Uklonite vezu iz odobrenja projekta u skup odobrenja kada se podudaranje ciljnog statusa podudara. |
| Vrijeme i trošak | 2468108 | Zadatak Raspored ne bi trebao postaviti **status** obrade za skup odobravanja. |
| Vrijeme i trošak | 2471503 | Izbrišite skupove odobrenja stare sedam dana. |
| Naplata i određivanje cijene | 2480687 | Referenca retka ponude ne smije se ukloniti prilikom stvaranja prekretnice retka ponude. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje projektom i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani iznosi dobavljača u transakcijama troškova projekta nisu prikazani na popisu transakcija. |
| Upravljanje projektom i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača prekida se kada je uključena integracija faktura dobavljača. |
| Upravljanje projektom i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uvjeti plaćanja na projektnim fakturama ne funkcioniraju prema očekivanjima. |
| Upravljanje projektom i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se oslobodi zadržavanje dobavljača, knjiženje vaučera ima dodatne retke koji nisu točni. |
| Upravljanje projektom i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kada se proknjiži temeljnica integracije operacija projekata, ona ne uspijeva zbog nedostajućih dimenzija za račun na koji se ne knjiži. |
| Upravljanje projektom i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Karticu Projekt** nije moguće uređivati na fakturi dobavljača na čekanju kada je kategorija nabave dodijeljena artiklu. |
| Upravljanje projektom i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigacijsko okno nedostaje ako niste prijavljeni u projektne operacije Dataverse. |
| Upravljanje projektom i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kada knjižite prihod od projektne fakture u slučaju zatvorenog držača, pojavljuje se problem jer transakcije na vaučeru ne saldo. |
| Upravljanje projektom i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procjene nakon knjiženja prijedloga fakture blokira retke ispravka od uvoza. |
| Upravljanje projektom i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmjena potpuno fakturiranog zapisa o prekretnici ne bi trebala biti moguća. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Sva izvješća o troškovima vidljiva su kada tražite kategoriju u mobilnoj aplikaciji Trošak. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netočni iznosi na transakcijama dobavljača i transakcijama poreza na promet knjižiju se iz troška kreiranog iz transakcije kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Prilikom osvježavanja stranice izvješća o troškovima pojavljuje se nevažno **upozorenje**. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešan privremeni odobravatelj koristi se kada izbrišete privremenog odobravatelja, a zatim ponovno poslate izvješće o troškovima kroz tijek rada. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Pojavljuje se pogreška pri knjiženju koja je povezana s postavljanjem kilometraže. |
