---
title: Određivanje cijene redaka ponude utemeljenih na proizvodu
description: U ovoj temi nalaze se informacije o primjeni cijene koštanja na redak ponude koji se temelji na proizvodu.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003442"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="210d8-103">Određivanje cijene redaka ponude utemeljenih na proizvodu</span><span class="sxs-lookup"><span data-stu-id="210d8-103">Costing product-based quote lines</span></span>

<span data-ttu-id="210d8-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="210d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="210d8-105">Redci ponude koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations također imaju polje **Cijena koštanja**.</span><span class="sxs-lookup"><span data-stu-id="210d8-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="210d8-106">To se polje upotrebljava za praćenje cijene koštanja proizvoda na retku ponude i za izračun profitabilnosti na nižim razinama.</span><span class="sxs-lookup"><span data-stu-id="210d8-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="210d8-107">Kada se za kataloški proizvod stvara redak ponude koji se temelji na proizvodu, cijenu retka ponude koji se temelji na proizvodu zadaje polje **Standardni trošak** iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="210d8-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="210d8-108">Polje standardnih troškova u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="210d8-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="210d8-109">Zadani jedinični trošak u retku ponude koji se temelji na proizvodu pretvara se u valutu prodaje na ponudi.</span><span class="sxs-lookup"><span data-stu-id="210d8-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="210d8-110">Jedinična cijena u retku ponude utemeljenom na proizvodu</span><span class="sxs-lookup"><span data-stu-id="210d8-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="210d8-111">Svrha jediničnog troška u retku ponude koji se temelji na proizvodu jest omogućivanje različitih troškova proizvoda za svaku prodaju.</span><span class="sxs-lookup"><span data-stu-id="210d8-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="210d8-112">To nije uobičajen scenarij, ali dobavljač ponekad može sniziti cijenu proizvoda ovisno o krajnjem klijentu.</span><span class="sxs-lookup"><span data-stu-id="210d8-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="210d8-113">Na primjer:</span><span class="sxs-lookup"><span data-stu-id="210d8-113">For example:</span></span>

<span data-ttu-id="210d8-114">Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum.</span><span class="sxs-lookup"><span data-stu-id="210d8-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="210d8-115">Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="210d8-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="210d8-116">Ako instalacija robotskih ruku u tvrtki A Datum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey, Trey bi mogao dati poseban popust za ovaj posao tvrtki Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="210d8-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="210d8-117">U ovom slučaju, Fabrikam će stvoriti redak ponude koji se temelji na proizvodu za robotske ruke i unijeti posebnu jediničnu cijenu za ovu ponudu.</span><span class="sxs-lookup"><span data-stu-id="210d8-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="210d8-118">Ta cijena razlikuje se od standardne cijene tvrtke Trey Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="210d8-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]