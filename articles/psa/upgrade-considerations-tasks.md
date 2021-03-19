---
title: Razmatranja nadogradnje za strukturnu analizu rada
description: Ova tema pruža informacije o nadogradnji strukturne analize rada s Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281739"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="8eab1-103">Razmatranja nadogradnje za strukturnu analizu rada</span><span class="sxs-lookup"><span data-stu-id="8eab1-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8eab1-104">Ova tema pruža informacije o nadogradnji strukturne analize rada s Project Service Automation 2.x na 3.x.</span><span class="sxs-lookup"><span data-stu-id="8eab1-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="8eab1-105">Ova tema definira zdravo stanje projekta u Project Service Automation (PSA) koje je potrebno za uspješnu nadogradnju.</span><span class="sxs-lookup"><span data-stu-id="8eab1-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="8eab1-106">Postoje i informacije o uobičajenim uvjetima blokiranja koji će uzrokovati neuspjeh nadogradnje.</span><span class="sxs-lookup"><span data-stu-id="8eab1-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="8eab1-107">Dodatne informacije o određivanju projektnih zadataka i njihovih funkcija unutar rasporeda projekta potražite u članku [Rasporedi projekata](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="8eab1-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="8eab1-108">Ključni entiteti</span><span class="sxs-lookup"><span data-stu-id="8eab1-108">Key entities</span></span>
<span data-ttu-id="8eab1-109">Za točnu strukturnu analizu rada koja je već napunjena resursima, potrebni su sljedeći entiteti:</span><span class="sxs-lookup"><span data-stu-id="8eab1-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="8eab1-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="8eab1-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="8eab1-111">Projektni tim</span><span class="sxs-lookup"><span data-stu-id="8eab1-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="8eab1-112">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="8eab1-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="8eab1-113">Dodjele resursa</span><span class="sxs-lookup"><span data-stu-id="8eab1-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="8eab1-114">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="8eab1-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="8eab1-115">Resursi koje je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="8eab1-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="8eab1-116">Da biste definirali strukturnu analizu rada napunjenu resursima, morate dovršiti sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="8eab1-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="8eab1-117">Stvorite novi projekt.</span><span class="sxs-lookup"><span data-stu-id="8eab1-117">Create a new project.</span></span> <span data-ttu-id="8eab1-118">Dodatne informacije o tome kako stvoriti novi projekt potražite u članku [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="8eab1-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="8eab1-119">Stvorite jedan ili više zadataka.</span><span class="sxs-lookup"><span data-stu-id="8eab1-119">Create one or more tasks.</span></span> <span data-ttu-id="8eab1-120">Dodatne informacije o tome kako stvoriti novi zadatak potražite u članku [msdyn_projecttast](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="8eab1-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="8eab1-121">Definirajte ovisnosti zadataka.</span><span class="sxs-lookup"><span data-stu-id="8eab1-121">Define the task dependencies.</span></span> <span data-ttu-id="8eab1-122">Dodatne informacije potražite u članku [Ovisnost projektnog zadatka](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="8eab1-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="8eab1-123">Dodijelite članove projektnih timova projektu.</span><span class="sxs-lookup"><span data-stu-id="8eab1-123">Assign project team members to the project.</span></span> <span data-ttu-id="8eab1-124">Dodatne informacije potražite u članku [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="8eab1-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="8eab1-125">Dodijelite članove projektnih timova zadatku.</span><span class="sxs-lookup"><span data-stu-id="8eab1-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="8eab1-126">Dodatne informacije potražite u članku [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="8eab1-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="8eab1-127">Odnosi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="8eab1-127">Project team relationships</span></span>

<span data-ttu-id="8eab1-128">Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="8eab1-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="8eab1-129">Svi članovi tima projektnih timova moraju biti pridruženi resursu koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="8eab1-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="8eab1-130">Svi članovi tima projektnih timova moraju biti pridruženi istom projektu.</span><span class="sxs-lookup"><span data-stu-id="8eab1-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="8eab1-131">Odnosi projektnih zadataka</span><span class="sxs-lookup"><span data-stu-id="8eab1-131">Project task relationships</span></span>
<span data-ttu-id="8eab1-132">Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="8eab1-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8eab1-133">Svi povezani zadaci moraju biti pridruženi istom projektu.</span><span class="sxs-lookup"><span data-stu-id="8eab1-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="8eab1-134">Svaki zadatak retka mora imati nadređeni zadatak.</span><span class="sxs-lookup"><span data-stu-id="8eab1-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="8eab1-135">Svaki zadatak mora imati nadređeni projekt.</span><span class="sxs-lookup"><span data-stu-id="8eab1-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="8eab1-136">Valjani uvjeti</span><span class="sxs-lookup"><span data-stu-id="8eab1-136">Valid conditions</span></span>

- <span data-ttu-id="8eab1-137">Sva trajanja zadatka moraju biti veća ili jednaka (> =) od jednog sata i manja od 1.800,000 minuta (1.250 dana). \*</span><span class="sxs-lookup"><span data-stu-id="8eab1-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="8eab1-138">Svi zadaci moraju imati datum početka ne ranije od 1. 1. 2000. \*</span><span class="sxs-lookup"><span data-stu-id="8eab1-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="8eab1-139">Svi zadaci moraju imati datum početka najkasnije 17 godina od ovog dana. \*</span><span class="sxs-lookup"><span data-stu-id="8eab1-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="8eab1-140">Svi zadaci moraju imati datum početka ranije ili jednak datumu završetka.</span><span class="sxs-lookup"><span data-stu-id="8eab1-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="8eab1-141">Sve vrste transakcija za klasifikacije (rashodi, materijal, porez i vrijeme) moraju imati vrijednosti za **Zadanu jedinicu** i **Grupu jedinica**.</span><span class="sxs-lookup"><span data-stu-id="8eab1-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="8eab1-142">Oblike datuma sa slovima treba izbjegavati.</span><span class="sxs-lookup"><span data-stu-id="8eab1-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8eab1-143">Mogući koraci ublažavanja</span><span class="sxs-lookup"><span data-stu-id="8eab1-143">Potential mitigation steps</span></span>
- <span data-ttu-id="8eab1-144">Upotrijebite mogućnost Napredno pretraživanje kako biste odredili Projektne zadatke koji ne sadrže ID projekta.</span><span class="sxs-lookup"><span data-stu-id="8eab1-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="8eab1-145">Upotrijebite mogućnost Napredno pretraživanje kako biste odredili Projektne zadatke planiranog trajanja duljeg od > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="8eab1-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="8eab1-146">Prije nego što izvršite bilo kakve promjene podataka, trebali biste istražiti sve prilagodbe povezane s entitetom koje su mogle dovesti do lošeg stanja podataka.</span><span class="sxs-lookup"><span data-stu-id="8eab1-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="8eab1-147">Ovim bi se prilagodbama trebalo pozabaviti prije nego što nastavite s ažuriranjem koje se odnosi na podatke.</span><span class="sxs-lookup"><span data-stu-id="8eab1-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="8eab1-148">Za određene zadatke koji su bili izolirani, razmotrite brisanje tih zadataka ako nisu potrebni ili ako bi trebali biti povezani s ispravnim nadređenim projektom.</span><span class="sxs-lookup"><span data-stu-id="8eab1-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="8eab1-149">Za sve zadatke u kojima je trajanje dulje od 1.250 dana, razmislite o dodavanju više zadataka kako biste prikazali ukupno trajanje, ako je izvedivo.</span><span class="sxs-lookup"><span data-stu-id="8eab1-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="8eab1-150">Stavke označene zvjezdicom (\*) imaju ograničenja koja postoje zbog činjenice da upravljanje odnosima s klijentima (CRM) podržava samo 7.320 poslova proširenja.</span><span class="sxs-lookup"><span data-stu-id="8eab1-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="8eab1-151">Morate ostati ispod ove granice.</span><span class="sxs-lookup"><span data-stu-id="8eab1-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="8eab1-152">Odnosi dodjele resursa</span><span class="sxs-lookup"><span data-stu-id="8eab1-152">Resource Assignment relationships</span></span>
<span data-ttu-id="8eab1-153">Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="8eab1-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8eab1-154">Sve Dodjele resursa u strukturnoj analizi rada moraju biti povezane s istim projektom.</span><span class="sxs-lookup"><span data-stu-id="8eab1-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="8eab1-155">Sve Dodjele resursa u strukturnoj analizi rada moraju biti povezane s članovima projektnog tima u istom projektu.</span><span class="sxs-lookup"><span data-stu-id="8eab1-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="8eab1-156">Mogući koraci ublažavanja</span><span class="sxs-lookup"><span data-stu-id="8eab1-156">Potential mitigation steps</span></span>
- <span data-ttu-id="8eab1-157">Odredite sve zadatke koji izlaze izvan gore opisanih uvjeta.</span><span class="sxs-lookup"><span data-stu-id="8eab1-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="8eab1-158">Sve Dodjele resursa koje više nisu valjane treba izbrisati.</span><span class="sxs-lookup"><span data-stu-id="8eab1-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="8eab1-159">Ovisni odnosi projektnih zadataka</span><span class="sxs-lookup"><span data-stu-id="8eab1-159">Project task dependency relationships</span></span>
<span data-ttu-id="8eab1-160">Da bi se osigurala uspješna nadogradnja, sljedeći se odnosi moraju pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="8eab1-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="8eab1-161">Sve ovisnosti projektnih zadataka moraju biti povezane s istim projektom.</span><span class="sxs-lookup"><span data-stu-id="8eab1-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="8eab1-162">Zadatak ne može imati istu ovisnost koja se spominje više puta.</span><span class="sxs-lookup"><span data-stu-id="8eab1-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]