---
title: Izrada rezervacije projekta s ploče rasporeda
description: Ova tema pruža informacije o izradi rezervacije projekta s ploče rasporeda.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073405"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="6b1c7-103">Izrada rezervacije projekta s ploče rasporeda</span><span class="sxs-lookup"><span data-stu-id="6b1c7-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="6b1c7-104">Možete rezervirati resurs za projekt izravno s kartice projekta **Tim** ili generiranjem zahtjeva resursa iz zadatka generičkog člana tima, a zatim ispunjavanjem generiranog zahtjeva s članom projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="6b1c7-105">Resurs možete rezervirati za projekt i izravno s ploče rasporeda.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="6b1c7-106">To možete učiniti na tri načina:</span><span class="sxs-lookup"><span data-stu-id="6b1c7-106">There are three ways to do this:</span></span>

- <span data-ttu-id="6b1c7-107">**Rezerviraj iz generiranog preduvjeta resursa:** Možete generirati preduvjet resursa nakon što izradite generički resurs i dodijelite zadatke unutar projekta.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="6b1c7-108">**Rezerviraj iz primarnog preduvjeta:** Primarni preduvjeti prikazuju se na ploči rasporeda na kartici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="6b1c7-109">**Rezerviraj iz novog preduvjeta resursa:** Možete izraditi preduvjet resursa od nule i povezati ga s projektom.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="6b1c7-110">Na ploči s rasporedom, preduvjet resursa prikazuje se na kartici **Otvoreni preduvjeti**.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="6b1c7-111">Rezervirajte iz generiranog preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="6b1c7-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="6b1c7-112">Možete izraditi generički resurs i dodijeliti ga jednom ili više zadataka unutar projekta.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="6b1c7-113">Zatim možete generirati preduvjet resursa od generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="6b1c7-114">Na ploči s rasporedom, taj resurs prikazat će se na kartici **Otvoreni zahtjevi**. Možda ćete morati koristiti filtre stupaca na rešetki ako imate mnogo otvorenih zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="6b1c7-115">![Dodavanje kartice preduvjeta ploči s rasporedom](media/FAQ-Project-Booking-Schedule-Board-1.png "Snimka zaslona tablice rezervacija i dodjela")</span><span class="sxs-lookup"><span data-stu-id="6b1c7-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="6b1c7-116">Odaberite preduvjet.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-116">Select the requirement.</span></span> <span data-ttu-id="6b1c7-117">Kartica **Pronađi dostupnost** pojavit će se pri vrhu odabranog retka.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="6b1c7-118">Odabirom kartice otvara se se Pomoćnik rasporeda ploče s rasporedom i filtriraju se dostupni resursi koji ispunjavaju zahtjev resursa.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="6b1c7-119">Zatim možete rezervirati resurs.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="6b1c7-120">Možete i povući i ispustiti odabrani redak s dna ploče s rasporedom do ćelije resursa na rešetki iznad.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="6b1c7-121">Kada ga ispustite, na desnoj strani će se otvoriti panel **Stvori rezervaciju za resurs**.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="6b1c7-122">Odabirom **Rezerviraj** resurs se rezervira za projektni tim.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-122">Selecting **Book** books the resource onto the project team.</span></span>

![Izrada panela Rezervacije resursa](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="6b1c7-124">Rezervacija od primarnog preduvjeta</span><span class="sxs-lookup"><span data-stu-id="6b1c7-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="6b1c7-125">Stvaranjem projekta u aplikaciji Project Service automatski se stvara preduvjet resursa nazvan primarnim preduvjetom.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="6b1c7-126">To je prazni zahtjev koji se koristi za brzo rezerviranje resursa s pomoću ploče s rasporedom bez generiranja zahtjeva ili njegove izrade od nule.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="6b1c7-127">Budući da je taj zahtjev prazan, morat ćete navesti datume, kao i način dodjele i sate, ako je primjenjivo.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="6b1c7-128">Za rezervaciju resursa s primarnim preduvjetom, na ploči s rasporedom odaberite karticu **Projekt**. Ako imate mnogo projekata, možda ćete morati koristiti filtar stupaca u stupcu **Projekt** .</span><span class="sxs-lookup"><span data-stu-id="6b1c7-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="6b1c7-129">![Filtri kolona na ploči s rasporedom](media/FAQ-Project-Booking-Schedule-Board-2.png "Snimka zaslona tablice rezervacija i dodjela")</span><span class="sxs-lookup"><span data-stu-id="6b1c7-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="6b1c7-130">Odaberite zahtjev koji ima samo naziv projekta u svom nazivu i koji ima trajanje vrijednosti nula (0).</span><span class="sxs-lookup"><span data-stu-id="6b1c7-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="6b1c7-131">Odaberite karticu **Pronađi dostupnost** koja se pojavi u tom retku.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="6b1c7-132">To će ploču s rasporedom prebaciti u način rada s pomoćnikom rasporeda i prikazat će dostupne resurse koji se mogu rezervirati za projekt.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="6b1c7-133">Budući da je **Primarrni zahtjev** prazni zahtjev s trajanjem vrijednosti nula (0), kada birate i rezervirate resurs, trebate postaviti trajanje na panelu **Izradi rezervaciju resursa**.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="6b1c7-134">Također možete odabrati **Primarni zahtjev projekta** pri dnu ploče s rasporedom i povući ga i ispustiti na resurs da biste ga rezervirali.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="6b1c7-135">Budući da je **Primarrni zahtjev** prazni zahtjev s trajanjem vrijednosti nula (0), kada birate i rezervirate resurs, trebate postaviti trajanje na panelu **Izradi rezervaciju resursa**.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="6b1c7-136">Kada rezervirate resurs putem **Primarrnog preduvjeta** na ploči s rasporedom, dodat ćete ga projektnom timu bez ikakvih zadataka.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="6b1c7-137">Rezervirajte iz novog preduvjeta resursa</span><span class="sxs-lookup"><span data-stu-id="6b1c7-137">Book from a new resource requirement</span></span>
<span data-ttu-id="6b1c7-138">Dovršite sljedeće korake za rezervaciju iz novog zahtjeva resursa.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="6b1c7-139">Idite na **Zahtjevi resursa** i odaberite **Novo** kako biste izradili novi zahtjev resursa.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-139">Go to **Resource Requirements** , and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="6b1c7-140">Na kartici **Projekt** odaberite projekt za pridruživanje zahtjeva projektu.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="6b1c7-141">Taj novi zahtjev prikazuje se kao **Otvoreni zahtjev** na ploči s rasporedom i možete ga ispuniti.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="6b1c7-142">Rezervirajte resurs da biste ga dodali projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="6b1c7-143">Sada kad je resurs rezerviran, morate ručno dodijeliti zadatke.</span><span class="sxs-lookup"><span data-stu-id="6b1c7-143">Now that the resource is booked, you must assign tasks manually.</span></span>

