---
title: Kako mogu resurs koji se može rezervirati dodijeliti zadatku u web-aplikaciji
description: Pregled načina na koje možete dodijeliti resurse koji se mogu rezervirati.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 7b95eff52351904f97c62b3806f17b02db47860b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073576"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="f7a32-103">Kako da zadatku dodijelim resurs koji se može rezervirati u web-aplikaciji (aplikaciji Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="f7a32-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f7a32-104">Postoje dva načina za dodjelu resursa zadatku u aplikaciji Project Service.</span><span class="sxs-lookup"><span data-stu-id="f7a32-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="f7a32-105">Možete rezervirati resurs kao član tima, a zatim ga dodijeliti zadatku.</span><span class="sxs-lookup"><span data-stu-id="f7a32-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="f7a32-106">Ili možete stvoriti generičkog člana tima putem dodjele uloge u zadacima, generirati tim, a zatim ispuniti dodatne preduvjete s imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="f7a32-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="f7a32-107">Imajte na umu da ako zadatku želite dodijeliti resurs koji se može rezervirati, član tima tog resursa mora imati dovoljno dostupnih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="f7a32-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="f7a32-108">Status rezervacije mora biti Vrsta izvršavanja: fiksna rezervacija i Status izvršen.</span><span class="sxs-lookup"><span data-stu-id="f7a32-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="f7a32-109">Ako nema dovoljno rezervacija za određeni resurs, aplikacija Project Service uklanja dodjelu i prikazuje sljedeću poruku o pogrešci:</span><span class="sxs-lookup"><span data-stu-id="f7a32-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="f7a32-110">*Nije moguće dodijeliti resurs zadatku - Sljedeći resurs/i nema/ju dovoljno rezerviranih sati za projekat*</span><span class="sxs-lookup"><span data-stu-id="f7a32-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="f7a32-111">Rezervirajte resurs kao član tima, a zatim ga dodijelite zadatku</span><span class="sxs-lookup"><span data-stu-id="f7a32-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="f7a32-112">Pomoću ove metode možete dodati resurs projektnom timu, a zatim dodijeliti zadatake tom resursu u projektnom rasporedu.</span><span class="sxs-lookup"><span data-stu-id="f7a32-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="f7a32-113">Evo kako da to uradite:</span><span class="sxs-lookup"><span data-stu-id="f7a32-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="f7a32-114">Na rešetki član tima dodajte novog člana tima odabirom **Novo**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="f7a32-115">Na ekranu za brzo stvaranje člana tima izaberite ime za resurs koji je moguće rezervirati i postavite ulogu.</span><span class="sxs-lookup"><span data-stu-id="f7a32-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="f7a32-116">Odaberite **od** i **do** datume.</span><span class="sxs-lookup"><span data-stu-id="f7a32-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f7a32-117">![Snimka zaslona dodavanja člana tima](media/FAQ-Resources-to-Tasks2-1.png "Snimka zaslona dodavanja člana tima")</span><span class="sxs-lookup"><span data-stu-id="f7a32-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="f7a32-118">Izaberite jednu od sljedećih metoda dodjeljivanja za rezervaciju resursa:</span><span class="sxs-lookup"><span data-stu-id="f7a32-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="f7a32-119">**Puni kapacitet** rezervira puni kapacitet resursa za odabrane datume od i do.</span><span class="sxs-lookup"><span data-stu-id="f7a32-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f7a32-120">**Postotni kapacitet** rezervira određeni postotak kapaciteta resursa za odabrane datume od i do.</span><span class="sxs-lookup"><span data-stu-id="f7a32-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="f7a32-121">**Ravnomjerna raspodjela po satima** rezervira resurs na određeni broj sati, ravnomjerno ga raspoređujući svakog dana za vrijeme određenog razdoblja.</span><span class="sxs-lookup"><span data-stu-id="f7a32-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="f7a32-122">**Punjenje sprijeda po satima** rezervira resurs na određeni broj sati, umečući sprijeda sate svakog dana za vrijeme određenog razdoblja.</span><span class="sxs-lookup"><span data-stu-id="f7a32-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="f7a32-123">Nemojte odabrati **Ništa** jer bi se time resurs dodao timu, ali ne bi se stvarile nikakve rezervacije koje troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="f7a32-124">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-124">Select **Save**.</span></span>

    <span data-ttu-id="f7a32-125">Imajte na umu da sati rezervacije moraju biti dovoljni da pokriju sate rada i datumske raspone za zadatke kojima dodijelite taj resurs.</span><span class="sxs-lookup"><span data-stu-id="f7a32-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="f7a32-126">Ako oni nisu usklađeni, nećete moći dodijeliti resurs tom zadatku.</span><span class="sxs-lookup"><span data-stu-id="f7a32-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="f7a32-127">U strukturnoj analizi rada (SAR-u) za taj zadatak, kliknite na padajući izbornik ćelije resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="f7a32-128">Zatim:</span><span class="sxs-lookup"><span data-stu-id="f7a32-128">Then:</span></span> 

    1. <span data-ttu-id="f7a32-129">Odaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-129">Select **Add**.</span></span>
    2. <span data-ttu-id="f7a32-130">Odaberite padajući izbornik pod **Resursi** i odaberite člana tima kojeg ste dodali gore.</span><span class="sxs-lookup"><span data-stu-id="f7a32-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="f7a32-131">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-131">Select **OK**.</span></span> <span data-ttu-id="f7a32-132">Taj član tima sada je dodijeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="f7a32-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f7a32-133">![Snimka zaslona dodavanja resursa sa SAR-om](media/FAQ-Resources-to-Tasks2-2.png "Snimka zaslona dodavanja resursa sa SAR-om")</span><span class="sxs-lookup"><span data-stu-id="f7a32-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="f7a32-134">Na rešetki član tima pod Dodijeljeni sati vidjet ćete agregat dodijeljenih sati resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="f7a32-135">Bit će jednak ili manji od rezerviranih sati resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f7a32-136">![Snimka zaslona dodijeljenih sati za resurs](media/FAQ-Resources-to-Tasks2-3.png "Snimka zaslona dodijeljenih sati za resurs")</span><span class="sxs-lookup"><span data-stu-id="f7a32-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="f7a32-137">Ako zadatak kojeg pokušavate dodijeliti resursu počinje nakon datuma završetka rezervacija resursa, taj resurs se neće prikazati u padajućem izborniku.</span><span class="sxs-lookup"><span data-stu-id="f7a32-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="f7a32-138">Imajte na umu da možete dodijeliti resurs većem broju sati od njegovih rezerviranih sati ako ima nešto preostalog nedodijeljenog kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="f7a32-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="f7a32-139">U tom slučaju resurs će biti samo djelomično dodijeljen do njihovih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="f7a32-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="f7a32-140">Dodavanjem stupca Sati bez djelatnika strukturnoj analizi rada možete vidjeti te preostale nedodijeljene sate zadatka.</span><span class="sxs-lookup"><span data-stu-id="f7a32-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="f7a32-141">Ako su resursi dodijeljeni njihovim rezerviranim satima (njihovi rezervirani sati su jednaki njihovim dodijeljenim satima), vidjet ćete sljedeću poruku o pogrešci kada im pokušate dodijeliti još zadataka:</span><span class="sxs-lookup"><span data-stu-id="f7a32-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="f7a32-142">*Nije moguće dodijeliti resurs zadatku - Sljedeći resurs/i nema/ju dovoljno rezerviranih sati za projekat.*</span><span class="sxs-lookup"><span data-stu-id="f7a32-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="f7a32-143">Uz to, član tima koji je zadani upravitelj projekta i koji je dodan timu kada stvorite projekat dodaje se bez ikakvih rezervacija i ne može biti dodijeljen nijednom zadatku.</span><span class="sxs-lookup"><span data-stu-id="f7a32-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="f7a32-144">On se neće pojaviti u padajućem izborniku resursa za zadatke.</span><span class="sxs-lookup"><span data-stu-id="f7a32-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="f7a32-145">Ako želite dodijeliti ovaj resurs, morate ukloniti tog člana iz tima i zatim ga ponovno dodati pomoću bilo koje metode dodjele osim metode Ništa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="f7a32-146">Taj član je dodan timu pri stvaranju projekta da bi projekat imao barem jednog zadanog projektnog odobravatelja.</span><span class="sxs-lookup"><span data-stu-id="f7a32-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="f7a32-147">Stvorite generičkog člana tima putem dodjele uloge za zadatke</span><span class="sxs-lookup"><span data-stu-id="f7a32-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="f7a32-148">Zahvaljujući ovoj metodi svaki resurs ima dovoljno rezervacija za zadatke.</span><span class="sxs-lookup"><span data-stu-id="f7a32-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="f7a32-149">Prvo ćete generiranjem tima nakon dodjele uloga zadacima stvoriti rezervirano mjesto ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg u konačnici želite da radi na zadacima.</span><span class="sxs-lookup"><span data-stu-id="f7a32-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="f7a32-150">Evo kako da to uradite:</span><span class="sxs-lookup"><span data-stu-id="f7a32-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="f7a32-151">Odaberite zadatak u strukturnoj analizi rada.</span><span class="sxs-lookup"><span data-stu-id="f7a32-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="f7a32-152">Odaberite padajuću ikonu **Dodijeljena uloga** u ćeliji resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="f7a32-153">Odaberite padajući izbornik **Uloga** , a zatim odaberite ulogu za generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="f7a32-154">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="f7a32-155">![Snimka zaslona uporabe SAR-a za dodavanja resursa](media/FAQ-Resources-to-Tasks2-4.png "Snimka zaslona uporabe SAR-a za dodavanja resursa")</span><span class="sxs-lookup"><span data-stu-id="f7a32-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="f7a32-156">Nakon dovršetka dodjele uloga zadacima u SAR-u, odaberite **Generiranje projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="f7a32-157">Aplikacija Project Service stvara najmanji broj generičkih članova tima na temelju uloga, organizacijskih jedinica za resurse i projektnog kalendara agregirajući dodjele zadataka.</span><span class="sxs-lookup"><span data-stu-id="f7a32-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f7a32-158">![Snimka zaslona generiranja projektnog tima](media/FAQ-Resources-to-Tasks2-5.png "Snimka zaslona generiranja projektnog tima")</span><span class="sxs-lookup"><span data-stu-id="f7a32-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="f7a32-159">Na rešetki član tima vidjet ćete resurse generičkog tipa s nazivom uloge i položaja.</span><span class="sxs-lookup"><span data-stu-id="f7a32-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="f7a32-160">Ako su dva resursa potrebna za određenu ulogu da dovrši rad, značajka Generiranje tima će stvoriti dva člana tima i koristit će naziv položaja da ih razlikuje.</span><span class="sxs-lookup"><span data-stu-id="f7a32-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f7a32-161">![Snimka zaslona dodavanja dva generička resursa](media/FAQ-Resources-to-Tasks2-6.png "Snimka zaslona dodavanja dva generička resursa")</span><span class="sxs-lookup"><span data-stu-id="f7a32-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="f7a32-162">Možete otvoriti dodatni preduvjet resursa za generičkog člana tima odabirom veze pod stavkom Preduvjet resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="f7a32-163">![Snimka zaslona otvaranja dodatnog preduvjeta resursa](media/FAQ-Resources-to-Tasks2-7.png "Snimka zaslona otvaranja dodatnog preduvjeta resursa")</span><span class="sxs-lookup"><span data-stu-id="f7a32-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="f7a32-164">Odaberite **Rezerviraj** za generički resurs, a zatim možete koristiti ploču s rasporedom za pronalaženje i rezerviranje pravog resursa.</span><span class="sxs-lookup"><span data-stu-id="f7a32-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="f7a32-165">Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa odabirom **Pošalji zahtjev**.</span><span class="sxs-lookup"><span data-stu-id="f7a32-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="f7a32-166">Kada se generički resurs ispuni imenovanim resursom, tada se uklanja iz tima i dodjele zadataka generičkog resursa se dodjeljuju imenovanom resursu koji je ispunio preduvjet generičkog resursa za resursom.</span><span class="sxs-lookup"><span data-stu-id="f7a32-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

