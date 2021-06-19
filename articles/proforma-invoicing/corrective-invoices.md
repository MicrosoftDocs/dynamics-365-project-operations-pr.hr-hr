---
title: Korektivne fakture koje se temelje na projektu
description: U ovoj temi nalaze se informacije o načinu stvaranja i potvrđivanja korektivnih faktura koje se temelje na projektu u aplikaciji Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012262"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="ef7d8-103">Korektivne fakture koje se temelje na projektu</span><span class="sxs-lookup"><span data-stu-id="ef7d8-103">Corrective project-based invoices</span></span>

<span data-ttu-id="ef7d8-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ef7d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ef7d8-105">Potvrđena faktura za projekt može se ispraviti kako bi se obradile promjene ili krediti prema dogovoru s klijentom i upraviteljem projekta.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="ef7d8-106">Kako biste izvršili uređivanje potvrđene fakture, otvorite potvrđenu fakturu i odaberite **Ispravi ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ef7d8-107">Ovaj odabir nije dostupan osim ako je faktura projekta potvrđena ili ako faktura koja se temelji na projektu sadrži predujmove ili akontacije tj. usklađivanje predujmova ili akontacija.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="ef7d8-108">Iz potvrđene fakture stvara se novi nacrt fakture.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="ef7d8-109">Sve pojedinosti retka fakture iz prethodno potvrđene fakture kopiraju se u novi nacrt.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="ef7d8-110">Slijede neke od ključnih točaka koje treba razumjeti o pojedinostima retka na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="ef7d8-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="ef7d8-111">Sve količine se ažuriraju na nulu.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-111">All quantities are updated to zero.</span></span> <span data-ttu-id="ef7d8-112">Dynamics 365 Project Operations pretpostavlja da su sve fakturirane stavke u cijelosti knjižene u korist.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="ef7d8-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturira, a ne količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="ef7d8-114">Na temelju količine koju unesete, aplikacija izračunava količinu koja se duguje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="ef7d8-115">Taj se iznos odražava u stvarnim podacima koji se stvaraju nakon potvrde ispravljene fakture.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="ef7d8-116">Ako mijenjate iznos poreza, morate unijeti točan iznos poreza, a ne iznos poreza koji se duguje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="ef7d8-117">Ispravci kontrolnih točaka uvijek se obrađuju kao puna dugovanja.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="ef7d8-118">Za pojedinosti retka fakture koje su ispravci za druge već fakturirane troškove, polje **Ispravak** postavljeno je na **Da**.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="ef7d8-119">Za pojedinosti koje imaju ispravljene pojedinosti retka fakture, polje **Ima ispravke** postavljeno je na **Da**.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="ef7d8-120">Stvarni podaci koji su stvoreni kada se potvrdi korektivna faktura</span><span class="sxs-lookup"><span data-stu-id="ef7d8-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="ef7d8-121">Tablica u nastavku navodi stvarne podatke koji se stvaraju nakon potvrde korektivne fakture.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ef7d8-122">
                    <strong>Scenarij</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef7d8-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ef7d8-123">
                    <strong>Stvarni podaci stvoreni potvrdom</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ef7d8-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ef7d8-124">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije vremena.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-125">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-126">Novi stvarni podatak o naplaćenoj prodaji za sate i iznos na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ef7d8-127">Fakturiranje djelomičnog duga za transakciju vremena.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-128">Storniranje naplaćene prodaje za sate i iznos fakturirane na izvornoj pojedinosti retka fakture za vrijeme.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-129">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za sate i iznos za pojedinosti retka uređene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-130">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ef7d8-131">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-132">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-133">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ef7d8-134">Fakturiranje djelomičnog duga prethodno fakturirane transakcije troška.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-135">Storniranje naplaćene prodaje za količinu i iznos naplaćen na izvornoj pojedinosti retka fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-136">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinosti retka ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-137">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ef7d8-138">Fakturiranje punog kredita prethodno fakturirane transakcije materijala.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-139">Storniranje naplate prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-140">Novi stvarni podatak o naplati prodaje za količinu i iznos na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ef7d8-141">Fakturiranje djelomičnog kredita za transakciju materijala.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-142">Storniranje naplate prodaje za količinu i iznos fakturirane na originalnoj pojedinosti retka fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-143">Novi stvarni podatak o nenaplaćenoj prodaji koji se može naplatiti za količinu i iznos na pojedinosti uređenog retka fakture, storniranje istog i ekvivalentni stvarni podatak o naplaćenoj prodaji.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-144">Novi stvarni podatak o nenaplaćenoj prodaji koji se naplaćuje za preostalu količinu i iznos nakon odbijanja ispravljenih podataka u pojedinosti retka računa.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ef7d8-145">Fakturiranje cjelokupnog duga prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-146">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-147">Novi stvarni podatak o nenaplaćenoj prodaji za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ef7d8-148">Fakturiranje djelomičnog duga iz prethodno fakturirane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-149">Storniranje naplaćene prodaje za količinu i iznos fakturirane na izvornoj pojedinosti retka fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-150">Novi stvarni podatak o nenaplaćenoj prodaji koja se naplaćuje za količinu i iznos za pojedinost retka uređene ispravljene fakture, storniranje istog i ekvivalentna stvarnom podatku naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ef7d8-151">Fakturiranje cjelokupnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-152">Storniranje naplaćene prodaje za sate i iznos na izvornoj pojedinosti retka za kontrolnu točku.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="ef7d8-153">Stanje fakture kontrolne točke ažurira se sa <b>Faktura za klijenta proknjižena</b> na <b>Spremno za fakturiranje</b>.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ef7d8-154">Fakturiranje djelomičnog duga prethodno fakturirane kontrolne točke.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ef7d8-155">Ovaj scenarij nije podržan.</span><span class="sxs-lookup"><span data-stu-id="ef7d8-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
