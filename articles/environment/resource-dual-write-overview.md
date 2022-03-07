---
title: Integracija dvostrukog zapisivanja aplikacije Project Operations
description: U ovoj temi nalazi se pregled integracije dvostrukog pisanja u aplikaciji Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998672"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled integracije dvostrukog pisanja u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Project Operations upotrebljavaju [mogućnosti dvostrukog pisanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinkronizaciju podataka u aplikacijama Microsoft Dataverse i Dynamics 365 Finance.

Na slici u nastavku prikazano je kako se podaci sinkroniziraju kao dio ove integracije između platforme Dataverse i aplikacije Financije.

![Pregled tijekova podataka aplikacije Project Operations](./media/ProjectOperationsFlows.jpg)

Project Operations na platformi Dataverse osigurava suvremeno korisničko sučelje (UI, user interface) i jednostavnu proširivost bez kôda / jednostavnog kôda s pomoću mogućnosti rješenja Power Platform. Voditelji projekata, voditelji resursa, članovi projektnog tima i druge osobe ureda za odnose s klijentima, obavljaju svoje aktivnosti u aplikaciji Project Operations na platformi Dataverse.

Project Operations u aplikaciji Financije pružaju podršku računovodstvu projekta i priznavanju prihoda. Project Operations uključuju se u financijski okvir u aplikaciji Financije za izračun poreza na promet, tečajeve valuta, izvješćivanje o financijskoj veličini i još mnogo toga. Iskustva računovođe projekta uglavnom se temelje na financijama.

Integracija aplikacije Project Operations sastoji se od integracije sljedećih komponenata:


- [Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations](resource-dual-write-setup-integration.md) 
- [Procjene projekata i stvarni podaci](resource-dual-write-estimates-actuals.md)
- [Fakture za projekt](resource-dual-write-project-invoice.md)
- [Upravljanje troškom](resource-dual-write-expense.md)
- [Faktura dobavljača](resource-dual-write-vendor-invoice.md)
