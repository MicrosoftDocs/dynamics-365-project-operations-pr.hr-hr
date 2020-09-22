---
title: Napredak projekta i potrošnja troškova
description: Ova tema pruža informacije o tome kako pratiti napredak projekta i potrošnju troškova.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750183"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="20762-103">Napredak projekta i potrošnja troškova</span><span class="sxs-lookup"><span data-stu-id="20762-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="20762-104">Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti.</span><span class="sxs-lookup"><span data-stu-id="20762-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="20762-105">Neke djelatnosti napredak prate na granularnoj razini, dok ga druge prate na višoj razini.</span><span class="sxs-lookup"><span data-stu-id="20762-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="20762-106">Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="20762-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="20762-107">Prikaz praćenja rada</span><span class="sxs-lookup"><span data-stu-id="20762-107">Effort tracking view</span></span>

<span data-ttu-id="20762-108">Prikaz **Praćenje truda** prati napredak zadataka u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="20762-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="20762-109">Uspoređuje stvarne sate rada potrošene na zadatak i planirane sate rada za taj zadatak.</span><span class="sxs-lookup"><span data-stu-id="20762-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="20762-110">PSA koristi sljedeće formule za izračun mjernih podataka o praćenju:</span><span class="sxs-lookup"><span data-stu-id="20762-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="20762-111">Postotak napretka = stvarni rad do danas ÷ planirani rad za zadatak</span><span class="sxs-lookup"><span data-stu-id="20762-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="20762-112">Predviđeni dovršetak (ETC) = planirani rad – stvarni rad do danas</span><span class="sxs-lookup"><span data-stu-id="20762-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="20762-113">Predviđeni dovršetak (EAC) = preostali rad + stvarni rad do danas</span><span class="sxs-lookup"><span data-stu-id="20762-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="20762-114">Predviđeno odstupanje rada = planirani rad – EAC</span><span class="sxs-lookup"><span data-stu-id="20762-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="20762-115">PSA prikazuje predviđanje odstupanja rada u zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="20762-116">Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="20762-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="20762-117">Stoga kasni za rasporedom.</span><span class="sxs-lookup"><span data-stu-id="20762-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="20762-118">Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="20762-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="20762-119">Stoga će se dovršiti prije roka.</span><span class="sxs-lookup"><span data-stu-id="20762-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="20762-120">Ponovno predviđanje rada</span><span class="sxs-lookup"><span data-stu-id="20762-120">Re-projecting effort</span></span>

<span data-ttu-id="20762-121">Uobičajeno je da upravitelj projekta revidira izvorne procjene u zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="20762-122">Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="20762-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="20762-123">Međutim, upraviteljima projekta ne preporučujemo promjenu osnovnih brojeva, jer osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.</span><span class="sxs-lookup"><span data-stu-id="20762-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="20762-124">Postoje dva načina na koje upravitelj projekta može ponovno procijeniti rad na zadacima:</span><span class="sxs-lookup"><span data-stu-id="20762-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="20762-125">Nadjačajte zadani ETC novom procjenom stvarnog preostalog rada zadatka.</span><span class="sxs-lookup"><span data-stu-id="20762-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="20762-126">Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="20762-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="20762-127">Svaki od tih pristupa uzrokuje ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="20762-128">EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.</span><span class="sxs-lookup"><span data-stu-id="20762-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="20762-129">Ponovno predviđanje rada na zadacima sažetka</span><span class="sxs-lookup"><span data-stu-id="20762-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="20762-130">Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti.</span><span class="sxs-lookup"><span data-stu-id="20762-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="20762-131">Bez obzira na to hoće li korisnik izvršiti ponovno predviđanje pomoću preostalog rada ili postotka napretka na zadacima sažetka, pokreće se sljedeći skup izračuna:</span><span class="sxs-lookup"><span data-stu-id="20762-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="20762-132">Izračunačava se EAC, ETC i postotak napretka na zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="20762-133">Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="20762-134">Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova.</span><span class="sxs-lookup"><span data-stu-id="20762-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="20762-135">ETC i postotak napretka za zahvaćene podređene zadatke lisnih čvorova ponovno se izračunavaju na temelju vrijednosti EAC-a.</span><span class="sxs-lookup"><span data-stu-id="20762-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="20762-136">To rezultira novim predviđanjem za odstupanje rada zadatka.</span><span class="sxs-lookup"><span data-stu-id="20762-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="20762-137">Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.</span><span class="sxs-lookup"><span data-stu-id="20762-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="20762-138">Prikaz praćenja troškova</span><span class="sxs-lookup"><span data-stu-id="20762-138">Cost tracking view</span></span> 

<span data-ttu-id="20762-139">Prikaz **Praćenje troškova** uspoređuje stvarni trošak koji je potrošen na zadatak s planiranim troškom zadatka.</span><span class="sxs-lookup"><span data-stu-id="20762-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="20762-140">Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procjena troškova.</span><span class="sxs-lookup"><span data-stu-id="20762-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="20762-141">PSA koristi sljedeće formule za izračun mjernih podataka o praćenju:</span><span class="sxs-lookup"><span data-stu-id="20762-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="20762-142">Postotak potrošenog troška = stvarni trošak do danas ÷ planirani trošak za zadatak</span><span class="sxs-lookup"><span data-stu-id="20762-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="20762-143">Trošak za dovršetak (CTC) = planirani trošak – stvarni trošak do danas</span><span class="sxs-lookup"><span data-stu-id="20762-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="20762-144">EAC = CTC + stvarni trošak do danas</span><span class="sxs-lookup"><span data-stu-id="20762-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="20762-145">Predviđeno odstupanje troškova = planirani trošak – EAC</span><span class="sxs-lookup"><span data-stu-id="20762-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="20762-146">Predviđanje odstupanja troškova prikazuje se u zadatku.</span><span class="sxs-lookup"><span data-stu-id="20762-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="20762-147">Ako je EAC veći od planiranog troška, predviđa se da će zadatak imati veći trošak nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="20762-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="20762-148">Stoga postoji tendencija premašivanja proračuna.</span><span class="sxs-lookup"><span data-stu-id="20762-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="20762-149">Ako je EAC manji od planiranog troška, predviđa se da će zadatak imati manji trošak nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="20762-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="20762-150">Stoga postoji tendencija neiskorištavanja proračuna.</span><span class="sxs-lookup"><span data-stu-id="20762-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="20762-151">Ponovno predvđanje troškova upravitelja projekta</span><span class="sxs-lookup"><span data-stu-id="20762-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="20762-152">Kada se rad ponovno predvidi, CTC, EAC, postotak potrošenog troška i predviđeno odstupanje troška ponovno se izračunavaju u prikazu **Praćenje troškova**.</span><span class="sxs-lookup"><span data-stu-id="20762-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="20762-153">Sažetak statusa projekta</span><span class="sxs-lookup"><span data-stu-id="20762-153">Project status summary</span></span>

<span data-ttu-id="20762-154">Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora.</span><span class="sxs-lookup"><span data-stu-id="20762-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="20762-155">Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.</span><span class="sxs-lookup"><span data-stu-id="20762-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="20762-156">Polja sažetka statusa</span><span class="sxs-lookup"><span data-stu-id="20762-156">Status summary fields</span></span>

<span data-ttu-id="20762-157">Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta.</span><span class="sxs-lookup"><span data-stu-id="20762-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="20762-158">Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="20762-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="20762-159">Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="20762-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="20762-160">Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="20762-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="20762-161">Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja.</span><span class="sxs-lookup"><span data-stu-id="20762-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="20762-162">Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**.</span><span class="sxs-lookup"><span data-stu-id="20762-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="20762-163">Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.</span><span class="sxs-lookup"><span data-stu-id="20762-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
