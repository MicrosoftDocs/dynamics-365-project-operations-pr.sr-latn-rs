---
title: Promene u upravljanju resursima (Project Service Automation 3.x)
description: Ova tema pruža informacije o promenama u oblasti upravljanja resursima.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083771"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="b8549-103">Promene u upravljanju resursima (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="b8549-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="b8549-104">Odeljci ove teme pružaju informacije o promenama koje su izvršene u oblasti upravljanja resursima u usluzi Dynamics 365 Project Service Automation verzije 3.x.</span><span class="sxs-lookup"><span data-stu-id="b8549-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="b8549-105">Procene za projekat</span><span class="sxs-lookup"><span data-stu-id="b8549-105">Project estimates</span></span>

<span data-ttu-id="b8549-106">Umesto da se zasniva na entitetu **msdyn\_projecttask** ( **Projektni zadatak** ), procene projekata se zasnivaju na entitetu **msdyn\_resourceassignment** ( **Dodela resursa** ).</span><span class="sxs-lookup"><span data-stu-id="b8549-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="b8549-107">Dodele resursa su postale „izvor istine“ za zakazivanje zadataka i određivanje cena zadataka.</span><span class="sxs-lookup"><span data-stu-id="b8549-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="b8549-108">Zadaci stavke</span><span class="sxs-lookup"><span data-stu-id="b8549-108">Line tasks</span></span>

<span data-ttu-id="b8549-109">U aplikaciji PSA 3.x, zadaci stavke su zastareli.</span><span class="sxs-lookup"><span data-stu-id="b8549-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="b8549-110">Zadaci sada ukazuju na ceo zadatak umesto na zadatke stavke.</span><span class="sxs-lookup"><span data-stu-id="b8549-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="b8549-111">Sledeći primer prikazuje kako se zadatak koji se zove „Probni zadatak“ dodeljuje A i B članovima tima u starijim verzijama aplikacije PSA i aplikaciji PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="b8549-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="b8549-112">**Pre verzije aplikacije PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="b8549-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="b8549-113">Probni zadatak</span><span class="sxs-lookup"><span data-stu-id="b8549-113">Test task</span></span>

        - <span data-ttu-id="b8549-114">Probni zadatak – 1. zadatak stavke</span><span class="sxs-lookup"><span data-stu-id="b8549-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="b8549-115">Dodela članu A</span><span class="sxs-lookup"><span data-stu-id="b8549-115">Assignment to A</span></span>

        - <span data-ttu-id="b8549-116">Probni zadatak – 2. zadatak stavke</span><span class="sxs-lookup"><span data-stu-id="b8549-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="b8549-117">Dodela članu B</span><span class="sxs-lookup"><span data-stu-id="b8549-117">Assignment to B</span></span>

- <span data-ttu-id="b8549-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="b8549-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="b8549-119">Probni zadatak</span><span class="sxs-lookup"><span data-stu-id="b8549-119">Test task</span></span>

        - <span data-ttu-id="b8549-120">Dodela članu A</span><span class="sxs-lookup"><span data-stu-id="b8549-120">Assignment to A</span></span>
        - <span data-ttu-id="b8549-121">Dodela članu B</span><span class="sxs-lookup"><span data-stu-id="b8549-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="b8549-122">Neodeljeni zadatak</span><span class="sxs-lookup"><span data-stu-id="b8549-122">Unassigned assignment</span></span>

<span data-ttu-id="b8549-123">U aplikaciji PSA 3.x, nedodeljeni zadatak je zadatak koji je dodeljen članu tima koji ima nultu vrednost ( **NULL** ) i resursu sa nultom vrednošću ( **NULL** ).</span><span class="sxs-lookup"><span data-stu-id="b8549-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="b8549-124">Nedodeljeni zadaci mogu se pojaviti u nekoliko scenarija:</span><span class="sxs-lookup"><span data-stu-id="b8549-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="b8549-125">Ako je zadatak kreiran, ali još uvek nije dodeljen nijednom članu tima, uvek se kreira nedodeljeni zadatak.</span><span class="sxs-lookup"><span data-stu-id="b8549-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="b8549-126">Ako se uklone svi dodeljeni korisnici iz zadatka, za taj zadatak se ponovo kreira nedodeljeni zadatak.</span><span class="sxs-lookup"><span data-stu-id="b8549-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="b8549-127">Polja za zakazivanje u entitetu Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="b8549-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="b8549-128">Polja u entitetu **msdyn\_projecttask** su zastarela ili premeštena u entitet **msdyn\_resourceassignment** ili se sada navode u entitetu **msdyn\_projectteam** ( **Član projektnog tima** ).</span><span class="sxs-lookup"><span data-stu-id="b8549-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="b8549-129">Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="b8549-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b8549-130">Novo polje u entitetu msdyn\_resourceassignment (dodela resursa)</span><span class="sxs-lookup"><span data-stu-id="b8549-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="b8549-131">Komentar</span><span class="sxs-lookup"><span data-stu-id="b8549-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="b8549-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="b8549-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="b8549-133">Nijedno</span><span class="sxs-lookup"><span data-stu-id="b8549-133">None</span></span> | |
| <span data-ttu-id="b8549-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="b8549-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="b8549-135">Nijedno</span><span class="sxs-lookup"><span data-stu-id="b8549-135">None</span></span> | |
| <span data-ttu-id="b8549-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="b8549-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="b8549-137">Nijedno</span><span class="sxs-lookup"><span data-stu-id="b8549-137">None</span></span> | |
| <span data-ttu-id="b8549-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="b8549-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="b8549-139">Nijedno</span><span class="sxs-lookup"><span data-stu-id="b8549-139">None</span></span> | |
| <span data-ttu-id="b8549-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="b8549-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="b8549-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="b8549-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="b8549-142">Format strukture podataka JSON (JavaScript Object Notation) koja se čuva u polju je promenjen.</span><span class="sxs-lookup"><span data-stu-id="b8549-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="b8549-143">Zakazivanje skice</span><span class="sxs-lookup"><span data-stu-id="b8549-143">Schedule contour</span></span>

<span data-ttu-id="b8549-144">Skica rasporeda se čuva u polju **Planirani rad** ( **msdyn\_plannedwork** ) svakog entiteta **Dodela resursa** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="b8549-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="b8549-145">Struktura</span><span class="sxs-lookup"><span data-stu-id="b8549-145">Structure</span></span>

<span data-ttu-id="b8549-146">Nova struktura skice rasporeda sastoji se od fleksibilnih delića vremena koji su definisani za svaki dan rasporeda.</span><span class="sxs-lookup"><span data-stu-id="b8549-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="b8549-147">Svaki delić vremena ima sledeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="b8549-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="b8549-148">**Početak** - Početak radnog vremena za dan, prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="b8549-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="b8549-149">**Kraj** - Kraj radnog vremena za dan, prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="b8549-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="b8549-150">**Radno vreme** - Broj sati koji su dodeljeni u danu.</span><span class="sxs-lookup"><span data-stu-id="b8549-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="b8549-151">**Primer**</span><span class="sxs-lookup"><span data-stu-id="b8549-151">**Example**</span></span>

<span data-ttu-id="b8549-152">Ovaj primer koristi kalendar projekta gde je radni dan od 9:00 do 17:00 u vremenskoj zoni UTC-8.</span><span class="sxs-lookup"><span data-stu-id="b8549-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="b8549-153">Automatsko zakazivanje i ručno zakazivanje</span><span class="sxs-lookup"><span data-stu-id="b8549-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="b8549-154">Ako je zadatak automatski zakazan, sati se učitavaju unapred, a trajanje zadatka može biti smanjeno.</span><span class="sxs-lookup"><span data-stu-id="b8549-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="b8549-155">**Primer**</span><span class="sxs-lookup"><span data-stu-id="b8549-155">**Example**</span></span>

<span data-ttu-id="b8549-156">Sledeći zadatak je automatski zakazan za 18 sati tokom tri dana (od 3. do 5. decembra 2018. godine).</span><span class="sxs-lookup"><span data-stu-id="b8549-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="b8549-157">Ako je zadatak ručno zakazan, sati su ravnomerno raspoređeni na sve datume.</span><span class="sxs-lookup"><span data-stu-id="b8549-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="b8549-158">**Primer**</span><span class="sxs-lookup"><span data-stu-id="b8549-158">**Example**</span></span>

<span data-ttu-id="b8549-159">Sledeći zadatak je ručno zakazan za 18 sati tokom tri dana (od 3. do 5. decembra 2018. godine).</span><span class="sxs-lookup"><span data-stu-id="b8549-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="b8549-160">Jedinica dodele</span><span class="sxs-lookup"><span data-stu-id="b8549-160">Assignment unit</span></span>

<span data-ttu-id="b8549-161">Jedinica dodele zastarela je u aplikaciji PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="b8549-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="b8549-162">Sati angažovanja na zadatku sada su ravnomerno podeljeni, po danu, na sve dodeljene resurse.</span><span class="sxs-lookup"><span data-stu-id="b8549-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="b8549-163">**Primer**</span><span class="sxs-lookup"><span data-stu-id="b8549-163">**Example**</span></span>

<span data-ttu-id="b8549-164">U ovom primeru, zadatak je dodeljen na dva resursa i automatski je zakazan za 36 sati tokom tri dana (od 3. do 5. decembra 2018. godine).</span><span class="sxs-lookup"><span data-stu-id="b8549-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="b8549-165">1. dodela:</span><span class="sxs-lookup"><span data-stu-id="b8549-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="b8549-166">2. dodela:</span><span class="sxs-lookup"><span data-stu-id="b8549-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="b8549-167">Dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="b8549-167">Pricing dimensions</span></span>

<span data-ttu-id="b8549-168">U aplikaciji PSA 3.x, polja dimenzija za određivanje cena, specifična za resurse (kao što su **Uloga** i **Organizaciona jedinica** ) su uklonjeni iz entiteta **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="b8549-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="b8549-169">Ova polja se sada mogu preuzeti od odgovarajućeg člana projektnog tima ( **msdyn\_projectteam** ) za dodelu resursa ( **msdyn\_resourceassignment** ) kada se generišu procene projekata.</span><span class="sxs-lookup"><span data-stu-id="b8549-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="b8549-170">Novo polje, **msdyn\_organizationalunit** , je dodato u entitet **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="b8549-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="b8549-171">Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="b8549-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b8549-172">Polje u entitetu msdyn\_projectteam (član projektnog tima) koje se koristi umesto toga</span><span class="sxs-lookup"><span data-stu-id="b8549-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="b8549-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b8549-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="b8549-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="b8549-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="b8549-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="b8549-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="b8549-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="b8549-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="b8549-177">Skiciranja</span><span class="sxs-lookup"><span data-stu-id="b8549-177">Contours</span></span>

<span data-ttu-id="b8549-178">Polja sa skicama za određivanje cena i procene su zastarela u entitetu **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="b8549-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="b8549-179">Premeštena su u entitet **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="b8549-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="b8549-180">Zastarelo polje u entitetu msdyn\_projecttask (projektni zadatak)</span><span class="sxs-lookup"><span data-stu-id="b8549-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="b8549-181">Novo polje u entitetu msdyn\_resourceassignment (dodela resursa)</span><span class="sxs-lookup"><span data-stu-id="b8549-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="b8549-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="b8549-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="b8549-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="b8549-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="b8549-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="b8549-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="b8549-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="b8549-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="b8549-186">Sledeća polja su dodata u entitet **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="b8549-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="b8549-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b8549-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="b8549-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b8549-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="b8549-189">Sledeća polja za planirane, stvarne i preostale troškove i prodaju nepromenjena su u entitetu **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="b8549-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="b8549-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="b8549-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="b8549-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="b8549-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="b8549-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="b8549-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="b8549-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="b8549-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="b8549-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="b8549-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="b8549-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="b8549-195">msdyn\_remainingsales</span></span>
