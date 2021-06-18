---
title: Pregledavanje predloženih resursa
description: Ova tema pruža informacije o tome kako predložiti resurse projekta.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000742"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="b37ac-103">Pregledavanje predloženih resursa</span><span class="sxs-lookup"><span data-stu-id="b37ac-103">Review proposed resources</span></span>

<span data-ttu-id="b37ac-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b37ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b37ac-105">Upravitelji resursa mogu predložiti resurs voditelju projekta pomoću zahtjeva za resurs.</span><span class="sxs-lookup"><span data-stu-id="b37ac-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="b37ac-106">Odaberite **Pronađi resurse** u rešetki zahtjeva ili u samom zahtjevu.</span><span class="sxs-lookup"><span data-stu-id="b37ac-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="b37ac-107">Na stranici **Pomoćnik za raspored** odaberite resurs, a zatim u oknu **Stvaranje rezervacije resursa** u polju **Status rezervacije** odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="b37ac-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="b37ac-108">Pojavljuju se sljedeća ažuriranja statusa:</span><span class="sxs-lookup"><span data-stu-id="b37ac-108">The following status updates occur:</span></span>

- <span data-ttu-id="b37ac-109">Na stranici **Pomoćnik za raspored** pokazatelji statusa ažuriraju se kako bi bilo jasno da je rezervacija predložena, a ne fiksno rezervirana.</span><span class="sxs-lookup"><span data-stu-id="b37ac-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="b37ac-110">Na zahtjevu za resurs status se mijenja u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="b37ac-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="b37ac-111">Na kartici **Tim** projekta vrijednost **Status zahtjeva** člana generičkog tima mijenja se u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="b37ac-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="b37ac-112">Voditelj projekta može prihvatiti ili odbaciti prijedlog.</span><span class="sxs-lookup"><span data-stu-id="b37ac-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="b37ac-113">Kada upravitelji resursa obrađuju zahtjeve za resurs, mogu upotrijebiti neki od sljedećih pristupa:</span><span class="sxs-lookup"><span data-stu-id="b37ac-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="b37ac-114">Predlaganje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi odradio potrebne sate.</span><span class="sxs-lookup"><span data-stu-id="b37ac-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="b37ac-115">Predloženi sati zatim se dijele na više resursa koji mogu odraditi potrebne sate.</span><span class="sxs-lookup"><span data-stu-id="b37ac-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="b37ac-116">U ovom scenariju sati se ne smiju preklapati.</span><span class="sxs-lookup"><span data-stu-id="b37ac-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="b37ac-117">Predložite manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="b37ac-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="b37ac-118">U ovom scenariju predloženi kapacitet resursa je manji od potrebnih sati koje je odredio podnositelj zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="b37ac-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="b37ac-119">Zbog toga se, kad podnositelj zahtjeva prihvati predložene resurse, stvara neispunjeni zahtjev za resurs koji pokriva preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="b37ac-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="b37ac-120">Rezerviranje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi dovršio posao.</span><span class="sxs-lookup"><span data-stu-id="b37ac-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="b37ac-121">Rezervirajte manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="b37ac-121">Book fewer resources than are required.</span></span> <span data-ttu-id="b37ac-122">U ovom scenariju rezerviranih je sati manje od potrebnih sati.</span><span class="sxs-lookup"><span data-stu-id="b37ac-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="b37ac-123">Sustav vas upućuje da predložite resurse umjesto rezervacija, tako da podnositelj zahtjeva može provjeriti valjanost i pratiti preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="b37ac-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="b37ac-124">dostupnost resursa</span><span class="sxs-lookup"><span data-stu-id="b37ac-124">Resource availability</span></span>

<span data-ttu-id="b37ac-125">Ključno je da upravitelji resursa mogu pregledavati dostupnost resursa i ažurirati rezervacije.</span><span class="sxs-lookup"><span data-stu-id="b37ac-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="b37ac-126">U nekim slučajevima ne postoji službena potražnja (zahtjev za resurs), ali upravitelj resursa mora odgovoriti na neplaniranu potražnju koja dolazi putem kanala kao što su e-pošta, telefonski poziv ili izravna poruka.</span><span class="sxs-lookup"><span data-stu-id="b37ac-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="b37ac-127">Upravitelji resursa ažuriraju resurse i rezervacije na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="b37ac-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="b37ac-128">Radno vrijeme resursa koristi se kao osnova za izračun dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="b37ac-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="b37ac-129">Rezervacije resursa iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="b37ac-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="b37ac-130">Na ploči s rasporedom boje i sjenčanje označavaju rezervacije, dostupnost i prekomjerne rezervacije, kao i status rezervacija.</span><span class="sxs-lookup"><span data-stu-id="b37ac-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="b37ac-131">Postavka u postavkama ploče s rasporedom omogućuje prikaz legende.</span><span class="sxs-lookup"><span data-stu-id="b37ac-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="b37ac-132">Ako se strelica udesno prikazuje pokraj pojedinačnog resursa koji se može rezervirati na ploči s rasporedom, resurs se može proširiti da bi se prikazale pojedinosti posla za koji je resurs rezerviran.</span><span class="sxs-lookup"><span data-stu-id="b37ac-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="b37ac-133">Budući da Dynamics 365 Project Operations upotrebljava modul Universal Resource Scheduling, a ako imate instaliranu značajku Dynamics 365 Field Service, možete pregledati pojedinosti o rezervacijama resursa za projekte, radne naloge i sve druge entitete na koje ste proširili zakazivanje.</span><span class="sxs-lookup"><span data-stu-id="b37ac-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="b37ac-134">Za prikaz dodatnih pojedinosti o pojedinačnom resursu desnom tipkom miša kliknite resurs za otvaranje kartice resursa.</span><span class="sxs-lookup"><span data-stu-id="b37ac-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]