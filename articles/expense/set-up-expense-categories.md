---
title: Postavljanje kategorije izdatka
description: U ovoj temi nalaze se informacije o načinu postavljanja kategorije troškova i dijeljene kategorije za izvješća o troškovima.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001778"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="118b8-103">Postavljanje kategorije izdatka</span><span class="sxs-lookup"><span data-stu-id="118b8-103">Set up expense categories</span></span>

<span data-ttu-id="118b8-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="118b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="118b8-105">Kad zaposlenici stvaraju izvješća o troškovima, svaki trošak koji evidentiraju mora biti povezan s kategorijom troška.</span><span class="sxs-lookup"><span data-stu-id="118b8-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="118b8-106">Kategorije troškova izvedene su iz dijeljenih kategorija koje se mogu dijeliti između pravnih osoba u vašoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="118b8-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="118b8-107">Ovisno o tome kako je definirana vaša tvrtka ili ustanova, ove se kategorije troškova mogu dijeliti i u drugim područjima.</span><span class="sxs-lookup"><span data-stu-id="118b8-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="118b8-108">Na temelju definicije vaše tvrtke ili ustanove i smjernica implementacijskog tima, morate odrediti hoće li se kategorije koje se upotrebljavaju u upravljanju troškovima upotrebljavati samo u upravljanju troškovima ili bi ih se trebalo dijeliti u drugim područjima.</span><span class="sxs-lookup"><span data-stu-id="118b8-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="118b8-109">Te se kategorije mogu dijeliti između Upravljanja projektima i računovodstva te Upravljanja troškovima tj. Upravljanja projektima i računovodstva te Proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="118b8-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="118b8-110">Međutim, ne mogu se dijeliti između Upravljanja troškovima i Proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="118b8-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="118b8-111">Prije nego što započnete postupak postavljanja, za svaku kategoriju troškova moraju se donijeti sljedeće odluke:</span><span class="sxs-lookup"><span data-stu-id="118b8-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="118b8-112">Što je kategorija troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-112">What is the expense category?</span></span> <span data-ttu-id="118b8-113">Primjeri uključuju kategorije za letove, hotele ili kilometražu.</span><span class="sxs-lookup"><span data-stu-id="118b8-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="118b8-114">Može li se kategorija troškova upotrebljavati i za Upravljanje projektima i računovodstvo?</span><span class="sxs-lookup"><span data-stu-id="118b8-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="118b8-115">Ako može, morate također donijeti sljedeće odluke:</span><span class="sxs-lookup"><span data-stu-id="118b8-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="118b8-116">Koji će se računi za troškove upotrebljavati za sljedeće troškove?</span><span class="sxs-lookup"><span data-stu-id="118b8-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="118b8-117">Cijena</span><span class="sxs-lookup"><span data-stu-id="118b8-117">Cost</span></span>
        - <span data-ttu-id="118b8-118">Raspodjela plaća</span><span class="sxs-lookup"><span data-stu-id="118b8-118">Payroll allocation</span></span>
        - <span data-ttu-id="118b8-119">Vrijednost troškova WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-119">WIP-cost value</span></span>
        - <span data-ttu-id="118b8-120">Troškovna stavka</span><span class="sxs-lookup"><span data-stu-id="118b8-120">Cost-item</span></span>
        - <span data-ttu-id="118b8-121">Vrijednosna stavka troškova WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="118b8-122">Obračunani gubitak</span><span class="sxs-lookup"><span data-stu-id="118b8-122">Accrued loss</span></span>
        - <span data-ttu-id="118b8-123">Obračunani gubitak WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="118b8-124">Koji će se računi prihoda upotrebljavati za sljedeće izvore prihoda?</span><span class="sxs-lookup"><span data-stu-id="118b8-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="118b8-125">Fakturirani prihod</span><span class="sxs-lookup"><span data-stu-id="118b8-125">Invoiced revenue</span></span>
        - <span data-ttu-id="118b8-126">Obračunani prihod – vrijednost prodaje</span><span class="sxs-lookup"><span data-stu-id="118b8-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="118b8-127">Prodajna vrijednost WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-127">WIP-sales value</span></span>
        - <span data-ttu-id="118b8-128">Obračunani prihod proizvodnje</span><span class="sxs-lookup"><span data-stu-id="118b8-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="118b8-129">Proizvodnja WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-129">WIP-production</span></span>
        - <span data-ttu-id="118b8-130">Obračunani prihod – dobit</span><span class="sxs-lookup"><span data-stu-id="118b8-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="118b8-131">Dobit WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-131">WIP-profit</span></span>
        - <span data-ttu-id="118b8-132">Obračunani prihod – pretplata</span><span class="sxs-lookup"><span data-stu-id="118b8-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="118b8-133">Pretplata WIP-a</span><span class="sxs-lookup"><span data-stu-id="118b8-133">WIP-subscription</span></span>

- <span data-ttu-id="118b8-134">Što je vrsta troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-134">What is the expense type?</span></span>
- <span data-ttu-id="118b8-135">Koji je zadani način plaćanja za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="118b8-136">Moraju li se specificirati troškovi iz kategorije troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="118b8-137">Koji je glavni zadani račun za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="118b8-138">Koja je zadana stavka grupe poreza na promet za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="118b8-139">Jesu li dodatni načini plaćanja dozvoljeni za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="118b8-140">Ako jesu, koji su?</span><span class="sxs-lookup"><span data-stu-id="118b8-140">If so, what are they?</span></span>
- <span data-ttu-id="118b8-141">Postoje li potkategorije u ovoj kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="118b8-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="118b8-142">Ako postoje potkategorije, morate također donijeti sljedeće odluke:</span><span class="sxs-lookup"><span data-stu-id="118b8-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="118b8-143">Je li neka od potkategorija izuzeta iz povrata poreza?</span><span class="sxs-lookup"><span data-stu-id="118b8-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="118b8-144">Koja je stavka grupe poreza na promet potkategorija?</span><span class="sxs-lookup"><span data-stu-id="118b8-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]