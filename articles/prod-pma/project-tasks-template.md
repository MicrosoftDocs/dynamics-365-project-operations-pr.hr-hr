---
title: Sinkronizirajte projektne zadatke izravno iz usluge Project Service Automation na uslugu Finance and Operations
description: U ovoj se temi opisuju predložak i temeljni zadatak koji se upotrebljavaju za sinkronizaciju projektnih zadataka izravno iz sustava Microsoft Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288910"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b9db4-103">Sinkronizirajte projektne zadatke izravno iz usluge Project Service Automation na uslugu Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b9db4-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b9db4-104">U ovoj se temi opisuju predložak i temeljni zadatak koji se upotrebljavaju za sinkronizaciju projektnih zadataka izravno iz sustava Dynamics 365 Project Service Automation u uslugu Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b9db4-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b9db4-105">Integracija projektnog zadatka, kategorije transakcija izdataka, procjene sati, procjene izdataka i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="b9db4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b9db4-106">Ako upotrebljavate Enterprise Edition 7.3.0, nakon što instalirate zakrpe KB 4132657 i KB 4132660 moći ćete upotrebljavati predloške za integraciju projektnih zadataka, kategorija transakcija izdataka, procjena sati rada, procjena izdataka i stvarnih podataka te za konfiguraciju funkcije zaključavanja.</span><span class="sxs-lookup"><span data-stu-id="b9db4-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b9db4-107">Ako morate vratiti zadane računovodstvene distribucije, preporučujemo da instalirate i zakrpu KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="b9db4-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="b9db4-108">Integracija stvarnih podataka dostupna je u verziji 8.0.1. i kasnijim.</span><span class="sxs-lookup"><span data-stu-id="b9db4-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="b9db4-109">Tijek podataka s usluge Project Service Automation na Financije</span><span class="sxs-lookup"><span data-stu-id="b9db4-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="b9db4-110">Rješenje za integraciju usluge Project Service Automation u Financije upotrebljava značajku Integracija podataka za sinkronizaciju podataka diljem instanci aplikacija Project Service Automation i Financije.</span><span class="sxs-lookup"><span data-stu-id="b9db4-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b9db4-111">Predložak integracije koji je dostupan sa značajkom Integracija podataka omogućuje protok podataka o projektnim zadacima s usluge Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="b9db4-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b9db4-112">Na slijedećoj slici prikazan je način na koji se podaci sinkroniziraju između usluge Project Service Automation i Financija.</span><span class="sxs-lookup"><span data-stu-id="b9db4-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b9db4-113">[![Tijek podataka za integraciju usluge Project Service Automation s Financijama](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b9db4-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="b9db4-114">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="b9db4-114">Template and task</span></span>

<span data-ttu-id="b9db4-115">Kako biste pristupili predlošku, u centru za administratore platforme Microsoft Power Apps odaberite **Projekti**, a zatim u gornjem desnom kutu odaberite **Novi projekt** za odabir javnih predložaka.</span><span class="sxs-lookup"><span data-stu-id="b9db4-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b9db4-116">Predložak u nastavku i temeljni zadatak upotrebljavaju se za sinkronizaciju projektnih zadataka iz usluge Project Service Automation u Financije:</span><span class="sxs-lookup"><span data-stu-id="b9db4-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b9db4-117">**Naziv predloška u Integraciji podataka:** Projektni zadaci (PSA u Fin i Ops)</span><span class="sxs-lookup"><span data-stu-id="b9db4-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b9db4-118">**Naziv zadatka u projektu:** Projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="b9db4-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="b9db4-119">Prije nego što dođe do sinkronizacije projektnih zadataka, morate sinkronizirati ugovore o projektima i projekte.</span><span class="sxs-lookup"><span data-stu-id="b9db4-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b9db4-120">Postavljanje entiteta</span><span class="sxs-lookup"><span data-stu-id="b9db4-120">Entity set</span></span>

| <span data-ttu-id="b9db4-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b9db4-121">Project Service Automation</span></span> | <span data-ttu-id="b9db4-122">Financije</span><span class="sxs-lookup"><span data-stu-id="b9db4-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="b9db4-123">Zadaci projekta</span><span class="sxs-lookup"><span data-stu-id="b9db4-123">Project Tasks</span></span>              | <span data-ttu-id="b9db4-124">Entitet integracije za projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="b9db4-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b9db4-125">Tijek entiteta</span><span class="sxs-lookup"><span data-stu-id="b9db4-125">Entity flow</span></span>

<span data-ttu-id="b9db4-126">Projektnim zadacima upravlja se u usluzi Project Service Automation, a sinkroniziraju se s Financijama kao projektne aktivnostima.</span><span class="sxs-lookup"><span data-stu-id="b9db4-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b9db4-127">Preduvjeti i postavljanje mapiranja</span><span class="sxs-lookup"><span data-stu-id="b9db4-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="b9db4-128">Prije nego što dođe do sinkronizacije projektnih zadataka, morate sinkronizirati ugovore o projektima i projekte.</span><span class="sxs-lookup"><span data-stu-id="b9db4-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="b9db4-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="b9db4-129">Power Query</span></span>

<span data-ttu-id="b9db4-130">Morate upotrijebiti uslugu Microsoft Power Query za Excel kako biste filtrirali podatke ako je ispunjen ovaj uvjet:</span><span class="sxs-lookup"><span data-stu-id="b9db4-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="b9db4-131">U projektnom zadatku imate zapise specifične za resurse.</span><span class="sxs-lookup"><span data-stu-id="b9db4-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="b9db4-132">Ako morate upotrijebiti modul Power Query, slijedite ovu smjernicu:</span><span class="sxs-lookup"><span data-stu-id="b9db4-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="b9db4-133">Predložak projektnih zadataka (PSA u Fin i Ops) ima zadani filtar koji isključuje zapise specifične za resurse iz projektnog zadatka postavljanjem filtra na stavki **IsLineTask** na **Netočno**.</span><span class="sxs-lookup"><span data-stu-id="b9db4-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="b9db4-134">Ako stvorite vlastiti predložak, morate dodati ovaj filtar.</span><span class="sxs-lookup"><span data-stu-id="b9db4-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b9db4-135">Mapiranje predloška u integraciji podataka</span><span class="sxs-lookup"><span data-stu-id="b9db4-135">Template mapping in Data integration</span></span>

<span data-ttu-id="b9db4-136">Sljedeća slika prikazuje primjer mapiranja zadataka predloška u Integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="b9db4-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="b9db4-137">Mapiranje prikazuje podatke polja koji će se sinkronizirati iz aplikacije Project Service Automation u Financije.</span><span class="sxs-lookup"><span data-stu-id="b9db4-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b9db4-138">[![Mapiranje predloška](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="b9db4-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]