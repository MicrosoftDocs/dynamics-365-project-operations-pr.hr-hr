---
title: Rezerviranje za projekt
description: U ovoj temi nalaze se informacije o načinu rezervacije resursa za projekt.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 15de5735ba6d25994a68192ebdf80aefec772d6e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998807"
---
# <a name="book-to-a-project"></a><span data-ttu-id="a5307-103">Rezerviranje za projekt</span><span class="sxs-lookup"><span data-stu-id="a5307-103">Book to a project</span></span>

<span data-ttu-id="a5307-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="a5307-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a5307-105">Postoje slučajevi u kojima će voditelj projekta ili voditelj resursa trebati dodijeliti resurs projektu bez da generički član tima definira određeni zahtjev.</span><span class="sxs-lookup"><span data-stu-id="a5307-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="a5307-106">To se može postići na jedan od tri načina.</span><span class="sxs-lookup"><span data-stu-id="a5307-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="a5307-107">Rezervacija iz rešetke člana tima.</span><span class="sxs-lookup"><span data-stu-id="a5307-107">Book from the team member grid</span></span>
- <span data-ttu-id="a5307-108">Rezerviranje s ploče s rasporedom</span><span class="sxs-lookup"><span data-stu-id="a5307-108">Book from the schedule board</span></span>
- <span data-ttu-id="a5307-109">Rezervacija iz obrasca **Projekt**</span><span class="sxs-lookup"><span data-stu-id="a5307-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="a5307-110">Rezervacija iz rešetke člana tima.</span><span class="sxs-lookup"><span data-stu-id="a5307-110">Book from the team member grid</span></span>

<span data-ttu-id="a5307-111">Ako vaša tvrtka ili ustanova radi u hibridnom načinu raspodjele resursa, voditelj projekta može rezervirati resurs izravno projektu izvršavajući sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="a5307-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="a5307-112">Iz projekta idite na rešetku člana tima i odaberite mogućnost **Novi**.</span><span class="sxs-lookup"><span data-stu-id="a5307-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="a5307-113">Definirajte naziv položaja i ulogu resursa.</span><span class="sxs-lookup"><span data-stu-id="a5307-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="a5307-114">Odaberite resurs koji možete rezervirati iz dostupnog pretraživanja.</span><span class="sxs-lookup"><span data-stu-id="a5307-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="a5307-115">Nakon što odaberete resurs, definirajte sljedeće podatke o polju kako biste rezervirali resurs:</span><span class="sxs-lookup"><span data-stu-id="a5307-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="a5307-116">Datum početka</span><span class="sxs-lookup"><span data-stu-id="a5307-116">Start date</span></span>
    - <span data-ttu-id="a5307-117">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="a5307-117">Finish date</span></span>
    - <span data-ttu-id="a5307-118">Način dodjele</span><span class="sxs-lookup"><span data-stu-id="a5307-118">Allocation method</span></span>
    - <span data-ttu-id="a5307-119">Sati, ako je primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a5307-119">Hours, if applicable</span></span>
    - <span data-ttu-id="a5307-120">Odobravatelj projekta</span><span class="sxs-lookup"><span data-stu-id="a5307-120">Project approver</span></span>

6. <span data-ttu-id="a5307-121">Odaberite **Spremi i zatvori**</span><span class="sxs-lookup"><span data-stu-id="a5307-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="a5307-122">Rezerviranje s ploče s rasporedom</span><span class="sxs-lookup"><span data-stu-id="a5307-122">Book from the schedule board</span></span>

<span data-ttu-id="a5307-123">Kada upravitelj resursa treba rezervirati resurs izravno projektu, može upotrijebiti ploču s rasporedom i zahtjev projekta.</span><span class="sxs-lookup"><span data-stu-id="a5307-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="a5307-124">Preduvjet projekta preduvjet je resursa koji je uvijek dostupan za rezerviranje.</span><span class="sxs-lookup"><span data-stu-id="a5307-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="a5307-125">Kako biste rezervirali izravno obrascu projekta ploče s rasporedom, izvršite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="a5307-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="a5307-126">Pomaknite se do ploče s rasporedom i na lijevoj stranici filtrirajte resurse koje razmatrate za zahtjev.</span><span class="sxs-lookup"><span data-stu-id="a5307-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="a5307-127">U donjem oknu odaberite karticu **Projekt** za prikaz popisa projektnih zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="a5307-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="a5307-128">Povucite zahtjev na resurs i definirajte sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="a5307-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="a5307-129">Datum početka</span><span class="sxs-lookup"><span data-stu-id="a5307-129">Start date</span></span>
    - <span data-ttu-id="a5307-130">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="a5307-130">Finish date</span></span>
    - <span data-ttu-id="a5307-131">Status rezervacije</span><span class="sxs-lookup"><span data-stu-id="a5307-131">Booking status</span></span>
    - <span data-ttu-id="a5307-132">Način rezervacije</span><span class="sxs-lookup"><span data-stu-id="a5307-132">Booking method</span></span>
    - <span data-ttu-id="a5307-133">Trajanje</span><span class="sxs-lookup"><span data-stu-id="a5307-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="a5307-134">Rezervacija iz obrasca Projekt</span><span class="sxs-lookup"><span data-stu-id="a5307-134">Book from the Project form</span></span>

<span data-ttu-id="a5307-135">Kao voditelj projekta, možda ćete trebati rezervirati resurs za projekt, ali znate samo kriterije, a ne i naziv resursa.</span><span class="sxs-lookup"><span data-stu-id="a5307-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="a5307-136">Izvršite sljedeće korake kako biste s pomoću pomoćnika za raspored pronašli resurs utemeljen na nekom dostupnom atributu resursa.</span><span class="sxs-lookup"><span data-stu-id="a5307-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="a5307-137">Pomaknite se do projekta i odaberite mogućnost **Rezerviraj** kako biste otvorili pomoćnika za raspored.</span><span class="sxs-lookup"><span data-stu-id="a5307-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="a5307-138">S pomoću filtara s lijeve strane pomoćnika za raspored suzite kriterije i odaberite mogućnost **Traži**.</span><span class="sxs-lookup"><span data-stu-id="a5307-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="a5307-139">Na temelju resursa vraćenih u rezultatima, možete rezervirati resurs.</span><span class="sxs-lookup"><span data-stu-id="a5307-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="a5307-140">Ova metoda ne stvara nikakve rezervacije za resurs.</span><span class="sxs-lookup"><span data-stu-id="a5307-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="a5307-141">Umjesto toga, ona resurs dodaje timu.</span><span class="sxs-lookup"><span data-stu-id="a5307-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="a5307-142">Nakon što je član tima dodan u projekt, voditelj projekta može upotrijebiti održavanje rezervacija ili produžiti rezervacije kako bi potrebne resurse dodao resursu.</span><span class="sxs-lookup"><span data-stu-id="a5307-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]