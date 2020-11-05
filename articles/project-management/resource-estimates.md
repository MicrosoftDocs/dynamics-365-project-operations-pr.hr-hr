---
title: Procjene resursa
description: U ovoj temi nalaze se informacije o načinu izračuna procjena resursa u aplikaciji Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073308"
---
# <a name="resource-estimates"></a><span data-ttu-id="5a3d6-103">Procjene resursa</span><span class="sxs-lookup"><span data-stu-id="5a3d6-103">Resource estimates</span></span>

<span data-ttu-id="5a3d6-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="5a3d6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a3d6-105">Procjene resursa potječu iz vremenski razrađenog rada koji je definiran u strukturnoj analizi rada zajedno s mjerodavnom dimenzijama cijena.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="5a3d6-106">Uobičajeno, izračun je **cijena/sat za svaku ulogu x sati**.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="5a3d6-107">Vremenski razrađeni rad za svaki resurs pohranjen je u zapisu o dodjeli resursa.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="5a3d6-108">Cijene su pohranjene u unaprijed definiranom cjeniku.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="5a3d6-109">Pretvaranje jedinice primjenjuje se na temelju mjerodavnog cjenika.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-109">Unit conversion is applied based on the applicable price list.</span></span>

![Procjene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="5a3d6-111">Zadana cijena koštanja i valuta troška</span><span class="sxs-lookup"><span data-stu-id="5a3d6-111">Default cost price and cost currency</span></span>

<span data-ttu-id="5a3d6-112">Cijene koštanja zadane su u Organizacijskoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="5a3d6-113">Zadane cijena naplate i valute prodaje</span><span class="sxs-lookup"><span data-stu-id="5a3d6-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="5a3d6-114">Prodajne cijene primjenjuju se za jedan posao.</span><span class="sxs-lookup"><span data-stu-id="5a3d6-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="5a3d6-115">Hijerarhija prodajnog cjenika prema zadanim postavkama je sljedeća:</span><span class="sxs-lookup"><span data-stu-id="5a3d6-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="5a3d6-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="5a3d6-116">Organization</span></span>
2. <span data-ttu-id="5a3d6-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="5a3d6-117">Customer</span></span>
3. <span data-ttu-id="5a3d6-118">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="5a3d6-118">Quote/contract</span></span>
