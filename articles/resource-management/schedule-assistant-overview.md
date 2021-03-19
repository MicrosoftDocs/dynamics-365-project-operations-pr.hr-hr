---
title: Prikaz pomoćnika za raspored
description: U ovoj temi nalaze se informacije o radu s pomoćnikom za raspored za rezerviranje resursa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279219"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="210c1-103">Prikaz pomoćnika za raspored</span><span class="sxs-lookup"><span data-stu-id="210c1-103">Schedule assistant overview</span></span>

<span data-ttu-id="210c1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="210c1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="210c1-105">Pomoćnik za raspored upotrebljava se za rezerviranje resursa na temelju zahtjeva definiranih od strane voditelja projekta.</span><span class="sxs-lookup"><span data-stu-id="210c1-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="210c1-106">Pomoćnik za raspored oslanja se na parametre dane u preduvjetu resursa kako bi pronašao resurs.</span><span class="sxs-lookup"><span data-stu-id="210c1-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="210c1-107">Pomoćnik za raspored preporučuje resurse koji se podudaraju s relevantnim preduvjetima, poput vremenskih okvira ili potrebnih vještina.</span><span class="sxs-lookup"><span data-stu-id="210c1-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="210c1-108">Nakon što se utvrde prikladni resursi, voditelj resursa ili projekta može rezervirati resurs za rad.</span><span class="sxs-lookup"><span data-stu-id="210c1-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="210c1-109">Preduvjeti</span><span class="sxs-lookup"><span data-stu-id="210c1-109">Prerequisites</span></span>

<span data-ttu-id="210c1-110">Pomoćnik za raspored dio je rješenja Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="210c1-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="210c1-111">Ovo je rješenje uključeno i instalirano uz aplikacije Dynamics 365 Project Operations, Dynamics 365 Field Service i Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="210c1-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="210c1-112">Odgovarajući zahtjevi i resursi</span><span class="sxs-lookup"><span data-stu-id="210c1-112">Matching requirements and resources</span></span>

<span data-ttu-id="210c1-113">Preduvjet generiranog resursa temelji se na pojedinostima kao što su:</span><span class="sxs-lookup"><span data-stu-id="210c1-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="210c1-114">Značajke</span><span class="sxs-lookup"><span data-stu-id="210c1-114">Characteristics</span></span>
-   <span data-ttu-id="210c1-115">Uloge</span><span class="sxs-lookup"><span data-stu-id="210c1-115">Roles</span></span>
-   <span data-ttu-id="210c1-116">Poslovne jedinice</span><span class="sxs-lookup"><span data-stu-id="210c1-116">Business units</span></span>
-   <span data-ttu-id="210c1-117">Preference resursa</span><span class="sxs-lookup"><span data-stu-id="210c1-117">Resource preferences</span></span>
-   <span data-ttu-id="210c1-118">Konture rada</span><span class="sxs-lookup"><span data-stu-id="210c1-118">Effort contours</span></span>
-   <span data-ttu-id="210c1-119">Vremenska zona</span><span class="sxs-lookup"><span data-stu-id="210c1-119">Time zone</span></span>

<span data-ttu-id="210c1-120">Pomoćnik za raspored ove pojedinosti upotrebljava za filtriranje resursa.</span><span class="sxs-lookup"><span data-stu-id="210c1-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="210c1-121">Pokretanje pomoćnika za raspored</span><span class="sxs-lookup"><span data-stu-id="210c1-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="210c1-122">Postoje dva načina na koja se pokreće pomoćnik za raspored.</span><span class="sxs-lookup"><span data-stu-id="210c1-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="210c1-123">Ako upotrebljavate hibridni način, u rešetki članova tima možete odabrati bilo kojeg člana tima s neispunjenim preduvjetima resursa, a zatim odabrati mogućnost **Rezerviraj**.</span><span class="sxs-lookup"><span data-stu-id="210c1-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="210c1-124">Ako koristite središnji način, resurs pronalazi i odabire upravitelj resursa.</span><span class="sxs-lookup"><span data-stu-id="210c1-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="210c1-125">Filtri pomoćnika za raspored</span><span class="sxs-lookup"><span data-stu-id="210c1-125">Schedule assistant filters</span></span>

<span data-ttu-id="210c1-126">Nakon pokretanja pomoćnika za raspored, pojedinosti iz preduvjeta resursa prikazuju se kao filtrirane vrijednosti u lijevom oknu.</span><span class="sxs-lookup"><span data-stu-id="210c1-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="210c1-127">Upravitelj resursa ili projekta može precizno prilagoditi rezultate prilagodbom filtara kako bi udovoljili potrebama planiranja.</span><span class="sxs-lookup"><span data-stu-id="210c1-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="210c1-128">Okno filtra prikazuje mogućnosti povezane s radom, uključujući:</span><span class="sxs-lookup"><span data-stu-id="210c1-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="210c1-129">Početak i završetak rada</span><span class="sxs-lookup"><span data-stu-id="210c1-129">Work start and end</span></span>
-   <span data-ttu-id="210c1-130">Značajke</span><span class="sxs-lookup"><span data-stu-id="210c1-130">Characteristics</span></span>
-   <span data-ttu-id="210c1-131">Uloge</span><span class="sxs-lookup"><span data-stu-id="210c1-131">Roles</span></span>
-   <span data-ttu-id="210c1-132">Organizacijske jedinice</span><span class="sxs-lookup"><span data-stu-id="210c1-132">Organizational units</span></span>
-   <span data-ttu-id="210c1-133">Tvrtka resursa</span><span class="sxs-lookup"><span data-stu-id="210c1-133">Resourcing company</span></span>
-   <span data-ttu-id="210c1-134">Vrste resursa</span><span class="sxs-lookup"><span data-stu-id="210c1-134">Resource types</span></span>
-   <span data-ttu-id="210c1-135">Željeni resursi</span><span class="sxs-lookup"><span data-stu-id="210c1-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]