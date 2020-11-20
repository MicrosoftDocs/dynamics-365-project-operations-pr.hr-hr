---
title: Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno
description: U ovoj temi nalaze se informacije o načinu postavljanja troškova i prodajnih cijena za stavke u katalogu proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176692"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="c0771-103">Postavljanje cijena koštanja i prodaje za kataloške proizvode – jednostavno</span><span class="sxs-lookup"><span data-stu-id="c0771-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="c0771-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="c0771-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c0771-105">Postavljanje cijena za stavke kataloga proizvoda u aplikaciji Dynamics 365 Project Operations isto je kao i u aplikaciji Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="c0771-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="c0771-106">Budući da se proizvodi ne mogu procijeniti ili upotrijebiti na projektima u aplikaciji Project Operations, nije potrebno postavljati cijene kataloga proizvoda na cjenike za projekt za ponude i ugovore.</span><span class="sxs-lookup"><span data-stu-id="c0771-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="c0771-107">Cijene kataloga proizvoda trebaju se postaviti u polje **Cijena proizvoda** ponude, ugovora ili računa.</span><span class="sxs-lookup"><span data-stu-id="c0771-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="c0771-108">Nemojte postavljati cijene kataloga proizvoda u cjenike za projekt za te entitete.</span><span class="sxs-lookup"><span data-stu-id="c0771-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="c0771-109">Cjenici za projekt ekskluzivni su za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c0771-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="c0771-110">Postoji poslovna logika specifična za aplikaciju, koja cjenike kopira iz ponude u ugovor.</span><span class="sxs-lookup"><span data-stu-id="c0771-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="c0771-111">Rezultat je cjenik projekta specifičan za ugovor.</span><span class="sxs-lookup"><span data-stu-id="c0771-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="c0771-112">Operacija kopiranja može odgoditi postupak usvajanja ponude ako cjenik za projekt na ponudi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="c0771-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="c0771-113">Cjenici proizvoda ne kopiraju se kako bi stvorili prilagođene cjenike u ugovorima.</span><span class="sxs-lookup"><span data-stu-id="c0771-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="c0771-114">To znači da cjenici proizvoda ne utječu na učinkovitost postupka usvajanja ponude.</span><span class="sxs-lookup"><span data-stu-id="c0771-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
