---
title: Izradi cjenik
description: Kako izraditi cjenik u programu Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290305"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="2c228-103">Izradi cjenik (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2c228-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2c228-104">Cjenici nude predložak koji vaši upravitelji računa mogu koristiti za izradu ponuda i projekata kao i za utvrđivanje troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="2c228-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="2c228-105">Omogućuju popis redaka uloga i troškova te cijenu koju ćete naplatiti za svaku stavku retka.</span><span class="sxs-lookup"><span data-stu-id="2c228-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="2c228-106">Možete izraditi više cjenika da biste mogli održavati zasebne cjenovne strukture za različite regije u kojima prodajete proizvode ili različite prodajne kanale.</span><span class="sxs-lookup"><span data-stu-id="2c228-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="2c228-107">Dobro je izraditi barem jedan cjenik za svaku valutu koju planirate koristiti za naplatu klijentima.</span><span class="sxs-lookup"><span data-stu-id="2c228-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="2c228-108">Da biste izradili financijske procjene za isporučeni rad, provjerite ima li svaki projekt zamjenski cjenik troškova i prodaje.</span><span class="sxs-lookup"><span data-stu-id="2c228-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="2c228-109">Postavite zadani cjenik troškova i prodaje koji se primjenjuje na sve projekte koji su izrađeni u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="2c228-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="2c228-110">Cjenici ovise o ulogama i kategorijama troškova, tako da prije no što izradite cjenik, provjerite jeste li već konfigurirali uloge i kategorije troškova koje želite koristiti prilikom izrade cjenika.</span><span class="sxs-lookup"><span data-stu-id="2c228-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="2c228-111">Idite na **Project Service > Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="2c228-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="2c228-112">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="2c228-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="2c228-113">U izborniku **Kontekst**, odaberite je li cjenik za kategoriju **Trošak**, **Nabava** ili **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="2c228-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="2c228-114">U kategoriji **Naziv**, unesite naziv za cjenik.</span><span class="sxs-lookup"><span data-stu-id="2c228-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="2c228-115">U kategoriji **Valuta**, odaberite valutu koji ćete koristiti za naplatu i obračun troškova.</span><span class="sxs-lookup"><span data-stu-id="2c228-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="2c228-116">U kategoriji **Jedinica vremena** navedite razdoblje na koje se cijena odnosi, kao što su dan ili sat.</span><span class="sxs-lookup"><span data-stu-id="2c228-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="2c228-117">Ispunite **Datum početka**, **Datum završetka** i **Opis**, prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="2c228-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="2c228-118">Kliknite **Spremi** da biste izradili zapis tako da možete nastaviti s uređivanjem.</span><span class="sxs-lookup"><span data-stu-id="2c228-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="2c228-119">Da biste cjeniku dodali cijenu uloge, kliknite **+** pod **Cijene uloge**.</span><span class="sxs-lookup"><span data-stu-id="2c228-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="2c228-120">U oknu **Cijena uloge** unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2c228-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="2c228-121">Nastavite s dodavanjem cijena uloge prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="2c228-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="2c228-122">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="2c228-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="2c228-123">Da biste cjeniku dodali cijenu kategorije troškova, kliknite **+** pod **Cijene kategorije**.</span><span class="sxs-lookup"><span data-stu-id="2c228-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="2c228-124">U oknu **Cijena kategorije transakcija**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2c228-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="2c228-125">Nastavite s dodavanjem cijena kategorija prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="2c228-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="2c228-126">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="2c228-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="2c228-127">Da biste cjeniku dodali stavke cjenika, kliknite **+** pod **Stavke cjenika**.</span><span class="sxs-lookup"><span data-stu-id="2c228-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="2c228-128">U oknu **Stavka cjenika**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2c228-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="2c228-129">Nastavite s dodavanjem stavki cjenika prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="2c228-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="2c228-130">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="2c228-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="2c228-131">Da biste cjeniku dodali odnose teritorija, kliknite **+** pod **Odnosi teritorija**.</span><span class="sxs-lookup"><span data-stu-id="2c228-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="2c228-132">U prozoru **Nova veza**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="2c228-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="2c228-133">Nastavite s dodavanjem odnosa teritorija prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="2c228-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="2c228-134">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="2c228-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2c228-135">Također pogledajte</span><span class="sxs-lookup"><span data-stu-id="2c228-135">See Also</span></span>  
 [<span data-ttu-id="2c228-136">Konfiguriraj sustav Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2c228-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]