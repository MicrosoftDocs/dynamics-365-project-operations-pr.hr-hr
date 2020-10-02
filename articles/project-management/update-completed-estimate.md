---
title: Ažuriranje očekivanog troška na završetku
description: U ovoj se temi nalaze informacije o ažuriranju predviđanja rada na projektu.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897757"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="fb7f0-103">Ažuriranje očekivanog troška na završetku</span><span class="sxs-lookup"><span data-stu-id="fb7f0-103">Update estimate at completion</span></span>

<span data-ttu-id="fb7f0-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavno uvođenje – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="fb7f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fb7f0-105">Uobičajeno je da upravitelj projekta revidira izvorne procjene u zadatku.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="fb7f0-106">Ponovna predviđanja projekta proizlaze iz procjena upravitelja projekta s obzirom na trenutačno stanje projekta.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="fb7f0-107">Međutim, upraviteljima projekta ne preporučujemo promjenu osnovnih brojeva, jer osnova projekta predstavlja utvrđeni izvor podataka za raspored projekta i procjenu troškova oko koje su se sve zainteresirane strane dogovorile.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="fb7f0-108">Postoje dva načina na koja upravitelj projekta može ponovno predvidjeti rad na zadacima:</span><span class="sxs-lookup"><span data-stu-id="fb7f0-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="fb7f0-109">Zamijenite zadani procijenjeni dovršetak (ETC, estimate to complete) novom procjenom stvarnog preostalog rada na zadatku.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="fb7f0-110">Nadjačajte zadani postotak napretka novom procjenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="fb7f0-111">Svaki od tih pristupa uzrokuje ponovno izračunavanje ETC-a, procijene dovršetka (EAC) i postotka napretka zadatka te predviđena odstupanja rada na zadatku.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="fb7f0-112">EAC, ETC i postotak napretka na zadacima sažetka ponovno se izračunavaju i stvara se novo predviđanje odstupanja rada.</span><span class="sxs-lookup"><span data-stu-id="fb7f0-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>