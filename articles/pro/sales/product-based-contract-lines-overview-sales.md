---
title: Pregled redaka ugovora koji se temelje na proizvodu – jednostavno
description: Ova tema pruža informacije o redcima ugovora koji se temelje na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177862"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="0d0d9-103">Pregled redaka ugovora koji se temelje na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="0d0d9-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="0d0d9-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="0d0d9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d0d9-105">U aplikaciji Dynamics 365 Project Operations možete stvoriti retke ugovora koji se temelje na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="0d0d9-106">Redci ugovora koji se temelje na proizvodu mogu biti ručno stvoreni redci ili stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="0d0d9-107">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="0d0d9-107">Product catalog</span></span>

<span data-ttu-id="0d0d9-108">Proizvodi u katalogu proizvoda imaju zadanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="0d0d9-109">Ako nekoliko proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja također ima te atribute.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="0d0d9-110">Svi proizvodi u jednoj skupini proizvoda nasljeđuju isti skup atributa.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="0d0d9-111">Na primjer, tvrtka prodaje pretplatničke licence za razne vrste softvera.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="0d0d9-112">Svi pretplatnički programi imaju sljedeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="0d0d9-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="0d0d9-113">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="0d0d9-113">Number of users</span></span>
- <span data-ttu-id="0d0d9-114">Trajanje pretplate (u mjesecima)</span><span class="sxs-lookup"><span data-stu-id="0d0d9-114">Subscription duration (in months)</span></span>

<span data-ttu-id="0d0d9-115">Kako biste održali ovu vrstu kataloga, stvorite asortiman proizvoda pod nazivom **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="0d0d9-116">Asortimanu proizvoda dodajte atribute **Broj korisnika** i **Trajanje pretplate**.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="0d0d9-117">Zatim dodajte pojedinačne proizvode u asortiman proizvoda **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="0d0d9-118">Dodavanje stavki kataloga proizvoda u ugovor o projektu</span><span class="sxs-lookup"><span data-stu-id="0d0d9-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="0d0d9-119">Ugovori o projektu imaju odjeljke za dvije vrste redaka, one koji se temelje na projektu i one koji se temelje na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="0d0d9-120">Redci koji se temelje na proizvodu uključuju sve proizvode i jedinice u cjeniku proizvoda na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="0d0d9-121">Proizvodi koji nisu dio cjenika proizvoda iz ugovora mogu se dodati.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="0d0d9-122">Proizvode možete odabrati iz drugih cjenika ili izravno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="0d0d9-123">Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda upotrebljava se za dohvaćanje prodajne cijene proizvoda.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="0d0d9-124">Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="0d0d9-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="0d0d9-125">Ako se redak ugovora temelji na katalogu proizvoda, prodajnu cijenu možete izravno zamijeniti u retku.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="0d0d9-126">Redak ugovora sadrži polje **Određivanje cijene** s dvije vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="0d0d9-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="0d0d9-127">**Zamijeni cijene**</span><span class="sxs-lookup"><span data-stu-id="0d0d9-127">**Override pricing**</span></span>
- <span data-ttu-id="0d0d9-128">**Koristi zadano**</span><span class="sxs-lookup"><span data-stu-id="0d0d9-128">**Use default**</span></span>

<span data-ttu-id="0d0d9-129">Ako polje **Određivanje cijene** postavite na **Zamjensko određivanje cijene**, zadana se cijena ne postavlja.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="0d0d9-130">Unesite cijenu za proizvod u redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="0d0d9-131">Ako polje postavite na **Upotrijebi zadano**, upotrebljava se zadana prodajna cijena i polje se ne može uređivati.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="0d0d9-132">Nakon instaliranja aplikacije Project Operations, zadane prodajne cijene unose se u retke koji se temelje na proizvodu u ugovoru.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="0d0d9-133">Polje **Određivanje cijena** postavlja se na **Zamijeni cijene** kako biste mogli urediti zadanu cijenu u redcima ugovora.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="0d0d9-134">Ova je zamjena za ponašanje redaka koji se temelje na proizvodu u aplikaciji Dynamics 365 Sales specifična za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="0d0d9-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
