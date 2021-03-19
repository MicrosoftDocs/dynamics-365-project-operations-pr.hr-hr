---
title: Narudžbenice za projekte
description: U ovom se članku opisuju različite metode koje možete upotrebljavati za stvaranje narudžbenica za projekt. Način koji upotrebljavate ovisi o svrsi narudžbenice i vremenu kada su kupljene stavke utrošene u projektu i naplaćene.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289180"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="867b0-104">Narudžbenice za projekte</span><span class="sxs-lookup"><span data-stu-id="867b0-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="867b0-105">U ovom se članku opisuju različite metode koje možete upotrebljavati za stvaranje narudžbenica za projekt.</span><span class="sxs-lookup"><span data-stu-id="867b0-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="867b0-106">Način koji upotrebljavate ovisi o svrsi narudžbenice i vremenu kada su kupljene stavke utrošene u projektu i naplaćene.</span><span class="sxs-lookup"><span data-stu-id="867b0-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="867b0-107">Načini stvaranja narudžbenice</span><span class="sxs-lookup"><span data-stu-id="867b0-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="867b0-108">Za stvaranje narudžbenice u Upravljanju projektima i računovodstvu možete upotrijebiti jednu od sljedećih metoda.</span><span class="sxs-lookup"><span data-stu-id="867b0-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="867b0-109">Svrha narudžbenice određuje kada se narudžbenica troši i, prema tome, kada se stavke naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="867b0-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="867b0-110">Način</span><span class="sxs-lookup"><span data-stu-id="867b0-110">Method</span></span></th>
<th><span data-ttu-id="867b0-111">Svrha</span><span class="sxs-lookup"><span data-stu-id="867b0-111">Purpose</span></span></th>
<th><span data-ttu-id="867b0-112">Potrošnja stavki</span><span class="sxs-lookup"><span data-stu-id="867b0-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="867b0-113">Stvorite narudžbenicu izravno iz projekta.</span><span class="sxs-lookup"><span data-stu-id="867b0-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="867b0-114">Ovaj način upotrebljavajte kako biste stavke koje se troše na projektu kupili od vanjskog dobavljača.</span><span class="sxs-lookup"><span data-stu-id="867b0-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="867b0-115">Narudžbenicu možete stvoriti na dva načina:</span><span class="sxs-lookup"><span data-stu-id="867b0-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="867b0-116">Iz samog projekta.</span><span class="sxs-lookup"><span data-stu-id="867b0-116">From the project itself.</span></span> <span data-ttu-id="867b0-117">U tom je slučaju projekt već definiran za narudžbenicu.</span><span class="sxs-lookup"><span data-stu-id="867b0-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="867b0-118">Pomicanjem do narudžbenice za projekt.</span><span class="sxs-lookup"><span data-stu-id="867b0-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="867b0-119">Morate odabrati dobavljača i projekt za koji ćete stvoriti narudžbenicu.</span><span class="sxs-lookup"><span data-stu-id="867b0-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="867b0-120">Stavke se troše kada se ažurira faktura dobavljača.</span><span class="sxs-lookup"><span data-stu-id="867b0-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="867b0-121">Stvorite narudžbenicu izravno iz prodajnog naloga.</span><span class="sxs-lookup"><span data-stu-id="867b0-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="867b0-122">Ovaj način upotrijebite kako biste stavke kupili kada iz projekta stvorite prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="867b0-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="867b0-123">Stavke se troše kad se klijentu fakturira prodajni nalog.</span><span class="sxs-lookup"><span data-stu-id="867b0-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="867b0-124">Stvorite narudžbenicu iz zahtjeva za stavkom.</span><span class="sxs-lookup"><span data-stu-id="867b0-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="867b0-125">Ovaj način upotrijebite kako biste stavke kupili kada iz projekta stvorite zahtjev za stavkom.</span><span class="sxs-lookup"><span data-stu-id="867b0-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="867b0-126">Stavke se troše kada se ažurira otpremnica zahtjeva za stavkom.</span><span class="sxs-lookup"><span data-stu-id="867b0-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="867b0-127">Kada ažurirate fakturu dobavljača ili otpremnicu, od vas će se zatražiti da ažurirate otpremnicu na zahtjevu za stavku.</span><span class="sxs-lookup"><span data-stu-id="867b0-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="867b0-128">Dodatne informacija potražite u odjeljku [Primanje stavki na narudžbenicu iz zahtjeva za stavkom](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="867b0-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]