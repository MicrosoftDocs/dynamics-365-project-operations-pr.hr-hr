---
title: Pregled stvarnih podataka
description: Ova tema pruža informacije o stvarnim vrijednostima projekta.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368152"
---
# <a name="actuals-overview"></a><span data-ttu-id="5336f-103">Pregled stvarnih podataka</span><span class="sxs-lookup"><span data-stu-id="5336f-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5336f-104">Stvarne vrijednosti su količina dovršenog posla na projektu.</span><span class="sxs-lookup"><span data-stu-id="5336f-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5336f-105">Stvarne vrijednosti projekta mogu se pratiti natrag do njihovih izvornih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="5336f-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5336f-106">Ti izvorni dokumenti uključuju unose vremena, izdataka i dnevnika, a također i faktura.</span><span class="sxs-lookup"><span data-stu-id="5336f-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se stvarne vrijednosti projekta prate do izvornih dokumenata](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5336f-108">Slanje unosa vremena</span><span class="sxs-lookup"><span data-stu-id="5336f-108">Submitting a time entry</span></span>

<span data-ttu-id="5336f-109">U aplikaciji PSA, kada se šalje unos vremena za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5336f-110">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="5336f-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5336f-111">Kada se unos vremena šalje za projekt koji je mapiran u redak ugovora fiksne cijene, redak u dnevniku izrađuje se samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="5336f-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5336f-112">Logika za unos zadanih cijena temelji se na retku u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5336f-113">Sve vrijednosti polja iz unosa vremena kopiraju se u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5336f-114">Ta polja uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5336f-115">Polja koja utječu na zadane cijene, kao što su **Uloga** i **Org jedinica** uzrokuju odgovarajuću cijenu koja se prema zadanim postavkama unosi u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5336f-116">Ako u unos vremena dodate prilagođeno polje, a želite da se vrijednost polja propagira do stvarnih vrijednosti, izradite polje u entitetu Stvarne vrijednosti i koristite mapiranja polja da biste kopirali polje iz unosa vremena u stvarnu vrijednost.</span><span class="sxs-lookup"><span data-stu-id="5336f-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5336f-117">Slanje unosa izdatka</span><span class="sxs-lookup"><span data-stu-id="5336f-117">Submitting an expense entry</span></span>

<span data-ttu-id="5336f-118">U aplikaciji PSA, kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="5336f-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5336f-119">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="5336f-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5336f-120">Kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora fiksne cijene, izrađuje se redak u dnevniku samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="5336f-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5336f-121">Logika za unos zadanih cijena za izdatke temelji se na kategoriji troška koja se odabire na stranici **Unos izdataka**.</span><span class="sxs-lookup"><span data-stu-id="5336f-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5336f-122">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="5336f-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5336f-123">Međutim, za samu cijenu, iznos koji je korisnik unio postavljen je izravno na povezane retke u dnevniku za izdatak i prodaju prema zadanim postavkama.</span><span class="sxs-lookup"><span data-stu-id="5336f-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5336f-124">U trenutačnoj verziji aplikacije PSA, unos zadanih cijena po jedinici koji se temelji na kategoriji u unosima troška nije dostupan.</span><span class="sxs-lookup"><span data-stu-id="5336f-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="5336f-125">Uporaba dnevnika unosa za zapis troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="5336f-126">U aplikaciji PSA, dnevnici unosa služe za zapis troškova ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="5336f-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5336f-127">Dnevnik ima zaglavlje, retke i radnju **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="5336f-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5336f-128">Evo nekih scenarija u kojima biste mogli koristiti dnevnik:</span><span class="sxs-lookup"><span data-stu-id="5336f-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5336f-129">Morate zapisati stvarne troškove materijala i prodaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="5336f-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5336f-130">Morate premještati stvarne vrijednosti transakcije iz drugog sustava u aplikaciju PSA.</span><span class="sxs-lookup"><span data-stu-id="5336f-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5336f-131">Morate zapisati troškove koji su se pojavili u drugom sustavu, kao što su troškovi nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="5336f-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5336f-132">Uporabu dnevnika unosa za stvaranje stvarnih podataka trebao bi napraviti samo korisnik koji je u potpunosti svjestan računovodstvenog utjecaja koje stvarni podaci imaju na projekt.</span><span class="sxs-lookup"><span data-stu-id="5336f-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="5336f-133">To je zato što aplikacija ne provjerava valjanost vrste retka u dnevniku ili povezanu cijenu koja je unesena u redak dnevnika.</span><span class="sxs-lookup"><span data-stu-id="5336f-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5336f-134">Zbog utjecaja ovog tipa dnevnika, budite dovoljno oprezni kada drugima omogućujete pristup stvaranju dnevnika unosa.</span><span class="sxs-lookup"><span data-stu-id="5336f-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5336f-135">Zapis stvarnih vrijednosti na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="5336f-135">Recording actuals based on project events</span></span>

<span data-ttu-id="5336f-136">PSA zapisuje financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="5336f-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5336f-137">Te se transakcije zapisuju kao **stvarne vrijednosti**.</span><span class="sxs-lookup"><span data-stu-id="5336f-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5336f-138">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="5336f-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5336f-139">**Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta**</span><span class="sxs-lookup"><span data-stu-id="5336f-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5336f-140">Događaj</span><span class="sxs-lookup"><span data-stu-id="5336f-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5336f-141">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="5336f-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5336f-142">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5336f-143">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="5336f-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5336f-144">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="5336f-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5336f-145">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="5336f-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5336f-146">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-146">Actuals</span></span></th>
<th><span data-ttu-id="5336f-147">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="5336f-147">Transaction currency</span></span></th>
<th><span data-ttu-id="5336f-148">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="5336f-148">Fixed price</span></span></th>
<th><span data-ttu-id="5336f-149">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="5336f-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5336f-150">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="5336f-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5336f-151">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-152">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="5336f-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5336f-153">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5336f-154">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="5336f-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5336f-155">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-155">Cost actual</span></span></td>
<td><span data-ttu-id="5336f-156">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-157">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-158">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5336f-159">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-160">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-161">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="5336f-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5336f-162">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5336f-163">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="5336f-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5336f-164">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-164">Cost actual</span></span></td>
<td><span data-ttu-id="5336f-165">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-166">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-167">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-168">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-169">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-170">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-171">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-172">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-173">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5336f-174">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="5336f-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5336f-175">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5336f-176">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-177">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="5336f-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-178">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-179">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-180">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-181">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-181">Billed sales</span></span></td>
<td><span data-ttu-id="5336f-182">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5336f-183">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="5336f-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5336f-184">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5336f-185">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-186">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-187">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-188">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-189">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-190">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-191">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-192">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-193">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5336f-194">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="5336f-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5336f-195">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="5336f-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5336f-196">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5336f-197">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="5336f-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5336f-198">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="5336f-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5336f-199">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-200">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-201">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-202">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-202">Billed sales</span></span></td>
<td><span data-ttu-id="5336f-203">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5336f-204">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="5336f-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5336f-205">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="5336f-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5336f-206">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-207">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-208">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-209">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-210">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5336f-211">**Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta**</span><span class="sxs-lookup"><span data-stu-id="5336f-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5336f-212">Događaj</span><span class="sxs-lookup"><span data-stu-id="5336f-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5336f-213">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="5336f-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5336f-214">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5336f-215">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="5336f-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5336f-216">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="5336f-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5336f-217">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="5336f-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5336f-218">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-218">Actuals</span></span></th>
<th><span data-ttu-id="5336f-219">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="5336f-219">Transaction currency</span></span></th>
<th><span data-ttu-id="5336f-220">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="5336f-220">Fixed price</span></span></th>
<th><span data-ttu-id="5336f-221">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="5336f-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5336f-222">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="5336f-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5336f-223">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-224">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="5336f-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5336f-225">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="5336f-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5336f-226">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="5336f-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5336f-227">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-227">Cost actual</span></span></td>
<td><span data-ttu-id="5336f-228">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5336f-229">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5336f-230">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5336f-231">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5336f-232">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-233">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="5336f-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5336f-234">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-235">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="5336f-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5336f-236">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-237">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5336f-238">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5336f-239">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="5336f-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5336f-240">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-240">Cost actual</span></span></td>
<td><span data-ttu-id="5336f-241">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-242">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-243">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-244">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-245">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="5336f-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-246">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="5336f-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5336f-247">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-248">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5336f-249">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="5336f-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-250">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-251">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-252">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-253">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5336f-254">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="5336f-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5336f-255">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5336f-256">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-257">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="5336f-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-258">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-259">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5336f-260">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-261">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-261">Billed sales</span></span></td>
<td><span data-ttu-id="5336f-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5336f-263">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="5336f-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5336f-264">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="5336f-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5336f-265">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-266">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-267">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-268">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5336f-269">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-270">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-271">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-272">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-273">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5336f-274">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="5336f-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5336f-275">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="5336f-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5336f-276">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5336f-277">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="5336f-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5336f-278">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="5336f-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5336f-279">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-280">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5336f-281">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="5336f-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-282">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="5336f-282">Billed sales</span></span></td>
<td><span data-ttu-id="5336f-283">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5336f-284">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="5336f-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5336f-285">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="5336f-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5336f-286">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-287">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="5336f-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5336f-288">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5336f-289">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="5336f-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5336f-290">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="5336f-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]