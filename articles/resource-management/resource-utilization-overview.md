---
title: Prikaz korištenja resursa
description: U ovoj temi nalaze se informacije o iskoristivosti resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401367"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="bd313-103">Prikaz korištenja resursa</span><span class="sxs-lookup"><span data-stu-id="bd313-103">Resource utilization overview</span></span>

<span data-ttu-id="bd313-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="bd313-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd313-105">Resursi mogu imati ciljanu naplativu upotrebu.</span><span class="sxs-lookup"><span data-stu-id="bd313-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="bd313-106">Ova ciljna iskoristivost definira se kao atribut u zadanoj ulozi resursa ili je postavljena na zapisu pojedinačnog resursa koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="bd313-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="bd313-107">Izračuni upotrebe temelje se na stvarnim satima koje su resursi prijavili pomoću odobrenih vremenskih unosa.</span><span class="sxs-lookup"><span data-stu-id="bd313-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="bd313-108">Formule u nastavku služe za izračun upotrebe:</span><span class="sxs-lookup"><span data-stu-id="bd313-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="bd313-109">Naplativa upotreba = naplativi stvarni sati ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="bd313-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="bd313-110">Nenaplativa upotreba = stvarno vrijeme s ID-om vrste naplate = nenaplativo, besplatno ili nije dostupno ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="bd313-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="bd313-111">Interno = stvarno vrijeme bez prodajnog ugovora ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="bd313-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="bd313-112">Kapacitet resursa = radno vrijeme resursa – izvan ureda – neradni dani</span><span class="sxs-lookup"><span data-stu-id="bd313-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="bd313-113">Prikaz **Upotreba resursa** možete pronaći u oknu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="bd313-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="bd313-114">Svaka ćelija u rešetki predstavlja postotak naplative upotrebe resursa u razdoblju, kao što je dan, tjedan ili mjesec.</span><span class="sxs-lookup"><span data-stu-id="bd313-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="bd313-115">Formule u nastavku služe za označavanje ćelija bojom:</span><span class="sxs-lookup"><span data-stu-id="bd313-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="bd313-116">**Zelena**: Naplativa iskoristivost >= Ciljna iskoristivost resursa</span><span class="sxs-lookup"><span data-stu-id="bd313-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="bd313-117">**Žuta**: Ciljna iskoristivost – 20 <= Naplativa iskoristivost < Ciljna iskoristivost.</span><span class="sxs-lookup"><span data-stu-id="bd313-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="bd313-118">**Crvena**: Naplativa iskoristivost < Ciljna iskoristivost – 20</span><span class="sxs-lookup"><span data-stu-id="bd313-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="bd313-119">Budući da se prikaz **Upotreba resursa** temelji na ploči s rasporedom, možete filtrirati rezultate pomoću mogućnosti filtriranja na ploči s rasporedom.</span><span class="sxs-lookup"><span data-stu-id="bd313-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="bd313-120">U rešetki je potrebno postaviti ciljnu upotrebu za svaku ulogu ili pojedinačni resurs.</span><span class="sxs-lookup"><span data-stu-id="bd313-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="bd313-121">Kako biste to učinili, idite na mogućnost **Resursi** > **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="bd313-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="bd313-122">Osim toga, svakom resursu koji se može rezervirati potrebno je dodijeliti zadanu ulogu.</span><span class="sxs-lookup"><span data-stu-id="bd313-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="bd313-123">Idite na mogućnost **Resursi** > **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="bd313-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="bd313-124">Na kartici **Project Service** provjerite je li definirana uloga resursa i je li polje **Zadano je** postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="bd313-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="bd313-125">Možete dodati dodatne uloge ako je polje **Zadano je** = **Ne**.</span><span class="sxs-lookup"><span data-stu-id="bd313-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="bd313-126">Uloga u kojoj se polje **Zadano je** = **Da** upotrebljava za procjenu iskoristivosti resursa u odnosu na cilj za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="bd313-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="bd313-127">Na kartici **Project Service** možete postaviti i pojedinačnu ciljnu upotrebu za resurs.</span><span class="sxs-lookup"><span data-stu-id="bd313-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="bd313-128">Izračun upotrebe zatim upotrebljava ciljnu upotrebu da bi se procijenio cilj resursa, a ne cilj zadane uloge resursa.</span><span class="sxs-lookup"><span data-stu-id="bd313-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="bd313-129">Iskoristivost se prikazuje za resurs samo ako taj resurs ima odobreno naplativo vrijeme tijekom razdoblja prikazanog u rešetki.</span><span class="sxs-lookup"><span data-stu-id="bd313-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>
