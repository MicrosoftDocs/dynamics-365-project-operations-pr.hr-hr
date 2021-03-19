---
title: Početna stranica Dimenzije cijena i troškova
description: Ova tema pruža pregled dimenzija cijena.
author: rumant
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
ms.openlocfilehash: 137fee27dd2302d47ae12faccde1682cff43db93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284124"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="79d75-103">Početna stranica Dimenzije cijena i troškova</span><span class="sxs-lookup"><span data-stu-id="79d75-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="79d75-104">Na dimenzije koje se upotrebljavaju za određivanje cijena i troškova rada u tvrtkama i ustanovama koje se temelje na projektu utječu sljedeći atributi:</span><span class="sxs-lookup"><span data-stu-id="79d75-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="79d75-105">Ljudi koji rade posao sličan svojem iskustvu, ulozi ili zemljopisnom području</span><span class="sxs-lookup"><span data-stu-id="79d75-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="79d75-106">Posao koji treba odraditi slično složenosti ili dobu dana</span><span class="sxs-lookup"><span data-stu-id="79d75-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="79d75-107">S obzirom na tipičnu prirodu ovih atributa posla i ljudi koji su potrebni za obavljanje posla, u aplikaciji Project Service Automation dostupne su dvije vrste vrijednosti dimenzija za određivanje cijena:</span><span class="sxs-lookup"><span data-stu-id="79d75-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="79d75-108">**Skupovi mogućnosti** – Atributi koji su fiksni popisi skupa vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="79d75-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="79d75-109">**Entitetne vrijednosti** – Atributi koji mogu imati različit skup vrijednosti koji je konačan, ali se može mijenjati tijekom vremena.</span><span class="sxs-lookup"><span data-stu-id="79d75-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="79d75-110">Cjenovne veličine</span><span class="sxs-lookup"><span data-stu-id="79d75-110">Pricing dimensions</span></span>

<span data-ttu-id="79d75-111">PSA se isporučuje sa zadanim skupom dimenzija cijena.</span><span class="sxs-lookup"><span data-stu-id="79d75-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="79d75-112">Možete ih pregledati tako da idete na **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="79d75-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="79d75-113">U zapisu parametra na kartici **Dimenzije cijena temeljene na iznosu** potvrdite da uloga **msdyn_resourcecategory** i organizacijska jedinica za resurse **msdyn_organizationalunit** sadrže polja **Primjenjivo na prodaju** i **Primjenjivo na trošak** postavljena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="79d75-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="79d75-114">To će vam omogućiti da postavite cijenu i trošak za svaku kombinaciju uloge i organizacijske jedinice.</span><span class="sxs-lookup"><span data-stu-id="79d75-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Snimka zaslona parametara sustava Project Service s istaknutom mogućnosti "Primjenjivo na prodaju"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="79d75-116">Ako ste upotrebljavali gotova polja uloge i organizacijske jedinice kao dimenzije cijena prije verzije 3 sustava PSA, neće biti vidljivih promjena.</span><span class="sxs-lookup"><span data-stu-id="79d75-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="79d75-117">Možete nastaviti uobičajeno koristiti aplikaciju Project Service.</span><span class="sxs-lookup"><span data-stu-id="79d75-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="79d75-118">Ako trebate odrediti cijenu ili trošak resursa pomoću dodatnih atributa, možete stvoriti prilagođena polja, entitete i dimenzije.</span><span class="sxs-lookup"><span data-stu-id="79d75-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="79d75-119">Za više informacija pogledajte sljedeće teme, međutim, napominjemo da morate dovršiti postupke redoslijedom navedenim u nastavku:</span><span class="sxs-lookup"><span data-stu-id="79d75-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="79d75-120">Stvaranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="79d75-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="79d75-121">Dodavanje prilagođenih polja postavljanju cijena i transakcijskim entitetima</span><span class="sxs-lookup"><span data-stu-id="79d75-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="79d75-122">Postavljanje prilagođenih polja kao cjenovnih veličina</span><span class="sxs-lookup"><span data-stu-id="79d75-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="79d75-123">Ažuriranje atributa dodatka za uključivanje novih dimenzija cijena</span><span class="sxs-lookup"><span data-stu-id="79d75-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="79d75-124">Određivanje cijene vremena ljudskog resursa</span><span class="sxs-lookup"><span data-stu-id="79d75-124">Pricing human resource time</span></span>
<span data-ttu-id="79d75-125">Način na koji tvrtka ili ustanova određuje cijenu vremena ljudskog resursa često je važno strateško razmatranje koje izravno utječe na profitabilnost tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="79d75-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="79d75-126">Surađujte s financijskim timovima i voditeljima kada je vaša tvrtka ili ustanova spremna identificirati način na koji želi postaviti naplatu i stope troškova za vrijeme ljudskog resursa.</span><span class="sxs-lookup"><span data-stu-id="79d75-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="79d75-127">Druga razmatranja za određivanje cijena uključuju želite li ponovno koristiti polja ili entitete koji trenutačno ne određuju cijene dimenzija, ali se primjenjuju kao dimenzija cijena za vašu tvrtku ili ustanovu.</span><span class="sxs-lookup"><span data-stu-id="79d75-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="79d75-128">Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji je moguće rezervirati** (**bookableresource**) primjeri su dimenzija kandidata.</span><span class="sxs-lookup"><span data-stu-id="79d75-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="79d75-129">Razmotrite treba li dimenzija određivanja cijena biti tablica ili skup mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="79d75-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="79d75-130">Ako predviđate promjene vrijednosti dimenzije koja će premašiti 10 ili 12, a potrebni su vam dodatni atributi tih vrijednosti, možete stvoriti entitet umjesto skupa mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="79d75-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="79d75-131">Održavanje skupa mogućnosti, kao što je dodavanje ili uklanjanje vrijednosti, zahtijeva administratora ili razvojnog programera dok dodavanje novih redaka u tablicu može izvršiti većina poslovnih korisnika.</span><span class="sxs-lookup"><span data-stu-id="79d75-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="79d75-132">Sljedeći primjer prikazuje stope naplate postavljene na temelju uloge i organizacijske jedinice za resurse kojoj resurs pripada.</span><span class="sxs-lookup"><span data-stu-id="79d75-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="79d75-133">Stope troškova obično se temelje na platnom razredu zaposlenika i organizacijskoj jedinici kojoj pripadaju.</span><span class="sxs-lookup"><span data-stu-id="79d75-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="79d75-134">U ovom primjeru tablice stopa naplate i stopa troškovaa izgledat će kao sljedeće.</span><span class="sxs-lookup"><span data-stu-id="79d75-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="79d75-135">**Primjeri stopa naplate**</span><span class="sxs-lookup"><span data-stu-id="79d75-135">**Sample bill rates**</span></span>

| <span data-ttu-id="79d75-136">Uloga</span><span class="sxs-lookup"><span data-stu-id="79d75-136">Role</span></span>        | <span data-ttu-id="79d75-137">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="79d75-137">Org Unit</span></span>    |<span data-ttu-id="79d75-138">Jedinica</span><span class="sxs-lookup"><span data-stu-id="79d75-138">Unit</span></span>      |<span data-ttu-id="79d75-139">Cijena</span><span class="sxs-lookup"><span data-stu-id="79d75-139">Price</span></span>      |<span data-ttu-id="79d75-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="79d75-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="79d75-141">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="79d75-141">Developer</span></span>   | <span data-ttu-id="79d75-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="79d75-142">Contoso US</span></span>  |<span data-ttu-id="79d75-143">Hour</span><span class="sxs-lookup"><span data-stu-id="79d75-143">Hour</span></span> | <span data-ttu-id="79d75-144">200</span><span class="sxs-lookup"><span data-stu-id="79d75-144">200</span></span>|<span data-ttu-id="79d75-145">USD</span><span class="sxs-lookup"><span data-stu-id="79d75-145">USD</span></span>     |
| <span data-ttu-id="79d75-146">Razvojni inženjer</span><span class="sxs-lookup"><span data-stu-id="79d75-146">Developer</span></span>   | <span data-ttu-id="79d75-147">Contoso, Indija</span><span class="sxs-lookup"><span data-stu-id="79d75-147">Contoso India</span></span> |<span data-ttu-id="79d75-148">Hour</span><span class="sxs-lookup"><span data-stu-id="79d75-148">Hour</span></span>|   <span data-ttu-id="79d75-149">112</span><span class="sxs-lookup"><span data-stu-id="79d75-149">112</span></span>|<span data-ttu-id="79d75-150">USD</span><span class="sxs-lookup"><span data-stu-id="79d75-150">USD</span></span>     |


<span data-ttu-id="79d75-151">**Primjeri stopa troškova**</span><span class="sxs-lookup"><span data-stu-id="79d75-151">**Sample cost rates**</span></span>

| <span data-ttu-id="79d75-152">Platni razred</span><span class="sxs-lookup"><span data-stu-id="79d75-152">Salary Band</span></span>     | <span data-ttu-id="79d75-153">Organizacijska jedinica</span><span class="sxs-lookup"><span data-stu-id="79d75-153">Org Unit</span></span>    |<span data-ttu-id="79d75-154">Jedinica</span><span class="sxs-lookup"><span data-stu-id="79d75-154">Unit</span></span>      |<span data-ttu-id="79d75-155">Cijena</span><span class="sxs-lookup"><span data-stu-id="79d75-155">Price</span></span>      |<span data-ttu-id="79d75-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="79d75-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="79d75-157">My company_Band1</span><span class="sxs-lookup"><span data-stu-id="79d75-157">My company_Band1</span></span> | <span data-ttu-id="79d75-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="79d75-158">Contoso US</span></span>  |<span data-ttu-id="79d75-159">Hour</span><span class="sxs-lookup"><span data-stu-id="79d75-159">Hour</span></span> | <span data-ttu-id="79d75-160">145</span><span class="sxs-lookup"><span data-stu-id="79d75-160">145</span></span>|<span data-ttu-id="79d75-161">USD</span><span class="sxs-lookup"><span data-stu-id="79d75-161">USD</span></span>     |
| <span data-ttu-id="79d75-162">My company_Band2</span><span class="sxs-lookup"><span data-stu-id="79d75-162">My company_Band2</span></span> | <span data-ttu-id="79d75-163">Contoso, Indija</span><span class="sxs-lookup"><span data-stu-id="79d75-163">Contoso India</span></span> |<span data-ttu-id="79d75-164">Hour</span><span class="sxs-lookup"><span data-stu-id="79d75-164">Hour</span></span>|   <span data-ttu-id="79d75-165">67</span><span class="sxs-lookup"><span data-stu-id="79d75-165">67</span></span>|<span data-ttu-id="79d75-166">USD</span><span class="sxs-lookup"><span data-stu-id="79d75-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]