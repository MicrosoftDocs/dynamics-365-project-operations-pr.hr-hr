---
title: Potvrda predračuna za projekt
description: U ovoj temi nalaze se informacije o potvrđivanju predračuna za projekt u aplikaciji Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004117"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="5aa8c-103">Potvrda predračuna za projekt</span><span class="sxs-lookup"><span data-stu-id="5aa8c-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="5aa8c-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="5aa8c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5aa8c-105">Nakon potvrde predračuna status fakture za projekt ažurira se na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="5aa8c-106">Kad se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="5aa8c-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijent.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="5aa8c-108">Sljedeća tablica navodi stvarne podatke koje je stvorio sustav.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="5aa8c-109">Ti se stvarni podaci stvaraju kada se izvrše određene radnje na nacrtu fakture za projekt prije nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="5aa8c-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5aa8c-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="5aa8c-111">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5aa8c-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-112">Fakturiranje predujma ili akontacije</span><span class="sxs-lookup"><span data-stu-id="5aa8c-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-113">Stvarni podatak o naplati prodaje vrste <strong>Akontacija</strong> stvara se za iznos predujma ili akontacije.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-114">Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-115">Nakon potpunog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-116">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5aa8c-117">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-118">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5aa8c-119">Nakon djelomičnog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-120">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5aa8c-121">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-122">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-123">Negativni stvarni podatak o nenaplaćenoj prodaji preostalog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-124">Fakturiranje transakcije vremena bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-125">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-126">Stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5aa8c-127">Fakturiranje transakcije vremena koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-128">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-129">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-130">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-131">Fakturiranje transakcije vremena koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-132">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-133">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-134">Fakturiranje transakcije troška bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-135">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-136">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom odobrenju troška</span><span class="sxs-lookup"><span data-stu-id="5aa8c-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5aa8c-137">Fakturiranje transakcije troška koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-138">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-139">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-140">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-141">Fakturiranje transakcije troška koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-142">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-143">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-144">Fakturiranje transakcije materijala bez ikakvih izmjena na skici fakture.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-145">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za utrošeni materijal.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-146">Naplaćena stvarna prodaja za količinu i iznos na originalnom odobrenju za utrošeni materijal.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5aa8c-147">Fakturiranje transakcije materijala koja je uređena kako bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-148">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-149">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-150">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-151">Fakturiranje transakcije materijala koja je uređena kako bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-152">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za utrošeni materijal.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-153">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5aa8c-154">Fakturiranje naknade.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-155">Storniranje nenaplaćene prodaje za iznos naknade na izvornom retku dnevnika.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-156">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom retku dnevnika naknade.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5aa8c-157">Fakturiranje kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-158">Stvarni podatak naplaćene prodaje za iznos kontrolne točke na izvornoj kontrolnoj točki retka ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5aa8c-159">Fakturiranje retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5aa8c-160">Stvarni podatak naplaćene prodaje za redak proizvoda s količinom i iznosom koji dolaze iz retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="5aa8c-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
