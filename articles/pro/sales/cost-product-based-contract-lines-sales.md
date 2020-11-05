---
title: Određivanje cijene redaka ugovora utemeljenih na proizvodu
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/20/2020
ms.locfileid: "4073619"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="763a7-103">Određivanje cijene redaka ugovora utemeljenih na proizvodu</span><span class="sxs-lookup"><span data-stu-id="763a7-103">Costing product-based contract lines</span></span>

<span data-ttu-id="763a7-104">_**Odnosi se na:** Jednostavno uvođenje – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="763a7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="763a7-105">Redci ugovora koji se temelje na proizvodima u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena troška** u kojem je pohranjena cijena troška proizvoda za izračun nizvodne profitabilnosti.</span><span class="sxs-lookup"><span data-stu-id="763a7-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="763a7-106">Kada se za kataloški proizvod stvara redak ugovora koji se temelji na proizvodu, cijenu retka ugovora koji se temelji na proizvodu zadaje polje **Standardna cijena** iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="763a7-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="763a7-107">Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="763a7-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="763a7-108">Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="763a7-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="763a7-109">Jedinična cijena u retku ugovora koji se temelji na proizvodu</span><span class="sxs-lookup"><span data-stu-id="763a7-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="763a7-110">Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice.</span><span class="sxs-lookup"><span data-stu-id="763a7-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="763a7-111">Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda.</span><span class="sxs-lookup"><span data-stu-id="763a7-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="763a7-112">Razmotrite sljedeći scenarij:</span><span class="sxs-lookup"><span data-stu-id="763a7-112">Consider the following scenario:</span></span>

<span data-ttu-id="763a7-113">Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum.</span><span class="sxs-lookup"><span data-stu-id="763a7-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="763a7-114">Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="763a7-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="763a7-115">Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="763a7-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="763a7-116">U tom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms i za taj ugovor unosi jediničnu cijenu koja se razlikuje od standardnih cijena robotskih ruku tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="763a7-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
