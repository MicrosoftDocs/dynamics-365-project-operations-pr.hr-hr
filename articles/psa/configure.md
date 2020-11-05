---
title: Konfiguriraj sustav Project Service Automation
description: Koraci za konfiguriranje programa Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fd02611b5b3133e097b2818a725b6c5d667e5ac0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073497"
---
# <a name="configure-project-service"></a><span data-ttu-id="6a7a5-103">Konfiguriraj program Project Service</span><span class="sxs-lookup"><span data-stu-id="6a7a5-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6a7a5-104">Prije no što možete upotrebljavati mogućnosti automatizacije sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] za upravljanje računima, projektima i resursima, morate izvršiti nekoliko koraka konfiguracije da biste osigurali da rješenje sustava [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] odgovara potrebama vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="6a7a5-105">Ti koraci uključuju:</span><span class="sxs-lookup"><span data-stu-id="6a7a5-105">These steps include:</span></span>  
  
-   <span data-ttu-id="6a7a5-106">[Postavi jedinice vremena](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="6a7a5-107">Konfigurirajte jedinice vremena u katalogu proizvoda koji ćete koristiti kao osnovu za planiranje i naplatu projekata.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="6a7a5-108">[Postavi valute i tečajeve](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="6a7a5-109">Postavite valute koje ćete koristiti za projekte.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="6a7a5-110">[Izradi organizacijske jedinice](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="6a7a5-111">Postavite grupe koje vaše poduzeće koristi za podjelu poslovanja prema zemljopisnoj lokaciji, poslovnoj funkciji ili drugoj logičnoj podjeli.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="6a7a5-112">[Postavi učestalosti faktura](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="6a7a5-113">Postavite razdoblja koja želite koristiti za naplatu.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="6a7a5-114">[Konfiguriraj kategorije transakcije](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="6a7a5-115">Postavite kategorije transakcije prema kojima savjetnici mogu naplatiti naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="6a7a5-116">[Konfiguriraj kategorije troškova](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="6a7a5-117">Postavite kategorije prema kojima savjetnici mogu naplatiti naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="6a7a5-118">[Izradi stavke kataloga proizvoda](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="6a7a5-119">Dodajte proizvode koje prodajete, kao što su licence za softver, u katalog proizvoda.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="6a7a5-120">[Izradi cjenik](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="6a7a5-121">Konfigurirajte različite cjenike, ovisno o tome koliko želite naplatiti klijentima za svaku ulogu koju njihov projekt zahtijeva.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="6a7a5-122">[Postavi resurse](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="6a7a5-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="6a7a5-123">Dodajte vještine, stručnosti, uloge resursa i druge informacije o resursu koje će vam trebati za projekte.</span><span class="sxs-lookup"><span data-stu-id="6a7a5-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6a7a5-124">Također pogledajte</span><span class="sxs-lookup"><span data-stu-id="6a7a5-124">See Also</span></span>  
 <span data-ttu-id="6a7a5-125">[Pregled sustava Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="6a7a5-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="6a7a5-126">[Konfiguriraj sustav Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="6a7a5-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="6a7a5-127">[Vodič za upravitelja računa](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6a7a5-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="6a7a5-128">[Vodič za upravitelja projekta](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6a7a5-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="6a7a5-129">[Vodič za upravitelja resursa](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6a7a5-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="6a7a5-130">Vodič za vrijeme, troškove i suradnju</span><span class="sxs-lookup"><span data-stu-id="6a7a5-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
