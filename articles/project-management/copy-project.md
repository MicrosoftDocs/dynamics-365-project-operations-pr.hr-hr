---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131784"
---
# <a name="copy-a-project"></a><span data-ttu-id="5ef33-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-103">Copy a project</span></span>

<span data-ttu-id="5ef33-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="5ef33-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ef33-105">S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** iz obrasca **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="5ef33-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="5ef33-106">Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="5ef33-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="5ef33-107">Radnja će kopirati:</span><span class="sxs-lookup"><span data-stu-id="5ef33-107">The action will copy:</span></span>

- <span data-ttu-id="5ef33-108">Svojstava projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-108">Project properties</span></span>
- <span data-ttu-id="5ef33-109">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="5ef33-109">The Work breakdown structure</span></span>
- <span data-ttu-id="5ef33-110">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5ef33-110">Project team members</span></span>
- <span data-ttu-id="5ef33-111">Procjene projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-111">Project estimates</span></span>
- <span data-ttu-id="5ef33-112">Procjene izdataka za projekt</span><span class="sxs-lookup"><span data-stu-id="5ef33-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="5ef33-113">Svojstava projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-113">Project properties</span></span>

<span data-ttu-id="5ef33-114">Kada se projekt kopira, kopiraju se vrijednosti u sljedećim poljima:</span><span class="sxs-lookup"><span data-stu-id="5ef33-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="5ef33-115">Ime</span><span class="sxs-lookup"><span data-stu-id="5ef33-115">Name</span></span>
- <span data-ttu-id="5ef33-116">Opis</span><span class="sxs-lookup"><span data-stu-id="5ef33-116">Description</span></span>
- <span data-ttu-id="5ef33-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="5ef33-117">Customer</span></span>
- <span data-ttu-id="5ef33-118">Predložak kalendara</span><span class="sxs-lookup"><span data-stu-id="5ef33-118">Calendar Template</span></span>
- <span data-ttu-id="5ef33-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="5ef33-119">Currency</span></span>
- <span data-ttu-id="5ef33-120">Ugovorena jedinica</span><span class="sxs-lookup"><span data-stu-id="5ef33-120">Contracting Unit</span></span>
- <span data-ttu-id="5ef33-121">Voditelj projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-121">Project Manager</span></span>
- <span data-ttu-id="5ef33-122">Stanje</span><span class="sxs-lookup"><span data-stu-id="5ef33-122">Status</span></span>
- <span data-ttu-id="5ef33-123">Sveukupno stanje projekta</span><span class="sxs-lookup"><span data-stu-id="5ef33-123">Overall Project Status</span></span>
- <span data-ttu-id="5ef33-124">Komentari</span><span class="sxs-lookup"><span data-stu-id="5ef33-124">Comments</span></span>
- <span data-ttu-id="5ef33-125">Procjene</span><span class="sxs-lookup"><span data-stu-id="5ef33-125">Estimates</span></span>
- <span data-ttu-id="5ef33-126">Predviđeni datum početka</span><span class="sxs-lookup"><span data-stu-id="5ef33-126">Estimated Start Date</span></span>
- <span data-ttu-id="5ef33-127">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="5ef33-127">Finish Date</span></span>
- <span data-ttu-id="5ef33-128">Rad (sati)</span><span class="sxs-lookup"><span data-stu-id="5ef33-128">Effort (Hours)</span></span>
- <span data-ttu-id="5ef33-129">Procijenjena cijena rada</span><span class="sxs-lookup"><span data-stu-id="5ef33-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="5ef33-130">Procijenjeni troškovi</span><span class="sxs-lookup"><span data-stu-id="5ef33-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="5ef33-131">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="5ef33-131">Work breakdown structure</span></span>

<span data-ttu-id="5ef33-132">Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima.</span><span class="sxs-lookup"><span data-stu-id="5ef33-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="5ef33-133">Imenovani resursi mijenjaju se generičkim resursima.</span><span class="sxs-lookup"><span data-stu-id="5ef33-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="5ef33-134">Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati i trajanje zadatka može se promijeniti.</span><span class="sxs-lookup"><span data-stu-id="5ef33-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="5ef33-135">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5ef33-135">Project team members</span></span>

<span data-ttu-id="5ef33-136">Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi.</span><span class="sxs-lookup"><span data-stu-id="5ef33-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="5ef33-137">Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu.</span><span class="sxs-lookup"><span data-stu-id="5ef33-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="5ef33-138">Imenovani resursi pretvorit će se u generičke članove tima.</span><span class="sxs-lookup"><span data-stu-id="5ef33-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="5ef33-139">Procjene</span><span class="sxs-lookup"><span data-stu-id="5ef33-139">Estimates</span></span>

<span data-ttu-id="5ef33-140">Kada se projekt kopira, iz izvornog projekta kopiraju se i redci za procjenu resursa i troška.</span><span class="sxs-lookup"><span data-stu-id="5ef33-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="5ef33-141">Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="5ef33-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>
