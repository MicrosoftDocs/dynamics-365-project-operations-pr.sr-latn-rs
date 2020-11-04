---
title: Pregled pomoćnika za zakazivanje
description: Ova tema pruža informacije o radu sa pomoćnikom za planiranje radi rezervisanja resursa.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083436"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="78c1e-103">Pregled pomoćnika za zakazivanje</span><span class="sxs-lookup"><span data-stu-id="78c1e-103">Schedule assistant overview</span></span>

<span data-ttu-id="78c1e-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="78c1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78c1e-105">Pomoćnik za planiranje se koristi za rezervisanje resursa na osnovu zahteva koje je definisao menadžer projekta.</span><span class="sxs-lookup"><span data-stu-id="78c1e-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="78c1e-106">Pomoćnik za planiranje se oslanja na parametre navedene u zahtevu za resursom da bi pronašao resurs.</span><span class="sxs-lookup"><span data-stu-id="78c1e-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="78c1e-107">Pomoćnik za planiranje preporučuje resurse koji odgovaraju relevantnim zahtevima, poput dostupnih vremena ili potrebnih veština.</span><span class="sxs-lookup"><span data-stu-id="78c1e-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="78c1e-108">Kada se identifikuju odgovarajući resursi, menadžer resursa ili projekta može rezervisati resurs za rad.</span><span class="sxs-lookup"><span data-stu-id="78c1e-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78c1e-109">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="78c1e-109">Prerequisites</span></span>

<span data-ttu-id="78c1e-110">Pomoćnik za planiranje je deo rešenja Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="78c1e-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="78c1e-111">Ovo rešenje je uključeno i instalirano sa uslugama Dynamics 365 Project Operations, Dynamics 365 Field Service i Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="78c1e-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="78c1e-112">Zahtevi i resursi koji se podudaraju</span><span class="sxs-lookup"><span data-stu-id="78c1e-112">Matching requirements and resources</span></span>

<span data-ttu-id="78c1e-113">Zahtev za generisanim resursom zasniva se na detaljima kao što su:</span><span class="sxs-lookup"><span data-stu-id="78c1e-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="78c1e-114">Karakteristike</span><span class="sxs-lookup"><span data-stu-id="78c1e-114">Characteristics</span></span>
-   <span data-ttu-id="78c1e-115">Uloge</span><span class="sxs-lookup"><span data-stu-id="78c1e-115">Roles</span></span>
-   <span data-ttu-id="78c1e-116">Poslovne jedinice</span><span class="sxs-lookup"><span data-stu-id="78c1e-116">Business units</span></span>
-   <span data-ttu-id="78c1e-117">Željene postavke resursa</span><span class="sxs-lookup"><span data-stu-id="78c1e-117">Resource preferences</span></span>
-   <span data-ttu-id="78c1e-118">Konture angažovanja</span><span class="sxs-lookup"><span data-stu-id="78c1e-118">Effort contours</span></span>
-   <span data-ttu-id="78c1e-119">Vremenska zona</span><span class="sxs-lookup"><span data-stu-id="78c1e-119">Time zone</span></span>

<span data-ttu-id="78c1e-120">Pomoćnik za planiranje koristi ove detalje za filtriranje resursa.</span><span class="sxs-lookup"><span data-stu-id="78c1e-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="78c1e-121">Pokretanje pomoćnika za planiranje</span><span class="sxs-lookup"><span data-stu-id="78c1e-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="78c1e-122">Postoje dva načina na koje se pokreće pomoćnik za planiranje.</span><span class="sxs-lookup"><span data-stu-id="78c1e-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="78c1e-123">Ako koristite hibridni režim, u mreži člana tima možete da izaberete bilo kog člana tima sa neispunjenim zahtevima za resursima, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="78c1e-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="78c1e-124">Ako koristite centralni režim, menadžer resursa pronalazi i bira resurs.</span><span class="sxs-lookup"><span data-stu-id="78c1e-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="78c1e-125">Filter pomoćnika za planiranje</span><span class="sxs-lookup"><span data-stu-id="78c1e-125">Schedule assistant filters</span></span>

<span data-ttu-id="78c1e-126">Nakon pokretanja pomoćnika za planiranje, detalji iz zahteva za resursom prikazuju se kao filtrirane vrednosti u levom oknu.</span><span class="sxs-lookup"><span data-stu-id="78c1e-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="78c1e-127">Menadžer resursa ili menadžer projekata mogu precizno podesiti rezultate prilagođavanjem filtera kako bi udovoljili potrebama rasporeda.</span><span class="sxs-lookup"><span data-stu-id="78c1e-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="78c1e-128">Okno filtera prikazuje opcije vezane za posao, uključujući:</span><span class="sxs-lookup"><span data-stu-id="78c1e-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="78c1e-129">Početak i završetak posla</span><span class="sxs-lookup"><span data-stu-id="78c1e-129">Work start and end</span></span>
-   <span data-ttu-id="78c1e-130">Karakteristike</span><span class="sxs-lookup"><span data-stu-id="78c1e-130">Characteristics</span></span>
-   <span data-ttu-id="78c1e-131">Uloge</span><span class="sxs-lookup"><span data-stu-id="78c1e-131">Roles</span></span>
-   <span data-ttu-id="78c1e-132">Organizacione jedinice</span><span class="sxs-lookup"><span data-stu-id="78c1e-132">Organizational units</span></span>
-   <span data-ttu-id="78c1e-133">Preduzeće koje obezbeđuje resurse</span><span class="sxs-lookup"><span data-stu-id="78c1e-133">Resourcing company</span></span>
-   <span data-ttu-id="78c1e-134">Tipovi resursa</span><span class="sxs-lookup"><span data-stu-id="78c1e-134">Resource types</span></span>
-   <span data-ttu-id="78c1e-135">Željeni resursi</span><span class="sxs-lookup"><span data-stu-id="78c1e-135">Preferred resources</span></span>
