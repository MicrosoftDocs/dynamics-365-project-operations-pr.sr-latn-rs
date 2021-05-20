---
title: Režimi planiranja
description: Ova tema pruža informacije o režimima planiranja.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981452"
---
# <a name="scheduling-modes"></a><span data-ttu-id="1a73d-103">Režimi planiranja</span><span class="sxs-lookup"><span data-stu-id="1a73d-103">Scheduling modes</span></span>

<span data-ttu-id="1a73d-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="1a73d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1a73d-105">Dynamics 365 Project Operations pruža mogućnost organizacijama da definišu kako upravljaju promenama ključnih promenljivih u zadacima unutar strukture raspodele rada.</span><span class="sxs-lookup"><span data-stu-id="1a73d-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="1a73d-106">Na osnovu specifičnih potreba organizacije, projekt menadžeri mogu da izvrše promene u načinu raspoređivanja kada se projekat kreira.</span><span class="sxs-lookup"><span data-stu-id="1a73d-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="1a73d-107">U Project Operations dostupna su tri načina raspoređivanja:</span><span class="sxs-lookup"><span data-stu-id="1a73d-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="1a73d-108">Fiksno trajanje (ovo je podrazumevani režim)</span><span class="sxs-lookup"><span data-stu-id="1a73d-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="1a73d-109">Fiksni rad</span><span class="sxs-lookup"><span data-stu-id="1a73d-109">Fixed work</span></span>
  - <span data-ttu-id="1a73d-110">Fiksne jedinice</span><span class="sxs-lookup"><span data-stu-id="1a73d-110">Fixed units</span></span>

<span data-ttu-id="1a73d-111">Vrednosti na koje utiče definicija određenog režima rasporeda određuju se sledećom formulom:</span><span class="sxs-lookup"><span data-stu-id="1a73d-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="1a73d-112">Napor (*Posao*) = Trajanje x Jedinice</span><span class="sxs-lookup"><span data-stu-id="1a73d-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="1a73d-113">Kada definišete režim zakazivanja projekta, postavljate jednu od ovih vrednosti, koje se potom ne mogu promeniti.</span><span class="sxs-lookup"><span data-stu-id="1a73d-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="1a73d-114">Držanje ove vrednosti kao konstante stavlja prioritet na tu vrednost, što obaveštava sistem da je ne menja kada se promene druge dve vrednosti.</span><span class="sxs-lookup"><span data-stu-id="1a73d-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="1a73d-115">Sledeća tabela pruža informacije o uticajima izbora određenog režima.</span><span class="sxs-lookup"><span data-stu-id="1a73d-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="1a73d-116">**U ovom zadatku**</span><span class="sxs-lookup"><span data-stu-id="1a73d-116">**In this task**</span></span>             | <span data-ttu-id="1a73d-117">**Ako revidirate jedinice**</span><span class="sxs-lookup"><span data-stu-id="1a73d-117">**If you revise units**</span></span>   | <span data-ttu-id="1a73d-118">**Ako revidirate trajanje**</span><span class="sxs-lookup"><span data-stu-id="1a73d-118">**If you revise duration**</span></span> | <span data-ttu-id="1a73d-119">**Ako revidirate napor**</span><span class="sxs-lookup"><span data-stu-id="1a73d-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="1a73d-120">Zadatak sa fiksnim jedinicama</span><span class="sxs-lookup"><span data-stu-id="1a73d-120">Fixed units task</span></span>     | <span data-ttu-id="1a73d-121">Trajanje je preračunato.</span><span class="sxs-lookup"><span data-stu-id="1a73d-121">Duration is recalculated.</span></span> | <span data-ttu-id="1a73d-122">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="1a73d-122">Effort is recalculated.</span></span>    | <span data-ttu-id="1a73d-123">Trajanje je preračunato.</span><span class="sxs-lookup"><span data-stu-id="1a73d-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="1a73d-124">Zadatak fiksnog angažovanja</span><span class="sxs-lookup"><span data-stu-id="1a73d-124">Fixed effort task</span></span>    | <span data-ttu-id="1a73d-125">Trajanje je preračunato.</span><span class="sxs-lookup"><span data-stu-id="1a73d-125">Duration is recalculated.</span></span> | <span data-ttu-id="1a73d-126">Jedinice se preračunavaju.</span><span class="sxs-lookup"><span data-stu-id="1a73d-126">Units are recalculated.</span></span>    | <span data-ttu-id="1a73d-127">Trajanje je preračunato.</span><span class="sxs-lookup"><span data-stu-id="1a73d-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="1a73d-128">Zadatak fiksnog trajanja</span><span class="sxs-lookup"><span data-stu-id="1a73d-128">Fixed duration task</span></span>  | <span data-ttu-id="1a73d-129">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="1a73d-129">Effort is recalculated.</span></span>   | <span data-ttu-id="1a73d-130">Napor se preračunava.</span><span class="sxs-lookup"><span data-stu-id="1a73d-130">Effort is recalculated.</span></span>    | <span data-ttu-id="1a73d-131">Jedinice se preračunavaju.</span><span class="sxs-lookup"><span data-stu-id="1a73d-131">Units are recalculated.</span></span>   |

<span data-ttu-id="1a73d-132">Za više informacija o implikacijama datog režima pogledajte [Promenite tip zadatka za tačnije raspoređivanje](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="1a73d-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="1a73d-133">U temi se pojam **Posao** koristi umesto **Napor**.</span><span class="sxs-lookup"><span data-stu-id="1a73d-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="1a73d-134">Promenite režim zakazivanja organizacije</span><span class="sxs-lookup"><span data-stu-id="1a73d-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="1a73d-135">Dovršite sledeće korake da biste definisali režim zakazivanja organizacije.</span><span class="sxs-lookup"><span data-stu-id="1a73d-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="1a73d-136">Idite na **Podešavanja** \> **Opšta** \> **Parametri**, a zatim izaberite parametar projekta.</span><span class="sxs-lookup"><span data-stu-id="1a73d-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="1a73d-137">Na stranici **Parametri projekta** izaberite podrazumevani režim zakazivanja za organizaciju, a zatim definišite sposobnost da menadžer projekta zameni postavku prilikom kreiranja novog projekta.</span><span class="sxs-lookup"><span data-stu-id="1a73d-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="1a73d-138">Promenite postavku režima zakazivanja na projektu</span><span class="sxs-lookup"><span data-stu-id="1a73d-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="1a73d-139">Ako organizacija dozvoli menadžeru projekta da zameni zadati režim raspoređivanja, menadžer projekta može to promeniti kada kreira novi projekat.</span><span class="sxs-lookup"><span data-stu-id="1a73d-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="1a73d-140">Međutim, nakon što je projekat sačuvan, režim zakazivanja ne može se promeniti.</span><span class="sxs-lookup"><span data-stu-id="1a73d-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="1a73d-141">Kopirani projekti</span><span class="sxs-lookup"><span data-stu-id="1a73d-141">Copied projects</span></span>

<span data-ttu-id="1a73d-142">Budući da se projekat kreira kada se preduzme akcija kopiranja, menadžer projekta ne može da postavi režim zakazivanja.</span><span class="sxs-lookup"><span data-stu-id="1a73d-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="1a73d-143">Odredišni projekat će se uvek podrazumevati za režim definisan na organizacionom nivou.</span><span class="sxs-lookup"><span data-stu-id="1a73d-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="1a73d-144">Kopirani zadaci</span><span class="sxs-lookup"><span data-stu-id="1a73d-144">Copied tasks</span></span>

<span data-ttu-id="1a73d-145">Kada se zadatak kopira iz jednog projekta u drugi, zadatak nasleđuje režim rasporeda odredišnog projekta.</span><span class="sxs-lookup"><span data-stu-id="1a73d-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
