---
title: Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja
description: Ovaj članak pruža informacije i primere za korišćenje API-ja rasporeda projekata.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541142"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_


**Entiteti planiranja**

API-ji za raspored projekata pružaju mogućnost izvršavanja operacija kreiranja, ažuriranja i brisanja pomoću **entiteta za zakazivanje**. Tim entitetima se upravlja putem mehanizma za raspoređivanje u aplikaciji Project za veb. Kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja** bili su ograničeni u ranijim izdanjima usluge Dynamics 365 Project Operations.

Sledeća tabela daje potpunu listu entiteta za raspored projekata.

| **Ime entiteta**         | **Logičko ime entiteta**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektni zadatak            | msdyn_projecttask           |
| Zavisnost projektnog zadatka | msdyn_projecttaskdependency |
| Dodela resursa     | msdyn_resourceassignment    |
| Kontejner projekta          | msdyn_projectbucket         |
| Član projektnog tima     | msdyn_projectteam           |
| Liste za proveru projekta      | msdyn_projectchecklist      |
| Oznaka projekta           | msdyn_projectlabel          |
| Zavisnost projektnog zadataka i oznake   | msdyn_projecttasktolabel    |
| Sprint projekta          | msdyn_projectsprint         |

**OperationSet**

Entitet OperationSet je obrazac jedinice rada koji se može koristiti kada se u transakciji mora obraditi nekoliko zahteva koji utiču na raspored.

**API-ji za raspored projekata**

Sledi lista aktuelnih API-ja za raspored projekata.

| **API**                                 | Opis                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Ovaj API se koristi za kreiranje projekta. Projekat i podrazumevani kontejner projekta kreiraju se odmah.                         |
| **msdyn_CreateTeamMemberV1**            | Ovaj API se koristi za kreiranje člana projektnog tima. Evidencija člana tima kreira se odmah.                                  |
| **msdyn_CreateOperationSetV1**          | Ovaj API se koristi za zakazivanje nekoliko zahteva koji se moraju izvršiti u okviru transakcije.                                        |
| **msdyn_PssCreateV1**                   | Ovaj API se koristi za kreiranje entiteta. Entitet može biti bilo koji entitet raspoređivanja projekta koji podržava operaciju kreiranja. |
| **msdyn_PssUpdateV1**                   | Ovaj API se koristi za ažuriranje entiteta. Entitet može biti bilo koji entitet raspoređivanja projekta koji podržava operaciju ažuriranja  |
| **msdyn_PssDeleteV1**                   | Ovaj API se koristi za brisanje entiteta. Entitet može biti bilo koji entitet raspoređivanja projekta koji podržava operaciju brisanja. |
| **msdyn_ExecuteOperationSetV1**         | Ovaj API se koristi za izvršavanje svih operacija unutar datog skupa operacija.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Ovaj API se koristi za ažuriranje konture planiranog rada dodele resursa.                                                        |



**Korišćenje API-ja za raspored projekata sa entitetom OperationSet**

Pošto se zapisi sa **CreateProjectV1** i **CreateTeamMemberV1** kreiraju odmah, ovi API-ji se ne mogu koristiti u **OperationSet entitetu** direktno. Međutim, API možete koristiti za kreiranje potrebnih zapisa, kreirajte **OperationSet entitet**, a zatim koristite ove unapred kreirane zapise u **OperationSet entitetu**.

**Podržane operacije**

| **Entitet planiranja**   | **Kreiranje** | **Ažuriranje** | **Delete** | **Važna razmatranja**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektni zadatak            | Da        | Da        | Da        | Polja **Napredak**, **EffortCompleted** i **EffortRemaining** možete uređivati u rešenju Project for the Web, ali ih ne možete uređivati u rešenju Project Operations.                                                                                                                                                                                             |
| Zavisnost projektnog zadatka | Da        | No         | Da        | Zapisi zavisnosti projektnih zadataka se ne ažuriraju. Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis.                                                                                                                                                                                                                                 |
| Dodela resursa     | Da        | Da\*      | Da        | Nisu podržane operacije sa sledećim poljima: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Zapisi o dodeli resursa se ne ažuriraju. Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis. Obezbeđen je poseban API za ažuriranje kontura dodele resursa. |
| Kontejner projekta          | Da        | Da        | Da        | Podrazumevani kontejner se kreira se koristeći API **CreateProjectV1**. Podrška za kreiranje i brisanje kontejnera projekta je dodata u izdanju 16 ažuriranja.                                                                                                                                                                                                   |
| Član projektnog tima     | Da        | Da        | Da        | Za operaciju kreiranja koristite API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Da        | Da        |            | Nisu podržane operacije sa sledećim poljima: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.                                                                                       |
| Liste za proveru projekta      | Da        | Da        | Da        |                                                                                                                                                                                                                                                                                                                                                         |
| Oznaka projekta           | No         | Da        | No         | Nazivi oznaka se mogu promeniti. Ova funkcija je dostupna samo za Project for the Web                                                                                                                                                                                                                                                                      |
| Zavisnost projektnog zadataka i oznake   | Da        | No         | Da        | Ova funkcija je dostupna samo za Project for the Web                                                                                                                                                                                                                                                                                                  |
| Sprint projekta          | Da        | Da        | Da        | Polje **Početak** mora imati datum raniji od polja **Završetak**. Sprintevi za isti projekat ne mogu da se preklapaju jedni sa drugima. Ova funkcija je dostupna samo za Project for the Web                                                                                                                                                                    |




Svojstvo ID je opcionalno. Ako je obezbeđeno, sistem pokušava da ga koristi i izbacuje izuzetak ako ne može da ga koristi. Ako nije obezbeđeno, sistem će ga generisati.

**Ograničenja i poznati problemi**

Sledi lista ograničenja i poznatih problema:

-   API-je za raspored projekata mogu da koriste samo **Korisnici sa licencom za Microsoft Project**. Ne mogu ih koristiti:
    -   Korisnici aplikacije
    -   Korisnici sistema
    -   Korisnici integracije
    -   Ostali korisnici koji nemaju potrebnu licencu
-   Svaki **OperationSet entitet** može da ima najviše 100 operacija.
-   Svaki korisnik može da ima najviše 10 otvorenih **OperationSet entiteta**.
-   Project Operations trenutno podržava maksimalno 500 ukupnih zadataka na projektu.
-   Svaka operacija ažuriranja konture dodele resursa se računa kao jedna operacija.
-   Svaka lista ažuriranih kontura može da sadrži najviše 100 vremenskih isečaka.
-   Status greške i evidencije grešaka **OperationSet entiteta** trenutno nisu dostupne.
-   Postoji najviše 400 sprintova po projektu.
-   [Ograničenja i granice projekata i zadataka](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Oznake su trenutno dostupne samo za Project for the Web.

**Rukovanje greškama**

-   Da biste pregledali greške generisane iz skupova operacija, idite na **Podešavanja** \> **Zakaži integraciju** \> **Skupovi operacija**.
-   Da biste pregledali greške koje je generisala usluga rasporeda projekata, idite na **Podešavanja** \> **Integracija rasporeda** \> **PSS evidencije grešaka**.

**Uređivanje kontura dodele resursa**

Za razliku od svih drugih API-ja za planiranje koji ažuriraju entitet, API za konturu dodele resursa je isključivo odgovoran za ažuriranja jednog polja, msdyn_plannedwork, na jednim entitetom, msydn_resourceassignment.

Dati režim rasporeda je:

-   **fiksne jedinice**
-   kalendar projekta je 9-5p je 9-5pst, pon, uto čet, petak (SREDA JE NERADNA)
-   a kalendar resursa je 9-1p PST pon. do pet.

Ovaj zadatak je za nedelju dana, četiri sata dnevno. To je zato što je kalendar resursa od 9-1 PST ili četiri sata dnevno.

| &nbsp;     | Zadatak | Datum početka | Datum završetka  | Količina | 13.6.2022. | 14.6.2022. | 15.6.2022. | 16.6.2022. | 17.6.2022. |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 radnik |  T1  | 13.6.2022.  | 17.6.2022. | 20       | 4         | 4         | 4         | 4         | 4         |

Na primer, ako želite da radnik radi samo tri sata svakog dana ove sedmice i omogućite jedan sat za druge zadatke.

#### <a name="updatedcontours-sample-payload"></a>Korisni podaci primera za UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Ovo je dodela nakon što se pokrene API za ažuriranje rasporeda kontura.

| &nbsp;     | Zadatak | Datum početka | Datum završetka  | Količina | 13.6.2022. | 14.6.2022. | 15.6.2022. | 16.6.2022. | 17.6.2022. |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 radnik | T1   | 13.6.2022.  | 17.6.2022. | 15       | 3         | 3         | 3         | 3         | 3         |


**Primer scenarija**

U ovom scenariju, kreiraćete projekat, člana tima, četiri zadatka i dva zadatka resursa. Zatim ćete ažurirati jedan zadatak, ažurirati projekat, izbrisati jedan zadatak, izbrisati jednu dodelu resursa i kreirati zavisnost zadatka.

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

** Dodatni primeri

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
