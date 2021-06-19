---
title: Uporaba API-jeva rasporeda za izvođenje operacija s pomoću entiteta planiranja
description: U ovoj temi nalaze se informacije i uzorci za uporabu API-jeva rasporeda.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116788"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="4d0a1-103">Uporaba API-jeva rasporeda za izvođenje operacija s pomoću entiteta planiranja</span><span class="sxs-lookup"><span data-stu-id="4d0a1-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="4d0a1-104">_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_</span><span class="sxs-lookup"><span data-stu-id="4d0a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="4d0a1-105">Neke ili sve funkcionalnosti navedeni u ovoj temi dostupne su kao dio izdanja za pretpregled.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="4d0a1-106">Sadržaj i funkcionalnost podložni su promjenama.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="4d0a1-107">Entiteti planiranja</span><span class="sxs-lookup"><span data-stu-id="4d0a1-107">Scheduling entities</span></span>

<span data-ttu-id="4d0a1-108">API-ji rasporeda pružaju mogućnost izvršenja operacija stvaranja, ažuriranja i brisanja s pomoću **Entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="4d0a1-109">Tim se entitetima upravlja putem mehanizma za planiranje u aplikaciji Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="4d0a1-110">Operacije stvaranja, ažuriranja i brisanja s pomoću značajke **Entiteti planiranja** bile su ograničene u ranijim verzijama aplikacije Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="4d0a1-111">Sljedeća tablica daje cjelovit popis **Entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="4d0a1-112">Naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="4d0a1-112">Entity name</span></span>  | <span data-ttu-id="4d0a1-113">Logički naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="4d0a1-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="4d0a1-114">Project</span><span class="sxs-lookup"><span data-stu-id="4d0a1-114">Project</span></span> | <span data-ttu-id="4d0a1-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4d0a1-115">msdyn_project</span></span> |
| <span data-ttu-id="4d0a1-116">Zadatak projekta</span><span class="sxs-lookup"><span data-stu-id="4d0a1-116">Project Task</span></span>  | <span data-ttu-id="4d0a1-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="4d0a1-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="4d0a1-118">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="4d0a1-118">Project Task Dependency</span></span>  | <span data-ttu-id="4d0a1-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="4d0a1-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="4d0a1-120">Dodjela resursa</span><span class="sxs-lookup"><span data-stu-id="4d0a1-120">Resource Assignment</span></span> | <span data-ttu-id="4d0a1-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="4d0a1-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="4d0a1-122">Grupa projekta</span><span class="sxs-lookup"><span data-stu-id="4d0a1-122">Project Bucket</span></span>  | <span data-ttu-id="4d0a1-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="4d0a1-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="4d0a1-124">Članov projektnog tima</span><span class="sxs-lookup"><span data-stu-id="4d0a1-124">Project Team Member</span></span> | <span data-ttu-id="4d0a1-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="4d0a1-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="4d0a1-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="4d0a1-126">OperationSet</span></span>

<span data-ttu-id="4d0a1-127">OperationSet obrazac je jedinice rada koji se može upotrebljavati kada se u transakciji mora obraditi nekoliko zahtjeva koji utječu na raspored.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="4d0a1-128">API-ji rasporeda</span><span class="sxs-lookup"><span data-stu-id="4d0a1-128">Schedule APIs</span></span>

<span data-ttu-id="4d0a1-129">Slijedi popis trenutačnih API-ja rasporeda.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="4d0a1-130">**msdyn_CreateProjectV1**: Ovaj se API može upotrebljavati za stvaranje projekta.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="4d0a1-131">Projekt i zadani skup projekata stvaraju se odmah.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="4d0a1-132">**msdyn_CreateTeamMemberV1**: Ovaj se API može upotrebljavati za stvaranje člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="4d0a1-133">Zapis člana tima stvara se odmah.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="4d0a1-134">**msdyn_CreateOperationSetV1**: Ovaj se API može upotrebljavati za raspored nekoliko zahtjeva koji se moraju izvršiti unutar transakcije.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="4d0a1-135">**msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za stvaranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="4d0a1-136">Entitet može biti bilo koji entitet planiranja koji podržava operaciju stvaranja.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="4d0a1-137">**msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za ažuriranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="4d0a1-138">Entitet može biti bilo koji entitet planiranja koji podržava operaciju ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="4d0a1-139">**msdyn_PSSDeleteV1**: Ovaj se API može upotrebljavati za brisanje entiteta.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="4d0a1-140">Entitet može biti bilo koji entitet planiranja koji podržava operaciju brisanja.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="4d0a1-141">**msdyn_ExecuteOperationSetV1**: Ovaj se API upotrebljava za izvršavanje svih operacija unutar zadanog skupa operacija.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="4d0a1-142">Uporaba API-jeva rasporeda sa značajkom Skup operacija</span><span class="sxs-lookup"><span data-stu-id="4d0a1-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="4d0a1-143">Kako se oba zapisa, i **CreateProjectV1** i **reateTeamMemberV1**, stvaraju odmah, ti se API-ji ne mogu izravno upotrebljavati u značajci **Skup operacija**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="4d0a1-144">Međutim, možete upotrebljavati API za stvaranje potrebnih zapisa, stvaranje značajke **Skup operacija**, a zatim upotrijebite ove unaprijed stvorene zapise u značajci **Skup operacija**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="4d0a1-145">Podržane operacije</span><span class="sxs-lookup"><span data-stu-id="4d0a1-145">Supported operations</span></span>

| <span data-ttu-id="4d0a1-146">Entitet planiranja</span><span class="sxs-lookup"><span data-stu-id="4d0a1-146">Scheduling entity</span></span> | <span data-ttu-id="4d0a1-147">Stvaranje</span><span class="sxs-lookup"><span data-stu-id="4d0a1-147">Create</span></span> | <span data-ttu-id="4d0a1-148">Ažuriranje</span><span class="sxs-lookup"><span data-stu-id="4d0a1-148">Update</span></span> | <span data-ttu-id="4d0a1-149">Izbriši</span><span class="sxs-lookup"><span data-stu-id="4d0a1-149">Delete</span></span> | <span data-ttu-id="4d0a1-150">Važne stavke</span><span class="sxs-lookup"><span data-stu-id="4d0a1-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="4d0a1-151">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="4d0a1-151">Project task</span></span> | <span data-ttu-id="4d0a1-152">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-152">Yes</span></span> | <span data-ttu-id="4d0a1-153">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-153">Yes</span></span> | <span data-ttu-id="4d0a1-154">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-154">Yes</span></span> | <span data-ttu-id="4d0a1-155">Nijedno</span><span class="sxs-lookup"><span data-stu-id="4d0a1-155">None</span></span> |
| <span data-ttu-id="4d0a1-156">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="4d0a1-156">Project task dependency</span></span> | <span data-ttu-id="4d0a1-157">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-157">Yes</span></span> | <span data-ttu-id="4d0a1-158">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-158">Yes</span></span> | | <span data-ttu-id="4d0a1-159">Zapisi ovisnosti projektnog zadatka ne ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="4d0a1-160">Umjesto toga, može se izbrisati stari zapis i stvoriti novi.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4d0a1-161">Dodjela resursa</span><span class="sxs-lookup"><span data-stu-id="4d0a1-161">Resource assignment</span></span> | <span data-ttu-id="4d0a1-162">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-162">Yes</span></span> | <span data-ttu-id="4d0a1-163">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-163">Yes</span></span> | | <span data-ttu-id="4d0a1-164">Nisu podržane operacije sa sljedećim poljima: **ID resursa koji se može rezervirati**, **Rad**, **Rad dovršen**, **Preostali rad** i **Planirani rad**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="4d0a1-165">Zapisi o dodjeli resursa ne ažuriraju se.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="4d0a1-166">Umjesto toga, može se izbrisati stari zapis i stvoriti novi.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="4d0a1-167">Grupa projekata</span><span class="sxs-lookup"><span data-stu-id="4d0a1-167">Project bucket</span></span> | <span data-ttu-id="4d0a1-168">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="4d0a1-168">N/A</span></span> | <span data-ttu-id="4d0a1-169">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="4d0a1-169">N/A</span></span> | <span data-ttu-id="4d0a1-170">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="4d0a1-170">N/A</span></span> | <span data-ttu-id="4d0a1-171">Zadana grupa kreira se s pomoću API-ja **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="4d0a1-172">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="4d0a1-172">Project team member</span></span> | <span data-ttu-id="4d0a1-173">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-173">Yes</span></span> | <span data-ttu-id="4d0a1-174">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-174">Yes</span></span> | <span data-ttu-id="4d0a1-175">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-175">Yes</span></span> | <span data-ttu-id="4d0a1-176">Za operaciju stvaranja upotrijebite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="4d0a1-177">Project</span><span class="sxs-lookup"><span data-stu-id="4d0a1-177">Project</span></span> | <span data-ttu-id="4d0a1-178">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-178">Yes</span></span> | <span data-ttu-id="4d0a1-179">Jest</span><span class="sxs-lookup"><span data-stu-id="4d0a1-179">Yes</span></span> | <span data-ttu-id="4d0a1-180">Nije dostupno</span><span class="sxs-lookup"><span data-stu-id="4d0a1-180">N/A</span></span> | <span data-ttu-id="4d0a1-181">Nisu podržane operacije sa sljedećim poljima: **Šifra države**, **Stanje skupnog generiranja**, **Token globalne revizije**, **ID kalendara**, **Rad**, **Rad dovršen**, **Preostali rad**, **Napredak**, **Završi**, **Najraniji početak zadatka** i **Trajanje**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="4d0a1-182">Ti se API-ji mogu pozivati s pomoću objekata entiteta koji uključuju prilagođena polja.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="4d0a1-183">Svojstvo ID-a nije obvezno.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-183">The ID property is optional.</span></span> <span data-ttu-id="4d0a1-184">Ako je omogućeno, sustav ga pokušava upotrijebiti i izbacuje iznimku ako se ne može upotrebljavati.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="4d0a1-185">Ako nije navedeno, sustav će ga generirati.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="4d0a1-186">Ograničena polja</span><span class="sxs-lookup"><span data-stu-id="4d0a1-186">Restricted fields</span></span>

<span data-ttu-id="4d0a1-187">Sljedeće tablice definiraju polja koja su ograničena za **Stvaranje** i **Uređivanje.**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="4d0a1-188">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="4d0a1-188">Project task</span></span>

| <span data-ttu-id="4d0a1-189">**Logički naziv**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-189">**Logical name**</span></span>                       | <span data-ttu-id="4d0a1-190">**Može se stvoriti**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-190">**Can create**</span></span> | <span data-ttu-id="4d0a1-191">**Može se uređivati**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="4d0a1-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="4d0a1-193">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-193">no</span></span>             | <span data-ttu-id="4d0a1-194">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-194">no</span></span>               |
| <span data-ttu-id="4d0a1-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="4d0a1-196">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-196">no</span></span>             | <span data-ttu-id="4d0a1-197">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-197">no</span></span>               |
| <span data-ttu-id="4d0a1-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="4d0a1-198">msdyn_actualend</span></span>                        | <span data-ttu-id="4d0a1-199">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-199">no</span></span>             | <span data-ttu-id="4d0a1-200">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-200">no</span></span>               |
| <span data-ttu-id="4d0a1-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="4d0a1-202">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-202">no</span></span>             | <span data-ttu-id="4d0a1-203">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-203">no</span></span>               |
| <span data-ttu-id="4d0a1-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4d0a1-205">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-205">no</span></span>             | <span data-ttu-id="4d0a1-206">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-206">no</span></span>               |
| <span data-ttu-id="4d0a1-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="4d0a1-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="4d0a1-208">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-208">no</span></span>             | <span data-ttu-id="4d0a1-209">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-209">no</span></span>               |
| <span data-ttu-id="4d0a1-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="4d0a1-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="4d0a1-211">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-211">no</span></span>             | <span data-ttu-id="4d0a1-212">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-212">no</span></span>               |
| <span data-ttu-id="4d0a1-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="4d0a1-214">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-214">no</span></span>             | <span data-ttu-id="4d0a1-215">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-215">no</span></span>               |
| <span data-ttu-id="4d0a1-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4d0a1-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="4d0a1-217">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-217">no</span></span>             | <span data-ttu-id="4d0a1-218">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-218">no</span></span>               |
| <span data-ttu-id="4d0a1-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4d0a1-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4d0a1-220">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-220">no</span></span>             | <span data-ttu-id="4d0a1-221">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-221">no</span></span>               |
| <span data-ttu-id="4d0a1-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4d0a1-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="4d0a1-223">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-223">no</span></span>             | <span data-ttu-id="4d0a1-224">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-224">no</span></span>               |
| <span data-ttu-id="4d0a1-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="4d0a1-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="4d0a1-226">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-226">no</span></span>             | <span data-ttu-id="4d0a1-227">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-227">no</span></span>               |
| <span data-ttu-id="4d0a1-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="4d0a1-229">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-229">no</span></span>             | <span data-ttu-id="4d0a1-230">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-230">no</span></span>               |
| <span data-ttu-id="4d0a1-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="4d0a1-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="4d0a1-232">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-232">no</span></span>             | <span data-ttu-id="4d0a1-233">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-233">no</span></span>               |
| <span data-ttu-id="4d0a1-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="4d0a1-235">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-235">no</span></span>             | <span data-ttu-id="4d0a1-236">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-236">no</span></span>               |
| <span data-ttu-id="4d0a1-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="4d0a1-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="4d0a1-238">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-238">no</span></span>             | <span data-ttu-id="4d0a1-239">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-239">no</span></span>               |
| <span data-ttu-id="4d0a1-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="4d0a1-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="4d0a1-241">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-241">no</span></span>             | <span data-ttu-id="4d0a1-242">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-242">no</span></span>               |
| <span data-ttu-id="4d0a1-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="4d0a1-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="4d0a1-244">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-244">no</span></span>             | <span data-ttu-id="4d0a1-245">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-245">no</span></span>               |
| <span data-ttu-id="4d0a1-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="4d0a1-247">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-247">no</span></span>             | <span data-ttu-id="4d0a1-248">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-248">no</span></span>               |
| <span data-ttu-id="4d0a1-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="4d0a1-250">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-250">no</span></span>             | <span data-ttu-id="4d0a1-251">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-251">no</span></span>               |
| <span data-ttu-id="4d0a1-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="4d0a1-253">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-253">no</span></span>             | <span data-ttu-id="4d0a1-254">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-254">no</span></span>               |
| <span data-ttu-id="4d0a1-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="4d0a1-256">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-256">no</span></span>             | <span data-ttu-id="4d0a1-257">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-257">no</span></span>               |
| <span data-ttu-id="4d0a1-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4d0a1-259">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-259">no</span></span>             | <span data-ttu-id="4d0a1-260">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-260">no</span></span>               |
| <span data-ttu-id="4d0a1-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4d0a1-262">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-262">no</span></span>             | <span data-ttu-id="4d0a1-263">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-263">no</span></span>               |
| <span data-ttu-id="4d0a1-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="4d0a1-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="4d0a1-265">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-265">no</span></span>             | <span data-ttu-id="4d0a1-266">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-266">no</span></span>               |
| <span data-ttu-id="4d0a1-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4d0a1-267">msdyn_progress</span></span>                         | <span data-ttu-id="4d0a1-268">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-268">no</span></span>             | <span data-ttu-id="4d0a1-269">ne (da za P4W)</span><span class="sxs-lookup"><span data-stu-id="4d0a1-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="4d0a1-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4d0a1-271">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-271">no</span></span>             | <span data-ttu-id="4d0a1-272">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-272">no</span></span>               |
| <span data-ttu-id="4d0a1-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4d0a1-274">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-274">no</span></span>             | <span data-ttu-id="4d0a1-275">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-275">no</span></span>               |
| <span data-ttu-id="4d0a1-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4d0a1-277">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-277">no</span></span>             | <span data-ttu-id="4d0a1-278">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-278">no</span></span>               |
| <span data-ttu-id="4d0a1-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4d0a1-280">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-280">no</span></span>             | <span data-ttu-id="4d0a1-281">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-281">no</span></span>               |
| <span data-ttu-id="4d0a1-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="4d0a1-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="4d0a1-283">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-283">no</span></span>             | <span data-ttu-id="4d0a1-284">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-284">no</span></span>               |
| <span data-ttu-id="4d0a1-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4d0a1-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="4d0a1-286">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-286">no</span></span>             | <span data-ttu-id="4d0a1-287">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-287">no</span></span>               |
| <span data-ttu-id="4d0a1-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="4d0a1-289">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-289">no</span></span>             | <span data-ttu-id="4d0a1-290">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-290">no</span></span>               |
| <span data-ttu-id="4d0a1-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="4d0a1-292">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-292">no</span></span>             | <span data-ttu-id="4d0a1-293">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-293">no</span></span>               |
| <span data-ttu-id="4d0a1-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="4d0a1-295">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-295">no</span></span>             | <span data-ttu-id="4d0a1-296">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-296">no</span></span>               |
| <span data-ttu-id="4d0a1-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="4d0a1-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="4d0a1-298">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-298">no</span></span>             | <span data-ttu-id="4d0a1-299">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-299">no</span></span>               |
| <span data-ttu-id="4d0a1-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4d0a1-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="4d0a1-301">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-301">no</span></span>             | <span data-ttu-id="4d0a1-302">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-302">no</span></span>               |
| <span data-ttu-id="4d0a1-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="4d0a1-304">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-304">no</span></span>             | <span data-ttu-id="4d0a1-305">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-305">no</span></span>               |
| <span data-ttu-id="4d0a1-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4d0a1-307">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-307">no</span></span>             | <span data-ttu-id="4d0a1-308">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-308">no</span></span>               |
| <span data-ttu-id="4d0a1-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4d0a1-310">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-310">no</span></span>             | <span data-ttu-id="4d0a1-311">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-311">no</span></span>               |
| <span data-ttu-id="4d0a1-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="4d0a1-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="4d0a1-313">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-313">no</span></span>             | <span data-ttu-id="4d0a1-314">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-314">no</span></span>               |
| <span data-ttu-id="4d0a1-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="4d0a1-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="4d0a1-316">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-316">no</span></span>             | <span data-ttu-id="4d0a1-317">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-317">no</span></span>               |
| <span data-ttu-id="4d0a1-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="4d0a1-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="4d0a1-319">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-319">no</span></span>             | <span data-ttu-id="4d0a1-320">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-320">no</span></span>               |
| <span data-ttu-id="4d0a1-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4d0a1-322">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-322">no</span></span>             | <span data-ttu-id="4d0a1-323">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-323">no</span></span>               |
| <span data-ttu-id="4d0a1-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="4d0a1-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="4d0a1-325">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-325">no</span></span>             | <span data-ttu-id="4d0a1-326">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-326">no</span></span>               |
| <span data-ttu-id="4d0a1-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="4d0a1-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="4d0a1-328">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-328">no</span></span>             | <span data-ttu-id="4d0a1-329">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-329">no</span></span>               |
| <span data-ttu-id="4d0a1-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="4d0a1-330">msdyn_summary</span></span>                          | <span data-ttu-id="4d0a1-331">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-331">no</span></span>             | <span data-ttu-id="4d0a1-332">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-332">no</span></span>               |
| <span data-ttu-id="4d0a1-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="4d0a1-334">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-334">no</span></span>             | <span data-ttu-id="4d0a1-335">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-335">no</span></span>               |
| <span data-ttu-id="4d0a1-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="4d0a1-337">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-337">no</span></span>             | <span data-ttu-id="4d0a1-338">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="4d0a1-339">Ovisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="4d0a1-339">Project task dependency</span></span>

| <span data-ttu-id="4d0a1-340">**Logički naziv**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-340">**Logical name**</span></span>              | <span data-ttu-id="4d0a1-341">**Može se stvoriti**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-341">**Can create**</span></span> | <span data-ttu-id="4d0a1-342">**Može se uređivati**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="4d0a1-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="4d0a1-343">msdyn_linktype</span></span>                | <span data-ttu-id="4d0a1-344">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-344">no</span></span>             | <span data-ttu-id="4d0a1-345">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-345">no</span></span>           |
| <span data-ttu-id="4d0a1-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="4d0a1-346">msdyn_linktypename</span></span>            | <span data-ttu-id="4d0a1-347">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-347">no</span></span>             | <span data-ttu-id="4d0a1-348">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-348">no</span></span>           |
| <span data-ttu-id="4d0a1-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="4d0a1-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="4d0a1-350">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-350">yes</span></span>            | <span data-ttu-id="4d0a1-351">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-351">no</span></span>           |
| <span data-ttu-id="4d0a1-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="4d0a1-353">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-353">yes</span></span>            | <span data-ttu-id="4d0a1-354">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-354">no</span></span>           |
| <span data-ttu-id="4d0a1-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="4d0a1-355">msdyn_project</span></span>                 | <span data-ttu-id="4d0a1-356">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-356">yes</span></span>            | <span data-ttu-id="4d0a1-357">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-357">no</span></span>           |
| <span data-ttu-id="4d0a1-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-358">msdyn_projectname</span></span>             | <span data-ttu-id="4d0a1-359">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-359">yes</span></span>            | <span data-ttu-id="4d0a1-360">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-360">no</span></span>           |
| <span data-ttu-id="4d0a1-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="4d0a1-362">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-362">yes</span></span>            | <span data-ttu-id="4d0a1-363">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-363">no</span></span>           |
| <span data-ttu-id="4d0a1-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="4d0a1-364">msdyn_successortask</span></span>           | <span data-ttu-id="4d0a1-365">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-365">yes</span></span>            | <span data-ttu-id="4d0a1-366">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-366">no</span></span>           |
| <span data-ttu-id="4d0a1-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="4d0a1-368">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-368">yes</span></span>            | <span data-ttu-id="4d0a1-369">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="4d0a1-370">Dodjela resursa</span><span class="sxs-lookup"><span data-stu-id="4d0a1-370">Resource assignment</span></span>

| <span data-ttu-id="4d0a1-371">**Logički naziv**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-371">**Logical name**</span></span>             | <span data-ttu-id="4d0a1-372">**Može se stvoriti**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-372">**Can create**</span></span> | <span data-ttu-id="4d0a1-373">**Može se uređivati**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="4d0a1-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="4d0a1-375">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-375">yes</span></span>            | <span data-ttu-id="4d0a1-376">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-376">no</span></span>           |
| <span data-ttu-id="4d0a1-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="4d0a1-378">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-378">yes</span></span>            | <span data-ttu-id="4d0a1-379">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-379">no</span></span>           |
| <span data-ttu-id="4d0a1-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="4d0a1-381">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-381">no</span></span>             | <span data-ttu-id="4d0a1-382">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-382">no</span></span>           |
| <span data-ttu-id="4d0a1-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="4d0a1-384">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-384">no</span></span>             | <span data-ttu-id="4d0a1-385">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-385">no</span></span>           |
| <span data-ttu-id="4d0a1-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="4d0a1-386">msdyn_committype</span></span>             | <span data-ttu-id="4d0a1-387">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-387">no</span></span>             | <span data-ttu-id="4d0a1-388">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-388">no</span></span>           |
| <span data-ttu-id="4d0a1-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="4d0a1-389">msdyn_committypename</span></span>         | <span data-ttu-id="4d0a1-390">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-390">no</span></span>             | <span data-ttu-id="4d0a1-391">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-391">no</span></span>           |
| <span data-ttu-id="4d0a1-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4d0a1-392">msdyn_effort</span></span>                 | <span data-ttu-id="4d0a1-393">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-393">no</span></span>             | <span data-ttu-id="4d0a1-394">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-394">no</span></span>           |
| <span data-ttu-id="4d0a1-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4d0a1-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="4d0a1-396">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-396">no</span></span>             | <span data-ttu-id="4d0a1-397">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-397">no</span></span>           |
| <span data-ttu-id="4d0a1-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4d0a1-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="4d0a1-399">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-399">no</span></span>             | <span data-ttu-id="4d0a1-400">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-400">no</span></span>           |
| <span data-ttu-id="4d0a1-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4d0a1-401">msdyn_finish</span></span>                 | <span data-ttu-id="4d0a1-402">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-402">no</span></span>             | <span data-ttu-id="4d0a1-403">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-403">no</span></span>           |
| <span data-ttu-id="4d0a1-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="4d0a1-405">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-405">no</span></span>             | <span data-ttu-id="4d0a1-406">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-406">no</span></span>           |
| <span data-ttu-id="4d0a1-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="4d0a1-408">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-408">no</span></span>             | <span data-ttu-id="4d0a1-409">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-409">no</span></span>           |
| <span data-ttu-id="4d0a1-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="4d0a1-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="4d0a1-411">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-411">no</span></span>             | <span data-ttu-id="4d0a1-412">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-412">no</span></span>           |
| <span data-ttu-id="4d0a1-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="4d0a1-414">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-414">no</span></span>             | <span data-ttu-id="4d0a1-415">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-415">no</span></span>           |
| <span data-ttu-id="4d0a1-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="4d0a1-417">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-417">no</span></span>             | <span data-ttu-id="4d0a1-418">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-418">no</span></span>           |
| <span data-ttu-id="4d0a1-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="4d0a1-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="4d0a1-420">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-420">no</span></span>             | <span data-ttu-id="4d0a1-421">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-421">no</span></span>           |
| <span data-ttu-id="4d0a1-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="4d0a1-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="4d0a1-423">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-423">no</span></span>             | <span data-ttu-id="4d0a1-424">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-424">no</span></span>           |
| <span data-ttu-id="4d0a1-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-425">msdyn_projectid</span></span>              | <span data-ttu-id="4d0a1-426">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-426">yes</span></span>            | <span data-ttu-id="4d0a1-427">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-427">no</span></span>           |
| <span data-ttu-id="4d0a1-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-428">msdyn_projectidname</span></span>          | <span data-ttu-id="4d0a1-429">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-429">no</span></span>             | <span data-ttu-id="4d0a1-430">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-430">no</span></span>           |
| <span data-ttu-id="4d0a1-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="4d0a1-432">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-432">no</span></span>             | <span data-ttu-id="4d0a1-433">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-433">no</span></span>           |
| <span data-ttu-id="4d0a1-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="4d0a1-435">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-435">no</span></span>             | <span data-ttu-id="4d0a1-436">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-436">no</span></span>           |
| <span data-ttu-id="4d0a1-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4d0a1-437">msdyn_start</span></span>                  | <span data-ttu-id="4d0a1-438">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-438">no</span></span>             | <span data-ttu-id="4d0a1-439">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-439">no</span></span>           |
| <span data-ttu-id="4d0a1-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-440">msdyn_taskid</span></span>                 | <span data-ttu-id="4d0a1-441">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-441">no</span></span>             | <span data-ttu-id="4d0a1-442">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-442">no</span></span>           |
| <span data-ttu-id="4d0a1-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-443">msdyn_taskidname</span></span>             | <span data-ttu-id="4d0a1-444">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-444">no</span></span>             | <span data-ttu-id="4d0a1-445">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-445">no</span></span>           |
| <span data-ttu-id="4d0a1-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="4d0a1-447">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-447">no</span></span>             | <span data-ttu-id="4d0a1-448">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="4d0a1-449">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="4d0a1-449">Project team member</span></span>

| <span data-ttu-id="4d0a1-450">**Logički naziv**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-450">**Logical name**</span></span>                                 | <span data-ttu-id="4d0a1-451">**Može se stvoriti**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-451">**Can create**</span></span> | <span data-ttu-id="4d0a1-452">**Može se uređivati**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="4d0a1-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="4d0a1-454">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-454">no</span></span>             | <span data-ttu-id="4d0a1-455">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-455">no</span></span>           |
| <span data-ttu-id="4d0a1-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="4d0a1-457">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-457">no</span></span>             | <span data-ttu-id="4d0a1-458">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-458">no</span></span>           |
| <span data-ttu-id="4d0a1-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="4d0a1-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="4d0a1-460">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-460">no</span></span>             | <span data-ttu-id="4d0a1-461">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-461">no</span></span>           |
| <span data-ttu-id="4d0a1-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="4d0a1-463">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-463">no</span></span>             | <span data-ttu-id="4d0a1-464">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-464">no</span></span>           |
| <span data-ttu-id="4d0a1-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4d0a1-465">msdyn_effort</span></span>                                     | <span data-ttu-id="4d0a1-466">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-466">no</span></span>             | <span data-ttu-id="4d0a1-467">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-467">no</span></span>           |
| <span data-ttu-id="4d0a1-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4d0a1-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="4d0a1-469">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-469">no</span></span>             | <span data-ttu-id="4d0a1-470">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-470">no</span></span>           |
| <span data-ttu-id="4d0a1-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4d0a1-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="4d0a1-472">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-472">no</span></span>             | <span data-ttu-id="4d0a1-473">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-473">no</span></span>           |
| <span data-ttu-id="4d0a1-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4d0a1-474">msdyn_finish</span></span>                                     | <span data-ttu-id="4d0a1-475">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-475">no</span></span>             | <span data-ttu-id="4d0a1-476">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-476">no</span></span>           |
| <span data-ttu-id="4d0a1-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="4d0a1-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="4d0a1-478">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-478">no</span></span>             | <span data-ttu-id="4d0a1-479">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-479">no</span></span>           |
| <span data-ttu-id="4d0a1-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="4d0a1-480">msdyn_hours</span></span>                                      | <span data-ttu-id="4d0a1-481">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-481">no</span></span>             | <span data-ttu-id="4d0a1-482">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-482">no</span></span>           |
| <span data-ttu-id="4d0a1-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="4d0a1-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="4d0a1-484">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-484">no</span></span>             | <span data-ttu-id="4d0a1-485">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-485">no</span></span>           |
| <span data-ttu-id="4d0a1-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="4d0a1-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="4d0a1-487">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-487">no</span></span>             | <span data-ttu-id="4d0a1-488">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-488">no</span></span>           |
| <span data-ttu-id="4d0a1-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="4d0a1-490">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-490">no</span></span>             | <span data-ttu-id="4d0a1-491">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-491">no</span></span>           |
| <span data-ttu-id="4d0a1-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="4d0a1-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="4d0a1-493">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-493">no</span></span>             | <span data-ttu-id="4d0a1-494">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-494">no</span></span>           |
| <span data-ttu-id="4d0a1-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="4d0a1-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="4d0a1-496">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-496">no</span></span>             | <span data-ttu-id="4d0a1-497">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-497">no</span></span>           |
| <span data-ttu-id="4d0a1-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="4d0a1-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="4d0a1-499">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-499">no</span></span>             | <span data-ttu-id="4d0a1-500">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-500">no</span></span>           |
| <span data-ttu-id="4d0a1-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="4d0a1-501">msdyn_start</span></span>                                      | <span data-ttu-id="4d0a1-502">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-502">no</span></span>             | <span data-ttu-id="4d0a1-503">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="4d0a1-504">Project</span><span class="sxs-lookup"><span data-stu-id="4d0a1-504">Project</span></span>

| <span data-ttu-id="4d0a1-505">**Logički naziv**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-505">**Logical name**</span></span>                       | <span data-ttu-id="4d0a1-506">**Može se stvoriti**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-506">**Can create**</span></span> | <span data-ttu-id="4d0a1-507">**Može se uređivati**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="4d0a1-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="4d0a1-509">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-509">no</span></span>             | <span data-ttu-id="4d0a1-510">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-510">no</span></span>           |
| <span data-ttu-id="4d0a1-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="4d0a1-512">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-512">no</span></span>             | <span data-ttu-id="4d0a1-513">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-513">no</span></span>           |
| <span data-ttu-id="4d0a1-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="4d0a1-515">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-515">no</span></span>             | <span data-ttu-id="4d0a1-516">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-516">no</span></span>           |
| <span data-ttu-id="4d0a1-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="4d0a1-518">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-518">no</span></span>             | <span data-ttu-id="4d0a1-519">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-519">no</span></span>           |
| <span data-ttu-id="4d0a1-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="4d0a1-521">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-521">no</span></span>             | <span data-ttu-id="4d0a1-522">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-522">no</span></span>           |
| <span data-ttu-id="4d0a1-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="4d0a1-524">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-524">no</span></span>             | <span data-ttu-id="4d0a1-525">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-525">no</span></span>           |
| <span data-ttu-id="4d0a1-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="4d0a1-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="4d0a1-527">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-527">yes</span></span>            | <span data-ttu-id="4d0a1-528">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-528">no</span></span>           |
| <span data-ttu-id="4d0a1-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="4d0a1-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="4d0a1-530">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-530">yes</span></span>            | <span data-ttu-id="4d0a1-531">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-531">no</span></span>           |
| <span data-ttu-id="4d0a1-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="4d0a1-533">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-533">yes</span></span>            | <span data-ttu-id="4d0a1-534">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-534">no</span></span>           |
| <span data-ttu-id="4d0a1-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="4d0a1-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="4d0a1-536">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-536">no</span></span>             | <span data-ttu-id="4d0a1-537">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-537">no</span></span>           |
| <span data-ttu-id="4d0a1-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="4d0a1-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="4d0a1-539">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-539">no</span></span>             | <span data-ttu-id="4d0a1-540">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-540">no</span></span>           |
| <span data-ttu-id="4d0a1-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="4d0a1-542">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-542">no</span></span>             | <span data-ttu-id="4d0a1-543">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-543">no</span></span>           |
| <span data-ttu-id="4d0a1-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="4d0a1-545">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-545">no</span></span>             | <span data-ttu-id="4d0a1-546">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-546">no</span></span>           |
| <span data-ttu-id="4d0a1-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="4d0a1-548">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-548">no</span></span>             | <span data-ttu-id="4d0a1-549">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-549">no</span></span>           |
| <span data-ttu-id="4d0a1-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="4d0a1-550">msdyn_duration</span></span>                         | <span data-ttu-id="4d0a1-551">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-551">no</span></span>             | <span data-ttu-id="4d0a1-552">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-552">no</span></span>           |
| <span data-ttu-id="4d0a1-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="4d0a1-553">msdyn_effort</span></span>                           | <span data-ttu-id="4d0a1-554">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-554">no</span></span>             | <span data-ttu-id="4d0a1-555">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-555">no</span></span>           |
| <span data-ttu-id="4d0a1-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="4d0a1-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="4d0a1-557">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-557">no</span></span>             | <span data-ttu-id="4d0a1-558">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-558">no</span></span>           |
| <span data-ttu-id="4d0a1-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4d0a1-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="4d0a1-560">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-560">no</span></span>             | <span data-ttu-id="4d0a1-561">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-561">no</span></span>           |
| <span data-ttu-id="4d0a1-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="4d0a1-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="4d0a1-563">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-563">no</span></span>             | <span data-ttu-id="4d0a1-564">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-564">no</span></span>           |
| <span data-ttu-id="4d0a1-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="4d0a1-565">msdyn_finish</span></span>                           | <span data-ttu-id="4d0a1-566">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-566">yes</span></span>            | <span data-ttu-id="4d0a1-567">da</span><span class="sxs-lookup"><span data-stu-id="4d0a1-567">yes</span></span>          |
| <span data-ttu-id="4d0a1-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="4d0a1-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="4d0a1-569">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-569">no</span></span>             | <span data-ttu-id="4d0a1-570">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-570">no</span></span>           |
| <span data-ttu-id="4d0a1-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="4d0a1-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="4d0a1-572">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-572">no</span></span>             | <span data-ttu-id="4d0a1-573">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-573">no</span></span>           |
| <span data-ttu-id="4d0a1-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="4d0a1-575">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-575">no</span></span>             | <span data-ttu-id="4d0a1-576">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-576">no</span></span>           |
| <span data-ttu-id="4d0a1-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="4d0a1-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="4d0a1-578">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-578">no</span></span>             | <span data-ttu-id="4d0a1-579">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-579">no</span></span>           |
| <span data-ttu-id="4d0a1-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="4d0a1-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="4d0a1-581">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-581">no</span></span>             | <span data-ttu-id="4d0a1-582">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-582">no</span></span>           |
| <span data-ttu-id="4d0a1-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="4d0a1-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="4d0a1-584">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-584">no</span></span>             | <span data-ttu-id="4d0a1-585">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-585">no</span></span>           |
| <span data-ttu-id="4d0a1-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="4d0a1-587">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-587">no</span></span>             | <span data-ttu-id="4d0a1-588">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-588">no</span></span>           |
| <span data-ttu-id="4d0a1-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="4d0a1-590">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-590">no</span></span>             | <span data-ttu-id="4d0a1-591">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-591">no</span></span>           |
| <span data-ttu-id="4d0a1-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="4d0a1-593">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-593">no</span></span>             | <span data-ttu-id="4d0a1-594">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-594">no</span></span>           |
| <span data-ttu-id="4d0a1-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="4d0a1-596">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-596">no</span></span>             | <span data-ttu-id="4d0a1-597">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-597">no</span></span>           |
| <span data-ttu-id="4d0a1-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="4d0a1-599">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-599">no</span></span>             | <span data-ttu-id="4d0a1-600">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-600">no</span></span>           |
| <span data-ttu-id="4d0a1-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="4d0a1-602">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-602">no</span></span>             | <span data-ttu-id="4d0a1-603">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-603">no</span></span>           |
| <span data-ttu-id="4d0a1-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="4d0a1-604">msdyn_progress</span></span>                         | <span data-ttu-id="4d0a1-605">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-605">no</span></span>             | <span data-ttu-id="4d0a1-606">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-606">no</span></span>           |
| <span data-ttu-id="4d0a1-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="4d0a1-608">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-608">no</span></span>             | <span data-ttu-id="4d0a1-609">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-609">no</span></span>           |
| <span data-ttu-id="4d0a1-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="4d0a1-611">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-611">no</span></span>             | <span data-ttu-id="4d0a1-612">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-612">no</span></span>           |
| <span data-ttu-id="4d0a1-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4d0a1-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="4d0a1-614">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-614">no</span></span>             | <span data-ttu-id="4d0a1-615">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-615">no</span></span>           |
| <span data-ttu-id="4d0a1-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="4d0a1-617">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-617">no</span></span>             | <span data-ttu-id="4d0a1-618">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-618">no</span></span>           |
| <span data-ttu-id="4d0a1-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="4d0a1-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="4d0a1-620">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-620">no</span></span>             | <span data-ttu-id="4d0a1-621">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-621">no</span></span>           |
| <span data-ttu-id="4d0a1-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="4d0a1-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="4d0a1-623">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-623">no</span></span>             | <span data-ttu-id="4d0a1-624">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-624">no</span></span>           |
| <span data-ttu-id="4d0a1-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="4d0a1-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="4d0a1-626">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-626">no</span></span>             | <span data-ttu-id="4d0a1-627">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-627">no</span></span>           |
| <span data-ttu-id="4d0a1-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="4d0a1-629">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-629">no</span></span>             | <span data-ttu-id="4d0a1-630">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-630">no</span></span>           |
| <span data-ttu-id="4d0a1-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="4d0a1-632">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-632">no</span></span>             | <span data-ttu-id="4d0a1-633">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-633">no</span></span>           |
| <span data-ttu-id="4d0a1-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="4d0a1-635">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-635">no</span></span>             | <span data-ttu-id="4d0a1-636">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-636">no</span></span>           |
| <span data-ttu-id="4d0a1-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="4d0a1-638">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-638">no</span></span>             | <span data-ttu-id="4d0a1-639">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-639">no</span></span>           |
| <span data-ttu-id="4d0a1-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="4d0a1-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="4d0a1-641">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-641">no</span></span>             | <span data-ttu-id="4d0a1-642">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-642">no</span></span>           |
| <span data-ttu-id="4d0a1-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="4d0a1-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="4d0a1-644">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-644">no</span></span>             | <span data-ttu-id="4d0a1-645">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-645">no</span></span>           |
| <span data-ttu-id="4d0a1-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="4d0a1-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="4d0a1-647">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-647">no</span></span>             | <span data-ttu-id="4d0a1-648">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-648">no</span></span>           |
| <span data-ttu-id="4d0a1-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="4d0a1-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="4d0a1-650">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-650">no</span></span>             | <span data-ttu-id="4d0a1-651">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-651">no</span></span>           |
| <span data-ttu-id="4d0a1-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="4d0a1-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="4d0a1-653">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-653">no</span></span>             | <span data-ttu-id="4d0a1-654">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-654">no</span></span>           |
| <span data-ttu-id="4d0a1-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="4d0a1-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="4d0a1-656">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-656">no</span></span>             | <span data-ttu-id="4d0a1-657">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-657">no</span></span>           |
| <span data-ttu-id="4d0a1-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="4d0a1-659">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-659">no</span></span>             | <span data-ttu-id="4d0a1-660">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-660">no</span></span>           |
| <span data-ttu-id="4d0a1-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="4d0a1-662">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-662">no</span></span>             | <span data-ttu-id="4d0a1-663">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-663">no</span></span>           |
| <span data-ttu-id="4d0a1-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="4d0a1-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="4d0a1-665">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-665">no</span></span>             | <span data-ttu-id="4d0a1-666">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-666">no</span></span>           |
| <span data-ttu-id="4d0a1-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="4d0a1-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="4d0a1-668">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-668">no</span></span>             | <span data-ttu-id="4d0a1-669">ne</span><span class="sxs-lookup"><span data-stu-id="4d0a1-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="4d0a1-670">Ograničenja i poznati problemi</span><span class="sxs-lookup"><span data-stu-id="4d0a1-670">Limitations and known issues</span></span>
<span data-ttu-id="4d0a1-671">Slijedi popis ograničenja i poznatih problema:</span><span class="sxs-lookup"><span data-stu-id="4d0a1-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="4d0a1-672">API-je rasporeda mogu upotrebljavati samo **Korisnici s licencom za Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="4d0a1-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="4d0a1-673">Ne mogu ih upotrebljavati:</span><span class="sxs-lookup"><span data-stu-id="4d0a1-673">They can't be used by:</span></span>
    - <span data-ttu-id="4d0a1-674">Korisnici aplikacije</span><span class="sxs-lookup"><span data-stu-id="4d0a1-674">Application users</span></span>
    - <span data-ttu-id="4d0a1-675">Korisnici sustava</span><span class="sxs-lookup"><span data-stu-id="4d0a1-675">System users</span></span>
    - <span data-ttu-id="4d0a1-676">Korisnici integracije</span><span class="sxs-lookup"><span data-stu-id="4d0a1-676">Integration users</span></span>
    - <span data-ttu-id="4d0a1-677">Ostali korisnici koji nemaju potrebnu licencu</span><span class="sxs-lookup"><span data-stu-id="4d0a1-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="4d0a1-678">Svaki **Skup operacija** može imati najviše 100 operacija.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="4d0a1-679">Svaki korisnik može imati najviše 10 otvorenih **Skupova operacija**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="4d0a1-680">Project Operations trenutačno podržava maksimalno 500 ukupnih zadataka na projektu.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="4d0a1-681">Stanje neuspjeha i dnevnici stanja značajke **Skup operacija** trenutačno nisu dostupni.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="4d0a1-682">Ograničenja i granice projekata i zadataka</span><span class="sxs-lookup"><span data-stu-id="4d0a1-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="4d0a1-683">Rukovanje pogreškama</span><span class="sxs-lookup"><span data-stu-id="4d0a1-683">Error handling</span></span>

   - <span data-ttu-id="4d0a1-684">Kako biste pregledali pogreške generirane iz skupova operacija, idite na **Postavke** \> **Raspored integracije** \> **Skupovi operacija**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="4d0a1-685">Kako biste pregledali pogreške generirane uslugom planiranja projekata, idite na **Postavke** \> **Raspored integracije** \> **Zapisnici pogrešaka PSS-a**.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="4d0a1-686">Primjer scenarija</span><span class="sxs-lookup"><span data-stu-id="4d0a1-686">Sample scenario</span></span>

<span data-ttu-id="4d0a1-687">U ovom ćete scenariju stvoriti projekt, člana tima, četiri zadatka i dvije dodjele resursa.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="4d0a1-688">Zatim ćete ažurirati jedan zadatak, ažurirati projekt, izbrisati jedan zadatak, izbrisati jednu dodjelu resursa i stvoriti ovisnost zadatka.</span><span class="sxs-lookup"><span data-stu-id="4d0a1-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="4d0a1-689">Dodatni primjeri</span><span class="sxs-lookup"><span data-stu-id="4d0a1-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
