---
title: Stvaranje i potvrda dnevnika ispravaka
description: U ovoj se temi nalaze informacije o načinu izrade i potvrde dnevnika ispravaka.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996647"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="473df-103">Stvaranje i potvrda dnevnika ispravaka</span><span class="sxs-lookup"><span data-stu-id="473df-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="473df-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="473df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="473df-105">Povremeno se mogu pogrešno unijeti unosi vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="473df-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="473df-106">Na primjer, tijekom stvaranja vremenskog unosa savjetnik može odabrati pogrešan datum ili tijekom unosa troškova zamijeniti redoslijed brojeva.</span><span class="sxs-lookup"><span data-stu-id="473df-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="473df-107">Ako savjetnik ne može izvršiti ažuriranja poslanih unosa, administrator može izravno ispraviti unos za projekt.</span><span class="sxs-lookup"><span data-stu-id="473df-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="473df-108">Kako biste dovršili postupke u ovoj temi, trebat će vam dopuštenja administratora.</span><span class="sxs-lookup"><span data-stu-id="473df-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="473df-109">Ispravljanje odobrenih vremenskih unosa</span><span class="sxs-lookup"><span data-stu-id="473df-109">Correct approved time entries</span></span>     

<span data-ttu-id="473df-110">Izvršite sljedeće korake kako biste ispravili pojedinačne ili višestruke vremenske unose za projekt.</span><span class="sxs-lookup"><span data-stu-id="473df-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="473df-111">U području mogućnosti **Prodaja**, odaberite stavku **Transakcije**, a zatim odaberite mogućnost **Odobreno vrijeme**,</span><span class="sxs-lookup"><span data-stu-id="473df-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="473df-112">U popisu **Odobreno vrijeme** pronađite i odaberite jedan ili više odobrenih vremenskih unosa koje želite ispraviti.</span><span class="sxs-lookup"><span data-stu-id="473df-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="473df-113">Možete upotrijebiti filtar za pronalaženje povezanih unosa.</span><span class="sxs-lookup"><span data-stu-id="473df-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="473df-114">Na primjer, možete filtrirati po ID-u projekta i odabrati sve odobrene vremenske unose s tim ID-om projekta.</span><span class="sxs-lookup"><span data-stu-id="473df-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="473df-115">Odaberite mogućnost **Ispravi unose**.</span><span class="sxs-lookup"><span data-stu-id="473df-115">Select **Correct entries**.</span></span> <span data-ttu-id="473df-116">Automatski se stvara novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak vremena**.</span><span class="sxs-lookup"><span data-stu-id="473df-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="473df-117">Unosi koje ste odabrali dodaju se u dnevnik.</span><span class="sxs-lookup"><span data-stu-id="473df-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="473df-118">Na stranicu **Novi dnevnik** unesite **Opis** za svoj dnevnik ispravaka, a zatim odaberite karticu **Ispravci vremenskih unosa**.</span><span class="sxs-lookup"><span data-stu-id="473df-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="473df-119">U odjeljku **Nove vrijednosti za vremenske unose**, po potrebi, polja ažurirajte ispravnim podacima.</span><span class="sxs-lookup"><span data-stu-id="473df-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="473df-120">Na primjer, možete promijeniti dodijeljeni projekt ili resurs koji se može rezervirati.</span><span class="sxs-lookup"><span data-stu-id="473df-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="473df-121">Odaberite mogućnost **Pretpregled**.</span><span class="sxs-lookup"><span data-stu-id="473df-121">Select **Preview**.</span></span> <span data-ttu-id="473df-122">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="473df-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="473df-123">Na kartici **Redci dnevnika** možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim vremenskim unosima koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.</span><span class="sxs-lookup"><span data-stu-id="473df-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="473df-124">Ako je potrebno izvršiti dodatne ispravke, ponovite korake 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="473df-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="473df-125">Svi ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za vremenske unose**.</span><span class="sxs-lookup"><span data-stu-id="473df-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="473df-126">Ako se ispravci prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="473df-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="473df-127">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="473df-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="473df-128">Vratite se na područje **Prodaja**, odaberite stavku **Projekti** i otvorite projekt za koji ste upravo ažurirali vremenske unose.</span><span class="sxs-lookup"><span data-stu-id="473df-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="473df-129">Na stranici **Projekti**, kartici **Stvarni podaci**, pogledajte promjene koje ste napravili.</span><span class="sxs-lookup"><span data-stu-id="473df-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="473df-130">Ako kartica **Stvarni podaci** nije vidljiva, odaberite mogućnost **Povezani** > **Stvarni podaci**.</span><span class="sxs-lookup"><span data-stu-id="473df-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="473df-131">Na popisu **Stvarni pridruženi prikaz** možete vidjeti da se izvorni vremenski unosi koji su poništeni i dalje navode, kao i odgovarajući ispravljeni vremenski unosi.</span><span class="sxs-lookup"><span data-stu-id="473df-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="473df-132">Na primjer, na sljedećoj slici postoje dvije stavke retka s količinom od 8,00 koje imaju zaduženja navedena u stupcu Iznos.</span><span class="sxs-lookup"><span data-stu-id="473df-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="473df-133">Uz to, postoje dvije stavke retka s količinom od -8,00, koje prikazuju kreditirane iznose u stupcu Iznos.</span><span class="sxs-lookup"><span data-stu-id="473df-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="473df-134">Ovim se korekcijama količina svodi na nulu.</span><span class="sxs-lookup"><span data-stu-id="473df-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="473df-135">Ispravljanje odobrenih unosa troškova</span><span class="sxs-lookup"><span data-stu-id="473df-135">Correct approved expense entries</span></span>

<span data-ttu-id="473df-136">Izvršite sljedeće korake za ispravljanje jednog ili više unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="473df-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="473df-137">U lijevom navigacijskom oknu područja **Prodaja**, ispod stavke **Transakcije**, odaberite mogućnost **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="473df-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="473df-138">Na popisu **Odobreni troškovi** odaberite projekt koji želite ispraviti i zatim odaberite mogućnost **Ispravni unosi**.</span><span class="sxs-lookup"><span data-stu-id="473df-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="473df-139">Automatski će se stvoriti novi dnevnik ispravljanja, s pomoću dodijeljene vrste stavke **Ispravak troška**.</span><span class="sxs-lookup"><span data-stu-id="473df-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="473df-140">Na stranici **Novi dnevnik** unesite **Opis** za ispravak, a na kartici **Ispravljanje troškova**, u odjeljku **Nove vrijednosti za rashode**, odaberite polja podataka koja želite ispraviti za odabrane retke troškova.</span><span class="sxs-lookup"><span data-stu-id="473df-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="473df-141">Na primjer, trošak možete dodijeliti drugom **Projektu** ili ispraviti stavke **Kategorija troškova**, **Datum troška** ili **Resurs koji se može rezervirati**.</span><span class="sxs-lookup"><span data-stu-id="473df-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="473df-142">Odaberite mogućnost **Pretpregled**.</span><span class="sxs-lookup"><span data-stu-id="473df-142">Select **Preview**.</span></span> <span data-ttu-id="473df-143">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="473df-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="473df-144">Na kartici **Redci dnevnika** provjerite ispravke. Možete vidjeti popis izvornih stvarnih podataka povezanih s odabranim unosima troškova koji su preokrenuti i odgovarajuće ispravljene retke koji su stvoreni.</span><span class="sxs-lookup"><span data-stu-id="473df-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="473df-145">Ako se ispravljene vrijednosti prikazuju onako kako ste očekivali, odaberite mogućnost **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="473df-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="473df-146">U dijaloškom okviru odaberite mogućnost **U redu**.</span><span class="sxs-lookup"><span data-stu-id="473df-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="473df-147">Ako se vrijednosti ne prikazuju onako kako ste očekivali, odaberite mogućnost **Otkaži** kako biste se vratili na popis **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="473df-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="473df-148">Ponovite korake 2 do 5.</span><span class="sxs-lookup"><span data-stu-id="473df-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="473df-149">Ispravljeni stvarni podaci imat će iste vrijednosti koje ste odabrali u odjeljku **Nove vrijednosti za troškove**.</span><span class="sxs-lookup"><span data-stu-id="473df-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="473df-150">Nakon što potvrdite dnevnik ispravaka, vratite se na projekt ili projekte koje ste ažurirali kako biste pogledali promjene.</span><span class="sxs-lookup"><span data-stu-id="473df-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="473df-151">Na stranici projekta, na kartici **Stvarni podaci**, pregledajte mogućnost **Stvarni pridruženi prikaz**.</span><span class="sxs-lookup"><span data-stu-id="473df-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="473df-152">Navedeni su izvorni i ispravljeni unosi.</span><span class="sxs-lookup"><span data-stu-id="473df-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="473df-153">Sljedeća slika prikazuje unose izvornih iznosa troškova i odgovarajuće ispravljene iznose unosa troškova.</span><span class="sxs-lookup"><span data-stu-id="473df-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]