---
title: Faze projekta
description: Ova tema pruža informacije o fazama projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750099"
---
# <a name="project-stages"></a><span data-ttu-id="26ac8-103">Faze projekta</span><span class="sxs-lookup"><span data-stu-id="26ac8-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="26ac8-104">Faze projekta ažuriraju se kako bi odražavale napredak projekta.</span><span class="sxs-lookup"><span data-stu-id="26ac8-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="26ac8-105">Zadani tijek poslovnog procesa automatski ažurira neke faze projekta dok druge faze ručno ažurira upravitelj projekta.</span><span class="sxs-lookup"><span data-stu-id="26ac8-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="26ac8-106">Sljedeće su faze definirane u zadanom BPF-u:</span><span class="sxs-lookup"><span data-stu-id="26ac8-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="26ac8-107">Novo</span><span class="sxs-lookup"><span data-stu-id="26ac8-107">New</span></span>
- <span data-ttu-id="26ac8-108">Ponuda</span><span class="sxs-lookup"><span data-stu-id="26ac8-108">Quote</span></span>
- <span data-ttu-id="26ac8-109">Plan</span><span class="sxs-lookup"><span data-stu-id="26ac8-109">Plan</span></span>
- <span data-ttu-id="26ac8-110">Isporuka</span><span class="sxs-lookup"><span data-stu-id="26ac8-110">Deliver</span></span>
- <span data-ttu-id="26ac8-111">Dovršetak</span><span class="sxs-lookup"><span data-stu-id="26ac8-111">Complete</span></span>
- <span data-ttu-id="26ac8-112">Zatvori</span><span class="sxs-lookup"><span data-stu-id="26ac8-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="26ac8-113">Novo</span><span class="sxs-lookup"><span data-stu-id="26ac8-113">New</span></span>

<span data-ttu-id="26ac8-114">Kada stvorite projekt, faza projekta postavljena je na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="26ac8-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="26ac8-115">Ako je projekt stvoren na temelju predloška, možda sadrži raspored, procjenu i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="26ac8-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="26ac8-116">U suprotnom, to je samo skica projekta, a preostale komponente moraju se unijeti.</span><span class="sxs-lookup"><span data-stu-id="26ac8-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="26ac8-117">Ponuda</span><span class="sxs-lookup"><span data-stu-id="26ac8-117">Quote</span></span>

<span data-ttu-id="26ac8-118">Kada projekt povežete s projektom ili ponudom ili kada stvorite projekt na temelju ponude, faza projekta postavljena je na mogućnost **Ponuda**, a procijenjeni datumi početka i završetka ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="26ac8-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="26ac8-119">Kada je projekt u fazi **Ponuda**, pojedinosti o ponudi prikazuju se na kartici **Prodaja** na stranici **Entitet projekta**.</span><span class="sxs-lookup"><span data-stu-id="26ac8-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="26ac8-120">Plan</span><span class="sxs-lookup"><span data-stu-id="26ac8-120">Plan</span></span>

<span data-ttu-id="26ac8-121">Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze **Ugovor**, faza projekta ažurira se na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="26ac8-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="26ac8-122">Kada je projekt u fazi **Plan**, stranica **Entitet projekta** prikazuje pojedinosti o ugovoru.</span><span class="sxs-lookup"><span data-stu-id="26ac8-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="26ac8-123">Isporuka</span><span class="sxs-lookup"><span data-stu-id="26ac8-123">Deliver</span></span>

<span data-ttu-id="26ac8-124">Kada se plan projekta dovrši i spremni ste započeti projekt, upravitelj projekta trebao bi ažurirati fazu projekta na **Isporuka** da bi se prikazalo da je projekt započeo.</span><span class="sxs-lookup"><span data-stu-id="26ac8-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="26ac8-125">Dovršetak</span><span class="sxs-lookup"><span data-stu-id="26ac8-125">Complete</span></span> 

<span data-ttu-id="26ac8-126">Kada se posao projekta dovrši, upravitelj projekta može ažurirati fazu na **Dovršetak**.</span><span class="sxs-lookup"><span data-stu-id="26ac8-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="26ac8-127">Ažuriranjem faze projekta na **Dovršetak** upravitelj projekta označava da je rad 100 posto dovršen, no projekt ostaje otvoren kako bi se unosi vremena ili troškova na čekanju mogli zabilježiti.</span><span class="sxs-lookup"><span data-stu-id="26ac8-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="26ac8-128">Zatvori</span><span class="sxs-lookup"><span data-stu-id="26ac8-128">Close</span></span>

<span data-ttu-id="26ac8-129">Kada se zabilježe sve transakcije za projekt, upravitelj projekta može ažurirati fazu na **Zatvaranje**.</span><span class="sxs-lookup"><span data-stu-id="26ac8-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="26ac8-130">U tom trenutku nije moguće bilježiti transakcije, a projekt je postavljen samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="26ac8-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
