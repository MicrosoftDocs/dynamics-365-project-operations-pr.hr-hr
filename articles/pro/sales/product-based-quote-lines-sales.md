---
title: Pregled redaka ponude koji se temelje na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o radu s redcima ponude koji se temelje na proizvodu.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369772"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="578b6-103">Pregled redaka ponude koji se temelje na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="578b6-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="578b6-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="578b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="578b6-105">Možete stvoriti retke ponude temeljene na proizvodu u sustavu Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="578b6-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="578b6-106">Redci ponude koji se temelje na proizvodu mogu se ručno dodati ili mogu biti stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="578b6-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="578b6-107">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="578b6-107">Product catalog</span></span>

<span data-ttu-id="578b6-108">Svaki proizvod u katalogu proizvoda ima zadanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="578b6-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="578b6-109">Ako više proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja dijeli te atribute.</span><span class="sxs-lookup"><span data-stu-id="578b6-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="578b6-110">Na primjer, tvrtka prodaje pretplatničke licence za razne vrste softvera.</span><span class="sxs-lookup"><span data-stu-id="578b6-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="578b6-111">Svi pretplatnički programi imaju sljedeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="578b6-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="578b6-112">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="578b6-112">Number of users</span></span>
- <span data-ttu-id="578b6-113">Trajanje pretplate mjereno u mjesecima</span><span class="sxs-lookup"><span data-stu-id="578b6-113">A subscription duration measured in months</span></span>

<span data-ttu-id="578b6-114">Za održavanje ove vrste kataloga stvorite skupine proizvoda naziva **Softver za pretplatu** i dodajte broj korisnika i trajanje pretplate kao atribute.</span><span class="sxs-lookup"><span data-stu-id="578b6-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="578b6-115">Nadalje, možete dodati pojedinačne proizvode u skupinu proizvoda **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="578b6-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="578b6-116">Dodavanje stavki kataloga proizvoda u ponudu projekta</span><span class="sxs-lookup"><span data-stu-id="578b6-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="578b6-117">Stranice **Ponuda projekta** i **Ugovor o projektu** imaju odjeljke za retke koji se temelje na projektu i retke koji se temelje na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="578b6-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="578b6-118">Za retke koji se temelje na proizvodu, padajući popis u retku ponude ili retku ugovora o projektu obuhvaća sve proizvode i jedinice u cjeniku proizvoda.</span><span class="sxs-lookup"><span data-stu-id="578b6-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="578b6-119">Možete i dodati proizvode koji nisu dio cjenika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="578b6-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="578b6-120">Osim toga, možete odabrati proizvode iz drugih cjenika ili izravno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="578b6-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="578b6-121">Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda koristi se za dohvaćanje prodajne cijene proizvoda.</span><span class="sxs-lookup"><span data-stu-id="578b6-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="578b6-122">Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost nula (0).</span><span class="sxs-lookup"><span data-stu-id="578b6-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="578b6-123">Kada se redak ponude temelji na katalogu proizvoda, prodajnu cijenu možete nadjačati izravno u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="578b6-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="578b6-124">Redak ponude u polju **Cijene** s dvije dostupne vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="578b6-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="578b6-125">**Nadjačaj cijenu**</span><span class="sxs-lookup"><span data-stu-id="578b6-125">**Override Pricing**</span></span>
- <span data-ttu-id="578b6-126">**Koristi zadano**</span><span class="sxs-lookup"><span data-stu-id="578b6-126">**Use Default**</span></span>

<span data-ttu-id="578b6-127">Ako odaberete mogućnost **Nadjačaj cijenu**, zadana se cijena ne postavlja.</span><span class="sxs-lookup"><span data-stu-id="578b6-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="578b6-128">Umjesto toga, cijenu proizvoda morate unijeti u redak ponude.</span><span class="sxs-lookup"><span data-stu-id="578b6-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="578b6-129">Ako odaberete **Upotrijebi zadano**, upotrebljava se zadana prodajna cijena i polje se zaključava za uređivanje.</span><span class="sxs-lookup"><span data-stu-id="578b6-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="578b6-130">Zadane prodajne cijene unose se u retke ponude koji se temelje na proizvodu u ponudi.</span><span class="sxs-lookup"><span data-stu-id="578b6-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="578b6-131">Polje **Cijene** zatim se postavlja na **Nadjačaj cijene** kako biste mogli urediti zadanu cijenu u redcima ponude.</span><span class="sxs-lookup"><span data-stu-id="578b6-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="578b6-132">Ovo nadjačavanje ponašanja redaka koji se temelje na proizvodima u aplikaciji Dynamics 365 Sales, specifično je za aplikaciju Project Operations.</span><span class="sxs-lookup"><span data-stu-id="578b6-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]