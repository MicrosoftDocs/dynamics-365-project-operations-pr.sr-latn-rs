---
title: Rezervisanje za projekat
description: Ova tema pruža informacije o rezervisanju resursa u projekat.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908547"
---
# <a name="book-to-a-project"></a><span data-ttu-id="29083-103">Rezervisanje za projekat</span><span class="sxs-lookup"><span data-stu-id="29083-103">Book to a project</span></span>

<span data-ttu-id="29083-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="29083-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="29083-105">Postoje slučajevi u kojima će menadžer projekta ili menadžer resursa morati da dodeli resurs projektu, a da od generičkog člana tima nije definisan poseban zahtev.</span><span class="sxs-lookup"><span data-stu-id="29083-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="29083-106">To se može postići na jedan od tri načina.</span><span class="sxs-lookup"><span data-stu-id="29083-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="29083-107">Rezervacija iz mreže člana tima</span><span class="sxs-lookup"><span data-stu-id="29083-107">Book from the team member grid</span></span>
- <span data-ttu-id="29083-108">Rezervisanje sa tabele rasporeda</span><span class="sxs-lookup"><span data-stu-id="29083-108">Book from the schedule board</span></span>
- <span data-ttu-id="29083-109">Rezervacija iz obrasca **Projekat**</span><span class="sxs-lookup"><span data-stu-id="29083-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="29083-110">Rezervacija iz mreže člana tima</span><span class="sxs-lookup"><span data-stu-id="29083-110">Book from the team member grid</span></span>

<span data-ttu-id="29083-111">Ako vaša organizacija radi u hibridnom režimu dodele resursa, menadžer projekta može rezervisati resurs direktno u projekat tako što će izvršiti sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="29083-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="29083-112">Iz projekta idite na mrežu članova tima i izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="29083-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="29083-113">Definišite naziv pozicije i ulogu resursa.</span><span class="sxs-lookup"><span data-stu-id="29083-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="29083-114">Izaberite resurs koji može da se rezerviše iz dostupnog pronalaženja.</span><span class="sxs-lookup"><span data-stu-id="29083-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="29083-115">Kada odaberete resurs, definišite sledeće informacije o polju da biste rezervisali resurs:</span><span class="sxs-lookup"><span data-stu-id="29083-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="29083-116">Datum početka</span><span class="sxs-lookup"><span data-stu-id="29083-116">Start date</span></span>
    - <span data-ttu-id="29083-117">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="29083-117">Finish date</span></span>
    - <span data-ttu-id="29083-118">Način dodele</span><span class="sxs-lookup"><span data-stu-id="29083-118">Allocation method</span></span>
    - <span data-ttu-id="29083-119">Sati, ako je primenljivo</span><span class="sxs-lookup"><span data-stu-id="29083-119">Hours, if applicable</span></span>
    - <span data-ttu-id="29083-120">Davalac odobrenja za projekat</span><span class="sxs-lookup"><span data-stu-id="29083-120">Project approver</span></span>

6. <span data-ttu-id="29083-121">Izaberite stavku **Sačuvaj i zatvori**</span><span class="sxs-lookup"><span data-stu-id="29083-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="29083-122">Rezervisanje sa tabele rasporeda</span><span class="sxs-lookup"><span data-stu-id="29083-122">Book from the schedule board</span></span>

<span data-ttu-id="29083-123">Kada menadžer resursa treba da rezerviše resurs direktno za projekat, može da koristi tablu rasporeda i zahteve projekta.</span><span class="sxs-lookup"><span data-stu-id="29083-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="29083-124">Zahtev projekta je zahtev za resursom koji je uvek dostupan za rezervisanje.</span><span class="sxs-lookup"><span data-stu-id="29083-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="29083-125">Da biste rezervisali direktno u obrazac projekta iz tabele rasporeda, obavite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="29083-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="29083-126">Idite na tabelu rasporeda i na levoj stranici filtrirajte resurse koje uzimate u obzir za zahtev.</span><span class="sxs-lookup"><span data-stu-id="29083-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="29083-127">U donjem oknu izaberite karticu **Projekat** da biste videli listu projektnih zahteva.</span><span class="sxs-lookup"><span data-stu-id="29083-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="29083-128">Prevucite zahtev na resurs i definišite sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="29083-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="29083-129">Datum početka</span><span class="sxs-lookup"><span data-stu-id="29083-129">Start date</span></span>
    - <span data-ttu-id="29083-130">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="29083-130">Finish date</span></span>
    - <span data-ttu-id="29083-131">Status rezervacije</span><span class="sxs-lookup"><span data-stu-id="29083-131">Booking status</span></span>
    - <span data-ttu-id="29083-132">Metod rezervacije</span><span class="sxs-lookup"><span data-stu-id="29083-132">Booking method</span></span>
    - <span data-ttu-id="29083-133">Trajanje</span><span class="sxs-lookup"><span data-stu-id="29083-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="29083-134">Rezervacija iz obrasca Projekat</span><span class="sxs-lookup"><span data-stu-id="29083-134">Book from the Project form</span></span>

<span data-ttu-id="29083-135">Kao menadžer projekta, možda ćete morati da rezervišete resurs za projekat, ali znate samo kriterijume, a ne i naziv resursa.</span><span class="sxs-lookup"><span data-stu-id="29083-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="29083-136">Dovršite sledeće korake da biste pomoću pomoćnika za planiranje pronašli resurs na osnovu bilo kojih dostupnih atributa resursa.</span><span class="sxs-lookup"><span data-stu-id="29083-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="29083-137">Dođite do projekta i izaberite **Rezerviši** da biste otvorili pomoćnika za planiranje.</span><span class="sxs-lookup"><span data-stu-id="29083-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="29083-138">Pomoću filtera na levoj strani pomoćnika za planiranje, suzite kriterijume i izaberite **Pretraga.**</span><span class="sxs-lookup"><span data-stu-id="29083-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="29083-139">Na osnovu resursa vraćenih u rezultatima, možete rezervisati resurs.</span><span class="sxs-lookup"><span data-stu-id="29083-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="29083-140">Ova metoda ne kreira nikakve rezervacije za resurs.</span><span class="sxs-lookup"><span data-stu-id="29083-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="29083-141">Umesto toga, dodaje resurs timu.</span><span class="sxs-lookup"><span data-stu-id="29083-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="29083-142">Kada se član tima doda u projekat, menadžer projekta može koristiti održavanje rezervacija ili produžiti rezervacije da bi potrebne rezervacije dodao resursu.</span><span class="sxs-lookup"><span data-stu-id="29083-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
