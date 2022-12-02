---
title: Novosti u kolovozu 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz kolovoza 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403847"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u kolovozu 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.45.0.53
- Upravljanje projektima i računovodstvo u verziji 10.0.28 okruženja aplikacije Dynamics 365 Finance

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
|   Upravljanje prilikama | 2762089 | Rješavanje pogreške prilikom zatvaranja ugovora kao izgubljenog ako je automatsko spremanje onemogućeno u organizaciji.|
|Planiranje i praćenje projekta | 2767841 | Ažuriranja telemetrije Entitet projekta Stvorite ili ažurirajte scenarije.|
|Naplata i određivanje cijene | 2771072 | Rukovanje iznimkama nulte reference tijekom osvajanja ponude.|
|Naplata i određivanje cijene | 2844181 |Neuspjeh u dobivanju ID-a korelacije i blokiranje izrade fakture.|
|Naplata i određivanje cijene | 2852836 | Nedostaju međukompanijske stvarne vrijednosti za međukompanijske troškove kreirane i odobrene u CE-u.|


### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektom i računovodstvo u aplikaciji Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se na platformu Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
