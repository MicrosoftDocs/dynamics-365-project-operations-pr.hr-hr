---
title: Pregled usluge Project Service Automation
description: U ovoj se temi nalaze informacije o rješenju za integraciju usluge Dynamics 365 Project Service Automation u aplikaciju Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073529"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="8005a-103">Pregled usluge Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8005a-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8005a-104">Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Dynamics 365 Finance i Dynamics 365 Project Service Automation preko platforme Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8005a-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="8005a-105">Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek projekata, ugovore o projektu, retke ugovora o projektu, prekretnice u retku ugovora o projektu, projektne zadatke, kategorije transakcija izdataka, procjene sati i izdataka od usluge Project Service Automation do Financija.</span><span class="sxs-lookup"><span data-stu-id="8005a-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8005a-106">Ako upotrebljavate verziju 7.3.0, morate instalirati zakrpu KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="8005a-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="8005a-107">Tada ćete moći integrirati projekte s fiksnom cijenom.</span><span class="sxs-lookup"><span data-stu-id="8005a-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="8005a-108">Ako upotrebljavate verziju 7.3.0 i transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati zakrpu KB 4345320 kako biste te naknade uključili u fakturu projekta.</span><span class="sxs-lookup"><span data-stu-id="8005a-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="8005a-109">Ako upotrebljavate verziju 8.0, moći ćete upotrebljavati integraciju projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="8005a-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="8005a-110">Ako upotrebljavate verziju 8.0.1 ili noviju, moći ćete sinkronizirati stvarne podatke.</span><span class="sxs-lookup"><span data-stu-id="8005a-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="8005a-111">Kako biste mogli integrirati Financije usluge Project Service Automation, morate konfigurirati parametre integracije usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="8005a-112">Dodatne informacije potražite u odjeljku [Parametri integracije usluge Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8005a-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="8005a-113">Ovo rješenje integracije omogućuje izravnu sinkronizaciju u sljedećim scenarijima:</span><span class="sxs-lookup"><span data-stu-id="8005a-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="8005a-114">Održavajte ugovore o projektu u usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-115">Stvarajte projekte na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-116">Održavajte retke ugovora o projektu na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-117">Održavajte prekretnice redaka ugovora o projektu na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-118">Održavajte projektne zadatke na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-119">Održavajte kategorije transakcija izdatka u Financijama i sinkronizirajte ih izravno s Financija na uslugu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="8005a-120">Stvarajte procjene sati za projekt na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-121">Stvarajte procjene izdataka za projekt na usluzi Project Service Automation i sinkronizirajte ih s Financijama izravno iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8005a-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="8005a-122">Stvorite vrijeme za projekt, izdatke i stvarne naknade na usluzi Project Service Automation i stvorite projektne transakcije u dnevniku o integraciji usluge Project Service Automation tako da se mogu objaviti u Financijama.</span><span class="sxs-lookup"><span data-stu-id="8005a-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="8005a-123">Sinkronizacija podataka</span><span class="sxs-lookup"><span data-stu-id="8005a-123">Data synchronization</span></span>

<span data-ttu-id="8005a-124">Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju kao dio integracije između usluge Project Service Automation i Financija.</span><span class="sxs-lookup"><span data-stu-id="8005a-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="8005a-125">Trenutačno nisu dostupni svi predlošci.</span><span class="sxs-lookup"><span data-stu-id="8005a-125">Not all templates are currently available.</span></span> <span data-ttu-id="8005a-126">Predlošci će se objaviti čim budu dovršeni.</span><span class="sxs-lookup"><span data-stu-id="8005a-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="8005a-127">[![Integracija usluge Project Service Automation s Financijama](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="8005a-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="8005a-128">Preduvjeti sustava za financije</span><span class="sxs-lookup"><span data-stu-id="8005a-128">System requirements for Finance</span></span>

<span data-ttu-id="8005a-129">Kako biste upotrebljavali rješenje za integraciju usluge Project Service Automation s Financijama, morate instalirati verziju Enterprise Edition 7.3 s ažuriranjem platforme 12 ili novijim.</span><span class="sxs-lookup"><span data-stu-id="8005a-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="8005a-130">Preduvjeti sustava za uslugu Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8005a-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="8005a-131">Kako biste upotrebljavali rješenje za integraciju usluge Project Service Automation s Financijama, morate instalirati sljedeće komponente:</span><span class="sxs-lookup"><span data-stu-id="8005a-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="8005a-132">Dynamics 365 Project Service Automation, verzija 9.0.0.0 ili noviji</span><span class="sxs-lookup"><span data-stu-id="8005a-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="8005a-133">Mogućnost gotovinskog rješenja za aplikaciju Dynamics 365 Sales, verzija 1.14.0.0 (v14) ili novija</span><span class="sxs-lookup"><span data-stu-id="8005a-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="8005a-134">Rješenje Project Service Automation u Financije za aplikaciju Dynamics 365 Project Service Automation verzija 1.0.0.0 ili novija</span><span class="sxs-lookup"><span data-stu-id="8005a-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="8005a-135">Instalirajte rješenje za integraciju usluge Project Service Automation u Financije u svojoj instanci Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8005a-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="8005a-136">Preuzmite rješenje za integraciju usluge Project Service Automation u Financije u [Microsoftovu centru za preuzimanje](https://www.microsoft.com/download/details.aspx?id=57016) i slijedite upute koje ste dobili uz rješenje.</span><span class="sxs-lookup"><span data-stu-id="8005a-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
