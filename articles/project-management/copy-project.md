---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091271"
---
# <a name="copy-a-project"></a><span data-ttu-id="5382b-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-103">Copy a project</span></span>

<span data-ttu-id="5382b-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="5382b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5382b-105">Uz Dynamics 365 Project Operations, možete brzo da pravite nove projekte izborom opcije **Kopiraj projekat** u obrascu **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="5382b-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="5382b-106">Da biste kopirali projekat, otvorite projekat koji želite da kopirate, a zatim izaberite **Kopiraj projekat**.</span><span class="sxs-lookup"><span data-stu-id="5382b-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="5382b-107">Radnja će kopirati sledeće:</span><span class="sxs-lookup"><span data-stu-id="5382b-107">The action will copy the following:</span></span>

- <span data-ttu-id="5382b-108">Svojstva projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-108">Project properties</span></span> 
- <span data-ttu-id="5382b-109">Strukturna analiza posla</span><span class="sxs-lookup"><span data-stu-id="5382b-109">Work breakdown structure</span></span>
- <span data-ttu-id="5382b-110">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5382b-110">Project team members</span></span>
- <span data-ttu-id="5382b-111">Procene za projekat</span><span class="sxs-lookup"><span data-stu-id="5382b-111">Project estimates</span></span>
- <span data-ttu-id="5382b-112">Procene troškova projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-112">Project expense estimates</span></span>
- <span data-ttu-id="5382b-113">Procene materijala za projekat</span><span class="sxs-lookup"><span data-stu-id="5382b-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="5382b-114">Svojstva projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-114">Project properties</span></span>

<span data-ttu-id="5382b-115">Kada se projekat kopira, kopiraju se vrednosti u sledećim poljima:</span><span class="sxs-lookup"><span data-stu-id="5382b-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="5382b-116">+Ime</span><span class="sxs-lookup"><span data-stu-id="5382b-116">Name</span></span>
- <span data-ttu-id="5382b-117">Opis</span><span class="sxs-lookup"><span data-stu-id="5382b-117">Description</span></span>
- <span data-ttu-id="5382b-118">Klijent</span><span class="sxs-lookup"><span data-stu-id="5382b-118">Customer</span></span>
- <span data-ttu-id="5382b-119">Predložak kalendara</span><span class="sxs-lookup"><span data-stu-id="5382b-119">Calendar Template</span></span>
- <span data-ttu-id="5382b-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="5382b-120">Currency</span></span>
- <span data-ttu-id="5382b-121">Jedinica ugovaranja</span><span class="sxs-lookup"><span data-stu-id="5382b-121">Contracting Unit</span></span>
- <span data-ttu-id="5382b-122">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-122">Project Manager</span></span>
- <span data-ttu-id="5382b-123">Status</span><span class="sxs-lookup"><span data-stu-id="5382b-123">Status</span></span>
- <span data-ttu-id="5382b-124">Ukupan status projekta</span><span class="sxs-lookup"><span data-stu-id="5382b-124">Overall Project Status</span></span>
- <span data-ttu-id="5382b-125">Komentari</span><span class="sxs-lookup"><span data-stu-id="5382b-125">Comments</span></span>
- <span data-ttu-id="5382b-126">Procene</span><span class="sxs-lookup"><span data-stu-id="5382b-126">Estimates</span></span>
- <span data-ttu-id="5382b-127">Procenjeni datum početka: Ovo je datum kada se projekat kreira iz kopije.</span><span class="sxs-lookup"><span data-stu-id="5382b-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="5382b-128">Procenjeni datum završetka: Ovaj datum se prilagođava na osnovu datuma početka novog projekta koji je napravljen iz kopije.</span><span class="sxs-lookup"><span data-stu-id="5382b-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="5382b-129">Angažovanje (časovi)</span><span class="sxs-lookup"><span data-stu-id="5382b-129">Effort (Hours)</span></span>
- <span data-ttu-id="5382b-130">Procenjeni troškovi rada</span><span class="sxs-lookup"><span data-stu-id="5382b-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="5382b-131">Procenjeni iznos troškova</span><span class="sxs-lookup"><span data-stu-id="5382b-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="5382b-132">Iznos procenjenih troškova materijala</span><span class="sxs-lookup"><span data-stu-id="5382b-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="5382b-133">Kopiranje projekta je dugotrajna operacija.</span><span class="sxs-lookup"><span data-stu-id="5382b-133">Copy project is a long running operation.</span></span> <span data-ttu-id="5382b-134">Kopiraju se i zapisi projekta, njihovi relevantni atributi i mnogi povezani entiteti.</span><span class="sxs-lookup"><span data-stu-id="5382b-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="5382b-135">Zbog dugotrajne prirode operacije, nakon započinjanja kopiranja, ciljna stranica projekta se zaključava za uređivanje dok se operacija kopiranja ne dovrši.</span><span class="sxs-lookup"><span data-stu-id="5382b-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="5382b-136">Strukturna analiza posla</span><span class="sxs-lookup"><span data-stu-id="5382b-136">Work breakdown structure</span></span>

<span data-ttu-id="5382b-137">Kada se projekat kopira, kopira se celokupna strukturna analiza posla učitanog resursa.</span><span class="sxs-lookup"><span data-stu-id="5382b-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="5382b-138">Imenovani resurs zamenjuje generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="5382b-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="5382b-139">Ako imenovani resursi nemaju isto radno vreme kao generički resurs, raspored će se ponovo izračunati i trajanje zadatka se može promeniti.</span><span class="sxs-lookup"><span data-stu-id="5382b-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="5382b-140">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="5382b-140">Project team members</span></span>

<span data-ttu-id="5382b-141">Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi.</span><span class="sxs-lookup"><span data-stu-id="5382b-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="5382b-142">Dodele generičkih resursa takođe se održavaju kao u izvornom projektu.</span><span class="sxs-lookup"><span data-stu-id="5382b-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="5382b-143">Imenovani resursi će se pretvoriti u generičke članove tima.</span><span class="sxs-lookup"><span data-stu-id="5382b-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="5382b-144">Procene</span><span class="sxs-lookup"><span data-stu-id="5382b-144">Estimates</span></span>

<span data-ttu-id="5382b-145">Kada se projekat kopira, stavke resursa, troškova i procene materijala kopiraju se iz izvornog projekta.</span><span class="sxs-lookup"><span data-stu-id="5382b-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="5382b-146">Za informacije o tome kako programski pristupiti opciji Kopiraj projekat, pogledajte [Razvijajte predloške projekata pomoću opcije Kopiraj projekat](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="5382b-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
