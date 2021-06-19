---
title: Kopiranje projekta
description: U ovoj temi nalaze se informacije o kopiranju projekata u aplikaciji Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091245"
---
# <a name="copy-a-project"></a><span data-ttu-id="e1169-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-103">Copy a project</span></span>

<span data-ttu-id="e1169-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="e1169-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e1169-105">S pomoću aplikacije Dynamics 365 Project Operations možete brzo graditi nove projekte odabirom mogućnosti **Kopiraj projekt** na obrascu **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="e1169-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="e1169-106">Kako biste kopirali projekt, otvorite projekt koji želite kopirati, a zatim odaberite **Kopiraj projekt**.</span><span class="sxs-lookup"><span data-stu-id="e1169-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="e1169-107">Radnja će kopirati sljedeće:</span><span class="sxs-lookup"><span data-stu-id="e1169-107">The action will copy the following:</span></span>

- <span data-ttu-id="e1169-108">Svojstava projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-108">Project properties</span></span> 
- <span data-ttu-id="e1169-109">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="e1169-109">Work breakdown structure</span></span>
- <span data-ttu-id="e1169-110">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="e1169-110">Project team members</span></span>
- <span data-ttu-id="e1169-111">Procjene projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-111">Project estimates</span></span>
- <span data-ttu-id="e1169-112">Procjene izdataka za projekt</span><span class="sxs-lookup"><span data-stu-id="e1169-112">Project expense estimates</span></span>
- <span data-ttu-id="e1169-113">Procjene materijala za projekt</span><span class="sxs-lookup"><span data-stu-id="e1169-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="e1169-114">Svojstava projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-114">Project properties</span></span>

<span data-ttu-id="e1169-115">Kada se projekt kopira, kopiraju se vrijednosti u sljedećim poljima:</span><span class="sxs-lookup"><span data-stu-id="e1169-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="e1169-116">Ime</span><span class="sxs-lookup"><span data-stu-id="e1169-116">Name</span></span>
- <span data-ttu-id="e1169-117">Opis</span><span class="sxs-lookup"><span data-stu-id="e1169-117">Description</span></span>
- <span data-ttu-id="e1169-118">Klijent</span><span class="sxs-lookup"><span data-stu-id="e1169-118">Customer</span></span>
- <span data-ttu-id="e1169-119">Predložak kalendara</span><span class="sxs-lookup"><span data-stu-id="e1169-119">Calendar Template</span></span>
- <span data-ttu-id="e1169-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="e1169-120">Currency</span></span>
- <span data-ttu-id="e1169-121">Ugovorena jedinica</span><span class="sxs-lookup"><span data-stu-id="e1169-121">Contracting Unit</span></span>
- <span data-ttu-id="e1169-122">Voditelj projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-122">Project Manager</span></span>
- <span data-ttu-id="e1169-123">Stanje</span><span class="sxs-lookup"><span data-stu-id="e1169-123">Status</span></span>
- <span data-ttu-id="e1169-124">Sveukupno stanje projekta</span><span class="sxs-lookup"><span data-stu-id="e1169-124">Overall Project Status</span></span>
- <span data-ttu-id="e1169-125">Komentari</span><span class="sxs-lookup"><span data-stu-id="e1169-125">Comments</span></span>
- <span data-ttu-id="e1169-126">Procjene</span><span class="sxs-lookup"><span data-stu-id="e1169-126">Estimates</span></span>
- <span data-ttu-id="e1169-127">Procijenjeni datum početka: Ovo je datum kada je projekt stvoren iz kopije.</span><span class="sxs-lookup"><span data-stu-id="e1169-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="e1169-128">Procijenjeni datum završetka: Ovaj se datum prilagođava na temelju datuma početka novog projekta izrađenog iz kopije.</span><span class="sxs-lookup"><span data-stu-id="e1169-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="e1169-129">Rad (sati)</span><span class="sxs-lookup"><span data-stu-id="e1169-129">Effort (Hours)</span></span>
- <span data-ttu-id="e1169-130">Procijenjena cijena rada</span><span class="sxs-lookup"><span data-stu-id="e1169-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="e1169-131">Procijenjena cijena troška</span><span class="sxs-lookup"><span data-stu-id="e1169-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="e1169-132">Procijenjena cijena materijala</span><span class="sxs-lookup"><span data-stu-id="e1169-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="e1169-133">Projekt kopiranja dugotrajan je postupak.</span><span class="sxs-lookup"><span data-stu-id="e1169-133">Copy project is a long running operation.</span></span> <span data-ttu-id="e1169-134">Kopiraju se i projektni zapisi, njihovi relevantni atributi i mnogi povezani entiteti.</span><span class="sxs-lookup"><span data-stu-id="e1169-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="e1169-135">Zbog dugotrajnosti postupka, nakon započinjanja kopiranja, ciljna stranica projekta zaključava se kako se ne bi mogla uređivati dok se postupak kopiranja ne dovrši.</span><span class="sxs-lookup"><span data-stu-id="e1169-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="e1169-136">Strukturna analiza rada</span><span class="sxs-lookup"><span data-stu-id="e1169-136">Work breakdown structure</span></span>

<span data-ttu-id="e1169-137">Kada se projekt kopira, kopira se cijela strukturna analiza rada ispunjena resursima.</span><span class="sxs-lookup"><span data-stu-id="e1169-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="e1169-138">Imenovani resursi mijenjaju se generičkim resursima.</span><span class="sxs-lookup"><span data-stu-id="e1169-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="e1169-139">Ako imenovani resursi nemaju isto radno vrijeme kao generički resurs, raspored će se ponovno izračunati i trajanje zadatka može se promijeniti.</span><span class="sxs-lookup"><span data-stu-id="e1169-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="e1169-140">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="e1169-140">Project team members</span></span>

<span data-ttu-id="e1169-141">Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi.</span><span class="sxs-lookup"><span data-stu-id="e1169-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="e1169-142">Zadaci generičkih resursa također se zadržavaju onakvi kakvi su bili u izvornom projektu.</span><span class="sxs-lookup"><span data-stu-id="e1169-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="e1169-143">Imenovani resursi pretvorit će se u generičke članove tima.</span><span class="sxs-lookup"><span data-stu-id="e1169-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="e1169-144">Procjene</span><span class="sxs-lookup"><span data-stu-id="e1169-144">Estimates</span></span>

<span data-ttu-id="e1169-145">Kada se projekt kopira, redci procjene resursa, troškova i materijala kopiraju se iz izvornog projekta.</span><span class="sxs-lookup"><span data-stu-id="e1169-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="e1169-146">Za informacije o načinu programskog pristupanja aplikaciji Copy Project, pogledajte odjeljak [Razvoj predložaka projekata s pomoću aplikacije Copy Project](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="e1169-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
