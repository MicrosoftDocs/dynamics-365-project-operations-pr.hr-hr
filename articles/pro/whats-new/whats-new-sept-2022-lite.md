---
title: Što je novo u rujnu 2022. – Osnovna implementacija aplikacije Project Operations
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju osnovne implementacije aplikacije Microsoft Dynamics 365 Project Operations iz rujna 2022.
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

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.46.0.60

## <a name="features-included-in-this-release"></a>Značajke koje su obuhvaćene ovim izdanjem

| Područje značajke | Naziv značajke | Dodatne informacije |
| --- | --- | --- |
| Upravljanje prilikama | **Revizija i aktivacija ponuda**<br>Project Operations donosi punu podršku prodajnom procesu. Projektne ponude mogu se aktivirati da predstavljaju stanje u kojem je ponuda samo za čitanje i pregledava se. Aktivirane ponude mogu se revidirati kako bi se stvorile nove ponude koji imaju uvećani broj revizije. Aktivirane projekte ponude ili revizije ponuda mogu se zatvoriti kao dobivene ili izgubljene. | [Aktivacija i revidiranje projektne ponude](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cijene | **Neispunjenje cijena neovisno o vremenskoj zoni**<br>Aplikacija Project Operations uvela je koncept agnostičkog datuma vremenske zone za sve stvarne vrijednosti projekta. Novo polje, **Datum transakcije**, sada je dostupan u recima dnevnika i stvarnim vrijednostima i koristit će se za pohranjivanje datuma kada se transakcija dogodila, ali bez pretvaranja tog datuma u koordinirano univerzalno vrijeme. Taj će se datum koristiti za daljnje procese kao što su neispunjenje cijena i stvaranje faktura. | <p>[Određivanje stopa troškova za procjene i stvarne vrijednosti temeljene na projektu](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Određivanje prodajnih cijena za procjene i stvarne vrijednosti temeljene na projektu](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Naplata i određivanje cijene | **Poništavanje cijena s datumom stupanja na snagu u aplikaciji Project Operations**<br>Poništavanje cijena s datumom stupanja na snagu omogućuje način za poništavanje ili promjenu određenih cijena u cjeniku. | [Poništavanje cijena s datumom stupanja na snagu](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Vrijeme i trošak | **Globalni odobravatelj**<br>Ova značajka omogućuje neovisnog dobavljača softvera (ISV) i centralizirano odobrenje, bez obzira na projekt ili status člana tima u projektu. | [Sigurnost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
|Planiranje i praćenje projekta|**Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja** </br> </br>API za uređivanje obrisa dodjele resursa omogućuje razvojnim programerima da programski odrede napor primatelja zadatka u bilo kojem podržanom rasponu datuma za detaljnije planiranje napora u vremenskim fazama.|[Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Ažuriranja kvalitete

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Naplata i određivanje cijene | 2754422 | Procjene materijala i troškova ne idu u aplikaciju Dynamics 365 Finance kada se projekti kopiraju na platformu Dataverse. |
| Vrijeme i trošak | 2787409 | Nevažeći odobravatelj može odobriti unos vremena koji nije projekt. |
| Upravljanje prilikama | 2788907 | Ažurirana poruka o pogrešci o provjeri valjanosti jedinstvenosti za retke narudžbe koji uključuju oznake. |
| Vrijeme i trošak | 2842253 | Rukovanje nultom iznimkom za odobrenje vremena. |
| Naplata i određivanje cijene | 2844181 | Neuspjeh u dobivanju ID-a korelacije blokira izradu fakture. |
| Naplata i određivanje cijene | 2876628 | QLD, CLD – Rješenje cjenika procjena treba koristiti naslijeđena polja datumskog raspona cjenika. |
| Podugovaranje | 2893222 | Ako za redak podugovora nije određena uloga, trebalo bi biti moguće odabrati taj redak na članu tima za bilo koju ulogu. |
