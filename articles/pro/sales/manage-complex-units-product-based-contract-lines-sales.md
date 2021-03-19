---
title: Upravljanje složenim jedinicama za retke ugovora utemeljene na proizvodu – jednostavno
description: U ovoj temi nalaze se informacije o podršci prodaji proizvoda koji se temelje na pretplati.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273324"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="a324b-103">Upravljanje složenim jedinicama za retke ugovora utemeljene na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="a324b-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="a324b-104">_**Odnosi se na:** Jednostavna implementacija – od sklapanja posla do predračuna_</span><span class="sxs-lookup"><span data-stu-id="a324b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a324b-105">Dynamics 365 Project Operations upotrebljava čimbenike količine za podršku pri prodaji proizvoda temeljenih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="a324b-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="a324b-106">Za proizvode temeljene na pretplati količina u retku ugovora ili ugovora o projektu izražena je kao broj korisničkih mjeseci.</span><span class="sxs-lookup"><span data-stu-id="a324b-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="a324b-107">Cijena softvera za pretplatu pohranjuje se u katalog kao mjesečna cijena po korisniku.</span><span class="sxs-lookup"><span data-stu-id="a324b-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="a324b-108">Tijekom prodajnog postupka cijena u retku ugovora obično je dogovorena mjesečna cijena po korisniku uz popust prodajnog predstavnika.</span><span class="sxs-lookup"><span data-stu-id="a324b-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="a324b-109">Svaki ugovor ima različit broj korisnika i različit broj mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="a324b-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="a324b-110">Količina koja se upotrebljava za izračun iznosa retka ugovora proizvod je broja korisnika i broja mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="a324b-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="a324b-111">Kako bi se podržala ova vrsta prodaje, Project Operations podržava koncept *čimbenika količine*.</span><span class="sxs-lookup"><span data-stu-id="a324b-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="a324b-112">Čimbenici količine oslanjaju se na atribute proizvoda.</span><span class="sxs-lookup"><span data-stu-id="a324b-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="a324b-113">Kada konfigurirate određena svojstva za proizvod, možete označiti podskup tih svojstava ili svih svojstava kao čimbenika količine.</span><span class="sxs-lookup"><span data-stu-id="a324b-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="a324b-114">Project Operations provjerava valjanost jesu li samo numerička svojstva ili svojstva proizvoda koja imaju numeričku vrstu podataka označena kao čimbenici količine.</span><span class="sxs-lookup"><span data-stu-id="a324b-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="a324b-115">Kad se proizvod s konfiguriranim čimbenicima količine doda u redak ugovora, polje **Količina** postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="a324b-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="a324b-116">Nakon što unesete vrijednosti za svojstva proizvoda koja su čimbenici količine, Project Operations izračunava količinu retka ugovora.</span><span class="sxs-lookup"><span data-stu-id="a324b-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="a324b-117">Na primjer, Dynamics 365 Sales može imati sljedeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="a324b-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="a324b-118">**Broj korisnika**: Broj korisnika.</span><span class="sxs-lookup"><span data-stu-id="a324b-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="a324b-119">**Broj mjeseci**: Broj mjeseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="a324b-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="a324b-120">**SKU proizvoda**: Skladišni broj (SKU) proizvoda.</span><span class="sxs-lookup"><span data-stu-id="a324b-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="a324b-121">Svojstva **Broj korisnika** i **Broj mjeseci** mogu se označiti kao čimbenici količine uređivanjem svojstava retka proizvoda.</span><span class="sxs-lookup"><span data-stu-id="a324b-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="a324b-122">Kako biste stvorili čimbenike količine iz svojstava proizvoda, poduzmite sljedeće korake.</span><span class="sxs-lookup"><span data-stu-id="a324b-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="a324b-123">U aplikaciji **Project Operations** odaberite **Prodaja-Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="a324b-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="a324b-124">Otvorite proizvod za koji trebate postaviti faktore količine.</span><span class="sxs-lookup"><span data-stu-id="a324b-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="a324b-125">Uvjerite se da proizvod ima svojstva koja su već postavljena.</span><span class="sxs-lookup"><span data-stu-id="a324b-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="a324b-126">Na stranici **Informacije o projektu** odaberite karticu **Čimbenici količine**.</span><span class="sxs-lookup"><span data-stu-id="a324b-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="a324b-127">U podrešetki odaberite **+ Izračun novog polja**.</span><span class="sxs-lookup"><span data-stu-id="a324b-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="a324b-128">Unesite naziv **Čimbenika količine** i odaberite vrijednost svojstva koja se mapira u izračun polja.</span><span class="sxs-lookup"><span data-stu-id="a324b-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="a324b-129">Spremanje i zatvaranje obrasca.</span><span class="sxs-lookup"><span data-stu-id="a324b-129">Save and close the form.</span></span>
7. <span data-ttu-id="a324b-130">Ponovite korake 2 – 6 za sva svojstva koja će zajedno činiti količinu za redak ugovora koji se temelji na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="a324b-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="a324b-131">S postavljenim čimbenicima količine, kada korisnik stvara redak ugovora za ovaj proizvod, količina retka ugovora zaključava se.</span><span class="sxs-lookup"><span data-stu-id="a324b-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="a324b-132">Količina se zatim izračunava kao umnožak vrijednosti svojstva za taj redak ugovora.</span><span class="sxs-lookup"><span data-stu-id="a324b-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]