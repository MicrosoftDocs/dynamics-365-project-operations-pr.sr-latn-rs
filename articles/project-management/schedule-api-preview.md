---
title: Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja
description: Ova tema pruža informacije i primere za korišćenje API-ja za raspored.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116814"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="11628-103">Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja</span><span class="sxs-lookup"><span data-stu-id="11628-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="11628-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="11628-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="11628-105">Neke ili sve funkcionalnosti zabeležene u ovoj temi dostupne su kao deo izdanja verzije za pregled.</span><span class="sxs-lookup"><span data-stu-id="11628-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="11628-106">Sadržaj i funkcionalnost su podložni promenama.</span><span class="sxs-lookup"><span data-stu-id="11628-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="11628-107">Entiteti planiranja</span><span class="sxs-lookup"><span data-stu-id="11628-107">Scheduling entities</span></span>

<span data-ttu-id="11628-108">API-ji za raspored pružaju mogućnost izvršavanja operacija kreiranja, ažuriranja i brisanja pomoću **entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="11628-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="11628-109">Tim entitetima se upravlja putem mehanizma za raspoređivanje u aplikaciji Project za veb.</span><span class="sxs-lookup"><span data-stu-id="11628-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="11628-110">Kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja** bili su ograničeni u ranijim izdanjima usluge Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="11628-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="11628-111">Sledeća tabela daje potpunu listu **entiteta planiranja**.</span><span class="sxs-lookup"><span data-stu-id="11628-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="11628-112">Naziv entiteta</span><span class="sxs-lookup"><span data-stu-id="11628-112">Entity name</span></span>  | <span data-ttu-id="11628-113">Logičko ime entiteta</span><span class="sxs-lookup"><span data-stu-id="11628-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="11628-114">Project</span><span class="sxs-lookup"><span data-stu-id="11628-114">Project</span></span> | <span data-ttu-id="11628-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="11628-115">msdyn_project</span></span> |
| <span data-ttu-id="11628-116">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="11628-116">Project Task</span></span>  | <span data-ttu-id="11628-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="11628-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="11628-118">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="11628-118">Project Task Dependency</span></span>  | <span data-ttu-id="11628-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="11628-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="11628-120">Dodela resursa</span><span class="sxs-lookup"><span data-stu-id="11628-120">Resource Assignment</span></span> | <span data-ttu-id="11628-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="11628-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="11628-122">Kontejner projekta</span><span class="sxs-lookup"><span data-stu-id="11628-122">Project Bucket</span></span>  | <span data-ttu-id="11628-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="11628-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="11628-124">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="11628-124">Project Team Member</span></span> | <span data-ttu-id="11628-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="11628-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="11628-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="11628-126">OperationSet</span></span>

<span data-ttu-id="11628-127">Entitet OperationSet je obrazac jedinice rada koji se može koristiti kada se u transakciji mora obraditi nekoliko zahteva koji utiču na raspored.</span><span class="sxs-lookup"><span data-stu-id="11628-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="11628-128">API-ji za raspored</span><span class="sxs-lookup"><span data-stu-id="11628-128">Schedule APIs</span></span>

<span data-ttu-id="11628-129">Sledi lista aktuelnih API-ja za raspored.</span><span class="sxs-lookup"><span data-stu-id="11628-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="11628-130">**msdyn_CreateProjectV1**: Ovaj API se može koristiti za kreiranje projekta.</span><span class="sxs-lookup"><span data-stu-id="11628-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="11628-131">Projekat i podrazumevani kontejner projekta kreiraju se odmah.</span><span class="sxs-lookup"><span data-stu-id="11628-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="11628-132">**msdyn_CreateTeamMemberV1**: Ovaj API se može koristiti za kreiranje člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="11628-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="11628-133">Evidencija člana tima kreira se odmah.</span><span class="sxs-lookup"><span data-stu-id="11628-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="11628-134">**msdyn_CreateOperationSetV1**: Ovaj API se može koristiti za zakazivanje nekoliko zahteva koji se moraju izvršiti u okviru transakcije.</span><span class="sxs-lookup"><span data-stu-id="11628-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="11628-135">**msdyn_PSSCreateV1**: Ovaj API se može koristiti za kreiranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="11628-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="11628-136">Entitet može biti bilo koji entitet planiranja koji podržava operaciju kreiranja.</span><span class="sxs-lookup"><span data-stu-id="11628-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="11628-137">**msdyn_PSSUpdateV1**: Ovaj API se može koristiti za ažuriranje entiteta.</span><span class="sxs-lookup"><span data-stu-id="11628-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="11628-138">Entitet može biti bilo koji entitet planiranja koji podržava operaciju ažuriranja.</span><span class="sxs-lookup"><span data-stu-id="11628-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="11628-139">**msdyn_PSSDeleteV1**: Ovaj API se može koristiti za brisanje entiteta.</span><span class="sxs-lookup"><span data-stu-id="11628-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="11628-140">Entitet može biti bilo koji entitet planiranja koji podržava operaciju brisanja.</span><span class="sxs-lookup"><span data-stu-id="11628-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="11628-141">**msdyn_ExecuteOperationSetV1**: Ovaj API se koristi za izvršavanje svih operacija unutar datog skupa operacija.</span><span class="sxs-lookup"><span data-stu-id="11628-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="11628-142">Korišćenje API-ja rasporeda sa OperationSet entitetom</span><span class="sxs-lookup"><span data-stu-id="11628-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="11628-143">Pošto se zapisi sa **CreateProjectV1** i **CreateTeamMemberV1** kreiraju odmah, ovi API-ji se ne mogu koristiti u **OperationSet entitetu** direktno.</span><span class="sxs-lookup"><span data-stu-id="11628-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="11628-144">Međutim, API možete koristiti za kreiranje potrebnih zapisa, kreirajte **OperationSet entitet**, a zatim koristite ove unapred kreirane zapise u **OperationSet entitetu**.</span><span class="sxs-lookup"><span data-stu-id="11628-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="11628-145">Podržane operacije</span><span class="sxs-lookup"><span data-stu-id="11628-145">Supported operations</span></span>

| <span data-ttu-id="11628-146">Entitet planiranja</span><span class="sxs-lookup"><span data-stu-id="11628-146">Scheduling entity</span></span> | <span data-ttu-id="11628-147">Kreiranje</span><span class="sxs-lookup"><span data-stu-id="11628-147">Create</span></span> | <span data-ttu-id="11628-148">Ažuriranje</span><span class="sxs-lookup"><span data-stu-id="11628-148">Update</span></span> | <span data-ttu-id="11628-149">Delete</span><span class="sxs-lookup"><span data-stu-id="11628-149">Delete</span></span> | <span data-ttu-id="11628-150">Važna razmatranja</span><span class="sxs-lookup"><span data-stu-id="11628-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="11628-151">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="11628-151">Project task</span></span> | <span data-ttu-id="11628-152">Da</span><span class="sxs-lookup"><span data-stu-id="11628-152">Yes</span></span> | <span data-ttu-id="11628-153">Da</span><span class="sxs-lookup"><span data-stu-id="11628-153">Yes</span></span> | <span data-ttu-id="11628-154">Da</span><span class="sxs-lookup"><span data-stu-id="11628-154">Yes</span></span> | <span data-ttu-id="11628-155">Ništa</span><span class="sxs-lookup"><span data-stu-id="11628-155">None</span></span> |
| <span data-ttu-id="11628-156">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="11628-156">Project task dependency</span></span> | <span data-ttu-id="11628-157">Da</span><span class="sxs-lookup"><span data-stu-id="11628-157">Yes</span></span> | <span data-ttu-id="11628-158">Da</span><span class="sxs-lookup"><span data-stu-id="11628-158">Yes</span></span> | | <span data-ttu-id="11628-159">Zapisi zavisnosti projektnih zadataka se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="11628-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="11628-160">Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis.</span><span class="sxs-lookup"><span data-stu-id="11628-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="11628-161">Dodela resursa</span><span class="sxs-lookup"><span data-stu-id="11628-161">Resource assignment</span></span> | <span data-ttu-id="11628-162">Da</span><span class="sxs-lookup"><span data-stu-id="11628-162">Yes</span></span> | <span data-ttu-id="11628-163">Da</span><span class="sxs-lookup"><span data-stu-id="11628-163">Yes</span></span> | | <span data-ttu-id="11628-164">Nisu podržane operacije sa sledećim poljima: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** i **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="11628-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="11628-165">Zapisi o dodeli resursa se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="11628-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="11628-166">Umesto toga, stari zapis može da se izbriše i može da se kreira novi zapis.</span><span class="sxs-lookup"><span data-stu-id="11628-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="11628-167">Kontejner projekta</span><span class="sxs-lookup"><span data-stu-id="11628-167">Project bucket</span></span> | <span data-ttu-id="11628-168">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="11628-168">N/A</span></span> | <span data-ttu-id="11628-169">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="11628-169">N/A</span></span> | <span data-ttu-id="11628-170">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="11628-170">N/A</span></span> | <span data-ttu-id="11628-171">Podrazumevani kontejner se kreira se pomoću API-ja **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="11628-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="11628-172">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="11628-172">Project team member</span></span> | <span data-ttu-id="11628-173">Da</span><span class="sxs-lookup"><span data-stu-id="11628-173">Yes</span></span> | <span data-ttu-id="11628-174">Da</span><span class="sxs-lookup"><span data-stu-id="11628-174">Yes</span></span> | <span data-ttu-id="11628-175">Da</span><span class="sxs-lookup"><span data-stu-id="11628-175">Yes</span></span> | <span data-ttu-id="11628-176">Za operaciju kreiranja koristite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="11628-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="11628-177">Project</span><span class="sxs-lookup"><span data-stu-id="11628-177">Project</span></span> | <span data-ttu-id="11628-178">Da</span><span class="sxs-lookup"><span data-stu-id="11628-178">Yes</span></span> | <span data-ttu-id="11628-179">Da</span><span class="sxs-lookup"><span data-stu-id="11628-179">Yes</span></span> | <span data-ttu-id="11628-180">Nije primenljivo</span><span class="sxs-lookup"><span data-stu-id="11628-180">N/A</span></span> | <span data-ttu-id="11628-181">Nisu podržane operacije sa sledećim poljima: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** i **Duration**.</span><span class="sxs-lookup"><span data-stu-id="11628-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="11628-182">Ovi API-ji se mogu pozivati sa objektima entiteta koji uključuju prilagođena polja.</span><span class="sxs-lookup"><span data-stu-id="11628-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="11628-183">Svojstvo ID je opcionalno.</span><span class="sxs-lookup"><span data-stu-id="11628-183">The ID property is optional.</span></span> <span data-ttu-id="11628-184">Ako je obezbeđeno, sistem pokušava da ga koristi i izbacuje izuzetak ako ne može da ga koristi.</span><span class="sxs-lookup"><span data-stu-id="11628-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="11628-185">Ako nije obezbeđeno, sistem će ga generisati.</span><span class="sxs-lookup"><span data-stu-id="11628-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="11628-186">Ograničena polja</span><span class="sxs-lookup"><span data-stu-id="11628-186">Restricted fields</span></span>

<span data-ttu-id="11628-187">Sledeće tabele definišu polja za koja je ograničeno **Kreiraj** i **Uredi.**</span><span class="sxs-lookup"><span data-stu-id="11628-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="11628-188">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="11628-188">Project task</span></span>

| <span data-ttu-id="11628-189">**Logičko ime**</span><span class="sxs-lookup"><span data-stu-id="11628-189">**Logical name**</span></span>                       | <span data-ttu-id="11628-190">**Može da kreira**</span><span class="sxs-lookup"><span data-stu-id="11628-190">**Can create**</span></span> | <span data-ttu-id="11628-191">**Može da menja**</span><span class="sxs-lookup"><span data-stu-id="11628-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="11628-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="11628-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="11628-193">ne</span><span class="sxs-lookup"><span data-stu-id="11628-193">no</span></span>             | <span data-ttu-id="11628-194">ne</span><span class="sxs-lookup"><span data-stu-id="11628-194">no</span></span>               |
| <span data-ttu-id="11628-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="11628-196">ne</span><span class="sxs-lookup"><span data-stu-id="11628-196">no</span></span>             | <span data-ttu-id="11628-197">ne</span><span class="sxs-lookup"><span data-stu-id="11628-197">no</span></span>               |
| <span data-ttu-id="11628-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="11628-198">msdyn_actualend</span></span>                        | <span data-ttu-id="11628-199">ne</span><span class="sxs-lookup"><span data-stu-id="11628-199">no</span></span>             | <span data-ttu-id="11628-200">ne</span><span class="sxs-lookup"><span data-stu-id="11628-200">no</span></span>               |
| <span data-ttu-id="11628-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="11628-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="11628-202">ne</span><span class="sxs-lookup"><span data-stu-id="11628-202">no</span></span>             | <span data-ttu-id="11628-203">ne</span><span class="sxs-lookup"><span data-stu-id="11628-203">no</span></span>               |
| <span data-ttu-id="11628-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="11628-205">ne</span><span class="sxs-lookup"><span data-stu-id="11628-205">no</span></span>             | <span data-ttu-id="11628-206">ne</span><span class="sxs-lookup"><span data-stu-id="11628-206">no</span></span>               |
| <span data-ttu-id="11628-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="11628-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="11628-208">ne</span><span class="sxs-lookup"><span data-stu-id="11628-208">no</span></span>             | <span data-ttu-id="11628-209">ne</span><span class="sxs-lookup"><span data-stu-id="11628-209">no</span></span>               |
| <span data-ttu-id="11628-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="11628-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="11628-211">ne</span><span class="sxs-lookup"><span data-stu-id="11628-211">no</span></span>             | <span data-ttu-id="11628-212">ne</span><span class="sxs-lookup"><span data-stu-id="11628-212">no</span></span>               |
| <span data-ttu-id="11628-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="11628-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="11628-214">ne</span><span class="sxs-lookup"><span data-stu-id="11628-214">no</span></span>             | <span data-ttu-id="11628-215">ne</span><span class="sxs-lookup"><span data-stu-id="11628-215">no</span></span>               |
| <span data-ttu-id="11628-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="11628-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="11628-217">ne</span><span class="sxs-lookup"><span data-stu-id="11628-217">no</span></span>             | <span data-ttu-id="11628-218">ne</span><span class="sxs-lookup"><span data-stu-id="11628-218">no</span></span>               |
| <span data-ttu-id="11628-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="11628-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="11628-220">ne</span><span class="sxs-lookup"><span data-stu-id="11628-220">no</span></span>             | <span data-ttu-id="11628-221">ne</span><span class="sxs-lookup"><span data-stu-id="11628-221">no</span></span>               |
| <span data-ttu-id="11628-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="11628-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="11628-223">ne</span><span class="sxs-lookup"><span data-stu-id="11628-223">no</span></span>             | <span data-ttu-id="11628-224">ne</span><span class="sxs-lookup"><span data-stu-id="11628-224">no</span></span>               |
| <span data-ttu-id="11628-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="11628-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="11628-226">ne</span><span class="sxs-lookup"><span data-stu-id="11628-226">no</span></span>             | <span data-ttu-id="11628-227">ne</span><span class="sxs-lookup"><span data-stu-id="11628-227">no</span></span>               |
| <span data-ttu-id="11628-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="11628-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="11628-229">ne</span><span class="sxs-lookup"><span data-stu-id="11628-229">no</span></span>             | <span data-ttu-id="11628-230">ne</span><span class="sxs-lookup"><span data-stu-id="11628-230">no</span></span>               |
| <span data-ttu-id="11628-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="11628-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="11628-232">ne</span><span class="sxs-lookup"><span data-stu-id="11628-232">no</span></span>             | <span data-ttu-id="11628-233">ne</span><span class="sxs-lookup"><span data-stu-id="11628-233">no</span></span>               |
| <span data-ttu-id="11628-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="11628-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="11628-235">ne</span><span class="sxs-lookup"><span data-stu-id="11628-235">no</span></span>             | <span data-ttu-id="11628-236">ne</span><span class="sxs-lookup"><span data-stu-id="11628-236">no</span></span>               |
| <span data-ttu-id="11628-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="11628-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="11628-238">ne</span><span class="sxs-lookup"><span data-stu-id="11628-238">no</span></span>             | <span data-ttu-id="11628-239">ne</span><span class="sxs-lookup"><span data-stu-id="11628-239">no</span></span>               |
| <span data-ttu-id="11628-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="11628-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="11628-241">ne</span><span class="sxs-lookup"><span data-stu-id="11628-241">no</span></span>             | <span data-ttu-id="11628-242">ne</span><span class="sxs-lookup"><span data-stu-id="11628-242">no</span></span>               |
| <span data-ttu-id="11628-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="11628-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="11628-244">ne</span><span class="sxs-lookup"><span data-stu-id="11628-244">no</span></span>             | <span data-ttu-id="11628-245">ne</span><span class="sxs-lookup"><span data-stu-id="11628-245">no</span></span>               |
| <span data-ttu-id="11628-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="11628-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="11628-247">ne</span><span class="sxs-lookup"><span data-stu-id="11628-247">no</span></span>             | <span data-ttu-id="11628-248">ne</span><span class="sxs-lookup"><span data-stu-id="11628-248">no</span></span>               |
| <span data-ttu-id="11628-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="11628-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="11628-250">ne</span><span class="sxs-lookup"><span data-stu-id="11628-250">no</span></span>             | <span data-ttu-id="11628-251">ne</span><span class="sxs-lookup"><span data-stu-id="11628-251">no</span></span>               |
| <span data-ttu-id="11628-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="11628-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="11628-253">ne</span><span class="sxs-lookup"><span data-stu-id="11628-253">no</span></span>             | <span data-ttu-id="11628-254">ne</span><span class="sxs-lookup"><span data-stu-id="11628-254">no</span></span>               |
| <span data-ttu-id="11628-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="11628-256">ne</span><span class="sxs-lookup"><span data-stu-id="11628-256">no</span></span>             | <span data-ttu-id="11628-257">ne</span><span class="sxs-lookup"><span data-stu-id="11628-257">no</span></span>               |
| <span data-ttu-id="11628-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="11628-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="11628-259">ne</span><span class="sxs-lookup"><span data-stu-id="11628-259">no</span></span>             | <span data-ttu-id="11628-260">ne</span><span class="sxs-lookup"><span data-stu-id="11628-260">no</span></span>               |
| <span data-ttu-id="11628-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="11628-262">ne</span><span class="sxs-lookup"><span data-stu-id="11628-262">no</span></span>             | <span data-ttu-id="11628-263">ne</span><span class="sxs-lookup"><span data-stu-id="11628-263">no</span></span>               |
| <span data-ttu-id="11628-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="11628-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="11628-265">ne</span><span class="sxs-lookup"><span data-stu-id="11628-265">no</span></span>             | <span data-ttu-id="11628-266">ne</span><span class="sxs-lookup"><span data-stu-id="11628-266">no</span></span>               |
| <span data-ttu-id="11628-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="11628-267">msdyn_progress</span></span>                         | <span data-ttu-id="11628-268">ne</span><span class="sxs-lookup"><span data-stu-id="11628-268">no</span></span>             | <span data-ttu-id="11628-269">ne (da za P4W)</span><span class="sxs-lookup"><span data-stu-id="11628-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="11628-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="11628-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="11628-271">ne</span><span class="sxs-lookup"><span data-stu-id="11628-271">no</span></span>             | <span data-ttu-id="11628-272">ne</span><span class="sxs-lookup"><span data-stu-id="11628-272">no</span></span>               |
| <span data-ttu-id="11628-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="11628-274">ne</span><span class="sxs-lookup"><span data-stu-id="11628-274">no</span></span>             | <span data-ttu-id="11628-275">ne</span><span class="sxs-lookup"><span data-stu-id="11628-275">no</span></span>               |
| <span data-ttu-id="11628-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="11628-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="11628-277">ne</span><span class="sxs-lookup"><span data-stu-id="11628-277">no</span></span>             | <span data-ttu-id="11628-278">ne</span><span class="sxs-lookup"><span data-stu-id="11628-278">no</span></span>               |
| <span data-ttu-id="11628-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="11628-280">ne</span><span class="sxs-lookup"><span data-stu-id="11628-280">no</span></span>             | <span data-ttu-id="11628-281">ne</span><span class="sxs-lookup"><span data-stu-id="11628-281">no</span></span>               |
| <span data-ttu-id="11628-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="11628-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="11628-283">ne</span><span class="sxs-lookup"><span data-stu-id="11628-283">no</span></span>             | <span data-ttu-id="11628-284">ne</span><span class="sxs-lookup"><span data-stu-id="11628-284">no</span></span>               |
| <span data-ttu-id="11628-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="11628-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="11628-286">ne</span><span class="sxs-lookup"><span data-stu-id="11628-286">no</span></span>             | <span data-ttu-id="11628-287">ne</span><span class="sxs-lookup"><span data-stu-id="11628-287">no</span></span>               |
| <span data-ttu-id="11628-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="11628-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="11628-289">ne</span><span class="sxs-lookup"><span data-stu-id="11628-289">no</span></span>             | <span data-ttu-id="11628-290">ne</span><span class="sxs-lookup"><span data-stu-id="11628-290">no</span></span>               |
| <span data-ttu-id="11628-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="11628-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="11628-292">ne</span><span class="sxs-lookup"><span data-stu-id="11628-292">no</span></span>             | <span data-ttu-id="11628-293">ne</span><span class="sxs-lookup"><span data-stu-id="11628-293">no</span></span>               |
| <span data-ttu-id="11628-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="11628-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="11628-295">ne</span><span class="sxs-lookup"><span data-stu-id="11628-295">no</span></span>             | <span data-ttu-id="11628-296">ne</span><span class="sxs-lookup"><span data-stu-id="11628-296">no</span></span>               |
| <span data-ttu-id="11628-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="11628-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="11628-298">ne</span><span class="sxs-lookup"><span data-stu-id="11628-298">no</span></span>             | <span data-ttu-id="11628-299">ne</span><span class="sxs-lookup"><span data-stu-id="11628-299">no</span></span>               |
| <span data-ttu-id="11628-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="11628-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="11628-301">ne</span><span class="sxs-lookup"><span data-stu-id="11628-301">no</span></span>             | <span data-ttu-id="11628-302">ne</span><span class="sxs-lookup"><span data-stu-id="11628-302">no</span></span>               |
| <span data-ttu-id="11628-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="11628-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="11628-304">ne</span><span class="sxs-lookup"><span data-stu-id="11628-304">no</span></span>             | <span data-ttu-id="11628-305">ne</span><span class="sxs-lookup"><span data-stu-id="11628-305">no</span></span>               |
| <span data-ttu-id="11628-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="11628-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="11628-307">ne</span><span class="sxs-lookup"><span data-stu-id="11628-307">no</span></span>             | <span data-ttu-id="11628-308">ne</span><span class="sxs-lookup"><span data-stu-id="11628-308">no</span></span>               |
| <span data-ttu-id="11628-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="11628-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="11628-310">ne</span><span class="sxs-lookup"><span data-stu-id="11628-310">no</span></span>             | <span data-ttu-id="11628-311">ne</span><span class="sxs-lookup"><span data-stu-id="11628-311">no</span></span>               |
| <span data-ttu-id="11628-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="11628-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="11628-313">ne</span><span class="sxs-lookup"><span data-stu-id="11628-313">no</span></span>             | <span data-ttu-id="11628-314">ne</span><span class="sxs-lookup"><span data-stu-id="11628-314">no</span></span>               |
| <span data-ttu-id="11628-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="11628-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="11628-316">ne</span><span class="sxs-lookup"><span data-stu-id="11628-316">no</span></span>             | <span data-ttu-id="11628-317">ne</span><span class="sxs-lookup"><span data-stu-id="11628-317">no</span></span>               |
| <span data-ttu-id="11628-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="11628-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="11628-319">ne</span><span class="sxs-lookup"><span data-stu-id="11628-319">no</span></span>             | <span data-ttu-id="11628-320">ne</span><span class="sxs-lookup"><span data-stu-id="11628-320">no</span></span>               |
| <span data-ttu-id="11628-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="11628-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="11628-322">ne</span><span class="sxs-lookup"><span data-stu-id="11628-322">no</span></span>             | <span data-ttu-id="11628-323">ne</span><span class="sxs-lookup"><span data-stu-id="11628-323">no</span></span>               |
| <span data-ttu-id="11628-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="11628-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="11628-325">ne</span><span class="sxs-lookup"><span data-stu-id="11628-325">no</span></span>             | <span data-ttu-id="11628-326">ne</span><span class="sxs-lookup"><span data-stu-id="11628-326">no</span></span>               |
| <span data-ttu-id="11628-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="11628-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="11628-328">ne</span><span class="sxs-lookup"><span data-stu-id="11628-328">no</span></span>             | <span data-ttu-id="11628-329">ne</span><span class="sxs-lookup"><span data-stu-id="11628-329">no</span></span>               |
| <span data-ttu-id="11628-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="11628-330">msdyn_summary</span></span>                          | <span data-ttu-id="11628-331">ne</span><span class="sxs-lookup"><span data-stu-id="11628-331">no</span></span>             | <span data-ttu-id="11628-332">ne</span><span class="sxs-lookup"><span data-stu-id="11628-332">no</span></span>               |
| <span data-ttu-id="11628-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="11628-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="11628-334">ne</span><span class="sxs-lookup"><span data-stu-id="11628-334">no</span></span>             | <span data-ttu-id="11628-335">ne</span><span class="sxs-lookup"><span data-stu-id="11628-335">no</span></span>               |
| <span data-ttu-id="11628-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="11628-337">ne</span><span class="sxs-lookup"><span data-stu-id="11628-337">no</span></span>             | <span data-ttu-id="11628-338">ne</span><span class="sxs-lookup"><span data-stu-id="11628-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="11628-339">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="11628-339">Project task dependency</span></span>

| <span data-ttu-id="11628-340">**Logičko ime**</span><span class="sxs-lookup"><span data-stu-id="11628-340">**Logical name**</span></span>              | <span data-ttu-id="11628-341">**Može da kreira**</span><span class="sxs-lookup"><span data-stu-id="11628-341">**Can create**</span></span> | <span data-ttu-id="11628-342">**Može da menja**</span><span class="sxs-lookup"><span data-stu-id="11628-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="11628-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="11628-343">msdyn_linktype</span></span>                | <span data-ttu-id="11628-344">ne</span><span class="sxs-lookup"><span data-stu-id="11628-344">no</span></span>             | <span data-ttu-id="11628-345">ne</span><span class="sxs-lookup"><span data-stu-id="11628-345">no</span></span>           |
| <span data-ttu-id="11628-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="11628-346">msdyn_linktypename</span></span>            | <span data-ttu-id="11628-347">ne</span><span class="sxs-lookup"><span data-stu-id="11628-347">no</span></span>             | <span data-ttu-id="11628-348">ne</span><span class="sxs-lookup"><span data-stu-id="11628-348">no</span></span>           |
| <span data-ttu-id="11628-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="11628-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="11628-350">da</span><span class="sxs-lookup"><span data-stu-id="11628-350">yes</span></span>            | <span data-ttu-id="11628-351">ne</span><span class="sxs-lookup"><span data-stu-id="11628-351">no</span></span>           |
| <span data-ttu-id="11628-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="11628-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="11628-353">da</span><span class="sxs-lookup"><span data-stu-id="11628-353">yes</span></span>            | <span data-ttu-id="11628-354">ne</span><span class="sxs-lookup"><span data-stu-id="11628-354">no</span></span>           |
| <span data-ttu-id="11628-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="11628-355">msdyn_project</span></span>                 | <span data-ttu-id="11628-356">da</span><span class="sxs-lookup"><span data-stu-id="11628-356">yes</span></span>            | <span data-ttu-id="11628-357">ne</span><span class="sxs-lookup"><span data-stu-id="11628-357">no</span></span>           |
| <span data-ttu-id="11628-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="11628-358">msdyn_projectname</span></span>             | <span data-ttu-id="11628-359">da</span><span class="sxs-lookup"><span data-stu-id="11628-359">yes</span></span>            | <span data-ttu-id="11628-360">ne</span><span class="sxs-lookup"><span data-stu-id="11628-360">no</span></span>           |
| <span data-ttu-id="11628-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="11628-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="11628-362">da</span><span class="sxs-lookup"><span data-stu-id="11628-362">yes</span></span>            | <span data-ttu-id="11628-363">ne</span><span class="sxs-lookup"><span data-stu-id="11628-363">no</span></span>           |
| <span data-ttu-id="11628-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="11628-364">msdyn_successortask</span></span>           | <span data-ttu-id="11628-365">da</span><span class="sxs-lookup"><span data-stu-id="11628-365">yes</span></span>            | <span data-ttu-id="11628-366">ne</span><span class="sxs-lookup"><span data-stu-id="11628-366">no</span></span>           |
| <span data-ttu-id="11628-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="11628-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="11628-368">da</span><span class="sxs-lookup"><span data-stu-id="11628-368">yes</span></span>            | <span data-ttu-id="11628-369">ne</span><span class="sxs-lookup"><span data-stu-id="11628-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="11628-370">Dodela resursa</span><span class="sxs-lookup"><span data-stu-id="11628-370">Resource assignment</span></span>

| <span data-ttu-id="11628-371">**Logičko ime**</span><span class="sxs-lookup"><span data-stu-id="11628-371">**Logical name**</span></span>             | <span data-ttu-id="11628-372">**Može da kreira**</span><span class="sxs-lookup"><span data-stu-id="11628-372">**Can create**</span></span> | <span data-ttu-id="11628-373">**Može da menja**</span><span class="sxs-lookup"><span data-stu-id="11628-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="11628-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="11628-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="11628-375">da</span><span class="sxs-lookup"><span data-stu-id="11628-375">yes</span></span>            | <span data-ttu-id="11628-376">ne</span><span class="sxs-lookup"><span data-stu-id="11628-376">no</span></span>           |
| <span data-ttu-id="11628-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="11628-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="11628-378">da</span><span class="sxs-lookup"><span data-stu-id="11628-378">yes</span></span>            | <span data-ttu-id="11628-379">ne</span><span class="sxs-lookup"><span data-stu-id="11628-379">no</span></span>           |
| <span data-ttu-id="11628-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="11628-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="11628-381">ne</span><span class="sxs-lookup"><span data-stu-id="11628-381">no</span></span>             | <span data-ttu-id="11628-382">ne</span><span class="sxs-lookup"><span data-stu-id="11628-382">no</span></span>           |
| <span data-ttu-id="11628-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="11628-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="11628-384">ne</span><span class="sxs-lookup"><span data-stu-id="11628-384">no</span></span>             | <span data-ttu-id="11628-385">ne</span><span class="sxs-lookup"><span data-stu-id="11628-385">no</span></span>           |
| <span data-ttu-id="11628-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="11628-386">msdyn_committype</span></span>             | <span data-ttu-id="11628-387">ne</span><span class="sxs-lookup"><span data-stu-id="11628-387">no</span></span>             | <span data-ttu-id="11628-388">ne</span><span class="sxs-lookup"><span data-stu-id="11628-388">no</span></span>           |
| <span data-ttu-id="11628-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="11628-389">msdyn_committypename</span></span>         | <span data-ttu-id="11628-390">ne</span><span class="sxs-lookup"><span data-stu-id="11628-390">no</span></span>             | <span data-ttu-id="11628-391">ne</span><span class="sxs-lookup"><span data-stu-id="11628-391">no</span></span>           |
| <span data-ttu-id="11628-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="11628-392">msdyn_effort</span></span>                 | <span data-ttu-id="11628-393">ne</span><span class="sxs-lookup"><span data-stu-id="11628-393">no</span></span>             | <span data-ttu-id="11628-394">ne</span><span class="sxs-lookup"><span data-stu-id="11628-394">no</span></span>           |
| <span data-ttu-id="11628-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="11628-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="11628-396">ne</span><span class="sxs-lookup"><span data-stu-id="11628-396">no</span></span>             | <span data-ttu-id="11628-397">ne</span><span class="sxs-lookup"><span data-stu-id="11628-397">no</span></span>           |
| <span data-ttu-id="11628-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="11628-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="11628-399">ne</span><span class="sxs-lookup"><span data-stu-id="11628-399">no</span></span>             | <span data-ttu-id="11628-400">ne</span><span class="sxs-lookup"><span data-stu-id="11628-400">no</span></span>           |
| <span data-ttu-id="11628-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="11628-401">msdyn_finish</span></span>                 | <span data-ttu-id="11628-402">ne</span><span class="sxs-lookup"><span data-stu-id="11628-402">no</span></span>             | <span data-ttu-id="11628-403">ne</span><span class="sxs-lookup"><span data-stu-id="11628-403">no</span></span>           |
| <span data-ttu-id="11628-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="11628-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="11628-405">ne</span><span class="sxs-lookup"><span data-stu-id="11628-405">no</span></span>             | <span data-ttu-id="11628-406">ne</span><span class="sxs-lookup"><span data-stu-id="11628-406">no</span></span>           |
| <span data-ttu-id="11628-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="11628-408">ne</span><span class="sxs-lookup"><span data-stu-id="11628-408">no</span></span>             | <span data-ttu-id="11628-409">ne</span><span class="sxs-lookup"><span data-stu-id="11628-409">no</span></span>           |
| <span data-ttu-id="11628-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="11628-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="11628-411">ne</span><span class="sxs-lookup"><span data-stu-id="11628-411">no</span></span>             | <span data-ttu-id="11628-412">ne</span><span class="sxs-lookup"><span data-stu-id="11628-412">no</span></span>           |
| <span data-ttu-id="11628-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="11628-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="11628-414">ne</span><span class="sxs-lookup"><span data-stu-id="11628-414">no</span></span>             | <span data-ttu-id="11628-415">ne</span><span class="sxs-lookup"><span data-stu-id="11628-415">no</span></span>           |
| <span data-ttu-id="11628-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="11628-417">ne</span><span class="sxs-lookup"><span data-stu-id="11628-417">no</span></span>             | <span data-ttu-id="11628-418">ne</span><span class="sxs-lookup"><span data-stu-id="11628-418">no</span></span>           |
| <span data-ttu-id="11628-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="11628-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="11628-420">ne</span><span class="sxs-lookup"><span data-stu-id="11628-420">no</span></span>             | <span data-ttu-id="11628-421">ne</span><span class="sxs-lookup"><span data-stu-id="11628-421">no</span></span>           |
| <span data-ttu-id="11628-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="11628-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="11628-423">ne</span><span class="sxs-lookup"><span data-stu-id="11628-423">no</span></span>             | <span data-ttu-id="11628-424">ne</span><span class="sxs-lookup"><span data-stu-id="11628-424">no</span></span>           |
| <span data-ttu-id="11628-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="11628-425">msdyn_projectid</span></span>              | <span data-ttu-id="11628-426">da</span><span class="sxs-lookup"><span data-stu-id="11628-426">yes</span></span>            | <span data-ttu-id="11628-427">ne</span><span class="sxs-lookup"><span data-stu-id="11628-427">no</span></span>           |
| <span data-ttu-id="11628-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="11628-428">msdyn_projectidname</span></span>          | <span data-ttu-id="11628-429">ne</span><span class="sxs-lookup"><span data-stu-id="11628-429">no</span></span>             | <span data-ttu-id="11628-430">ne</span><span class="sxs-lookup"><span data-stu-id="11628-430">no</span></span>           |
| <span data-ttu-id="11628-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="11628-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="11628-432">ne</span><span class="sxs-lookup"><span data-stu-id="11628-432">no</span></span>             | <span data-ttu-id="11628-433">ne</span><span class="sxs-lookup"><span data-stu-id="11628-433">no</span></span>           |
| <span data-ttu-id="11628-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="11628-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="11628-435">ne</span><span class="sxs-lookup"><span data-stu-id="11628-435">no</span></span>             | <span data-ttu-id="11628-436">ne</span><span class="sxs-lookup"><span data-stu-id="11628-436">no</span></span>           |
| <span data-ttu-id="11628-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="11628-437">msdyn_start</span></span>                  | <span data-ttu-id="11628-438">ne</span><span class="sxs-lookup"><span data-stu-id="11628-438">no</span></span>             | <span data-ttu-id="11628-439">ne</span><span class="sxs-lookup"><span data-stu-id="11628-439">no</span></span>           |
| <span data-ttu-id="11628-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="11628-440">msdyn_taskid</span></span>                 | <span data-ttu-id="11628-441">ne</span><span class="sxs-lookup"><span data-stu-id="11628-441">no</span></span>             | <span data-ttu-id="11628-442">ne</span><span class="sxs-lookup"><span data-stu-id="11628-442">no</span></span>           |
| <span data-ttu-id="11628-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="11628-443">msdyn_taskidname</span></span>             | <span data-ttu-id="11628-444">ne</span><span class="sxs-lookup"><span data-stu-id="11628-444">no</span></span>             | <span data-ttu-id="11628-445">ne</span><span class="sxs-lookup"><span data-stu-id="11628-445">no</span></span>           |
| <span data-ttu-id="11628-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="11628-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="11628-447">ne</span><span class="sxs-lookup"><span data-stu-id="11628-447">no</span></span>             | <span data-ttu-id="11628-448">ne</span><span class="sxs-lookup"><span data-stu-id="11628-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="11628-449">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="11628-449">Project team member</span></span>

| <span data-ttu-id="11628-450">**Logičko ime**</span><span class="sxs-lookup"><span data-stu-id="11628-450">**Logical name**</span></span>                                 | <span data-ttu-id="11628-451">**Može da kreira**</span><span class="sxs-lookup"><span data-stu-id="11628-451">**Can create**</span></span> | <span data-ttu-id="11628-452">**Može da menja**</span><span class="sxs-lookup"><span data-stu-id="11628-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="11628-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="11628-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="11628-454">ne</span><span class="sxs-lookup"><span data-stu-id="11628-454">no</span></span>             | <span data-ttu-id="11628-455">ne</span><span class="sxs-lookup"><span data-stu-id="11628-455">no</span></span>           |
| <span data-ttu-id="11628-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="11628-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="11628-457">ne</span><span class="sxs-lookup"><span data-stu-id="11628-457">no</span></span>             | <span data-ttu-id="11628-458">ne</span><span class="sxs-lookup"><span data-stu-id="11628-458">no</span></span>           |
| <span data-ttu-id="11628-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="11628-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="11628-460">ne</span><span class="sxs-lookup"><span data-stu-id="11628-460">no</span></span>             | <span data-ttu-id="11628-461">ne</span><span class="sxs-lookup"><span data-stu-id="11628-461">no</span></span>           |
| <span data-ttu-id="11628-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="11628-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="11628-463">ne</span><span class="sxs-lookup"><span data-stu-id="11628-463">no</span></span>             | <span data-ttu-id="11628-464">ne</span><span class="sxs-lookup"><span data-stu-id="11628-464">no</span></span>           |
| <span data-ttu-id="11628-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="11628-465">msdyn_effort</span></span>                                     | <span data-ttu-id="11628-466">ne</span><span class="sxs-lookup"><span data-stu-id="11628-466">no</span></span>             | <span data-ttu-id="11628-467">ne</span><span class="sxs-lookup"><span data-stu-id="11628-467">no</span></span>           |
| <span data-ttu-id="11628-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="11628-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="11628-469">ne</span><span class="sxs-lookup"><span data-stu-id="11628-469">no</span></span>             | <span data-ttu-id="11628-470">ne</span><span class="sxs-lookup"><span data-stu-id="11628-470">no</span></span>           |
| <span data-ttu-id="11628-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="11628-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="11628-472">ne</span><span class="sxs-lookup"><span data-stu-id="11628-472">no</span></span>             | <span data-ttu-id="11628-473">ne</span><span class="sxs-lookup"><span data-stu-id="11628-473">no</span></span>           |
| <span data-ttu-id="11628-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="11628-474">msdyn_finish</span></span>                                     | <span data-ttu-id="11628-475">ne</span><span class="sxs-lookup"><span data-stu-id="11628-475">no</span></span>             | <span data-ttu-id="11628-476">ne</span><span class="sxs-lookup"><span data-stu-id="11628-476">no</span></span>           |
| <span data-ttu-id="11628-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="11628-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="11628-478">ne</span><span class="sxs-lookup"><span data-stu-id="11628-478">no</span></span>             | <span data-ttu-id="11628-479">ne</span><span class="sxs-lookup"><span data-stu-id="11628-479">no</span></span>           |
| <span data-ttu-id="11628-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="11628-480">msdyn_hours</span></span>                                      | <span data-ttu-id="11628-481">ne</span><span class="sxs-lookup"><span data-stu-id="11628-481">no</span></span>             | <span data-ttu-id="11628-482">ne</span><span class="sxs-lookup"><span data-stu-id="11628-482">no</span></span>           |
| <span data-ttu-id="11628-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="11628-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="11628-484">ne</span><span class="sxs-lookup"><span data-stu-id="11628-484">no</span></span>             | <span data-ttu-id="11628-485">ne</span><span class="sxs-lookup"><span data-stu-id="11628-485">no</span></span>           |
| <span data-ttu-id="11628-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="11628-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="11628-487">ne</span><span class="sxs-lookup"><span data-stu-id="11628-487">no</span></span>             | <span data-ttu-id="11628-488">ne</span><span class="sxs-lookup"><span data-stu-id="11628-488">no</span></span>           |
| <span data-ttu-id="11628-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="11628-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="11628-490">ne</span><span class="sxs-lookup"><span data-stu-id="11628-490">no</span></span>             | <span data-ttu-id="11628-491">ne</span><span class="sxs-lookup"><span data-stu-id="11628-491">no</span></span>           |
| <span data-ttu-id="11628-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="11628-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="11628-493">ne</span><span class="sxs-lookup"><span data-stu-id="11628-493">no</span></span>             | <span data-ttu-id="11628-494">ne</span><span class="sxs-lookup"><span data-stu-id="11628-494">no</span></span>           |
| <span data-ttu-id="11628-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="11628-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="11628-496">ne</span><span class="sxs-lookup"><span data-stu-id="11628-496">no</span></span>             | <span data-ttu-id="11628-497">ne</span><span class="sxs-lookup"><span data-stu-id="11628-497">no</span></span>           |
| <span data-ttu-id="11628-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="11628-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="11628-499">ne</span><span class="sxs-lookup"><span data-stu-id="11628-499">no</span></span>             | <span data-ttu-id="11628-500">ne</span><span class="sxs-lookup"><span data-stu-id="11628-500">no</span></span>           |
| <span data-ttu-id="11628-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="11628-501">msdyn_start</span></span>                                      | <span data-ttu-id="11628-502">ne</span><span class="sxs-lookup"><span data-stu-id="11628-502">no</span></span>             | <span data-ttu-id="11628-503">ne</span><span class="sxs-lookup"><span data-stu-id="11628-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="11628-504">Project</span><span class="sxs-lookup"><span data-stu-id="11628-504">Project</span></span>

| <span data-ttu-id="11628-505">**Logičko ime**</span><span class="sxs-lookup"><span data-stu-id="11628-505">**Logical name**</span></span>                       | <span data-ttu-id="11628-506">**Može da kreira**</span><span class="sxs-lookup"><span data-stu-id="11628-506">**Can create**</span></span> | <span data-ttu-id="11628-507">**Može da menja**</span><span class="sxs-lookup"><span data-stu-id="11628-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="11628-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="11628-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="11628-509">ne</span><span class="sxs-lookup"><span data-stu-id="11628-509">no</span></span>             | <span data-ttu-id="11628-510">ne</span><span class="sxs-lookup"><span data-stu-id="11628-510">no</span></span>           |
| <span data-ttu-id="11628-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="11628-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="11628-512">ne</span><span class="sxs-lookup"><span data-stu-id="11628-512">no</span></span>             | <span data-ttu-id="11628-513">ne</span><span class="sxs-lookup"><span data-stu-id="11628-513">no</span></span>           |
| <span data-ttu-id="11628-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="11628-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="11628-515">ne</span><span class="sxs-lookup"><span data-stu-id="11628-515">no</span></span>             | <span data-ttu-id="11628-516">ne</span><span class="sxs-lookup"><span data-stu-id="11628-516">no</span></span>           |
| <span data-ttu-id="11628-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="11628-518">ne</span><span class="sxs-lookup"><span data-stu-id="11628-518">no</span></span>             | <span data-ttu-id="11628-519">ne</span><span class="sxs-lookup"><span data-stu-id="11628-519">no</span></span>           |
| <span data-ttu-id="11628-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="11628-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="11628-521">ne</span><span class="sxs-lookup"><span data-stu-id="11628-521">no</span></span>             | <span data-ttu-id="11628-522">ne</span><span class="sxs-lookup"><span data-stu-id="11628-522">no</span></span>           |
| <span data-ttu-id="11628-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="11628-524">ne</span><span class="sxs-lookup"><span data-stu-id="11628-524">no</span></span>             | <span data-ttu-id="11628-525">ne</span><span class="sxs-lookup"><span data-stu-id="11628-525">no</span></span>           |
| <span data-ttu-id="11628-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="11628-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="11628-527">da</span><span class="sxs-lookup"><span data-stu-id="11628-527">yes</span></span>            | <span data-ttu-id="11628-528">ne</span><span class="sxs-lookup"><span data-stu-id="11628-528">no</span></span>           |
| <span data-ttu-id="11628-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="11628-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="11628-530">da</span><span class="sxs-lookup"><span data-stu-id="11628-530">yes</span></span>            | <span data-ttu-id="11628-531">ne</span><span class="sxs-lookup"><span data-stu-id="11628-531">no</span></span>           |
| <span data-ttu-id="11628-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="11628-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="11628-533">da</span><span class="sxs-lookup"><span data-stu-id="11628-533">yes</span></span>            | <span data-ttu-id="11628-534">ne</span><span class="sxs-lookup"><span data-stu-id="11628-534">no</span></span>           |
| <span data-ttu-id="11628-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="11628-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="11628-536">ne</span><span class="sxs-lookup"><span data-stu-id="11628-536">no</span></span>             | <span data-ttu-id="11628-537">ne</span><span class="sxs-lookup"><span data-stu-id="11628-537">no</span></span>           |
| <span data-ttu-id="11628-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="11628-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="11628-539">ne</span><span class="sxs-lookup"><span data-stu-id="11628-539">no</span></span>             | <span data-ttu-id="11628-540">ne</span><span class="sxs-lookup"><span data-stu-id="11628-540">no</span></span>           |
| <span data-ttu-id="11628-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="11628-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="11628-542">ne</span><span class="sxs-lookup"><span data-stu-id="11628-542">no</span></span>             | <span data-ttu-id="11628-543">ne</span><span class="sxs-lookup"><span data-stu-id="11628-543">no</span></span>           |
| <span data-ttu-id="11628-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="11628-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="11628-545">ne</span><span class="sxs-lookup"><span data-stu-id="11628-545">no</span></span>             | <span data-ttu-id="11628-546">ne</span><span class="sxs-lookup"><span data-stu-id="11628-546">no</span></span>           |
| <span data-ttu-id="11628-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="11628-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="11628-548">ne</span><span class="sxs-lookup"><span data-stu-id="11628-548">no</span></span>             | <span data-ttu-id="11628-549">ne</span><span class="sxs-lookup"><span data-stu-id="11628-549">no</span></span>           |
| <span data-ttu-id="11628-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="11628-550">msdyn_duration</span></span>                         | <span data-ttu-id="11628-551">ne</span><span class="sxs-lookup"><span data-stu-id="11628-551">no</span></span>             | <span data-ttu-id="11628-552">ne</span><span class="sxs-lookup"><span data-stu-id="11628-552">no</span></span>           |
| <span data-ttu-id="11628-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="11628-553">msdyn_effort</span></span>                           | <span data-ttu-id="11628-554">ne</span><span class="sxs-lookup"><span data-stu-id="11628-554">no</span></span>             | <span data-ttu-id="11628-555">ne</span><span class="sxs-lookup"><span data-stu-id="11628-555">no</span></span>           |
| <span data-ttu-id="11628-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="11628-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="11628-557">ne</span><span class="sxs-lookup"><span data-stu-id="11628-557">no</span></span>             | <span data-ttu-id="11628-558">ne</span><span class="sxs-lookup"><span data-stu-id="11628-558">no</span></span>           |
| <span data-ttu-id="11628-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="11628-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="11628-560">ne</span><span class="sxs-lookup"><span data-stu-id="11628-560">no</span></span>             | <span data-ttu-id="11628-561">ne</span><span class="sxs-lookup"><span data-stu-id="11628-561">no</span></span>           |
| <span data-ttu-id="11628-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="11628-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="11628-563">ne</span><span class="sxs-lookup"><span data-stu-id="11628-563">no</span></span>             | <span data-ttu-id="11628-564">ne</span><span class="sxs-lookup"><span data-stu-id="11628-564">no</span></span>           |
| <span data-ttu-id="11628-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="11628-565">msdyn_finish</span></span>                           | <span data-ttu-id="11628-566">da</span><span class="sxs-lookup"><span data-stu-id="11628-566">yes</span></span>            | <span data-ttu-id="11628-567">da</span><span class="sxs-lookup"><span data-stu-id="11628-567">yes</span></span>          |
| <span data-ttu-id="11628-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="11628-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="11628-569">ne</span><span class="sxs-lookup"><span data-stu-id="11628-569">no</span></span>             | <span data-ttu-id="11628-570">ne</span><span class="sxs-lookup"><span data-stu-id="11628-570">no</span></span>           |
| <span data-ttu-id="11628-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="11628-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="11628-572">ne</span><span class="sxs-lookup"><span data-stu-id="11628-572">no</span></span>             | <span data-ttu-id="11628-573">ne</span><span class="sxs-lookup"><span data-stu-id="11628-573">no</span></span>           |
| <span data-ttu-id="11628-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="11628-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="11628-575">ne</span><span class="sxs-lookup"><span data-stu-id="11628-575">no</span></span>             | <span data-ttu-id="11628-576">ne</span><span class="sxs-lookup"><span data-stu-id="11628-576">no</span></span>           |
| <span data-ttu-id="11628-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="11628-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="11628-578">ne</span><span class="sxs-lookup"><span data-stu-id="11628-578">no</span></span>             | <span data-ttu-id="11628-579">ne</span><span class="sxs-lookup"><span data-stu-id="11628-579">no</span></span>           |
| <span data-ttu-id="11628-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="11628-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="11628-581">ne</span><span class="sxs-lookup"><span data-stu-id="11628-581">no</span></span>             | <span data-ttu-id="11628-582">ne</span><span class="sxs-lookup"><span data-stu-id="11628-582">no</span></span>           |
| <span data-ttu-id="11628-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="11628-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="11628-584">ne</span><span class="sxs-lookup"><span data-stu-id="11628-584">no</span></span>             | <span data-ttu-id="11628-585">ne</span><span class="sxs-lookup"><span data-stu-id="11628-585">no</span></span>           |
| <span data-ttu-id="11628-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="11628-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="11628-587">ne</span><span class="sxs-lookup"><span data-stu-id="11628-587">no</span></span>             | <span data-ttu-id="11628-588">ne</span><span class="sxs-lookup"><span data-stu-id="11628-588">no</span></span>           |
| <span data-ttu-id="11628-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="11628-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="11628-590">ne</span><span class="sxs-lookup"><span data-stu-id="11628-590">no</span></span>             | <span data-ttu-id="11628-591">ne</span><span class="sxs-lookup"><span data-stu-id="11628-591">no</span></span>           |
| <span data-ttu-id="11628-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="11628-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="11628-593">ne</span><span class="sxs-lookup"><span data-stu-id="11628-593">no</span></span>             | <span data-ttu-id="11628-594">ne</span><span class="sxs-lookup"><span data-stu-id="11628-594">no</span></span>           |
| <span data-ttu-id="11628-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="11628-596">ne</span><span class="sxs-lookup"><span data-stu-id="11628-596">no</span></span>             | <span data-ttu-id="11628-597">ne</span><span class="sxs-lookup"><span data-stu-id="11628-597">no</span></span>           |
| <span data-ttu-id="11628-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="11628-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="11628-599">ne</span><span class="sxs-lookup"><span data-stu-id="11628-599">no</span></span>             | <span data-ttu-id="11628-600">ne</span><span class="sxs-lookup"><span data-stu-id="11628-600">no</span></span>           |
| <span data-ttu-id="11628-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="11628-602">ne</span><span class="sxs-lookup"><span data-stu-id="11628-602">no</span></span>             | <span data-ttu-id="11628-603">ne</span><span class="sxs-lookup"><span data-stu-id="11628-603">no</span></span>           |
| <span data-ttu-id="11628-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="11628-604">msdyn_progress</span></span>                         | <span data-ttu-id="11628-605">ne</span><span class="sxs-lookup"><span data-stu-id="11628-605">no</span></span>             | <span data-ttu-id="11628-606">ne</span><span class="sxs-lookup"><span data-stu-id="11628-606">no</span></span>           |
| <span data-ttu-id="11628-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="11628-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="11628-608">ne</span><span class="sxs-lookup"><span data-stu-id="11628-608">no</span></span>             | <span data-ttu-id="11628-609">ne</span><span class="sxs-lookup"><span data-stu-id="11628-609">no</span></span>           |
| <span data-ttu-id="11628-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="11628-611">ne</span><span class="sxs-lookup"><span data-stu-id="11628-611">no</span></span>             | <span data-ttu-id="11628-612">ne</span><span class="sxs-lookup"><span data-stu-id="11628-612">no</span></span>           |
| <span data-ttu-id="11628-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="11628-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="11628-614">ne</span><span class="sxs-lookup"><span data-stu-id="11628-614">no</span></span>             | <span data-ttu-id="11628-615">ne</span><span class="sxs-lookup"><span data-stu-id="11628-615">no</span></span>           |
| <span data-ttu-id="11628-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="11628-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="11628-617">ne</span><span class="sxs-lookup"><span data-stu-id="11628-617">no</span></span>             | <span data-ttu-id="11628-618">ne</span><span class="sxs-lookup"><span data-stu-id="11628-618">no</span></span>           |
| <span data-ttu-id="11628-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="11628-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="11628-620">ne</span><span class="sxs-lookup"><span data-stu-id="11628-620">no</span></span>             | <span data-ttu-id="11628-621">ne</span><span class="sxs-lookup"><span data-stu-id="11628-621">no</span></span>           |
| <span data-ttu-id="11628-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="11628-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="11628-623">ne</span><span class="sxs-lookup"><span data-stu-id="11628-623">no</span></span>             | <span data-ttu-id="11628-624">ne</span><span class="sxs-lookup"><span data-stu-id="11628-624">no</span></span>           |
| <span data-ttu-id="11628-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="11628-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="11628-626">ne</span><span class="sxs-lookup"><span data-stu-id="11628-626">no</span></span>             | <span data-ttu-id="11628-627">ne</span><span class="sxs-lookup"><span data-stu-id="11628-627">no</span></span>           |
| <span data-ttu-id="11628-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="11628-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="11628-629">ne</span><span class="sxs-lookup"><span data-stu-id="11628-629">no</span></span>             | <span data-ttu-id="11628-630">ne</span><span class="sxs-lookup"><span data-stu-id="11628-630">no</span></span>           |
| <span data-ttu-id="11628-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="11628-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="11628-632">ne</span><span class="sxs-lookup"><span data-stu-id="11628-632">no</span></span>             | <span data-ttu-id="11628-633">ne</span><span class="sxs-lookup"><span data-stu-id="11628-633">no</span></span>           |
| <span data-ttu-id="11628-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="11628-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="11628-635">ne</span><span class="sxs-lookup"><span data-stu-id="11628-635">no</span></span>             | <span data-ttu-id="11628-636">ne</span><span class="sxs-lookup"><span data-stu-id="11628-636">no</span></span>           |
| <span data-ttu-id="11628-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="11628-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="11628-638">ne</span><span class="sxs-lookup"><span data-stu-id="11628-638">no</span></span>             | <span data-ttu-id="11628-639">ne</span><span class="sxs-lookup"><span data-stu-id="11628-639">no</span></span>           |
| <span data-ttu-id="11628-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="11628-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="11628-641">ne</span><span class="sxs-lookup"><span data-stu-id="11628-641">no</span></span>             | <span data-ttu-id="11628-642">ne</span><span class="sxs-lookup"><span data-stu-id="11628-642">no</span></span>           |
| <span data-ttu-id="11628-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="11628-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="11628-644">ne</span><span class="sxs-lookup"><span data-stu-id="11628-644">no</span></span>             | <span data-ttu-id="11628-645">ne</span><span class="sxs-lookup"><span data-stu-id="11628-645">no</span></span>           |
| <span data-ttu-id="11628-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="11628-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="11628-647">ne</span><span class="sxs-lookup"><span data-stu-id="11628-647">no</span></span>             | <span data-ttu-id="11628-648">ne</span><span class="sxs-lookup"><span data-stu-id="11628-648">no</span></span>           |
| <span data-ttu-id="11628-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="11628-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="11628-650">ne</span><span class="sxs-lookup"><span data-stu-id="11628-650">no</span></span>             | <span data-ttu-id="11628-651">ne</span><span class="sxs-lookup"><span data-stu-id="11628-651">no</span></span>           |
| <span data-ttu-id="11628-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="11628-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="11628-653">ne</span><span class="sxs-lookup"><span data-stu-id="11628-653">no</span></span>             | <span data-ttu-id="11628-654">ne</span><span class="sxs-lookup"><span data-stu-id="11628-654">no</span></span>           |
| <span data-ttu-id="11628-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="11628-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="11628-656">ne</span><span class="sxs-lookup"><span data-stu-id="11628-656">no</span></span>             | <span data-ttu-id="11628-657">ne</span><span class="sxs-lookup"><span data-stu-id="11628-657">no</span></span>           |
| <span data-ttu-id="11628-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="11628-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="11628-659">ne</span><span class="sxs-lookup"><span data-stu-id="11628-659">no</span></span>             | <span data-ttu-id="11628-660">ne</span><span class="sxs-lookup"><span data-stu-id="11628-660">no</span></span>           |
| <span data-ttu-id="11628-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="11628-662">ne</span><span class="sxs-lookup"><span data-stu-id="11628-662">no</span></span>             | <span data-ttu-id="11628-663">ne</span><span class="sxs-lookup"><span data-stu-id="11628-663">no</span></span>           |
| <span data-ttu-id="11628-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="11628-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="11628-665">ne</span><span class="sxs-lookup"><span data-stu-id="11628-665">no</span></span>             | <span data-ttu-id="11628-666">ne</span><span class="sxs-lookup"><span data-stu-id="11628-666">no</span></span>           |
| <span data-ttu-id="11628-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="11628-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="11628-668">ne</span><span class="sxs-lookup"><span data-stu-id="11628-668">no</span></span>             | <span data-ttu-id="11628-669">ne</span><span class="sxs-lookup"><span data-stu-id="11628-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="11628-670">Ograničenja i poznati problemi</span><span class="sxs-lookup"><span data-stu-id="11628-670">Limitations and known issues</span></span>
<span data-ttu-id="11628-671">Sledi lista ograničenja i poznatih problema:</span><span class="sxs-lookup"><span data-stu-id="11628-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="11628-672">API-je za raspored mogu da koriste samo **korisnici sa licencom za Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="11628-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="11628-673">Ne mogu ih koristiti:</span><span class="sxs-lookup"><span data-stu-id="11628-673">They can't be used by:</span></span>
    - <span data-ttu-id="11628-674">Korisnici aplikacije</span><span class="sxs-lookup"><span data-stu-id="11628-674">Application users</span></span>
    - <span data-ttu-id="11628-675">Korisnici sistema</span><span class="sxs-lookup"><span data-stu-id="11628-675">System users</span></span>
    - <span data-ttu-id="11628-676">Korisnici integracije</span><span class="sxs-lookup"><span data-stu-id="11628-676">Integration users</span></span>
    - <span data-ttu-id="11628-677">Ostali korisnici koji nemaju potrebnu licencu</span><span class="sxs-lookup"><span data-stu-id="11628-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="11628-678">Svaki **OperationSet entitet** može da ima najviše 100 operacija.</span><span class="sxs-lookup"><span data-stu-id="11628-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="11628-679">Svaki korisnik može da ima najviše 10 otvorenih **OperationSet entiteta**.</span><span class="sxs-lookup"><span data-stu-id="11628-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="11628-680">Project Operations trenutno podržava maksimalno 500 ukupnih zadataka na projektu.</span><span class="sxs-lookup"><span data-stu-id="11628-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="11628-681">Status greške i evidencije grešaka **OperationSet entiteta** trenutno nisu dostupne.</span><span class="sxs-lookup"><span data-stu-id="11628-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="11628-682">Ograničenja i granice projekata i zadataka</span><span class="sxs-lookup"><span data-stu-id="11628-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="11628-683">Rukovanje greškama</span><span class="sxs-lookup"><span data-stu-id="11628-683">Error handling</span></span>

   - <span data-ttu-id="11628-684">Da biste pregledali greške generisane iz skupova operacija, idite na **Podešavanja** \> **Zakaži integraciju** \> **Skupovi operacija**.</span><span class="sxs-lookup"><span data-stu-id="11628-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="11628-685">Da biste pregledali greške generisane uslugom planiranja projekata, idite na **Podešavanja** \> **Zakaži integraciju** \> **Dnevnici grešaka PSS-a**.</span><span class="sxs-lookup"><span data-stu-id="11628-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="11628-686">Primer scenarija</span><span class="sxs-lookup"><span data-stu-id="11628-686">Sample scenario</span></span>

<span data-ttu-id="11628-687">U ovom scenariju, kreiraćete projekat, člana tima, četiri zadatka i dva zadatka resursa.</span><span class="sxs-lookup"><span data-stu-id="11628-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="11628-688">Zatim ćete ažurirati jedan zadatak, ažurirati projekat, izbrisati jedan zadatak, izbrisati jednu dodelu resursa i kreirati zavisnost zadatka.</span><span class="sxs-lookup"><span data-stu-id="11628-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="11628-689">Dodatni primeri</span><span class="sxs-lookup"><span data-stu-id="11628-689">Additional samples</span></span>

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
