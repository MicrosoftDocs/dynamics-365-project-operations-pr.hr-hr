---
title: Promjene upravljanja resursima (Project Service Automation 3.x)
description: Ovaj tema sadrži informacije o promjenama u području upravljanja resursima.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750142"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="42ac1-103">Promjene upravljanja resursima (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="42ac1-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="42ac1-104">Odjeljci ove teme sadrže informacije o promjenama koje su uvedene u području upravljanja resursima verzije 3.x aplikacije Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="42ac1-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="42ac1-105">Procjene projekta</span><span class="sxs-lookup"><span data-stu-id="42ac1-105">Project estimates</span></span>

<span data-ttu-id="42ac1-106">Umjesto entiteta **msdyn\_projecttask** (**Projektni zadatak**), procjene projekta temelje se na entitetu **msdyn\_resourceassignment** (**Dodjela resursa**).</span><span class="sxs-lookup"><span data-stu-id="42ac1-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="42ac1-107">Dodjele resursa postale su "izvor podataka" za planiranje zadataka i određivanje cijena.</span><span class="sxs-lookup"><span data-stu-id="42ac1-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="42ac1-108">Zadaci retka</span><span class="sxs-lookup"><span data-stu-id="42ac1-108">Line tasks</span></span>

<span data-ttu-id="42ac1-109">U aplikaciji PSA 3.x zadaci retka su zastarjeli (obustavljeni).</span><span class="sxs-lookup"><span data-stu-id="42ac1-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="42ac1-110">Dodjele više ne ukazuju na zadatke retka, već na cijeli zadatak.</span><span class="sxs-lookup"><span data-stu-id="42ac1-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="42ac1-111">Primjer u nastavku pokazuje kako se zadatak koji se zove "Probni zadatak" dodjeljuje članovima tima A i B u ranijim verzijama aplikacije PSA i u aplikaciji PSA 3. x.</span><span class="sxs-lookup"><span data-stu-id="42ac1-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="42ac1-112">**Prije PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="42ac1-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="42ac1-113">Probni zadatak</span><span class="sxs-lookup"><span data-stu-id="42ac1-113">Test task</span></span>

        - <span data-ttu-id="42ac1-114">Probni zadatak – zadatak retka 1</span><span class="sxs-lookup"><span data-stu-id="42ac1-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="42ac1-115">Dodjela u tim A</span><span class="sxs-lookup"><span data-stu-id="42ac1-115">Assignment to A</span></span>

        - <span data-ttu-id="42ac1-116">Probni zadatak – zadatak retka 2</span><span class="sxs-lookup"><span data-stu-id="42ac1-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="42ac1-117">Dodjela u tim B</span><span class="sxs-lookup"><span data-stu-id="42ac1-117">Assignment to B</span></span>

- <span data-ttu-id="42ac1-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="42ac1-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="42ac1-119">Probni zadatak</span><span class="sxs-lookup"><span data-stu-id="42ac1-119">Test task</span></span>

        - <span data-ttu-id="42ac1-120">Dodjela u tim A</span><span class="sxs-lookup"><span data-stu-id="42ac1-120">Assignment to A</span></span>
        - <span data-ttu-id="42ac1-121">Dodjela u tim B</span><span class="sxs-lookup"><span data-stu-id="42ac1-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="42ac1-122">Nedodijeljena dodjela</span><span class="sxs-lookup"><span data-stu-id="42ac1-122">Unassigned assignment</span></span>

<span data-ttu-id="42ac1-123">U aplikaciji PSA 3. x nedodijeljena dodjela je dodjela koja je dodijeljena članu tima **NULL** i resursu **NULL**.</span><span class="sxs-lookup"><span data-stu-id="42ac1-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="42ac1-124">Nedodijeljene dodjele mogu se pojaviti u nekoliko scenarija:</span><span class="sxs-lookup"><span data-stu-id="42ac1-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="42ac1-125">Ako je zadatak izrađen, ali još nije dodijeljen članu tima, uvijek se stvara nedodijeljena dodjela.</span><span class="sxs-lookup"><span data-stu-id="42ac1-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="42ac1-126">Ako se uklone svi primatelji u zadatku, za taj zadatak će se ponovno izraditi nedodijeljena dodjela.</span><span class="sxs-lookup"><span data-stu-id="42ac1-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="42ac1-127">Polja rasporeda u entitetu Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="42ac1-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="42ac1-128">Polja u entitetu **msdyn\_projecttask** obustavljena su ili premještena u entitet **msdyn\_resourceassignment** ili su sada povezana referencom iz entiteta **msdyn\_projectteam** (**Član projektnog tima**).</span><span class="sxs-lookup"><span data-stu-id="42ac1-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="42ac1-129">Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="42ac1-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="42ac1-130">Novo polje u entitetu msdyn\_resourceassignment (Dodjela resursa)</span><span class="sxs-lookup"><span data-stu-id="42ac1-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="42ac1-131">Komentar</span><span class="sxs-lookup"><span data-stu-id="42ac1-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="42ac1-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="42ac1-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="42ac1-133">Nema</span><span class="sxs-lookup"><span data-stu-id="42ac1-133">None</span></span> | |
| <span data-ttu-id="42ac1-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="42ac1-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="42ac1-135">Nema</span><span class="sxs-lookup"><span data-stu-id="42ac1-135">None</span></span> | |
| <span data-ttu-id="42ac1-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="42ac1-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="42ac1-137">Nema</span><span class="sxs-lookup"><span data-stu-id="42ac1-137">None</span></span> | |
| <span data-ttu-id="42ac1-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="42ac1-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="42ac1-139">Nema</span><span class="sxs-lookup"><span data-stu-id="42ac1-139">None</span></span> | |
| <span data-ttu-id="42ac1-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="42ac1-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="42ac1-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="42ac1-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="42ac1-142">Promijenjen je format podatkovne strukture JavaScript Object Notation (JSON) koja je spremljena u polju.</span><span class="sxs-lookup"><span data-stu-id="42ac1-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="42ac1-143">Kontura rasporeda</span><span class="sxs-lookup"><span data-stu-id="42ac1-143">Schedule contour</span></span>

<span data-ttu-id="42ac1-144">Kontura rasporeda spremljena je u polju **Planirani rad** (**msdyn\_plannedwork**) svakog entiteta **Dodjela resursa** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="42ac1-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="42ac1-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="42ac1-145">Structure</span></span>

<span data-ttu-id="42ac1-146">Nova struktura konture rasporeda sastoji se od fleksibilnih isječaka vremena definiranih za svaki dan u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="42ac1-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="42ac1-147">Svaki isječak vremena ima sljedeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="42ac1-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="42ac1-148">**Početak** – početak radnog vremena na određeni dan, prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="42ac1-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="42ac1-149">**Kraj** – kraj radnog vremena na određeni dan, prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="42ac1-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="42ac1-150">**Sati** – broj sati koji su dodijeljeni određeni dan.</span><span class="sxs-lookup"><span data-stu-id="42ac1-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="42ac1-151">**Primjer**</span><span class="sxs-lookup"><span data-stu-id="42ac1-151">**Example**</span></span>

<span data-ttu-id="42ac1-152">Za ovaj se primjer koristi kalendar projekta u kojem je radni dan od 9:00 do 17:00 u vremenskoj zoni UTC-8.</span><span class="sxs-lookup"><span data-stu-id="42ac1-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="42ac1-153">Automatsko zakazivanje i ručno zakazivanje</span><span class="sxs-lookup"><span data-stu-id="42ac1-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="42ac1-154">Ako je zadatak automatski zakazan, sati su unaprijed učitani, a trajanje zadatka može se skratiti.</span><span class="sxs-lookup"><span data-stu-id="42ac1-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="42ac1-155">**Primjer**</span><span class="sxs-lookup"><span data-stu-id="42ac1-155">**Example**</span></span>

<span data-ttu-id="42ac1-156">Sljedeći zadatak automatski je zakazan na 18 sati tijekom tri dana (od 3. do 5. prosinca 2018.).</span><span class="sxs-lookup"><span data-stu-id="42ac1-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="42ac1-157">Ako je zadatak ručno zakazan, sati su ravnomjerno raspoređeni po svim danima.</span><span class="sxs-lookup"><span data-stu-id="42ac1-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="42ac1-158">**Primjer**</span><span class="sxs-lookup"><span data-stu-id="42ac1-158">**Example**</span></span>

<span data-ttu-id="42ac1-159">Sljedeći zadatak ručno je zakazan na 18 sati tijekom tri dana (od 3. do 5. prosinca 2018.).</span><span class="sxs-lookup"><span data-stu-id="42ac1-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="42ac1-160">Jedinica dodjele</span><span class="sxs-lookup"><span data-stu-id="42ac1-160">Assignment unit</span></span>

<span data-ttu-id="42ac1-161">Jedinica dodjele je obustavljena je u aplikaciji PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="42ac1-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="42ac1-162">Sati rada za zadatak sada su podjednako podijeljeni po danu među svim dodijeljenim resursima.</span><span class="sxs-lookup"><span data-stu-id="42ac1-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="42ac1-163">**Primjer**</span><span class="sxs-lookup"><span data-stu-id="42ac1-163">**Example**</span></span>

<span data-ttu-id="42ac1-164">U ovom primjeru zadatak je dodijeljen dvama resursima i automatski je zakazan na 36 sati tijekom tri dana (od 3. do 5. prosinca 2018.).</span><span class="sxs-lookup"><span data-stu-id="42ac1-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="42ac1-165">Dodjela 1:</span><span class="sxs-lookup"><span data-stu-id="42ac1-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="42ac1-166">Dodjela 2:</span><span class="sxs-lookup"><span data-stu-id="42ac1-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="42ac1-167">Dimenzije cijena</span><span class="sxs-lookup"><span data-stu-id="42ac1-167">Pricing dimensions</span></span>

<span data-ttu-id="42ac1-168">U aplikaciji PSA 3.x polja dimenzija cijena prema resursu (kao što su **Uloga** i **Organizacijska jedinica**) uklonjena su iz entiteta **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="42ac1-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="42ac1-169">Ta se polja sada mogu dohvatiti iz odgovarajućeg člana projektnog tima **(msdyn\_projectteam**) dodjele resursa (**msdyn\_resourceassignment**) kad se generiraju procjene projekta.</span><span class="sxs-lookup"><span data-stu-id="42ac1-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="42ac1-170">Novo polje **, msdyn\_organizationalunit**, dodano je u entitet **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="42ac1-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="42ac1-171">Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="42ac1-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="42ac1-172">Polje iz entiteta msdyn\_projectteam (Član projektnog tima) koje se upotrebljava umjesto njega</span><span class="sxs-lookup"><span data-stu-id="42ac1-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="42ac1-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="42ac1-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="42ac1-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="42ac1-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="42ac1-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="42ac1-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="42ac1-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="42ac1-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="42ac1-177">Konture</span><span class="sxs-lookup"><span data-stu-id="42ac1-177">Contours</span></span>

<span data-ttu-id="42ac1-178">Polja konture cijena i procjene obustavljena su u entitetu **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="42ac1-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="42ac1-179">Premještena su u entitet **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="42ac1-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="42ac1-180">Obustavljeno polje u entitetu msdyn\_projektnom zadatku (Projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="42ac1-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="42ac1-181">Novo polje u entitetu msdyn\_resourceassignment (Dodjela resursa)</span><span class="sxs-lookup"><span data-stu-id="42ac1-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="42ac1-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="42ac1-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="42ac1-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="42ac1-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="42ac1-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="42ac1-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="42ac1-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="42ac1-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="42ac1-186">Polja u nastavku dodana su u entitet **msdyn.\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="42ac1-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="42ac1-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="42ac1-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="42ac1-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="42ac1-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="42ac1-189">Sljedeća polja za planirani, stvarni i preostali trošak i prodaju ostaju ista u entitetu **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="42ac1-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="42ac1-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="42ac1-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="42ac1-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="42ac1-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="42ac1-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="42ac1-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="42ac1-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="42ac1-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="42ac1-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="42ac1-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="42ac1-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="42ac1-195">msdyn\_remainingsales</span></span>
