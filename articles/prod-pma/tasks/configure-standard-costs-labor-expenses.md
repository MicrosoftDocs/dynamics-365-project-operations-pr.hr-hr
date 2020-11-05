---
title: Konfiguriranje standardnih troškova rada i izdataka
description: U ovoj temi objašnjava se način postavljanja standardnih troškova rada i izdataka za projekt.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073445"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="c4c62-103">Konfiguriranje standardnih troškova rada i izdataka</span><span class="sxs-lookup"><span data-stu-id="c4c62-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4c62-104">U ovoj temi objašnjava se način postavljanja standardnih troškova rada i izdataka za projekt.</span><span class="sxs-lookup"><span data-stu-id="c4c62-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="c4c62-105">Ovaj zadatak upotrebljava skup podataka USSI.</span><span class="sxs-lookup"><span data-stu-id="c4c62-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c4c62-106">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena koštanja (sat)**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="c4c62-107">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-107">Select **New**.</span></span>
3. <span data-ttu-id="c4c62-108">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="c4c62-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="c4c62-109">U polje **Cijena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="c4c62-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c4c62-110">Možete postaviti standardnu cijenu koštanja za kategoriju projekta ili možete postaviti cijenu koštanja prema broju radnika, broju projekta, kategoriji, datumu ili nekoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="c4c62-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="c4c62-111">Primijenjena cijena koštanja cijena je koštanja s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="c4c62-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="c4c62-112">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-112">Select **Save**.</span></span>
6. <span data-ttu-id="c4c62-113">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Prodajna cijena (sat)**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="c4c62-114">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-114">Select **New**.</span></span>
8. <span data-ttu-id="c4c62-115">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="c4c62-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="c4c62-116">U polju **Vrijedi za** odaberite jednu mogućnost.</span><span class="sxs-lookup"><span data-stu-id="c4c62-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="c4c62-117">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="c4c62-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c4c62-118">Možete postaviti standardnu prodajnu cijenu za transakcije sati rada ili za kategoriju projekta.</span><span class="sxs-lookup"><span data-stu-id="c4c62-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="c4c62-119">Također možete postaviti prodajne cijene prema broju radnika, broju projekta, kategoriji, datumu transakcije ili nekoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="c4c62-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="c4c62-120">Stvarna prodajna cijena koja se primjenjuje kada radnik unosi transakciju u Dnevnik sati rada, prodajna je cijena s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="c4c62-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c4c62-121">Na primjer, ako su postavljene i opća prodajna cijena i prodajna cijena specifična za radnika, upotrebljava se prodajna cijena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="c4c62-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="c4c62-122">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-122">Select **Save**.</span></span>
12. <span data-ttu-id="c4c62-123">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="c4c62-123">Close the page.</span></span>
13. <span data-ttu-id="c4c62-124">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena koštanja (izdatak)**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="c4c62-125">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-125">Select **New**.</span></span>
15. <span data-ttu-id="c4c62-126">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="c4c62-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="c4c62-127">U polje **Cijena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="c4c62-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="c4c62-128">Može se popuniti više polja, ali to je najmanje što je potrebno za spremanje zapisa.</span><span class="sxs-lookup"><span data-stu-id="c4c62-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="c4c62-129">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-129">Select **Save**.</span></span>
18. <span data-ttu-id="c4c62-130">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Prodajna cijena (izdatak)**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="c4c62-131">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-131">Select **New**.</span></span>
20. <span data-ttu-id="c4c62-132">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="c4c62-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="c4c62-133">U polju **Vrijedi za** odaberite jednu mogućnost.</span><span class="sxs-lookup"><span data-stu-id="c4c62-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="c4c62-134">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="c4c62-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="c4c62-135">Stvarna prodajna cijena koja se primjenjuje kada radnik unosi transakcije u Dnevnik izdataka, prodajna je cijena s najvišom razinom pojedinosti.</span><span class="sxs-lookup"><span data-stu-id="c4c62-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="c4c62-136">Na primjer, ako su postavljene i opća prodajna cijena i prodajna cijena specifična za radnika, upotrebljava se prodajna cijena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="c4c62-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="c4c62-137">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="c4c62-137">Select **Save**.</span></span>

