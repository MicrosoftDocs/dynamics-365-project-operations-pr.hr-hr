---
title: Postavljanje troškova i prodajnih cijena za kataloške proizvode
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073455"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="aa101-103">Postavljanje troškova i prodajnih cijena za kataloške proizvode</span><span class="sxs-lookup"><span data-stu-id="aa101-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="aa101-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="aa101-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="aa101-105">Postavljanje cijena za stavke kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="aa101-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="aa101-106">Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene kataloga proizvoda na cjenike projekata za ponude i ugovore.</span><span class="sxs-lookup"><span data-stu-id="aa101-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="aa101-107">Cijene kataloga proizvoda trebaju se postaviti u polje **Cijena proizvoda** ponude, ugovora ili računa.</span><span class="sxs-lookup"><span data-stu-id="aa101-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="aa101-108">Nemojte postavljati cijene kataloga proizvoda u cjenike projekta za te entitete.</span><span class="sxs-lookup"><span data-stu-id="aa101-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="aa101-109">Cjenici projekta ekskluzivni su za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="aa101-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="aa101-110">Postoji poslovna logika specifična za aplikaciju, koja cjenike kopira iz ponude u ugovor.</span><span class="sxs-lookup"><span data-stu-id="aa101-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="aa101-111">Rezultat je cjenik projekta specifičan za ugovor.</span><span class="sxs-lookup"><span data-stu-id="aa101-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="aa101-112">Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="aa101-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="aa101-113">Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima.</span><span class="sxs-lookup"><span data-stu-id="aa101-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="aa101-114">To znači da cjenici proizvoda ne utječu na učinkovitost postupka usvajanja ponude.</span><span class="sxs-lookup"><span data-stu-id="aa101-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
