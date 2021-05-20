---
title: Integracija dvostrukog zapisivanja aplikacije Project Operations
description: U ovoj temi nalazi se pregled integracije dvostrukog pisanja u aplikaciji Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955649"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="594ba-103">Pregled integracije dvostrukog pisanja u aplikaciji Project Operations</span><span class="sxs-lookup"><span data-stu-id="594ba-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="594ba-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="594ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="594ba-105">Project Operations upotrebljavaju [mogućnosti dvostrukog pisanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinkronizaciju podataka u aplikacijama Microsoft Dataverse i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="594ba-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="594ba-106">Na slici u nastavku prikazano je kako se podaci sinkroniziraju kao dio ove integracije između platforme Dataverse i aplikacije Financije.</span><span class="sxs-lookup"><span data-stu-id="594ba-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Pregled tijekova podataka aplikacije Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="594ba-108">Project Operations na platformi Dataverse osigurava suvremeno korisničko sučelje (UI, user interface) i jednostavnu proširivost bez kôda / jednostavnog kôda s pomoću mogućnosti rješenja Power Platform.</span><span class="sxs-lookup"><span data-stu-id="594ba-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="594ba-109">Voditelji projekata, voditelji resursa, članovi projektnog tima i druge osobe ureda za odnose s klijentima, obavljaju svoje aktivnosti u aplikaciji Project Operations na platformi Dataverse.</span><span class="sxs-lookup"><span data-stu-id="594ba-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="594ba-110">Project Operations u aplikaciji Financije pružaju podršku računovodstvu projekta i priznavanju prihoda.</span><span class="sxs-lookup"><span data-stu-id="594ba-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="594ba-111">Project Operations uključuju se u financijski okvir u aplikaciji Financije za izračun poreza na promet, tečajeve valuta, izvješćivanje o financijskoj veličini i još mnogo toga.</span><span class="sxs-lookup"><span data-stu-id="594ba-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="594ba-112">Iskustva računovođe projekta uglavnom se temelje na financijama.</span><span class="sxs-lookup"><span data-stu-id="594ba-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="594ba-113">Integracija aplikacije Project Operations sastoji se od integracije sljedećih komponenata:</span><span class="sxs-lookup"><span data-stu-id="594ba-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="594ba-114">Postavljanje i integracija konfiguracijskih podataka aplikacije Project Operations</span><span class="sxs-lookup"><span data-stu-id="594ba-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="594ba-115">Procjene projekata i stvarni podaci</span><span class="sxs-lookup"><span data-stu-id="594ba-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="594ba-116">Fakture za projekt</span><span class="sxs-lookup"><span data-stu-id="594ba-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="594ba-117">Upravljanje troškom</span><span class="sxs-lookup"><span data-stu-id="594ba-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="594ba-118">Faktura dobavljača</span><span class="sxs-lookup"><span data-stu-id="594ba-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
