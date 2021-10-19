---
title: Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja
description: U ovoj temi nalaze se informacije i primjeri za uporabu API-ja rasporeda projekta.
author: sigitac
ms.date: 09/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6be35b1c52996f4f94dc429974ef47343a027c8c
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487676"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_



## <a name="scheduling-entities"></a>Entiteti planiranja

API-ji rasporeda projekta pružaju mogućnost izvođenja operacija stvaranja, ažuriranja i brisanja s pomoću **Entiteta planiranja**. Tim se entitetima upravlja putem mehanizma za planiranje u aplikaciji Project for the Web. Operacije stvaranja, ažuriranja i brisanja s pomoću značajke **Entiteti planiranja** bile su ograničene u ranijim verzijama aplikacije Dynamics 365 Project Operations.

Sljedeća tablica pruža cjelovit popis entiteta rasporeda projekta.

| Naziv entiteta  | Logički naziv entiteta |
| --- | --- |
| Project | msdyn_project |
| Zadatak projekta  | msdyn_projecttask  |
| Ovisnost projektnog zadatka  | msdyn_projecttaskdependency  |
| Dodjela resursa | msdyn_resourceassignment |
| Grupa projekta  | msdyn_projectbucket |
| Članov projektnog tima | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet obrazac je jedinice rada koji se može upotrebljavati kada se u transakciji mora obraditi nekoliko zahtjeva koji utječu na raspored.

## <a name="project-schedule-apis"></a>API-ji rasporeda projekta

Slijedi popis trenutačnih API-ja rasporeda projekta.

- **msdyn_CreateProjectV1**: Ovaj se API može upotrebljavati za stvaranje projekta. Projekt i zadani skup projekata stvaraju se odmah.
- **msdyn_CreateTeamMemberV1**: Ovaj se API može upotrebljavati za stvaranje člana projektnog tima. Zapis člana tima stvara se odmah.
- **msdyn_CreateOperationSetV1**: Ovaj se API može upotrebljavati za raspored nekoliko zahtjeva koji se moraju izvršiti unutar transakcije.
- **msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za stvaranje entiteta. Entitet može biti svaki entitet rasporeda projekta koji podržava operaciju stvaranja.
- **msdyn_PSSCreateV1**: Ovaj se API može upotrebljavati za ažuriranje entiteta. Entitet može biti svaki entitet rasporeda projekta koji podržava operaciju ažuriranja.
- **msdyn_PSSDeleteV1**: Ovaj se API može upotrebljavati za brisanje entiteta. Entitet može biti svaki entitet rasporeda projekta koji podržava operaciju brisanja.
- **msdyn_ExecuteOperationSetV1**: Ovaj se API upotrebljava za izvršavanje svih operacija unutar zadanog skupa operacija.

## <a name="using-project-schedule-apis-with-operationset"></a>Uporaba API-ja rasporeda projekta s pomoću OperationSet

Kako se oba zapisa, i **CreateProjectV1** i **reateTeamMemberV1**, stvaraju odmah, ti se API-ji ne mogu izravno upotrebljavati u značajci **Skup operacija**. Međutim, možete upotrebljavati API za stvaranje potrebnih zapisa, stvaranje značajke **Skup operacija**, a zatim upotrijebite ove unaprijed stvorene zapise u značajci **Skup operacija**.

## <a name="supported-operations"></a>Podržane operacije

| Entitet planiranja | Stvaranje | Ažuriranje | Izbriši | Važne stavke |
| --- | --- | --- | --- | --- |
Projektni zadatak | Jest | Jest | Jest | Nijedno |
| Ovisnost projektnog zadatka | Jest | Jest | | Zapisi ovisnosti projektnog zadatka ne ažuriraju se. Umjesto toga, može se izbrisati stari zapis i stvoriti novi. |
| Dodjela resursa | Jest | Jest | | Nisu podržane operacije sa sljedećim poljima: **ID resursa koji se može rezervirati**, **Rad**, **Rad dovršen**, **Preostali rad** i **Planirani rad**. Zapisi o dodjeli resursa ne ažuriraju se. Umjesto toga, može se izbrisati stari zapis i stvoriti novi. |
| Grupa projekata | Nije dostupno | Nije dostupno | Nije dostupno | Zadana grupa kreira se s pomoću API-ja **CreateProjectV1**. |
| Član projektnog tima | Jest | Jest | Jest | Za operaciju stvaranja upotrijebite API **CreateTeamMemberV1**. |
| Project | Jest | Jest | Nije dostupno | Nisu podržane operacije sa sljedećim poljima: **Šifra države**, **Stanje skupnog generiranja**, **Token globalne revizije**, **ID kalendara**, **Rad**, **Rad dovršen**, **Preostali rad**, **Napredak**, **Završi**, **Najraniji početak zadatka** i **Trajanje**. |

Ti se API-ji mogu pozivati s pomoću objekata entiteta koji uključuju prilagođena polja.

Svojstvo ID-a nije obvezno. Ako je omogućeno, sustav ga pokušava upotrijebiti i izbacuje iznimku ako se ne može upotrebljavati. Ako nije navedeno, sustav će ga generirati.

## <a name="restricted-fields"></a>Ograničena polja

Sljedeće tablice definiraju polja koja su ograničena za **Stvaranje** i **Uređivanje.**

### <a name="project-task"></a>Projektni zadatak

| **Logički naziv**                       | **Može se stvoriti** | **Može se uređivati**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ne             | ne               |
| msdyn_actualcost_base                  | ne             | ne               |
| msdyn_actualend                        | ne             | ne               |
| msdyn_actualsales                      | ne             | ne               |
| msdyn_actualsales_base                 | ne             | ne               |
| msdyn_actualstart                      | ne             | ne               |
| msdyn_costatcompleteestimate           | ne             | ne               |
| msdyn_costatcompleteestimate_base      | ne             | ne               |
| msdyn_costconsumptionpercentage        | ne             | ne               |
| msdyn_effortcompleted                  | ne             | ne               |
| msdyn_effortestimateatcomplete         | ne             | ne               |
| msdyn_iscritical                       | ne             | ne               |
| msdyn_iscriticalname                   | ne             | ne               |
| msdyn_ismanual                         | ne             | ne               |
| msdyn_ismanualname                     | ne             | ne               |
| msdyn_ismilestone                      | ne             | ne               |
| msdyn_ismilestonename                  | ne             | ne               |
| msdyn_LinkStatus                       | ne             | ne               |
| msdyn_linkstatusname                   | ne             | ne               |
| msdyn_msprojectclientid                | ne             | ne               |
| msdyn_plannedcost                      | ne             | ne               |
| msdyn_plannedcost_base                 | ne             | ne               |
| msdyn_plannedsales                     | ne             | ne               |
| msdyn_plannedsales_base                | ne             | ne               |
| msdyn_pluginprocessingdata             | ne             | ne               |
| msdyn_progress                         | ne             | ne (da za P4W) |
| msdyn_remainingcost                    | ne             | ne               |
| msdyn_remainingcost_base               | ne             | ne               |
| msdyn_remainingsales                   | ne             | ne               |
| msdyn_remainingsales_base              | ne             | ne               |
| msdyn_requestedhours                   | ne             | ne               |
| msdyn_resourcecategory                 | ne             | ne               |
| msdyn_resourcecategoryname             | ne             | ne               |
| msdyn_resourceorganizationalunitid     | ne             | ne               |
| msdyn_resourceorganizationalunitidname | ne             | ne               |
| msdyn_salesconsumptionpercentage       | ne             | ne               |
| msdyn_salesestimateatcomplete          | ne             | ne               |
| msdyn_salesestimateatcomplete_base     | ne             | ne               |
| msdyn_salesvariance                    | ne             | ne               |
| msdyn_salesvariance_base               | ne             | ne               |
| msdyn_scheduleddurationminutes         | ne             | ne               |
| msdyn_scheduledend                     | ne             | ne               |
| msdyn_scheduledstart                   | ne             | ne               |
| msdyn_schedulevariance                 | ne             | ne               |
| msdyn_skipupdateestimateline           | ne             | ne               |
| msdyn_skipupdateestimatelinename       | ne             | ne               |
| msdyn_summary                          | ne             | ne               |
| msdyn_varianceofcost                   | ne             | ne               |
| msdyn_varianceofcost_base              | ne             | ne               |

### <a name="project-task-dependency"></a>Ovisnost projektnog zadatka

| **Logički naziv**              | **Može se stvoriti** | **Može se uređivati** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ne             | ne           |
| msdyn_linktypename            | ne             | ne           |
| msdyn_predecessortask         | da            | ne           |
| msdyn_predecessortaskname     | da            | ne           |
| msdyn_project                 | da            | ne           |
| msdyn_projectname             | da            | ne           |
| msdyn_projecttaskdependencyid | da            | ne           |
| msdyn_successortask           | da            | ne           |
| msdyn_successortaskname       | da            | ne           |

### <a name="resource-assignment"></a>Dodjela resursa

| **Logički naziv**             | **Može se stvoriti** | **Može se uređivati** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | da            | ne           |
| msdyn_bookableresourceidname | da            | ne           |
| msdyn_bookingstatusid        | ne             | ne           |
| msdyn_bookingstatusidname    | ne             | ne           |
| msdyn_committype             | ne             | ne           |
| msdyn_committypename         | ne             | ne           |
| msdyn_effort                 | ne             | ne           |
| msdyn_effortcompleted        | ne             | ne           |
| msdyn_effortremaining        | ne             | ne           |
| msdyn_finish                 | ne             | ne           |
| msdyn_plannedcost            | ne             | ne           |
| msdyn_plannedcost_base       | ne             | ne           |
| msdyn_plannedcostcontour     | ne             | ne           |
| msdyn_plannedsales           | ne             | ne           |
| msdyn_plannedsales_base      | ne             | ne           |
| msdyn_plannedsalescontour    | ne             | ne           |
| msdyn_plannedwork            | ne             | ne           |
| msdyn_projectid              | da            | ne           |
| msdyn_projectidname          | ne             | ne           |
| msdyn_projectteamid          | ne             | ne           |
| msdyn_projectteamidname      | ne             | ne           |
| msdyn_start                  | ne             | ne           |
| msdyn_taskid                 | ne             | ne           |
| msdyn_taskidname             | ne             | ne           |
| msdyn_userresourceid         | ne             | ne           |

### <a name="project-team-member"></a>Član projektnog tima

| **Logički naziv**                                 | **Može se stvoriti** | **Može se uređivati** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ne             | ne           |
| msdyn_creategenericteammemberwithrequirementname | ne             | ne           |
| msdyn_deletestatus                               | ne             | ne           |
| msdyn_deletestatusname                           | ne             | ne           |
| msdyn_effort                                     | ne             | ne           |
| msdyn_effortcompleted                            | ne             | ne           |
| msdyn_effortremaining                            | ne             | ne           |
| msdyn_finish                                     | ne             | ne           |
| msdyn_hardbookedhours                            | ne             | ne           |
| msdyn_hours                                      | ne             | ne           |
| msdyn_markedfordeletiontimer                     | ne             | ne           |
| msdyn_markedfordeletiontimestamp                 | ne             | ne           |
| msdyn_msprojectclientid                          | ne             | ne           |
| msdyn_percentage                                 | ne             | ne           |
| msdyn_requiredhours                              | ne             | ne           |
| msdyn_softbookedhours                            | ne             | ne           |
| msdyn_start                                      | ne             | ne           |

### <a name="project"></a>Project

| **Logički naziv**                       | **Može se stvoriti** | **Može se uređivati** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ne             | ne           |
| msdyn_actualexpensecost_base           | ne             | ne           |
| msdyn_actuallaborcost                  | ne             | ne           |
| msdyn_actuallaborcost_base             | ne             | ne           |
| msdyn_actualsales                      | ne             | ne           |
| msdyn_actualsales_base                 | ne             | ne           |
| msdyn_contractlineproject              | da            | ne           |
| msdyn_contractorganizationalunitid     | da            | ne           |
| msdyn_contractorganizationalunitidname | da            | ne           |
| msdyn_costconsumption                  | ne             | ne           |
| msdyn_costestimateatcomplete           | ne             | ne           |
| msdyn_costestimateatcomplete_base      | ne             | ne           |
| msdyn_costvariance                     | ne             | ne           |
| msdyn_costvariance_base                | ne             | ne           |
| msdyn_duration                         | ne             | ne           |
| msdyn_effort                           | ne             | ne           |
| msdyn_effortcompleted                  | ne             | ne           |
| msdyn_effortestimateatcompleteeac      | ne             | ne           |
| msdyn_effortremaining                  | ne             | ne           |
| msdyn_finish                           | da            | da          |
| msdyn_globalrevisiontoken              | ne             | ne           |
| msdyn_islinkedtomsprojectclient        | ne             | ne           |
| msdyn_islinkedtomsprojectclientname    | ne             | ne           |
| msdyn_linkeddocumenturl                | ne             | ne           |
| msdyn_msprojectdocument                | ne             | ne           |
| msdyn_msprojectdocumentname            | ne             | ne           |
| msdyn_plannedexpensecost               | ne             | ne           |
| msdyn_plannedexpensecost_base          | ne             | ne           |
| msdyn_plannedlaborcost                 | ne             | ne           |
| msdyn_plannedlaborcost_base            | ne             | ne           |
| msdyn_plannedsales                     | ne             | ne           |
| msdyn_plannedsales_base                | ne             | ne           |
| msdyn_progress                         | ne             | ne           |
| msdyn_remainingcost                    | ne             | ne           |
| msdyn_remainingcost_base               | ne             | ne           |
| msdyn_remainingsales                   | ne             | ne           |
| msdyn_remainingsales_base              | ne             | ne           |
| msdyn_replaylogheader                  | ne             | ne           |
| msdyn_salesconsumption                 | ne             | ne           |
| msdyn_salesestimateatcompleteeac       | ne             | ne           |
| msdyn_salesestimateatcompleteeac_base  | ne             | ne           |
| msdyn_salesvariance                    | ne             | ne           |
| msdyn_salesvariance_base               | ne             | ne           |
| msdyn_scheduleperformance              | ne             | ne           |
| msdyn_scheduleperformancename          | ne             | ne           |
| msdyn_schedulevariance                 | ne             | ne           |
| msdyn_taskearlieststart                | ne             | ne           |
| msdyn_teamsize                         | ne             | ne           |
| msdyn_teamsize_date                    | ne             | ne           |
| msdyn_teamsize_state                   | ne             | ne           |
| msdyn_totalactualcost                  | ne             | ne           |
| msdyn_totalactualcost_base             | ne             | ne           |
| msdyn_totalplannedcost                 | ne             | ne           |
| msdyn_totalplannedcost_base            | ne             | ne           |


## <a name="limitations-and-known-issues"></a>Ograničenja i poznati problemi
Slijedi popis ograničenja i poznatih problema:

- API-je rasporeda projekta mogu upotrebljavati samo **Korisnici s licencom za aplikaciju Microsoft Project.** Ne mogu ih upotrebljavati:
    - Korisnici aplikacije
    - Korisnici sustava
    - Korisnici integracije
    - Ostali korisnici koji nemaju potrebnu licencu
- Svaki **Skup operacija** može imati najviše 100 operacija.
- Svaki korisnik može imati najviše 10 otvorenih **Skupova operacija**.
- Project Operations trenutačno podržava maksimalno 500 ukupnih zadataka na projektu.
- Stanje neuspjeha i dnevnici stanja značajke **Skup operacija** trenutačno nisu dostupni.
- [Ograničenja i granice projekata i zadataka](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Rukovanje pogreškama

   - Kako biste pregledali pogreške generirane iz skupova operacija, idite na **Postavke** \> **Raspored integracije** \> **Skupovi operacija**.
   - Kako biste pregledali pogreške generirane iz Usluge rasporeda projekta, idite na **Postavke** \> **Integracija rasporeda** \> **Dnevnici pogrešaka PSS-a**.

## <a name="sample-scenario"></a>Primjer scenarija

U ovom ćete scenariju stvoriti projekt, člana tima, četiri zadatka i dvije dodjele resursa. Zatim ćete ažurirati jedan zadatak, ažurirati projekt, izbrisati jedan zadatak, izbrisati jednu dodjelu resursa i stvoriti ovisnost zadatka.

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

## <a name="additional-samples"></a>Dodatni primjeri

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
