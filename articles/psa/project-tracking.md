---
title: Napredak projekta i troškovi korišćenja
description: Ova tema pruža informacije o praćenju napretka projekta i troškova korišćenja.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083741"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="9e0f2-103">Napredak projekta i troškovi korišćenja</span><span class="sxs-lookup"><span data-stu-id="9e0f2-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9e0f2-104">Potreba da se prati napredak u odnosu na raspored razlikuje se od delatnosti do delatnosti.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="9e0f2-105">Neke delatnosti obavljaju praćenje na najdetaljnijem nivou, dok druge to rade na višem nivou.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="9e0f2-106">Ova tema pokazuje kako obaviti zakazivanje da biste ispunili potrebe svoje organizacije.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="9e0f2-107">Prikaz za praćenje angažovanja</span><span class="sxs-lookup"><span data-stu-id="9e0f2-107">Effort tracking view</span></span>

<span data-ttu-id="9e0f2-108">Prikaz **Praćenje aktivnosti** prati napredak zadataka u rasporedu.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="9e0f2-109">Prikaz poredi stvarno utrošene časove angažovanja na zadatku prema planiranim časovima angažovanja za zadatak.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="9e0f2-110">Project Service Automation koristi sledeće formule za izračunavanje metrika za praćenje:</span><span class="sxs-lookup"><span data-stu-id="9e0f2-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="9e0f2-111">U početku na kreiranju zadatka: Planirani troškovi će biti postavljeni na procenjene troškove po završetku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="9e0f2-112">Kada se stvarne vrednosti evidentiraju u zadatku, sledi izračunavanje na osnovu prikaza praćenja za angažovanje</span><span class="sxs-lookup"><span data-stu-id="9e0f2-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="9e0f2-113">Procenat napretka = Stvarno vreme angažovanja do danas ÷ Procena pri završetku (EAC)</span><span class="sxs-lookup"><span data-stu-id="9e0f2-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="9e0f2-114">Procena do završetka (ETC) = Procena pri završetku (EAC) – Stvarno vreme angažovanja do danas</span><span class="sxs-lookup"><span data-stu-id="9e0f2-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="9e0f2-115">EAC = Preostalo angažovanje + Stvarno vreme angažovanja do danas</span><span class="sxs-lookup"><span data-stu-id="9e0f2-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="9e0f2-116">Odstupanje od projektovanog angažovanja = Planirano angažovanje - EAC</span><span class="sxs-lookup"><span data-stu-id="9e0f2-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="9e0f2-117">Project Service Automation prikazuje projekciju odstupanja od angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="9e0f2-118">Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="9e0f2-119">Stoga, zaostaje za planom.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="9e0f2-120">Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="9e0f2-121">Stoga će biti dovršen pre nego što je planirano.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="9e0f2-122">Ponovno projektovanje angažovanja</span><span class="sxs-lookup"><span data-stu-id="9e0f2-122">Reprojecting effort</span></span>

<span data-ttu-id="9e0f2-123">Uobičajeno je da menadžer projekta revidira originalne procene zadatka.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="9e0f2-124">Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="9e0f2-125">Međutim, ne preporučujemo da menadžeri projekta menjaju osnovne vrednosti zato što osnovne vrednosti projekta predstavljaju uspostavljen izvor istine za raspored projekta i procenu troškova, a svi zainteresovani za projekat su je prihvatili.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="9e0f2-126">Postoje dva načina na koje menadžer projekta može ponovo da projektuje angažovanje na zadacima:</span><span class="sxs-lookup"><span data-stu-id="9e0f2-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="9e0f2-127">Izmenite podrazumevani ETC novom procenom stvarnog preostalog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="9e0f2-128">Izmenite podrazumevani procenat napretka novom procenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="9e0f2-129">Svaki od ovih pristupa dovodi do toga da se ponovo izračunaju ETC, EAC i procenat napretka zadatka, kao i odstupanje od projektovanog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="9e0f2-130">EAC, ETC i procenat napretka u rezimiranim zadacima takođe se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="9e0f2-131">Ponovna projekcija angažovanja za rezimirane zadatke</span><span class="sxs-lookup"><span data-stu-id="9e0f2-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="9e0f2-132">Angažovanje na rezimiranim zadacima ili zadacima kontejnera može se ponovno projektovati.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="9e0f2-133">Bez obzira da li korisnik ponovo projektuje pomoću preostalog angažovanja ili procenta napretka rezimiranih zadataka, započinje sledeći niz izračunavanja:</span><span class="sxs-lookup"><span data-stu-id="9e0f2-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="9e0f2-134">EAC, ETC i procenat napretka zadatka se izračunavaju.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="9e0f2-135">Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni EAC za zadatak.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="9e0f2-136">Izračunava se novi EAC za svaki od pojedinačnih zadataka sve do zadataka čvora lista.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="9e0f2-137">Nadređeni zadaci na koje ovo utiče, sve do čvorova lista, imaju ponovno izračunat ETC i procenat napretka na osnovu EAC vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="9e0f2-138">To rezultira novom projekcijom odstupanja od angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="9e0f2-139">Ponovo se izračunavaju EAC-ovi rezimiranih zadataka sve do osnovnog čvora.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="9e0f2-140">Prikaz praćenja troškova</span><span class="sxs-lookup"><span data-stu-id="9e0f2-140">Cost tracking view</span></span> 

<span data-ttu-id="9e0f2-141">Prikaz **Praćenje troškova** upoređuje stvarne troškove potrošene na zadatak i planirane troškove.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="9e0f2-142">Ovaj prikaz prikazuje samo troškove rada i ne uključuje troškove iz procena troškova.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="9e0f2-143">Project Service Automation koristi sledeće formule za izračunavanje metrika za praćenje:</span><span class="sxs-lookup"><span data-stu-id="9e0f2-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="9e0f2-144">Kada se kreira zadatak, planirani trošak jednak je procenjenim troškovima pri završetku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="9e0f2-145">Kada se stvarne vrednosti evidentiraju u zadatku, sledeće će biti izračunato na osnovu prikaza **Praćenje** za troškove:</span><span class="sxs-lookup"><span data-stu-id="9e0f2-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="9e0f2-146">Procenat ostvarenih troškova = Stvarni troškovi do danas ÷ Procenjeni troškovi po završetku za zadatak</span><span class="sxs-lookup"><span data-stu-id="9e0f2-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="9e0f2-147">Troškovi do završetka (CTC) = Procenjeni troškovi po završetku – Stvarni troškovi ostvareni do danas</span><span class="sxs-lookup"><span data-stu-id="9e0f2-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="9e0f2-148">Procenjeni troškovi po završetku = CTC + Stvarni troškovi ostvareni do danas</span><span class="sxs-lookup"><span data-stu-id="9e0f2-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="9e0f2-149">Predviđeno odstupanje od troškova = Planirani troškovi – Procenjeni troškovi po završetku</span><span class="sxs-lookup"><span data-stu-id="9e0f2-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="9e0f2-150">Projekcija odstupanja od troškova je prikazana na zadatku.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="9e0f2-151">Ako su procenjeni troškovi po završetku veći od planiranih troškova, predviđa se da će zadatak koštati više nego što je prvobitno planirano.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="9e0f2-152">Zbog toga ima trend prekoračenja budžeta.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="9e0f2-153">Ako su procenjeni troškovi po završetku manji od planiranih troškova, predviđa se da će zadatak koštati manje nego što je prvobitno planirano i da ima trend neiskorišćenog budžeta.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="9e0f2-154">Ponovna projekcija troškova od strane menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="9e0f2-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="9e0f2-155">Kada se angažovanje ponovo projektuje, CTC, Procenjeni troškovi po završetku, procenat ostvarenih troškova i odstupanja od projektovanih troškova ponovo se izračunavaju u prikazu **Praćenje troškova**.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="9e0f2-156">Rezime statusa projekta</span><span class="sxs-lookup"><span data-stu-id="9e0f2-156">Project status summary</span></span>

<span data-ttu-id="9e0f2-157">Podaci za praćenje u prikazima **Praćenje aktivnosti** i **Praćenje troškova** prikazuju napredak i troškove korišćenja na nivou osnovnog čvora projekta, rezimiranih zadataka i zadataka čvorova lista.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="9e0f2-158">Odeljak **Status** na stranici **Entitet projekta** prikazuje rezime statusa na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="9e0f2-159">Polja rezimea statusa</span><span class="sxs-lookup"><span data-stu-id="9e0f2-159">Status summary fields</span></span>

<span data-ttu-id="9e0f2-160">Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="9e0f2-161">Koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="9e0f2-162">Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="9e0f2-163">Polje **Status ažuriran dana** nije moguće uređivati i vrednost je vremenska oznaka koja pokazuje kada je status zadnji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="9e0f2-164">Polja **Performanse rasporeda** i **Performanse troškova** su podešena od datuma praćenja.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="9e0f2-165">Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete podesiti ova polja na **Pre plana**.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="9e0f2-166">Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, možete ih podesiti na **Zaostaje za planom**.</span><span class="sxs-lookup"><span data-stu-id="9e0f2-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
