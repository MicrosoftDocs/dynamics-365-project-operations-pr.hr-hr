---
title: Pregledavanje predloženih resursa
description: Ova tema pruža informacije o tome kako predložiti resurse projekta.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073355"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="6bbf1-103">Pregledavanje predloženih resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-103">Review proposed resources</span></span>

<span data-ttu-id="6bbf1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="6bbf1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6bbf1-105">Upravitelji resursa mogu predložiti resurs voditelju projekta pomoću zahtjeva za resurs.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="6bbf1-106">Odaberite **Pronađi resurse** u rešetki zahtjeva ili u samom zahtjevu.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="6bbf1-107">Na stranici **Pomoćnik za raspored** odaberite resurs, a zatim u oknu **Stvaranje rezervacije resursa** u polju **Status rezervacije** odaberite **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="6bbf1-108">Pojavljuju se sljedeća ažuriranja statusa:</span><span class="sxs-lookup"><span data-stu-id="6bbf1-108">The following status updates occur:</span></span>

- <span data-ttu-id="6bbf1-109">Na stranici **Pomoćnik za raspored** pokazatelji statusa ažuriraju se kako bi bilo jasno da je rezervacija predložena, a ne fiksno rezervirana.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="6bbf1-110">Na zahtjevu za resurs status se mijenja u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="6bbf1-111">Na kartici **Tim** projekta vrijednost **Status zahtjeva** člana generičkog tima mijenja se u **Potreban pregled**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="6bbf1-112">Voditelj projekta može prihvatiti ili odbaciti prijedlog.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="6bbf1-113">Kada upravitelji resursa obrađuju zahtjeve za resurs, mogu upotrijebiti neki od sljedećih pristupa:</span><span class="sxs-lookup"><span data-stu-id="6bbf1-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="6bbf1-114">Predlaganje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi odradio potrebne sate.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="6bbf1-115">Predloženi sati zatim se dijele na više resursa koji mogu odraditi potrebne sate.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="6bbf1-116">U ovom scenariju sati se ne smiju preklapati.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="6bbf1-117">Predložite manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="6bbf1-118">U ovom scenariju predloženi kapacitet resursa je manji od potrebnih sati koje je odredio podnositelj zahtjeva.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="6bbf1-119">Zbog toga se, kad podnositelj zahtjeva prihvati predložene resurse, stvara neispunjeni zahtjev za resurs koji pokriva preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="6bbf1-120">Rezerviranje više resursa kako bi se zadovoljila potražnja ako nije dostupan jedan resurs koji bi dovršio posao.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="6bbf1-121">Rezervirajte manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-121">Book fewer resources than are required.</span></span> <span data-ttu-id="6bbf1-122">U ovom scenariju rezerviranih je sati manje od potrebnih sati.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="6bbf1-123">Sustav vas upućuje da predložite resurse umjesto rezervacija, tako da podnositelj zahtjeva može provjeriti valjanost i pratiti preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="6bbf1-124">Naplativa upotreba</span><span class="sxs-lookup"><span data-stu-id="6bbf1-124">Billable utilization</span></span>

<span data-ttu-id="6bbf1-125">Resursi mogu imati ciljanu naplativu upotrebu.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="6bbf1-126">Ova ciljana upotreba definira se kao atribut u zadanoj ulozi resursa ili je postavljena na zapisu pojedinačnog resursa koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="6bbf1-127">Izračuni upotrebe temelje se na stvarnim satima koje su resursi prijavili pomoću odobrenih vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="6bbf1-128">Formule u nastavku služe za izračun upotrebe:</span><span class="sxs-lookup"><span data-stu-id="6bbf1-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="6bbf1-129">Naplativa upotreba = naplativi stvarni sati ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="6bbf1-130">Nenaplativa upotreba = stvarno vrijeme s ID-om vrste naplate = nenaplativo, besplatno ili nije dostupno ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="6bbf1-131">Interno = stvarno vrijeme bez prodajnog ugovora ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="6bbf1-132">Kapacitet resursa = radno vrijeme resursa – izvan ureda – neradni dani</span><span class="sxs-lookup"><span data-stu-id="6bbf1-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="6bbf1-133">Prikaz **Upotreba resursa** možete pronaći u oknu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="6bbf1-134">Svaka ćelija u rešetki predstavlja postotak naplative upotrebe resursa u razdoblju, kao što je dan, tjedan ili mjesec.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="6bbf1-135">Formule u nastavku služe za označavanje ćelija bojom:</span><span class="sxs-lookup"><span data-stu-id="6bbf1-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="6bbf1-136">**Zelena:** naplativa upotreba \>= ciljna upotreba resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="6bbf1-137">**Žuta:** ciljna upotreba – 20 \<= naplativa upotreba \< ciljna upotreba</span><span class="sxs-lookup"><span data-stu-id="6bbf1-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="6bbf1-138">**Crvena:** naplativa upotreba \< ciljna upotreba – 20</span><span class="sxs-lookup"><span data-stu-id="6bbf1-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="6bbf1-139">Budući da se prikaz **Upotreba resursa** temelji na ploči s rasporedom, možete filtrirati rezultate pomoću mogućnosti filtriranja na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="6bbf1-140">U rešetki je potrebno postaviti ciljnu upotrebu za svaku ulogu ili pojedinačni resurs.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="6bbf1-141">Da biste to učinili, otvorite **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="6bbf1-142">Osim toga, svakom resursu koji se može rezervirati potrebno je dodijeliti zadanu ulogu.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="6bbf1-143">Otvorite **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="6bbf1-144">Na kartici **Project Service** provjerite je li definirana uloga resursa i je li polje **Zadano je** postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="6bbf1-145">Možete dodati dodatne uloge ako je polje **Zadano je = Ne**.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="6bbf1-146">Uloga u kojoj se koristi polje **Zadano je = Da** služi za procjenu upotrebe resursa u odnosu na cilj za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="6bbf1-147">Na kartici **Project Service** možete postaviti i pojedinačnu ciljnu upotrebu za resurs.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="6bbf1-148">Izračun upotrebe zatim upotrebljava ciljnu upotrebu da bi se procijenio cilj resursa, a ne cilj zadane uloge resursa.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="6bbf1-149">Upotreba se prikazuje za resurs samo ako taj resurs ima odobreno naplativo vrijeme tijekom razdoblja koje je prikazano u rešetki.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="6bbf1-150">dostupnost resursa</span><span class="sxs-lookup"><span data-stu-id="6bbf1-150">Resource availability</span></span>

<span data-ttu-id="6bbf1-151">Ključno je da upravitelji resursa mogu pregledavati dostupnost resursa i ažurirati rezervacije.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="6bbf1-152">U nekim slučajevima ne postoji službena potražnja (zahtjev za resurs), ali upravitelj resursa mora odgovoriti na neplaniranu potražnju koja dolazi putem kanala kao što su e-pošta, telefonski poziv ili izravna poruka.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="6bbf1-153">Upravitelji resursa ažuriraju resurse i rezervacije na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="6bbf1-154">Radno vrijeme resursa koristi se kao osnova za izračun dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="6bbf1-155">Rezervacije resursa iskorištavaju kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="6bbf1-156">Na ploči s rasporedom boje i sjenčanje označavaju rezervacije, dostupnost i prekomjerne rezervacije, kao i status rezervacija.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="6bbf1-157">Postavka u postavkama ploče s rasporedom omogućuje prikaz legende.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="6bbf1-158">Ako se strelica udesno prikazuje pokraj pojedinačnog resursa koji se može rezervirati na ploči s rasporedom, resurs se može proširiti da bi se prikazale pojedinosti posla za koji je resurs rezerviran.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="6bbf1-159">Budući da Dynamics 365 Project Operations upotrebljava modul Universal Resource Scheduling, ako imate instaliranu uslugu Dynamics 365 Field Service, možete pregledati pojedinosti o rezervacijama resursa za projekte, radne naloge i sve druge entitete na koje ste proširili planiranje.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="6bbf1-160">Za prikaz dodatnih pojedinosti o pojedinačnom resursu desnom tipkom miša kliknite resurs za otvaranje kartice resursa.</span><span class="sxs-lookup"><span data-stu-id="6bbf1-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

