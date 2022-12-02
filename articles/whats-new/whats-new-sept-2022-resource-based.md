---
title: Novosti u studenom 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz rujna 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634796"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.46.0.60
- Upravljanje projektima i računovodstvo u verziji 10.0.29 okruženja aplikacije Dynamics 365 Finance

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Upravljanje prilikama | **Revizija i aktivacija ponuda**<br>Project Operations donosi punu podršku prodajnom procesu. Projektne ponude mogu se aktivirati da predstavljaju stanje u kojem je ponuda samo za čitanje i pregledava se. Aktivirane ponude mogu se revidirati kako bi se stvorile nove ponude koji imaju uvećani broj revizije. Aktivirane projekte ponude ili revizije ponuda mogu se zatvoriti kao dobivene ili izgubljene. | [Aktivacija i revidiranje projektne ponude](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cijene | **Neispunjenje cijena neovisno o vremenskoj zoni**<br>Aplikacija Project Operations uvela je koncept agnostičkog datuma vremenske zone za sve stvarne vrijednosti projekta. Novo polje, **Datum transakcije**, sada je dostupan u recima dnevnika i stvarnim vrijednostima i koristit će se za pohranjivanje datuma kada se transakcija dogodila, ali bez pretvaranja tog datuma u koordinirano univerzalno vrijeme. Taj će se datum koristiti za daljnje procese kao što su neispunjenje cijena i stvaranje faktura. | <p>[Određivanje stopa troškova za procjene i stvarne vrijednosti temeljene na projektu](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Određivanje prodajnih cijena za procjene i stvarne vrijednosti temeljene na projektu](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Naplata i određivanje cijene | **Poništavanje cijena s datumom stupanja na snagu u aplikaciji Project Operations**<br>Poništavanje cijena s datumom stupanja na snagu omogućuje način za poništavanje ili promjenu određenih cijena u cjeniku. | [Poništavanje cijena s datumom stupanja na snagu](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podugovaranje | **Podugovaranje i usklađivanje faktura dobavljača**<br>Ova značajka omogućuje klijentima stvaranje podugovora za kupnju vremena resursa, kategorija troškova i materijala koji se koriste za rad na projektu. Također omogućuje klijentima da u aplikacijama za financije i operacije bilježe fakture dobavljača koji će biti dostupni voditeljima projekata na platformi Dataverse za provjeru. | <p>[Upravljanje podugovorima](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Izrada faktura dobavljača](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Vrijeme i trošak | **Globalni odobravatelj**<br>Ova značajka omogućuje neovisnog dobavljača softvera (ISV) i centralizirano odobrenje, bez obzira na projekt ili status člana tima u projektu. | [Sigurnost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje troškovima | **Mogućnost knjiženja obveze troškova u valuti dobavljača**<br>Ova značajka omogućuje knjiženje izvješća o troškovima u valuti dobavljača za način gotovinskog plaćanja. | [Mogućnost knjiženja obveze troškova u valuti dobavljača](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabava projekta | **Plaćanja dobavljača po načelu „plati kad bude plaćeno”**<br>Ova značajka omogućuje korištenje značajke Plaćanje kad bude plaćeno (PWP) s okruženjima aplikacije Project Operations bez zaliha. Omogućuje blokiranje/zadržavanje plaćanja dobavljača na temelju uvjeta zadržavanja dok se plaćanje ne primi od klijenta. | [Plaćanja dobavljača po načelu „plati kad bude plaćeno”](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabava projekta | **Zahtjevnice za nabavu za projekte**<br>Ova značajka omogućuje korisnicima stvaranje narudžbenica povezanih s projektom u pravnim subjektima u kojima je omogućena integracija aplikacije Project Operations u aplikaciju Dynamics 365 Customer Engagement. Narudžbenice za projekt mogu se koristiti za bilježenje nabave materijala koji nije na zalihama prema projektu od strane osobe odjela nabave. Narudžbenice za projekt neće se sinkronizirati s platformom Dataverse. Međutim, možete upotrijebiti virtualni entitet za prikaz redova narudžbenice za projekt na platformi Dataverse za informacije o voditelju projekata. Trošak fakture dobavljača povezan s projektom integriran je s entitetom Project Actuals na platformi Dataverse. Trošak projekta zabilježen je u glavnoj knjizi projekta putem dnevnika integracije aplikacije Project Operations. | |
|Planiranje i praćenje projekta|**Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja** </br> </br>API za uređivanje obrisa dodjele resursa omogućuje razvojnim programerima da programski odrede napor primatelja zadatka u bilo kojem podržanom rasponu datuma za detaljnije planiranje napora u vremenskim fazama.|[Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanje aplikacije Project Operations za rujan 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| -------------- | ------------------- | ------------|
| Stvarni podaci aplikacije Project Operations (msdyn_actuals) | 1.0.0.15 | Ova karta podržava obradu stvarnih vrijednosti podugovora s aplikacijom Project Operations za scenarije temeljene na resursima. |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Ova karta podržava obradu stvarnih vrijednosti podugovora s aplikacijom Project Operations za scenarije temeljene na resursima. |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ova karta podržava obradu stvarnih vrijednosti podugovora s aplikacijom Project Operations za scenarije temeljene na resursima. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2754422 | Procjene materijala i troškova ne idu u Financije kada se projekti kopiraju na platformu Dataverse. |
| Vrijeme i trošak | 2787409 | Nevažeći odobravatelj može odobriti unos vremena koji nije projekt. |
| Upravljanje prilikama | 2788907 | Ažurirana poruka o pogrešci o provjeri valjanosti jedinstvenosti za retke narudžbe koji uključuju oznake. |
| Vrijeme i trošak | 2842253 | Rukovanje nultom iznimkom za odobrenje vremena. |
| Naplata i određivanje cijene | 2844181 | Neuspjeh u dobivanju ID-a korelacije blokira izradu fakture. |
| Naplata i određivanje cijene | 2876628 | QLD, CLD – Rješenje cjenika procjena treba koristiti naslijeđena polja datumskog raspona cjenika. |
| Podugovaranje | 2893222 | Ako za redak podugovora nije određena uloga, trebalo bi biti moguće odabrati taj redak na članu tima za bilo koju ulogu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se u aplikaciju Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Značajke uključene prema zadanim postavkama u nadolazećem izdanju

Sljedeća tablica navodi značajke koje su uključene prema zadanim postavkama u verziji 10.0.30. Većina značajki koje su automatski uključene može se isključiti u [Upravljanju značajkama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). U budućnosti bi se neke značajke koje su automatski uključene mogle ukloniti iz Upravljanja značajkama i postati obavezne. Ova promjena osigurava da korisnici koriste trenutačnu funkcionalnost, tako da se poboljšanja mogu nadograđivati na trenutačnu funkcionalnost kako se dodaju. Značajke nikada neće biti automatski omogućene za manje od godinu dana, osim ako se ne utvrdi da su bitne.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- |--- |--- |
| Omogućivanje asinkrone operacije kada se korisnik treba prebacivati između sinkronizacije i asinkronizacije | 21. listopada 2022. | 9. travnja 2021. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Potrebna je procjena politike troškova za račune | 21. listopada 2022. | 20. prosinca 2021. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Prikaz popisa izvješća o troškovima koje su izradili delegirani radnici | 21. listopada 2022. | 19. veljače 2020. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Izračun ukupne kilometraže prema poslovnoj godini | 21. listopada 2022. | 10. svibnja 2022. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
