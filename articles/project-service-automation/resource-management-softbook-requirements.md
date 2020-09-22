---
title: Promjenjivo rezerviranje preduvjeta
description: Ova tema pruža informacije o tome kako promjenjivo rezervirati preduvjete.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 97323b73-c6de-4a7f-b889-19d4c42cf17a
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 08a8b46ee03fb93b30d178756e38c3086880f774
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750202"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="c5db1-103">Promjenjivo rezerviranje preduvjeta</span><span class="sxs-lookup"><span data-stu-id="c5db1-103">Soft-book requirements</span></span>

<span data-ttu-id="c5db1-104">Preduvjet resursa može biti fiksno rezerviran.</span><span class="sxs-lookup"><span data-stu-id="c5db1-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="c5db1-105">Fiksno rezerviranje stvara prijedlog koji iskorištava kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="c5db1-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="c5db1-106">Prijedlog se zatim šalje natrag podnositelju zahtjeva na odobrenje.</span><span class="sxs-lookup"><span data-stu-id="c5db1-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="c5db1-107">Promjenjivo rezerviranje uvjetno dodaje resurs u projektni tim i ima drugačiji status na ploči s rasporedom, ali ne iskorištava kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="c5db1-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="c5db1-108">Za promjenjivo rezerviranje resursa na ploči s rasporedom postavite polje **Status rezervacije** na **Promjenjivo**.</span><span class="sxs-lookup"><span data-stu-id="c5db1-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Status rezervacije postavljen je na Promjenjivo](media/Resource-Management-image77.png)

<span data-ttu-id="c5db1-110">Kada je kartica **Tim** u prikazu **Imenovani članovi tima**, resurs se prikazuje tamo.</span><span class="sxs-lookup"><span data-stu-id="c5db1-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="c5db1-111">Promjenjivo rezervirani sati zabilježeni su u stupcu **Promjenjivo rezervirani sati**.</span><span class="sxs-lookup"><span data-stu-id="c5db1-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Promjenjivo rezervirani sati u prikazu Imenovani članovi tima](media/Resource-Management-image78.png)

<span data-ttu-id="c5db1-113">Promjenjivo rezervirani članovi tima ne mogu biti dodijeljeni zadacima.</span><span class="sxs-lookup"><span data-stu-id="c5db1-113">Soft-booked team members can be assigned to tasks.</span></span>

![Promjenjivo rezervirani član tima dodijeljen zadatku](media/Resource-Management-image79.png)

<span data-ttu-id="c5db1-115">Na kartici **Usklađivanje** nema prikazanih rezervacija za promjenjivo rezervirani resurs jer se na kartici **Usklađivanje** bilježe samo fiksne rezervacije.</span><span class="sxs-lookup"><span data-stu-id="c5db1-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Promjenjivo rezervirani resurs bez rezervacija na kartici Usklađivanje](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="c5db1-117">Ne možete promjenjivo rezervirati resurs iz preduvjeta koji je generiran iz generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="c5db1-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="c5db1-118">Na ploči s rasporedom promjenjive rezervacije za resurs označene su drugom bojom.</span><span class="sxs-lookup"><span data-stu-id="c5db1-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Promjenjive rezervacije na ploči s rasporedom](media/Resource-Management-image81.png)

<span data-ttu-id="c5db1-120">Da biste promjenjivu rezervaciju pretvorili u fiksnu rezervaciju, na ploči s rasporedom kliknite desnom tipkom miša na promjenjivu rezervaciju, a zatim odaberite **Promjena statusa** \> **Fiksna rezervacija** \> **Fiksno**.</span><span class="sxs-lookup"><span data-stu-id="c5db1-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Promjena statusa rezervacije u Fiksno](media/Resource-Management-image82.png)

<span data-ttu-id="c5db1-122">Rezervacija je promijenjena, a status se mijenja na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="c5db1-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="c5db1-123">Budući da je status rezervacije sada **Fiksno**, resurs se prikazuje kao rezerviran, a njegov kapacitet i dostupnost su prilagođeni.</span><span class="sxs-lookup"><span data-stu-id="c5db1-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="c5db1-124">Pomoću iste metode možete otkazati fiksnu rezervaciju ili promjenjivu rezervaciju na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="c5db1-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="c5db1-125">Da biste promjenjivo rezervirani resurs pretvorili u fiksno rezervirani resurs na kartici **Tim** projekta, odaberite resurs, a zatim **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="c5db1-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Potvrda naredbe](media/Resource-Management-image83.png)
