---
title: Konfiguriranje fakturiranja projekta unutar tvrtke
description: U ovoj temi opisuje se način postavljanja fakturiranja projekata između dviju tvrtki u vašoj tvrtki ili ustanovi.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073447"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="39c75-103">Konfiguriranje fakturiranja projekta unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="39c75-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39c75-104">U ovoj temi opisuje se način postavljanja fakturiranja projekata između dviju tvrtki u vašoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="39c75-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="39c75-105">Ovaj zadatak upotrebljava skup podataka USSI.</span><span class="sxs-lookup"><span data-stu-id="39c75-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="39c75-106">U navigacijskom oknu idite na **Moduli> Dugovanja> Dobavljači> Svi dobavljač**.</span><span class="sxs-lookup"><span data-stu-id="39c75-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="39c75-107">U popisu **Svi dobavljači** , pronađite i odaberite željeni zapis.</span><span class="sxs-lookup"><span data-stu-id="39c75-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="39c75-108">U Oknu radnji odaberite **Općenito**.</span><span class="sxs-lookup"><span data-stu-id="39c75-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="39c75-109">Odaberite **Unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="39c75-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="39c75-110">Postavite **Aktivan** na **Da** kako biste omogućili trgovanje unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="39c75-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="39c75-111">U polje **Tvrtka klijenta** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="39c75-112">U polje **Moj račun** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="39c75-113">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="39c75-113">Select **Save**.</span></span>
9. <span data-ttu-id="39c75-114">Zatvorite stranice kako biste se vratili na početnu stranicu.</span><span class="sxs-lookup"><span data-stu-id="39c75-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="39c75-115">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Parametri za upravljanje projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="39c75-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="39c75-116">Odaberite karticu **Unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="39c75-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="39c75-117">Pomaknite klizač na **Da** kako biste omogućili raspoređivanje resursa i vremenske tablice unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="39c75-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="39c75-118">Na popisu označite odabrani redak.</span><span class="sxs-lookup"><span data-stu-id="39c75-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="39c75-119">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="39c75-119">Select **New**.</span></span>
15. <span data-ttu-id="39c75-120">U polje **Zaduživanje pravne osobe** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="39c75-121">Odaberite potvrdni okvir **Obračunaj prihod**.</span><span class="sxs-lookup"><span data-stu-id="39c75-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="39c75-122">U polje **Kategorija zadane vremenske tablice** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="39c75-123">U polje **Kategorija zadanog izdatka** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="39c75-124">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="39c75-124">Select **Save**.</span></span>
20. <span data-ttu-id="39c75-125">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="39c75-125">Close the page.</span></span>
21. <span data-ttu-id="39c75-126">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Objavljivanje > Postavljanje objavljivanja glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="39c75-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="39c75-127">U polju **Vrste računa glavne knjige** odaberite mogućnost.</span><span class="sxs-lookup"><span data-stu-id="39c75-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="39c75-128">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="39c75-128">Select **New**.</span></span>
24. <span data-ttu-id="39c75-129">U polju novog retka **Glavni račun** navedite željene vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="39c75-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="39c75-130">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="39c75-130">Select **Save**.</span></span>
26. <span data-ttu-id="39c75-131">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="39c75-131">Close the page.</span></span>
27. <span data-ttu-id="39c75-132">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena prijenosa**.</span><span class="sxs-lookup"><span data-stu-id="39c75-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="39c75-133">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="39c75-133">Select **New**.</span></span>
29. <span data-ttu-id="39c75-134">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="39c75-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="39c75-135">U polje **Zaduživanje pravne osobe** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="39c75-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="39c75-136">U polju **Model cijene prijenosa** odaberite mogućnost.</span><span class="sxs-lookup"><span data-stu-id="39c75-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="39c75-137">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="39c75-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="39c75-138">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="39c75-138">Select **Save**.</span></span>

