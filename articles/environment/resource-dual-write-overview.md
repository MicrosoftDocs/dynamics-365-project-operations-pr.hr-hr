---
title: Integracija dvostrukog zapisivanja aplikacije Project Operations
description: U ovom se članku daje pregled integracije dvostrukog pisanja project operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927963"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled integracije dvostrukog pisanja u aplikaciji Project Operations

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_

Project Operations koristi [mogućnosti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) dvostrukog pisanja za sinkronizaciju podataka na svim Microsoft Dataverse Dynamics 365 Finance i Dynamics 365 Finance.

Na slici u nastavku prikazano je kako se podaci sinkroniziraju kao dio ove integracije između platforme Dataverse i aplikacije Financije.

![Pregled tijekova podataka aplikacije Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations na platformi Dataverse osigurava suvremeno korisničko sučelje (UI, user interface) i jednostavnu proširivost bez kôda / jednostavnog kôda s pomoću mogućnosti rješenja Power Platform. Voditelji projekata, voditelji resursa, članovi projektnog tima i druge osobe ureda za odnose s klijentima, obavljaju svoje aktivnosti u aplikaciji Project Operations na platformi Dataverse.

Project Operations u aplikaciji Financije pružaju podršku računovodstvu projekta i priznavanju prihoda. Project Operations uključuju se u financijski okvir u aplikaciji Financije za izračun poreza na promet, tečajeve valuta, izvješćivanje o financijskoj veličini i još mnogo toga. Iskustva računovođe projekta uglavnom se temelje na financijama.

Integracija aplikacije Project Operations sastoji se od integracije sljedećih komponenata:


- [Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations](resource-dual-write-setup-integration.md) 
- [Procjene projekata i stvarni podaci](resource-dual-write-estimates-actuals.md)
- [Fakture za projekt](resource-dual-write-project-invoice.md)
- [Upravljanje troškom](resource-dual-write-expense.md)
- [Faktura dobavljača](resource-dual-write-vendor-invoice.md)
