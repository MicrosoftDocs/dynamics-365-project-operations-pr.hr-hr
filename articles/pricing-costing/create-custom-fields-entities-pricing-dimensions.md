---
title: Stvaranje prilagođenih polja i entitete kao cjenovnih veličina
description: U ovoj se temi nalaze informacije o načinu stvaranja prilagođenih skupova mogućnosti ili entiteta.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275619"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="7e5e6-103">Stvaranje prilagođenih polja i entitete kao cjenovnih veličina</span><span class="sxs-lookup"><span data-stu-id="7e5e6-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="7e5e6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="7e5e6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7e5e6-105">Poduzmite sljedeće korake kada želite izraditi prilagođeni skup mogućnosti ili entitet koji biste upotrebljavali kao veličinu za određivane cijene.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="7e5e6-106">Dodatne informacije potražite u odjeljku [Pregled veličina za određivanje cijene](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7e5e6-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="7e5e6-107">Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="7e5e6-108">Ova značajna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="7e5e6-109">To će pomoći i pri ponovnoj uporabi vašeg posla i olakšat će prijenos ovih promjena na drugu instancu. Nakon što izvršite sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance za ponovnu uporabu postavki cijena.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="7e5e6-110">Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="7e5e6-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="7e5e6-111">Dimenzija određivanja cijena može biti skup mogućnosti ili entitet.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="7e5e6-112">Oboje se moraju izraditi u vašem rješenju za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="7e5e6-113">Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="7e5e6-114">Dimenzije koje se temelje na entitetu</span><span class="sxs-lookup"><span data-stu-id="7e5e6-114">Entity-based dimensions</span></span>
<span data-ttu-id="7e5e6-115">Kako biste stvorili veličine koje se temelje na entitetu, slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="7e5e6-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="7e5e6-116">Idite na **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="7e5e6-117">U pregledniku rješenja, u lijevom navigacijskom oknu, odaberite mogućnost **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="7e5e6-118">Odaberite **Novo** kako biste stvorili novi entitet pod nazivom **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="7e5e6-119">Unesite preostale potrebne informacije, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="7e5e6-121">Dimenzije koje se temelje na skupu mogućnosti</span><span class="sxs-lookup"><span data-stu-id="7e5e6-121">Option set-based dimensions</span></span> 
<span data-ttu-id="7e5e6-122">Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="7e5e6-123">S pomoću stavke **Mjesto rada resursa** pratite cijene rada na mjestu **Početno** i rada **Na lokaciji**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="7e5e6-124">Upotrijebite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Tijekom vremena** kako biste primjenili proviziju kad se posao završi.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="7e5e6-125">Sljedeći grafika daje prikaz veličine **Mjesto rada resursa**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Lokacija rada resursa](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="7e5e6-127">Sljedeći grafika daje prikaz veličine **Radno vrijeme resursa**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Radno vrijeme resursa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="7e5e6-129">Idite na **Postavke** > **Rješenja** i dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="7e5e6-130">U pregledniku rješenja, u lijevom navigacijskom oknu, odaberite stavku **Skupovi mogućnosti**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="7e5e6-131">Odaberite **Novo** kako biste stvorili novi skup mogućnosti, unesite preostale potrebne podatke, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="7e5e6-132">Izradi podatake za dimenzije koje se temeljene na entitetu</span><span class="sxs-lookup"><span data-stu-id="7e5e6-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="7e5e6-133">Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="7e5e6-134">Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="7e5e6-135">Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="7e5e6-136">Odaberite **Napredno traženje**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="7e5e6-137">Odaberite entitet **Standardni naslov** i zatim **Rezultati** .</span><span class="sxs-lookup"><span data-stu-id="7e5e6-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="7e5e6-138">Prikazat će se svi redci u entitetu **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="7e5e6-139">Odaberite **Novo** i upolju **Naziv** unesite „Inženjer sustava”, a zatim odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="7e5e6-140">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="7e5e6-140">Close the page.</span></span> 
5. <span data-ttu-id="7e5e6-141">Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".</span><span class="sxs-lookup"><span data-stu-id="7e5e6-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Uzorak podataka za entitet Standardni naslov](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]