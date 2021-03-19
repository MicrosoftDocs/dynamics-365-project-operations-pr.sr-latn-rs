---
title: Kopiranje projekta
description: Ova tema pruža informacije o kopiranju projekata u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479536"
---
# <a name="copy-a-project"></a><span data-ttu-id="af183-103">Kopiranje projekta</span><span class="sxs-lookup"><span data-stu-id="af183-103">Copy a project</span></span>

<span data-ttu-id="af183-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="af183-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="af183-105">Uz Dynamics 365 Project Operations, možete brzo da pravite nove projekte izborom opcije **Kopiraj projekat** u obrascu **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="af183-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="af183-106">Da biste kopirali projekat, otvorite projekat koji želite da kopirate, a zatim izaberite **Kopiraj projekat**.</span><span class="sxs-lookup"><span data-stu-id="af183-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="af183-107">Radnja će kopirati:</span><span class="sxs-lookup"><span data-stu-id="af183-107">The action will copy:</span></span>

- <span data-ttu-id="af183-108">Svojstva projekta (procenjeni datum početka se kopira iz izvornog projekta)</span><span class="sxs-lookup"><span data-stu-id="af183-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="af183-109">Strukturnu analizu posla</span><span class="sxs-lookup"><span data-stu-id="af183-109">The Work breakdown structure</span></span>
- <span data-ttu-id="af183-110">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="af183-110">Project team members</span></span>
- <span data-ttu-id="af183-111">Procene za projekat</span><span class="sxs-lookup"><span data-stu-id="af183-111">Project estimates</span></span>
- <span data-ttu-id="af183-112">Procene troškova projekta</span><span class="sxs-lookup"><span data-stu-id="af183-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="af183-113">Svojstva projekta</span><span class="sxs-lookup"><span data-stu-id="af183-113">Project properties</span></span>

<span data-ttu-id="af183-114">Kada se projekat kopira, kopiraju se vrednosti u sledećim poljima:</span><span class="sxs-lookup"><span data-stu-id="af183-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="af183-115">+Ime</span><span class="sxs-lookup"><span data-stu-id="af183-115">Name</span></span>
- <span data-ttu-id="af183-116">Opis</span><span class="sxs-lookup"><span data-stu-id="af183-116">Description</span></span>
- <span data-ttu-id="af183-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="af183-117">Customer</span></span>
- <span data-ttu-id="af183-118">Predložak kalendara</span><span class="sxs-lookup"><span data-stu-id="af183-118">Calendar Template</span></span>
- <span data-ttu-id="af183-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="af183-119">Currency</span></span>
- <span data-ttu-id="af183-120">Jedinica ugovaranja</span><span class="sxs-lookup"><span data-stu-id="af183-120">Contracting Unit</span></span>
- <span data-ttu-id="af183-121">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="af183-121">Project Manager</span></span>
- <span data-ttu-id="af183-122">Status</span><span class="sxs-lookup"><span data-stu-id="af183-122">Status</span></span>
- <span data-ttu-id="af183-123">Ukupan status projekta</span><span class="sxs-lookup"><span data-stu-id="af183-123">Overall Project Status</span></span>
- <span data-ttu-id="af183-124">Komentari</span><span class="sxs-lookup"><span data-stu-id="af183-124">Comments</span></span>
- <span data-ttu-id="af183-125">Procene</span><span class="sxs-lookup"><span data-stu-id="af183-125">Estimates</span></span>
- <span data-ttu-id="af183-126">Procenjeni datum početka</span><span class="sxs-lookup"><span data-stu-id="af183-126">Estimated Start Date</span></span>
- <span data-ttu-id="af183-127">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="af183-127">Finish Date</span></span>
- <span data-ttu-id="af183-128">Angažovanje (časovi)</span><span class="sxs-lookup"><span data-stu-id="af183-128">Effort (Hours)</span></span>
- <span data-ttu-id="af183-129">Procenjeni troškovi rada</span><span class="sxs-lookup"><span data-stu-id="af183-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="af183-130">Procenjeni iznos troškova</span><span class="sxs-lookup"><span data-stu-id="af183-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="af183-131">Strukturna analiza posla</span><span class="sxs-lookup"><span data-stu-id="af183-131">Work breakdown structure</span></span>

<span data-ttu-id="af183-132">Kada se projekat kopira, kopira se celokupna strukturna analiza posla učitanog resursa.</span><span class="sxs-lookup"><span data-stu-id="af183-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="af183-133">Imenovani resurs zamenjuje generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="af183-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="af183-134">Ako imenovani resursi nemaju isto radno vreme kao generički resurs, raspored će se ponovo izračunati i trajanje zadatka se može promeniti.</span><span class="sxs-lookup"><span data-stu-id="af183-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="af183-135">Članovi projektnog tima</span><span class="sxs-lookup"><span data-stu-id="af183-135">Project team members</span></span>

<span data-ttu-id="af183-136">Kada se projektni tim kopira iz izvornog projekta, kopiraju se generički resursi.</span><span class="sxs-lookup"><span data-stu-id="af183-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="af183-137">Dodele generičkih resursa takođe se održavaju kao u izvornom projektu.</span><span class="sxs-lookup"><span data-stu-id="af183-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="af183-138">Imenovani resursi će se pretvoriti u generičke članove tima.</span><span class="sxs-lookup"><span data-stu-id="af183-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="af183-139">Procene</span><span class="sxs-lookup"><span data-stu-id="af183-139">Estimates</span></span>

<span data-ttu-id="af183-140">Kada se projekat kopira, iz izvornog projekta se kopiraju i stavke procene resursa i troškova.</span><span class="sxs-lookup"><span data-stu-id="af183-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="af183-141">Za informacije o tome kako programski pristupiti opciji Kopiraj projekat, pogledajte [Razvijajte predloške projekata pomoću opcije Kopiraj projekat](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="af183-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
