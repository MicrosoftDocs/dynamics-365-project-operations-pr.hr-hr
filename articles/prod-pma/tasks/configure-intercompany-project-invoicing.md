---
title: Konfiguriranje fakturiranja projekta unutar tvrtke
description: U ovoj temi opisuje se način postavljanja fakturiranja projekata između dviju tvrtki u vašoj tvrtki ili ustanovi.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
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
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001192"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="be70a-103">Konfiguriranje fakturiranja projekta unutar tvrtke</span><span class="sxs-lookup"><span data-stu-id="be70a-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be70a-104">U ovoj temi opisuje se način postavljanja fakturiranja projekata između dviju tvrtki u vašoj tvrtki ili ustanovi.</span><span class="sxs-lookup"><span data-stu-id="be70a-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="be70a-105">Ovaj zadatak upotrebljava skup podataka USSI.</span><span class="sxs-lookup"><span data-stu-id="be70a-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="be70a-106">U navigacijskom oknu idite na **Moduli> Dugovanja> Dobavljači> Svi dobavljač**.</span><span class="sxs-lookup"><span data-stu-id="be70a-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="be70a-107">U popisu **Svi dobavljači**, pronađite i odaberite željeni zapis.</span><span class="sxs-lookup"><span data-stu-id="be70a-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="be70a-108">U Oknu radnji odaberite **Općenito**.</span><span class="sxs-lookup"><span data-stu-id="be70a-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="be70a-109">Odaberite **Unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="be70a-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="be70a-110">Postavite **Aktivan** na **Da** kako biste omogućili trgovanje unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="be70a-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="be70a-111">U polje **Tvrtka klijenta** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="be70a-112">U polje **Moj račun** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="be70a-113">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="be70a-113">Select **Save**.</span></span>
9. <span data-ttu-id="be70a-114">Zatvorite stranice kako biste se vratili na početnu stranicu.</span><span class="sxs-lookup"><span data-stu-id="be70a-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="be70a-115">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Parametri za upravljanje projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="be70a-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="be70a-116">Odaberite karticu **Unutar tvrtke**.</span><span class="sxs-lookup"><span data-stu-id="be70a-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="be70a-117">Pomaknite klizač na **Da** kako biste omogućili raspoređivanje resursa i vremenske tablice unutar tvrtke.</span><span class="sxs-lookup"><span data-stu-id="be70a-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="be70a-118">Na popisu označite odabrani redak.</span><span class="sxs-lookup"><span data-stu-id="be70a-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="be70a-119">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="be70a-119">Select **New**.</span></span>
15. <span data-ttu-id="be70a-120">U polje **Zaduživanje pravne osobe** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="be70a-121">Odaberite potvrdni okvir **Obračunaj prihod**.</span><span class="sxs-lookup"><span data-stu-id="be70a-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="be70a-122">U polje **Kategorija zadane vremenske tablice** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="be70a-123">U polje **Kategorija zadanog izdatka** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="be70a-124">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="be70a-124">Select **Save**.</span></span>
20. <span data-ttu-id="be70a-125">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="be70a-125">Close the page.</span></span>
21. <span data-ttu-id="be70a-126">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Objavljivanje > Postavljanje objavljivanja glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="be70a-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="be70a-127">U polju **Vrste računa glavne knjige** odaberite mogućnost.</span><span class="sxs-lookup"><span data-stu-id="be70a-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="be70a-128">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="be70a-128">Select **New**.</span></span>
24. <span data-ttu-id="be70a-129">U polju novog retka **Glavni račun** navedite željene vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="be70a-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="be70a-130">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="be70a-130">Select **Save**.</span></span>
26. <span data-ttu-id="be70a-131">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="be70a-131">Close the page.</span></span>
27. <span data-ttu-id="be70a-132">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Postavljanje > Cijene > Cijena prijenosa**.</span><span class="sxs-lookup"><span data-stu-id="be70a-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="be70a-133">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="be70a-133">Select **New**.</span></span>
29. <span data-ttu-id="be70a-134">U polje **Stvarni datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="be70a-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="be70a-135">U polje **Zaduživanje pravne osobe** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="be70a-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="be70a-136">U polju **Model cijene prijenosa** odaberite mogućnost.</span><span class="sxs-lookup"><span data-stu-id="be70a-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="be70a-137">U polje **Određivanje cijene** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="be70a-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="be70a-138">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="be70a-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]