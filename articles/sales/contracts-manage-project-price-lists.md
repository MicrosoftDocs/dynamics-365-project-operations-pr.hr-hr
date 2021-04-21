---
title: Upravljanje cjenicima za projekt u ugovorima o projektu
description: U ovoj temi nalaze se informacije o upravljanju cjenicima za projekt u ugovorima o projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858554"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="ab1c6-103">Upravljanje cjenicima za projekt u ugovorima o projektu</span><span class="sxs-lookup"><span data-stu-id="ab1c6-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="ab1c6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ab1c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ab1c6-105">Ugovori o projektu u aplikaciji Dynamics 365 Project Operations osmišljeni su tako da u ugovoru podržavaju prodajne cjenike mjerodavne na više datuma.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="ab1c6-106">U aplikaciji Project Operations postoji novi povezani entitet naziva **Cjenici za projekt**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="ab1c6-107">Ovaj je entitet u odnosu jedan na više prema ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="ab1c6-108">Cjenici za projekte upotrebljavaju se za određivanje cijene vremena, materijala i transakcija troškova na projektu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-108">Project price lists are used to price time, material, and expense transactions on a project.</span></span> <span data-ttu-id="ab1c6-109">Kada ugovor ima jedan ili više cjenika za projekt, ti se cjenici upotrebljavaju za cijenu procijenjenih vremena, materijala, troškova i stvarnih podataka na projektima koji su povezani s ugovorom putem retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-109">When a contract has one or more project price lists, these price lists are used to price for time, material, expense estimates, and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="ab1c6-110">Kad na ugovoru o projektu ne postoje cjenici za projekt, vidjet ćete poruku upozorenja da ne postoje cjenici za projekt, a vaše procjene, stvarni rad na projektu, materijal i zabilježeni troškovi neće imati cijenu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, material, and expenses logged will not be priced.</span></span> <span data-ttu-id="ab1c6-111">Neće biti cijena za prodajne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="ab1c6-112">Povežite ili prekinite vezu cjenika za projekt s ugovorom o projektu</span><span class="sxs-lookup"><span data-stu-id="ab1c6-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a><span data-ttu-id="ab1c6-113">Stvaranje ili povezivanje određenog cjenika za procijenjeni rad, materijal i troškove koji se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="ab1c6-113">Create or associate a specific price list for estimating project-based work, material, and expenses</span></span>

1. <span data-ttu-id="ab1c6-114">Na ugovoru o projektu odaberite karticu **Cjenici za projekt**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="ab1c6-115">U podrešetki odaberite **+ Dodaj novi cjenik za projekt**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="ab1c6-116">Na klizaču **Brzo stvaranje** odaberite cjenik.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="ab1c6-117">Padajući popis prikazuje sve cjenike kojima je kontekst postavljen na **Prodaja**, pri čemu se valuta na cjeniku poklapa s valutom iz ugovora.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="ab1c6-118">Unesite opis za povezivanje cjenika za projekt, odaberite **Spremi**, a zatim zatvorite klizač **Brzo stvaranje**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="ab1c6-119">Stvoren je povezani cjenik projekta.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="ab1c6-120">Ponovite korake 1 – 4 kako biste povezali više od jednog cjenika za projekt s ugovorom o projektu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="ab1c6-121">Više cjenika za projekt stvorite samo ako imate različite datume stupanja na snagu na svakom povezanom cjeniku za projekt.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="ab1c6-122">Project Operations ne podržava preklapanje datuma stupanja na snagu cjenika za projekt.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="ab1c6-123">Ako postoji više cjenika za projekt za transakciju s danim datumom, cijena te transakcije bit će zadana na nulu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="ab1c6-124">Uklanjanje povezanosti cjenika za projekt</span><span class="sxs-lookup"><span data-stu-id="ab1c6-124">Remove a project price list association</span></span>

- <span data-ttu-id="ab1c6-125">Odaberite cjenik za projekt, a zatim na podrešetki odaberite **Izbriši cjenik ugovorna o projektu**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="ab1c6-126">Cjenik se uklanja iz cjenika za projekt na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="ab1c6-127">Sam cjenik neće se izbrisati.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="ab1c6-128">Izbrisat će se samo povezanost s ugovorom.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="ab1c6-129">Postavljanje automatskog zadavanje cjenika za projekt na ugovor</span><span class="sxs-lookup"><span data-stu-id="ab1c6-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="ab1c6-130">Cjenik projekta može se postaviti kao zadani cjenik projekta.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-130">A project price list can be set up as the default project price list.</span></span> <span data-ttu-id="ab1c6-131">Ova postavka osigurava da svi ugovori u vašoj tvrtki ili ustanovi uvijek započinju standardnim cjenikom za projekt u tom cjenovnom razdoblju.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-131">This setup ensures that all contracts in your organization always start with a standard project price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="ab1c6-132">Postavljanje organizacijski zadanih cjenika za projekt</span><span class="sxs-lookup"><span data-stu-id="ab1c6-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="ab1c6-133">Idite na **Postavke** > **Općenito**, a zatim odaberite **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="ab1c6-134">Na stranici s popisom **Aktivni parametri** odaberite i dvaput kliknite zapis kako biste ga otvorili.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="ab1c6-135">Kada dvaput kliknete, pazite da ne kliknete na vrijednost polja koja je hiperveza.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="ab1c6-136">Na stranici **Aktivni parametri** odaberite karticu **Cjenik**. Podrešetka prikazuje popis zadanih cjenika.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="ab1c6-137">Ovo je popis cjenika standardnih troškova i prodajnih cijena.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="ab1c6-138">Postojanje cjenika **Prodaja** povezanog ovdje za svaku valutu u kojoj obavljate prodaju osigurava da je prodajni cjenik zadan za bilo koji ugovor koji stvarate za klijente koji obavljaju transakcije u toj valuti.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="ab1c6-139">Postavljanje cjenika za projekt specifičnog za klijenta</span><span class="sxs-lookup"><span data-stu-id="ab1c6-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="ab1c6-140">Možete postaviti i cjenike za projekt specifične za klijenta kada ste sa svojim klijentima dogovorili glavni ugovor o cijenama.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="ab1c6-141">Idite na **Prodaja** > **Klijenti**.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="ab1c6-142">S popisa aktivnih računa odaberite klijenta za kojeg imate poseban cjenik.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="ab1c6-143">Odaberite zapis o klijentu kako biste ga otvorili, a zatim odaberite karticu **Cjenici za projekt**. Podrešetka prikazuje popis cjenika za projekt specifičnih za tog klijenta.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="ab1c6-144">Ovdje stvorite vezu s novim cjenikom kako biste imali cjenik za projekt specifičan za ovog klijenta.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="ab1c6-145">Prilagođeno određivanje cijena za ugovor o projektu</span><span class="sxs-lookup"><span data-stu-id="ab1c6-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="ab1c6-146">Nakon što ste dobili cjenike za projekt zadane organizacijski i za specifičnog klijenta, ugovori o projektu automatski će se stvoriti s tim vezama cjenika za projekt.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="ab1c6-147">Međutim, cjenici za projekt na ugovoru o projektu uvijek se kopiraju s datumom i nazivom ugovora koji im je dodan.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="ab1c6-148">Voditelji računa i projekata tada mogu početi uređivati cijene na tim kopijama.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="ab1c6-149">Ove izmijenjene cijene primjenjivat će se samo na ovaj ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ab1c6-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
