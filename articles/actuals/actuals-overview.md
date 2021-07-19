---
title: Stvarni podaci
description: U ovoj temi nalaze se informacije o radu sa stvarnim podacima u aplikaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368602"
---
# <a name="actuals"></a><span data-ttu-id="a86e7-103">Stvarni podaci</span><span class="sxs-lookup"><span data-stu-id="a86e7-103">Actuals</span></span> 

<span data-ttu-id="a86e7-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="a86e7-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a86e7-105">Stvarni podaci predstavljaju pregledani i odobreni financijski napredak i napredak rasporeda na projektu.</span><span class="sxs-lookup"><span data-stu-id="a86e7-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="a86e7-106">Stvoreni su kao rezultat odobravanja unosa vremena, troškova, utrošenog materijala te unosa i faktura dnevnika.</span><span class="sxs-lookup"><span data-stu-id="a86e7-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="a86e7-107">Redci temeljnice i prijavljivanje vremena</span><span class="sxs-lookup"><span data-stu-id="a86e7-107">Journal lines and time submission</span></span>

<span data-ttu-id="a86e7-108">Dodatne informacije o unosu vremena potražite u odjeljku [Pregled unosa vremena](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a86e7-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a86e7-109">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="a86e7-109">Time and materials</span></span>

<span data-ttu-id="a86e7-110">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="a86e7-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a86e7-111">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-111">Fixed price</span></span>

<span data-ttu-id="a86e7-112">Kada je poslani unos vremena povezan s projektom koji je mapiran u redak ugovora s nepromjenjivom cijenom, sustav stvara jedan redak u temeljnici za trošak.</span><span class="sxs-lookup"><span data-stu-id="a86e7-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a86e7-113">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="a86e7-113">Default pricing</span></span>

<span data-ttu-id="a86e7-114">Logika za stvaranje zadanih cijena temelji se na retku temeljnice.</span><span class="sxs-lookup"><span data-stu-id="a86e7-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="a86e7-115">Vrijednosti polja iz unosa vremena kopiraju se u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="a86e7-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="a86e7-116">Te vrijednosti uključuju datum transakcije, redak ugovora u koji je projekt mapiran i rezultat valute na odgovarajućem cjeniku.</span><span class="sxs-lookup"><span data-stu-id="a86e7-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="a86e7-117">Polja koja utječu na zadane cijene, kao što su **Uloga** i **Jedinica resursa** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="a86e7-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a86e7-118">Na unos vremena možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="a86e7-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="a86e7-119">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="a86e7-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a86e7-120">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="a86e7-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a86e7-121">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a86e7-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="a86e7-122">Redci temeljnice i slanje osnovnih troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="a86e7-123">Dodatne informacije o unosu troška potražite u odjeljku [Pregled unosa troška](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a86e7-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a86e7-124">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="a86e7-124">Time and materials</span></span>

<span data-ttu-id="a86e7-125">Kada je poslani unos osnovnog troška povezan s projektom koji je mapiran u redak ugovora za vrijeme i materijal, sustav stvara dva retka temeljnice, jedan za troškove i drugi za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="a86e7-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a86e7-126">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-126">Fixed price</span></span>

<span data-ttu-id="a86e7-127">Kada je prijavljeni osnovni unos troška povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.</span><span class="sxs-lookup"><span data-stu-id="a86e7-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a86e7-128">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="a86e7-128">Default pricing</span></span>

<span data-ttu-id="a86e7-129">Logika unošenja zadanih cijena za troškove temelji se na kategoriji troškova.</span><span class="sxs-lookup"><span data-stu-id="a86e7-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="a86e7-130">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="a86e7-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a86e7-131">Polja koja utječu na zadane cijene, kao što su **Kategorija transakcije** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="a86e7-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a86e7-132">Međutim, to djeluje samo kada je način određivanja cijene u cjeniku **Cijena po jedinici**.</span><span class="sxs-lookup"><span data-stu-id="a86e7-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="a86e7-133">Ako je način određivanja cijene **Prema trošku** ili **Provizija povrh troška**, cijena unesena kada se stvorio unos troška upotrebljava se za trošak, a cijena u retku dnevnika prodaje izračunava se na temelju načina za određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="a86e7-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="a86e7-134">Na unos troška možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="a86e7-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="a86e7-135">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="a86e7-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a86e7-136">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="a86e7-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a86e7-137">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a86e7-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="a86e7-138">Redci dnevnika i slanje zapisnika o utrošenom materijalu</span><span class="sxs-lookup"><span data-stu-id="a86e7-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="a86e7-139">Dodatne informacije o unosu troškova potražite u odjeljku [Zapisnik o utrošenom materijalu](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="a86e7-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a86e7-140">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="a86e7-140">Time and materials</span></span>

<span data-ttu-id="a86e7-141">Kada je prijavljeni zapisnik o utrošenom materijalu povezan s projektom koji je mapiran na redak ugovora o vremenu i materijalima, sustav stvara dva retka dnevnika, jedan za trošak i jedan za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="a86e7-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a86e7-142">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-142">Fixed price</span></span>

<span data-ttu-id="a86e7-143">Kada je prijavljeni unos zapisnika o utrošenom materijalu povezan s projektom koji je mapiran u redak ugovora s fiksnom cijenom, sustav stvara jedan redak u dnevniku za trošak.</span><span class="sxs-lookup"><span data-stu-id="a86e7-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a86e7-144">Zadano određivanje cijene</span><span class="sxs-lookup"><span data-stu-id="a86e7-144">Default pricing</span></span>

<span data-ttu-id="a86e7-145">Logika unošenja zadanih cijena materijala temelji se na kombinaciji proizvoda i jedinice.</span><span class="sxs-lookup"><span data-stu-id="a86e7-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="a86e7-146">Datum transakcije, redak ugovora u kojem je projekt mapiran i valuta koriste se za određivanje odgovarajućeg cjenika.</span><span class="sxs-lookup"><span data-stu-id="a86e7-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a86e7-147">Polja koja utječu na zadane cijene, kao što su **ID proizvoda** i **Jedinica** upotrebljavaju se za određivanje odgovarajuće cijene u redak u dnevniku.</span><span class="sxs-lookup"><span data-stu-id="a86e7-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a86e7-148">Međutim, ovo vrijedi samo za kataloške proizvode.</span><span class="sxs-lookup"><span data-stu-id="a86e7-148">However, this only works for catalog products.</span></span> <span data-ttu-id="a86e7-149">Za proizvode koji se umeću, cijena unesena kada se stvarao unos zapisnika o utrošenom materijalu upotrebljava se za cijenu troška i prodajnu cijenu u redcima dnevnika.</span><span class="sxs-lookup"><span data-stu-id="a86e7-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="a86e7-150">Na unos **Zapisnik o utrošenom materijalu** možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="a86e7-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="a86e7-151">Ako želite da se vrijednost polja proširi na stvarne podatke, stvorite polje u tablicama **Stvarni podaci** i **Redak dnevnika**.</span><span class="sxs-lookup"><span data-stu-id="a86e7-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a86e7-152">Upotrijebite prilagođeni kôd za širenje odabrane vrijednosti polja iz Vremenskog unosa u Stvarne podatke putem retka dnevnika s pomoću izvora transakcija.</span><span class="sxs-lookup"><span data-stu-id="a86e7-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a86e7-153">Dodatne informacija o izvorima transakcija i vezama potražite u odjeljku [Povezivanje stvarnih podataka s izvornim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a86e7-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="a86e7-154">Uporaba temeljnica za unos za bilježenje troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-154">Use entry journals to record costs</span></span>

<span data-ttu-id="a86e7-155">Temeljnice za unos možete upotrebljavati za bilježenje troška ili prihoda u razredima materijala, naknade, vremena, troška ili porezne transakcije.</span><span class="sxs-lookup"><span data-stu-id="a86e7-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a86e7-156">Temeljnice se mogu upotrebljavati u sljedeće svrhe:</span><span class="sxs-lookup"><span data-stu-id="a86e7-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="a86e7-157">Premjestite stvarne vrijednosti transakcije iz drugog sustava u aplikaciju Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a86e7-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="a86e7-158">Bilježite troškove koji su se dogodili u drugom sustavu.</span><span class="sxs-lookup"><span data-stu-id="a86e7-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="a86e7-159">Ti troškovi mogu uključivati troškove nabave ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="a86e7-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a86e7-160">Aplikacija ne provjerava valjanost vrste retka temeljnice ili povezanog određivanja cijene koje se unosi u redak temeljnice.</span><span class="sxs-lookup"><span data-stu-id="a86e7-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a86e7-161">Stoga bi samo korisnik koji je potpuno svjestan računovodstvenog utjecaja koji stvarni podaci imaju na projekt trebao upotrebljavati temeljnice unosa za stvaranje stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="a86e7-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="a86e7-162">Zbog utjecaja ove vrste temeljnice, trebali biste pažljivo odabrati tko ima pristup za stvaranje temeljnica za unos.</span><span class="sxs-lookup"><span data-stu-id="a86e7-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="a86e7-163">Bilježenje stvarnih podataka na temelju projektnih događaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-163">Record actuals based on project events</span></span>

<span data-ttu-id="a86e7-164">Project Operations bilježi financijske transakcije koje se odvijaju tijekom projekta.</span><span class="sxs-lookup"><span data-stu-id="a86e7-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a86e7-165">Te se transakcije zapisuju kao stvarne vrijednosti.</span><span class="sxs-lookup"><span data-stu-id="a86e7-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="a86e7-166">Sljedeće tablice prikazuju različite vrste stvarnih vrijednosti koje se izrađuju, ovisno o tome radi li se o projektu s vremenom i materijalima ili o projektu s fiksnom cijenom, o projektu u fazi pretprodaje ili o internom projektu.</span><span class="sxs-lookup"><span data-stu-id="a86e7-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="a86e7-167">Resurs pripada istoj organizacijskoj jedinici kao i ugovorna jedinica projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a86e7-168">Događaj</span><span class="sxs-lookup"><span data-stu-id="a86e7-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a86e7-169">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="a86e7-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a86e7-170">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a86e7-171">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="a86e7-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a86e7-172">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="a86e7-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a86e7-173">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a86e7-174">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-174">Actuals</span></span></th>
<th><span data-ttu-id="a86e7-175">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="a86e7-175">Transaction currency</span></span></th>
<th><span data-ttu-id="a86e7-176">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-176">Fixed price</span></span></th>
<th><span data-ttu-id="a86e7-177">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="a86e7-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a86e7-178">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="a86e7-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a86e7-179">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-180">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="a86e7-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a86e7-181">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a86e7-182">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="a86e7-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a86e7-183">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-183">Cost actual</span></span></td>
<td><span data-ttu-id="a86e7-184">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-185">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-186">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a86e7-187">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-188">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-189">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="a86e7-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a86e7-190">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a86e7-191">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="a86e7-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a86e7-192">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-192">Cost actual</span></span></td>
<td><span data-ttu-id="a86e7-193">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-194">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-195">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-196">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-197">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-198">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-199">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-200">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-201">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a86e7-202">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="a86e7-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a86e7-203">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a86e7-204">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-205">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="a86e7-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-206">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-207">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-208">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-209">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-209">Billed sales</span></span></td>
<td><span data-ttu-id="a86e7-210">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a86e7-211">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="a86e7-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a86e7-212">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a86e7-213">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-214">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-215">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-216">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-217">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-218">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-219">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-220">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-221">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a86e7-222">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="a86e7-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a86e7-223">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="a86e7-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a86e7-224">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a86e7-225">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="a86e7-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a86e7-226">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="a86e7-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a86e7-227">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-228">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-229">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-230">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-230">Billed sales</span></span></td>
<td><span data-ttu-id="a86e7-231">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a86e7-232">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="a86e7-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a86e7-233">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="a86e7-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a86e7-234">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-235">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-236">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-237">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-238">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="a86e7-239">Resurs pripada organizacijskoj jedinici koja se razlikuje od ugovorne jedinice projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a86e7-240">Događaj</span><span class="sxs-lookup"><span data-stu-id="a86e7-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a86e7-241">Naplativi ili prodani projekt</span><span class="sxs-lookup"><span data-stu-id="a86e7-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a86e7-242">Projekt u fazi pretprodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a86e7-243">Interni projekt</span><span class="sxs-lookup"><span data-stu-id="a86e7-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a86e7-244">Vrijeme i materijali</span><span class="sxs-lookup"><span data-stu-id="a86e7-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a86e7-245">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a86e7-246">Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-246">Actuals</span></span></th>
<th><span data-ttu-id="a86e7-247">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="a86e7-247">Transaction currency</span></span></th>
<th><span data-ttu-id="a86e7-248">Fiksna cijena</span><span class="sxs-lookup"><span data-stu-id="a86e7-248">Fixed price</span></span></th>
<th><span data-ttu-id="a86e7-249">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="a86e7-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a86e7-250">Stvoren je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="a86e7-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a86e7-251">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-252">Poslan je unos vremena.</span><span class="sxs-lookup"><span data-stu-id="a86e7-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a86e7-253">Nema aktivnosti u entitetu Stvarne vrijednosti</span><span class="sxs-lookup"><span data-stu-id="a86e7-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a86e7-254">Vrijeme je odobreno i nema promjene ili povećanja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="a86e7-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a86e7-255">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-255">Cost actual</span></span></td>
<td><span data-ttu-id="a86e7-256">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a86e7-257">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a86e7-258">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a86e7-259">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a86e7-260">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-261">Stvarna vrijednost nenaplaćene prodaje – Naplativa</span><span class="sxs-lookup"><span data-stu-id="a86e7-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a86e7-262">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-263">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="a86e7-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a86e7-264">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-265">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a86e7-266">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a86e7-267">Vrijeme je odobreno i dolazi do smanjenja u naplativim satima tijekom odobravanja.</span><span class="sxs-lookup"><span data-stu-id="a86e7-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a86e7-268">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-268">Cost actual</span></span></td>
<td><span data-ttu-id="a86e7-269">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-270">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-271">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-272">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-273">Stvarna vrijednost troškova</span><span class="sxs-lookup"><span data-stu-id="a86e7-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-274">Jedinična cijena resursa</span><span class="sxs-lookup"><span data-stu-id="a86e7-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a86e7-275">Valuta resursne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-276">Međuorganizacijska prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a86e7-277">Valuta ugovorne jedinice</span><span class="sxs-lookup"><span data-stu-id="a86e7-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-278">Stvarna vrijednost nenaplaćene prodaje – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-279">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-280">Stvarna vrijednost nenaplaćene prodaje – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-281">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a86e7-282">Faktura je potvrđena i nema promjene ili povećanja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="a86e7-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a86e7-283">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a86e7-284">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-285">Naplaćena prodaja za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="a86e7-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-286">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-287">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a86e7-288">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-289">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-289">Billed sales</span></span></td>
<td><span data-ttu-id="a86e7-290">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a86e7-291">Faktura je potvrđena i dolazi do smanjenja u naplativim satima.</span><span class="sxs-lookup"><span data-stu-id="a86e7-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a86e7-292">Preokret nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="a86e7-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a86e7-293">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-294">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-295">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-296">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a86e7-297">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-298">Naplaćena prodaja – Naplativa za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-299">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-300">Naplaćena prodaja – Nenaplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-301">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a86e7-302">Faktura je ispravljena da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="a86e7-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a86e7-303">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="a86e7-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a86e7-304">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a86e7-305">Preokret naplaćene prodaje za ključnu točku</span><span class="sxs-lookup"><span data-stu-id="a86e7-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a86e7-306">Promjena statusa ključne točke iz <strong>Fakturirano</strong> u <strong>Spremno za fakturiranje</strong></span><span class="sxs-lookup"><span data-stu-id="a86e7-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a86e7-307">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-308">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a86e7-309">Nije primjenjivo</span><span class="sxs-lookup"><span data-stu-id="a86e7-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-310">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="a86e7-310">Billed sales</span></span></td>
<td><span data-ttu-id="a86e7-311">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a86e7-312">Faktura je ispravljena da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="a86e7-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a86e7-313">Naplaćena prodaja – Preokret</span><span class="sxs-lookup"><span data-stu-id="a86e7-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a86e7-314">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-315">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="a86e7-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a86e7-316">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a86e7-317">Nenaplaćena prodaja – Naplativa za razliku</span><span class="sxs-lookup"><span data-stu-id="a86e7-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a86e7-318">Valuta ugovora projekta</span><span class="sxs-lookup"><span data-stu-id="a86e7-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
