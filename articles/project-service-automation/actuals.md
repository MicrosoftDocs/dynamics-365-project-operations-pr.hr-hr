---
title: Stvarne vrijednosti
description: Ova tema pruža informacije o stvarnim vrijednostima projekta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750187"
---
# <a name="actuals"></a><span data-ttu-id="895c3-103">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="895c3-104">Stvarne vrijednosti su količina dovršenog posla na projektu.</span><span class="sxs-lookup"><span data-stu-id="895c3-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="895c3-105">Stvarne vrijednosti projekta mogu se pratiti natrag do njihovih izvornih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="895c3-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="895c3-106">Ti izvorni dokumenti uključuju unose vremena, izdataka i dnevnika, a također i faktura.</span><span class="sxs-lookup"><span data-stu-id="895c3-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se stvarne vrijednosti projekta prate do izvornih dokumenata](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="895c3-108">Slanje unosa vremena</span><span class="sxs-lookup"><span data-stu-id="895c3-108">Submitting a time entry</span></span>

<span data-ttu-id="895c3-109">U aplikaciji PSA, kada se šalje unos vremena za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="895c3-110">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="895c3-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="895c3-111">Kada se unos vremena šalje za projekt koji je mapiran u redak ugovora fiksne cijene, redak u dnevniku izrađuje se samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="895c3-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="895c3-112">Logika za unos zadanih cijena temelji se na retku u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="895c3-113">Sve vrijednosti polja iz unosa vremena kopiraju se u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="895c3-114">Ta polja uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="895c3-115">Polja koja utječu na zadane cijene, kao što su **Uloga** i **Org jedinica** uzrokuju odgovarajuću cijenu koja se prema zadanim postavkama unosi u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="895c3-116">Ako u unos vremena dodate prilagođeno polje, a želite da se vrijednost polja propagira do stvarnih vrijednosti, izradite polje u entitetu Stvarne vrijednosti i koristite mapiranja polja da biste kopirali polje iz unosa vremena u stvarnu vrijednost.</span><span class="sxs-lookup"><span data-stu-id="895c3-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="895c3-117">Slanje unosa izdatka</span><span class="sxs-lookup"><span data-stu-id="895c3-117">Submitting an expense entry</span></span>

<span data-ttu-id="895c3-118">U aplikaciji PSA, kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="895c3-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="895c3-119">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="895c3-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="895c3-120">Kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora fiksne cijene, izrađuje se redak u dnevniku samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="895c3-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="895c3-121">Logika za unos zadanih cijena za izdatke temelji se na kategoriji troška koja se odabire na stranici **Unos izdataka**.</span><span class="sxs-lookup"><span data-stu-id="895c3-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="895c3-122">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="895c3-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="895c3-123">Međutim, za samu cijenu, iznos koji je korisnik unio postavljen je izravno na povezane retke u dnevniku za izdatak i prodaju prema zadanim postavkama.</span><span class="sxs-lookup"><span data-stu-id="895c3-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="895c3-124">U trenutačnoj verziji aplikacije PSA, unos zadanih cijena po jedinici koji se temelji na kategoriji u unosima izdatka nije dostupan.</span><span class="sxs-lookup"><span data-stu-id="895c3-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="895c3-125">Korištenje dnevnika za zapis troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-125">Using journals to record costs</span></span>

<span data-ttu-id="895c3-126">U aplikaciji PSA, dnevnici služe za zapis troška ili prihoda u razredima materijala, naknade, vremena, izdatka ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="895c3-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="895c3-127">Dnevnik ima zaglavlje, retke i radnju **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="895c3-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="895c3-128">Evo nekih scenarija u kojima biste mogli koristiti dnevnik:</span><span class="sxs-lookup"><span data-stu-id="895c3-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="895c3-129">Morate zapisati stvarne troškove materijala i prodaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="895c3-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="895c3-130">Morate premještati stvarne vrijednosti transakcije iz drugog sustava u aplikaciju PSA.</span><span class="sxs-lookup"><span data-stu-id="895c3-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="895c3-131">Morate zapisati troškove koji su se pojavili u drugom sustavu, kao što su troškovi nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="895c3-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="895c3-132">Zapis stvarnih vrijednosti na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="895c3-132">Recording actuals based on project events</span></span>

<span data-ttu-id="895c3-133">PSA zapisuje financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="895c3-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="895c3-134">Te se transakcije zapisuju kao **stvarne vrijednosti**.</span><span class="sxs-lookup"><span data-stu-id="895c3-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="895c3-135">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="895c3-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="895c3-136">**Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta**</span><span class="sxs-lookup"><span data-stu-id="895c3-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="895c3-137">Događaj</span><span class="sxs-lookup"><span data-stu-id="895c3-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="895c3-138">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="895c3-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="895c3-139">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="895c3-140">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="895c3-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="895c3-141">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="895c3-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="895c3-142">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="895c3-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="895c3-143">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-143">Actuals</span></span></th>
<th><span data-ttu-id="895c3-144">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="895c3-144">Transaction currency</span></span></th>
<th><span data-ttu-id="895c3-145">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="895c3-145">Fixed price</span></span></th>
<th><span data-ttu-id="895c3-146">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="895c3-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="895c3-147">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="895c3-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="895c3-148">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-149">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="895c3-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="895c3-150">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="895c3-151">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="895c3-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="895c3-152">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-152">Cost actual</span></span></td>
<td><span data-ttu-id="895c3-153">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-154">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-155">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="895c3-156">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-157">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-158">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="895c3-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="895c3-159">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="895c3-160">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="895c3-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="895c3-161">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-161">Cost actual</span></span></td>
<td><span data-ttu-id="895c3-162">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-163">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-164">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-165">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-166">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-167">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-168">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-169">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-170">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="895c3-171">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="895c3-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="895c3-172">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="895c3-173">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-174">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="895c3-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-175">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-176">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-177">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-178">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-178">Billed sales</span></span></td>
<td><span data-ttu-id="895c3-179">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="895c3-180">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="895c3-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="895c3-181">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="895c3-182">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-183">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-184">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-185">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-186">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-187">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-188">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-189">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-190">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="895c3-191">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="895c3-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="895c3-192">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="895c3-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="895c3-193">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="895c3-194">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="895c3-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="895c3-195">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="895c3-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="895c3-196">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-197">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-198">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-199">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-199">Billed sales</span></span></td>
<td><span data-ttu-id="895c3-200">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="895c3-201">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="895c3-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="895c3-202">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="895c3-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="895c3-203">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-204">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-205">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-206">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-207">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="895c3-208">**Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta**</span><span class="sxs-lookup"><span data-stu-id="895c3-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="895c3-209">Događaj</span><span class="sxs-lookup"><span data-stu-id="895c3-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="895c3-210">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="895c3-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="895c3-211">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="895c3-212">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="895c3-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="895c3-213">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="895c3-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="895c3-214">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="895c3-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="895c3-215">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-215">Actuals</span></span></th>
<th><span data-ttu-id="895c3-216">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="895c3-216">Transaction currency</span></span></th>
<th><span data-ttu-id="895c3-217">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="895c3-217">Fixed price</span></span></th>
<th><span data-ttu-id="895c3-218">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="895c3-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="895c3-219">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="895c3-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="895c3-220">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-221">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="895c3-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="895c3-222">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="895c3-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="895c3-223">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="895c3-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="895c3-224">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-224">Cost actual</span></span></td>
<td><span data-ttu-id="895c3-225">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="895c3-226">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="895c3-227">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="895c3-228">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="895c3-229">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-230">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="895c3-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="895c3-231">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-232">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="895c3-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="895c3-233">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-234">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="895c3-235">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="895c3-236">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="895c3-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="895c3-237">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-237">Cost actual</span></span></td>
<td><span data-ttu-id="895c3-238">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-239">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-240">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-241">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-242">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="895c3-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-243">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="895c3-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="895c3-244">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-245">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="895c3-246">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="895c3-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-247">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-248">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-249">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-250">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="895c3-251">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="895c3-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="895c3-252">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="895c3-253">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-254">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="895c3-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-255">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-256">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="895c3-257">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-258">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-258">Billed sales</span></span></td>
<td><span data-ttu-id="895c3-259">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="895c3-260">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="895c3-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="895c3-261">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="895c3-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="895c3-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-263">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-264">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-265">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="895c3-266">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-267">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-268">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-269">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-270">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="895c3-271">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="895c3-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="895c3-272">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="895c3-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="895c3-273">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="895c3-274">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="895c3-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="895c3-275">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="895c3-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="895c3-276">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-277">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="895c3-278">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="895c3-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-279">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="895c3-279">Billed sales</span></span></td>
<td><span data-ttu-id="895c3-280">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="895c3-281">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="895c3-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="895c3-282">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="895c3-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="895c3-283">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-284">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="895c3-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="895c3-285">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="895c3-286">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="895c3-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="895c3-287">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="895c3-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
