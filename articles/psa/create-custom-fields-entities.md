---
title: Izradi prilagođena polja i entitete
description: U ovoj se temi pojašnjava način izrade skupova mogućnosti i entiteta u vlastitom rješenju na platformi Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144854"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="fa42b-103">Izradi prilagođena polja i entitete</span><span class="sxs-lookup"><span data-stu-id="fa42b-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fa42b-104">Izvršite sljedeće korake u bilo kojem trenutku kada želite izraditi prilagođeni skup mogućnosti ili entitet na platformi Power Apps.</span><span class="sxs-lookup"><span data-stu-id="fa42b-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="fa42b-105">Postupci u ovoj temi trebaju se izvršiti s pomoću web-sučelja sustava Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="fa42b-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa42b-106">Preporučujemo da sve promjene prilagođene dimenzije određivanja cijena izvršite u zasebnom rješenju.</span><span class="sxs-lookup"><span data-stu-id="fa42b-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="fa42b-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promjena po potrebi, pomoći će u ponovnom korištenju vašeg rada i olakšava prebacivanje tih promjena na drugu instancu.</span><span class="sxs-lookup"><span data-stu-id="fa42b-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="fa42b-108">Nakon što ste izvršili sve potrebne promjene, izvezite ovo rješenje kao **Upravljano rješenje** i uvezite ga u druge instance da biste ponovno upotrijebili postavljanje određivanja cijena.</span><span class="sxs-lookup"><span data-stu-id="fa42b-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="fa42b-109">Izradi prilagođena polja i skupove mogućnosti u rješenju dimenzije određivanja cijena</span><span class="sxs-lookup"><span data-stu-id="fa42b-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="fa42b-110">Dimenzija određivanja cijena može biti skup mogućnosti ili entitet.</span><span class="sxs-lookup"><span data-stu-id="fa42b-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="fa42b-111">Oboje se moraju izraditi u vašem rješenju za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="fa42b-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="fa42b-112">Koraci u ovom postupku objašnjavaju kako izraditi dimenzije koje se temelje na entitetima i dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="fa42b-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="fa42b-113">Dimenzije koje se temelje na entitetu</span><span class="sxs-lookup"><span data-stu-id="fa42b-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="fa42b-114">U PSA-u kliknite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="fa42b-115">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="fa42b-116">Kliknite **Novo** da biste izradili novi entitet pod nazivom **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="fa42b-117">Unesite preostale potrebne informacije, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija entiteta Standardni naslov](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="fa42b-119">Dimenzije koje se temelje na skupu mogućnosti</span><span class="sxs-lookup"><span data-stu-id="fa42b-119">Option set-based dimensions</span></span> 
<span data-ttu-id="fa42b-120">Možete izraditi dvije dimenzije koje se temelje na skupu mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="fa42b-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="fa42b-121">Koristite **Mjesto rada resursa** da biste pratili cijenu rada **Od kuće** i rada **Na radnom mjestu** i koristite **Radno vrijeme resursa** s vrijednostima **Redovito** i **Prekovremeno** da biste primijenili maržu kada se dovrši rad.</span><span class="sxs-lookup"><span data-stu-id="fa42b-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="fa42b-122">U PSA-u kliknite **Postavke** > **Rješenja** i zatim dvaput kliknite **\<your organization name> dimenzije za određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="fa42b-123">U istraživaču rješenja, u lijevom navigacijskom oknu, odaberite  **Skupovi mogućnosti**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="fa42b-124">Kliknite **Novo** da biste izradili novi skup mogućnosti, unesite preostale potrebne informacije, a zatim kliknite **Spremi.**</span><span class="sxs-lookup"><span data-stu-id="fa42b-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="fa42b-125">Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Lokacija rada resursa</span><span class="sxs-lookup"><span data-stu-id="fa42b-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="fa42b-126">Dimenzija određivanja cijena koja se temelji na skupu mogućnosti pod nazivom Radno vrijeme resursa</span><span class="sxs-lookup"><span data-stu-id="fa42b-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="fa42b-127">Izradi podatake za dimenzije koje se temeljene na entitetu</span><span class="sxs-lookup"><span data-stu-id="fa42b-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="fa42b-128">Podatke za dimenzije koje se temeljene na entitetu možete izraditi ručno ili s pomoću Microsoft Excel poziva za uvoz ili servisiranje.</span><span class="sxs-lookup"><span data-stu-id="fa42b-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="fa42b-129">Koristite korake u ovom postupku za izradu dvaju standardnih naslova, **Inženjer sustava** i **Viši inženjer sustava** iz dimenzije koja se temelji na entitetu, **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="fa42b-130">Ako su podaci koje želite izraditi mali, kao u sljedećem primjeru, možete koristiti standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="fa42b-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="fa42b-131">U sustavu PSA, Kliknite **Napredno pretraživanje**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="fa42b-132">Odaberite entitet **Standardni naslov** i zatim kliknite **Rezultati** .</span><span class="sxs-lookup"><span data-stu-id="fa42b-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="fa42b-133">Prikazat će se svi redovi u entitetu **Standardni naslov**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="fa42b-134">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-134">Click **New**.</span></span> <span data-ttu-id="fa42b-135">U polje **Naziv** unesite "Inženjer sustava", a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="fa42b-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="fa42b-136">Zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="fa42b-136">Close the form.</span></span> 
4. <span data-ttu-id="fa42b-137">Ponovite korake 1 - 3 za izradu drugog standardnog naslova za "Viši inženjer sustava".</span><span class="sxs-lookup"><span data-stu-id="fa42b-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="fa42b-138">Ogledni podaci za entitet Standardni naslov</span><span class="sxs-lookup"><span data-stu-id="fa42b-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


