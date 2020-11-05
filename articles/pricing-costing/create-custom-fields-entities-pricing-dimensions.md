---
title: Stvaranje prilagođenih polja i entitete kao cjenovnih veličina
description: U ovoj se temi nalaze informacije o načinu stvaranja prilagođenih skupova mogućnosti ili entiteta.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073426"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="03405-103">Stvaranje prilagođenih polja i entitete kao cjenovnih veličina</span><span class="sxs-lookup"><span data-stu-id="03405-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="03405-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="03405-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="03405-105">Dovršite sljedeće korake u bilo kojem trenutku kada želite stvoriti prilagođeni skup mogućnosti ili entitet.</span><span class="sxs-lookup"><span data-stu-id="03405-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03405-106">Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="03405-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="03405-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu.</span><span class="sxs-lookup"><span data-stu-id="03405-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="03405-108">Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="03405-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="03405-109">Izradi prilagođeno rješenje za dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="03405-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="03405-110">Idite na **Postavke** > **Rješenja** , a zatim odaberite **Novo** kako biste stvorili novo rješenje.</span><span class="sxs-lookup"><span data-stu-id="03405-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="03405-111">Rješenju dodijelite naziv **\<your organization name> dimenzije za određivanje cijena** , unesite preostale potrebne podatke, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="03405-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="03405-112">Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="03405-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="03405-113">Dimenzija određivanja cijena može biti skup mogućnosti ili entitet.</span><span class="sxs-lookup"><span data-stu-id="03405-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="03405-114">Oboje se moraju izraditi u vašem rješenju za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="03405-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="03405-115">Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="03405-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="03405-116">Dimenzije koje se temelje na entitetu</span><span class="sxs-lookup"><span data-stu-id="03405-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="03405-117">Idite na **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="03405-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="03405-118">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="03405-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="03405-119">Odaberite **Novo** kako biste stvorili novi entitet pod nazivom **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="03405-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="03405-120">Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="03405-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="03405-121">Dimenzije koje se temelje na skupu mogućnosti</span><span class="sxs-lookup"><span data-stu-id="03405-121">Option set-based dimensions</span></span> 
<span data-ttu-id="03405-122">Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="03405-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="03405-123">Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.</span><span class="sxs-lookup"><span data-stu-id="03405-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="03405-124">Idite na **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="03405-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="03405-125">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Skupovi mogućnosti**.</span><span class="sxs-lookup"><span data-stu-id="03405-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="03405-126">Odaberite **Novo** kako biste stvorili novi skup mogućnosti, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="03405-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="03405-127">Izradi podatake za dimenzije koje se temeljene na entitetu</span><span class="sxs-lookup"><span data-stu-id="03405-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="03405-128">Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje.</span><span class="sxs-lookup"><span data-stu-id="03405-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="03405-129">Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="03405-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="03405-130">Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="03405-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="03405-131">Odaberite **Napredno pretraživanje** , odaberite entitet **Standardni naslov** , a zatim odaberite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="03405-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="03405-132">Prikazat će se svi redovi u entitetu **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="03405-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="03405-133">Odaberite **Novo** i upolju **Naziv** unesite „Inženjer sustava”, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="03405-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="03405-134">Zatvori obrazac.</span><span class="sxs-lookup"><span data-stu-id="03405-134">Close the form.</span></span> 
4. <span data-ttu-id="03405-135">Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".</span><span class="sxs-lookup"><span data-stu-id="03405-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="03405-136">Dodavanje svih potrebnih entiteta i povezanih komponenti u rješenje dimenzije za određivanje cijena</span><span class="sxs-lookup"><span data-stu-id="03405-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="03405-137">Morat ćete dodati sljedeće entitete svojem rješenju za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="03405-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="03405-138">Koristite ove korake u tom postupku da biste izvršili neke važne promjene sheme u rješenju određivanja cijena da bi entiteti prepoznali nove dimenzije određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="03405-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="03405-139">Odaberite **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="03405-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="03405-140">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Dodaj postojeći** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="03405-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="03405-141">U dijaloškom okviru **Komponente rješenja** odaberite sljedeće entitete:</span><span class="sxs-lookup"><span data-stu-id="03405-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="03405-142">Stvarna vrijednost</span><span class="sxs-lookup"><span data-stu-id="03405-142">Actual</span></span>
  - <span data-ttu-id="03405-143">Resurs koji se može rezervirati</span><span class="sxs-lookup"><span data-stu-id="03405-143">Bookable Resource</span></span>
  - <span data-ttu-id="03405-144">Redak procjene</span><span class="sxs-lookup"><span data-stu-id="03405-144">Estimate Line</span></span>
  - <span data-ttu-id="03405-145">Pojedinost retka fakture</span><span class="sxs-lookup"><span data-stu-id="03405-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="03405-146">Redak u dnevniku</span><span class="sxs-lookup"><span data-stu-id="03405-146">Journal Line</span></span>
  - <span data-ttu-id="03405-147">Pojedinost retka ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="03405-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="03405-148">Članov projektnog tima</span><span class="sxs-lookup"><span data-stu-id="03405-148">Project Team Member</span></span>
  - <span data-ttu-id="03405-149">Pojedinost retka ponude</span><span class="sxs-lookup"><span data-stu-id="03405-149">Quote Line Detail</span></span>
  - <span data-ttu-id="03405-150">Provizija cijene uloge</span><span class="sxs-lookup"><span data-stu-id="03405-150">Role Price Markup</span></span>
  - <span data-ttu-id="03405-151">Cijena uloge</span><span class="sxs-lookup"><span data-stu-id="03405-151">Role Price</span></span> 
  - <span data-ttu-id="03405-152">Vremenski unos</span><span class="sxs-lookup"><span data-stu-id="03405-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="03405-153">Obavezno uključite sve obrasce i prikaze za svaki odabrani entitet.</span><span class="sxs-lookup"><span data-stu-id="03405-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="03405-154">Kada se od vas zatraži da uključite ovisne entitete za odabrane entitete, odaberite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="03405-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

