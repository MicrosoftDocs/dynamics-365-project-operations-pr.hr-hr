---
title: Konfiguriranje standardnih troškova rada i izdataka
description: U ovoj temi objašnjava se način postavljanja standardnih troškova rada i izdataka za projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750216"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="2fb81-103">Konfiguriranje standardnih troškova rada i izdataka</span><span class="sxs-lookup"><span data-stu-id="2fb81-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2fb81-104">U ovoj temi objašnjava se način postavljanja standardnih troškova rada i izdataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="2fb81-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="2fb81-105">Ovaj zadatak upotrebljava skup podataka USSI.</span><span class="sxs-lookup"><span data-stu-id="2fb81-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="2fb81-106">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena koštanja (sat)**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="2fb81-107">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-107">Select **New**.</span></span>
3. <span data-ttu-id="2fb81-108">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="2fb81-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="2fb81-109">U polje **Cijena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="2fb81-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2fb81-110">Možete postaviti standardnu cijenu koštanja za kategoriju projekta ili možete postaviti cijenu koštanja prema broju radnika, broju projekta, kategoriji, datumu ili nekoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="2fb81-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="2fb81-111">Primijenjena cijena koštanja cijena je koštanja s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="2fb81-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="2fb81-112">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-112">Select **Save**.</span></span>
6. <span data-ttu-id="2fb81-113">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Prodajna cijena (sat)**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="2fb81-114">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-114">Select **New**.</span></span>
8. <span data-ttu-id="2fb81-115">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="2fb81-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="2fb81-116">U polju **Vrijedi za** odaberite jednu mogućnost.</span><span class="sxs-lookup"><span data-stu-id="2fb81-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="2fb81-117">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="2fb81-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2fb81-118">Možete postaviti standardnu prodajnu cijenu za transakcije sati rada ili za kategoriju projekta.</span><span class="sxs-lookup"><span data-stu-id="2fb81-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="2fb81-119">Također možete postaviti prodajne cijene prema broju radnika, broju projekta, kategoriji, datumu transakcije ili nekoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="2fb81-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="2fb81-120">Stvarna prodajna cijena koja se primjenjuje kada radnik unosi transakciju u Dnevnik sati rada, prodajna je cijena s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="2fb81-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2fb81-121">Na primjer, ako su postavljene i opća prodajna cijena i prodajna cijena specifična za radnika, upotrebljava se prodajna cijena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="2fb81-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="2fb81-122">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-122">Select **Save**.</span></span>
12. <span data-ttu-id="2fb81-123">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="2fb81-123">Close the page.</span></span>
13. <span data-ttu-id="2fb81-124">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena koštanja (izdatak)**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="2fb81-125">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-125">Select **New**.</span></span>
15. <span data-ttu-id="2fb81-126">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="2fb81-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="2fb81-127">U polje **Cijena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="2fb81-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="2fb81-128">Može se popuniti više polja, ali to je najmanje što je potrebno za spremanje zapisa.</span><span class="sxs-lookup"><span data-stu-id="2fb81-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="2fb81-129">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-129">Select **Save**.</span></span>
18. <span data-ttu-id="2fb81-130">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Prodajna cijena (izdatak)**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="2fb81-131">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-131">Select **New**.</span></span>
20. <span data-ttu-id="2fb81-132">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="2fb81-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="2fb81-133">U polju **Vrijedi za** odaberite jednu mogućnost.</span><span class="sxs-lookup"><span data-stu-id="2fb81-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="2fb81-134">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="2fb81-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="2fb81-135">Stvarna prodajna cijena koja se primjenjuje kada radnik unosi transakcije u Dnevnik izdataka, prodajna je cijena s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="2fb81-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="2fb81-136">Na primjer, ako su postavljene i opća prodajna cijena i prodajna cijena specifična za radnika, upotrebljava se prodajna cijena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="2fb81-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="2fb81-137">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2fb81-137">Select **Save**.</span></span>

