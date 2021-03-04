---
title: Praćenje statusa projekta
description: Praćenje statusa projekta u programu Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149579"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="89adf-103">Praćenje statusa projekta (Project Service)</span><span class="sxs-lookup"><span data-stu-id="89adf-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="89adf-104">Koristite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] da biste pratili tijek klijentovog projekta.</span><span class="sxs-lookup"><span data-stu-id="89adf-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="89adf-105">Kako aktivnost napreduje tako se faze projekta ažuriraju kako bi odražavale fazu aktivnosti:</span><span class="sxs-lookup"><span data-stu-id="89adf-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="89adf-106">**Novo**</span><span class="sxs-lookup"><span data-stu-id="89adf-106">**New**</span></span>    | <span data-ttu-id="89adf-107">Kada stvorite projekt, faza je postavljena na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="89adf-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="89adf-108">Ako ste projekt stvorili iz predloška, u ovoj fazi projekt možda ima raspored, procjene i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="89adf-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="89adf-109">U suprotnom, imat ćete strukturu projekta i morat ćete ručno unijeti ostale komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="89adf-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="89adf-110">**Ponuda**</span><span class="sxs-lookup"><span data-stu-id="89adf-110">**Quote**</span></span>   |      <span data-ttu-id="89adf-111">Kada projekt pridružujete ponudi ili ga stvarate iz ponude, faza projekta postavljena je na **Ponuda** i procijenjeni datumi početka i završetka također se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="89adf-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="89adf-112">Kada je projekt u fazi ponude, detalji o ponudi prikazuju se na kartici **Prodaja** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="89adf-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="89adf-113">**Plan**</span><span class="sxs-lookup"><span data-stu-id="89adf-113">**Plan**</span></span>   |                                     <span data-ttu-id="89adf-114">Kada osvojite ponudu povezanu s projektom i kada aktivnost napreduje do faze ugovora, faza projekta ažurira se na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="89adf-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="89adf-115">Detalji o ugovoru prikazuju se na kartici **Prodaja** na stranici **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="89adf-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="89adf-116">**Dovrši**</span><span class="sxs-lookup"><span data-stu-id="89adf-116">**Complete**</span></span> |                    <span data-ttu-id="89adf-117">Nakon dovršetka projekta možete prebaciti fazu na **Dovršeno**.</span><span class="sxs-lookup"><span data-stu-id="89adf-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="89adf-118">Kada je faza projekta postavljena na dovršeno, podrazumijeva se da je posao 100% dovršen, ali je projekt još uvijek otvoren za vrijeme na čekanju ili stavke troškova koje treba zabilježiti.</span><span class="sxs-lookup"><span data-stu-id="89adf-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="89adf-119">**Zatvori**</span><span class="sxs-lookup"><span data-stu-id="89adf-119">**Close**</span></span>   |           <span data-ttu-id="89adf-120">Kada zabilježite sve transakcije na projektu i ne očekujete daljnje transakcije, možete fazu ručno postaviti na **Zatvoreno**.</span><span class="sxs-lookup"><span data-stu-id="89adf-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="89adf-121">Kada je projekt postavljen na **Zatvoreno**, više ne možete bilježiti transakcije na projektu i projekt će biti samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="89adf-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="89adf-122">Za praćenje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="89adf-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="89adf-123">Idite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="89adf-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="89adf-124">Kliknite projekt na kojem radite.</span><span class="sxs-lookup"><span data-stu-id="89adf-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="89adf-125">Na traci na vrhu ekrana odaberite strelicu prema dolje pokraj naziva projekta, a zatim kliknite **Praćenje projekta**.</span><span class="sxs-lookup"><span data-stu-id="89adf-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="89adf-126">Odaberite **Praćenje truda** ili **Praćenje troška** na padajućem popisu iznad popisa zadataka.</span><span class="sxs-lookup"><span data-stu-id="89adf-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="89adf-127">Dvokliknite bilo koji zadatak da biste ga uredili.</span><span class="sxs-lookup"><span data-stu-id="89adf-127">Double-click any task to edit it.</span></span> <span data-ttu-id="89adf-128">Također možete premjestiti ili promijeniti veličinu traka u Ganttovom grafikonu da biste promijenili vrijeme i tijek za zadatak.</span><span class="sxs-lookup"><span data-stu-id="89adf-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="89adf-129">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="89adf-129">See Also</span></span>  
 [<span data-ttu-id="89adf-130">Vodič voditelja projekta</span><span class="sxs-lookup"><span data-stu-id="89adf-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
