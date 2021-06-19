---
title: Definiranje vještina i stručnosti
description: U ovoj temi nalaze se informacije o načinu uporabe modela stručnosti za ocjenu resursa.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015322"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="60932-103">Definiranje vještina i stručnosti</span><span class="sxs-lookup"><span data-stu-id="60932-103">Define skills and proficiencies</span></span>

<span data-ttu-id="60932-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="60932-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="60932-105">Vještine su značajke resursa koje se dijele između aplikacije Dynamics 365 Project Operations i značajke Dynamics 365 Field Service, ako ona postoji.</span><span class="sxs-lookup"><span data-stu-id="60932-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="60932-106">Kako biste zadržali spremište vještina u aplikaciji Project Operations, idite na **Resursi** \> **Vještine resursa**.</span><span class="sxs-lookup"><span data-stu-id="60932-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="60932-107">Upotreba modela stručnosti za ocjenjivanje resursa</span><span class="sxs-lookup"><span data-stu-id="60932-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="60932-108">Vještine za resurse ocjenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="60932-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="60932-109">Model stručnosti sadrži pojedinačne ocjene.</span><span class="sxs-lookup"><span data-stu-id="60932-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="60932-110">Da biste izradili model stručnosti, otvorite **Resursi** \> **Modeli stručnosti**, a zatim odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="60932-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="60932-111">U novom modelu ocjenjivanja navedite vrijednost najniže ocjene, vrijednost najviše ocjene i entitet koji se ocjenjuje.</span><span class="sxs-lookup"><span data-stu-id="60932-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="60932-112">Na podrešetki **Vrijednosti ocjene** možete definirati različite vrijednosti ocjene, od najniže do najviše.</span><span class="sxs-lookup"><span data-stu-id="60932-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="60932-113">Ove vrijednosti ocjena prikazane su u filtrima **Preduvjeti resursa**, **Ploča s rasporedom** i **Pomoćnik za raspored**.</span><span class="sxs-lookup"><span data-stu-id="60932-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]