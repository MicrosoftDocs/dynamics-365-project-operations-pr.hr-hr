---
title: Novosti u studenom 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom se članku nalaze informacije o ažuriranjima kvalitete koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/ne zalihama iz rujna 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621319"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.46.0.60
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.29

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Upravljanje prilikama | **Revizija i aktivacija ponuda**<br>Project Operations donosi punu podršku prodajnog procesa. Citati projekta mogu se aktivirati tako da predstavljaju stanje u kojem je ponuda samo za čitanje i pregledava se. Aktivirane ponude mogu se revidirati kako bi se stvorile nove ponude koje imaju povećani broj revizije. Aktivirane ponude projekta ili revizije ponuda mogu se zatvoriti kao osvojene ili izgubljene. | [Aktivacija i revidiranje projektne ponude](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cijene | **Zadana agnostička cijena vremenske zone**<br>Projektne operacije uvele su koncept agnostičkog datuma vremenske zone za sve stvarne projekte. Novo polje, **Datum** transakcije, sada je dostupno u recima i stvarnim vrijednostima temeljnice i koristit će se za pohranu datuma kada je transakcija nastupila, ali bez pretvaranja tog datuma u koordinirano univerzalno vrijeme. Taj će se datum koristiti za silazne procese kao što su zadano određivanje cijena i stvaranje fakture. | <p>[Određivanje stopa troškova za procjene i stvarne procjene temeljene na projektima](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Određivanje prodajnih cijena za procjene i stvarne procjene temeljene na projektima](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Naplata i određivanje cijene | **Datum na snazi nadjačavanja cijena u projektnim operacijama**<br>Nadjačavanja cijena s datumskom učinkovitošću omogućuju nadjačavanje ili promjenu određenih cijena u cjeniku. | [Datum na snazi nadjačavanja cijena](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Ugovaranje o kooperaciji | **Usklađivanje kooperacije i faktura dobavljača**<br>Ova značajka omogućuje kupcima stvaranje podugovaratelja za kupnju vremena resursa, kategorija troškova i materijala koji se koriste za projektni rad. Također omogućuje kupcima da u aplikacijama za financije i operacije zabilježe fakture dobavljača koje će biti dostupne voditeljima projekata za Dataverse provjeru. | <p>[Upravljanje kooperantima](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Izrada faktura dobavljača](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Vrijeme i trošak | **Globalni odobravatelj**<br>Ova značajka omogućuje neovisnog dobavljača softvera (ISV) i centralizirano odobrenje, bez obzira na status projekta ili člana tima u projektu. | [Sigurnost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje troškovima | **Mogućnost knjiženja obveze prema troškovima u valuti dobavljača**<br>Ova značajka omogućuje knjiženje izvješća o troškovima u valuti dobavljača za način gotovinskog plaćanja. | [Mogućnost knjiženja obveze prema troškovima u valuti dobavljača](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabava projekata | **Plaćanje prilikom plaćanja dobavljaču**<br>Ova značajka omogućuje da se značajka Plati kada se plati (PWP) koristi u ne-stock okruženjima Project Operations. Omogućuje blokiranje/zadržavanje plaćanja dobavljača na temelju uvjeta zadržavanja, sve dok uplata ne bude primljena od kupca. | [Plaćanje prilikom plaćanja dobavljaču](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabava projekata | **Zahtjevnice za kupnju projekta**<br>Ova značajka omogućuje korisnicima kreiranje narudžbenica povezanih s projektom u pravnim osobama u kojima je omogućena projektna operacija na Dynamics 365 Customer Engagement integraciji. Narudžbenice za projekt mogu se koristiti za bilježenje nespremne nabave materijala u odnosu na projekt od strane persona Odjela nabave. Narudžbenice za projekt neće se sinkronizirati s programom Dataverse. Međutim, virtualni entitet možete koristiti za površinu redaka narudžbenice projekta za informacije o upravitelju Dataverse projekta. Trošak fakture za dobavljača povezan s projektom integriran je s entitetom Stvarni projekt u sustavu Dataverse. Trošak projekta bilježi se u podprostor projekta pomoću temeljnice Integracija operacija projekta. | |

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

Sljedeća tablica prikazuje karte s dvostrukim pisanjem koje su izmijenjene ili dodane u izdanju Project Operations iz rujna 2022.

| Karta entiteta | Ažurirana verzija | Komentari |
| -------------- | ------------------- | ------------|
| Stvarni podaci aplikacije Project Operations (msdyn_actuals) | 1.0.0.15 | Ova karta podržava obradu stvarnih kooperanta s projektnim operacijama za scenarije temeljene na resursima. |
| Entitet izvoza fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Ova karta podržava obradu stvarnih kooperanta s projektnim operacijama za scenarije temeljene na resursima. |
| Entitet izvoza retka fakture dobavljača projekata integracije aplikacije Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ova karta podržava obradu stvarnih kooperanta s projektnim operacijama za scenarije temeljene na resursima. |

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2754422 | Procjene materijala i troškova ne teku u financije kada se projekti kopiraju u Dataverse sustavu. |
| Vrijeme i trošak | 2787409 | Nevaljani odobravatelj može odobriti unos vremena koji nije projekt. |
| Upravljanje prilikama | 2788907 | Ažurirana poruka o pogrešci o provjeri valjanosti jedinstvenosti za retke naloga koji sadrže zastavice. |
| Vrijeme i trošak | 2842253 | Null rukovanje iznimkama za odobrenje vremena. |
| Naplata i određivanje cijene | 2844181 | Nedostatak dohvaćanja ID-a korelacije blokira stvaranje fakture. |
| Naplata i određivanje cijene | 2876628 | QLD, CLD - Procjena razlučivosti cjenika trebala bi koristiti naslijeđena polja datumskog raspona cjenika. |
| Ugovaranje o kooperaciji | 2893222 | Ako za redak podugovaranja nije navedena uloga, trebalo bi biti moguće odabrati taj redak na članu tima za bilo koju ulogu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu i članku iz [baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Značajke uključene prema zadanim postavkama u nadolazećem izdanju

U sljedećoj su tablici navedene značajke koje su prema zadanim postavkama uključene u verziji 10.0.30. Većina značajki koje su automatski uključene mogu se isključiti u [upravljanju](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) značajkama. Ubuduće bi se neke značajke koje su automatski uključene mogle ukloniti iz upravljanja značajkama i postati obvezne. Ova promjena osigurava da korisnici koriste trenutnu funkcionalnost kako bi se poboljšanja mogla nadovezati na trenutnu funkcionalnost kako se dodaju. Značajke se nikada neće automatski omogućiti za manje od godinu dana, osim ako se utvrdi da su bitne.

| Naziv značajke | Omogući datum | Dodana značajka | Stanje značajke | Modul |
| --- | --- | --- |--- |--- |
| Omogući rad async-a kada se korisnik treba prebacivati između sinkronizacije i Async operacija | 21. listopada 2022. | 9. travnja 2021. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Potrebna procjena politike troškova za primitke | 21. listopada 2022. | 20. prosinca 2021. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Prikaz izvješća o troškovima stvorenih delegiranjem radnika | 21. listopada 2022. | 19. veljače 2020. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
| Izračun ukupnih vrijednosti kilometraže prema poslovna godina | 21. listopada 2022. | 10. svibnja 2022. | Uključeno prema zadanim postavkama | Upravljanje troškovima |
