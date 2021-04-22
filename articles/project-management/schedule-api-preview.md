---
title: Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja
description: Ova tema pruža informacije i primere za korišćenje API-ja za raspored.
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
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868146"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

> [!IMPORTANT] 
> Neke ili sve funkcionalnosti zabeležene u ovoj temi dostupne su kao deo izdanja verzije za pregled. Sadržaj i funkcionalnost su podložni promenama. 

## <a name="scheduling-entities"></a>Entiteti planiranja

API-ji za raspored pružaju mogućnost izvršavanja operacija kreiranja, ažuriranja i brisanja pomoću **entiteta planiranja**. Tim entitetima se upravlja putem mehanizma za raspoređivanje u aplikaciji Project za veb. Kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja** bili su ograničeni u ranijim izdanjima usluge Dynamics 365 Project Operations.

Sledeća tabela daje potpunu listu **entiteta planiranja**.

| Naziv entiteta  | Logičko ime entiteta |
| --- | --- |
| Project | msdyn_project |
| Projektni zadatak  | msdyn_projecttask  |
| Zavisnost projektnog zadatka  | msdyn_projecttaskdependency  |
| Dodela resursa | msdyn_resourceassignment |
| Kontejner projekta  | msdyn_projectbucket |
| Član projektnog tima | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

Entitet OperationSet je obrazac jedinice rada koji se može koristiti kada se u transakciji mora obraditi nekoliko zahteva koji utiču na raspored.

## <a name="schedule-apis"></a>API-ji za raspored

Sledi lista aktuelnih API-ja za raspored.

- **msdyn_CreateProjectV1**: Ovaj API se može koristiti za kreiranje projekta. Projekat i podrazumevani kontejner projekta kreiraju se odmah.
- **msdyn_CreateTeamMemberV1**: Ovaj API se može koristiti za kreiranje člana projektnog tima. Evidencija člana tima kreira se odmah.
- **msdyn_CreateOperationSetV1**: Ovaj API se može koristiti za zakazivanje nekoliko zahteva koji se moraju izvršiti u okviru transakcije.
- **msdyn_PSSCreateV1**: Ovaj API se može koristiti za kreiranje entiteta. Entitet može biti bilo koji entitet planiranja koji podržava operaciju kreiranja.
- **msdyn_PSSUpdateV1**: Ovaj API se može koristiti za ažuriranje entiteta. Entitet može biti bilo koji entitet planiranja koji podržava operaciju ažuriranja.
- **msdyn_PSSDeleteV1**: Ovaj API se može koristiti za brisanje entiteta. Entitet može biti bilo koji entitet planiranja koji podržava operaciju brisanja.
- **msdyn_ExecuteOperationSetV1**: Ovaj API se koristi za izvršavanje svih operacija unutar datog skupa operacija.

## <a name="using-schedule-apis-with-operationset"></a>Korišćenje API-ja rasporeda sa OperationSet entitetom

Pošto se zapisi sa **CreateProjectV1** i **CreateTeamMemberV1** kreiraju odmah, ovi API-ji se ne mogu koristiti u **OperationSet entitetu** direktno. Međutim, API možete koristiti za kreiranje potrebnih zapisa, kreirajte **OperationSet entitet**, a zatim koristite ove unapred kreirane zapise u **OperationSet entitetu**.

## <a name="supported-operations"></a>Podržane operacije

| Entitet planiranja | Kreiranje | Ažuriranje | Delete | Važna razmatranja |
| --- | --- | --- | --- | --- |
Projektni zadatak | Da | Da | Da | Ništa |
| Zavisnost projektnog zadatka | Da | Da | | Zapisi zavisnosti projektnih zadataka se ne ažuriraju. Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis. |
| Dodela resursa | Da | Da | | Nisu podržane operacije sa sledećim poljima: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**. Zapisi o dodeli resursa se ne ažuriraju. Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis. |
| Kontejner projekta | Nije primenljivo | Nije primenljivo | Nije primenljivo | Podrazumevani kontejner se kreira se pomoću API-ja **CreateProjectV1**. |
| Član projektnog tima | Da | Da | Da | Za operaciju kreiranja koristite API **CreateTeamMemberV1**. |
| Project | Da | Da | Nije primenljivo | Nisu podržane operacije sa sledećim poljima: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**. |

Ovi API-ji se mogu pozivati sa objektima entiteta koji uključuju prilagođena polja.

Svojstvo ID je opcionalno. Ako je obezbeđeno, sistem pokušava da ga koristi i izbacuje izuzetak ako ne može da ga koristi. Ako nije obezbeđeno, sistem će ga generisati.

## <a name="limitations-and-known-issues"></a>Ograničenja i poznati problemi
Sledi lista ograničenja i poznatih problema:

- API-je za raspored mogu da koriste samo **korisnici sa licencom za Microsoft Project.** Ne mogu ih koristiti:
    - Korisnici aplikacije
    - Korisnici sistema
    - Korisnici integracije
    - Ostali korisnici koji nemaju potrebnu licencu
- Svaki **OperationSet entitet** može da ima najviše 100 operacija.
- Svaki korisnik može da ima najviše 10 otvorenih **OperationSet entiteta**.
- Project Operations trenutno podržava maksimalno 500 ukupnih zadataka na projektu.
- Status greške i evidencije grešaka **OperationSet entiteta** trenutno nisu dostupne.
- API-ji za raspored su u verziji za javni pregled. Microsoft ne podržava upotrebu ovih API-ja u proizvodnom okruženju.

## <a name="sample-scenario"></a>Primer scenarija

U ovom scenariju, kreiraćete projekat, člana tima, četiri zadatka i dva zadatka resursa. Zatim ćete ažurirati jedan zadatak, ažurirati projekat, izbrisati jedan zadatak, izbrisati jednu dodelu resursa i kreirati zavisnost zadatka.

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

## <a name="additional-samples"></a>Dodatni primeri

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
