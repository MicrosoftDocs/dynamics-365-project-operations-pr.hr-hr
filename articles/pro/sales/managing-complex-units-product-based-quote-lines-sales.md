---
title: Upravljanje složenim jedinicama, primjerice po korisniku, po mjesecu za retke ponude utemeljene na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o upravljanju složenim jedinicama za retke ponude koji se temelje na projektu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272874"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="71648-103">Upravljanje složenim jedinicama, primjerice po korisniku, po mjesecu za retke ponude utemeljene na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="71648-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="71648-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="71648-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71648-105">Dynamics 365 Project Operations upotrebljava čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="71648-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="71648-106">Za proizvode temeljene na pretplati količina u retku ponude ili ugovora o projektu izražena je kao broj korisničkih mjeseci.</span><span class="sxs-lookup"><span data-stu-id="71648-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="71648-107">Cijena softvera za pretplatu obično se pohranjuje u katalog kao mjesečna cijena po korisniku.</span><span class="sxs-lookup"><span data-stu-id="71648-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="71648-108">Tijekom prodajnog postupka cijena u retku ponude obično je dogovorena mjesečna cijena cijena po korisniku uz popust IT prodajnog predstavnika.</span><span class="sxs-lookup"><span data-stu-id="71648-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="71648-109">Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="71648-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="71648-110">Količina koja se upotrebljava za izračun retka ponude proizvod je broja korisnika i broja mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="71648-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="71648-111">Kako bi podržao ovu vrstu prodaje, Project Operations je uveo koncept čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="71648-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="71648-112">Čimbenici količine oslanjaju se na atribute proizvoda u sustavu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="71648-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="71648-113">Kada konfigurirate određena svojstva za proizvod, Project Operations omogućuje vam označavanje podskupa ili svih svojstava kao čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="71648-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="71648-114">Project Operations provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine.</span><span class="sxs-lookup"><span data-stu-id="71648-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="71648-115">Kada u redak ponude dodate proizvod s čimbenicima količine, polje **Količina** postaje polje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="71648-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="71648-116">Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, Project Operations izračunava količinu retka ponude.</span><span class="sxs-lookup"><span data-stu-id="71648-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="71648-117">Na primjer, Dynamics 365 Sales može imati sljedeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="71648-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="71648-118">**Broj korisnika**: broj korisnika</span><span class="sxs-lookup"><span data-stu-id="71648-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="71648-119">**Broj mjeseci**: broj mjeseci pretplate</span><span class="sxs-lookup"><span data-stu-id="71648-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="71648-120">**SKU proizvoda**</span><span class="sxs-lookup"><span data-stu-id="71648-120">**Product SKU**</span></span>

<span data-ttu-id="71648-121">Svojstva **Broj korisnika** i **Broj mjeseci** možete označiti kao čimbenike količine uređivanjem svojstava retka proizvoda.</span><span class="sxs-lookup"><span data-stu-id="71648-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="71648-122">Kako biste stvorili čimbenike količine iz svojstava proizvoda, slijedite ove korake:</span><span class="sxs-lookup"><span data-stu-id="71648-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="71648-123">U lijevom navigacijskom oknu aplikacije Project Operations idite na **Prodaja** > **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="71648-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="71648-124">Otvorite proizvod za koji trebate konfigurirati čimbenike količine.</span><span class="sxs-lookup"><span data-stu-id="71648-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="71648-125">Provjerite imaju li proizvodi već konfigurirana svojstva.</span><span class="sxs-lookup"><span data-stu-id="71648-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="71648-126">Na stranici **Informacije o projektu** za Proizvod, odaberite karticu **Čimbenici količine**.</span><span class="sxs-lookup"><span data-stu-id="71648-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="71648-127">U podrešetki odaberite **+ Izračun novog polja**.</span><span class="sxs-lookup"><span data-stu-id="71648-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="71648-128">Unesite naziv čimbenika količine i odaberite vrijednost svojstva koja se mapira u izračun polja.</span><span class="sxs-lookup"><span data-stu-id="71648-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="71648-129">Spremanje i zatvaranje obrasca.</span><span class="sxs-lookup"><span data-stu-id="71648-129">Save and close the form.</span></span> <span data-ttu-id="71648-130">Ponovite ove korake za sva svojstva koja ćete upotrebljavati za izračunavanje količine za redak ponude koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="71648-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="71648-131">Kada stvarate redak ponude koji se temelji na proizvodu, količina retka ponude bit će zaključana.</span><span class="sxs-lookup"><span data-stu-id="71648-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="71648-132">Količina će se izračunati kao umnožak vrijednosti svojstva koje ste unijeli za taj redak ponude.</span><span class="sxs-lookup"><span data-stu-id="71648-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]