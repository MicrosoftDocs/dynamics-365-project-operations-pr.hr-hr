---
title: Novosti u studenom 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovoj temi nalaze se podaci o ažuriranjima kvalitete dostupnim u izdanju za rujan 2021. godine aplikacije Project Operations za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547145"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u studenom 2021. – Project Operations za scenarije temeljene na resursima / bez zaliha

*Odnosi se na: Project Operations za scenarije temeljene na resursu / bez zaliha*

Ova tema odnosi se na sljedeće komponente i verzije aplikacije Dynamics 365 Project Operations:

   - Project Operations u okruženju platforme Microsoft Dataverse verzije 4.14.0.99.
   - Upravljanje projektima i računovodstvo u okruženju aplikacije Dynamics 365 Finance verzije 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane tablične karte dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti na stranici **Dvostruko pisanje** u stupcu **Verzija**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem pri pokretanju karte, slijedite upute u odjeljku [Problem s nedostajućim stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje problema s dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| **Područje značajke** | **Broj reference** | **Ažuriranja kvalitete** |
| --- | --- | --- |
| Vrijeme i trošak | 1811407 | Prilagođeno sigurnosnoj ulozi Odobravatelja projekta za odobrenja unosa troškova. |
| Vrijeme i trošak | 1811438 | Prilagođeno sigurnosnoj ulozi Odobravatelja projekta za otkazivnje odobrenja unosa vremena. |
| Vrijeme i trošak | 2370126 | Ažurirane ikone **Projektni zadatak** i **Uloga** u entitetu **Vremenski unos**. |
| Vrijeme i trošak | 2379879 | Ispravljena je funkcija **Kopiraj tjedan** u unosu vremena kada upotrebljavate aplikaciju Dynamics 365 za telefon. |
| Naplata i određivanje cijene | 2371906 | Ukupni iznos predračuna ne smije se prilagođavati u aplikaciji Project Operations za implementacije koje se temelje na resursima. |
| Naplata i određivanje cijene | 2385802 | Ispravljena je pogreška koja se prikazivala s negativnim stvarnim satima kada su se osvježili ukupni iznosi projekta. |
| Naplata i određivanje cijene | 2389675 | Poboljšano ponašanje potvrde predračuna. Entitet s dugotrajnim poslovima mora uzeti u obzir aktivnosti potrebne za pisanje rezultata potvrde za računovodstvo. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Dynamics 365 Finance

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi transakcija dobavljača i poreza na promet koji su knjiženi iz troškova nastalih transakcijom kreditnom karticom nisu točni. |
| Putovanje i trošak | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Pogrešni redci obračuna stvaraju se tijekom generiranja dnevnika plaćanja. |
| Putovanje i trošak | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Iznosi transakcije poreza na promet koji su knjiženi iz troškova nastalih transakcijom kreditnom karticom nisu točni. |
| Putovanje i trošak | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Brisanje retka troška može potrajati. |
| Projektno računovodstvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Nakon što primijenite KB 4619395, promjena niza brojeva u **Neprekidan** nije podržana i kada knjižite procjenu, dolazi do sljedeće pogreške: „Sustav ne podržava postavljanje 'kontinuiranog' niza brojeva Proj_X.” |
| Projektno računovodstvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Knjiženje fakture dobavljača možda neće uspjeti uz sljedeću poruku o pogrešci: „Transakcije na vaučeru nisu uravnotežene na 17. 5. 2021. (računovodstvena valuta: 0,00 – izvještajna valuta: 0,01)” |
