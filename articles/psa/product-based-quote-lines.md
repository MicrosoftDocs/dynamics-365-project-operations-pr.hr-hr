---
title: Reci ponude temeljeni na proizvodu
description: Ova tema pruža informacije o recima ponude temeljenim na proizvodu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073568"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="939a8-103">Reci ponude temeljeni na proizvodu</span><span class="sxs-lookup"><span data-stu-id="939a8-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="939a8-104">Možete stvoriti retke ponude temeljene na proizvodu u sustavu Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="939a8-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="939a8-105">Reci ponude temeljeni na proizvodu mogu biti reci "upisa" ili mogu biti stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="939a8-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="939a8-106">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="939a8-106">Product catalog</span></span>

<span data-ttu-id="939a8-107">Proizvodi u katalogu proizvoda sustava Dynamics 365 imaju zadanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="939a8-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="939a8-108">Ako nekoliko proizvoda dijeli isti skup atributa, možete stvoriti skupinu proizvoda koja također ima te atribute.</span><span class="sxs-lookup"><span data-stu-id="939a8-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="939a8-109">Svi proizvodi u jednoj skupini proizvoda nasljeđuju isti skup atributa.</span><span class="sxs-lookup"><span data-stu-id="939a8-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="939a8-110">Na primjer, tvrtka prodaje pretplatničke licence za razne programe.</span><span class="sxs-lookup"><span data-stu-id="939a8-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="939a8-111">Svi pretplatnički programi imaju sljedeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="939a8-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="939a8-112">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="939a8-112">Number of users</span></span> 
- <span data-ttu-id="939a8-113">Trajanje pretplate (u mjesecima)</span><span class="sxs-lookup"><span data-stu-id="939a8-113">Subscription duration (in months)</span></span>

<span data-ttu-id="939a8-114">Dobar način za održavanje ove vrste kataloga jest stvaranje skupine proizvoda naziva **Softver za pretplatu** koja sadrži atribute **Broj korisnika** i **Trajanje pretplate**.</span><span class="sxs-lookup"><span data-stu-id="939a8-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="939a8-115">Skupini proizvoda **Softver za pretplatu** zatim možete dodati pojedinačne proizvode, kao što su **Dynamics 365 Sales** ili **Dynamics 365 Field Service**.</span><span class="sxs-lookup"><span data-stu-id="939a8-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="939a8-116">Dodavanje stavki kataloga proizvoda u ponudu projekta</span><span class="sxs-lookup"><span data-stu-id="939a8-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="939a8-117">Stranice ponude projekta i ugovora o projektu imaju odjeljke za dvije vrste redaka: retke temeljene na projektu i retke temeljene na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="939a8-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="939a8-118">Za retke temeljene na proizvodu Dynamics 365 koristi se za dodavanje stavki iz kataloga proizvoda u ponudu.</span><span class="sxs-lookup"><span data-stu-id="939a8-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="939a8-119">Padajući popis u retku ponude ili retku ugovora o projektu obuhvaća sve proizvode i jedinice u cjeniku proizvoda koji je priložen ponudi ili ugovoru o projektu.</span><span class="sxs-lookup"><span data-stu-id="939a8-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="939a8-120">Možete i dodati proizvode koji nisu dio cjenika proizvoda ponude.</span><span class="sxs-lookup"><span data-stu-id="939a8-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="939a8-121">Osim toga, možete odabrati proizvode s drugih cjenika ili možete odabrati proizvode izravno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="939a8-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="939a8-122">Kada odaberete proizvode izravno iz kataloga proizvoda, zadani cjenik tog proizvoda koristi se za dohvaćanje prodajne cijene proizvoda.</span><span class="sxs-lookup"><span data-stu-id="939a8-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="939a8-123">Ako zadani cjenik nije postavljen, cijena je postavljena na vrijednost 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="939a8-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="939a8-124">Ako se redak ponude temelji na katalogu proizvoda, prodajnu cijenu možete izravno zamijeniti u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="939a8-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="939a8-125">Imajte na umu da redak ponude u sustavu Dynamics 365 sadrži polje **Određivanje cijena**.</span><span class="sxs-lookup"><span data-stu-id="939a8-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="939a8-126">Dostupne su dvije vrijednosti:</span><span class="sxs-lookup"><span data-stu-id="939a8-126">Two values are available:</span></span>

- <span data-ttu-id="939a8-127">Zamijeni cijene</span><span class="sxs-lookup"><span data-stu-id="939a8-127">Override pricing</span></span>  
- <span data-ttu-id="939a8-128">Koristi zadano</span><span class="sxs-lookup"><span data-stu-id="939a8-128">Use default</span></span>

<span data-ttu-id="939a8-129">Ako ovo polje postavite na **Zamijeni cijene** , Dynamics 365 ne postavlja zadanu cijenu.</span><span class="sxs-lookup"><span data-stu-id="939a8-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="939a8-130">Morate unijeti cijenu proizvoda u retku ponude.</span><span class="sxs-lookup"><span data-stu-id="939a8-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="939a8-131">Ako ovo polje postavite na **Koristi zadano** , Dynamics 365 koristi zadanu prodajnu cijenu i zaključava polje kako bi se spriječilo uređivanje.</span><span class="sxs-lookup"><span data-stu-id="939a8-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="939a8-132">Nakon instaliranja PSA-a zadane prodajne cijene unose se u retke temeljene na proizvodu u ponudi.</span><span class="sxs-lookup"><span data-stu-id="939a8-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="939a8-133">Polje **Određivanje cijena** zatim se postavlja na **Zamijeni cijene** kako biste mogli urediti zadanu cijenu u recima ponude.</span><span class="sxs-lookup"><span data-stu-id="939a8-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Postavljanje zamjene cijena](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="939a8-135">Čimbenici količine za proizvode</span><span class="sxs-lookup"><span data-stu-id="939a8-135">Quantity factors for products</span></span>

<span data-ttu-id="939a8-136">PSA koristi čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="939a8-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="939a8-137">Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.</span><span class="sxs-lookup"><span data-stu-id="939a8-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="939a8-138">Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku.</span><span class="sxs-lookup"><span data-stu-id="939a8-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="939a8-139">Međutim, umjesto toga možete koristiti druge vremenske opise.</span><span class="sxs-lookup"><span data-stu-id="939a8-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="939a8-140">Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika.</span><span class="sxs-lookup"><span data-stu-id="939a8-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="939a8-141">Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="939a8-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="939a8-142">Količina koja se koristi za izračun iznosa retka ponude proizvod je broja korisnika i broja mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="939a8-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="939a8-143">Da bi podržao ovu vrstu prodaje, PSA je uveo koncept čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="939a8-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="939a8-144">Čimbenici količine oslanjaju se na atribute proizvoda u sustavu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="939a8-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="939a8-145">Kada konfigurirate određena svojstva za proizvod, PSA vam omogućuje označavanje podskupa tih svojstava ili svih svojstava kao čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="939a8-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="939a8-146">PSA potvrđuje da su samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine.</span><span class="sxs-lookup"><span data-stu-id="939a8-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="939a8-147">Kada se proizvod za koji su konfigurirani čimbenici količine doda u redak ponude, polje **Količina** u retku ponude postaje polje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="939a8-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="939a8-148">Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, PSA izračunava količinu retka ponude.</span><span class="sxs-lookup"><span data-stu-id="939a8-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="939a8-149">Na primjer, Dynamics 365 može imati sljedeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="939a8-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="939a8-150">**Broj korisnika** – broj korisnika</span><span class="sxs-lookup"><span data-stu-id="939a8-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="939a8-151">**Broj mjeseci** – broj mjeseci pretplate</span><span class="sxs-lookup"><span data-stu-id="939a8-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="939a8-152">**SKU proizvoda**</span><span class="sxs-lookup"><span data-stu-id="939a8-152">**Product SKU**</span></span> 

<span data-ttu-id="939a8-153">Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda.</span><span class="sxs-lookup"><span data-stu-id="939a8-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Označavanje broja korisnika i mjeseci kao čimbenika kvalitete](media/basic-guide-11.png)
 
