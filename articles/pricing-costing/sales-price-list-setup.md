---
title: Postavljanje prodajnog cjenika
description: U ovoj temi nalaze se informacije o prodajnim cjenicima za određivanje cijena za projekte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073443"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="a3675-103">Postavljanje prodajnog cjenika</span><span class="sxs-lookup"><span data-stu-id="a3675-103">Sales price list setup</span></span>

<span data-ttu-id="a3675-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="a3675-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3675-105">Za ponude i ugovore projekta, cjenik projekta ima različit uzorak otpisa cijena od cjenika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="a3675-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="a3675-106">U retku ponude koji se temelji na katalogu proizvoda možete otpisati cijenu za uloge i kategorije izravno u retku ponude jer svaki redak ponude upućuje na točno jednu stavku kataloga.</span><span class="sxs-lookup"><span data-stu-id="a3675-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="a3675-107">Međutim, u retku ponude koji se temelji na projektu ne možete otpisati cijenu za uloge i kategorije izravno u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="a3675-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="a3675-108">Možete upotrijebiti cjenik za projekt kako biste radili s dva različita uzorka za zamjenu.</span><span class="sxs-lookup"><span data-stu-id="a3675-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="a3675-109">Preporučujemo da imate zaseban cjenik za svoje projektne resurse i artikle kataloga zbog razlika u ponašanju između njih kada otpisujete cijene.</span><span class="sxs-lookup"><span data-stu-id="a3675-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="a3675-110">Svaki od sljedećih entiteta može imati jedan ili više pridruženih prodajnih cjenika za određivanje cijena projekta:</span><span class="sxs-lookup"><span data-stu-id="a3675-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="a3675-111">Klijent (račun)</span><span class="sxs-lookup"><span data-stu-id="a3675-111">Customer (account)</span></span> 
- <span data-ttu-id="a3675-112">Prilika</span><span class="sxs-lookup"><span data-stu-id="a3675-112">Opportunity</span></span> 
- <span data-ttu-id="a3675-113">Ponuda</span><span class="sxs-lookup"><span data-stu-id="a3675-113">Quote</span></span> 
- <span data-ttu-id="a3675-114">Ugovor o projektu</span><span class="sxs-lookup"><span data-stu-id="a3675-114">Project Contract</span></span>

<span data-ttu-id="a3675-115">Pridruživanje tih entiteta cjeniku naznačeno je cjenikom projekta.</span><span class="sxs-lookup"><span data-stu-id="a3675-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="a3675-116">Jedan ili više cjenika možete prudružiti prodajnim entitetima Klijent, Prilika, Ponuda i Ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="a3675-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="a3675-117">Zadani cjenik projekta ne unosi se automatski u zapis klijenta.</span><span class="sxs-lookup"><span data-stu-id="a3675-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="a3675-118">Međutim, cjenik projekta možete ručno priložiti zapisu klijenta.</span><span class="sxs-lookup"><span data-stu-id="a3675-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="a3675-119">Ipak, trebate ručno priložiti cjenik projekta samo kada imate prilagođeni ugovor o određivanju cijena s klijentom.</span><span class="sxs-lookup"><span data-stu-id="a3675-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="a3675-120">Kada se cjenik projekta prilaže entitetu prodaje, provjeravaju se sljedeći podaci:</span><span class="sxs-lookup"><span data-stu-id="a3675-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="a3675-121">Cjenik ima kontekst **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="a3675-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="a3675-122">Valuta cjenika podudara se s valutom klijenta.</span><span class="sxs-lookup"><span data-stu-id="a3675-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="a3675-123">Na ugovoru o projektu, sljedeći redoslijed prvenstva upotrebljava se za automatsko postavljanje povezanih cjenika za projekt:</span><span class="sxs-lookup"><span data-stu-id="a3675-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="a3675-124">Ponuda</span><span class="sxs-lookup"><span data-stu-id="a3675-124">Quote</span></span>
2. <span data-ttu-id="a3675-125">Prilika</span><span class="sxs-lookup"><span data-stu-id="a3675-125">Opportunity</span></span>
3. <span data-ttu-id="a3675-126">Klijent</span><span class="sxs-lookup"><span data-stu-id="a3675-126">Customer</span></span> 
4. <span data-ttu-id="a3675-127">Globalne postavke</span><span class="sxs-lookup"><span data-stu-id="a3675-127">Global settings</span></span> 

<span data-ttu-id="a3675-128">Ako je cjenik projekta unesen po zadanim postavkama, sustav provjerava odgovara li valuta valuti klijenta i imaju li zadani cjenici koji su uneseni kontekst **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="a3675-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="a3675-129">Entitete Klijent, Prilika, Ponuda i Ugovor projekta možete povezati s nekoliko cjenika projekta.</span><span class="sxs-lookup"><span data-stu-id="a3675-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="a3675-130">Ova mogućnost podržava zadane cijene za određeni datum za ugovor o dugoročnom projektu, u kojem bi moglo biti potrebno više od jednog cjenika za ažuriranje cijena koje se pojavljuju zbog inflacije.</span><span class="sxs-lookup"><span data-stu-id="a3675-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="a3675-131">Međutim, ako cjenici koje pridružujete entitetu Klijent, Prilika, Ponuda ili Ugovor o projektu imaju preklapajući datum stupanja na snagu, zadane cijene možda nisu točne.</span><span class="sxs-lookup"><span data-stu-id="a3675-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="a3675-132">Stoga biste trebali osigurati da cjenici projekta koji imaju preklapajući datum stupanja na snagu nisu pridruženi tim entitetima.</span><span class="sxs-lookup"><span data-stu-id="a3675-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
