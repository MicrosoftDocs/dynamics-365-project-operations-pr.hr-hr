---
title: Novosti u svibnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha
description: U ovom članku nalaze se informacije o ažuriranjima kvalitete dostupnima u izdanju aplikacije Microsoft Dynamics 365 Project Operations iz svibnja 2022. za scenarije koji se temelje na resursu / bez zaliha.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921385"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u svibnju 2022. – Project Operations za scenarije temeljene na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj članak odnosi se na sljedeće komponente i verzije aplikacije Microsoft Dynamics 365 Project Operations:

- Project Operations u okruženju platforme Dataverse verzije 4.42.0.70
- Upravljanje projektima i računovodstvo u verziji 10.0.26 okruženja aplikacije Dynamics 365 Finance

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablice dok ažurirate svoje rješenje Project Operations Dataverse i verziju rješenja Financija. Određene značajke i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija karte. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem s pokretanjem karte, slijedite upute u odjeljku [Problem nedostatka stupaca tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rješavanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete
### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
| Upravljanje resursima | 2634019 | Poboljšane poruke o pogrešci za poslovne provjere valjanosti prilikom dodavanja generičkih članova tima kao resursa. |
| Planiranje i praćenje projekta | 2648515 | Ograničena ažuriranja u entitetima planiranja **ownerid**, **state** i **status**. |
| Naplata i određivanje cijene | 2653167 | Decimalni razdjelnik rešetke **Procjene** mora slijediti postavke formata u **Osobnim opcijama**. |
| Naplata i određivanje cijene| 2662251 | Vrijednosti u poljima **Ispravljena jedinica** i **Grupa jedinica** zadaju se kada se stvaraju zapisi u procjenama materijala. |
| Naplata i određivanje cijene| 2571408 | Stvarne vrijednosti nenaplaćene prodaje označene su brojem predračuna prilikom izrade nacrta fakture. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u aplikaciji Dynamics 365 Finance

Za informacije o ispravcima uključenima u ovo ažuriranje prijavite se na platformu Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak iz baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
