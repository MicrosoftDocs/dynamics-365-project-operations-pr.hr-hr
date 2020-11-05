---
title: Pregled cjenovnih veličina
description: U ovoj se temi nalaze informacije o dimenzijama određivanja cijena u aplikaciji Dynamics 365 Project Operations.
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073495"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="ed5ce-103">Pregled cjenovnih veličina</span><span class="sxs-lookup"><span data-stu-id="ed5ce-103">Pricing dimensions overview</span></span>

<span data-ttu-id="ed5ce-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ed5ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed5ce-105">Dimenzije koje se koriste u ljudskim resursima za postavljanje cijena i troškova spadaju u dvije kategorije:</span><span class="sxs-lookup"><span data-stu-id="ed5ce-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="ed5ce-106">Osobe</span><span class="sxs-lookup"><span data-stu-id="ed5ce-106">People</span></span>
- <span data-ttu-id="ed5ce-107">Planirani rad</span><span class="sxs-lookup"><span data-stu-id="ed5ce-107">Planned work</span></span>

<span data-ttu-id="ed5ce-108">Zbog toga postoje dvije vrste dostupnih vrijednosti dimenzija za određivanje cijena:</span><span class="sxs-lookup"><span data-stu-id="ed5ce-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="ed5ce-109">**Skupovi mogućnosti** : dimenzije koje su fiksne enumeracije za skup vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="ed5ce-110">**Vrijednosti temeljene na entitetima** : dimenzije koje mogu biti različiti skup vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="ed5ce-111">Cjenovne veličine</span><span class="sxs-lookup"><span data-stu-id="ed5ce-111">Pricing dimensions</span></span>

<span data-ttu-id="ed5ce-112">Dynamics 365 Project Operations isporučuje se sa zadanim skupom dimenzija za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="ed5ce-113">Te dimenzije za određivanje cijena možete pregledati tako da odete na **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="ed5ce-114">U zapisu parametra na kartici **Dimenzije cijena temeljene na iznosu** potvrdite da uloga **msdyn_resourcecategory** i organizacijska jedinica za resurse **msdyn_organizationalunit** sadrže polja **Primjenjivo na prodaju** i **Primjenjivo na trošak** postavljena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="ed5ce-115">Ako su ta polja omogućena, možete postaviti cijenu i trošak za svaku kombinaciju uloge i organizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="ed5ce-116">Ako trebate odrediti cijenu ili trošak resursa pomoću dodatnih atributa, možete stvoriti prilagođena polja, entitete i dimenzije.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="ed5ce-117">Određivanje cijene vremena ljudskog resursa</span><span class="sxs-lookup"><span data-stu-id="ed5ce-117">Pricing human resource time</span></span>
<span data-ttu-id="ed5ce-118">Način na koji tvrtka ili ustanova određuje cijenu vremena ljudskog resursa često je važno strateško razmatranje koje izravno utječe na profitabilnost tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="ed5ce-119">Surađujte s financijskim timovima i voditeljima kada je vaša tvrtka ili ustanova spremna identificirati način na koji želi postaviti naplatu i stope troškova za vrijeme ljudskog resursa.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="ed5ce-120">Druga razmatranja za određivanje cijena uključuju želite li ponovno koristiti polja ili entitete koji trenutačno ne određuju cijene dimenzija, ali se primjenjuju kao dimenzija cijena za vašu tvrtku ili ustanovu.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="ed5ce-121">Polja kao što su **Kategorija transakcije** ( **msdyn_transactioncategory** ) i **Resurs koji je moguće rezervirati** ( **bookableresource** ) primjeri su dimenzija kandidata.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="ed5ce-122">Razmotrite treba li dimenzija određivanja cijena biti tablica ili skup mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="ed5ce-123">Ako predviđate promjene vrijednosti dimenzije koja će premašiti 10 ili 12, a potrebni su vam dodatni atributi tih vrijednosti, možete stvoriti entitet umjesto skupa mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="ed5ce-124">Održavanje skupa mogućnosti, kao što je dodavanje ili uklanjanje vrijednosti, zahtijeva administratora ili razvojnog programera dok dodavanje novih redaka u tablicu može izvršiti većina korisnika.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="ed5ce-125">Sljedeći primjer prikazuje stope naplate postavljene na temelju uloge i organizacijske jedinice za resurse kojoj resurs pripada.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="ed5ce-126">Stope troškova obično se temelje na platnom razredu zaposlenika i organizacijskoj jedinici kojoj pripadaju.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="ed5ce-127">U ovom primjeru tablice stopa naplate i stopa troškovaa izgledat će kao sljedeće.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="ed5ce-128">**Primjeri stopa naplate**</span><span class="sxs-lookup"><span data-stu-id="ed5ce-128">**Sample bill rates**</span></span>

| <span data-ttu-id="ed5ce-129">Uloga</span><span class="sxs-lookup"><span data-stu-id="ed5ce-129">Role</span></span>        | <span data-ttu-id="ed5ce-130">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="ed5ce-130">Org Unit</span></span>    |<span data-ttu-id="ed5ce-131">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ed5ce-131">Unit</span></span>      |<span data-ttu-id="ed5ce-132">Cijena</span><span class="sxs-lookup"><span data-stu-id="ed5ce-132">Price</span></span>      |<span data-ttu-id="ed5ce-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="ed5ce-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ed5ce-134">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="ed5ce-134">Developer</span></span>   | <span data-ttu-id="ed5ce-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ed5ce-135">Contoso US</span></span>  |<span data-ttu-id="ed5ce-136">Hour</span><span class="sxs-lookup"><span data-stu-id="ed5ce-136">Hour</span></span> | <span data-ttu-id="ed5ce-137">200</span><span class="sxs-lookup"><span data-stu-id="ed5ce-137">200</span></span>|<span data-ttu-id="ed5ce-138">USD</span><span class="sxs-lookup"><span data-stu-id="ed5ce-138">USD</span></span>     |
| <span data-ttu-id="ed5ce-139">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="ed5ce-139">Developer</span></span>   | <span data-ttu-id="ed5ce-140">Contoso, Indija</span><span class="sxs-lookup"><span data-stu-id="ed5ce-140">Contoso India</span></span> |<span data-ttu-id="ed5ce-141">Hour</span><span class="sxs-lookup"><span data-stu-id="ed5ce-141">Hour</span></span>|   <span data-ttu-id="ed5ce-142">112</span><span class="sxs-lookup"><span data-stu-id="ed5ce-142">112</span></span>|<span data-ttu-id="ed5ce-143">USD</span><span class="sxs-lookup"><span data-stu-id="ed5ce-143">USD</span></span>     |


<span data-ttu-id="ed5ce-144">**Primjeri stopa troškova**</span><span class="sxs-lookup"><span data-stu-id="ed5ce-144">**Sample cost rates**</span></span>

| <span data-ttu-id="ed5ce-145">Platni razred</span><span class="sxs-lookup"><span data-stu-id="ed5ce-145">Salary Band</span></span>     | <span data-ttu-id="ed5ce-146">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="ed5ce-146">Org Unit</span></span>    |<span data-ttu-id="ed5ce-147">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ed5ce-147">Unit</span></span>      |<span data-ttu-id="ed5ce-148">Cijena</span><span class="sxs-lookup"><span data-stu-id="ed5ce-148">Price</span></span>      |<span data-ttu-id="ed5ce-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="ed5ce-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ed5ce-150">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="ed5ce-150">My company_Band1</span></span> | <span data-ttu-id="ed5ce-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ed5ce-151">Contoso US</span></span>  |<span data-ttu-id="ed5ce-152">Hour</span><span class="sxs-lookup"><span data-stu-id="ed5ce-152">Hour</span></span> | <span data-ttu-id="ed5ce-153">145</span><span class="sxs-lookup"><span data-stu-id="ed5ce-153">145</span></span>|<span data-ttu-id="ed5ce-154">USD</span><span class="sxs-lookup"><span data-stu-id="ed5ce-154">USD</span></span>     |
| <span data-ttu-id="ed5ce-155">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="ed5ce-155">My company_Band2</span></span> | <span data-ttu-id="ed5ce-156">Contoso, Indija</span><span class="sxs-lookup"><span data-stu-id="ed5ce-156">Contoso India</span></span> |<span data-ttu-id="ed5ce-157">Hour</span><span class="sxs-lookup"><span data-stu-id="ed5ce-157">Hour</span></span>|   <span data-ttu-id="ed5ce-158">67</span><span class="sxs-lookup"><span data-stu-id="ed5ce-158">67</span></span>|<span data-ttu-id="ed5ce-159">USD</span><span class="sxs-lookup"><span data-stu-id="ed5ce-159">USD</span></span>     |
