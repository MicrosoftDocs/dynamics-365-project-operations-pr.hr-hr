---
title: Isključivanje cjenovne veličine
description: U ovoj se temi nalaze informacije o načinu isključivanja cjenovnih veličina.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650040"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="5a802-103">Isključivanje cjenovne veličine</span><span class="sxs-lookup"><span data-stu-id="5a802-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="5a802-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="5a802-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a802-105">Možda ćete morati pregledati i ažurirati svoju strategiju određivanja cijena svakih nekoliko godina.</span><span class="sxs-lookup"><span data-stu-id="5a802-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="5a802-106">Za ažuriranja koja izvršite možda bude potrebno da isključite postojeću dimenziju cijena i stvorite novu.</span><span class="sxs-lookup"><span data-stu-id="5a802-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="5a802-107">Na primjer, možda ste prethodno određivali cijenu po dimenziji **Uloga**, ali sada ste odlučili određivati cijenu po dimenziji **Radno iskustvo**.</span><span class="sxs-lookup"><span data-stu-id="5a802-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="5a802-108">To od vas može zatražiti da isključite **Ulogu** kao cjenovnu veličinu i kao novu cjenovnu veličinu stvorite **Radno iskustvo**.</span><span class="sxs-lookup"><span data-stu-id="5a802-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="5a802-109">Isključivanje dimenzije cijena, bez obzira na to je li unaprijed pripremljena ili prilagođena, možete provesti postavljanjem polja **Primjenjivo na trošak** i **Primjenjivo na prodaju** za dimenzije cijena na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="5a802-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="5a802-110">Međutim, kada to učinite, možda ćete dobiti poruku o pogrešci **Cjenovna veličina ne može se ažurirati ili izbrisati ako postoje povezani podaci o cijenama.**</span><span class="sxs-lookup"><span data-stu-id="5a802-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Vjerojatnost pogreške poslovnog procesa kad se isključi dimenzija cijena](media/Business-Process-Error.png)

<span data-ttu-id="5a802-112">Ta poruka o pogrešci ukazuje na to da postoje zapisi cijena koji su prethodno postavljeni za dimenziju koja se isključuje.</span><span class="sxs-lookup"><span data-stu-id="5a802-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="5a802-113">Svi zapisi u recima **Cijena uloge** i **Provizija cijene uloge** koji se odnose na dimenziju moraju se izbrisati prije postavljanja primjenjivosti dimenzije na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="5a802-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="5a802-114">Ovo se pravilo odnosi na unaprijed pripremljene dimenzije cijena i na prilagođene dimenzije cijena koje ste izradili.</span><span class="sxs-lookup"><span data-stu-id="5a802-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="5a802-115">Ova provjera valjanosti provodi se zbog toga što svaki zapis **Cijena uloge** mora imati jedinstvenu kombinaciju veličina.</span><span class="sxs-lookup"><span data-stu-id="5a802-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="5a802-116">Na primjer, u cjeniku pod nazivom **Cijene koštanja za SAD, 2018.**, imate sljedeće retke **Cijena uloge**.</span><span class="sxs-lookup"><span data-stu-id="5a802-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="5a802-117">Radno mjesto – standardno</span><span class="sxs-lookup"><span data-stu-id="5a802-117">Standard Title</span></span>         | <span data-ttu-id="5a802-118">Org. jedinica</span><span class="sxs-lookup"><span data-stu-id="5a802-118">Org Unit</span></span>    |<span data-ttu-id="5a802-119">Jedinica</span><span class="sxs-lookup"><span data-stu-id="5a802-119">Unit</span></span>   |<span data-ttu-id="5a802-120">Cijena</span><span class="sxs-lookup"><span data-stu-id="5a802-120">Price</span></span>  |<span data-ttu-id="5a802-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="5a802-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="5a802-122">Inženjer sustava</span><span class="sxs-lookup"><span data-stu-id="5a802-122">Systems Engineer</span></span>|<span data-ttu-id="5a802-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5a802-123">Contoso US</span></span>|<span data-ttu-id="5a802-124">Hour</span><span class="sxs-lookup"><span data-stu-id="5a802-124">Hour</span></span>| <span data-ttu-id="5a802-125">100</span><span class="sxs-lookup"><span data-stu-id="5a802-125">100</span></span>|<span data-ttu-id="5a802-126">USD</span><span class="sxs-lookup"><span data-stu-id="5a802-126">USD</span></span>|
| <span data-ttu-id="5a802-127">Viši inženjer sustava</span><span class="sxs-lookup"><span data-stu-id="5a802-127">Senior Systems Engineer</span></span>|<span data-ttu-id="5a802-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5a802-128">Contoso US</span></span>|<span data-ttu-id="5a802-129">Hour</span><span class="sxs-lookup"><span data-stu-id="5a802-129">Hour</span></span>| <span data-ttu-id="5a802-130">150</span><span class="sxs-lookup"><span data-stu-id="5a802-130">150</span></span>| <span data-ttu-id="5a802-131">USD</span><span class="sxs-lookup"><span data-stu-id="5a802-131">USD</span></span>|


<span data-ttu-id="5a802-132">Kada kao cjenovnu veličinu isključite **Standardni naslov**, a cjenovna veličina i modul za određivanje cijene pretražuje cijenu, upotrebljava se samo vrijednost **Org. jedinica** iz konteksta unosa.</span><span class="sxs-lookup"><span data-stu-id="5a802-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="5a802-133">Ako je **Org. jedinica** ulaznog konteksta „Contoso US”, rezultat će biti neodređen jer se oba retka podudaraju.</span><span class="sxs-lookup"><span data-stu-id="5a802-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="5a802-134">Kako biste to izbjegli, kada stvorite zapise **Cijena uloge**, sustav provjerava je li kombinacija veličina jedinstvena.</span><span class="sxs-lookup"><span data-stu-id="5a802-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="5a802-135">Ako je dimenzija isključena nakon stvaranja zapisa **Cijena uloge**, ovo ograničenje može biti prekršeno.</span><span class="sxs-lookup"><span data-stu-id="5a802-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="5a802-136">Stoga je potrebno da prije nego što isključite dimenziju izbrišete sve retke **Cijena uloge** i **Provizija cijene uloge** koji imaju tu vrijednost dimenzije.</span><span class="sxs-lookup"><span data-stu-id="5a802-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
