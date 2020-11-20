---
title: Održavanje članova tima
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za projektne timove i o dodjeli istih zadacima.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131514"
---
# <a name="maintain-team-members"></a><span data-ttu-id="2b4af-103">Održavanje članova tima</span><span class="sxs-lookup"><span data-stu-id="2b4af-103">Maintain team members</span></span>

<span data-ttu-id="2b4af-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="2b4af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2b4af-105">Možete dodati imenovani resurs projektnom timu tako da ga izravno rezervirate za tim.</span><span class="sxs-lookup"><span data-stu-id="2b4af-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="2b4af-106">U aplikaciji Dynamics 365 Project Operations, idite na **Projekti** i odaberite otvori projekt za koji rezerviraš.</span><span class="sxs-lookup"><span data-stu-id="2b4af-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="2b4af-107">Na stranici **Projekt**, na kartici **Tim**, odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="2b4af-108">U dijaloškom okviru **Brza izrada člana projektnog tima** odaberite resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="2b4af-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="2b4af-109">Polje **Uloga** popunit će se zadanom ulogom resursa ako mu je dodijeljena jedna.</span><span class="sxs-lookup"><span data-stu-id="2b4af-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="2b4af-110">Ulogu možete promijeniti.</span><span class="sxs-lookup"><span data-stu-id="2b4af-110">You can change the role.</span></span> 
4. <span data-ttu-id="2b4af-111">Odaberite početni i završni datum koji će biti potrebni za resurs i odaberite način dodjele kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="2b4af-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="2b4af-112">Ako želite da član tima bude odobravatelj projekta, u polju **Odobravatelj projekta** odaberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="2b4af-113">Član tima može odobriti poslane unose vremena i troška za ovaj projekt.</span><span class="sxs-lookup"><span data-stu-id="2b4af-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="2b4af-114">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-114">Select **Save**.</span></span>

<span data-ttu-id="2b4af-115">Sada možete dodijeliti rezervirani resurs zadacima na projektu.</span><span class="sxs-lookup"><span data-stu-id="2b4af-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="2b4af-116">Na stranici **Projekt**, na kartici **Raspored**, dodijelite zadatke novom resursu.</span><span class="sxs-lookup"><span data-stu-id="2b4af-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="2b4af-117">Birač resursa koji je pokrenut iz polja **Resursi** u rešetki zadataka pokazat će članove tima koje možete odabrati.</span><span class="sxs-lookup"><span data-stu-id="2b4af-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="2b4af-118">U aplikaciji Project Operations, rezerviranja resursa i dodjele zadataka nisu usko povezani.</span><span class="sxs-lookup"><span data-stu-id="2b4af-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="2b4af-119">Kada upotrebljavate birač resursa u rasporedu, možete dodijeliti zadatke članovima tima za više sati nego što njihove rezervacije pokrivaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="2b4af-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="2b4af-120">Razlike između rezervacija i zadataka članova tima prikazane su na karticama **Tim** i **Usklađivanje resursa**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="2b4af-121">Također možete uskladiti razlike između rezervacija i zadataka za resurse na podrobnijoj razini.</span><span class="sxs-lookup"><span data-stu-id="2b4af-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="2b4af-122">Upotrijebite birač resursa na kartici **Raspored** kako biste potražili i odabrali resurse koji se mogu rezervirati, a koji još nisu dio projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="2b4af-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="2b4af-123">Ti se resursi prikazuju u biraču resursa kao **Ostali resursi**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="2b4af-124">Kada izvršite odabir, resurs se dodaje projektnom timu i dodjeljuje zadatku, ali rezervacije se ne generiraju.</span><span class="sxs-lookup"><span data-stu-id="2b4af-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="2b4af-125">Možete koristiti mogućnost proširenja rezervacije kartice **Usklađivanje** ili **Ploča s rasporedom** da biste rezervirali kapacitet resursa za projekt.</span><span class="sxs-lookup"><span data-stu-id="2b4af-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="2b4af-126">Nakon što je član tima rezerviran za vaš projekt, za upravljanje rezervacijama možete upotrijebiti mogućnost **Održavanje rezervacija** ili izravno **Ploču s rasporedom**.</span><span class="sxs-lookup"><span data-stu-id="2b4af-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
