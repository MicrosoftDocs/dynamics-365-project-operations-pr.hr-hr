---
title: Cjenici proizvoda
description: U ovoj se temi nalaze informacije o cjenicima u određivanju kataloških cijena koje se upotrebljavaju u ponudama za projekt i ugovore o projektu.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877481"
---
# <a name="product-price-lists"></a><span data-ttu-id="8e03c-103">Cjenici proizvoda</span><span class="sxs-lookup"><span data-stu-id="8e03c-103">Product price lists</span></span>

<span data-ttu-id="8e03c-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="8e03c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="8e03c-105">**Cjenici proizvoda** u aplikaciji Project Operations i povezani entiteti stavke cjenika podržavaju funkcionalnost za određivanje cijena proizvoda na ponudama i redcima ugovora koji se temelje na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="8e03c-106">Za proizvode koji se upotrebljavaju na projektima upotrebljavaju se zapisi stavki cjenika za cjenike projekata.</span><span class="sxs-lookup"><span data-stu-id="8e03c-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="8e03c-107">Proizvodi se trebaju postaviti tako da sadrže zadani trošak i cjenike u katalogu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="8e03c-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="8e03c-108">Upotrebljavajte kataloške cijena, standardni trošak i trenutačni trošak kako biste konfigurirali zadani trošak i kataloških cijena.</span><span class="sxs-lookup"><span data-stu-id="8e03c-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="8e03c-109">Zadane kataloške cijene koriste se u retku ponude ili u retku ugovora o projektu samo ako sustav ne može pronaći redak cjenika za taj proizvod u cjeniku proizvoda za ponudu ili ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="8e03c-110">Cijena koštanja redaka kataloga proizvoda može se promijeniti između ponuda.</span><span class="sxs-lookup"><span data-stu-id="8e03c-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="8e03c-111">Ta je mogućnost važna jer ako ne pratite precizno troškove, ne možete odrediti operativnu dobit u projektnim angažmanima.</span><span class="sxs-lookup"><span data-stu-id="8e03c-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="8e03c-112">Prema zadanim postavkama standardna cijena proizvoda upotrebljava se kao cijena koštanja.</span><span class="sxs-lookup"><span data-stu-id="8e03c-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="8e03c-113">Međutim, zadana cijena koštanja može se ažurirati u retku ponude ako postoji drugačija cijena koštanja za tu ponudu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="8e03c-114">Stavke cjenika</span><span class="sxs-lookup"><span data-stu-id="8e03c-114">Price list items</span></span>

<span data-ttu-id="8e03c-115">Proizvode iz kataloga proizvoda možete dodavati na različite cjenike.</span><span class="sxs-lookup"><span data-stu-id="8e03c-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="8e03c-116">Reci cjenika za proizvode uvijek upućuju na određenu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="8e03c-117">Cijena za proizvod u stavkama cjenika može se konfigurirati kao iznos valute.</span><span class="sxs-lookup"><span data-stu-id="8e03c-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="8e03c-118">Ili se može konfigurirati kao funkcija kataloške cijene, trenutačnog troška ili standardnog troška.</span><span class="sxs-lookup"><span data-stu-id="8e03c-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="8e03c-119">Funkcionalnost određivanja cijena podržava različite mogućnosti zaokruživanja kada su cijene proizvoda konfigurirane kao funkcija kataloške cijene, standardnog ili trenutačnog troška.</span><span class="sxs-lookup"><span data-stu-id="8e03c-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="8e03c-120">Uz iskorištavanje prednosti više načina određivanja cijena i mogućnosti zaokruživanja, popise popusta možete povezati sa stavkama cjenika.</span><span class="sxs-lookup"><span data-stu-id="8e03c-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="8e03c-121">Zadani cjenik proizvoda</span><span class="sxs-lookup"><span data-stu-id="8e03c-121">Default product price list</span></span>
<span data-ttu-id="8e03c-122">Svaki zapis klijenta sadrži polje **Zadani cjenik**, gdje možete navesti cjenik koji odgovara valuti klijenta.</span><span class="sxs-lookup"><span data-stu-id="8e03c-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="8e03c-123">Zadana vrijednost ne unosi se automatski u ovo polje.</span><span class="sxs-lookup"><span data-stu-id="8e03c-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="8e03c-124">Kada postoji prilagođeni ugovor o određivanju cijena s određenim klijentom, ovo polje možete koristiti za povezivanje cjenika s tim klijentom.</span><span class="sxs-lookup"><span data-stu-id="8e03c-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="8e03c-125">Entiteti Prilika, Ponuda i Ugovor o projektu koriste sljedeću ponudu za unos zadanih cjenika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="8e03c-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="8e03c-126">Ista ponuda upotrebljava se za cjenike za projekt.</span><span class="sxs-lookup"><span data-stu-id="8e03c-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="8e03c-127">Ponuda</span><span class="sxs-lookup"><span data-stu-id="8e03c-127">Quote</span></span>
2.  <span data-ttu-id="8e03c-128">Prilika</span><span class="sxs-lookup"><span data-stu-id="8e03c-128">Opportunity</span></span>
3.  <span data-ttu-id="8e03c-129">Klijent</span><span class="sxs-lookup"><span data-stu-id="8e03c-129">Customer</span></span>
4.  <span data-ttu-id="8e03c-130">Globalne postavke</span><span class="sxs-lookup"><span data-stu-id="8e03c-130">Global settings</span></span> 

<span data-ttu-id="8e03c-131">Prema zadanim postavkama polje **Proizvod** u retku ponude popisuje sve aktivne proizvode u cjeniku proizvoda ponude.</span><span class="sxs-lookup"><span data-stu-id="8e03c-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="8e03c-132">Ako je proizvod neaktivan ili je skica proizvoda, ne navodi se na popisu, čak i ako je naveden u cjeniku.</span><span class="sxs-lookup"><span data-stu-id="8e03c-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="8e03c-133">Reci kataloga proizvoda dodaju se kao reci fakture u prvoj fakturi koja se izrađuje za ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="8e03c-134">U skici fakture ti se reci fakture mogu izbrisati.</span><span class="sxs-lookup"><span data-stu-id="8e03c-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="8e03c-135">U tom će se slučaju reci prikazati u sljedećoj fakturi dok se ne fakturiraju ili dok se faktura ne pošalje klijentu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="8e03c-136">Ne možete fakturirati djelomičnu količinu retka fakture za proizvod.</span><span class="sxs-lookup"><span data-stu-id="8e03c-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="8e03c-137">Kada se reci proizvoda iz ugovora o projektu fakturiraju, izrađuju se stvarni podaci.</span><span class="sxs-lookup"><span data-stu-id="8e03c-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="8e03c-138">Međutim, ti stvarni podaci ne povezuju se s povezanim entitetom projekta.</span><span class="sxs-lookup"><span data-stu-id="8e03c-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="8e03c-139">Drugim riječima, reci projekta temeljeni na proizvodu neovisni su o bilo kakvoj upotrebi temeljenoj na projektu.</span><span class="sxs-lookup"><span data-stu-id="8e03c-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
