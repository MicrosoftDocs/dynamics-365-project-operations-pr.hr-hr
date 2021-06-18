---
title: Dodjela resursa zadatku
description: Ova tema pruža informacije o tome kako dodijeliti resurse zadacima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: a348130ee5760196b2f008ea811e7a81758dd73e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993227"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="fba80-103">Dodjela resursa zadatku</span><span class="sxs-lookup"><span data-stu-id="fba80-103">Assign a resource to a task</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fba80-104">Postoje tri načina za dodjelu resursa zadatku u aplikaciji Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fba80-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="fba80-105">Rezervirajte resurs kao član tima, a zatim ga dodijelite zadatku</span><span class="sxs-lookup"><span data-stu-id="fba80-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="fba80-106">Možete dodati resurs projektnom timu i zatim ga dodijeliti zadacima u projektnom rasporedu.</span><span class="sxs-lookup"><span data-stu-id="fba80-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="fba80-107">Na kartici **Član tima** dodajte novog člana tima odabirom **Novo**.</span><span class="sxs-lookup"><span data-stu-id="fba80-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="fba80-108">Otvora se panel **Brza izrada člana tima** na kojem možete odabrati naziv za resurs koji je moguće rezervirati i postaviti ulogu.</span><span class="sxs-lookup"><span data-stu-id="fba80-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="fba80-109">Odaberite jednu od sljedećih načina dodjeljivanja za rezervaciju resursa:</span><span class="sxs-lookup"><span data-stu-id="fba80-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="fba80-110">**Puni kapacitet** rezervira puni kapacitet resursa za odabrane datume od i do.</span><span class="sxs-lookup"><span data-stu-id="fba80-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="fba80-111">**Postotni kapacitet** rezervira određeni postotak kapaciteta resursa za odabrane datume od i do.</span><span class="sxs-lookup"><span data-stu-id="fba80-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="fba80-112">**Ravnomjerna raspodjela po satima** rezervira resurs na određeni broj sati, ravnomjerno ih raspoređujući svakog dana za vrijeme određenih od i do datuma.</span><span class="sxs-lookup"><span data-stu-id="fba80-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="fba80-113">**Punjenje sprijeda po satima** rezervira resurs na određeni broj sati, umečući sprijeda sate svakog dana za vrijeme određenog razdoblja.</span><span class="sxs-lookup"><span data-stu-id="fba80-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="fba80-114">**Ništa** dodaje resurs timu, ali ne stvara nikakve rezervacije koje bi trošile njegov kapacitet.</span><span class="sxs-lookup"><span data-stu-id="fba80-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="fba80-115">Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa, a zatim pod **Članovi tima** odaberite člana tima kojeg ste upravo dodali.</span><span class="sxs-lookup"><span data-stu-id="fba80-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members**, select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="fba80-116">Na karticama **Članovi tima** i **Usklađivanje**, resurs pokazuje rezervirane i dodijeljene sate.</span><span class="sxs-lookup"><span data-stu-id="fba80-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="fba80-117">Sati bi trebali biti isti, ali ne moraju biti, budući da rezervacije i zadaci nisu usko povezani.</span><span class="sxs-lookup"><span data-stu-id="fba80-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="fba80-118">Kartica **Usklađivanje** pruža vam pojedinosti kada su različite, na primjer, kada dodijelite resursu više sati nego što ste rezervirali.</span><span class="sxs-lookup"><span data-stu-id="fba80-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="fba80-119">Po potrebi, možete ispraviti informacije produljivanjem rezervacija resursa ili izmjenom zadatka.</span><span class="sxs-lookup"><span data-stu-id="fba80-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="fba80-120">Izrada generičkog člana tima putem dodjele zadatka</span><span class="sxs-lookup"><span data-stu-id="fba80-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="fba80-121">Kada izrađujete generičkog člana tima putem dodjele zadatka, izrađujete rezervirano mjesto ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg u konačnici želite da radi na zadacima.</span><span class="sxs-lookup"><span data-stu-id="fba80-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="fba80-122">Zatim generirate uvjet (ili šaljete zahtjev koristeći uvjet) koji se koristi za pretraživanje i rezervaciju imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="fba80-123">Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="fba80-124">Upišite naziv koji će služiti kao naziv rezerviranog mjesta resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="fba80-125">Na primjer, upravitelj programa.</span><span class="sxs-lookup"><span data-stu-id="fba80-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="fba80-126">Odaberite **Izradi** i u polju **Brza izrada projektnog člana tima** postavite ulogu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="fba80-126">Select **Create**, and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="fba80-127">Možete nastaviti dodjeljivati zadatke tom rezerviranom mjestu resursa odabirom resursa na **Biraču resursa** za taj zadatak.</span><span class="sxs-lookup"><span data-stu-id="fba80-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="fba80-128">Navedeni su pod stavkom **Članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="fba80-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="fba80-129">Kada završite s dodjelom generičkog resursa, odaberite ga na kartici **Tim**, a zatim odaberite **Generiraj preduvjet** da biste izradili preduvjet resursa za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="fba80-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="fba80-130">Odaberite **Rezerviraj** za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="fba80-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="fba80-131">Zatim možete koristiti Ploču s rasporedom za pronalazak i rezerviranje pravog resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="fba80-132">Možete poslati i zahtjev za ispunjenje od strane upravitelja resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="fba80-133">Kada se generički resurs ispuni imenovanim resursom, tada se uklanja iz tima i dodjele zadataka generičkog resursa se dodjeljuju imenovanom resursu koji je ispunio preduvjet generičkog resursa za resursom.</span><span class="sxs-lookup"><span data-stu-id="fba80-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="fba80-134">Dodijeli imenovani resurs s popisa svih resursa koje je moguće rezervirati</span><span class="sxs-lookup"><span data-stu-id="fba80-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="fba80-135">Možete koristiti okvir za pretraživanje u **Biraču resursa** za pretraživanje resursa koje je moguće rezervirati i za njihovo dodjeljivanje zadatku.</span><span class="sxs-lookup"><span data-stu-id="fba80-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="fba80-136">Resursi dodijeljeni na taj način dodaju se timu bez rezervacija.</span><span class="sxs-lookup"><span data-stu-id="fba80-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="fba80-137">To je slično dodavanju člana tima i odabiru Nijedan kao načina dodjele.</span><span class="sxs-lookup"><span data-stu-id="fba80-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="fba80-138">Resurs je prikazan na karticama **Tim** i **Usklađivanje** kao resursi koji imaju samo zadatke i koji imaju manjak rezervacija.</span><span class="sxs-lookup"><span data-stu-id="fba80-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="fba80-139">Rezervirajte ih ako želite da iskoristite njihovu dostupnost.</span><span class="sxs-lookup"><span data-stu-id="fba80-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="fba80-140">Na rešetki **Raspored** za zadatak, odaberite ikonu **Resurs** u ćeliji resursa.</span><span class="sxs-lookup"><span data-stu-id="fba80-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="fba80-141">Počnite tipkati naziv.</span><span class="sxs-lookup"><span data-stu-id="fba80-141">Start typing a name.</span></span> <span data-ttu-id="fba80-142">Rezultati pretraživanja za naziv prikazuju se u **Biraču resursa** pod stavkom **Ostali resursi**.</span><span class="sxs-lookup"><span data-stu-id="fba80-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="fba80-143">Odaberite resurs koji želite dodijeliti zadatku.</span><span class="sxs-lookup"><span data-stu-id="fba80-143">Select the resource that you want to assign to the task.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]