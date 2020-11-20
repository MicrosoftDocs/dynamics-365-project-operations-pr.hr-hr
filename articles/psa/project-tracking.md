---
title: Napredak projekta i cijena troška
description: U ovoj temi nalaze se informacije o načinu praćenja napretka projekta i potrošnje troškova.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0793ee0c75bcbdde0fd92a16634457f73f872b5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120624"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="76881-103">Napredak projekta i cijena troška</span><span class="sxs-lookup"><span data-stu-id="76881-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="76881-104">Potreba praćenja napretka u odnosu na raspored razlikuje se ovisno o djelatnosti.</span><span class="sxs-lookup"><span data-stu-id="76881-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="76881-105">Neke djelatnosti napredak prate na granularnoj razini, dok ga druge prate na višoj razini.</span><span class="sxs-lookup"><span data-stu-id="76881-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="76881-106">Ova tema pokazuje kako postaviti raspored da biste ispunili zahtjeve tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="76881-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="76881-107">Prikaz praćenja rada</span><span class="sxs-lookup"><span data-stu-id="76881-107">Effort tracking view</span></span>

<span data-ttu-id="76881-108">Prikaz **Praćenje truda** prati napredak zadataka u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="76881-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="76881-109">Uspoređuje sate stvarnog rada utrošenog na zadatak s planiranim satima rada na tom zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="76881-110">Project Service Automation upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:</span><span class="sxs-lookup"><span data-stu-id="76881-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="76881-111">Na početku rada na stvaranju zadatka: Planirani troškovi postavljaju se na procijenjeni trošak na završetku.</span><span class="sxs-lookup"><span data-stu-id="76881-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="76881-112">Nakon što se stvarni podaci zabilježe na zadatku, slijedi izračun u prikazu praćenja za rad</span><span class="sxs-lookup"><span data-stu-id="76881-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="76881-113">Postotak dovršenosti = stvarni rad utrošen do danas ÷ procijenjeni rad na završetku (EAC, Estimate at complete)</span><span class="sxs-lookup"><span data-stu-id="76881-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="76881-114">Procijenjeni rad na završetku (ETC) = procijenjeni rada na završetku (EAC) – stvarni rad utrošen do danas</span><span class="sxs-lookup"><span data-stu-id="76881-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="76881-115">EAC = preostali rad + stvarni rad do danas</span><span class="sxs-lookup"><span data-stu-id="76881-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="76881-116">Predviđeno odstupanje rada = planirani rad – EAC</span><span class="sxs-lookup"><span data-stu-id="76881-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="76881-117">Project Service Automation prikazuje predviđanje odstupanja rada u zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="76881-118">Ako je EAC veći od planiranog rada, predviđa se da će zadatak potrajati dulje nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="76881-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="76881-119">Stoga kasni za rasporedom.</span><span class="sxs-lookup"><span data-stu-id="76881-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="76881-120">Ako je EAC manji od planiranog rada, predviđa se da će zadatak potrajati kraće nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="76881-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="76881-121">Stoga će se dovršiti prije roka.</span><span class="sxs-lookup"><span data-stu-id="76881-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="76881-122">Ponovno predviđanje rada</span><span class="sxs-lookup"><span data-stu-id="76881-122">Reprojecting effort</span></span>

<span data-ttu-id="76881-123">Uobičajeno je da upravitelj projekta revidira izvorne procjene u zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="76881-124">Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="76881-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="76881-125">Međutim, upraviteljima projekta ne preporučujemo promjenu osnovnih brojeva, jer osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.</span><span class="sxs-lookup"><span data-stu-id="76881-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="76881-126">Postoje dva načina na koja upravitelj projekta može ponovno predvidjeti rad na zadacima:</span><span class="sxs-lookup"><span data-stu-id="76881-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="76881-127">Nadjačajte zadani ETC novom procjenom stvarnog preostalog rada zadatka.</span><span class="sxs-lookup"><span data-stu-id="76881-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="76881-128">Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="76881-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="76881-129">Svaki od tih pristupa uzrokuje ponovno izračunavanje ETC-a, EAC-a i postotka napretka zadatka te predviđena odstupanja rada na zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="76881-130">EAC, ETC i postotak napretka na zadacima sažetka također se ponovno izračunavaju i stvara se novo predviđanje odstupanja rada.</span><span class="sxs-lookup"><span data-stu-id="76881-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="76881-131">Ponovno predviđanje rada na zadacima sažetka</span><span class="sxs-lookup"><span data-stu-id="76881-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="76881-132">Rad na zadacima sažetka ili zadacima spremnika može se ponovno predvidjeti.</span><span class="sxs-lookup"><span data-stu-id="76881-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="76881-133">Bez obzira na to hoće li korisnik izvršiti ponovno predviđanje pomoću preostalog rada ili postotka napretka na zadacima sažetka, pokreće se sljedeći skup izračuna:</span><span class="sxs-lookup"><span data-stu-id="76881-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="76881-134">Izračunačava se EAC, ETC i postotak napretka na zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="76881-135">Novi EAC distribuira se na podređene zadatke u istom omjeru kao izvorni EAC na zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="76881-136">Izračunava se novi EAC za svaki od pojedinačnih zadataka lisnih čvorova.</span><span class="sxs-lookup"><span data-stu-id="76881-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="76881-137">ETC i postotak napretka za zahvaćene podređene zadatke lisnih čvorova ponovno se izračunavaju na temelju vrijednosti EAC-a.</span><span class="sxs-lookup"><span data-stu-id="76881-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="76881-138">To rezultira novim predviđanjem za odstupanje rada zadatka.</span><span class="sxs-lookup"><span data-stu-id="76881-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="76881-139">Ponovno se izračunavaju EAC-ovi zadataka sažetka sve do korijenskog čvora.</span><span class="sxs-lookup"><span data-stu-id="76881-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="76881-140">Prikaz praćenja troškova</span><span class="sxs-lookup"><span data-stu-id="76881-140">Cost tracking view</span></span> 

<span data-ttu-id="76881-141">Prikaz **Praćenje troškova** uspoređuje stvarni trošak koji je potrošen na zadatak s planiranim troškom.</span><span class="sxs-lookup"><span data-stu-id="76881-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="76881-142">Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procjena troškova.</span><span class="sxs-lookup"><span data-stu-id="76881-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="76881-143">Project Service Automation upotrebljava sljedeće formule za izračun mjernih podataka o praćenju:</span><span class="sxs-lookup"><span data-stu-id="76881-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="76881-144">Kada se stvara zadatak, planirani trošak jednak je procijenjenom trošku na završetku.</span><span class="sxs-lookup"><span data-stu-id="76881-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="76881-145">Nakon što se stvarni podaci zabilježe na zadatku, slijedi izračun u prikazu **Praćenje** za trošak:</span><span class="sxs-lookup"><span data-stu-id="76881-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="76881-146">Postotak utrošenog troška = stvarni trošak utrošen do danas ÷ procijenjeni trošak na završetku zadatka</span><span class="sxs-lookup"><span data-stu-id="76881-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="76881-147">Trošak na završetku (CTC, Cost to complete) = procijenjeni trošak na završetku – stvarni trošak utrošen do danas</span><span class="sxs-lookup"><span data-stu-id="76881-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="76881-148">Procijenjeni trošak na završetku = CTC + stvarni trošak utrošen do danas</span><span class="sxs-lookup"><span data-stu-id="76881-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="76881-149">Predviđeno odstupanje troška = planirani trošak – procijenjeni trošak na završetku</span><span class="sxs-lookup"><span data-stu-id="76881-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="76881-150">Predviđanje odstupanja troškova prikazuje se u zadatku.</span><span class="sxs-lookup"><span data-stu-id="76881-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="76881-151">Ako je procijenjeni trošak na završetku veći od planiranog troška, predviđa se da će zadatak imati veći trošak nego što je izvorno planirano.</span><span class="sxs-lookup"><span data-stu-id="76881-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="76881-152">Stoga postoji tendencija premašivanja proračuna.</span><span class="sxs-lookup"><span data-stu-id="76881-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="76881-153">Ako je procijenjeni trošak na završetku manji od planiranog troška, predviđa se da će zadatak imati manji trošak nego što je izvorno planirano i postoji tendencija neiskorištavanja proračuna.</span><span class="sxs-lookup"><span data-stu-id="76881-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="76881-154">Ponovno predvđanje troškova od strane upravitelja projekta</span><span class="sxs-lookup"><span data-stu-id="76881-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="76881-155">Kada se rad ponovno predviđa, CTC, procijenjeni trošak na završetku, postotak utrošenog troška i predviđeno odstupanje troška ponovno se izračunavaju u prikazu **Praćenje troškova**.</span><span class="sxs-lookup"><span data-stu-id="76881-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="76881-156">Sažetak statusa projekta</span><span class="sxs-lookup"><span data-stu-id="76881-156">Project status summary</span></span>

<span data-ttu-id="76881-157">Praćenje podataka u prikazu **Praćenje rada** i **Praćenje troškova** prikazuje napredak i potrošnju troškova u korijenskom čvoru projekta, zadacima sažetka i zadacima na razini lisnog čvora.</span><span class="sxs-lookup"><span data-stu-id="76881-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="76881-158">Odjeljak **Status** na stranici **Entitet projekta** prikazuje sažetak statusa na razini projekta.</span><span class="sxs-lookup"><span data-stu-id="76881-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="76881-159">Polja sažetka statusa</span><span class="sxs-lookup"><span data-stu-id="76881-159">Status summary fields</span></span>

<span data-ttu-id="76881-160">Polje **Sveukupni status projekta** polje je koje se može uređivati, a prikazuje sveukupni status projekta.</span><span class="sxs-lookup"><span data-stu-id="76881-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="76881-161">Koristi kodiranje bojama, kao što su zelena, žuta i crvena, kako bi se naznačio povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="76881-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="76881-162">Polje **Komentari** omogućuje upravitelju projekta da unese određene komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="76881-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="76881-163">Polje **Datum ažuriranja statusa** nije moguće uređivati, a vrijednost je vremenska oznaka koja označava kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="76881-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="76881-164">Polja **Uspješnost rasporeda** i **Uspješnost troška** postavljaju se na temelju datuma praćenja.</span><span class="sxs-lookup"><span data-stu-id="76881-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="76881-165">Kada je odstupanje rasporeda i troškova za korijenski čvor u prikazu **Praćenje rada** pozitivno, ta polja možete postaviti na **Ispred**.</span><span class="sxs-lookup"><span data-stu-id="76881-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="76881-166">Kada je odstupanje rasporeda i troška za korijenski čvor negativno, možete ih postaviti na **Iza**.</span><span class="sxs-lookup"><span data-stu-id="76881-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
