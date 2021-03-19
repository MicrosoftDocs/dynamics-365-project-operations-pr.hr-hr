---
title: Jedinice i grupe jedinica
description: U ovoj temi nalaze se informacije o načinu stvaranja jedinica i grupa jedinica u aplikaciji Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 162366f4b7aa678b4e39d9745a657037bf36cbe0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277329"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="ae5e1-103">Jedinice i grupe jedinica</span><span class="sxs-lookup"><span data-stu-id="ae5e1-103">Units and unit groups</span></span>

<span data-ttu-id="ae5e1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="ae5e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae5e1-105">Jedinice su količine ili mjerne jedinice u kojima prodajete proizvode ili servise.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="ae5e1-106">Na primjer, ako prodajete proizvode za vrtlarenje, možda prodajete sjemenje u jedinicama paketa, kutija i paleta.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="ae5e1-107">Grupa jedinica je skup tih različitih jedinica.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="ae5e1-108">Kako biste dovršili korake iz ove teme, provjerite jeste li dodijeljeni ulozi administratora sustava ili voditelja Sales Professional ili imate jednake dozvole.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="ae5e1-109">Stvaranje grupe jedinica</span><span class="sxs-lookup"><span data-stu-id="ae5e1-109">Create a unit group</span></span>

1. <span data-ttu-id="ae5e1-110">U karti web-mjesta odaberite mogućnost **Jedinice**.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="ae5e1-111">Odaberite **Novo** i u dijaloški okvir **Stvori grupu jedinica** unesite naziv jedinice.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="ae5e1-112">U polje **Primarna jedinica** unesite najmanju uobičajenu mjernu jedinicu u kojoj se proizvod prodaje.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="ae5e1-113">Na primjer, možete unijeti „komad” ili „unca”.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="ae5e1-114">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="ae5e1-115">Dodavanje jedinica grupi</span><span class="sxs-lookup"><span data-stu-id="ae5e1-115">Add units to a unit group</span></span>

1. <span data-ttu-id="ae5e1-116">Otvorite grupu jedinica i na kartici **Povezano** odaberite **Jedinice**.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="ae5e1-117">Vidjet ćete kako je primarna jedinica već dodana.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="ae5e1-118">Odaberite **Dodaj novu jedinicu** i na stranici **Brzo stvaranje: Jedinica**, u polje **Naziv**, unesite naziv jedinice.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="ae5e1-119">U polje **Količina** unesite količinu koju će jedinica sadržavati.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="ae5e1-120">Na primjer, ako kutija sadrži dva komada, unesite „2”.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="ae5e1-121">U polju **Osnovna jedinica** odaberite osnovnu jedinicu kako biste za jedinicu postavili najnižu mjernu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="ae5e1-122">Na primjer, možete odabrati „Komad”.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="ae5e1-123">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="ae5e1-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]