---
title: Što je novo u rujnu 2022. – Osnovna implementacija aplikacije Project Operations
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima dostupnima u izdanju implementacije sustava Microsoft Dynamics 365 Project Operations Lite u rujnu 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634843"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Što je novo u rujnu 2022. – Osnovna implementacija aplikacije Project Operations

_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.46.0.60

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Upravljanje prilikama | **Revizija i aktivacija ponuda**<br>Project Operations donosi punu podršku prodajnog procesa. Citati projekta mogu se aktivirati tako da predstavljaju stanje u kojem je ponuda samo za čitanje i pregledava se. Aktivirane ponude mogu se revidirati kako bi se stvorile nove ponude koje imaju povećani broj revizije. Aktivirane ponude projekta ili revizije ponuda mogu se zatvoriti kao osvojene ili izgubljene. | [Aktivacija i revidiranje projektne ponude](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cijene | **Zadana agnostička cijena vremenske zone**<br>Projektne operacije uvele su koncept agnostičkog datuma vremenske zone za sve stvarne projekte. Novo polje, **Datum** transakcije, sada je dostupno u recima i stvarnim vrijednostima temeljnice i koristit će se za pohranu datuma kada je transakcija nastupila, ali bez pretvaranja tog datuma u koordinirano univerzalno vrijeme. Taj će se datum koristiti za silazne procese kao što su zadano određivanje cijena i stvaranje fakture. | <p>[Određivanje stopa troškova za procjene i stvarne procjene temeljene na projektima](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Određivanje prodajnih cijena za procjene i stvarne procjene temeljene na projektima](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Naplata i određivanje cijene | **Datum na snazi nadjačavanja cijena u projektnim operacijama**<br>Nadjačavanja cijena s datumskom učinkovitošću omogućuju nadjačavanje ili promjenu određenih cijena u cjeniku. | [Datum na snazi nadjačavanja cijena](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Vrijeme i trošak | **Globalni odobravatelj**<br>Ova značajka omogućuje neovisnom dobavljaču softvera (ISV) i centralizirano odobrenje, bez obzira na status projekta ili člana tima u projektu. | [Sigurnost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
|Planiranje i praćenje projekta|**Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja** </br> </br>API za uređivanje konture dodjele resursa omogućuje programerima programsko određivanje napora davatelja zadataka u bilo kojem podržanom datumskom rasponu za detaljnije planiranje napora u fazama.|[Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2754422 | Procjene materijala i troškova ne teku u Dynamics 365 Finance kada se projekti kopiraju u Dataverse. |
| Vrijeme i trošak | 2787409 | Nevaljani odobravatelj može odobriti unos vremena koji nije projekt. |
| Upravljanje prilikama | 2788907 | Ažurirana poruka o pogrešci o provjeri valjanosti jedinstvenosti za retke naloga koji sadrže zastavice. |
| Vrijeme i trošak | 2842253 | Null rukovanje iznimkama za odobrenje vremena. |
| Naplata i određivanje cijene | 2844181 | Nedostatak dohvaćanja ID-a korelacije blokira stvaranje fakture. |
| Naplata i određivanje cijene | 2876628 | QLD, CLD - Procjena razlučivosti cjenika trebala bi koristiti naslijeđena polja datumskog raspona cjenika. |
| Ugovaranje o kooperaciji | 2893222 | Ako za redak podugovaranja nije navedena uloga, trebalo bi biti moguće odabrati taj redak na članu tima za bilo koju ulogu. |
