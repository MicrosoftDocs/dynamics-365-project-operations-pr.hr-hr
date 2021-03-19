---
title: Potvrda predračuna – jednostavno
description: U ovoj temi nalaze se informacije o potvrđivanju predračuna u rješenju Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274269"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="dbd83-103">Potvrda predračuna – jednostavno</span><span class="sxs-lookup"><span data-stu-id="dbd83-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="dbd83-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="dbd83-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="dbd83-105">Nakon potvrde predračuna status fakture za projekt ažurira se na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="dbd83-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="dbd83-106">Kad se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="dbd83-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili dugovanja koje je pokrenuo klijent, ako je faktura označena kao plaćena.</span><span class="sxs-lookup"><span data-stu-id="dbd83-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="dbd83-108">Sljedeća tablica navodi stvarne podatke koje je stvorio sustav.</span><span class="sxs-lookup"><span data-stu-id="dbd83-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="dbd83-109">Ti se stvarni podaci stvaraju kada se izvrše određene radnje na nacrtu fakture za projekt prije nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="dbd83-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="dbd83-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dbd83-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="dbd83-111">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dbd83-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-112">Fakturiranje predujma ili akontacije</span><span class="sxs-lookup"><span data-stu-id="dbd83-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-113">Stvarni podatak o naplati prodaje vrste <strong>Akontacija</strong> stvara se za iznos predujma ili akontacije.</span><span class="sxs-lookup"><span data-stu-id="dbd83-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-114">Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-115">Nakon potpunog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="dbd83-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-116">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dbd83-117">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="dbd83-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-118">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="dbd83-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dbd83-119">Nakon djelomičnog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="dbd83-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-120">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dbd83-121">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="dbd83-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-122">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="dbd83-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-123">Negativni stvarni podatak o nenaplaćenoj prodaji preostalog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="dbd83-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-124">Fakturiranje transakcije vremena bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="dbd83-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-125">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="dbd83-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-126">Stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="dbd83-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dbd83-127">Fakturiranje transakcije vremena koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="dbd83-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-128">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="dbd83-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-129">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-130">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-131">Fakturiranje transakcije vremena koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="dbd83-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-132">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="dbd83-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-133">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-134">Fakturiranje transakcije troška bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="dbd83-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-135">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="dbd83-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-136">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom odobrenju troška</span><span class="sxs-lookup"><span data-stu-id="dbd83-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dbd83-137">Fakturiranje transakcije troška koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="dbd83-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-138">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="dbd83-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-139">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-140">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-141">Fakturiranje transakcije troška koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="dbd83-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-142">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="dbd83-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-143">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="dbd83-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dbd83-144">Fakturiranje naknade.</span><span class="sxs-lookup"><span data-stu-id="dbd83-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-145">Storniranje nenaplaćene prodaje za iznos naknade na izvornom retku dnevnika.</span><span class="sxs-lookup"><span data-stu-id="dbd83-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-146">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom retku dnevnika naknade.</span><span class="sxs-lookup"><span data-stu-id="dbd83-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dbd83-147">Fakturiranje kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="dbd83-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-148">Stvarni podatak naplaćene prodaje za iznos kontrolne točke na izvornoj kontrolnoj točki retka ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="dbd83-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dbd83-149">Fakturiranje retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="dbd83-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dbd83-150">Stvarni podatak naplaćene prodaje za redak proizvoda s količinom i iznosom koji dolaze iz retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="dbd83-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]