---
title: Izradi cjenik
description: Kako izraditi cjenik u programu Project Service
author: rumant
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
ms.openlocfilehash: 32f0cc66d1caa08bd24eb232338444df0388de3f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006052"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="0568e-103">Izradi cjenik (Project Service)</span><span class="sxs-lookup"><span data-stu-id="0568e-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0568e-104">Cjenici nude predložak koji vaši upravitelji računa mogu koristiti za izradu ponuda i projekata kao i za utvrđivanje troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="0568e-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="0568e-105">Omogućuju popis redaka uloga i troškova te cijenu koju ćete naplatiti za svaku stavku retka.</span><span class="sxs-lookup"><span data-stu-id="0568e-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="0568e-106">Možete izraditi više cjenika da biste mogli održavati zasebne cjenovne strukture za različite regije u kojima prodajete proizvode ili različite prodajne kanale.</span><span class="sxs-lookup"><span data-stu-id="0568e-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="0568e-107">Dobro je izraditi barem jedan cjenik za svaku valutu koju planirate koristiti za naplatu klijentima.</span><span class="sxs-lookup"><span data-stu-id="0568e-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="0568e-108">Da biste izradili financijske procjene za isporučeni rad, provjerite ima li svaki projekt zamjenski cjenik troškova i prodaje.</span><span class="sxs-lookup"><span data-stu-id="0568e-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="0568e-109">Postavite zadani cjenik troškova i prodaje koji se primjenjuje na sve projekte koji su izrađeni u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0568e-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="0568e-110">Cjenici ovise o ulogama i kategorijama troškova, tako da prije no što izradite cjenik, provjerite jeste li već konfigurirali uloge i kategorije troškova koje želite koristiti prilikom izrade cjenika.</span><span class="sxs-lookup"><span data-stu-id="0568e-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="0568e-111">Idite na **Project Service > Cjenici**.</span><span class="sxs-lookup"><span data-stu-id="0568e-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="0568e-112">Kliknite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0568e-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="0568e-113">U izborniku **Kontekst**, odaberite je li cjenik za kategoriju **Trošak**, **Nabava** ili **Prodaja**.</span><span class="sxs-lookup"><span data-stu-id="0568e-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="0568e-114">U kategoriji **Naziv**, unesite naziv za cjenik.</span><span class="sxs-lookup"><span data-stu-id="0568e-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="0568e-115">U kategoriji **Valuta**, odaberite valutu koji ćete koristiti za naplatu i obračun troškova.</span><span class="sxs-lookup"><span data-stu-id="0568e-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="0568e-116">U kategoriji **Jedinica vremena** navedite razdoblje na koje se cijena odnosi, kao što su dan ili sat.</span><span class="sxs-lookup"><span data-stu-id="0568e-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="0568e-117">Ispunite **Datum početka**, **Datum završetka** i **Opis**, prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="0568e-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="0568e-118">Kliknite **Spremi** da biste izradili zapis tako da možete nastaviti s uređivanjem.</span><span class="sxs-lookup"><span data-stu-id="0568e-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="0568e-119">Da biste cjeniku dodali cijenu uloge, kliknite **+** pod **Cijene uloge**.</span><span class="sxs-lookup"><span data-stu-id="0568e-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="0568e-120">U oknu **Cijena uloge** unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="0568e-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0568e-121">Nastavite s dodavanjem cijena uloge prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="0568e-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="0568e-122">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="0568e-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="0568e-123">Da biste cjeniku dodali cijenu kategorije troškova, kliknite **+** pod **Cijene kategorije**.</span><span class="sxs-lookup"><span data-stu-id="0568e-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="0568e-124">U oknu **Cijena kategorije transakcija**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="0568e-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0568e-125">Nastavite s dodavanjem cijena kategorija prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="0568e-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="0568e-126">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="0568e-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="0568e-127">Da biste cjeniku dodali stavke cjenika, kliknite **+** pod **Stavke cjenika**.</span><span class="sxs-lookup"><span data-stu-id="0568e-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="0568e-128">U oknu **Stavka cjenika**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="0568e-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0568e-129">Nastavite s dodavanjem stavki cjenika prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="0568e-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="0568e-130">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="0568e-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="0568e-131">Da biste cjeniku dodali odnose teritorija, kliknite **+** pod **Odnosi teritorija**.</span><span class="sxs-lookup"><span data-stu-id="0568e-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="0568e-132">U prozoru **Nova veza**, unesite pojedinosti, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="0568e-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="0568e-133">Nastavite s dodavanjem odnosa teritorija prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="0568e-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="0568e-134">Kada ste završili, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="0568e-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0568e-135">Također pogledajte</span><span class="sxs-lookup"><span data-stu-id="0568e-135">See Also</span></span>  
 [<span data-ttu-id="0568e-136">Konfiguriraj sustav Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="0568e-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]