---
title: Potvrda predračuna
description: U ovoj temi nalaze se informacije o potvrđivanju predračuna u rješenju Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073296"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="d3f4f-103">Potvrda predračuna</span><span class="sxs-lookup"><span data-stu-id="d3f4f-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="d3f4f-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="d3f4f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d3f4f-105">Nakon potvrde predračuna status fakture za projekt ažurira se na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="d3f4f-106">Kad se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="d3f4f-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili dugovanja koje je pokrenuo klijent, ako je faktura označena kao plaćena.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="d3f4f-108">Sljedeća tablica navodi stvarne podatke koje je stvorio sustav.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="d3f4f-109">Ti se stvarni podaci stvaraju kada se izvrše određene radnje na nacrtu fakture za projekt prije nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="d3f4f-110">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d3f4f-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="d3f4f-111">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d3f4f-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-112">Fakturiranje predujma ili akontacije</span><span class="sxs-lookup"><span data-stu-id="d3f4f-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-113">Stvarni podatak o naplati prodaje vrste <strong>Akontacija</strong> stvara se za iznos predujma ili akontacije.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-114">Stvarni podatak o nenaplaćenoj prodaji negativnog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-115">Nakon potpunog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-116">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d3f4f-117">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-118">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d3f4f-119">Nakon djelomičnog usklađenja akontacije ili predujma na računu.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-120">Storniranje nenaplaćene prodaje akontacije ili predujma koji je stvoren za usklađivanje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="d3f4f-121">Ovaj je iznos pozitivan jer se želi poništiti negativan iznos stvoren pri fakturiranju akontacije ili predujma.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-122">Stvarni podatak o naplati prodaje za iznos na toj fakturi.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-123">Negativni stvarni podatak o nenaplaćenoj prodaji preostalog iznosa akontacije ili predujma, koji će se upotrebljavati za usklađivanje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-124">Fakturiranje transakcije vremena bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-125">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-126">Stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d3f4f-127">Fakturiranje transakcije vremena koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-128">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-129">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-130">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-131">Fakturiranje transakcije vremena koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-132">Storniranje nenaplaćene prodaje za sate i iznos na izvornom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-133">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-134">Fakturiranje transakcije troška bez ikakvih uređivanja nacrta fakture.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-135">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-136">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom odobrenju troška</span><span class="sxs-lookup"><span data-stu-id="d3f4f-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="d3f4f-137">Fakturiranje transakcije troška koja je uređena za smanjenje količine.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-138">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-139">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-140">Novi stvarni podatak o nenaplaćenoj prodaji koji se ne naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih brojki u pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-141">Fakturiranje transakcije troška koja je uređena za povećanje količine.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-142">Storniranje nenaplaćene prodaje za količinu i iznos na izvornom odobrenju troška.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-143">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za količinu i iznos za pojedinosti retka uređene fakture, storniranje stvarnog podatka o nenaplaćenoj prodaji i ekvivalent stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d3f4f-144">Fakturiranje naknade.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-145">Storniranje nenaplaćene prodaje za iznos naknade na izvornom retku dnevnika.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-146">Stvarni podatak naplaćene prodaje za količinu i iznos na izvornom retku dnevnika naknade.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d3f4f-147">Fakturiranje kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-148">Stvarni podatak naplaćene prodaje za iznos kontrolne točke na izvornoj kontrolnoj točki retka ugovora o projektu.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="d3f4f-149">Fakturiranje retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="d3f4f-150">Stvarni podatak naplaćene prodaje za redak proizvoda s količinom i iznosom koji dolaze iz retka ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="d3f4f-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
