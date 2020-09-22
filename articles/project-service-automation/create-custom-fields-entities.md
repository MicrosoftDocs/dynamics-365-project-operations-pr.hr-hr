---
title: Izradi prilagođena polja i entitete
description: U ovoj se temi pojašnjava način izrade skupova mogućnosti i entiteta u vlastitom rješenju na platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750190"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="f0aac-103">Izradi prilagođena polja i entitete</span><span class="sxs-lookup"><span data-stu-id="f0aac-103">Create custom fields and entities</span></span> 

<span data-ttu-id="f0aac-104">Izvršite sljedeće korake u bilo kojem trenutku kada želite izraditi prilagođeni skup mogućnosti ili entitet na platformi Power Apps.</span><span class="sxs-lookup"><span data-stu-id="f0aac-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="f0aac-105">Postupci u ovoj temi trebaju se izvršiti s pomoću web-sučelja sustava Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f0aac-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0aac-106">Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="f0aac-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="f0aac-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu.</span><span class="sxs-lookup"><span data-stu-id="f0aac-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="f0aac-108">Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="f0aac-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="f0aac-109">Izradi prilagođeno rješenje za dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="f0aac-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="f0aac-110">U sustavu PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite **Novo** da biste izradili novo rješenje.</span><span class="sxs-lookup"><span data-stu-id="f0aac-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="f0aac-111">Rješenju dodijelite naziv **\<, naziv tvrtke ili ustanove >dimenzije određivanja cijena**, unesite preostale potrebne informacije, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Izrada prilagođenog rješenja za dimenzije određivanja cijena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="f0aac-113">Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="f0aac-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="f0aac-114">Dimenzija određivanja cijena može biti skup mogućnosti ili entitet.</span><span class="sxs-lookup"><span data-stu-id="f0aac-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="f0aac-115">Oboje se moraju izraditi u vašem rješenju za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="f0aac-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="f0aac-116">Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="f0aac-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="f0aac-117">Dimenzije koje se temelje na entitetu</span><span class="sxs-lookup"><span data-stu-id="f0aac-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="f0aac-118">U PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput **\<naziv organizacije> dimenzije određivanja cijena**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="f0aac-119">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="f0aac-120">Kliknite **Novo** da biste izradili novi entitet pod nazivom **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="f0aac-121">Unesite preostale potrebne informacije, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="f0aac-123">Dimenzije koje se temelje na skupu mogućnosti</span><span class="sxs-lookup"><span data-stu-id="f0aac-123">Option set-based dimensions</span></span> 
<span data-ttu-id="f0aac-124">Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="f0aac-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="f0aac-125">Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.</span><span class="sxs-lookup"><span data-stu-id="f0aac-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="f0aac-126">U sustavu PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput  **\<naziv organizacije> dimenzije određivanja cijena**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f0aac-127">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Skupovi mogućnosti**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="f0aac-128">Kliknite **Novo** da biste izradili novi skup mogućnosti, unesite preostale potrebne informacije, a zatim kliknite **Spremi.**</span><span class="sxs-lookup"><span data-stu-id="f0aac-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="f0aac-129">Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Lokacija rada resursa</span><span class="sxs-lookup"><span data-stu-id="f0aac-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="f0aac-130">Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Radno vrijeme resursa</span><span class="sxs-lookup"><span data-stu-id="f0aac-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="f0aac-131">Izradi podatake za dimenzije koje se temeljene na entitetu</span><span class="sxs-lookup"><span data-stu-id="f0aac-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="f0aac-132">Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje.</span><span class="sxs-lookup"><span data-stu-id="f0aac-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="f0aac-133">Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="f0aac-134">Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="f0aac-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="f0aac-135">U sustavu PSA, Kliknite **Napredno pretraživanje**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="f0aac-136">Odaberite entitet **Standardni naslov** i zatim kliknite **Rezultati** .</span><span class="sxs-lookup"><span data-stu-id="f0aac-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="f0aac-137">Prikazat će se svi redovi u entitetu **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="f0aac-138">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-138">Click **New**.</span></span> <span data-ttu-id="f0aac-139">U polje **Naziv** unesite "Inženjer sustava", a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="f0aac-140">Zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="f0aac-140">Close the form.</span></span> 
4. <span data-ttu-id="f0aac-141">Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".</span><span class="sxs-lookup"><span data-stu-id="f0aac-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="f0aac-142">Ogledni podaci za entitet Standardni naslov</span><span class="sxs-lookup"><span data-stu-id="f0aac-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="f0aac-143">Dodaj sve potrebne entiteta sustava PSA i srodne komponente u rješenje dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="f0aac-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="f0aac-144">Morat ćete dodati sljedeće entitete programa Project Service u svoje rješenje za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="f0aac-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="f0aac-145">Koristite ove korake u tom postupku da biste izvršili neke važne promjene sheme u rješenju određivanja cijena da bi entiteti prepoznali nove dimenzije određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="f0aac-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="f0aac-146">U PSA, kliknite **Postavke** > **Rješenja**, a zatim kliknite dvaput **\<naziv organizacije> dimenzije određivanja cijena**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="f0aac-147">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="f0aac-148">U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:</span><span class="sxs-lookup"><span data-stu-id="f0aac-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="f0aac-149">Stvarna vrijednost</span><span class="sxs-lookup"><span data-stu-id="f0aac-149">Actual</span></span>
- <span data-ttu-id="f0aac-150">Resurs koji se može rezervirati</span><span class="sxs-lookup"><span data-stu-id="f0aac-150">Bookable Resource</span></span>
- <span data-ttu-id="f0aac-151">Redak procjene</span><span class="sxs-lookup"><span data-stu-id="f0aac-151">Estimate Line</span></span>
- <span data-ttu-id="f0aac-152">Pojedinost retka fakture</span><span class="sxs-lookup"><span data-stu-id="f0aac-152">Invoice Line Detail</span></span>
- <span data-ttu-id="f0aac-153">Redak u dnevniku</span><span class="sxs-lookup"><span data-stu-id="f0aac-153">Journal Line</span></span>
- <span data-ttu-id="f0aac-154">Pojedinost retka ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="f0aac-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="f0aac-155">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="f0aac-155">Project Team Member</span></span>
- <span data-ttu-id="f0aac-156">Pojedinost retka ponude</span><span class="sxs-lookup"><span data-stu-id="f0aac-156">Quote Line Detail</span></span>
- <span data-ttu-id="f0aac-157">Provizija cijene uloge</span><span class="sxs-lookup"><span data-stu-id="f0aac-157">Role Price Markup</span></span>
- <span data-ttu-id="f0aac-158">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="f0aac-158">Role Price</span></span> 
- <span data-ttu-id="f0aac-159">Unos vremena</span><span class="sxs-lookup"><span data-stu-id="f0aac-159">Time Entry</span></span> 

> ![Dodaj postojeće entitete u rješenje dimenzija određivanja cijena](media/Existing-entities-to-PD-solution.png)

> ![Odaberi komponente rješenja](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="f0aac-162">Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.</span><span class="sxs-lookup"><span data-stu-id="f0aac-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="f0aac-163">Kada se od vas zatraži da uključite ovisne entitete za odabrane entitete, kliknite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="f0aac-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ne, ne želim dodati sve povezane komponente.](media/Do-not-include-required.png)


