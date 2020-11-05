---
title: Modeli vještina i stručnosti
description: Ovaj tema pruža informacije o tome kako upotrebljavati modele vještina i stručnosti.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073608"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="85163-103">Modeli vještina i stručnosti</span><span class="sxs-lookup"><span data-stu-id="85163-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="85163-104">Vještine su značajke resursa koje se dijele između aplikacije Dynamics 365 Project Service Automation i značajke Dynamics 365 Field Service, ako ona postoji.</span><span class="sxs-lookup"><span data-stu-id="85163-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="85163-105">Da biste zadržali spremište vještina u aplikaciji Project Service Automation, otvorite **Resursi** \> **Vještine resursa**.</span><span class="sxs-lookup"><span data-stu-id="85163-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Vještine resursa](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="85163-107">Upotreba modela stručnosti za ocjenjivanje resursa</span><span class="sxs-lookup"><span data-stu-id="85163-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="85163-108">Vještine za resurse ocjenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="85163-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="85163-109">Model stručnosti sadrži pojedinačne ocjene.</span><span class="sxs-lookup"><span data-stu-id="85163-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="85163-110">Da biste izradili model stručnosti, otvorite **Resursi** \> **Modeli stručnosti** , a zatim odaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="85163-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="85163-111">U novom modelu ocjenjivanja navedite vrijednost najniže ocjene, vrijednost najviše ocjene i entitet koji se ocjenjuje.</span><span class="sxs-lookup"><span data-stu-id="85163-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="85163-112">Na podrešetki **Vrijednosti ocjene** možete definirati različite vrijednosti ocjene, od najniže do najviše.</span><span class="sxs-lookup"><span data-stu-id="85163-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definirane najniže i najviše ocjene](media/Resource-Management-image85.png)

<span data-ttu-id="85163-114">Ove vrijednosti ocjena prikazane su u filtrima **Preduvjeti resursa** , **Ploča s rasporedom** i **Pomoćnik za raspored**.</span><span class="sxs-lookup"><span data-stu-id="85163-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
