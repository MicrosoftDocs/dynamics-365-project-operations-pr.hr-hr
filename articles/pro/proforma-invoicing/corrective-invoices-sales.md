---
title: Korektivne fakture za projekt
description: U ovoj temi nalaze se informacije o načinu stvaranja i potvrđivanja korektivnih faktura u aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004072"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="4d91b-103">Korektivne fakture za projekt</span><span class="sxs-lookup"><span data-stu-id="4d91b-103">Corrective project invoices</span></span>

<span data-ttu-id="4d91b-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="4d91b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d91b-105">Potvrđena faktura za projekt može se ispraviti kako bi se obradile promjene ili krediti prema dogovoru s klijentom i upraviteljem projekta.</span><span class="sxs-lookup"><span data-stu-id="4d91b-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="4d91b-106">Kako biste izvršili uređivanje potvrđene fakture, otvorite potvrđenu fakturu i odaberite **Ispravi ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="4d91b-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="4d91b-107">Ovaj odabir nije dostupan ako se faktura za projekt ne potvrdi.</span><span class="sxs-lookup"><span data-stu-id="4d91b-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="4d91b-108">Iz potvrđene fakture stvara se novi nacrt fakture.</span><span class="sxs-lookup"><span data-stu-id="4d91b-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="4d91b-109">Sve pojedinosti retka fakture iz prethodno potvrđene fakture kopiraju se u novi nacrt.</span><span class="sxs-lookup"><span data-stu-id="4d91b-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="4d91b-110">Slijede neke od ključnih točaka koje treba razumjeti o pojedinostima retka na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="4d91b-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="4d91b-111">Sve količine se ažuriraju na nulu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-111">All quantities are updated to zero.</span></span> <span data-ttu-id="4d91b-112">Aplikacija pretpostavlja da se sve fakturirane stavke u potpunosti duguju.</span><span class="sxs-lookup"><span data-stu-id="4d91b-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="4d91b-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturira, a ne količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="4d91b-114">Na temelju količine koju unesete, aplikacija izračunava količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="4d91b-115">Taj se iznos odražava u stvarnim podacima koji se stvaraju nakon potvrde ispravljene fakture.</span><span class="sxs-lookup"><span data-stu-id="4d91b-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="4d91b-116">Ako mijenjate iznos poreza, morate unijeti točan iznos poreza, a ne iznos poreza koji se duguje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="4d91b-117">Prethodno potvrđeni redci ugovora koji se temelje na proizvodu ne kopiraju se.</span><span class="sxs-lookup"><span data-stu-id="4d91b-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="4d91b-118">Obrada ispravaka na fakturi za projekt koja se temelji na proizvodu nije podržana.</span><span class="sxs-lookup"><span data-stu-id="4d91b-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="4d91b-119">Ispravci kontrolnih točaka uvijek se obrađuju kao puna dugovanja.</span><span class="sxs-lookup"><span data-stu-id="4d91b-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="4d91b-120">Iznos akontacije ili predujma može se ispraviti ako je klijentu fakturiran netočan iznos.</span><span class="sxs-lookup"><span data-stu-id="4d91b-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="4d91b-121">Usklađivanje iznosa akontacija i predujmova mogu se ispraviti ako se upotrebljavao netočan iznos za usklađivanje sa zaračunanim iznosima na prethodno potvrđenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="4d91b-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d91b-122">Pojedinosti retka fakture koje predstavljaju ispravke za ostale već fakturirane troškove imaju polje **Ispravak** postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="4d91b-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="4d91b-123">Fakture koje su ispravile pojedinosti retka fakture imaju polje koje se naziva **Ima ispravaka** koje je također postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="4d91b-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="4d91b-124">Stvarni podaci koji su stvoreni kada se potvrdi korektivna faktura</span><span class="sxs-lookup"><span data-stu-id="4d91b-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="4d91b-125">Tablica u nastavku navodi stvarne podatke koji se stvaraju nakon potvrde korektivne fakture.</span><span class="sxs-lookup"><span data-stu-id="4d91b-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="4d91b-126">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d91b-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="4d91b-127">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d91b-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4d91b-128">Potvrdite ispravak fakturiranog predujma ili akontacije.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="4d91b-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-129">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4d91b-130">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="4d91b-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-131">Stvarni podatak o storniranju naplaćene prodaje stvara se za iznos akontacije ili predujme za storniranje izvorno zaračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-132">Novi stvarni podatak o naplaćenoj prodaji stvara se za ispravljeni iznos na retku ispravljene fakture koji se temelji na akontaciji ili predujmu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-133">Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa retka fakture koji se temelji na akontaciji ili predujmu, koji će se upotrebljavati za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="4d91b-134">Potvrda ispravka prethodno usklađene akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="4d91b-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-135">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="4d91b-136">Ovaj je iznos pozitivan i namijenjen je poništenju negativnog iznosa stvorenog pri prethodnom usklađenju.</span><span class="sxs-lookup"><span data-stu-id="4d91b-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-137">Stvarni podatak o storniranoj naplati prodaje za iznos na prethodnoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="4d91b-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-138">Novi stvarni podatak o naplaćenoj prodaji za ispravljeni iznos akontacije koji se prikazuje na ispravljenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="4d91b-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-139">Stvarni podatak o nenaplaćenoj prodaji s negativnim iznosom ispravljenog ostatka akontacije ili predujma, koji će se upotrebljavati za usklađivanje u kasnijim fakturama.</span><span class="sxs-lookup"><span data-stu-id="4d91b-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4d91b-140">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije vremena.</span><span class="sxs-lookup"><span data-stu-id="4d91b-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-141">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="4d91b-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-142">Novi stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="4d91b-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4d91b-143">Fakturiranje djelomičnog duga za transakciju vremena.</span><span class="sxs-lookup"><span data-stu-id="4d91b-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-144">Storniranje naplaćene prodaje za sate i iznos fakturirane na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="4d91b-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-145">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-146">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="4d91b-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4d91b-147">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="4d91b-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-148">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="4d91b-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-149">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="4d91b-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4d91b-150">Fakturiranje djelomičnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="4d91b-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-151">Storniranje naplaćene prodaje za količinu i iznos naplaćen na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="4d91b-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-152">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinosti retka ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-153">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="4d91b-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4d91b-154">Fakturiranje punog kredita prethodno fakturirane transakcije materijala.</span><span class="sxs-lookup"><span data-stu-id="4d91b-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-155">Storniranje naplate prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="4d91b-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-156">Novi stvarni podatak o naplati prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="4d91b-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="4d91b-157">Fakturiranje djelomičnog kredita za transakciju materijala.</span><span class="sxs-lookup"><span data-stu-id="4d91b-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-158">Storniranje naplate prodaje za količinu i iznos fakturirane na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="4d91b-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-159">Novi stvarni podatak o nenaplaćenoj prodaji koji se može naplatiti za količinu i iznos na pojedinosti uređenog retka fakture, storniranje istog i ekvivalentni stvarni podatak o naplaćenoj prodaji.</span><span class="sxs-lookup"><span data-stu-id="4d91b-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-160">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="4d91b-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4d91b-161">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="4d91b-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-162">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-163">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4d91b-164">Fakturiranje djelomičnog duga iz prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="4d91b-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-165">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-166">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinost retka uređene ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="4d91b-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4d91b-167">Fakturiranje cjelokupnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="4d91b-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-168">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka za kontrolnu točku.</span><span class="sxs-lookup"><span data-stu-id="4d91b-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="4d91b-169">Stanje fakture kontrolne točke ažurira se sa <b>Faktura za klijenta proknjižena</b> na <b>Spremno za fakturiranje</b>.</span><span class="sxs-lookup"><span data-stu-id="4d91b-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4d91b-170">Fakturiranje djelomičnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="4d91b-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-171">Nije podržano</span><span class="sxs-lookup"><span data-stu-id="4d91b-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="4d91b-172">Dugovi i ispravci prethodno fakturiranog retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="4d91b-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="4d91b-173">Nije podržano</span><span class="sxs-lookup"><span data-stu-id="4d91b-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
