---
title: Procjene resursa
description: U ovoj temi nalaze se informacije o načinu izračuna procjena resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286509"
---
# <a name="resource-estimates"></a><span data-ttu-id="d2b87-103">Procjene resursa</span><span class="sxs-lookup"><span data-stu-id="d2b87-103">Resource estimates</span></span>

<span data-ttu-id="d2b87-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="d2b87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d2b87-105">Procjene resursa potječu iz vremenski razrađenog rada koji je definiran u strukturnoj analizi rada zajedno s mjerodavnom dimenzijama cijena.</span><span class="sxs-lookup"><span data-stu-id="d2b87-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="d2b87-106">Uobičajeno, izračun je **cijena/sat za svaku ulogu x sati**.</span><span class="sxs-lookup"><span data-stu-id="d2b87-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="d2b87-107">Vremenski razrađeni rad za svaki resurs pohranjen je u zapisu o dodjeli resursa.</span><span class="sxs-lookup"><span data-stu-id="d2b87-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="d2b87-108">Cijene su pohranjene u unaprijed definiranom cjeniku.</span><span class="sxs-lookup"><span data-stu-id="d2b87-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="d2b87-109">Pretvaranje jedinice primjenjuje se na temelju mjerodavnog cjenika.</span><span class="sxs-lookup"><span data-stu-id="d2b87-109">Unit conversion is applied based on the applicable price list.</span></span>

![Procjene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="d2b87-111">Zadana cijena koštanja i valuta troška</span><span class="sxs-lookup"><span data-stu-id="d2b87-111">Default cost price and cost currency</span></span>

<span data-ttu-id="d2b87-112">Cijene koštanja zadane su u Organizacijskoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="d2b87-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="d2b87-113">Zadane cijena naplate i valute prodaje</span><span class="sxs-lookup"><span data-stu-id="d2b87-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="d2b87-114">Prodajne cijene primjenjuju se za jedan posao.</span><span class="sxs-lookup"><span data-stu-id="d2b87-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="d2b87-115">Hijerarhija prodajnog cjenika prema zadanim postavkama je sljedeća:</span><span class="sxs-lookup"><span data-stu-id="d2b87-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="d2b87-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="d2b87-116">Organization</span></span>
2. <span data-ttu-id="d2b87-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="d2b87-117">Customer</span></span>
3. <span data-ttu-id="d2b87-118">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="d2b87-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]