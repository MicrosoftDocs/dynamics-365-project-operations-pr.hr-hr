---
title: Dodijeli generičke resurse koji se mogu rezervirati za zadatak i projektni tim
description: Ova tema pruža informacije o rezerviranju generičkih resursa za zadatke i projektne timove.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127059"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="d9016-103">Dodijeli generičke resurse koji se mogu rezervirati zadatku i generiraj zahtjeve resursa</span><span class="sxs-lookup"><span data-stu-id="d9016-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d9016-104">Osim rezerviranja i dodjele imenovanih ili stvarnih resursa vašem projektu, možete dodijeliti generičke resurse projektnim zadacima.</span><span class="sxs-lookup"><span data-stu-id="d9016-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="d9016-105">Ti resursi mogu poslužiti kao rezervirana mjesta za imenovane resurse dok ne budete spremni za popunjavanje projekta s imenovanim resursima.</span><span class="sxs-lookup"><span data-stu-id="d9016-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="d9016-106">U programu Project Service Automation (PSA), otvorite stranicu **Projekt** i na kartici **Raspored**, unesite naziv položaja generičkog resursa u ćeliji **Resurs** rasporeda.</span><span class="sxs-lookup"><span data-stu-id="d9016-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="d9016-107">Ili kliknite ikonu **Resurs** u ćeliji da biste otvorili birača resursa, a zatim unesite naziv generičkog resursa koji želite izraditi.</span><span class="sxs-lookup"><span data-stu-id="d9016-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Izrada i dodjela generičkog člana tima](media/RM-how-to-9.png)

<span data-ttu-id="d9016-109">Time će se otvoriti panel **Brza izrada: Član projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="d9016-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="d9016-110">Unesite ulogu i organizacijsku jedinicu člana tima generičkog resursa, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="d9016-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Brza izrada generičkog člana tima](media/RM-how-to-10.png)

3. <span data-ttu-id="d9016-112">Nakon što ste izradili novi član tima generičkog resursa, dodijeljen je zadatku.</span><span class="sxs-lookup"><span data-stu-id="d9016-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="d9016-113">Možete nastaviti dodjeljivati taj generički resurs drugim zadacima u rasporedu zadataka.</span><span class="sxs-lookup"><span data-stu-id="d9016-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Dodjela postojećeg generičkog člana tima zadacima](media/RM-how-to-11.png)

4. <span data-ttu-id="d9016-115">Nakon što ste dodijelili generički resurs, možete generirati zahtjev resursa i ispuniti ga izravnim rezerviranjem ili slanjem zahtjeva resursa upravitelju resursa.</span><span class="sxs-lookup"><span data-stu-id="d9016-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generiranje zahtjeva za generički član tima](media/RM-how-to-12.png)

<span data-ttu-id="d9016-117">Na rešetki člana tima, osim što imate mogućnost koristiti birača resursa kao što je navedeno gore, možete izravno dodati generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="d9016-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="d9016-118">Resursi se dodaju zahtjevom resursa koji se temelji na datumima početka/završetka i načinu dodjele navedenim na panelu **Brza izrada: Član projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="d9016-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="d9016-119">Možete vidjeti razliku ako izravno dodate generički član tima, a zatim dodijelite više zadataka generičkom resursu nego što imaju potrebnih sati za pokrivanje.</span><span class="sxs-lookup"><span data-stu-id="d9016-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="d9016-120">Kliknite **Generiraj zahtjev** za ponovno generiranje zahtjeva da biste uskladili potrebne sate i zadatke.</span><span class="sxs-lookup"><span data-stu-id="d9016-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="d9016-121">Možete kliknuti i vezu **Zahtjev resursa** u rešetki tima da biste otvorili zahtjev i dodali vještine, preferirane resurse, itd.</span><span class="sxs-lookup"><span data-stu-id="d9016-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Zahtjev resursa](media/RM-how-to-13.png)

