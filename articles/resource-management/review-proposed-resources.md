---
title: Pregled predloženih resursa
description: Ova tema pruža informacije o tome kako da predložite resurse za projekte.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000768"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="b6c73-103">Pregled predloženih resursa</span><span class="sxs-lookup"><span data-stu-id="b6c73-103">Review proposed resources</span></span>

<span data-ttu-id="b6c73-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="b6c73-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b6c73-105">Menadžeri resursa mogu da predlože resurs menadžeru projekata korišćenjem zahteva za resurs.</span><span class="sxs-lookup"><span data-stu-id="b6c73-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="b6c73-106">Iz mreže zahteva ili samog zahteva izaberite **Pronađi resurse**.</span><span class="sxs-lookup"><span data-stu-id="b6c73-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="b6c73-107">Na stranici **Pomoćnik za zakazivanje** izaberite resurs, a zatim u oknu **Kreiranje rezervacije resursa**, u polju **Status rezervacije**, izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="b6c73-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="b6c73-108">Dolazi do sledećih izmena statusa:</span><span class="sxs-lookup"><span data-stu-id="b6c73-108">The following status updates occur:</span></span>

- <span data-ttu-id="b6c73-109">Na stranici **Pomoćnik za zakazivanje** indikatori statusa se ažuriraju kako bi ukazali da je rezervacija predložena, a da resurs nije fiksno rezervisan.</span><span class="sxs-lookup"><span data-stu-id="b6c73-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="b6c73-110">U zahtevu za resurs se status menja u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="b6c73-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="b6c73-111">Na kartici **Tim** u okviru projekta, vrednost generičkog člana tima **Status zahteva** se menja u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="b6c73-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="b6c73-112">Menadžer projekta može predlog prihvatiti ili odbaciti.</span><span class="sxs-lookup"><span data-stu-id="b6c73-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="b6c73-113">Kada menadžeri resursa obrađuju zahteve za resurse, mogu koristiti bilo koji od sledećih pristupa:</span><span class="sxs-lookup"><span data-stu-id="b6c73-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="b6c73-114">Mogu da predlažu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za ispunjavanje zahtevanih sati.</span><span class="sxs-lookup"><span data-stu-id="b6c73-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="b6c73-115">Predloženi sati se zatim dele na više resursa koji mogu da zadovolje zahtevane sate.</span><span class="sxs-lookup"><span data-stu-id="b6c73-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="b6c73-116">U ovom scenariju, sati se ne mogu preklapati.</span><span class="sxs-lookup"><span data-stu-id="b6c73-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="b6c73-117">Mogu da predlažu manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="b6c73-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="b6c73-118">U ovom scenariju, kapacitet predloženog resursa je manji od zahtevanih sati koje je naveo podnosilac zahteva.</span><span class="sxs-lookup"><span data-stu-id="b6c73-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="b6c73-119">Stoga, kada podnosilac zahteva prihvati predložene resurse, kreira se potreba za neispunjenim resursom da bi se evidentirala preostala potražnja.</span><span class="sxs-lookup"><span data-stu-id="b6c73-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="b6c73-120">Mogu da rezervišu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za obavljanje posla.</span><span class="sxs-lookup"><span data-stu-id="b6c73-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="b6c73-121">Mogu da rezervišu manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="b6c73-121">Book fewer resources than are required.</span></span> <span data-ttu-id="b6c73-122">U ovom scenariju, broj rezervisanih sati je manji od broja zahtevanih sati.</span><span class="sxs-lookup"><span data-stu-id="b6c73-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="b6c73-123">Sistem vas upućuje da predložite resurse umesto rezervacija, tako da podnosilac zahteva može da proveri i prati preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="b6c73-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="b6c73-124">Dostupnosti resursa</span><span class="sxs-lookup"><span data-stu-id="b6c73-124">Resource availability</span></span>

<span data-ttu-id="b6c73-125">Od presudnog je značaja da menadžeri resursa mogu da pregledaju dostupnost resursa i ažuriraju rezervacije.</span><span class="sxs-lookup"><span data-stu-id="b6c73-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="b6c73-126">U nekim slučajevima, ne postoji formalna potražnja (zahtev za resurs), ali menadžer resursa mora da odgovori na neplaniranu potražnju koja dolazi preko kanala poput e-pošte, telefonskog poziva ili trenutne poruke.</span><span class="sxs-lookup"><span data-stu-id="b6c73-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="b6c73-127">Menadžeri resursa koriste tablu rasporeda za ažuriranje resursa i rezervacija.</span><span class="sxs-lookup"><span data-stu-id="b6c73-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="b6c73-128">Radno vreme resursa koristi se kao osnova za izračunavanje dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="b6c73-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="b6c73-129">Rezervacije resursa troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="b6c73-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="b6c73-130">Tabela rasporeda koristi boje i senčenja da bi prikazala rezervacije, dostupnost i prebukiranost, kao i status rezervacija.</span><span class="sxs-lookup"><span data-stu-id="b6c73-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="b6c73-131">Postavka u podešavanjima tabele rasporeda omogućava vam da prikažete legendu.</span><span class="sxs-lookup"><span data-stu-id="b6c73-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="b6c73-132">Ako se strelica usmerena udesno pojavi pored pojedinačnog resursa koji se može rezervisati u tabeli rasporeda, resurs se može proširiti i pokazati detalje posla za koji je resurs rezervisan.</span><span class="sxs-lookup"><span data-stu-id="b6c73-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="b6c73-133">Pošto Dynamics 365 Project Operations koristi Universal Resource Scheduling mehanizam, ako ste instalirali i Dynamics 365 Field Service, možete pregledati detalje o rezervacijama resursa za projekte, radnim nalozima i bilo kojim drugim entitetima za koje ste proširili zakazivanje.</span><span class="sxs-lookup"><span data-stu-id="b6c73-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="b6c73-134">Da biste videli više detalja o pojedinačnom resursu, kliknite desnim tasterom miša na resurs da biste otvorili karticu resursa.</span><span class="sxs-lookup"><span data-stu-id="b6c73-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]