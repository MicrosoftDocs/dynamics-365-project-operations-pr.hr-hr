---
title: Cijena redaka ugovora koji se temelje na proizvodu – osnovna
description: Ova tema pruža informacije o stvaranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177232"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="f43bd-103">Cijena redaka ugovora koji se temelje na proizvodu – osnovna</span><span class="sxs-lookup"><span data-stu-id="f43bd-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="f43bd-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="f43bd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f43bd-105">Redci ugovora koji se temelje na proizvodima u aplikaciji Dynamics 365 Project Operations uključuju polje **Cijena troška** u kojem je pohranjena cijena troška proizvoda za izračun nizvodne profitabilnosti.</span><span class="sxs-lookup"><span data-stu-id="f43bd-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="f43bd-106">Kada se za kataloški proizvod stvara redak ugovora koji se temelji na proizvodu, cijenu retka ugovora koji se temelji na proizvodu zadaje polje **Standardna cijena** iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="f43bd-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="f43bd-107">Polje **Standardna cijena** u katalogu proizvoda postavlja se u osnovnoj valuti tvrtke ili ustanove.</span><span class="sxs-lookup"><span data-stu-id="f43bd-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="f43bd-108">Kada je jedinična cijena zadana retku ugovora, pretvara se u valutu prodaje u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="f43bd-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="f43bd-109">Jedinična cijena u retku ugovora koji se temelji na proizvodu</span><span class="sxs-lookup"><span data-stu-id="f43bd-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="f43bd-110">Postojanje jedinične cijene u retku ugovora koji se temelji na proizvodu omogućuje različite cijene proizvoda za svaku prodaju jedinice.</span><span class="sxs-lookup"><span data-stu-id="f43bd-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="f43bd-111">Iako nisu uvijek nužni, postoje određeni scenariji u kojima dobavljač može klijentu sniziti troškove proizvoda.</span><span class="sxs-lookup"><span data-stu-id="f43bd-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="f43bd-112">Razmotrite sljedeći scenarij:</span><span class="sxs-lookup"><span data-stu-id="f43bd-112">Consider the following scenario:</span></span>

<span data-ttu-id="f43bd-113">Fabrikam Robotics instalira robotske ruke na montažne trake tvrtke A Datum.</span><span class="sxs-lookup"><span data-stu-id="f43bd-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="f43bd-114">Fabrikam pruža usluge ugradnje, ali robotske ruke nabavljaju se od tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="f43bd-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="f43bd-115">Ako instalacija robotskih ruku u tvrtki Adatum otvori novu industrijsku vertikalu za robotske ruke tvrtke Trey Research, za ovaj bi se posao mogao odobriti poseban popust tvrtki Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="f43bd-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="f43bd-116">U tom slučaju, Fabrikam stvara redak ugovora koji se temelji na proizvodu za tvrtku Robotic Arms i za taj ugovor unosi jediničnu cijenu koja se razlikuje od standardnih cijena robotskih ruku tvrtke Trey Research.</span><span class="sxs-lookup"><span data-stu-id="f43bd-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
