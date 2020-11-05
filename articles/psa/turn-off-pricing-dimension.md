---
title: Isključivanje dimenzije cijena
description: Ova tema pokazuje kako postaviti dimenzije cijena u rješenju Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
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
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073473"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="407cf-103">Isključivanje dimenzije cijena</span><span class="sxs-lookup"><span data-stu-id="407cf-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="407cf-104">Možda ćete morati pregledati i ažurirati svoju strategiju određivanja cijena svakih nekoliko godina.</span><span class="sxs-lookup"><span data-stu-id="407cf-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="407cf-105">Za ažuriranja koja izvršite možda bude potrebno da isključite postojeću dimenziju cijena i stvorite novu.</span><span class="sxs-lookup"><span data-stu-id="407cf-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="407cf-106">Na primjer, možda ste prethodno određivali cijenu po dimenziji **Uloga** , ali sada ste odlučili određivati cijenu po dimenziji **Radno iskustvo**.</span><span class="sxs-lookup"><span data-stu-id="407cf-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="407cf-107">To može zahtijevati da isključite dimenziju **Uloga** kao dimenziju cijena i izradite dimenziju **Radno iskustvo** kao novu dimenziju cijena.</span><span class="sxs-lookup"><span data-stu-id="407cf-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="407cf-108">Isključivanje dimenzije cijena, bez obzira na to je li unaprijed pripremljena ili prilagođena, možete provesti postavljanjem polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** za dimenzije cijena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="407cf-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="407cf-109">No, kada to učinite, možda ćete primiti sljedeću poruku o pogrešci.</span><span class="sxs-lookup"><span data-stu-id="407cf-109">However, when you do this, you might receive the following error message.</span></span>

![Vjerojatnost pogreške poslovnog procesa kad se isključi dimenzija cijena](media/Business-Process-Error.png)


<span data-ttu-id="407cf-111">Ta poruka o pogrešci ukazuje na to da postoje zapisi cijena koji su prethodno postavljeni za dimenziju koja se isključuje.</span><span class="sxs-lookup"><span data-stu-id="407cf-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="407cf-112">Svi zapisi u recima **Cijena uloge** i **Provizija cijene uloge** koji se odnose na dimenziju moraju se izbrisati prije postavljanja primjenjivosti dimenzije na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="407cf-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="407cf-113">Ovo se pravilo odnosi na unaprijed pripremljene dimenzije cijena i na prilagođene dimenzije cijena koje ste izradili.</span><span class="sxs-lookup"><span data-stu-id="407cf-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="407cf-114">Ova provjera valjanosti provodi se zbog toga što Project Service ima ograničenje da svaki zapis retka **Cijena uloge** mora imati jedinstvenu kombinaciju dimenzija.</span><span class="sxs-lookup"><span data-stu-id="407cf-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="407cf-115">Na primjer, u cjeniku pod nazivom **Stope troška za SAD, 2018.** , imate sljedeće retke **Cijena uloge**.</span><span class="sxs-lookup"><span data-stu-id="407cf-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="407cf-116">Radno mjesto – standardno</span><span class="sxs-lookup"><span data-stu-id="407cf-116">Standard Title</span></span>         | <span data-ttu-id="407cf-117">Org. jedinica</span><span class="sxs-lookup"><span data-stu-id="407cf-117">Org Unit</span></span>    |<span data-ttu-id="407cf-118">Jedinica</span><span class="sxs-lookup"><span data-stu-id="407cf-118">Unit</span></span>   |<span data-ttu-id="407cf-119">Cijena</span><span class="sxs-lookup"><span data-stu-id="407cf-119">Price</span></span>  |<span data-ttu-id="407cf-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="407cf-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="407cf-121">Inženjer sustava</span><span class="sxs-lookup"><span data-stu-id="407cf-121">Systems Engineer</span></span>|<span data-ttu-id="407cf-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="407cf-122">Contoso US</span></span>|<span data-ttu-id="407cf-123">Hour</span><span class="sxs-lookup"><span data-stu-id="407cf-123">Hour</span></span>| <span data-ttu-id="407cf-124">100</span><span class="sxs-lookup"><span data-stu-id="407cf-124">100</span></span>|<span data-ttu-id="407cf-125">USD</span><span class="sxs-lookup"><span data-stu-id="407cf-125">USD</span></span>|
| <span data-ttu-id="407cf-126">Viši inženjer sustava</span><span class="sxs-lookup"><span data-stu-id="407cf-126">Senior Systems Engineer</span></span>|<span data-ttu-id="407cf-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="407cf-127">Contoso US</span></span>|<span data-ttu-id="407cf-128">Hour</span><span class="sxs-lookup"><span data-stu-id="407cf-128">Hour</span></span>| <span data-ttu-id="407cf-129">150</span><span class="sxs-lookup"><span data-stu-id="407cf-129">150</span></span>| <span data-ttu-id="407cf-130">USD</span><span class="sxs-lookup"><span data-stu-id="407cf-130">USD</span></span>|


<span data-ttu-id="407cf-131">Kada isključite **Radno mjesto – standardno** kao dimenziju cijena, a modul za određivanje cijena Project Service pretražuje cijenu, upotrebljava se samo vrijednost **Org. jedinica** iz ulaznog konteksta.</span><span class="sxs-lookup"><span data-stu-id="407cf-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="407cf-132">Ako je **Org. jedinica** ulaznog konteksta „Contoso US”, rezultat će biti neodređen jer se oba retka podudaraju.</span><span class="sxs-lookup"><span data-stu-id="407cf-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="407cf-133">Da biste to izbjegli, kada stvorite zapise **Cijena uloge** , Project Service provjerava je li kombinacija dimenzija jedinstvena.</span><span class="sxs-lookup"><span data-stu-id="407cf-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="407cf-134">Ako je dimenzija isključena nakon stvaranja zapisa **Cijena uloge** , ovo ograničenje može biti prekršeno.</span><span class="sxs-lookup"><span data-stu-id="407cf-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="407cf-135">Stoga je potrebno da prije nego što isključite dimenziju izbrišete sve retke **Cijena uloge** i **Provizija cijene uloge** koji imaju tu vrijednost dimenzije.</span><span class="sxs-lookup"><span data-stu-id="407cf-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

