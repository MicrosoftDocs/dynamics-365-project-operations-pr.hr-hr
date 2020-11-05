---
title: Faze projekta
description: U ovoj se temi nalaze informacije o fazama projekta koje su dostupne u aplikaciji Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073515"
---
# <a name="project-stages"></a><span data-ttu-id="b4562-103">Faze projekta</span><span class="sxs-lookup"><span data-stu-id="b4562-103">Project stages</span></span>

<span data-ttu-id="b4562-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="b4562-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b4562-105">Faze projekta dizajnirane su tako da odražavaju napredak projekta.</span><span class="sxs-lookup"><span data-stu-id="b4562-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b4562-106">Prilagodbe se mogu upotrebljavati za automatsko ažuriranje faza s tijekovima poslovnih procesa, uslugom Power Automate ili proširenjima dodataka.</span><span class="sxs-lookup"><span data-stu-id="b4562-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b4562-107">Sljedeće su faze definirane u zadanom tijeku poslovnog procesa:</span><span class="sxs-lookup"><span data-stu-id="b4562-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b4562-108">Novo</span><span class="sxs-lookup"><span data-stu-id="b4562-108">New</span></span>
- <span data-ttu-id="b4562-109">Ponuda</span><span class="sxs-lookup"><span data-stu-id="b4562-109">Quote</span></span>
- <span data-ttu-id="b4562-110">Tarifa</span><span class="sxs-lookup"><span data-stu-id="b4562-110">Plan</span></span>
- <span data-ttu-id="b4562-111">Dostavi</span><span class="sxs-lookup"><span data-stu-id="b4562-111">Deliver</span></span>
- <span data-ttu-id="b4562-112">Dovršeno</span><span class="sxs-lookup"><span data-stu-id="b4562-112">Complete</span></span>
- <span data-ttu-id="b4562-113">Zatvaranje</span><span class="sxs-lookup"><span data-stu-id="b4562-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b4562-114">Novo</span><span class="sxs-lookup"><span data-stu-id="b4562-114">New</span></span>

<span data-ttu-id="b4562-115">Kada stvorite projekt, faza projekta postavljena je na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="b4562-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b4562-116">Ako je projekt stvoren na temelju predloška, možda sadrži raspored, procjenu i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="b4562-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b4562-117">U suprotnom, to je skica projekta, a preostale komponente moraju se unijeti.</span><span class="sxs-lookup"><span data-stu-id="b4562-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b4562-118">Ponuda</span><span class="sxs-lookup"><span data-stu-id="b4562-118">Quote</span></span>

<span data-ttu-id="b4562-119">Kada projekt povežete s projektom ili ponudom ili kada stvorite projekt na temelju ponude, faza projekta postavljena je na mogućnost **Ponuda** , a procijenjeni datumi početka i završetka ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="b4562-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b4562-120">Kada je projekt u fazi **Ponuda** , pojedinosti o ponudi prikazuju se na kartici **Prodaja** na stranici **Entitet projekta**.</span><span class="sxs-lookup"><span data-stu-id="b4562-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b4562-121">Plan</span><span class="sxs-lookup"><span data-stu-id="b4562-121">Plan</span></span>

<span data-ttu-id="b4562-122">Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze **Ugovor** , faza projekta ažurira se na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="b4562-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b4562-123">Kada je projekt u fazi **Plan** , stranica **Entitet projekta** prikazuje pojedinosti o ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b4562-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b4562-124">Isporuka</span><span class="sxs-lookup"><span data-stu-id="b4562-124">Deliver</span></span>

<span data-ttu-id="b4562-125">Kada se plan projekta dovrši i spremni ste započeti projekt, upravitelj projekta trebao bi ažurirati fazu projekta na **Isporuka** da bi se prikazalo da je projekt započeo.</span><span class="sxs-lookup"><span data-stu-id="b4562-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b4562-126">Dovršetak</span><span class="sxs-lookup"><span data-stu-id="b4562-126">Complete</span></span> 

<span data-ttu-id="b4562-127">Kada se posao projekta dovrši, upravitelj projekta može ažurirati fazu na **Dovršetak**.</span><span class="sxs-lookup"><span data-stu-id="b4562-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b4562-128">Ažuriranjem faze projekta na **Dovršetak** upravitelj projekta označava da je rad 100 posto dovršen, no projekt ostaje otvoren kako bi se unosi vremena ili troškova na čekanju mogli zabilježiti.</span><span class="sxs-lookup"><span data-stu-id="b4562-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b4562-129">Zatvori</span><span class="sxs-lookup"><span data-stu-id="b4562-129">Close</span></span>

<span data-ttu-id="b4562-130">Kada se zabilježe sve transakcije za projekt, upravitelj projekta može ažurirati fazu na **Zatvaranje**.</span><span class="sxs-lookup"><span data-stu-id="b4562-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b4562-131">U tom trenutku nije moguće bilježiti transakcije, a projekt je postavljen samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="b4562-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

