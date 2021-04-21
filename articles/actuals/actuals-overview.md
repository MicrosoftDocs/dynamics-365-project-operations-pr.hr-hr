---
title: Stvarni podaci
description: U ovoj temi nalaze se informacije o radu sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852535"
---
# <a name="actuals"></a><span data-ttu-id="ffb15-103">Stvarni podaci</span><span class="sxs-lookup"><span data-stu-id="ffb15-103">Actuals</span></span> 

<span data-ttu-id="ffb15-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ffb15-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ffb15-105">Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu.</span><span class="sxs-lookup"><span data-stu-id="ffb15-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="ffb15-106">Stvoreni su kao rezultat odobravanja unosa vremena, troškova, utrošenog materijala te unosa i faktura dnevnika.</span><span class="sxs-lookup"><span data-stu-id="ffb15-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="ffb15-107">Redci temeljnice i prijavljivanje vremena</span><span class="sxs-lookup"><span data-stu-id="ffb15-107">Journal lines and time submission</span></span>

<span data-ttu-id="ffb15-108">Dodatne informacije o unosu vremena potražite u odjeljku [Pregled unosa vremena](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ffb15-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ffb15-109">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="ffb15-109">Time and materials</span></span>

<span data-ttu-id="ffb15-110">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="ffb15-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ffb15-111">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-111">Fixed price</span></span>

<span data-ttu-id="ffb15-112">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora s nepromjenjivom cijenom, sustav stvara jedan redak u temeljnici za trošak.</span><span class="sxs-lookup"><span data-stu-id="ffb15-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ffb15-113">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="ffb15-113">Default pricing</span></span>

<span data-ttu-id="ffb15-114">Logika za stvaranje zadanih cijena temelji se na retku temeljnice.</span><span class="sxs-lookup"><span data-stu-id="ffb15-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="ffb15-115">Vrijednosti polja iz unosa vremena kopiraju se u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="ffb15-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="ffb15-116">Te vrijednosti uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="ffb15-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="ffb15-117">Polja koja utječu na zadane cijene, kao što su **Uloga** i **Jedinica resursa** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="ffb15-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ffb15-118">Na unos vremena možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="ffb15-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="ffb15-119">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="ffb15-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ffb15-120">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="ffb15-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ffb15-121">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ffb15-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="ffb15-122">Redci temeljnice i slanje osnovnih troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="ffb15-123">Dodatne informacije o unosu troška potražite u odjeljku [Pregled unosa troška](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ffb15-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ffb15-124">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="ffb15-124">Time and materials</span></span>

<span data-ttu-id="ffb15-125">Kada je poslani unos osnovnog troška povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="ffb15-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ffb15-126">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-126">Fixed price</span></span>

<span data-ttu-id="ffb15-127">Kada je prijavljeni osnovni unos troška povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.</span><span class="sxs-lookup"><span data-stu-id="ffb15-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ffb15-128">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="ffb15-128">Default pricing</span></span>

<span data-ttu-id="ffb15-129">Logika unošenja zadanih cijena za troškove temelji se na kategoriji troškova.</span><span class="sxs-lookup"><span data-stu-id="ffb15-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="ffb15-130">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="ffb15-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ffb15-131">Polja koja utječu na zadane cijene, kao što su **Kategorija transakcije** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="ffb15-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ffb15-132">Međutim, to djeluje samo kada je način određivanja cijene u cjeniku **Cijena po jedinici**.</span><span class="sxs-lookup"><span data-stu-id="ffb15-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="ffb15-133">Ako je način određivanja cijene **Prema trošku** ili **Provizija povrh troška**, cijena unesena kada se stvorio unos troška upotrebljava se za trošak, a cijena u retku dnevnika prodaje izračunava se na temelju načina za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="ffb15-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="ffb15-134">Na unos troška možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="ffb15-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="ffb15-135">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="ffb15-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ffb15-136">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="ffb15-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ffb15-137">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ffb15-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="ffb15-138">Redci dnevnika i slanje zapisnika o utrošenom materijalu</span><span class="sxs-lookup"><span data-stu-id="ffb15-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="ffb15-139">Dodatne informacije o unosu troškova potražite u odjeljku [Zapisnik o utrošenom materijalu](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="ffb15-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ffb15-140">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="ffb15-140">Time and materials</span></span>

<span data-ttu-id="ffb15-141">Kada je prijavljeni zapisnik o utrošenom materijalu povezan s projektom koji je mapiran na redak ugovora o vremenu i materijalima, sustav stvara dva retka dnevnika, jedan za trošak i jedan za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="ffb15-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ffb15-142">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-142">Fixed price</span></span>

<span data-ttu-id="ffb15-143">Kada je prijavljeni unos zapisnika o utrošenom materijalu povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.</span><span class="sxs-lookup"><span data-stu-id="ffb15-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ffb15-144">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="ffb15-144">Default pricing</span></span>

<span data-ttu-id="ffb15-145">Logika unošenja zadanih cijena materijala temelji se na kombinaciji proizvoda i jedinice.</span><span class="sxs-lookup"><span data-stu-id="ffb15-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="ffb15-146">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="ffb15-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ffb15-147">Polja koja utječu na zadane cijene, kao što su **ID proizvoda** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="ffb15-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ffb15-148">Međutim, ovo vrijedi samo za kataloške proizvode.</span><span class="sxs-lookup"><span data-stu-id="ffb15-148">However, this only works for catalog products.</span></span> <span data-ttu-id="ffb15-149">Za proizvode koji se umeću, cijena unesena kada se stvarao unos zapisnika o utrošenom materijalu upotrebljava se za cijenu troška i prodajnu cijenu u redcima dnevnika.</span><span class="sxs-lookup"><span data-stu-id="ffb15-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="ffb15-150">Na unos **Zapisnik o utrošenom materijalu** možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="ffb15-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="ffb15-151">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="ffb15-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="ffb15-152">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="ffb15-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="ffb15-153">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="ffb15-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="ffb15-154">Uporaba temeljnica za unos za bilježenje troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-154">Use entry journals to record costs</span></span>

<span data-ttu-id="ffb15-155">Temeljnice za unos možete upotrebljavati za bilježenje troška ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="ffb15-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ffb15-156">Temeljnice se mogu upotrebljavati u sljedeće svrhe:</span><span class="sxs-lookup"><span data-stu-id="ffb15-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="ffb15-157">Premjestite stvarne vrijednosti transakcije iz drugog sustava u aplikaciju Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ffb15-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="ffb15-158">Bilježite troškove koji su se dogodili u drugom sustavu.</span><span class="sxs-lookup"><span data-stu-id="ffb15-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="ffb15-159">Ti troškovi mogu uključivati troškove nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="ffb15-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffb15-160">Aplikacija ne provjerava valjanost vrste retka temeljnice ili povezanog određivanja cijene koje se unosi u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="ffb15-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ffb15-161">Stoga bi samo korisnik koji je potpuno svjestan računovodstvenog utjecaja koji stvarni podaci imaju na projekt trebao upotrebljavati temeljnice unosa za stvaranje stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="ffb15-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="ffb15-162">Zbog utjecaja ove vrste temeljnice, trebali biste pažljivo odabrati tko ima pristup za stvaranje temeljnica za unos.</span><span class="sxs-lookup"><span data-stu-id="ffb15-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="ffb15-163">Bilježenje stvarnih podataka na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-163">Record actuals based on project events</span></span>

<span data-ttu-id="ffb15-164">Project Operations bilježi financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="ffb15-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ffb15-165">Te se transakcije zapisuju kao stvarne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="ffb15-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="ffb15-166">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="ffb15-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="ffb15-167">Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ffb15-168">Događaj</span><span class="sxs-lookup"><span data-stu-id="ffb15-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ffb15-169">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="ffb15-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ffb15-170">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ffb15-171">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="ffb15-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ffb15-172">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="ffb15-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ffb15-173">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ffb15-174">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-174">Actuals</span></span></th>
<th><span data-ttu-id="ffb15-175">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="ffb15-175">Transaction currency</span></span></th>
<th><span data-ttu-id="ffb15-176">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-176">Fixed price</span></span></th>
<th><span data-ttu-id="ffb15-177">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="ffb15-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb15-178">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ffb15-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ffb15-179">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-180">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ffb15-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ffb15-181">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ffb15-182">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="ffb15-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ffb15-183">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-183">Cost actual</span></span></td>
<td><span data-ttu-id="ffb15-184">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-185">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-186">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ffb15-187">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-188">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-189">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="ffb15-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ffb15-190">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ffb15-191">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="ffb15-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ffb15-192">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-192">Cost actual</span></span></td>
<td><span data-ttu-id="ffb15-193">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-194">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-195">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-196">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-197">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-198">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-199">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-200">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-201">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ffb15-202">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="ffb15-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ffb15-203">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ffb15-204">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-205">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="ffb15-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-206">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-207">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-208">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-209">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-209">Billed sales</span></span></td>
<td><span data-ttu-id="ffb15-210">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ffb15-211">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="ffb15-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ffb15-212">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ffb15-213">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-214">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-215">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-216">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-217">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-218">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-219">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-220">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-221">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ffb15-222">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="ffb15-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ffb15-223">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="ffb15-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ffb15-224">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ffb15-225">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="ffb15-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ffb15-226">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="ffb15-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ffb15-227">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-228">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-229">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-230">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-230">Billed sales</span></span></td>
<td><span data-ttu-id="ffb15-231">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ffb15-232">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="ffb15-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ffb15-233">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="ffb15-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ffb15-234">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-235">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-236">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-237">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-238">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="ffb15-239">Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ffb15-240">Događaj</span><span class="sxs-lookup"><span data-stu-id="ffb15-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ffb15-241">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="ffb15-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ffb15-242">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ffb15-243">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="ffb15-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ffb15-244">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="ffb15-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ffb15-245">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ffb15-246">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-246">Actuals</span></span></th>
<th><span data-ttu-id="ffb15-247">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="ffb15-247">Transaction currency</span></span></th>
<th><span data-ttu-id="ffb15-248">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="ffb15-248">Fixed price</span></span></th>
<th><span data-ttu-id="ffb15-249">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="ffb15-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ffb15-250">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ffb15-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ffb15-251">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-252">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ffb15-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ffb15-253">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="ffb15-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ffb15-254">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="ffb15-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ffb15-255">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-255">Cost actual</span></span></td>
<td><span data-ttu-id="ffb15-256">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ffb15-257">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ffb15-258">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ffb15-259">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ffb15-260">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-261">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="ffb15-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ffb15-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-263">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="ffb15-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ffb15-264">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-265">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ffb15-266">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ffb15-267">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="ffb15-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ffb15-268">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-268">Cost actual</span></span></td>
<td><span data-ttu-id="ffb15-269">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-270">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-271">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-272">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-273">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="ffb15-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-274">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="ffb15-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ffb15-275">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-276">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ffb15-277">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="ffb15-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-278">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-279">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-280">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-281">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ffb15-282">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="ffb15-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ffb15-283">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ffb15-284">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-285">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="ffb15-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-286">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-287">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ffb15-288">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-289">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-289">Billed sales</span></span></td>
<td><span data-ttu-id="ffb15-290">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ffb15-291">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="ffb15-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ffb15-292">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="ffb15-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ffb15-293">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-294">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-295">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-296">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ffb15-297">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-298">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-299">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-300">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-301">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ffb15-302">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="ffb15-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ffb15-303">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="ffb15-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ffb15-304">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ffb15-305">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="ffb15-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ffb15-306">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="ffb15-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ffb15-307">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-308">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ffb15-309">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="ffb15-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-310">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="ffb15-310">Billed sales</span></span></td>
<td><span data-ttu-id="ffb15-311">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ffb15-312">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="ffb15-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ffb15-313">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="ffb15-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ffb15-314">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-315">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="ffb15-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ffb15-316">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ffb15-317">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="ffb15-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ffb15-318">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="ffb15-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
