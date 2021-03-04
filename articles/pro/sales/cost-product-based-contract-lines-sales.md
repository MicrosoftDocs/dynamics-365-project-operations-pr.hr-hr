---
title: Cijena redaka ugovora koji se temelje na proizvodu – osnovna
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764450"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="b248a-103">Cijena redaka ugovora koji se temelje na proizvodu – osnovna</span><span class="sxs-lookup"><span data-stu-id="b248a-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="b248a-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="b248a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b248a-105">Redci ugovora koji se temelje na proizvodu u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena koštanja**, u kojem je pohranjena cijena koštanja proizvoda za izračun profitabilnosti u daljnjem tijeku.</span><span class="sxs-lookup"><span data-stu-id="b248a-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="b248a-106">Kada se za proizvod iz kataloga stvori redak ugovora koji se temelji na proizvodu, cijenu u retku zadaje polje **Standardni trošak** iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b248a-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="b248a-107">Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="b248a-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="b248a-108">Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b248a-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="b248a-109">Jedinična cijena u retku ugovora koji se temelji na proizvodu</span><span class="sxs-lookup"><span data-stu-id="b248a-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="b248a-110">Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice.</span><span class="sxs-lookup"><span data-stu-id="b248a-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="b248a-111">Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b248a-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="b248a-112">Razmotrite sljedeći scenarij:</span><span class="sxs-lookup"><span data-stu-id="b248a-112">Consider the following scenario:</span></span>

<span data-ttu-id="b248a-113">Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum.</span><span class="sxs-lookup"><span data-stu-id="b248a-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="b248a-114">Fabrikam pruža usluge ugradnje, ali je tvrtka Robotic arms u sastavu tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b248a-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="b248a-115">Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b248a-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="b248a-116">U ovom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="b248a-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="b248a-117">U ovaj ugovor unosi se trošak po jedinici.</span><span class="sxs-lookup"><span data-stu-id="b248a-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="b248a-118">Cijena se razlikuje od cijene tvrtke Robotic arms koja je u sastavu tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b248a-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
