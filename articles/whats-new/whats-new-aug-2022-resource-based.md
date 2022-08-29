---
title: Novosti u kolovozu 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha
description: U ovom se članku nalaze informacije o kvalitetnim ažuriranjima koja su dostupna u izdanju microsofta Dynamics 365 Project Operations za scenarije temeljene na resursima/nenaseljenim resursima u kolovozu 2022.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 112dbb98de09ef342c03d122a29cb8025058e47f
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348094"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novosti u kolovozu 2022. – Project Operations za scenarije koji se temelje na resursu / bez zaliha

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Ovaj se članak odnosi na sljedeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji okruženja Dataverse 4.45.0.53
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja karata s dvostrukim pisanjem u aplikaciji Project Operations

U ovom izdanju nema ažuriranja za karte s dvostrukim pisanjem aplikacije Project Operations. Za trenutačni popis i verzije karata s dvostrukim pisanjem aplikacije Project Operations pogledajte [Verzije karte s dvostrukim pisanjem aplikacije Project Operations](../environment/resource-dual-write-maps.md).

Uvijek pokrenite najnoviju verziju karte u svom okruženju i omogućite sve povezane karte tablica dok ažurirate rješenje za Project Operations Dataverse i verziju rješenja za financije. Neke značajke i mogućnosti možda neće ispravno raditi ako najnovija verzija karte nije aktivirana. Aktivnu verziju karte možete vidjeti u stupcu **Verzija** na stranici **Dvostruko pisanje**. Kako biste aktivirali novu verziju karte, odaberite **Verzije karte tablice**, zatim odaberite najnoviju verziju, a zatim spremite odabranu verziju. Ako ste prilagodili gotovu kartu tablice, ponovno primijenite promjene. Dodatne informacije potražite u članku [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom pokretanja karte, slijedite upute u [odjeljku Nedostajući problemi sa stupcima tablice na kartama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za otklanjanje poteškoća s dvostrukim pisanjem.

## <a name="quality-updates"></a>Ažuriranja kvalitete

### <a name="project-operations-on-dataverse"></a>Project Operations na platformi Dataverse

| Područje značajke | Broj reference | Ažuriranja kvalitete |
| --- | --- | --- |
|   Upravljanje prilikama | 2762089 | Rukovanje pogreškama prilikom zatvaranja ugovora kao izgubljenog ako je automatsko spremanje onemogućeno u operacijskoj mreži.|

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u financijama

Informacije o ispravcima pogrešaka obuhvaćenima ovim ažuriranjem potražite u Microsoft Dynamics članku iz baze podataka o životu (LCS) i pogledajte članak iz [baze znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
