---
title: Stvarni podaci
description: U ovoj temi nalaze se informacije o načinu rada sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073378"
---
# <a name="actuals"></a><span data-ttu-id="168f4-103">Stvarni podaci</span><span class="sxs-lookup"><span data-stu-id="168f4-103">Actuals</span></span> 

<span data-ttu-id="168f4-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="168f4-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="168f4-105">Stvarne vrijednosti su količina dovršenog posla na projektu.</span><span class="sxs-lookup"><span data-stu-id="168f4-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="168f4-106">Stvoreni su kao rezultat unosa vremena i troškova, unosa temeljnica i faktura.</span><span class="sxs-lookup"><span data-stu-id="168f4-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="168f4-107">Redci temeljnice i prijavljivanje vremena</span><span class="sxs-lookup"><span data-stu-id="168f4-107">Journal lines and time submission</span></span>

<span data-ttu-id="168f4-108">Dodatne informacije o unosu vremena potražite u odjeljku [Pregled unosa vremena](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="168f4-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="168f4-109">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="168f4-109">Time and materials</span></span>

<span data-ttu-id="168f4-110">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="168f4-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="168f4-111">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-111">Fixed price</span></span>

<span data-ttu-id="168f4-112">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora s nepromjenjivom cijenom, sustav stvara jedan redak u temeljnici za trošak.</span><span class="sxs-lookup"><span data-stu-id="168f4-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="168f4-113">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="168f4-113">Default pricing</span></span>

<span data-ttu-id="168f4-114">Logika za stvaranje zadanih cijena temelji se na retku temeljnice.</span><span class="sxs-lookup"><span data-stu-id="168f4-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="168f4-115">Vrijednosti polja iz unosa vremena kopiraju se u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="168f4-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="168f4-116">Te vrijednosti uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="168f4-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="168f4-117">Polja koja utječu na zadano određivanje cijene, kao što su **Uloga** i **Org jedinica** obično određuju odgovarajuću cijenu retka temeljnice.</span><span class="sxs-lookup"><span data-stu-id="168f4-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="168f4-118">Na unos vremena možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="168f4-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="168f4-119">Ako želite da se vrijednost polja propagira do stvarnih vrijednosti, izradite polje u entitetu Stvarne vrijednosti i koristite mapiranja polja da biste kopirali polje iz unosa vremena u stvarnu vrijednost.</span><span class="sxs-lookup"><span data-stu-id="168f4-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="168f4-120">Redci temeljnice i slanje osnovnih troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="168f4-121">Dodatne informacije o unosu troška potražite u odjeljku [Pregled unosa troška](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="168f4-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="168f4-122">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="168f4-122">Time and materials</span></span>

<span data-ttu-id="168f4-123">Kada je poslani unos osnovnog troška povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="168f4-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="168f4-124">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-124">Fixed price</span></span>

<span data-ttu-id="168f4-125">Kada je poslani unos osnovnog troška povezan s projektom koji je mapiran u redak ugovora s nepromjenjivom cijenom, sustav stvara jedan redak u temeljnici za trošak.</span><span class="sxs-lookup"><span data-stu-id="168f4-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="168f4-126">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="168f4-126">Default pricing</span></span>

<span data-ttu-id="168f4-127">Logika unošenja zadanih cijena za troškove temelji se na kategoriji troškova.</span><span class="sxs-lookup"><span data-stu-id="168f4-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="168f4-128">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="168f4-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="168f4-129">Međutim, prema zadanim postavkama, iznos koji je sam korisnik unio za cijenu postavljen je izravno na povezane retke u temeljnici za trošak i prodaju.</span><span class="sxs-lookup"><span data-stu-id="168f4-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="168f4-130">Unosi zadanih cijena troška po jedinici koji se temelje na unosu na temelju kategorije nije dostupan.</span><span class="sxs-lookup"><span data-stu-id="168f4-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="168f4-131">Uporaba temeljnica za unos za bilježenje troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-131">Use entry journals to record costs</span></span>

<span data-ttu-id="168f4-132">Temeljnice za unos možete upotrebljavati za bilježenje troška ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="168f4-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="168f4-133">Temeljnice se mogu upotrebljavati u sljedeće svrhe:</span><span class="sxs-lookup"><span data-stu-id="168f4-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="168f4-134">Bilježite stvarni trošak materijala i prodaje na projektu.</span><span class="sxs-lookup"><span data-stu-id="168f4-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="168f4-135">Premještajte stvarne vrijednosti transakcije iz drugog sustava u aplikaciju Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="168f4-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="168f4-136">Bilježite troškove koji su se dogodili u drugom sustavu.</span><span class="sxs-lookup"><span data-stu-id="168f4-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="168f4-137">Ti troškovi mogu uključivati troškove nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="168f4-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="168f4-138">Aplikacija ne provjerava valjanost vrste retka temeljnice ili povezanog određivanja cijene koje se unosi u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="168f4-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="168f4-139">Stoga bi samo korisnik koji je potpuno svjestan računovodstvenog utjecaja koji stvarni podaci imaju na projekt trebao upotrebljavati temeljnice unosa za stvaranje stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="168f4-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="168f4-140">Zbog utjecaja ove vrste temeljnice, trebali biste pažljivo odabrati tko ima pristup za stvaranje temeljnica za unos.</span><span class="sxs-lookup"><span data-stu-id="168f4-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="168f4-141">Bilježenje stvarnih podataka na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="168f4-141">Record actuals based on project events</span></span>

<span data-ttu-id="168f4-142">Project Operations bilježi financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="168f4-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="168f4-143">Te se transakcije zapisuju kao stvarne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="168f4-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="168f4-144">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="168f4-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="168f4-145">Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="168f4-146">Događaj</span><span class="sxs-lookup"><span data-stu-id="168f4-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="168f4-147">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="168f4-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="168f4-148">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="168f4-149">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="168f4-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="168f4-150">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="168f4-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="168f4-151">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="168f4-152">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-152">Actuals</span></span></th>
<th><span data-ttu-id="168f4-153">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="168f4-153">Transaction currency</span></span></th>
<th><span data-ttu-id="168f4-154">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-154">Fixed price</span></span></th>
<th><span data-ttu-id="168f4-155">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="168f4-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="168f4-156">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="168f4-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="168f4-157">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-158">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="168f4-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="168f4-159">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="168f4-160">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="168f4-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="168f4-161">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-161">Cost actual</span></span></td>
<td><span data-ttu-id="168f4-162">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-163">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-164">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="168f4-165">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-166">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-167">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="168f4-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="168f4-168">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="168f4-169">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="168f4-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="168f4-170">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-170">Cost actual</span></span></td>
<td><span data-ttu-id="168f4-171">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-172">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-173">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-174">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-175">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-176">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-177">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-178">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-179">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="168f4-180">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="168f4-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="168f4-181">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="168f4-182">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-183">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="168f4-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-184">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-185">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-186">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-187">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-187">Billed sales</span></span></td>
<td><span data-ttu-id="168f4-188">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="168f4-189">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="168f4-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="168f4-190">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="168f4-191">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-192">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-193">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-194">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-195">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-196">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-197">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-198">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-199">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="168f4-200">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="168f4-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="168f4-201">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="168f4-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="168f4-202">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="168f4-203">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="168f4-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="168f4-204">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="168f4-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="168f4-205">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-206">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-207">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-208">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-208">Billed sales</span></span></td>
<td><span data-ttu-id="168f4-209">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="168f4-210">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="168f4-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="168f4-211">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="168f4-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="168f4-212">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-213">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-214">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-215">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-216">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="168f4-217">Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="168f4-218">Događaj</span><span class="sxs-lookup"><span data-stu-id="168f4-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="168f4-219">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="168f4-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="168f4-220">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="168f4-221">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="168f4-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="168f4-222">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="168f4-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="168f4-223">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="168f4-224">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-224">Actuals</span></span></th>
<th><span data-ttu-id="168f4-225">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="168f4-225">Transaction currency</span></span></th>
<th><span data-ttu-id="168f4-226">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="168f4-226">Fixed price</span></span></th>
<th><span data-ttu-id="168f4-227">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="168f4-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="168f4-228">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="168f4-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="168f4-229">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-230">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="168f4-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="168f4-231">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="168f4-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="168f4-232">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="168f4-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="168f4-233">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-233">Cost actual</span></span></td>
<td><span data-ttu-id="168f4-234">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="168f4-235">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="168f4-236">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="168f4-237">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="168f4-238">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-239">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="168f4-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="168f4-240">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-241">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="168f4-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="168f4-242">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-243">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="168f4-244">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="168f4-245">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="168f4-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="168f4-246">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-246">Cost actual</span></span></td>
<td><span data-ttu-id="168f4-247">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-248">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-249">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-250">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-251">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="168f4-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-252">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="168f4-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="168f4-253">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-254">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="168f4-255">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="168f4-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-256">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-257">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-258">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-259">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="168f4-260">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="168f4-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="168f4-261">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="168f4-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-263">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="168f4-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-264">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-265">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="168f4-266">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-267">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-267">Billed sales</span></span></td>
<td><span data-ttu-id="168f4-268">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="168f4-269">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="168f4-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="168f4-270">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="168f4-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="168f4-271">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-272">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-273">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-274">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="168f4-275">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-276">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-277">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-278">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-279">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="168f4-280">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="168f4-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="168f4-281">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="168f4-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="168f4-282">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="168f4-283">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="168f4-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="168f4-284">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="168f4-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="168f4-285">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-286">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="168f4-287">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="168f4-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-288">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="168f4-288">Billed sales</span></span></td>
<td><span data-ttu-id="168f4-289">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="168f4-290">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="168f4-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="168f4-291">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="168f4-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="168f4-292">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-293">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="168f4-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="168f4-294">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="168f4-295">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="168f4-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="168f4-296">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="168f4-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
