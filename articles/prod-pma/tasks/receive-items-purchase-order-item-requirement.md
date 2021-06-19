---
title: Primanje stavki na narudžbenicu iz zahtjeva za stavke
description: U ovoj se temi objašnjava način primanja stavki na narudžbenicu iz zahtjeva za stavkom.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011677"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="ac44b-103">Primanje stavki na narudžbenicu iz zahtjeva za stavke</span><span class="sxs-lookup"><span data-stu-id="ac44b-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac44b-104">U ovoj se temi objašnjava način primanja stavki na narudžbenicu iz zahtjeva za stavkom.</span><span class="sxs-lookup"><span data-stu-id="ac44b-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="ac44b-105">Uporabom zahtjeva za stavkom umjesto transakcije stavke, možete planirati isporuku neposredno prije stvarne uporabe stavke, stvoriti narudžbenicu, uključiti stavku u okvir trgovinskog sporazuma i uključiti zahtjev za stavkom u planiranje proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="ac44b-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="ac44b-106">Ovaj zadatak upotrebljava skup podataka USSI.</span><span class="sxs-lookup"><span data-stu-id="ac44b-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ac44b-107">U navigacijskom oknu idite na **Moduli > Upravljanje projektima i računovodstvo > Projekti > Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="ac44b-108">U odabranom retku na popisu odaberite vezu.</span><span class="sxs-lookup"><span data-stu-id="ac44b-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="ac44b-109">U Oknu radnji odaberite **Plan**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="ac44b-110">Odaberite **Zahtjevi za stavkom**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="ac44b-111">Odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-111">Select **New**.</span></span>
6. <span data-ttu-id="ac44b-112">U polje **Broj stavke** novog retka unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="ac44b-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="ac44b-113">U polje **Količina** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="ac44b-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="ac44b-114">Odaberite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-114">Select **Save**.</span></span>
9. <span data-ttu-id="ac44b-115">U Oknu radnji odaberite **Upravljaj**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="ac44b-116">Odaberite **Funkcije**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-116">Select **Functions**.</span></span>
11. <span data-ttu-id="ac44b-117">Odaberite **Stvori narudžbenicu**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="ac44b-118">Kliknite potvrdni okvir **Uključi sve**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="ac44b-119">U polje **Račun dobavljača** unesite ili u njemu odaberite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="ac44b-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="ac44b-120">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-120">Select **OK**.</span></span>
15. <span data-ttu-id="ac44b-121">U navigacijskom oknu idite na **Moduli > Dugovanja > Narudžbenice > Sve narudžbenice**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="ac44b-122">U odabranom retku na popisu odaberite vezu.</span><span class="sxs-lookup"><span data-stu-id="ac44b-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="ac44b-123">U Oknu radnji odaberite **Kupnja**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="ac44b-124">Odaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="ac44b-125">U Oknu radnji odaberite **Primanje**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="ac44b-126">Odaberite **Primitak proizvoda**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="ac44b-127">U polju **Primitak proizvoda** upišite vrijednost.</span><span class="sxs-lookup"><span data-stu-id="ac44b-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="ac44b-128">Odaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="ac44b-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]