---
title: Skupne korekcije stvarnih podataka stvorene odobrenim unosima vremena i rashoda
description: U ovoj temi objašnjava se kako administrator može izvršiti pojedinačne ili skupne ispravke prethodno odobrenih unosa vremena i rashoda ako naplata nije dovršena.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144944"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="41ded-103">Skupne korekcije stvarnih podataka stvorene odobrenim unosima vremena i rashoda</span><span class="sxs-lookup"><span data-stu-id="41ded-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="41ded-104">Povremeno se mogu pogrešno unijeti unosi vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="41ded-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="41ded-105">Na primjer, tijekom stvaranja vremenskog unosa savjetnik može odabrati pogrešan datum ili tijekom unosa troškova zamijeniti redoslijed brojeva.</span><span class="sxs-lookup"><span data-stu-id="41ded-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="41ded-106">Ako savjetnik ne može izvršiti ažuriranja poslanih unosa, administrator može izravno ispraviti unos za projekt.</span><span class="sxs-lookup"><span data-stu-id="41ded-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="41ded-107">Kako biste dovršili postupke u ovoj temi, trebat će vam dopuštenja administratora.</span><span class="sxs-lookup"><span data-stu-id="41ded-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="41ded-108">Ispravljanje odobrenih vremenskih unosa</span><span class="sxs-lookup"><span data-stu-id="41ded-108">Correct approved time entries</span></span>     

<span data-ttu-id="41ded-109">Izvršite sljedeće korake kako biste ispravili pojedinačne ili višestruke vremenske unose za projekt.</span><span class="sxs-lookup"><span data-stu-id="41ded-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="41ded-110">U području mogućnosti **Prodaja**, odaberite stavku **Transakcije**, a zatim odaberite mogućnost **Odobreno vrijeme**,</span><span class="sxs-lookup"><span data-stu-id="41ded-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="41ded-111">U popisu **Odobreno vrijeme** pronađite i odaberite jedan ili više odobrenih vremenskih unosa koje želite ispraviti.</span><span class="sxs-lookup"><span data-stu-id="41ded-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="41ded-112">Možete upotrijebiti filtar za pronalaženje povezanih unosa.</span><span class="sxs-lookup"><span data-stu-id="41ded-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="41ded-113">Na primjer, možete filtrirati po ID-u projekta i odabrati sve odobrene vremenske unose s tim ID-om projekta.</span><span class="sxs-lookup"><span data-stu-id="41ded-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="41ded-114">Odaberite mogućnost **Ispravi unose**.</span><span class="sxs-lookup"><span data-stu-id="41ded-114">Select **Correct entries**.</span></span> <span data-ttu-id="41ded-115">Automatski se stvara novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak vremena**.</span><span class="sxs-lookup"><span data-stu-id="41ded-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="41ded-116">Unosi koje ste odabrali dodaju se u dnevnik.</span><span class="sxs-lookup"><span data-stu-id="41ded-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="41ded-117">Na stranicu **Novi dnevnik** unesite **Opis** za svoj dnevnik ispravaka, a zatim odaberite karticu **Ispravci vremenskih unosa**.</span><span class="sxs-lookup"><span data-stu-id="41ded-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="41ded-118">U odjeljku **Nove vrijednosti za vremenske unose**, po potrebi, polja ažurirajte ispravnim podacima.</span><span class="sxs-lookup"><span data-stu-id="41ded-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="41ded-119">Na primjer, možete promijeniti dodijeljeni projekt ili resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="41ded-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="41ded-120">Odaberite mogućnost **Pretpregled**.</span><span class="sxs-lookup"><span data-stu-id="41ded-120">Select **Preview**.</span></span> <span data-ttu-id="41ded-121">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="41ded-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="41ded-122">Na kartici **Redci dnevnika** možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim vremenskim unosima koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.</span><span class="sxs-lookup"><span data-stu-id="41ded-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="41ded-123">Ako je potrebno izvršiti dodatne ispravke, ponovite korake 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="41ded-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="41ded-124">Svi ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za vremenske unose**.</span><span class="sxs-lookup"><span data-stu-id="41ded-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="41ded-125">Ako se ispravci prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="41ded-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="41ded-126">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="41ded-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="41ded-127">Vratite se na područje **Prodaja**, odaberite stavku **Projekti** i otvorite projekt za koji ste upravo ažurirali vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="41ded-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="41ded-128">Na stranici **Projekti**, kartici **Stvarni podaci**, pogledajte promjene koje ste napravili.</span><span class="sxs-lookup"><span data-stu-id="41ded-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="41ded-129">Ako kartica **Stvarni podaci** nije vidljiva, odaberite mogućnost **Povezani** > **Stvarni podaci**.</span><span class="sxs-lookup"><span data-stu-id="41ded-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="41ded-130">Na popisu **Stvarni pridruženi prikaz** možete vidjeti da se izvorni vremenski unosi koji su poništeni i dalje navode, kao i odgovarajući ispravljeni vremenski unosi.</span><span class="sxs-lookup"><span data-stu-id="41ded-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="41ded-131">Na primjer, na sljedećoj slici postoje dvije stavke retka s količinom od 8,00 koje imaju zaduženja navedena u stupcu Iznos.</span><span class="sxs-lookup"><span data-stu-id="41ded-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="41ded-132">Uz to, postoje dvije stavke retka s količinom od -8,00, koje prikazuju kreditirane iznose u stupcu Iznos.</span><span class="sxs-lookup"><span data-stu-id="41ded-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="41ded-133">Ovim se korekcijama količina svodi na nulu.</span><span class="sxs-lookup"><span data-stu-id="41ded-133">These corrections bring the quantity to zero.</span></span>

![Popis pridruženog prikaza stvarnih podataka](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="41ded-135">Ispravljanje odobrenih unosa troškova</span><span class="sxs-lookup"><span data-stu-id="41ded-135">Correct approved expense entries</span></span>

<span data-ttu-id="41ded-136">Izvršite sljedeće korake za ispravljanje jednog ili više unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="41ded-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="41ded-137">U lijevom navigacijskom oknu područja **Prodaja**, ispod stavke **Transakcije**, odaberite mogućnost **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="41ded-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="41ded-138">Na popisu **Odobreni troškovi** odaberite projekt koji želite ispraviti i zatim odaberite mogućnost **Ispravni unosi**.</span><span class="sxs-lookup"><span data-stu-id="41ded-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="41ded-139">Automatski će se stvoriti novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak troška**.</span><span class="sxs-lookup"><span data-stu-id="41ded-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="41ded-140">Na stranici **Novi dnevnik** unesite **Opis** za ispravak, a na kartici **Ispravljanje troškova**, u odjeljku **Nove vrijednosti za rashode**, odaberite polja podataka koja želite ispraviti za odabrane retke troškova.</span><span class="sxs-lookup"><span data-stu-id="41ded-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="41ded-141">Na primjer, trošak možete dodijeliti drugom **Projektu** ili ispraviti stavke **Kategorija troškova**, **Datum troška** ili **Resurs koji se može rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="41ded-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="41ded-142">Odaberite mogućnost **Pretpregled**.</span><span class="sxs-lookup"><span data-stu-id="41ded-142">Select **Preview**.</span></span> <span data-ttu-id="41ded-143">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="41ded-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="41ded-144">Na kartici **Redci dnevnika** provjerite ispravke. Možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim unosima troškova koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.</span><span class="sxs-lookup"><span data-stu-id="41ded-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="41ded-145">Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="41ded-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="41ded-146">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="41ded-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="41ded-147">Ako se vrijednosti ne prikazuju onako kako ste očekivali, odaberite mogućnost **Otkaži** kako biste se vratili na popis **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="41ded-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="41ded-148">Ponovite korake 2 do 5.</span><span class="sxs-lookup"><span data-stu-id="41ded-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="41ded-149">Ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za troškove**.</span><span class="sxs-lookup"><span data-stu-id="41ded-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="41ded-150">Nakon što potvrdite dnevnik ispravaka, vratite se na projekt ili projekte koje ste ažurirali kako biste pogledali promjene.</span><span class="sxs-lookup"><span data-stu-id="41ded-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="41ded-151">Na stranici projekta, na kartici **Stvarni podaci**, pregledajte mogućnost **Stvarni pridruženi prikaz**.</span><span class="sxs-lookup"><span data-stu-id="41ded-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="41ded-152">Navedeni su izvorni i ispravljeni unosi.</span><span class="sxs-lookup"><span data-stu-id="41ded-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="41ded-153">Sljedeća slika prikazuje unose izvornih iznosa troškova i odgovarajuće ispravljene iznose unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="41ded-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Stvarni podaci o troškovima](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
