---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479510"
---
# <a name="copy-a-project"></a><span data-ttu-id="d40e1-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="d40e1-103">Copy a project</span></span>

<span data-ttu-id="d40e1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="d40e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d40e1-105">S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** na obrascu **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="d40e1-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="d40e1-106">Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="d40e1-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="d40e1-107">Radnja će kopirati:</span><span class="sxs-lookup"><span data-stu-id="d40e1-107">The action will copy:</span></span>

- <span data-ttu-id="d40e1-108">Svojstva projekta (procijenjeni datum početka kopira se iz izvornog projekta)</span><span class="sxs-lookup"><span data-stu-id="d40e1-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="d40e1-109">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="d40e1-109">The Work breakdown structure</span></span>
- <span data-ttu-id="d40e1-110">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="d40e1-110">Project team members</span></span>
- <span data-ttu-id="d40e1-111">Procjene projekta</span><span class="sxs-lookup"><span data-stu-id="d40e1-111">Project estimates</span></span>
- <span data-ttu-id="d40e1-112">Procjene izdataka za projekt</span><span class="sxs-lookup"><span data-stu-id="d40e1-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="d40e1-113">Svojstava projekta</span><span class="sxs-lookup"><span data-stu-id="d40e1-113">Project properties</span></span>

<span data-ttu-id="d40e1-114">Kada se projekt kopira, kopiraju se vrijednosti u sljedećim poljima:</span><span class="sxs-lookup"><span data-stu-id="d40e1-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="d40e1-115">Ime</span><span class="sxs-lookup"><span data-stu-id="d40e1-115">Name</span></span>
- <span data-ttu-id="d40e1-116">Opis</span><span class="sxs-lookup"><span data-stu-id="d40e1-116">Description</span></span>
- <span data-ttu-id="d40e1-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="d40e1-117">Customer</span></span>
- <span data-ttu-id="d40e1-118">Predložak kalendara</span><span class="sxs-lookup"><span data-stu-id="d40e1-118">Calendar Template</span></span>
- <span data-ttu-id="d40e1-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="d40e1-119">Currency</span></span>
- <span data-ttu-id="d40e1-120">Ugovorena jedinica</span><span class="sxs-lookup"><span data-stu-id="d40e1-120">Contracting Unit</span></span>
- <span data-ttu-id="d40e1-121">Voditelj projekta</span><span class="sxs-lookup"><span data-stu-id="d40e1-121">Project Manager</span></span>
- <span data-ttu-id="d40e1-122">Stanje</span><span class="sxs-lookup"><span data-stu-id="d40e1-122">Status</span></span>
- <span data-ttu-id="d40e1-123">Sveukupno stanje projekta</span><span class="sxs-lookup"><span data-stu-id="d40e1-123">Overall Project Status</span></span>
- <span data-ttu-id="d40e1-124">Komentari</span><span class="sxs-lookup"><span data-stu-id="d40e1-124">Comments</span></span>
- <span data-ttu-id="d40e1-125">Procjene</span><span class="sxs-lookup"><span data-stu-id="d40e1-125">Estimates</span></span>
- <span data-ttu-id="d40e1-126">Predviđeni datum početka</span><span class="sxs-lookup"><span data-stu-id="d40e1-126">Estimated Start Date</span></span>
- <span data-ttu-id="d40e1-127">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="d40e1-127">Finish Date</span></span>
- <span data-ttu-id="d40e1-128">Rad (sati)</span><span class="sxs-lookup"><span data-stu-id="d40e1-128">Effort (Hours)</span></span>
- <span data-ttu-id="d40e1-129">Procijenjena cijena rada</span><span class="sxs-lookup"><span data-stu-id="d40e1-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="d40e1-130">Procijenjeni troškovi</span><span class="sxs-lookup"><span data-stu-id="d40e1-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="d40e1-131">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="d40e1-131">Work breakdown structure</span></span>

<span data-ttu-id="d40e1-132">Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima.</span><span class="sxs-lookup"><span data-stu-id="d40e1-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="d40e1-133">Imenovani resursi mijenjaju se generičkim resursima.</span><span class="sxs-lookup"><span data-stu-id="d40e1-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="d40e1-134">Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati i trajanje zadatka može se promijeniti.</span><span class="sxs-lookup"><span data-stu-id="d40e1-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="d40e1-135">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="d40e1-135">Project team members</span></span>

<span data-ttu-id="d40e1-136">Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi.</span><span class="sxs-lookup"><span data-stu-id="d40e1-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="d40e1-137">Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu.</span><span class="sxs-lookup"><span data-stu-id="d40e1-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="d40e1-138">Imenovani resursi pretvorit će se u generičke članove tima.</span><span class="sxs-lookup"><span data-stu-id="d40e1-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="d40e1-139">Procjene</span><span class="sxs-lookup"><span data-stu-id="d40e1-139">Estimates</span></span>

<span data-ttu-id="d40e1-140">Kada se projekt kopira, iz izvornog projekta kopiraju se i redci za procjenu resursa i troška.</span><span class="sxs-lookup"><span data-stu-id="d40e1-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="d40e1-141">Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="d40e1-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
