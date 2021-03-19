---
title: Prijenos proračuna projekata na kraju poslovne godine
description: U ovom članku nalaze se informacije o načinu prijenosa preostalog proračunskog iznosa u naredne godine i stvaranju pojedinosti proračunskog registra.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289720"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="37264-103">Prijenos proračuna projekata na kraju poslovne godine</span><span class="sxs-lookup"><span data-stu-id="37264-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37264-104">Kada radite na višegodišnjem projektu, možda ćete na kraju poslovne godine imati preostali proračun.</span><span class="sxs-lookup"><span data-stu-id="37264-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="37264-105">Preostale proračunske iznose možete prenijeti u narednu godinu i stvoriti pojedinosti registra proračuna za iznose na povezanim računima glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="37264-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="37264-106">Prije nego što prenesete preostale iznose, pregledajte i analizirajte preostale proračunske iznose.</span><span class="sxs-lookup"><span data-stu-id="37264-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="37264-107">Pregled i analiza preostalih proračunskih iznosa</span><span class="sxs-lookup"><span data-stu-id="37264-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="37264-108">Dovršite sljedeće korake kako biste pregledali proračunske iznose za projekte na kraju godine, ali nemojte iznose prenositi dalje.</span><span class="sxs-lookup"><span data-stu-id="37264-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="37264-109">Idite na stavku **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="37264-110">Na stranici **Postupak prijenosa proračuna projekta**, na kartici **Mogućnosti na kraju godine**, provjerite da mogućnost **Prenesi preostale proračunske iznose projekta** nije omogućena.</span><span class="sxs-lookup"><span data-stu-id="37264-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="37264-111">Na kartici **Parametri**, u polju **Proračunska godina projekta**, odaberite poslovnu godinu za koji želite prikazati preostali proračunski iznos.</span><span class="sxs-lookup"><span data-stu-id="37264-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="37264-112">U polju **Proračunska godina projekta**, odaberite poslovnu godinu za koji želite prikazati preostali proračunski iznos.</span><span class="sxs-lookup"><span data-stu-id="37264-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="37264-113">U polju **Iz modela predviđanja** odaberite **Preostali proračun**.</span><span class="sxs-lookup"><span data-stu-id="37264-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="37264-114">Kako biste uključili projekte koji ispunjavaju odabrane kriterije i nemaju preostali proračun, odaberite **Prikaži bez preostalog iznosa**.</span><span class="sxs-lookup"><span data-stu-id="37264-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="37264-115">Na kartici **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s odabranim kriterijima, a zatim odaberite **Postupak**.</span><span class="sxs-lookup"><span data-stu-id="37264-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="37264-116">Kako biste dizajnirali upit baze podataka koji učitava određeni skup proračuna u okno, odaberite **Dohvati odabrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="37264-117">Za više informacija o određenom retku u oknu odaberite redak, a zatim odaberite **Prikaži pojedinosti proračuna** ili **Prikaži račune**.</span><span class="sxs-lookup"><span data-stu-id="37264-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="37264-118">Prijenos preostalih proračunskih iznosa</span><span class="sxs-lookup"><span data-stu-id="37264-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="37264-119">Kada obrađujete preostale proračunske iznose, možete stvoriti transakcije u glavnoj knjizi za iznose koje prenosite.</span><span class="sxs-lookup"><span data-stu-id="37264-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="37264-120">Kako biste stvorili transakcije glavne knjige, poduzmite korake navedene u odjeljku [Prijenos proračunskih iznosa i stvaranje transakcija glavne knjige](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="37264-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="37264-121">Proračunski iznosi koji se prenose, prenose se na model predviđanja koji je odabran na stranici **Modeli predviđanja** kao model predviđanja za prijenos.</span><span class="sxs-lookup"><span data-stu-id="37264-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="37264-122">Prijenos proračunskih iznosa i stvaranje transakcija glavne knjige</span><span class="sxs-lookup"><span data-stu-id="37264-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="37264-123">Odaberite **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="37264-124">Na stranici **Postupak prijenosa proračuna projekta** odaberite **Kraj godine**, a zatim omogućite **Prijenos preostalog proračunskog iznosa projekta** i **Stvaranje unosa u registar proračuna u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="37264-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="37264-125">Na kartici **Parametri**, u grupi polja **Parametri projekta**, odaberite sljedeće:</span><span class="sxs-lookup"><span data-stu-id="37264-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="37264-126">**Proračunska godina projekta**: Odaberite početak poslovne godine za koji želite prikazati preostale iznose proračuna.</span><span class="sxs-lookup"><span data-stu-id="37264-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="37264-127">**Dobit i gubitak**: Stvorite transakcija dobiti i gubitka u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="37264-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="37264-128">**WIP**: Stvorite transakcije Rada u tijeku (WIP) u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="37264-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="37264-129">**Plaća**: Stvorite transakcije raspodjele plaća u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="37264-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="37264-130">U grupi polja **Glavna knjiga** navedite sljedeće informacije:</span><span class="sxs-lookup"><span data-stu-id="37264-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="37264-131">U polju **Otvaranje poslovne godine** odaberite poslovnu godinu u koju želite prenijeti preostali proračunski iznos za projekt.</span><span class="sxs-lookup"><span data-stu-id="37264-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="37264-132">Zadana vrijednost je jedna godina nakon vrijednosti u polju **Proračunska godina projekta**.</span><span class="sxs-lookup"><span data-stu-id="37264-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="37264-133">U polju **Razdoblje prijenosa** odaberite razdoblje za koje želite stvoriti pojedinosti proračunskog registra u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="37264-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="37264-134">To je obično prvo razdoblje na otvaranju poslovne godine.</span><span class="sxs-lookup"><span data-stu-id="37264-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="37264-135">U grupi polja **Kopiraj iz/na** navedite sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="37264-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="37264-136">U polju **Iz modela predviđanja** odaberite model predviđanja proračuna projekta povezan s preostalim proračunskim iznosima koje želite prenijeti za projekte.</span><span class="sxs-lookup"><span data-stu-id="37264-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="37264-137">U polju **Proračunski model za glavnu knjigu** odaberite model proračuna za glavnu knjigu povezan s proračunskim iznosima koje želite prenijeti u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="37264-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="37264-138">Odaberite **Valuta prijenosa prodaje** kako biste valutu prodaje projekta upotrebljavali za transakcije glavne knjige koje se kreiraju kada prenesete proračunske iznose za projekte.</span><span class="sxs-lookup"><span data-stu-id="37264-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="37264-139">Kad mogućnost nije odabrana, transakcije upotrebljavaju računovodstvenu valutu.</span><span class="sxs-lookup"><span data-stu-id="37264-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="37264-140">Odaberite **Prikaži bez preostalog iznosa** kako biste uključili projekte koji nemaju preostali iznos proračuna, ali zadovoljavaju ostale kriterije koje odaberete u projektima prikazanim u donjem oknu.</span><span class="sxs-lookup"><span data-stu-id="37264-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="37264-141">Na kartici **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s kriterijima koje ste odabrali.</span><span class="sxs-lookup"><span data-stu-id="37264-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="37264-142">Ako biste željeli dizajnirati upit baze podataka koji učitava određeni skup proračuna projekta u okno, odaberite **Dohvati odabrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="37264-143">Za svaki projekt koji želite obraditi, odaberite mogućnost na početku retka za projekt.</span><span class="sxs-lookup"><span data-stu-id="37264-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="37264-144">Kako biste odabrali sve ili većinu projekata, odaberite kvačicu u gornjem lijevom kutu.</span><span class="sxs-lookup"><span data-stu-id="37264-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="37264-145">Kako biste isključili obradu nekog projekta, uklonite kvačicu za taj projekt.</span><span class="sxs-lookup"><span data-stu-id="37264-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="37264-146">Kako biste prenijeli preostale proračunske iznose za odabrane projekte u odabranu poslovnu godinu i stvorili pojedinosti proračunskog registra u glavnoj knjizi, odaberite **Postupak**.</span><span class="sxs-lookup"><span data-stu-id="37264-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="37264-147">Prijenos proračunskih iznosa bez stvaranja transakcija glavne knjige</span><span class="sxs-lookup"><span data-stu-id="37264-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="37264-148">Idite na stavku **Upravljanje projektima i računovodstvo** > **Povremeno** > **Proračuni** > **Prenesi proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="37264-149">Na stranici **Postupak prijenosa proračuna projekta**, u polju **Mogućnosti na kraju godine**, odaberite mogućnost **Prenesi preostale iznose proračuna projekta**.</span><span class="sxs-lookup"><span data-stu-id="37264-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="37264-150">U grupi **Parametri**, u polju **Proračunska godina projekta**, odaberite poslovnu godinu za koju želite prikazati preostale iznose proračuna.</span><span class="sxs-lookup"><span data-stu-id="37264-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="37264-151">U grupi **Kopiraj iz/na** navedite sljedeće podatke:</span><span class="sxs-lookup"><span data-stu-id="37264-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="37264-152">U polju **Iz modela predviđanja** odaberite model predviđanja proračuna projekta koji je povezan s preostalim proračunskim iznosima koje želite prenijeti za projekte.</span><span class="sxs-lookup"><span data-stu-id="37264-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="37264-153">Kako biste uključili projekte koji nemaju preostali proračun, ali ispunjavaju kriterije koje ste odabrali, odaberite **Prikaži bez preostalog iznosa**.</span><span class="sxs-lookup"><span data-stu-id="37264-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="37264-154">U grupi **Odaberi proračune** odaberite **Dohvati sve proračune** kako biste učitali sve proračune koji se podudaraju s kriterijima koje ste odabrali.</span><span class="sxs-lookup"><span data-stu-id="37264-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="37264-155">Kako biste dizajnirali upit baze podataka koji učitava određeni skup proračuna projekta u okno, odaberite **Dohvati odabrane proračune**.</span><span class="sxs-lookup"><span data-stu-id="37264-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="37264-156">Za svaki projekt koji želite obraditi, odaberite mogućnost na početku retka za projekt.</span><span class="sxs-lookup"><span data-stu-id="37264-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="37264-157">Odaberite **Postupak** za prijenos preostalih proračunskih iznosa za odabrane projekte na odabranu poslovnu godinu.</span><span class="sxs-lookup"><span data-stu-id="37264-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]