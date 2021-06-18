---
title: Sinkronizacija procjena projekta izravno iz usluge Project Service Automation na uslugu Finance and Operations
description: U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju procjena radnih sati na projektu i procjena izdataka za projekt izravno iz sustava Microsoft Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a6955dcd1ebe494e0171c30ac4384089da6a8745
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999707"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="ec8a8-103">Sinkronizacija procjena projekta izravno iz usluge Project Service Automation na uslugu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ec8a8-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ec8a8-104">U ovoj se temi opisuju predlošci i temeljni zadaci koji se upotrebljavaju za sinkronizaciju procjena radnih sati na projektu i procjena izdataka za projekt izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="ec8a8-105">Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="ec8a8-106">Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="ec8a8-107">Tijek podataka s usluge Project Service Automation na Financije</span><span class="sxs-lookup"><span data-stu-id="ec8a8-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="ec8a8-108">Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="ec8a8-109">Predlošci integracije koji su dostupni uz značajku Integracija podataka omogućuju tijek podataka o procjeni sati rada na projektu i procjeni izdataka za projekt iz usluge Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ec8a8-110">Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="ec8a8-111">[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="ec8a8-112">Procjene sati rada na projektu</span><span class="sxs-lookup"><span data-stu-id="ec8a8-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ec8a8-113">Predlošci i zadaci</span><span class="sxs-lookup"><span data-stu-id="ec8a8-113">Template and tasks</span></span>

<span data-ttu-id="ec8a8-114">Kako biste pristupili dostupnim predlošcima, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="ec8a8-115">Predložak u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju procjena radnih sati za projekt iz usluge Project Service Automation u Financije:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ec8a8-116">**Naziv predloška u Integraciji podataka:** Procjene radnih sati za projekt (PSA u Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ec8a8-117">**Naziv zadataka u projektu:**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ec8a8-118">Odnosi transakcija</span><span class="sxs-lookup"><span data-stu-id="ec8a8-118">Transaction relationships</span></span>
    - <span data-ttu-id="ec8a8-119">Procjena troška</span><span class="sxs-lookup"><span data-stu-id="ec8a8-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ec8a8-120">Postavljanje entiteta</span><span class="sxs-lookup"><span data-stu-id="ec8a8-120">Entity set</span></span>

| <span data-ttu-id="ec8a8-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ec8a8-121">Project Service Automation</span></span> | <span data-ttu-id="ec8a8-122">Financije</span><span class="sxs-lookup"><span data-stu-id="ec8a8-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="ec8a8-123">Projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="ec8a8-123">Project tasks</span></span>              | <span data-ttu-id="ec8a8-124">Entitet integracije za procjenu sati rada na projektu</span><span class="sxs-lookup"><span data-stu-id="ec8a8-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="ec8a8-125">Tijek entiteta</span><span class="sxs-lookup"><span data-stu-id="ec8a8-125">Entity flow</span></span>

<span data-ttu-id="ec8a8-126">Procjenama radnih sati za projekt upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao predviđanja radnih sati za projekt.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ec8a8-127">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="ec8a8-127">Prerequisites</span></span>

<span data-ttu-id="ec8a8-128">Prije nego što se dogodi sinkronizacija procjena sati rada na projektu, morate sinkronizirati projekte, projektne zadatke i kategorije transakcija izdataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ec8a8-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="ec8a8-129">Power Query</span></span>

<span data-ttu-id="ec8a8-130">U predlošku procjene radnih sati za projekt morate upotrijebiti uslugu Microsoft Power Query za Excel kako biste izvršili ove zadatke:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="ec8a8-131">Postavite zadani ID modela predviđanja koji će se upotrebljavati kada integracija stvara nova predviđanja radnih sati.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ec8a8-132">U zadatku filtrirajte sve zapise specifične za resurse koji se neće uspjeti integrirati u predviđanja radnih sati.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="ec8a8-133">Filtrirajte sve prazne retke kategorija transakcija.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="ec8a8-134">Neispunjavanje ovog zadatka može dovesti do pogrešnih predviđanja radnih sati.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ec8a8-135">Postavljanje zadanog ID-a modela predviđanja</span><span class="sxs-lookup"><span data-stu-id="ec8a8-135">Set the default forecast model ID</span></span>

<span data-ttu-id="ec8a8-136">Kako biste u predlošku ažurirali zadani ID modela predviđanja, kliknite strelicu **Mapiraj** kako biste otvorili mapiranje.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ec8a8-137">Zatim odaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ec8a8-138">Ako upotrebljavate zadani predložak Procjene radnih sati za projekt (PSA u Fin i Ops), odaberite **Umetnuti uvjet** na popisu **Primijenjeni koraci**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="ec8a8-139">U unosu **Funkcija** zamijenite **O\_forecast** nazivom ID-a modela predviđanja koji bi se trebao upotrijebiti s integracijom.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ec8a8-140">Zadani predložak ima ID modela predviđanja iz pokaznih podataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ec8a8-141">Ako stvarate novi predložak, morate dodati ovaj stupac.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ec8a8-142">U modulu Power Query odaberite **Dodaj uvjetni stupac** i unesite naziv novog stupca, kao što je **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ec8a8-143">Unesite uvjet za stupac, gdje, ako Projektni zadatak ima vrijednost nula , onda \<enter the forecast model ID\>; inače ima vrijednost nula.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="ec8a8-144">Filtriranje zapisa specifičnih za resurse</span><span class="sxs-lookup"><span data-stu-id="ec8a8-144">Filter out resource-specific records</span></span>

<span data-ttu-id="ec8a8-145">Predložak procjena sati rada na projektu (PSA u Fin i Ops) ima zadani filtar koji uklanja sve zapise specifične za resurs.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="ec8a8-146">Ako stvorite vlastiti predložak, morate dodati ovaj filtar.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ec8a8-147">Odaberite vezu **Napredni upit i filtriranje** kako biste filtrirali stupac **msdyn\_islinetask** tako da su uključeni samo zapisi **Netočno**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="ec8a8-148">Filtriranje praznih redaka kategorija transakcija</span><span class="sxs-lookup"><span data-stu-id="ec8a8-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="ec8a8-149">Morate dodati filtar kako biste uklonili sve retke koji imaju prazne kategorije transakcija.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="ec8a8-150">Ovaj je zadatak potreban, bez obzira upotrebljavate li zadani predložak ili stvarate vlastiti.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="ec8a8-151">Ovaj filtar uklanja sve retke sažetka iz usluge Project Service Automation koji mogu uzrokovati netočna predviđanja radnih sati u Financijama.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="ec8a8-152">Odaberite vezu **Napredni upit i filtriranje** kako biste filtrirali prazne zapise u stupcu **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ec8a8-153">Mapiranje predloška u integraciji podataka</span><span class="sxs-lookup"><span data-stu-id="ec8a8-153">Template mapping in Data integration</span></span>

<span data-ttu-id="ec8a8-154">Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="ec8a8-155">Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ec8a8-156">[![Mapiranje zadatka predloška u integraciji podataka](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="ec8a8-157">Procjene izdataka za projekt</span><span class="sxs-lookup"><span data-stu-id="ec8a8-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="ec8a8-158">Predlošci i zadaci</span><span class="sxs-lookup"><span data-stu-id="ec8a8-158">Template and tasks</span></span>

<span data-ttu-id="ec8a8-159">Predložak u nastavku i temeljni zadaci upotrebljavaju se za sinkronizaciju procjena izdataka za projekt iz usluge Project Service Automation u Financije:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="ec8a8-160">**Naziv predloška u Integraciji podataka:** Procjene izdataka za projekt (PSA u Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="ec8a8-161">**Naziv zadataka u projektu:**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="ec8a8-162">Odnosi transakcija</span><span class="sxs-lookup"><span data-stu-id="ec8a8-162">Transaction relationships</span></span> 
    - <span data-ttu-id="ec8a8-163">Procjena troška</span><span class="sxs-lookup"><span data-stu-id="ec8a8-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="ec8a8-164">Postavljanje entiteta</span><span class="sxs-lookup"><span data-stu-id="ec8a8-164">Entity set</span></span>

| <span data-ttu-id="ec8a8-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ec8a8-165">Project Service Automation</span></span> | <span data-ttu-id="ec8a8-166">Financije</span><span class="sxs-lookup"><span data-stu-id="ec8a8-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="ec8a8-167">Veze transakcija</span><span class="sxs-lookup"><span data-stu-id="ec8a8-167">Transaction Connections</span></span>    | <span data-ttu-id="ec8a8-168">Entitet integracije za odnose transakcije projekta</span><span class="sxs-lookup"><span data-stu-id="ec8a8-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="ec8a8-169">Reci procjene</span><span class="sxs-lookup"><span data-stu-id="ec8a8-169">Estimate Lines</span></span>             | <span data-ttu-id="ec8a8-170">Entitet integracije za procjenu izdataka za projekt</span><span class="sxs-lookup"><span data-stu-id="ec8a8-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="ec8a8-171">Tijek entiteta</span><span class="sxs-lookup"><span data-stu-id="ec8a8-171">Entity flow</span></span>

<span data-ttu-id="ec8a8-172">Procjenama izdataka za projekt upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao predviđanja izdataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ec8a8-173">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="ec8a8-173">Prerequisites</span></span>

<span data-ttu-id="ec8a8-174">Prije nego što se dogodi sinkronizacija procjena izdataka na projektu, morate sinkronizirati projekte, projektne zadatke i kategorije transakcija izdataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="ec8a8-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="ec8a8-175">Power Query</span></span>

<span data-ttu-id="ec8a8-176">U predlošku procjene izdataka za projekt morate upotrijebiti modul Power Query kako biste izvršili sljedeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="ec8a8-177">Filtrirajte kako biste uključili samo zapise redaka procjene izdataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="ec8a8-178">Postavite zadani ID modela predviđanja koji će se upotrebljavati kada integracija stvara nova predviđanja radnih sati.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="ec8a8-179">Pretvorite vrste naplata.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-179">Transform the billing types.</span></span>
- <span data-ttu-id="ec8a8-180">Pretvorite vrste transakcija.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="ec8a8-181">Filtriranje kako bi se uključili samo redci procjene izdataka</span><span class="sxs-lookup"><span data-stu-id="ec8a8-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="ec8a8-182">Predložak procjena izdataka za projekt (PSA u Fin i Ops) ima zadani filtar koji pri integraciji uključuje samo retke izdataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="ec8a8-183">Ako stvorite vlastiti predložak, morate dodati ovaj filtar.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="ec8a8-184">Odaberite zadatak **Odnosi transakcije**, a zatim kliknite strelicu **Mapiraj** kako biste otvorili mapiranje.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ec8a8-185">Odaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="ec8a8-186">Filtrirajte stupac **msdyn\_transactiontype1** tako da uključuje samo **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="ec8a8-187">Postavljanje zadanog ID-a modela predviđanja</span><span class="sxs-lookup"><span data-stu-id="ec8a8-187">Set the default forecast model ID</span></span>

<span data-ttu-id="ec8a8-188">Kako biste u predlošku ažurirali zadani ID modela predviđanja, odaberite zadatak **Procjene izdataka** i zatim kliknite strelicu **Mapiraj** kako biste otvorili mapiranje.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="ec8a8-189">Odaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="ec8a8-190">Ako upotrebljavate zadani predložak Procjene izdataka za projekt (PSA u Fin i Ops), u modulu Power Query odaberite prvi **Umetnuti uvjet** iz odjeljka **Primijenjeni koraci**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="ec8a8-191">U unosu **Funkcija** zamijenite **O\_forecast** nazivom ID-a modela predviđanja koji bi se trebao upotrijebiti s integracijom.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="ec8a8-192">Zadani predložak ima ID modela predviđanja iz pokaznih podataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="ec8a8-193">Ako stvarate novi predložak, morate dodati ovaj stupac.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="ec8a8-194">U modulu Power Query odaberite **Dodaj uvjetni stupac** i unesite naziv novog stupca, kao što je **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="ec8a8-195">Unesite uvjet za stupac, gdje, ako vrijednost ID retka Procjene nije nula , onda \<enter the forecast model ID\>; inače ima vrijednost nula.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="ec8a8-196">Pretvaranje vrsta naplata</span><span class="sxs-lookup"><span data-stu-id="ec8a8-196">Transform the billing types</span></span>

<span data-ttu-id="ec8a8-197">Predložak procjene izdataka za projekt (PSA u Fin i Ops) uključuje uvjetni stupac koji se upotrebljava za pretvaranje vrsta naplate primljenih iz usluge Project Service Automation tijekom integracije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ec8a8-198">Ako stvorite vlastiti predložak, morate dodati ovaj uvjetni stupac.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ec8a8-199">Odaberite vezu **Napredni upit i filtriranje**, a zatim odaberite **Dodaj uvjetni stupac**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ec8a8-200">Unesite naziv novog stupca, kao što je **Vrsta naplate**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="ec8a8-201">Zatim unesite sljedeći uvjet:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-201">Then enter the following condition:</span></span>

<span data-ttu-id="ec8a8-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="ec8a8-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="ec8a8-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="ec8a8-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="ec8a8-206">Pretvaranje vrsta transakcija</span><span class="sxs-lookup"><span data-stu-id="ec8a8-206">Transform the transaction types</span></span>

<span data-ttu-id="ec8a8-207">Predložak procjene izdataka za projekt (PSA u Fin i Ops) uključuje uvjetni stupac koji se upotrebljava za pretvaranje vrsta transakcija primljenih iz usluge Project Service Automation tijekom integracije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="ec8a8-208">Ako stvorite vlastiti predložak, morate dodati ovaj uvjetni stupac.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="ec8a8-209">Odaberite vezu **Napredni upit i filtriranje**, a zatim odaberite **Dodaj uvjetni stupac**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="ec8a8-210">Unesite naziv novog stupca, kao što je **Vrsta transakcije**.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="ec8a8-211">Zatim unesite sljedeći uvjet:</span><span class="sxs-lookup"><span data-stu-id="ec8a8-211">Then enter the following condition:</span></span>

<span data-ttu-id="ec8a8-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="ec8a8-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="ec8a8-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="ec8a8-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ec8a8-215">Mapiranje predloška u integraciji podataka</span><span class="sxs-lookup"><span data-stu-id="ec8a8-215">Template mapping in Data integration</span></span>

<span data-ttu-id="ec8a8-216">Sljedeće slike prikazuju primjer mapiranja zadataka predloška u Integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="ec8a8-217">Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="ec8a8-218">[![Mapiranje predloška transakcija procjene troškova](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="ec8a8-219">[![Mapiranje predloška procjene troškova](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="ec8a8-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]