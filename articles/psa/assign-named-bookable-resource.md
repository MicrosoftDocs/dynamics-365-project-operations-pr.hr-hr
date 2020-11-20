---
title: Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke
description: U ovoj temi nalaze se informacije o načinu rezervacije imenovanih resursa za projektne timove i o njihovoj dodjeli zadacima.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 0300c494a3294b26e2de6bbfa1dd50a76bb72651
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130164"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="9cd5a-103">Rezerviraj imenovane resurse koji se mogu rezervirati za projektni tim i dodijeli zadatke</span><span class="sxs-lookup"><span data-stu-id="9cd5a-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9cd5a-104">Možete dodati imenovani resurs u projektni tim tako da ga izravno rezervirate za tim.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="9cd5a-105">Da biste to učinili, izvršite sljedeće korake:</span><span class="sxs-lookup"><span data-stu-id="9cd5a-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="9cd5a-106">U programu Project Service Automation, idite na **Projekti** i odaberite Otvori projekt za koji rezervirate.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="9cd5a-107">Na stranici **Projekt** na kartici **Tim** kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Dodavanje člana tima s kartice tima](media/RM-how-to-1.png)

3. <span data-ttu-id="9cd5a-109">U dijaloškom okviru **Brza izrada člana projektnog tima** odaberite resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="9cd5a-110">Polje **Uloga** popunit će se zadanom ulogom resursa ako mu je dodijeljena jedna.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="9cd5a-111">Prema potrebi, ulogu možete promijeniti.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="9cd5a-112">Odaberite od i do datume koji će biti potrebni za resurs i odaberite način dodjele kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="9cd5a-113">Ako želite da član tima bude odobravatelj projekta, odaberite **Da** u polju **Odobravatelj projekta**.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="9cd5a-114">To će značiti da član tima može odobriti poslane unose vremena i troška za ovaj projekt.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="9cd5a-115">Kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-115">Click **Save**.</span></span>

![Dodavanje člana tima u obrazac za brzu izradu](media/RM-how-to-2.png)


<span data-ttu-id="9cd5a-117">Sada možete dodijeliti rezervirani resurs zadacima na projektu.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="9cd5a-118">Na stranici **Projekt** kliknite karticu **Raspored** da biste dodijelili zadatke novom resursu.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="9cd5a-119">Birač resursa koji je pokrenut iz polja **Resursi** u rešetki zadataka pokazat će članove tima koje možete odabrati.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Dodjela člana tima zadatku na kartici rasporeda](media/RM-how-to-3.png)

<span data-ttu-id="9cd5a-121">U verziji 3 za program Project Service Automation (PSA), rezervacije resursa i dodjele zadataka nisu usko povezane.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="9cd5a-122">To znači da kada koristite birač resursa u rasporedu, možete dodijeliti zadatke članovima tima za više sati nego što njihove rezervacije pokrivaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="9cd5a-123">Možete vidjeti razlike između rezervacija članova tima i dodjela na kartici **Tim** ili na kartici **Usklađivanje resursa**. Možete i uskladiti razlike između rezervacija i dodjela za resurse na detaljnijoj razini.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Kartica Usklađivanje resursa](media/RM-how-to-4.png)

<span data-ttu-id="9cd5a-125">Možete koristiti i birača resursa na kartici **Raspored** da biste potražili i odabrali resurse koji se mogu rezervirati, a koji još nisu dio projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="9cd5a-126">Oni se prikazuju u biraču resursa kao **Ostali resursi**.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Dodjeljivanje resursa člana koji nije dio tima zadatku](media/RM-how-to-5.png)

<span data-ttu-id="9cd5a-128">Kada ovo činite, resurs se dodaje projektnom timu i dodjeljuje zadatku, ali rezervacije se ne generiraju.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Član tima s dodjelama i bez rezervacija](media/RM-how-to-6.png)

<span data-ttu-id="9cd5a-130">Možete koristiti mogućnost proširenja rezervacije kartice **Usklađivanje** ili **Ploča s rasporedom** da biste rezervirali kapacitet resursa za projekt.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Proširivanje rezervacija za člana tima na kartici usklađivanja resursa](media/RM-how-to-7.png)

<span data-ttu-id="9cd5a-132">Nakon što je član tima rezerviran za vaš projekt, možete koristiti održavanje rezervacija ili izravno koristiti Ploču s rasporedom za upravljanje rezervacijama.</span><span class="sxs-lookup"><span data-stu-id="9cd5a-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
