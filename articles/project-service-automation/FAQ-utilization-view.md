---
title: Prikaži naplativo korištenje za resurse
description: Ova tema pruža informacije o prikazu korištenja resursa.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750073"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="4cd67-103">Prikaži naplativo korištenje za resurse</span><span class="sxs-lookup"><span data-stu-id="4cd67-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="4cd67-104">**Prikaz korištenja** na stranici **Korištenje resursa programa Project Service** prikazuje naplativo korištenje za svaki resurs koji je moguće rezervirati.</span><span class="sxs-lookup"><span data-stu-id="4cd67-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="4cd67-105">Budući da se taj prikaz temelji na ploči s rasporedom, pronaći ćete mnoge iste funkcije.</span><span class="sxs-lookup"><span data-stu-id="4cd67-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Snimka zaslona prikaza korištenja](media/FAQ-utilization-1.png)
 

<span data-ttu-id="4cd67-107">Naplativo korištenje izračunava se na sljedeći način:</span><span class="sxs-lookup"><span data-stu-id="4cd67-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="4cd67-108">Naplativo korištenje = (Naplativi stvarni sati) / (kapacitet resursa)</span><span class="sxs-lookup"><span data-stu-id="4cd67-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="4cd67-109">Ćelije predstavljaju izračunato naplativo korištenje za odabrano razdoblje (dani, tjedni ili mjeseci).</span><span class="sxs-lookup"><span data-stu-id="4cd67-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="4cd67-110">Boje u ćelijama predstavljaju naplativo korištenje za resurs u usporedbi s njegovim ciljnim naplativim korištenjem.</span><span class="sxs-lookup"><span data-stu-id="4cd67-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="4cd67-111">Ciljno korištenje može se postaviti na zadanu ulogu resursa ili na sam određeni resurs.</span><span class="sxs-lookup"><span data-stu-id="4cd67-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="4cd67-112">Izračun prvo uzima u obzir pojedinačni za cilj, a zatim zadanu ulogu resursa.</span><span class="sxs-lookup"><span data-stu-id="4cd67-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="4cd67-113">Postavi cilj na resurs</span><span class="sxs-lookup"><span data-stu-id="4cd67-113">Set target on a resource</span></span>

1. <span data-ttu-id="4cd67-114">Otvorite **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="4cd67-115">Odaberite resurs da biste otvorili zapis.</span><span class="sxs-lookup"><span data-stu-id="4cd67-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="4cd67-116">Na kartici **Project Service**, možete postaviti ciljno korištenje resursa.</span><span class="sxs-lookup"><span data-stu-id="4cd67-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Snimka zaslona s prikazom postavljanja ciljnog korištenja s pomoću kartice Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="4cd67-118">Postavi ciljno korištenje na ulogu</span><span class="sxs-lookup"><span data-stu-id="4cd67-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="4cd67-119">Idite na **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="4cd67-120">Odaberite ulogu i otvorite zapis.</span><span class="sxs-lookup"><span data-stu-id="4cd67-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="4cd67-121">Postavite ciljno korištenje za ulogu.</span><span class="sxs-lookup"><span data-stu-id="4cd67-121">Set the target utilization for the role.</span></span>

> ![Snimka zaslona s prikazom postavljanja ciljnog korištenja s pomoću Uloga resursa](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="4cd67-123">Izračunaj naplativo korištenje za resurs</span><span class="sxs-lookup"><span data-stu-id="4cd67-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="4cd67-124">Da biste izračunali naplativo korištenje za resurs, morate ispuniti neke preduvjete.</span><span class="sxs-lookup"><span data-stu-id="4cd67-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="4cd67-125">Postavi zadanu ulogu za pojedinačni resurs</span><span class="sxs-lookup"><span data-stu-id="4cd67-125">Set default role for individual resource</span></span>

<span data-ttu-id="4cd67-126">Najprije, ciljno korištenje mora se postaviti na pojedinačni resurs ili na uloge resursa.</span><span class="sxs-lookup"><span data-stu-id="4cd67-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="4cd67-127">Ako za ciljeve upotrebljavate uloge resursa, svaki pojedinačni resurs mora imati zadanu ulogu.</span><span class="sxs-lookup"><span data-stu-id="4cd67-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="4cd67-128">Da biste to postavili, idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="4cd67-129">Odaberite resurs, otvorite zapis, a zatim odaberite karticu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="4cd67-130">U rešetki **Uloga resursa**, provjerite postoji li jedna uloga za resurs i je li **Zadana** postavljena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="4cd67-131">Promijeni vrstu naplate za ulogu resursa</span><span class="sxs-lookup"><span data-stu-id="4cd67-131">Change billing type for resource role</span></span>

<span data-ttu-id="4cd67-132">Uloge resursa moraju se postaviti tako da im je vrsta naplate **Naplativa**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="4cd67-133">Idite na **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="4cd67-134">Otvorite zapis koji želite ažurirati, a zatim postavite zadanu postavku vrste naplate na **Naplativa**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="4cd67-135">Postavi radno vrijeme za ulogu resursa</span><span class="sxs-lookup"><span data-stu-id="4cd67-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="4cd67-136">Da bi izračun kapaciteta bio moguć, za resurs mora biti postavljeno radno vrijeme.</span><span class="sxs-lookup"><span data-stu-id="4cd67-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="4cd67-137">Otvorite **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="4cd67-138">Odaberite resurs da biste otvorili zapis pa odaberite stavku **Prikaži radno vrijeme**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="4cd67-139">Možete skupno ažurirati popis resursa primjenom **Predložak radnog vremena** s prikaza **Popis resursa**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="4cd67-140">Uklanjanje poteškoća s naplativim stvarnim satima</span><span class="sxs-lookup"><span data-stu-id="4cd67-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="4cd67-141">Naplativi stvarni sati preuzimaju se iz entiteta **Stvarne vrijednosti**.</span><span class="sxs-lookup"><span data-stu-id="4cd67-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="4cd67-142">Stvarne vrijednosti s vrstom naplate **Naplativa** uključeni su u izračun i stoga morate imati projekte u kojima su stvarne vrijednosti naplative.</span><span class="sxs-lookup"><span data-stu-id="4cd67-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="4cd67-143">Ako nije prikazano naplativo korištenje, evo nekih stvari koje možete provjeriti:</span><span class="sxs-lookup"><span data-stu-id="4cd67-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="4cd67-144">je li za kapacitet resursa postavljeno radno vrijeme;</span><span class="sxs-lookup"><span data-stu-id="4cd67-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="4cd67-145">je li resursu dodijeljen pojedinačno definiran cilj korištenja ili mu je dodijeljena zadana uloga;</span><span class="sxs-lookup"><span data-stu-id="4cd67-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="4cd67-146">je li za ulogu definiran cilj korištenja;</span><span class="sxs-lookup"><span data-stu-id="4cd67-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="4cd67-147">Stvarne vrijednosti imaju vrstu naplate **Naplativa** za razdoblje za koje očekujete izračun korištenja.</span><span class="sxs-lookup"><span data-stu-id="4cd67-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="4cd67-148">Provjerite sljedeće ako su prikazane stvarne vrijednosti s drugačijim vrstama naplate od naplative:</span><span class="sxs-lookup"><span data-stu-id="4cd67-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="4cd67-149">je li zadana vrsta naplate za ulogu koja je upotrijebljena na stvarnoj vrijednosti drugačija od naplative;</span><span class="sxs-lookup"><span data-stu-id="4cd67-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="4cd67-150">je li uloga na retku ugovora projekta koja podržava projekt postavljena na nenaplativa;</span><span class="sxs-lookup"><span data-stu-id="4cd67-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="4cd67-151">je li projektu pridružen redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="4cd67-151">The project does not have an associated contract line.</span></span>

