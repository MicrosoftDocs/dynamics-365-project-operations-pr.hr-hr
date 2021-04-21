---
title: Uporaba API-jeva rasporeda za izvođenje operacija s pomoću entiteta planiranja
description: U ovoj temi nalaze se informacije i uzorci za uporabu API-jeva rasporeda.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868120"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="040b7-103">Uporaba API-jeva rasporeda za izvođenje operacija s pomoću entiteta planiranja</span><span class="sxs-lookup"><span data-stu-id="040b7-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="040b7-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="040b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="040b7-105">Neke ili sve funkcionalnosti navedeni u ovoj temi dostupne su kao dio izdanja za pretpregled.</span><span class="sxs-lookup"><span data-stu-id="040b7-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="040b7-106">Sadržaj i funkcionalnost podložni su promjenama.</span><span class="sxs-lookup"><span data-stu-id="040b7-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="040b7-107">Entiteti planiranja</span><span class="sxs-lookup"><span data-stu-id="040b7-107">Scheduling entities</span></span>

<span data-ttu-id="040b7-108">API-ji rasporeda pružaju mogućnost izvršenja operacija stvaranja, ažuriranja i brisanja s pomoću **Entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="040b7-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="040b7-109">Tim se entitetima upravlja putem mehanizma za planiranje u projektu za web.</span><span class="sxs-lookup"><span data-stu-id="040b7-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="040b7-110">Operacije stvaranja, ažuriranja i brisanja s pomoću značajke **Entiteti planiranja** bile su ograničene u ranijim verzijama aplikacije Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="040b7-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="040b7-111">Sljedeća tablica daje cjelovit popis **Entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="040b7-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="040b7-112">Naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="040b7-112">Entity name</span></span>  | <span data-ttu-id="040b7-113">Logički naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="040b7-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="040b7-114">Project</span><span class="sxs-lookup"><span data-stu-id="040b7-114">Project</span></span> | <span data-ttu-id="040b7-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="040b7-115">msdyn_project</span></span> |
| <span data-ttu-id="040b7-116">Zadatak projekta</span><span class="sxs-lookup"><span data-stu-id="040b7-116">Project Task</span></span>  | <span data-ttu-id="040b7-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="040b7-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="040b7-118">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="040b7-118">Project Task Dependency</span></span>  | <span data-ttu-id="040b7-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="040b7-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="040b7-120">Dodjela resursa</span><span class="sxs-lookup"><span data-stu-id="040b7-120">Resource Assignment</span></span> | <span data-ttu-id="040b7-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="040b7-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="040b7-122">Grupa projekta</span><span class="sxs-lookup"><span data-stu-id="040b7-122">Project Bucket</span></span>  | <span data-ttu-id="040b7-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="040b7-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="040b7-124">Članov projektnog tima</span><span class="sxs-lookup"><span data-stu-id="040b7-124">Project Team Member</span></span> | <span data-ttu-id="040b7-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="040b7-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="040b7-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="040b7-126">OperationSet</span></span>

<span data-ttu-id="040b7-127">OperationSet obrazac je jedinice rada koji se može upotrebljavati kada se u transakciji mora obraditi nekoliko zahtjeva koji utječu na raspored.</span><span class="sxs-lookup"><span data-stu-id="040b7-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="040b7-128">API-ji rasporeda</span><span class="sxs-lookup"><span data-stu-id="040b7-128">Schedule APIs</span></span>

<span data-ttu-id="040b7-129">Slijedi popis trenutačnih API-ja rasporeda.</span><span class="sxs-lookup"><span data-stu-id="040b7-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="040b7-130">**msdyn_CreateProjectV1**: Ovaj se API može upotrebljavati za stvaranje projekta.</span><span class="sxs-lookup"><span data-stu-id="040b7-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="040b7-131">Projekt i zadani skup projekata stvaraju se odmah.</span><span class="sxs-lookup"><span data-stu-id="040b7-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="040b7-132">**msdyn_CreateTeamMemberV1**: Ovaj se API može upotrebljavati za stvaranje člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="040b7-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="040b7-133">Zapis člana tima stvara se odmah.</span><span class="sxs-lookup"><span data-stu-id="040b7-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="040b7-134">**msdyn_CreateOperationSetV1**: Ovaj se API može upotrebljavati za raspored nekoliko zahtjeva koji se moraju izvršiti unutar transakcije.</span><span class="sxs-lookup"><span data-stu-id="040b7-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="040b7-135">**msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za stvaranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="040b7-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="040b7-136">Entitet može biti bilo koji entitet planiranja koji podržava operaciju stvaranja.</span><span class="sxs-lookup"><span data-stu-id="040b7-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="040b7-137">**msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za ažuriranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="040b7-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="040b7-138">Entitet može biti bilo koji entitet planiranja koji podržava operaciju ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="040b7-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="040b7-139">**msdyn_PSSDeleteV1**: Ovaj se API može upotrebljavati za brisanje entiteta.</span><span class="sxs-lookup"><span data-stu-id="040b7-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="040b7-140">Entitet može biti bilo koji entitet planiranja koji podržava operaciju brisanja.</span><span class="sxs-lookup"><span data-stu-id="040b7-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="040b7-141">**msdyn_ExecuteOperationSetV1**: Ovaj se API upotrebljava za izvršavanje svih operacija unutar zadanog skupa operacija.</span><span class="sxs-lookup"><span data-stu-id="040b7-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="040b7-142">Uporaba API-jeva rasporeda sa značajkom Skup operacija</span><span class="sxs-lookup"><span data-stu-id="040b7-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="040b7-143">Kako se oba zapisa, i **CreateProjectV1** i **reateTeamMemberV1**, stvaraju odmah, ti se API-ji ne mogu izravno upotrebljavati u značajci **Skup operacija**.</span><span class="sxs-lookup"><span data-stu-id="040b7-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="040b7-144">Međutim, možete upotrebljavati API za stvaranje potrebnih zapisa, stvaranje značajke **Skup operacija**, a zatim upotrijebite ove unaprijed stvorene zapise u značajci **Skup operacija**.</span><span class="sxs-lookup"><span data-stu-id="040b7-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="040b7-145">Podržane operacije</span><span class="sxs-lookup"><span data-stu-id="040b7-145">Supported operations</span></span>

| <span data-ttu-id="040b7-146">Entitet planiranja</span><span class="sxs-lookup"><span data-stu-id="040b7-146">Scheduling entity</span></span> | <span data-ttu-id="040b7-147">Stvaranje</span><span class="sxs-lookup"><span data-stu-id="040b7-147">Create</span></span> | <span data-ttu-id="040b7-148">Ažuriranje</span><span class="sxs-lookup"><span data-stu-id="040b7-148">Update</span></span> | <span data-ttu-id="040b7-149">Izbriši</span><span class="sxs-lookup"><span data-stu-id="040b7-149">Delete</span></span> | <span data-ttu-id="040b7-150">Važne stavke</span><span class="sxs-lookup"><span data-stu-id="040b7-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="040b7-151">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="040b7-151">Project task</span></span> | <span data-ttu-id="040b7-152">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-152">Yes</span></span> | <span data-ttu-id="040b7-153">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-153">Yes</span></span> | <span data-ttu-id="040b7-154">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-154">Yes</span></span> | <span data-ttu-id="040b7-155">Nijedno</span><span class="sxs-lookup"><span data-stu-id="040b7-155">None</span></span> |
| <span data-ttu-id="040b7-156">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="040b7-156">Project task dependency</span></span> | <span data-ttu-id="040b7-157">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-157">Yes</span></span> | <span data-ttu-id="040b7-158">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-158">Yes</span></span> | | <span data-ttu-id="040b7-159">Zapisi ovisnosti projektnog zadatka ne ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="040b7-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="040b7-160">Umjesto toga, može se izbrisati stari zapis i stvoriti novi.</span><span class="sxs-lookup"><span data-stu-id="040b7-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="040b7-161">Dodjela resursa</span><span class="sxs-lookup"><span data-stu-id="040b7-161">Resource assignment</span></span> | <span data-ttu-id="040b7-162">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-162">Yes</span></span> | <span data-ttu-id="040b7-163">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-163">Yes</span></span> | | <span data-ttu-id="040b7-164">Nisu podržane operacije sa sljedećim poljima: **ID resursa koji se može rezervirati**, **Rad**, **Rad dovršen**, **Preostali rad** i **Planirani rad**.</span><span class="sxs-lookup"><span data-stu-id="040b7-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="040b7-165">Zapisi o dodjeli resursa ne ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="040b7-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="040b7-166">Umjesto toga, može se izbrisati stari zapis i stvoriti novi.</span><span class="sxs-lookup"><span data-stu-id="040b7-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="040b7-167">Grupa projekata</span><span class="sxs-lookup"><span data-stu-id="040b7-167">Project bucket</span></span> | <span data-ttu-id="040b7-168">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="040b7-168">N/A</span></span> | <span data-ttu-id="040b7-169">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="040b7-169">N/A</span></span> | <span data-ttu-id="040b7-170">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="040b7-170">N/A</span></span> | <span data-ttu-id="040b7-171">Zadana grupa kreira se s pomoću API-ja **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="040b7-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="040b7-172">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="040b7-172">Project team member</span></span> | <span data-ttu-id="040b7-173">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-173">Yes</span></span> | <span data-ttu-id="040b7-174">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-174">Yes</span></span> | <span data-ttu-id="040b7-175">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-175">Yes</span></span> | <span data-ttu-id="040b7-176">Za operaciju stvaranja upotrijebite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="040b7-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="040b7-177">Project</span><span class="sxs-lookup"><span data-stu-id="040b7-177">Project</span></span> | <span data-ttu-id="040b7-178">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-178">Yes</span></span> | <span data-ttu-id="040b7-179">Jest</span><span class="sxs-lookup"><span data-stu-id="040b7-179">Yes</span></span> | <span data-ttu-id="040b7-180">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="040b7-180">N/A</span></span> | <span data-ttu-id="040b7-181">Nisu podržane operacije sa sljedećim poljima: **Šifra države**, **Stanje skupnog generiranja**, **Token globalne revizije**, **ID kalendara**, **Rad**, **Rad dovršen**, **Preostali rad**, **Napredak**, **Završi**, **Najraniji početak zadatka** i **Trajanje**.</span><span class="sxs-lookup"><span data-stu-id="040b7-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="040b7-182">Ti se API-ji mogu pozivati s pomoću objekata entiteta koji uključuju prilagođena polja.</span><span class="sxs-lookup"><span data-stu-id="040b7-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="040b7-183">Svojstvo ID-a nije obvezno.</span><span class="sxs-lookup"><span data-stu-id="040b7-183">The ID property is optional.</span></span> <span data-ttu-id="040b7-184">Ako je omogućeno, sustav ga pokušava upotrijebiti i izbacuje iznimku ako se ne može upotrebljavati.</span><span class="sxs-lookup"><span data-stu-id="040b7-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="040b7-185">Ako nije navedeno, sustav će ga generirati.</span><span class="sxs-lookup"><span data-stu-id="040b7-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="040b7-186">Ograničenja i poznati problemi</span><span class="sxs-lookup"><span data-stu-id="040b7-186">Limitations and known issues</span></span>
<span data-ttu-id="040b7-187">Slijedi popis ograničenja i poznatih problema:</span><span class="sxs-lookup"><span data-stu-id="040b7-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="040b7-188">API-je rasporeda mogu upotrebljavati samo **Korisnici s licencom za Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="040b7-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="040b7-189">Ne mogu ih upotrebljavati:</span><span class="sxs-lookup"><span data-stu-id="040b7-189">They can't be used by:</span></span>
    - <span data-ttu-id="040b7-190">Korisnici aplikacije</span><span class="sxs-lookup"><span data-stu-id="040b7-190">Application users</span></span>
    - <span data-ttu-id="040b7-191">Korisnici sustava</span><span class="sxs-lookup"><span data-stu-id="040b7-191">System users</span></span>
    - <span data-ttu-id="040b7-192">Korisnici integracije</span><span class="sxs-lookup"><span data-stu-id="040b7-192">Integration users</span></span>
    - <span data-ttu-id="040b7-193">Ostali korisnici koji nemaju potrebnu licencu</span><span class="sxs-lookup"><span data-stu-id="040b7-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="040b7-194">Svaki **Skup operacija** može imati najviše 100 operacija.</span><span class="sxs-lookup"><span data-stu-id="040b7-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="040b7-195">Svaki korisnik može imati najviše 10 otvorenih **Skupova operacija**.</span><span class="sxs-lookup"><span data-stu-id="040b7-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="040b7-196">Project Operations trenutačno podržava maksimalno 500 ukupnih zadataka na projektu.</span><span class="sxs-lookup"><span data-stu-id="040b7-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="040b7-197">Stanje neuspjeha i dnevnici stanja značajke **Skup operacija** trenutačno nisu dostupni.</span><span class="sxs-lookup"><span data-stu-id="040b7-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="040b7-198">API-ji rasporeda u javnom su pretpregledu.</span><span class="sxs-lookup"><span data-stu-id="040b7-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="040b7-199">Microsoft ne podržava uporabu ovih API-ja u radnom okruženju.</span><span class="sxs-lookup"><span data-stu-id="040b7-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="040b7-200">Primjer scenarija</span><span class="sxs-lookup"><span data-stu-id="040b7-200">Sample scenario</span></span>

<span data-ttu-id="040b7-201">U ovom ćete scenariju stvoriti projekt, člana tima, četiri zadatka i dvije dodjele resursa.</span><span class="sxs-lookup"><span data-stu-id="040b7-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="040b7-202">Zatim ćete ažurirati jedan zadatak, ažurirati projekt, izbrisati jedan zadatak, izbrisati jednu dodjelu resursa i stvoriti ovisnost zadatka.</span><span class="sxs-lookup"><span data-stu-id="040b7-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="040b7-203">Dodatni primjeri</span><span class="sxs-lookup"><span data-stu-id="040b7-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
