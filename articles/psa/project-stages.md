---
title: Vrste faza projekta
description: Ova tema pruža informacije o fazama projekta.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 61db23e19614f5c3be5c8b46fbf72463705e409c
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148094"
---
# <a name="project-stage-types"></a><span data-ttu-id="446ca-103">Vrste faza projekta</span><span class="sxs-lookup"><span data-stu-id="446ca-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="446ca-104">Faze projekta dizajnirane su tako da odražavaju napredak projekta.</span><span class="sxs-lookup"><span data-stu-id="446ca-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="446ca-105">Prilagodbe se mogu upotrebljavati za automatsko ažuriranje faza s tijekovima poslovnih procesa, uslugom Power Automate ili proširenjima dodataka.</span><span class="sxs-lookup"><span data-stu-id="446ca-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="446ca-106">Sljedeće su faze definirane u zadanom BPF-u:</span><span class="sxs-lookup"><span data-stu-id="446ca-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="446ca-107">Novo</span><span class="sxs-lookup"><span data-stu-id="446ca-107">New</span></span>
- <span data-ttu-id="446ca-108">Ponuda</span><span class="sxs-lookup"><span data-stu-id="446ca-108">Quote</span></span>
- <span data-ttu-id="446ca-109">Plan</span><span class="sxs-lookup"><span data-stu-id="446ca-109">Plan</span></span>
- <span data-ttu-id="446ca-110">Isporuka</span><span class="sxs-lookup"><span data-stu-id="446ca-110">Deliver</span></span>
- <span data-ttu-id="446ca-111">Dovršetak</span><span class="sxs-lookup"><span data-stu-id="446ca-111">Complete</span></span>
- <span data-ttu-id="446ca-112">Zatvori</span><span class="sxs-lookup"><span data-stu-id="446ca-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="446ca-113">Novo</span><span class="sxs-lookup"><span data-stu-id="446ca-113">New</span></span>

<span data-ttu-id="446ca-114">Kada stvorite projekt, faza projekta postavljena je na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="446ca-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="446ca-115">Ako je projekt stvoren na temelju predloška, možda sadrži raspored, procjenu i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="446ca-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="446ca-116">U suprotnom, to je samo skica projekta, a preostale komponente moraju se unijeti.</span><span class="sxs-lookup"><span data-stu-id="446ca-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="446ca-117">Ponuda</span><span class="sxs-lookup"><span data-stu-id="446ca-117">Quote</span></span>

<span data-ttu-id="446ca-118">Kada projekt povežete s projektom ili ponudom ili kada stvorite projekt na temelju ponude, faza projekta postavljena je na mogućnost **Ponuda**, a procijenjeni datumi početka i završetka ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="446ca-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="446ca-119">Kada je projekt u fazi **Ponuda**, pojedinosti o ponudi prikazuju se na kartici **Prodaja** na stranici **Entitet projekta**.</span><span class="sxs-lookup"><span data-stu-id="446ca-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="446ca-120">Plan</span><span class="sxs-lookup"><span data-stu-id="446ca-120">Plan</span></span>

<span data-ttu-id="446ca-121">Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze **Ugovor**, faza projekta ažurira se na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="446ca-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="446ca-122">Kada je projekt u fazi **Plan**, stranica **Entitet projekta** prikazuje pojedinosti o ugovoru.</span><span class="sxs-lookup"><span data-stu-id="446ca-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="446ca-123">Isporuka</span><span class="sxs-lookup"><span data-stu-id="446ca-123">Deliver</span></span>

<span data-ttu-id="446ca-124">Kada se plan projekta dovrši i spremni ste započeti projekt, upravitelj projekta trebao bi ažurirati fazu projekta na **Isporuka** da bi se prikazalo da je projekt započeo.</span><span class="sxs-lookup"><span data-stu-id="446ca-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="446ca-125">Dovršetak</span><span class="sxs-lookup"><span data-stu-id="446ca-125">Complete</span></span> 

<span data-ttu-id="446ca-126">Kada se posao projekta dovrši, upravitelj projekta može ažurirati fazu na **Dovršetak**.</span><span class="sxs-lookup"><span data-stu-id="446ca-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="446ca-127">Ažuriranjem faze projekta na **Dovršetak** upravitelj projekta označava da je rad 100 posto dovršen, no projekt ostaje otvoren kako bi se unosi vremena ili troškova na čekanju mogli zabilježiti.</span><span class="sxs-lookup"><span data-stu-id="446ca-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="446ca-128">Zatvori</span><span class="sxs-lookup"><span data-stu-id="446ca-128">Close</span></span>

<span data-ttu-id="446ca-129">Kada se zabilježe sve transakcije za projekt, upravitelj projekta može ažurirati fazu na **Zatvaranje**.</span><span class="sxs-lookup"><span data-stu-id="446ca-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="446ca-130">U tom trenutku nije moguće bilježiti transakcije, a projekt je postavljen samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="446ca-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
