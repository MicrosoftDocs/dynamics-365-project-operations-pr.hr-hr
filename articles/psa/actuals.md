---
title: Pregled stvarnih podataka
description: Ova tema pruža informacije o stvarnim vrijednostima projekta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: 9559cb2dcc38cb8058c5a9a3b97a35019fea486f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073586"
---
# <a name="actuals-overview"></a><span data-ttu-id="599da-103">Pregled stvarnih podataka</span><span class="sxs-lookup"><span data-stu-id="599da-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="599da-104">Stvarne vrijednosti su količina dovršenog posla na projektu.</span><span class="sxs-lookup"><span data-stu-id="599da-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="599da-105">Stvarne vrijednosti projekta mogu se pratiti natrag do njihovih izvornih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="599da-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="599da-106">Ti izvorni dokumenti uključuju unose vremena, izdataka i dnevnika, a također i faktura.</span><span class="sxs-lookup"><span data-stu-id="599da-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se stvarne vrijednosti projekta prate do izvornih dokumenata](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="599da-108">Slanje unosa vremena</span><span class="sxs-lookup"><span data-stu-id="599da-108">Submitting a time entry</span></span>

<span data-ttu-id="599da-109">U aplikaciji PSA, kada se šalje unos vremena za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="599da-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="599da-110">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="599da-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="599da-111">Kada se unos vremena šalje za projekt koji je mapiran u redak ugovora fiksne cijene, redak u dnevniku izrađuje se samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="599da-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="599da-112">Logika za unos zadanih cijena temelji se na retku u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="599da-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="599da-113">Sve vrijednosti polja iz unosa vremena kopiraju se u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="599da-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="599da-114">Ta polja uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="599da-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="599da-115">Polja koja utječu na zadane cijene, kao što su **Uloga** i **Org jedinica** uzrokuju odgovarajuću cijenu koja se prema zadanim postavkama unosi u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="599da-115">The fields that affect default prices, such as **Role** and **Org Unit** , cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="599da-116">Ako u unos vremena dodate prilagođeno polje, a želite da se vrijednost polja propagira do stvarnih vrijednosti, izradite polje u entitetu Stvarne vrijednosti i koristite mapiranja polja da biste kopirali polje iz unosa vremena u stvarnu vrijednost.</span><span class="sxs-lookup"><span data-stu-id="599da-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="599da-117">Slanje unosa izdatka</span><span class="sxs-lookup"><span data-stu-id="599da-117">Submitting an expense entry</span></span>

<span data-ttu-id="599da-118">U aplikaciji PSA, kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora vremena i materijala, izrađuju se dva retka u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="599da-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="599da-119">Jedan redak je za trošak, a drugi redak je za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="599da-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="599da-120">Kada se šalje unos izdatka za projekt koji je mapiran u redak ugovora fiksne cijene, izrađuje se redak u dnevniku samo za trošak.</span><span class="sxs-lookup"><span data-stu-id="599da-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="599da-121">Logika za unos zadanih cijena za izdatke temelji se na kategoriji troška koja se odabire na stranici **Unos izdataka**.</span><span class="sxs-lookup"><span data-stu-id="599da-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="599da-122">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="599da-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="599da-123">Međutim, za samu cijenu, iznos koji je korisnik unio postavljen je izravno na povezane retke u dnevniku za izdatak i prodaju prema zadanim postavkama.</span><span class="sxs-lookup"><span data-stu-id="599da-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="599da-124">U trenutačnoj verziji aplikacije PSA, unos zadanih cijena po jedinici koji se temelji na kategoriji u unosima troška nije dostupan.</span><span class="sxs-lookup"><span data-stu-id="599da-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="599da-125">Uporaba dnevnika unosa za zapis troškova</span><span class="sxs-lookup"><span data-stu-id="599da-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="599da-126">U aplikaciji PSA, dnevnici unosa služe za zapis troškova ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="599da-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="599da-127">Dnevnik ima zaglavlje, retke i radnju **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="599da-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="599da-128">Evo nekih scenarija u kojima biste mogli koristiti dnevnik:</span><span class="sxs-lookup"><span data-stu-id="599da-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="599da-129">Morate zapisati stvarne troškove materijala i prodaju na projektu.</span><span class="sxs-lookup"><span data-stu-id="599da-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="599da-130">Morate premještati stvarne vrijednosti transakcije iz drugog sustava u aplikaciju PSA.</span><span class="sxs-lookup"><span data-stu-id="599da-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="599da-131">Morate zapisati troškove koji su se pojavili u drugom sustavu, kao što su troškovi nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="599da-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="599da-132">Uporabu dnevnika unosa za stvaranje stvarnih podataka trebao bi napraviti samo korisnik koji je u potpunosti svjestan računovodstvenog utjecaja koje stvarni podaci imaju na projekt.</span><span class="sxs-lookup"><span data-stu-id="599da-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="599da-133">To je zato što aplikacija ne provjerava valjanost vrste retka u dnevniku ili povezanu cijenu koja je unesena u redak dnevnika.</span><span class="sxs-lookup"><span data-stu-id="599da-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="599da-134">Zbog utjecaja ovog tipa dnevnika, budite dovoljno oprezni kada drugima omogućujete pristup stvaranju dnevnika unosa.</span><span class="sxs-lookup"><span data-stu-id="599da-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="599da-135">Zapis stvarnih vrijednosti na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="599da-135">Recording actuals based on project events</span></span>

<span data-ttu-id="599da-136">PSA zapisuje financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="599da-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="599da-137">Te se transakcije zapisuju kao **stvarne vrijednosti**.</span><span class="sxs-lookup"><span data-stu-id="599da-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="599da-138">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="599da-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="599da-139">**Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta**</span><span class="sxs-lookup"><span data-stu-id="599da-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="599da-140">Događaj</span><span class="sxs-lookup"><span data-stu-id="599da-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="599da-141">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="599da-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="599da-142">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="599da-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="599da-143">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="599da-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="599da-144">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="599da-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="599da-145">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="599da-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="599da-146">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-146">Actuals</span></span></th>
<th><span data-ttu-id="599da-147">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="599da-147">Transaction currency</span></span></th>
<th><span data-ttu-id="599da-148">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="599da-148">Fixed price</span></span></th>
<th><span data-ttu-id="599da-149">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="599da-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="599da-150">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="599da-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="599da-151">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-152">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="599da-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="599da-153">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="599da-154">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="599da-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="599da-155">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-155">Cost actual</span></span></td>
<td><span data-ttu-id="599da-156">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-157">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-158">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="599da-159">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-160">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-161">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="599da-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="599da-162">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="599da-163">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="599da-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="599da-164">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-164">Cost actual</span></span></td>
<td><span data-ttu-id="599da-165">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-166">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-167">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-168">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-169">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-170">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="599da-171">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-172">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-173">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="599da-174">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="599da-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="599da-175">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="599da-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="599da-176">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-177">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="599da-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-178">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-179">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-180">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-181">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-181">Billed sales</span></span></td>
<td><span data-ttu-id="599da-182">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="599da-183">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="599da-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="599da-184">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="599da-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="599da-185">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-186">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-187">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-188">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-189">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-190">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="599da-191">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-192">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-193">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="599da-194">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="599da-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="599da-195">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="599da-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="599da-196">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="599da-197">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="599da-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="599da-198">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="599da-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="599da-199">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-200">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-201">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-202">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-202">Billed sales</span></span></td>
<td><span data-ttu-id="599da-203">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="599da-204">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="599da-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="599da-205">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="599da-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="599da-206">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-207">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="599da-208">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-209">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-210">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="599da-211">**Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta**</span><span class="sxs-lookup"><span data-stu-id="599da-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="599da-212">Događaj</span><span class="sxs-lookup"><span data-stu-id="599da-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="599da-213">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="599da-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="599da-214">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="599da-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="599da-215">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="599da-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="599da-216">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="599da-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="599da-217">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="599da-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="599da-218">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-218">Actuals</span></span></th>
<th><span data-ttu-id="599da-219">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="599da-219">Transaction currency</span></span></th>
<th><span data-ttu-id="599da-220">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="599da-220">Fixed price</span></span></th>
<th><span data-ttu-id="599da-221">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="599da-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="599da-222">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="599da-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="599da-223">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-224">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="599da-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="599da-225">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="599da-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="599da-226">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="599da-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="599da-227">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-227">Cost actual</span></span></td>
<td><span data-ttu-id="599da-228">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="599da-229">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="599da-230">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="599da-231">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="599da-232">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-233">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="599da-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="599da-234">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-235">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="599da-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="599da-236">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-237">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="599da-238">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="599da-239">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="599da-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="599da-240">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-240">Cost actual</span></span></td>
<td><span data-ttu-id="599da-241">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-242">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-243">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-244">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-245">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="599da-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-246">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="599da-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="599da-247">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-248">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="599da-249">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="599da-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-250">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="599da-251">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-252">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-253">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="599da-254">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="599da-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="599da-255">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="599da-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="599da-256">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-257">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="599da-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-258">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-259">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="599da-260">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-261">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-261">Billed sales</span></span></td>
<td><span data-ttu-id="599da-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="599da-263">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="599da-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="599da-264">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="599da-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="599da-265">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-266">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-267">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-268">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="599da-269">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-270">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="599da-271">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-272">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-273">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="599da-274">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="599da-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="599da-275">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="599da-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="599da-276">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="599da-277">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="599da-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="599da-278">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="599da-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="599da-279">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-280">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="599da-281">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="599da-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-282">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="599da-282">Billed sales</span></span></td>
<td><span data-ttu-id="599da-283">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="599da-284">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="599da-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="599da-285">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="599da-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="599da-286">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-287">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="599da-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="599da-288">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="599da-289">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="599da-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="599da-290">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="599da-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
