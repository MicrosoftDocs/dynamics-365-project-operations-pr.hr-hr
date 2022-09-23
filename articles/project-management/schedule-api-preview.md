---
title: Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja
description: U ovom se članku navode informacije i uzorci za korištenje API-ja za raspored projekta.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: hr-HR
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541115"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Uporaba API-ja rasporeda projekta za izvođenje operacija s entitetima planiranja

_**Odnosi se na:** Project Operations za scenarije temeljene na resursima / bez zaliha, jednostavna implementacija – poslovanje putem predračuna_


**Entiteti planiranja**

API-ji rasporeda projekta pružaju mogućnost izvođenja operacija stvaranja, ažuriranja i brisanja s pomoću **Entiteta planiranja**. Tim se entitetima upravlja putem mehanizma za planiranje u aplikaciji Project for the Web. Operacije stvaranja, ažuriranja i brisanja s pomoću značajke **Entiteti planiranja** bile su ograničene u ranijim verzijama aplikacije Dynamics 365 Project Operations.

Sljedeća tablica pruža cjelovit popis entiteta rasporeda projekta.

| **Naziv entiteta**         | **Logički naziv entiteta**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Zadatak projekta            | msdyn_projecttask           |
| Ovisnost projektnog zadatka | msdyn_projecttaskdependency |
| Dodjela resursa     | msdyn_resourceassignment    |
| Grupa projekta          | msdyn_projectbucket         |
| Članov projektnog tima     | msdyn_projectteam           |
| Popisi za provjeru projekta      | msdyn_projectchecklist      |
| Oznaka projekta           | msdyn_projectlabel          |
| Projektni zadatak za označavanje   | msdyn_projecttasktolabel    |
| Sprint projekta          | msdyn_projectsprint         |

**OperationSet**

OperationSet obrazac je jedinice rada koji se može upotrebljavati kada se u transakciji mora obraditi nekoliko zahtjeva koji utječu na raspored.

**API-ji rasporeda projekta**

Slijedi popis trenutačnih API-ja rasporeda projekta.

| **Api**                                 | Opis                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Ovaj se API koristi za stvaranje projekta. Projekt i zadana grupa projekta stvaraju se odmah.                         |
| **msdyn_CreateTeamMemberV1**            | Ovaj API koristi se za stvaranje člana projektnog tima. Zapis člana tima stvara se odmah.                                  |
| **msdyn_CreateOperationSetV1**          | Ovaj se API koristi za zakazivanje nekoliko zahtjeva koji se moraju izvršiti unutar transakcije.                                        |
| **msdyn_PssCreateV1**                   | Ovaj API koristi se za stvaranje entiteta. Entitet može biti svaki entitet rasporeda projekta koji podržava operaciju stvaranja. |
| **msdyn_PssUpdateV1**                   | Ovaj API koristi se za ažuriranje entiteta. Entitet može biti bilo koji entitet za raspoređivanje projekata koji podržava operaciju ažuriranja  |
| **msdyn_PssDeleteV1**                   | Ovaj API koristi se za brisanje entiteta. Entitet može biti svaki entitet rasporeda projekta koji podržava operaciju brisanja. |
| **msdyn_ExecuteOperationSetV1**         | Ovaj se API koristi za izvršavanje svih operacija unutar zadanog skupa operacija.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Ovaj se API koristi za ažuriranje planirane radne konture dodjele resursa.                                                        |



**Uporaba API-ja rasporeda projekta s pomoću OperationSet**

Kako se oba zapisa, i **CreateProjectV1** i **reateTeamMemberV1**, stvaraju odmah, ti se API-ji ne mogu izravno upotrebljavati u značajci **Skup operacija**. Međutim, možete upotrebljavati API za stvaranje potrebnih zapisa, stvaranje značajke **Skup operacija**, a zatim upotrijebite ove unaprijed stvorene zapise u značajci **Skup operacija**.

**Podržane operacije**

| **Entitet planiranja**   | **Stvaranje** | **Ažuriranje** | **Izbriši** | **Važne stavke**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektni zadatak            | Jest        | Jest        | Jest        | Polja **Progress**, **EffortCompleted** i **EffortRemaining** mogu se uređivati u programu Project za web, ali se ne mogu uređivati u operacijama projekta.                                                                                                                                                                                             |
| Ovisnost projektnog zadatka | Jest        | No         | Jest        | Zapisi ovisnosti projektnog zadatka ne ažuriraju se. Umjesto toga, stari zapis se može izbrisati i stvoriti novi zapis.                                                                                                                                                                                                                                 |
| Dodjela resursa     | Jest        | Jest\*      | Jest        | Nisu podržane operacije sa sljedećim poljima: **ID resursa koji se može rezervirati**, **Rad**, **Rad dovršen**, **Preostali rad** i **Planirani rad**. Zapisi o dodjeli resursa ne ažuriraju se. Umjesto toga, stari zapis se može izbrisati i stvoriti novi zapis. Izdan je poseban API za ažuriranje kontura dodjele resursa. |
| Grupa projekata          | Jest        | Jest        | Jest        | Zadana grupa stvara se pomoću API-ja **CreateProjectV1**. Podrška za stvaranje i brisanje projektnih grupa dodana je u Update Release 16.                                                                                                                                                                                                   |
| Član projektnog tima     | Jest        | Jest        | Jest        | Za operaciju stvaranja upotrijebite API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Jest        | Jest        |            | Nisu podržane operacije sa sljedećim poljima: **Šifra države**, **Stanje skupnog generiranja**, **Token globalne revizije**, **ID kalendara**, **Rad**, **Rad dovršen**, **Preostali rad**, **Napredak**, **Završi**, **Najraniji početak zadatka** i **Trajanje**.                                                                                       |
| Popisi za provjeru projekta      | Jest        | Jest        | Jest        |                                                                                                                                                                                                                                                                                                                                                         |
| Oznaka projekta           | No         | Jest        | No         | Nazivi naljepnica mogu se mijenjati. Ova je značajka dostupna samo za Project za Web                                                                                                                                                                                                                                                                      |
| Projektni zadatak za označavanje   | Jest        | No         | Jest        | Ova je značajka dostupna samo za Project za Web                                                                                                                                                                                                                                                                                                  |
| Sprint projekta          | Jest        | Jest        | Jest        | Polje **Start** mora imati datum raniji **od polja Završi**. Sprintevi za isti projekt ne mogu se međusobno preklapati. Ova je značajka dostupna samo za Project za Web                                                                                                                                                                    |




Svojstvo ID-a nije obvezno. Ako je omogućeno, sustav ga pokušava upotrijebiti i izbacuje iznimku ako se ne može upotrebljavati. Ako nije navedeno, sustav će ga generirati.

**Ograničenja i poznati problemi**

Slijedi popis ograničenja i poznatih problema:

-   API-je za planiranje projekta mogu koristiti samo korisnici s licencom **za** Microsoft Project. Ne mogu ih upotrebljavati:
    -   Korisnici aplikacije
    -   Korisnici sustava
    -   Korisnici integracije
    -   Ostali korisnici koji nemaju potrebnu licencu
-   Svaki **Skup operacija** može imati najviše 100 operacija.
-   Svaki korisnik može imati najviše 10 otvorenih **Skupova operacija**.
-   Project Operations trenutačno podržava maksimalno 500 ukupnih zadataka na projektu.
-   Svaka operacija konture dodjele resursa ažuriranja računa se kao jedna operacija.
-   Svaki popis ažuriranih kontura može sadržavati najviše 100 vremenskih isječaka.
-   Stanje neuspjeha i dnevnici stanja značajke **Skup operacija** trenutačno nisu dostupni.
-   Postoji najviše 400 sprinteva po projektu.
-   [Ograničenja i granice projekata i zadataka](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Oznake su trenutno dostupne samo za Project za Web.

**Rukovanje pogreškama**

-   Kako biste pregledali pogreške generirane iz skupova operacija, idite na **Postavke** \> **Raspored integracije** \> **Skupovi operacija**.
-   Kako biste pregledali pogreške generirane iz Usluge rasporeda projekta, idite na **Postavke** \> **Integracija rasporeda** \> **Dnevnici pogrešaka PSS-a**.

**Uređivanje kontura dodjele resursa**

Za razliku od svih ostalih API-ja za planiranje projekata koji ažuriraju entitet, API konture dodjele resursa odgovoran je isključivo za ažuriranja jednog polja, msdyn_plannedwork, na jednom entitetu, msydn_resourceassignment.

Zadani način rasporeda je:

-   **fiksne jedinice**
-   Kalendar projekta je 9-5p je 9-5pst, pon, uto, čet, petak (NEMA RADA SRIJEDOM)
-   A kalendar resursa je 9-1p PST pon do pet

Ovaj zadatak je za tjedan dana, četiri sata dnevno. To je zato što je kalendar resursa od 9-1 PST ili četiri sata dnevno.

| &nbsp;     | Zadatak | Datum početka | Datum završetka  | Količina | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 radnik |  T1  | 6/13/2022  | 6/17/2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Na primjer, ako želite da radnik radi samo tri sata svaki dan ovaj tjedan i dopusti jedan sat za druge zadatke.

#### <a name="updatedcontours-sample-payload"></a>Korisni teret uzorka UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Ovo je zadatak nakon pokretanja API-ja rasporeda konture ažuriranja.

| &nbsp;     | Zadatak | Datum početka | Datum završetka  | Količina | 6/13/2022 | 6/14/2022 | 6/15/2022 | 6/16/2022 | 6/17/2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 radnik | T1   | 6/13/2022  | 6/17/2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Primjer scenarija**

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

** Dodatni uzorci

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
