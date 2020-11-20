---
title: Raspoređivanje projekta sa strukturnom analizom rada
description: Raspoređivanje projekta sa strukturnom analizom rada u programu Project Service
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127869"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="c16e8-103">Raspoređivanje projekta sa strukturnom analizom rada (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c16e8-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c16e8-104">Raspored projekta objašnjava koji posao treba učiniti, koji će resursi izvesti posao i koji je vremenski okvir u kojem posao treba biti dovršen.</span><span class="sxs-lookup"><span data-stu-id="c16e8-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="c16e8-105">Raspored projekta odražava sve poslove povezane s pravovremenom isporukom projekta.</span><span class="sxs-lookup"><span data-stu-id="c16e8-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="c16e8-106">Jedan od prvih koraka u fazi pokretanja projekta je utvrđivanje rasporeda projekta.</span><span class="sxs-lookup"><span data-stu-id="c16e8-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="c16e8-107">Da biste utvrdili raspored projekta, morate stvoriti strukturnu analizu rada.</span><span class="sxs-lookup"><span data-stu-id="c16e8-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="c16e8-108">Stvorite strukturu projekta sa strukturnom analizom rada što će vam pomoći da:</span><span class="sxs-lookup"><span data-stu-id="c16e8-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="c16e8-109">Raščlanite posao na zadatke kojima se može upravljati</span><span class="sxs-lookup"><span data-stu-id="c16e8-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="c16e8-110">Procijenite vrijeme potrebno za dovršenje zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="c16e8-111">Postavite zavisnosti zadatka i trajanje zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="c16e8-112">Odredite uloge koje su potrebne za dovršetak svakog zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="c16e8-113">Raspored projekta u strukturnoj analizi rada ima poznati izgled sa interaktivnim Ganttovim grafikonom.</span><span class="sxs-lookup"><span data-stu-id="c16e8-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="c16e8-114">Stvaranje strukturne analize rada za projekt</span><span class="sxs-lookup"><span data-stu-id="c16e8-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="c16e8-115">Stvaranje strukturne analize rada za predstavljanje slijeda zadataka u projektu.</span><span class="sxs-lookup"><span data-stu-id="c16e8-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="c16e8-116">Strukturna analiza rada uključuje zadatke, zahtjeve za svaki zadatak i informacije o prihodu i trošku.</span><span class="sxs-lookup"><span data-stu-id="c16e8-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="c16e8-117">U strukturnu analizu rada možete dodati:</span><span class="sxs-lookup"><span data-stu-id="c16e8-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="c16e8-118">Slijed zadataka u hijerarhiji</span><span class="sxs-lookup"><span data-stu-id="c16e8-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="c16e8-119">Druge zadatke, ako ih ima, koje treba dovršiti prije nego što se zadatak može pokrenuti.</span><span class="sxs-lookup"><span data-stu-id="c16e8-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="c16e8-120">Početni datum, završni datum i trajanje zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="c16e8-121">Broj sati koji je potreban za zadatak</span><span class="sxs-lookup"><span data-stu-id="c16e8-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="c16e8-122">Potrebne vještine i obrazovanje radnika</span><span class="sxs-lookup"><span data-stu-id="c16e8-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="c16e8-123">Radnike koji su dodijeljeni zadatku</span><span class="sxs-lookup"><span data-stu-id="c16e8-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="c16e8-124">Očekivani prihod i troškove</span><span class="sxs-lookup"><span data-stu-id="c16e8-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="c16e8-125">Vrste zadataka</span><span class="sxs-lookup"><span data-stu-id="c16e8-125">Task types</span></span>  
<span data-ttu-id="c16e8-126">Prilikom stvaranja strukturne analize rada koristit ćete sljedeće vrsta zadataka:</span><span class="sxs-lookup"><span data-stu-id="c16e8-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="c16e8-127">**Korijenski čvor projekta**</span><span class="sxs-lookup"><span data-stu-id="c16e8-127">**Project root node**</span></span> | <span data-ttu-id="c16e8-128">Zadatak sažetka najviše razine za projekt.</span><span class="sxs-lookup"><span data-stu-id="c16e8-128">The top-level summary task for the project.</span></span> <span data-ttu-id="c16e8-129">Svi drugi zadaci projekta stvaraju se ispod njega.</span><span class="sxs-lookup"><span data-stu-id="c16e8-129">All other project tasks are created under it.</span></span> <span data-ttu-id="c16e8-130">Naziv korijenskog zadatka je naziv projekta.</span><span class="sxs-lookup"><span data-stu-id="c16e8-130">The name of the root task is the project name.</span></span> <span data-ttu-id="c16e8-131">Trud, datumi i trajanje korijenskog čvora temelje se na vrijednostima u hijerarhiji ispod njega.</span><span class="sxs-lookup"><span data-stu-id="c16e8-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="c16e8-132">Ne možete uređivati svojstva korijenskog čvora ili izbrisati korijenski čvor.</span><span class="sxs-lookup"><span data-stu-id="c16e8-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="c16e8-133">**Zadaci sažetka ili spremnika**</span><span class="sxs-lookup"><span data-stu-id="c16e8-133">**Summary or container tasks**</span></span> | <span data-ttu-id="c16e8-134">Zadatak sažetka je zadatak koji ispod sebe ima podzadatke.</span><span class="sxs-lookup"><span data-stu-id="c16e8-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="c16e8-135">Zadatak sažetka ne sadrži vlastiti trud ili trošak.</span><span class="sxs-lookup"><span data-stu-id="c16e8-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="c16e8-136">Njegov trud i trošak je skupna vrijednost njegovih podzadataka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="c16e8-137">Možete promijeniti naziv zadatka sažetka, ali ne možete promijeniti trud, datume ili trajanje jer se izračunavaju automatski.</span><span class="sxs-lookup"><span data-stu-id="c16e8-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="c16e8-138">Brisanje zadatka sažetka briše zadatak i sve njegove podzadatke.</span><span class="sxs-lookup"><span data-stu-id="c16e8-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="c16e8-139">**Zadaci lisnog čvora**</span><span class="sxs-lookup"><span data-stu-id="c16e8-139">**Leaf node tasks**</span></span> | <span data-ttu-id="c16e8-140">Zadatak lisnog čvora predstavlja najdetaljniji rad na projektu.</span><span class="sxs-lookup"><span data-stu-id="c16e8-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="c16e8-141">Sadrži procijenjeni trud, planirani broj resursa, planirane početne i završne datume i trajanje.</span><span class="sxs-lookup"><span data-stu-id="c16e8-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="c16e8-142">Hijerarhija zadataka</span><span class="sxs-lookup"><span data-stu-id="c16e8-142">Task hierarchy</span></span>  
 <span data-ttu-id="c16e8-143">Prilikom stvaranja hijerarhije zadataka pružaju vam se sljedeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="c16e8-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="c16e8-144">**Dodaj zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-144">**Add task**.</span></span>   <span data-ttu-id="c16e8-145">Zadatak možete dodati na položaj koji odaberete u hijerarhiji zadataka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="c16e8-146">Ako ne odaberete položaj, vaš novi zadatak pojavit će se na kraju.</span><span class="sxs-lookup"><span data-stu-id="c16e8-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="c16e8-147">**Uvuci zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-147">**Indent task**.</span></span>   <span data-ttu-id="c16e8-148">Uvucite zadatak da biste ga učinili podređenim zadatku izravno iznad njega.</span><span class="sxs-lookup"><span data-stu-id="c16e8-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="c16e8-149">**Izvuci zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-149">**Outdent task**.</span></span>   <span data-ttu-id="c16e8-150">Izvucite zadatak kako više ne bi bio podzadatak izvorno nadređenog zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="c16e8-151">**Premjesti gore i premjesti dolje**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-151">**Move up and Move down**.</span></span>   <span data-ttu-id="c16e8-152">Premjestite zadatke gore ili dolje u hijerarhiji nadređenog zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="c16e8-153">Premještanje zadataka gore ili dolje ne utječe na njegov trud, trošak, datume ili trajanje.</span><span class="sxs-lookup"><span data-stu-id="c16e8-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="c16e8-154">Atributi zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-154">Task attributes</span></span>  
 <span data-ttu-id="c16e8-155">Naziv zadatka opisuje posao koji treba dovršiti.</span><span class="sxs-lookup"><span data-stu-id="c16e8-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="c16e8-156">Koristite različite atribute zadatka da biste opisali raspored i zahtjeve za broj djelatnika za zadatak.</span><span class="sxs-lookup"><span data-stu-id="c16e8-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="c16e8-157">Atributi rasporeda</span><span class="sxs-lookup"><span data-stu-id="c16e8-157">Schedule attributes</span></span>

 - <span data-ttu-id="c16e8-158">Dodijelite vrijednosti stavkama **Sati truda**, **Broj resursa**, **Početni datum**, **Završni datum** i **Trajanje** da biste odredili raspored za zadatak.</span><span class="sxs-lookup"><span data-stu-id="c16e8-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="c16e8-159">**Trud** je procjena koliko će sati biti potrebno za dovršetak zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="c16e8-160">**Broj resursa** je procjena voditelja projekta za zadatak koja pomaže u stvaranju najboljeg mogućeg rasporeda.</span><span class="sxs-lookup"><span data-stu-id="c16e8-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="c16e8-161">**Trajanje** (u danima) označava broj radnih dana potrebnih za dovršetak zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="c16e8-162">Atributi broja djelatnika</span><span class="sxs-lookup"><span data-stu-id="c16e8-162">Staffing attributes</span></span>

 - <span data-ttu-id="c16e8-163">**Uloga**, **Organizacijska jedinica resursa**, **Broj resursa** i **Resursi** opisuju zahtjeve za brojem djelatnika za zadatak.</span><span class="sxs-lookup"><span data-stu-id="c16e8-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="c16e8-164">**Uloga** opisuje vrstu resursa potrebnih za izvođenje zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="c16e8-165">**Organizacijska jedinica resursa** označava organizacijsku jedinicu iz koje treba dodijeliti djelatnike resursima za taj zadatak; to također utječe na procjenu troška i prodaje za zadatak jer se to uzima u obzir prilikom određivanja prodajne cijene jedinice za resurs.</span><span class="sxs-lookup"><span data-stu-id="c16e8-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="c16e8-166">Stavka **Resursi** sadrži generički resurs ili resurs s nazivom kada je pronađen.</span><span class="sxs-lookup"><span data-stu-id="c16e8-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="c16e8-167">Zavisnosti zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-167">Task dependencies</span></span>  
 <span data-ttu-id="c16e8-168">Možete stvoriti odnose prethodnika između jednog ili više zadataka u strukturnoj analizi rada.</span><span class="sxs-lookup"><span data-stu-id="c16e8-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="c16e8-169">Možete postaviti jednu ili više vrijednosti za polje prethodnika za zadatke da biste označili zadatke o kojima će ovisiti.</span><span class="sxs-lookup"><span data-stu-id="c16e8-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="c16e8-170">Kada zadatku dodijelite vrijednost prethodnika, zadatak može započeti samo nakon dovršetka svih zadataka prethodnika.</span><span class="sxs-lookup"><span data-stu-id="c16e8-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="c16e8-171">Postavljanje te ovisnosti o zadatku rezultirat će ponovnim izračunavanjem planiranog početnog datuma zadatka kao najnovijeg kraja svih prethodnika.</span><span class="sxs-lookup"><span data-stu-id="c16e8-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="c16e8-172">Utjecaji na raspored povezani s prethodnikom nisu ograničeni načinom zadatka definiranim za zadatak.</span><span class="sxs-lookup"><span data-stu-id="c16e8-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="c16e8-173">Način zadatka</span><span class="sxs-lookup"><span data-stu-id="c16e8-173">Task mode</span></span>  
 <span data-ttu-id="c16e8-174">Način zadatka je jedan od važnih faktora koji određuju raspoređivanje zadataka lisnog čvora.</span><span class="sxs-lookup"><span data-stu-id="c16e8-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="c16e8-175">Postoje dva načina zadatka za svaki zadatak: način automatskog raspoređivanja i način ručnog raspoređivanja.</span><span class="sxs-lookup"><span data-stu-id="c16e8-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="c16e8-176">**Automatsko zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-176">**Auto scheduling**.</span></span>   <span data-ttu-id="c16e8-177">Kada način zadatka postavite na Automatsko raspoređivanje, modul raspoređivanja zadataka koristi pravila za raspoređivanje za sljedeće atribute zadatka kako bi odredio raspored za zadatak:</span><span class="sxs-lookup"><span data-stu-id="c16e8-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="c16e8-178">Prethodnici</span><span class="sxs-lookup"><span data-stu-id="c16e8-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="c16e8-179">Rad</span><span class="sxs-lookup"><span data-stu-id="c16e8-179">Effort</span></span>  
  
    -   <span data-ttu-id="c16e8-180">Broj resursa</span><span class="sxs-lookup"><span data-stu-id="c16e8-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="c16e8-181">datumi početka i završetka</span><span class="sxs-lookup"><span data-stu-id="c16e8-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="c16e8-182">**Pravila za zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-182">**Scheduling rules**.</span></span>   <span data-ttu-id="c16e8-183">Početni datum zadatka lisnog čvora koji nema prethodnike vraća se na početni datum raspoređivanja projekta.</span><span class="sxs-lookup"><span data-stu-id="c16e8-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="c16e8-184">Trajanje zadatka lisnog čvora uvijek se izračunava kao broj radnih dana između njegovog početnog i završnog datuma.</span><span class="sxs-lookup"><span data-stu-id="c16e8-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="c16e8-185">Kada se zadatak automatski raspoređuje, modul raspoređivanja uvijek slijedi pravila u nastavku:</span><span class="sxs-lookup"><span data-stu-id="c16e8-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="c16e8-186">Početni i završni datumi zadatka uvijek moraju biti radni dani prema kalendaru za raspoređivanje projekta</span><span class="sxs-lookup"><span data-stu-id="c16e8-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="c16e8-187">Početni datum zadatka koji ima prethodnike vraća se na najnoviji završni datum prethodnika</span><span class="sxs-lookup"><span data-stu-id="c16e8-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="c16e8-188">Trud = broj osoba \* trajanje \* sati u standardnom radnom danu kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="c16e8-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="c16e8-189">**Ručno planiranje**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-189">**Manual scheduling**.</span></span>   <span data-ttu-id="c16e8-190">U nekim slučajevima možda ćete željeti zaobići ta pravila.</span><span class="sxs-lookup"><span data-stu-id="c16e8-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="c16e8-191">U takvim slučajevima možete postaviti način zadatka na ručno raspoređivanje.</span><span class="sxs-lookup"><span data-stu-id="c16e8-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="c16e8-192">Time ćete zaustaviti modul raspoređivanja u izračunu vrijednosti za druge atribute raspoređivanja.</span><span class="sxs-lookup"><span data-stu-id="c16e8-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="c16e8-193">Postavljanje prethodnika na zadatke uvijek utječe na početni datum ovisnog zadatka.</span><span class="sxs-lookup"><span data-stu-id="c16e8-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="c16e8-194">Stvaranje strukturne analize rada</span><span class="sxs-lookup"><span data-stu-id="c16e8-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="c16e8-195">Idite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="c16e8-196">Kliknite projekt na kojem radite.</span><span class="sxs-lookup"><span data-stu-id="c16e8-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="c16e8-197">Na traci na vrhu ekrana odaberite strelicu prema dolje pokraj naziva projekta, a zatim kliknite Strukturna analiza rada.</span><span class="sxs-lookup"><span data-stu-id="c16e8-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="c16e8-198">Da biste dodali zadatak, kliknite **Dodaj zadatak**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="c16e8-199">Ispunite polja za zadatak, a zatim kliknite **Spremi**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="c16e8-200">Nastavite dodavati zadatke dok ne dovršite strukturnu analizu rada.</span><span class="sxs-lookup"><span data-stu-id="c16e8-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="c16e8-201">Prilikom stvaranja strukturne analize rada, možete učiniti sljedeće da biste organizirali svoje zadatke:</span><span class="sxs-lookup"><span data-stu-id="c16e8-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="c16e8-202">Odaberite zadatak i kliknite **Uvuci** da biste ga premjestite ispod drugog zadatka ili kliknite Izvuci da biste ga izvukli za jednu razinu.</span><span class="sxs-lookup"><span data-stu-id="c16e8-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="c16e8-203">Odaberite zadatak i kliknite **Premjesti gore** ili **Premjesti dolje** da biste ga pomaknuli gore ili dolje na popisu.</span><span class="sxs-lookup"><span data-stu-id="c16e8-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="c16e8-204">Kliknite **Sakrij Ganttov grafikon** da biste sakrili dijagrama i kliknite **Prikaži Ganttov grafikon** da biste ponovno prikazali.</span><span class="sxs-lookup"><span data-stu-id="c16e8-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="c16e8-205">Odaberite drugo vremensko razdoblje za Ganttov grafikon pod **Vremensko mjerilo**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="c16e8-206">Da biste uloge koje ste naveli u strukturnoj analizi rada dodali članovima tima projekta, kliknite **Generiraj tim za projekt**.</span><span class="sxs-lookup"><span data-stu-id="c16e8-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="c16e8-207">Kada ste gotovi s promjenama, kliknite **Spremi** u donjem desnom kutu zaslona.</span><span class="sxs-lookup"><span data-stu-id="c16e8-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c16e8-208">Pogledajte također</span><span class="sxs-lookup"><span data-stu-id="c16e8-208">See Also</span></span>  
 [<span data-ttu-id="c16e8-209">Vodič za voditelje projekata</span><span class="sxs-lookup"><span data-stu-id="c16e8-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
