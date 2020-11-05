---
title: Upravljanje vremenskim zonama
description: Kada se stvori projekt, njegova vremenska zona temelji se na vremenskoj zoni definiranoj u primijenjenom predlošku radnog vremena.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073326"
---
# <a name="manage-time-zones"></a><span data-ttu-id="56c01-103">Upravljanje vremenskim zonama</span><span class="sxs-lookup"><span data-stu-id="56c01-103">Manage time zones</span></span>

<span data-ttu-id="56c01-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="56c01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="56c01-105">Projekti</span><span class="sxs-lookup"><span data-stu-id="56c01-105">Projects</span></span>

<span data-ttu-id="56c01-106">Kada se stvori projekt, vremenska zona temelji se na vremenskoj zoni definiranoj u primijenjenom predlošku radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="56c01-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="56c01-107">Na obrascu **Projekt** datumi su uvijek u odnosu s vremenskom zonom korisnika koji je prijavljen na svakoj kartici, osim kartice **Zadatak**. Kada pogledate strukturnu analizu rada, datumi će se uvijek prikazivati u vremenskoj zoni projekta.</span><span class="sxs-lookup"><span data-stu-id="56c01-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="56c01-108">Zadaci</span><span class="sxs-lookup"><span data-stu-id="56c01-108">Tasks</span></span>

<span data-ttu-id="56c01-109">Kada se stvori zadatak, vrijeme početka, vrijeme završetka i sati/dan kontroliraju se radnim vremenom projekta.</span><span class="sxs-lookup"><span data-stu-id="56c01-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="56c01-110">Na primjer, ako je zadatak stvoren s projektom čija je vremenska zona – 8 PST i ima sljedeće radno vrijeme: 9:00 do 17:00, od ponedjeljka do petka, svaki zadatak stvoren bez dodjele poštivat će vrijeme početka i vrijeme završetka kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="56c01-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="56c01-111">Upravljanje resursima s pomoću vremenskih zona</span><span class="sxs-lookup"><span data-stu-id="56c01-111">Manage resources with time zones</span></span>

<span data-ttu-id="56c01-112">Za točne i predvidljive rezultate tijekom uporabe mogućnosti **Produlji rezervaciju** , dva su ključna preduvjeta koja se moraju ispuniti:</span><span class="sxs-lookup"><span data-stu-id="56c01-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="56c01-113">Korisnik mora konfigurirati vremensku zonu svog uređaja tako da odgovara vremenskoj zoni definiranoj u stavci **Postavke personalizacije** sustava.</span><span class="sxs-lookup"><span data-stu-id="56c01-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Postavke vremenske zone u programu Windows 10](media/reconcile-assignments-03.png)

  ![Postavke vremenske zone u personaliziranim postavkama](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="56c01-116">Resurs koji se može rezervirati mora imati najmanje jednu minutu radnog vremena koje se preklapa s konturama koje se upotrebljavaju za određivanje traženog produljenja.</span><span class="sxs-lookup"><span data-stu-id="56c01-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="56c01-117">Na primjer, sljedeći resursi s radnim vremenom koje pada između 9:00 i 19:00 sati.</span><span class="sxs-lookup"><span data-stu-id="56c01-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Usporedba kontura resursa](media/reconcile-assignments-05.png)

<span data-ttu-id="56c01-119">Tablice u nastavku prikazuju:</span><span class="sxs-lookup"><span data-stu-id="56c01-119">The following table shows:</span></span>

- <span data-ttu-id="56c01-120">Predložak kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="56c01-120">A project calendar template</span></span>
- <span data-ttu-id="56c01-121">Resurs A: Ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekt.</span><span class="sxs-lookup"><span data-stu-id="56c01-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="56c01-122">Vrijeme početka rezervacija bit će 9:00.</span><span class="sxs-lookup"><span data-stu-id="56c01-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="56c01-123">Resurs B: Ovaj se resurs nalazi u različitoj vremenskoj zoni od projekta i započinje u 7:00 u svojoj vremenskoj zoni.</span><span class="sxs-lookup"><span data-stu-id="56c01-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="56c01-124">Međutim, rezervacije će započeti u 9:00, jer je to najranije vrijeme početka konture dodjele.</span><span class="sxs-lookup"><span data-stu-id="56c01-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="56c01-125">Resursi C i D: Resursi se nalaze u različitim vremenskim zonama koje se razlikuju i međusobno i od projekta, a njihove rezervacije započinju najranije od odgovarajućih dostupnih vremena početka.</span><span class="sxs-lookup"><span data-stu-id="56c01-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="56c01-126">Entitet</span><span class="sxs-lookup"><span data-stu-id="56c01-126">Entity</span></span>  |<span data-ttu-id="56c01-127">Kalendar</span><span class="sxs-lookup"><span data-stu-id="56c01-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="56c01-128">Predložak kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="56c01-128">Project calendar template</span></span>   | ![kalendar projekta](media/reconcile-assignments-06.png) |
|<span data-ttu-id="56c01-130">Resurs A</span><span class="sxs-lookup"><span data-stu-id="56c01-130">Resource A</span></span>  | ![Kalendar resursa A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="56c01-132">Resurs B</span><span class="sxs-lookup"><span data-stu-id="56c01-132">Resource B</span></span>  |  ![Kalendar resursa B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="56c01-134">Resurs C</span><span class="sxs-lookup"><span data-stu-id="56c01-134">Resource C</span></span>  |  ![Kalendar resursa C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="56c01-136">Resurs D</span><span class="sxs-lookup"><span data-stu-id="56c01-136">Resource D</span></span>  | ![Kalendar resursa D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="56c01-138">Kada prijeđete na prikaz **Usklađivanje** , prikazuju se dodjele resursa i pridruženi nedostaci rezervacija.</span><span class="sxs-lookup"><span data-stu-id="56c01-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Prikaz usklađivanja prije produljena](media/reconcile-assignments-10.png)

<span data-ttu-id="56c01-140">Nakon što se za svaki resurs upotrijebi funkcija produljenog rezerviranja, rezervacije se uspješno produljuju za svaki resurs, jer se radno vrijeme svakog resursa preklapa s konturama nedostatka.</span><span class="sxs-lookup"><span data-stu-id="56c01-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Prikaz usklađivanja nakon produljena rezervacije](media/reconcile-assignments-11.png) 

<span data-ttu-id="56c01-142">Vidjet ćete kako podrobniji uvid u pojedinosti rezervacije pokazuje razlike u vremenu početka rezervacija.</span><span class="sxs-lookup"><span data-stu-id="56c01-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="56c01-143">Rezervacije započinju najranije s vremenom početka kontura dodjele i ne prije dostupnog vremena početka resursa.</span><span class="sxs-lookup"><span data-stu-id="56c01-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nove rezervacije resursa u ploči s rasporedom](media/reconcile-assignments-12.png)
