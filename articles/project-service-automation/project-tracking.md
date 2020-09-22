---
title: Napredak projekta i troškovi korišćenja
description: Ova tema pruža informacije o tome kako da pratite napredak projekta i troškove korišćenja.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755224"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="e1678-103">Napredak projekta i troškovi korišćenja</span><span class="sxs-lookup"><span data-stu-id="e1678-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e1678-104">Potreba da se prati napredak u odnosu na raspored razlikuje se od delatnosti do delatnosti.</span><span class="sxs-lookup"><span data-stu-id="e1678-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="e1678-105">Neke delatnosti obavljaju praćenje na najdetaljnijem nivou, dok druge to rade na višem nivou.</span><span class="sxs-lookup"><span data-stu-id="e1678-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="e1678-106">Ova tema pokazuje kako obaviti zakazivanje da biste ispunili potrebe svoje organizacije.</span><span class="sxs-lookup"><span data-stu-id="e1678-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="e1678-107">Prikaz za praćenje angažovanja</span><span class="sxs-lookup"><span data-stu-id="e1678-107">Effort tracking view</span></span>

<span data-ttu-id="e1678-108">Prikaz **Praćenje aktivnosti** prati napredak zadataka u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="e1678-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="e1678-109">Poredi stvarno utrošene sate angažovanja na zadatku sa planiranim satima angažovanja za taj zadatak.</span><span class="sxs-lookup"><span data-stu-id="e1678-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="e1678-110">PSA koristi sledeće formule za izračunavanje metrika za praćenje:</span><span class="sxs-lookup"><span data-stu-id="e1678-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="e1678-111">Procenat napretka = Stvarno vreme angažovanja do danas ÷ Planirano angažovanje za zadatak</span><span class="sxs-lookup"><span data-stu-id="e1678-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="e1678-112">Procena do završetka (ETC) = Planirano angažovanje - Stvarno vreme angažovanja do danas</span><span class="sxs-lookup"><span data-stu-id="e1678-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="e1678-113">Procena po završetku (EAC) = Preostalo angaživanje + Stvarno vreme angažovanja do danas</span><span class="sxs-lookup"><span data-stu-id="e1678-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="e1678-114">Odstupanje od projektovanog angažovanja = Planirano angažovanje - EAC</span><span class="sxs-lookup"><span data-stu-id="e1678-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="e1678-115">PSA prikazuje projekciju odstupanja od angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="e1678-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="e1678-116">Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="e1678-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="e1678-117">Stoga, zaostaje za planom.</span><span class="sxs-lookup"><span data-stu-id="e1678-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="e1678-118">Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="e1678-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="e1678-119">Stoga će biti dovršen pre nego što je planirano.</span><span class="sxs-lookup"><span data-stu-id="e1678-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="e1678-120">Ponovno projektovanje angažovanja</span><span class="sxs-lookup"><span data-stu-id="e1678-120">Re-projecting effort</span></span>

<span data-ttu-id="e1678-121">Uobičajeno je da menadžer projekta revidira originalne procene zadatka.</span><span class="sxs-lookup"><span data-stu-id="e1678-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e1678-122">Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta.</span><span class="sxs-lookup"><span data-stu-id="e1678-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e1678-123">Međutim, ne preporučujemo da menadžeri projekta menjaju osnovne vrednosti zato što osnovne vrednosti projekta predstavljaju uspostavljen izvor istine za raspored projekta i procenu troškova, a svi zainteresovani za projekat su je prihvatili.</span><span class="sxs-lookup"><span data-stu-id="e1678-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e1678-124">Postoje dva načina na koje menadžer projekta može ponovo da projektuje angažovanje na zadacima:</span><span class="sxs-lookup"><span data-stu-id="e1678-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="e1678-125">Izmenite podrazumevani ETC novom procenom stvarnog preostalog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="e1678-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e1678-126">Izmenite podrazumevani procenat napretka novom procenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="e1678-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e1678-127">Svaki od ovih pristupa dovodi do toga da se ponovo izračunaju ETC, EAC i procenat napretka zadatka, kao i odstupanje od projektovanog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="e1678-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e1678-128">EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.</span><span class="sxs-lookup"><span data-stu-id="e1678-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="e1678-129">Ponovna projekcija angažovanja za rezimirane zadatke</span><span class="sxs-lookup"><span data-stu-id="e1678-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="e1678-130">Angažovanje na rezimiranim zadacima ili zadacima kontejnera može se ponovno projektovati.</span><span class="sxs-lookup"><span data-stu-id="e1678-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="e1678-131">Bez obzira da li korisnik ponovo projektuje pomoću preostalog angažovanja ili procenta napretka rezimiranih zadataka, započinje sledeći niz izračunavanja:</span><span class="sxs-lookup"><span data-stu-id="e1678-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="e1678-132">EAC, ETC i procenat napretka zadatka se izračunavaju.</span><span class="sxs-lookup"><span data-stu-id="e1678-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="e1678-133">Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni EAC za zadatak.</span><span class="sxs-lookup"><span data-stu-id="e1678-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="e1678-134">Izračunava se novi EAC za svaki od pojedinačnih zadataka sve do zadataka čvora lista.</span><span class="sxs-lookup"><span data-stu-id="e1678-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="e1678-135">Nadređeni zadaci na koje ovo utiče, sve do čvorova lista, imaju ponovno izračunat ETC i procenat napretka na osnovu EAC vrednosti.</span><span class="sxs-lookup"><span data-stu-id="e1678-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="e1678-136">To rezultira novom projekcijom odstupanja od angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="e1678-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="e1678-137">Ponovo se izračunavaju EAC-ovi rezimiranih zadataka sve do osnovnog čvora.</span><span class="sxs-lookup"><span data-stu-id="e1678-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="e1678-138">Prikaz praćenja troškova</span><span class="sxs-lookup"><span data-stu-id="e1678-138">Cost tracking view</span></span> 

<span data-ttu-id="e1678-139">Prikaz **Praćenje troškova** upoređuje stvarne troškove potrošene na zadatak i planirane troškove zadatka.</span><span class="sxs-lookup"><span data-stu-id="e1678-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="e1678-140">Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procena troškova.</span><span class="sxs-lookup"><span data-stu-id="e1678-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="e1678-141">PSA koristi sledeće formule za izračunavanje metrika za praćenje:</span><span class="sxs-lookup"><span data-stu-id="e1678-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="e1678-142">Procenat ostvarenih troškova = Stvarni troškovi do danas ÷ Planirani troškovi zadatka</span><span class="sxs-lookup"><span data-stu-id="e1678-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="e1678-143">Troškovi do završetka (CTC) = Planirani troškovi - Stvarni troškovi ostvareni do danas</span><span class="sxs-lookup"><span data-stu-id="e1678-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="e1678-144">EAC = CTC + Stvarni troškovi ostvareni do danas</span><span class="sxs-lookup"><span data-stu-id="e1678-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="e1678-145">Odstupanje od projektovanih troškova = Planirani troškovi - EAC</span><span class="sxs-lookup"><span data-stu-id="e1678-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="e1678-146">Projekcija odstupanja od troškova je prikazana na zadatku.</span><span class="sxs-lookup"><span data-stu-id="e1678-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="e1678-147">Ako je EAC veći od planiranih troškova, predviđa se da će zadatak koštati više nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="e1678-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="e1678-148">Zbog toga ima trend prekoračenja budžeta.</span><span class="sxs-lookup"><span data-stu-id="e1678-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="e1678-149">Ako je EAC manji od planiranih troškova, predviđa se da će zadatak koštati manje nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="e1678-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="e1678-150">Zbog toga ima trend neiskorišćenog budžeta.</span><span class="sxs-lookup"><span data-stu-id="e1678-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="e1678-151">Ponovna projekcija troškova od strane menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="e1678-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="e1678-152">Kada se angažovanje ponovo projektuje, CTC, EAC, procenat ostvarenih troškova i odstupanja od projektovanih troškova se ponovo izračunavaju u prikazu **Praćenje troškova**.</span><span class="sxs-lookup"><span data-stu-id="e1678-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="e1678-153">Rezime statusa projekta</span><span class="sxs-lookup"><span data-stu-id="e1678-153">Project status summary</span></span>

<span data-ttu-id="e1678-154">Podaci za praćenje u prikazima **Praćenje aktivnosti** i **Praćenje troškova** prikazuju napredak i troškove korišćenja na nivou osnovnog čvora projekta, rezimiranih zadataka i zadataka čvorova lista.</span><span class="sxs-lookup"><span data-stu-id="e1678-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="e1678-155">Odeljak **Status** na stranici **Entitet projekta** prikazuje rezime statusa na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="e1678-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="e1678-156">Polja rezimea statusa</span><span class="sxs-lookup"><span data-stu-id="e1678-156">Status summary fields</span></span>

<span data-ttu-id="e1678-157">Polje **Opšti status projekta** je polje koje se može uređivati i koje pokazuje opšti status projekta.</span><span class="sxs-lookup"><span data-stu-id="e1678-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e1678-158">Koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="e1678-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="e1678-159">Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="e1678-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="e1678-160">Polje **Status ažuriran dana** nije moguće uređivati i vrednost je vremenska oznaka koja pokazuje kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="e1678-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="e1678-161">Polja **Performanse rasporeda** i **Performanse troškova** su podešena od datuma praćenja.</span><span class="sxs-lookup"><span data-stu-id="e1678-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="e1678-162">Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete podesiti ova polja na **Pre plana**.</span><span class="sxs-lookup"><span data-stu-id="e1678-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="e1678-163">Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, možete ih podesiti na **Zaostaje za planom**.</span><span class="sxs-lookup"><span data-stu-id="e1678-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
