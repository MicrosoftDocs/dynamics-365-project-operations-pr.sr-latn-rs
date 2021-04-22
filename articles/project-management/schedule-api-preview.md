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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="76c29-103">Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja</span><span class="sxs-lookup"><span data-stu-id="76c29-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="76c29-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="76c29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="76c29-105">Neke ili sve funkcionalnosti zabeležene u ovoj temi dostupne su kao deo izdanja verzije za pregled.</span><span class="sxs-lookup"><span data-stu-id="76c29-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="76c29-106">Sadržaj i funkcionalnost su podložni promenama.</span><span class="sxs-lookup"><span data-stu-id="76c29-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="76c29-107">Entiteti planiranja</span><span class="sxs-lookup"><span data-stu-id="76c29-107">Scheduling entities</span></span>

<span data-ttu-id="76c29-108">API-ji za raspored pružaju mogućnost izvršavanja operacija kreiranja, ažuriranja i brisanja pomoću **entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="76c29-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="76c29-109">Tim entitetima se upravlja putem mehanizma za raspoređivanje u aplikaciji Project za veb.</span><span class="sxs-lookup"><span data-stu-id="76c29-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="76c29-110">Kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja** bili su ograničeni u ranijim izdanjima usluge Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="76c29-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="76c29-111">Sledeća tabela daje potpunu listu **entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="76c29-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="76c29-112">Naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="76c29-112">Entity name</span></span>  | <span data-ttu-id="76c29-113">Logičko ime entiteta</span><span class="sxs-lookup"><span data-stu-id="76c29-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="76c29-114">Project</span><span class="sxs-lookup"><span data-stu-id="76c29-114">Project</span></span> | <span data-ttu-id="76c29-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="76c29-115">msdyn_project</span></span> |
| <span data-ttu-id="76c29-116">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="76c29-116">Project Task</span></span>  | <span data-ttu-id="76c29-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="76c29-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="76c29-118">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="76c29-118">Project Task Dependency</span></span>  | <span data-ttu-id="76c29-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="76c29-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="76c29-120">Dodela resursa</span><span class="sxs-lookup"><span data-stu-id="76c29-120">Resource Assignment</span></span> | <span data-ttu-id="76c29-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="76c29-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="76c29-122">Kontejner projekta</span><span class="sxs-lookup"><span data-stu-id="76c29-122">Project Bucket</span></span>  | <span data-ttu-id="76c29-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="76c29-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="76c29-124">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="76c29-124">Project Team Member</span></span> | <span data-ttu-id="76c29-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="76c29-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="76c29-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="76c29-126">OperationSet</span></span>

<span data-ttu-id="76c29-127">Entitet OperationSet je obrazac jedinice rada koji se može koristiti kada se u transakciji mora obraditi nekoliko zahteva koji utiču na raspored.</span><span class="sxs-lookup"><span data-stu-id="76c29-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="76c29-128">API-ji za raspored</span><span class="sxs-lookup"><span data-stu-id="76c29-128">Schedule APIs</span></span>

<span data-ttu-id="76c29-129">Sledi lista aktuelnih API-ja za raspored.</span><span class="sxs-lookup"><span data-stu-id="76c29-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="76c29-130">**msdyn_CreateProjectV1**: Ovaj API se može koristiti za kreiranje projekta.</span><span class="sxs-lookup"><span data-stu-id="76c29-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="76c29-131">Projekat i podrazumevani kontejner projekta kreiraju se odmah.</span><span class="sxs-lookup"><span data-stu-id="76c29-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="76c29-132">**msdyn_CreateTeamMemberV1**: Ovaj API se može koristiti za kreiranje člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="76c29-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="76c29-133">Evidencija člana tima kreira se odmah.</span><span class="sxs-lookup"><span data-stu-id="76c29-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="76c29-134">**msdyn_CreateOperationSetV1**: Ovaj API se može koristiti za zakazivanje nekoliko zahteva koji se moraju izvršiti u okviru transakcije.</span><span class="sxs-lookup"><span data-stu-id="76c29-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="76c29-135">**msdyn_PSSCreateV1**: Ovaj API se može koristiti za kreiranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="76c29-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="76c29-136">Entitet može biti bilo koji entitet planiranja koji podržava operaciju kreiranja.</span><span class="sxs-lookup"><span data-stu-id="76c29-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="76c29-137">**msdyn_PSSUpdateV1**: Ovaj API se može koristiti za ažuriranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="76c29-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="76c29-138">Entitet može biti bilo koji entitet planiranja koji podržava operaciju ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="76c29-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="76c29-139">**msdyn_PSSDeleteV1**: Ovaj API se može koristiti za brisanje entiteta.</span><span class="sxs-lookup"><span data-stu-id="76c29-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="76c29-140">Entitet može biti bilo koji entitet planiranja koji podržava operaciju brisanja.</span><span class="sxs-lookup"><span data-stu-id="76c29-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="76c29-141">**msdyn_ExecuteOperationSetV1**: Ovaj API se koristi za izvršavanje svih operacija unutar datog skupa operacija.</span><span class="sxs-lookup"><span data-stu-id="76c29-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="76c29-142">Korišćenje API-ja rasporeda sa OperationSet entitetom</span><span class="sxs-lookup"><span data-stu-id="76c29-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="76c29-143">Pošto se zapisi sa **CreateProjectV1** i **CreateTeamMemberV1** kreiraju odmah, ovi API-ji se ne mogu koristiti u **OperationSet entitetu** direktno.</span><span class="sxs-lookup"><span data-stu-id="76c29-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="76c29-144">Međutim, API možete koristiti za kreiranje potrebnih zapisa, kreirajte **OperationSet entitet**, a zatim koristite ove unapred kreirane zapise u **OperationSet entitetu**.</span><span class="sxs-lookup"><span data-stu-id="76c29-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="76c29-145">Podržane operacije</span><span class="sxs-lookup"><span data-stu-id="76c29-145">Supported operations</span></span>

| <span data-ttu-id="76c29-146">Entitet planiranja</span><span class="sxs-lookup"><span data-stu-id="76c29-146">Scheduling entity</span></span> | <span data-ttu-id="76c29-147">Kreiranje</span><span class="sxs-lookup"><span data-stu-id="76c29-147">Create</span></span> | <span data-ttu-id="76c29-148">Ažuriranje</span><span class="sxs-lookup"><span data-stu-id="76c29-148">Update</span></span> | <span data-ttu-id="76c29-149">Delete</span><span class="sxs-lookup"><span data-stu-id="76c29-149">Delete</span></span> | <span data-ttu-id="76c29-150">Važna razmatranja</span><span class="sxs-lookup"><span data-stu-id="76c29-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="76c29-151">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="76c29-151">Project task</span></span> | <span data-ttu-id="76c29-152">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-152">Yes</span></span> | <span data-ttu-id="76c29-153">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-153">Yes</span></span> | <span data-ttu-id="76c29-154">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-154">Yes</span></span> | <span data-ttu-id="76c29-155">Ništa</span><span class="sxs-lookup"><span data-stu-id="76c29-155">None</span></span> |
| <span data-ttu-id="76c29-156">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="76c29-156">Project task dependency</span></span> | <span data-ttu-id="76c29-157">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-157">Yes</span></span> | <span data-ttu-id="76c29-158">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-158">Yes</span></span> | | <span data-ttu-id="76c29-159">Zapisi zavisnosti projektnih zadataka se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="76c29-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="76c29-160">Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis.</span><span class="sxs-lookup"><span data-stu-id="76c29-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="76c29-161">Dodela resursa</span><span class="sxs-lookup"><span data-stu-id="76c29-161">Resource assignment</span></span> | <span data-ttu-id="76c29-162">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-162">Yes</span></span> | <span data-ttu-id="76c29-163">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-163">Yes</span></span> | | <span data-ttu-id="76c29-164">Nisu podržane operacije sa sledećim poljima: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="76c29-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="76c29-165">Zapisi o dodeli resursa se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="76c29-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="76c29-166">Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis.</span><span class="sxs-lookup"><span data-stu-id="76c29-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="76c29-167">Kontejner projekta</span><span class="sxs-lookup"><span data-stu-id="76c29-167">Project bucket</span></span> | <span data-ttu-id="76c29-168">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="76c29-168">N/A</span></span> | <span data-ttu-id="76c29-169">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="76c29-169">N/A</span></span> | <span data-ttu-id="76c29-170">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="76c29-170">N/A</span></span> | <span data-ttu-id="76c29-171">Podrazumevani kontejner se kreira se pomoću API-ja **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="76c29-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="76c29-172">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="76c29-172">Project team member</span></span> | <span data-ttu-id="76c29-173">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-173">Yes</span></span> | <span data-ttu-id="76c29-174">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-174">Yes</span></span> | <span data-ttu-id="76c29-175">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-175">Yes</span></span> | <span data-ttu-id="76c29-176">Za operaciju kreiranja koristite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="76c29-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="76c29-177">Project</span><span class="sxs-lookup"><span data-stu-id="76c29-177">Project</span></span> | <span data-ttu-id="76c29-178">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-178">Yes</span></span> | <span data-ttu-id="76c29-179">Da</span><span class="sxs-lookup"><span data-stu-id="76c29-179">Yes</span></span> | <span data-ttu-id="76c29-180">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="76c29-180">N/A</span></span> | <span data-ttu-id="76c29-181">Nisu podržane operacije sa sledećim poljima: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="76c29-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="76c29-182">Ovi API-ji se mogu pozivati sa objektima entiteta koji uključuju prilagođena polja.</span><span class="sxs-lookup"><span data-stu-id="76c29-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="76c29-183">Svojstvo ID je opcionalno.</span><span class="sxs-lookup"><span data-stu-id="76c29-183">The ID property is optional.</span></span> <span data-ttu-id="76c29-184">Ako je obezbeđeno, sistem pokušava da ga koristi i izbacuje izuzetak ako ne može da ga koristi.</span><span class="sxs-lookup"><span data-stu-id="76c29-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="76c29-185">Ako nije obezbeđeno, sistem će ga generisati.</span><span class="sxs-lookup"><span data-stu-id="76c29-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="76c29-186">Ograničenja i poznati problemi</span><span class="sxs-lookup"><span data-stu-id="76c29-186">Limitations and known issues</span></span>
<span data-ttu-id="76c29-187">Sledi lista ograničenja i poznatih problema:</span><span class="sxs-lookup"><span data-stu-id="76c29-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="76c29-188">API-je za raspored mogu da koriste samo **korisnici sa licencom za Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="76c29-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="76c29-189">Ne mogu ih koristiti:</span><span class="sxs-lookup"><span data-stu-id="76c29-189">They can't be used by:</span></span>
    - <span data-ttu-id="76c29-190">Korisnici aplikacije</span><span class="sxs-lookup"><span data-stu-id="76c29-190">Application users</span></span>
    - <span data-ttu-id="76c29-191">Korisnici sistema</span><span class="sxs-lookup"><span data-stu-id="76c29-191">System users</span></span>
    - <span data-ttu-id="76c29-192">Korisnici integracije</span><span class="sxs-lookup"><span data-stu-id="76c29-192">Integration users</span></span>
    - <span data-ttu-id="76c29-193">Ostali korisnici koji nemaju potrebnu licencu</span><span class="sxs-lookup"><span data-stu-id="76c29-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="76c29-194">Svaki **OperationSet entitet** može da ima najviše 100 operacija.</span><span class="sxs-lookup"><span data-stu-id="76c29-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="76c29-195">Svaki korisnik može da ima najviše 10 otvorenih **OperationSet entiteta**.</span><span class="sxs-lookup"><span data-stu-id="76c29-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="76c29-196">Project Operations trenutno podržava maksimalno 500 ukupnih zadataka na projektu.</span><span class="sxs-lookup"><span data-stu-id="76c29-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="76c29-197">Status greške i evidencije grešaka **OperationSet entiteta** trenutno nisu dostupne.</span><span class="sxs-lookup"><span data-stu-id="76c29-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="76c29-198">API-ji za raspored su u verziji za javni pregled.</span><span class="sxs-lookup"><span data-stu-id="76c29-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="76c29-199">Microsoft ne podržava upotrebu ovih API-ja u proizvodnom okruženju.</span><span class="sxs-lookup"><span data-stu-id="76c29-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="76c29-200">Primer scenarija</span><span class="sxs-lookup"><span data-stu-id="76c29-200">Sample scenario</span></span>

<span data-ttu-id="76c29-201">U ovom scenariju, kreiraćete projekat, člana tima, četiri zadatka i dva zadatka resursa.</span><span class="sxs-lookup"><span data-stu-id="76c29-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="76c29-202">Zatim ćete ažurirati jedan zadatak, ažurirati projekat, izbrisati jedan zadatak, izbrisati jednu dodelu resursa i kreirati zavisnost zadatka.</span><span class="sxs-lookup"><span data-stu-id="76c29-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="76c29-203">Dodatni primeri</span><span class="sxs-lookup"><span data-stu-id="76c29-203">Additional samples</span></span>

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
