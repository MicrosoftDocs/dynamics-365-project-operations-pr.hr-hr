---
title: Stvaranje korektivnih faktura koje se temelje na projektu
description: U ovoj temi nalaze se informacije o korektivnim fakturama u aplikaciji Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788840"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="730fd-103">Stvaranje korektivnih faktura koje se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="730fd-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="730fd-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="730fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="730fd-105">Potvrđena faktura za projekt može se ispraviti kako bi se obradile promjene ili krediti prema dogovoru s klijentom i upraviteljem projekta.</span><span class="sxs-lookup"><span data-stu-id="730fd-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="730fd-106">Kako biste izvršili uređivanje potvrđene fakture, otvorite potvrđenu fakturu i odaberite **Ispravi ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="730fd-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="730fd-107">Ovaj odabir nije dostupan ako se faktura za projekt ne potvrdi.</span><span class="sxs-lookup"><span data-stu-id="730fd-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="730fd-108">Iz potvrđene fakture stvara se novi nacrt fakture.</span><span class="sxs-lookup"><span data-stu-id="730fd-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="730fd-109">Sve pojedinosti retka fakture iz prethodno potvrđene fakture kopiraju se u novi nacrt.</span><span class="sxs-lookup"><span data-stu-id="730fd-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="730fd-110">Slijede neke ključne točke koje će vam pomoći da shvatite više o pojedinostima retka na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="730fd-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="730fd-111">Sve količine se ažuriraju na nulu.</span><span class="sxs-lookup"><span data-stu-id="730fd-111">All quantities are updated to zero.</span></span> <span data-ttu-id="730fd-112">To pretpostavlja da su sve fakturirane stavke u cijelosti knjižene u korist.</span><span class="sxs-lookup"><span data-stu-id="730fd-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="730fd-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturira, a ne količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="730fd-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="730fd-114">Na temelju količine koju unesete, aplikacija izračunava količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="730fd-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="730fd-115">Taj se iznos odražava u stvarnim podacima koji se stvaraju nakon potvrde ispravljene fakture.</span><span class="sxs-lookup"><span data-stu-id="730fd-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="730fd-116">Ako mijenjate iznos poreza, morate unijeti točan iznos poreza, a ne iznos poreza koji se duguje.</span><span class="sxs-lookup"><span data-stu-id="730fd-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="730fd-117">Ispravci kontrolnih točaka uvijek se obrađuju kao puna dugovanja.</span><span class="sxs-lookup"><span data-stu-id="730fd-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="730fd-118">Iznos akontacije ili predujma može se ispraviti ako je klijentu fakturiran netočan iznos.</span><span class="sxs-lookup"><span data-stu-id="730fd-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="730fd-119">Usklađivanje iznosa akontacija i predujmova mogu se ispraviti ako se upotrebljavao netočan iznos za usklađivanje sa zaračunanim iznosima na prethodno potvrđenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="730fd-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="730fd-120">Pojedinosti retka fakture koje su ispravci za druge već fakturirane troškove imaju polje **Ispravak** postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="730fd-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="730fd-121">Fakture koje su ispravile pojedinosti retka fakture imaju polje koje se naziva **Ima ispravaka** koje je također postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="730fd-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="730fd-122">Stvarni podaci stvoreni na potvrdi korektivne fakture</span><span class="sxs-lookup"><span data-stu-id="730fd-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="730fd-123">Tablica u nastavku navodi stvarne podatke koji se stvaraju nakon potvrde korektivne fakture.</span><span class="sxs-lookup"><span data-stu-id="730fd-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="730fd-124">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="730fd-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="730fd-125">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="730fd-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="730fd-126">Potvrdite ispravak fakturiranog predujma ili akontacije.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="730fd-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-127">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="730fd-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="730fd-128">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="730fd-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-129">Stvarni podatak o storniranju naplaćene prodaje stvara se za iznos akontacije ili predujme za storniranje izvorno zaračunane prodaje.</span><span class="sxs-lookup"><span data-stu-id="730fd-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-130">Novi stvarni podatak o naplaćenoj prodaji stvara se za ispravljeni iznos na retku ispravljene fakture koji se temelji na akontaciji ili predujmu.</span><span class="sxs-lookup"><span data-stu-id="730fd-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-131">Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa retka fakture koji se temelji na akontaciji ili predujmu, koji će se upotrebljavati za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="730fd-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="730fd-132">Potvrda ispravka prethodno usklađene akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="730fd-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-133">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="730fd-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="730fd-134">Ovaj je iznos pozitivan i namijenjen je poništenju negativnog iznosa stvorenog pri prethodnom usklađenju.</span><span class="sxs-lookup"><span data-stu-id="730fd-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-135">Stvarni podatak o storniranoj naplati prodaje za iznos na prethodnoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="730fd-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-136">Novi stvarni podatak o naplaćenoj prodaji za ispravljeni iznos akontacije koji se prikazuje na ispravljenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="730fd-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-137">Stvarni podatak o nenaplaćenoj prodaji s negativnim iznosom ispravljenog ostatka akontacije ili predujma, koji će se upotrebljavati za usklađivanje u kasnijim fakturama.</span><span class="sxs-lookup"><span data-stu-id="730fd-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="730fd-138">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije vremena.</span><span class="sxs-lookup"><span data-stu-id="730fd-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-139">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="730fd-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-140">Novi stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="730fd-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="730fd-141">Fakturiranje djelomičnog duga za transakciju vremena.</span><span class="sxs-lookup"><span data-stu-id="730fd-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-142">Storniranje naplaćene prodaje za sate i iznos fakturirane na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="730fd-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-143">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="730fd-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-144">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="730fd-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="730fd-145">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="730fd-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-146">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="730fd-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-147">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="730fd-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="730fd-148">Fakturiranje djelomičnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="730fd-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-149">Storniranje naplaćene prodaje za količinu i iznos naplaćen na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="730fd-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-150">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinosti retka ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="730fd-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-151">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="730fd-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="730fd-152">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="730fd-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-153">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="730fd-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-154">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="730fd-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="730fd-155">Fakturiranje djelomičnog duga iz prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="730fd-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-156">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="730fd-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-157">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinost retka uređene ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="730fd-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="730fd-158">Fakturiranje cjelokupnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="730fd-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-159">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka za kontrolnu točku.</span><span class="sxs-lookup"><span data-stu-id="730fd-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="730fd-160">Stanje fakture na kontrolnoj točki ažurira se sa <b>Faktura za klijenta proknjižena</b> na <b>Spremno za fakturiranje</b>.</span><span class="sxs-lookup"><span data-stu-id="730fd-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="730fd-161">Fakturiranje djelomičnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="730fd-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="730fd-162">Nije podržano</span><span class="sxs-lookup"><span data-stu-id="730fd-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
