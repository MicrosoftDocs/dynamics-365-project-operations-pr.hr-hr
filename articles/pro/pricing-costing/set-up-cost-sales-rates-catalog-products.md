---
title: Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004305"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="9fbf9-103">Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno</span><span class="sxs-lookup"><span data-stu-id="9fbf9-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="9fbf9-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="9fbf9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9fbf9-105">Postavljanje cijena za stavke iz kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9fbf9-106">Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene proizvoda iz kataloga na cjenike za projekt za ponude i ugovore.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9fbf9-107">Upotrijebite polje **Cijena proizvoda** ponude, ugovora ili računa kako biste postavili cijena proizvoda iz kataloga.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="9fbf9-108">Nemojte postavljati cijene proizvoda iz kataloga u cjenike za projekt.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="9fbf9-109">Cjenici za projekt ekskluzivni su za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9fbf9-110">Poslovna logika specifična za aplikaciju kopira cjenike iz ponude u ugovor.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9fbf9-111">Rezultat je cjenik projekta specifičan za ugovor.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9fbf9-112">Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9fbf9-113">Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9fbf9-114">Budući da nije uključeno kopiranje, to ne utječe na izvedbu postupka ponude.</span><span class="sxs-lookup"><span data-stu-id="9fbf9-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]