---
title: Rezerviraj imenovane resurse iz zahtjeva resursa
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za generički zahtjev resursa.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013387"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="d6870-103">Rezerviraj imenovane resurse iz zahtjeva resursa</span><span class="sxs-lookup"><span data-stu-id="d6870-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d6870-104">Možete rezervirati imenovani resurs da zamjenite generički resurs koji ima zahtjev resursa.</span><span class="sxs-lookup"><span data-stu-id="d6870-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="d6870-105">U sustavu Project Service Automation (PSA) na stranici **Projekti**, kliknite karticu **Tim**.</span><span class="sxs-lookup"><span data-stu-id="d6870-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="d6870-106">S popisa odaberite generički resurs koji ima zahtjev resursa, a zatim kliknite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="d6870-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="d6870-107">Ili otvorite zahtjev resursa, a zatim kliknite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="d6870-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervacija člana generičkog tima](media/RM-how-to-14.png)


3. <span data-ttu-id="d6870-109">Na stranici **Pomoćnik za raspored**, odaberite imenovani resurs koji ćete rezervirati u projektni tim, a zatim kliknite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="d6870-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervacija člana generičkog tima s pomoću pomoćnika za raspored](media/RM-how-to-15.png)

<span data-ttu-id="d6870-111">Kada je rezervacija dovršena i ispunjena od strane imenovanog resursa, generički resurs zamjenjuje se imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="d6870-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Imenovani član tima zamjenjuje člana generičkog tima](media/RM-how-to-16.png)

<span data-ttu-id="d6870-113">Zadaci u rasporedu ažuriraju se i s imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="d6870-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Imenovani član tima dodijeljen projektnim zadacima](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="d6870-115">Ispunite generički resurs s više imenovanih resursa</span><span class="sxs-lookup"><span data-stu-id="d6870-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="d6870-116">Ispunjavanje zahtjeva za generički resurs s više imenovanih resursa slično je dodjeljivanju jednog imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="d6870-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="d6870-117">Na primjer, postoji zadatak u trajanju od pet dana i 120 sati napora.</span><span class="sxs-lookup"><span data-stu-id="d6870-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="d6870-118">Ovaj zadatak ne može dovršiti jedan resurs koji odrađuje tipičan dan od osam sati u pet dana u tjednu.</span><span class="sxs-lookup"><span data-stu-id="d6870-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Zadatak koji treba 120 sati truda tijekom pet dana](media/RM-how-to-21.png)

<span data-ttu-id="d6870-120">Zahtjev je za 120 sati inženjerske robotike tijekom pet dana, što je 24 sata dnevno.</span><span class="sxs-lookup"><span data-stu-id="d6870-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Zahtjev po danu](media/RM-how-to-22.png)

<span data-ttu-id="d6870-122">Ovo je primjer kada je potrebno više imenovanih resursa za ispunjavanje zahtjeva generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="d6870-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="d6870-123">Morat ćete rezervirati više resursa za ispunjavanje zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="d6870-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervacija više resursa za ispunjavanje zahtjeva](media/RM-how-to-23.png)

<span data-ttu-id="d6870-125">Glavna razlika u ovom scenariju je da generički resurs ostaje u timu koji je dodijeljen zadatku, a članovi tima rezerviranog imenovanog resursa ne dodjeljuju se kao dio položaja.</span><span class="sxs-lookup"><span data-stu-id="d6870-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="d6870-126">Upravitelj projekta može dodijeliti rad po potrebi imenovanim resursima.</span><span class="sxs-lookup"><span data-stu-id="d6870-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="d6870-127">Prikaz **Usklađivanje** može pomoći upravitelju projekta kod razvrstavanja rezervacija više resursa u dodjele zadataka.</span><span class="sxs-lookup"><span data-stu-id="d6870-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="d6870-128">To se ne izvodi automatski jer u bilo kojem scenariju koji je složeniji od jednostavnog primjera gore, kao što je slučaj gdje postoji skupina zadataka koji čine zahtjev, namjera upravitelja projekta za dodjeljivanjem mora biti prepoznata od strane sustava.</span><span class="sxs-lookup"><span data-stu-id="d6870-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="d6870-129">Budući da sustav ne može razumjeti namjeru, šanse su da će pretpostavke biti različite od predviđenog i da će doći do netočnog ili nepredvidljivog rezultata.</span><span class="sxs-lookup"><span data-stu-id="d6870-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="d6870-130">Predvidljiv ishod je da generički resurs ostaje dodijeljen dok upravitelj projekta namjerno ne izradi dodjele, uz pomoć prikaza **Usklađivanje**.</span><span class="sxs-lookup"><span data-stu-id="d6870-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]