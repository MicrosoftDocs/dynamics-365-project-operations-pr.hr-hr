---
title: Popunjavanje zahtjeva za generičkim resursima
description: Ova tema pruža informacije o rezerviranju imenovanih resursa za generički zahtjev resursa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897577"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="9e2b0-103">Popunjavanje zahtjeva za generičkim resursima</span><span class="sxs-lookup"><span data-stu-id="9e2b0-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="9e2b0-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="9e2b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9e2b0-105">Možete rezervirati imenovani resurs da zamjenite generički resurs koji ima zahtjev resursa.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="9e2b0-106">Na stranici **Projekti** odaberite karticu **Tim**.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="9e2b0-107">S popisa odaberite generički resurs koji ima zahtjev za resursom, a zatim odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="9e2b0-108">Ili otvorite zahtjev za resursom, a zatim odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="9e2b0-109">Na stranici **Pomoćnik za raspored**, odaberite imenovani resurs koji ćete rezervirati u projektni tim, a zatim odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="9e2b0-110">Kada je rezervacija dovršena i ispunjena od strane imenovanog resursa, generički resurs zamjenjuje se imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="9e2b0-111">Zadaci u rasporedu ažuriraju se i s imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="9e2b0-112">Ispunite generički resurs s više imenovanih resursa</span><span class="sxs-lookup"><span data-stu-id="9e2b0-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="9e2b0-113">Ispunjavanje zahtjeva za generički resurs s više imenovanih resursa slično je dodjeljivanju jednog imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="9e2b0-114">Na primjer, postoji zadatak u trajanju od pet dana i 120 sati napora.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="9e2b0-115">Ovaj zadatak ne može dovršiti jedan resurs koji odrađuje uobičajeni osmosatni radni dan tijekom pet dana u tjednu.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="9e2b0-116">Zahtjev je za 120 sati inženjerske robotike tijekom pet dana, što je 24 sata dnevno.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="9e2b0-117">Ovo je primjer kada je potrebno više imenovanih resursa za ispunjavanje zahtjeva generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="9e2b0-118">Morat ćete rezervirati više resursa za ispunjavanje zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="9e2b0-119">Glavna razlika u ovom scenariju je da generički resurs ostaje u timu koji je dodijeljen zadatku, a članovi tima rezerviranog imenovanog resursa ne dodjeljuju se kao dio položaja.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="9e2b0-120">Upravitelj projekta može dodijeliti rad po potrebi imenovanim resursima.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="9e2b0-121">Prikaz **Usklađivanje** može pomoći upravitelju projekta kod razvrstavanja rezervacija više resursa u dodjele zadataka.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="9e2b0-122">To se ne izvodi automatski jer u bilo kojem scenariju koji je složeniji od jednostavnog primjera gore, kao što je slučaj gdje postoji skupina zadataka koji čine zahtjev ili namjera upravitelja projekta za dodjeljivanjem mora biti prepoznata od strane sustava.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="9e2b0-123">Budući da sustav ne može razumjeti namjeru, vjerojatnije je kako će se pretpostavke razlikovati od namjere i pojavit će se netočan ili nepredvidljiv rezultat.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="9e2b0-124">Predvidljiv ishod je da generički resurs ostaje dodijeljen dok upravitelj projekta namjerno ne izradi dodjele, uz pomoć prikaza **Usklađivanje**.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>

