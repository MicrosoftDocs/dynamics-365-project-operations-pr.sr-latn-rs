---
title: Kreiranje rezervacije u projektu iz tabele rasporeda
description: Ova tema pruža informacije o tome kako da kreirate rezervaciju u projektu na tabeli rasporeda.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146545"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="2e5f5-103">Kreiranje rezervacije u projektu iz tabele rasporeda</span><span class="sxs-lookup"><span data-stu-id="2e5f5-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2e5f5-104">Možete da rezervišete resurs za projekat direktno na kartici **Tim** za projekat ili da generišete potrebu za resursom iz dodele generičkog člana tima, a da zatim ispunite generisanu potrebu članom projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="2e5f5-105">Možete i da rezervišete resurs za projekat direktno iz tabele rasporeda.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="2e5f5-106">To može da se uradi na tri načina:</span><span class="sxs-lookup"><span data-stu-id="2e5f5-106">There are three ways to do this:</span></span>

- <span data-ttu-id="2e5f5-107">**Rezervisanje iz generisane potrebe za resursom:** Potrebu za resurs možete da generišete nakon što kreirate generički resurs i dodelite zadatke unutar projekta.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="2e5f5-108">**Rezervisanje iz primarne potrebe:** Primarne potrebe se pojavljuju na tabeli rasporeda na kartici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="2e5f5-109">**Rezervisanje iz nove potrebe za resursom:** Možete da kreirate potrebu za resursom ispočetka i povežete je sa projektom.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="2e5f5-110">Na tabeli rasporeda, potreba za resursom se prikazuje na kartici **Otvorene potrebe**.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="2e5f5-111">Rezervisanje iz generisanog zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="2e5f5-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="2e5f5-112">Možete da kreirate generički resurs i da mu dodelite zadatak ili više zadataka u okviru projekta.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="2e5f5-113">Zatim možete da generišete potrebu za resursom za generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="2e5f5-114">Na tabeli rasporeda, ovaj resurs će se prikazati na kartici **Otvorene potrebe**. Možda ćete morati da koristite filtere kolona na mreži ukoliko imate mnogo otvorenih zahteva.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="2e5f5-115">![Otvaranje kartice Zahtevi na tabeli rasporeda](media/FAQ-Project-Booking-Schedule-Board-1.png "Snimak ekrana tabele rezervacija i dodela")</span><span class="sxs-lookup"><span data-stu-id="2e5f5-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="2e5f5-116">Izaberite zahtev.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-116">Select the requirement.</span></span> <span data-ttu-id="2e5f5-117">Kartica **Pretraga dostupnosti** će se pojaviti pri vrhu izabranog reda.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="2e5f5-118">Kada izaberete karticu, pokreće se režim Pomoćnik za zakazivanje u tabeli rasporeda, a zatim filtrira dostupne resurse koji ispunjavaju potrebe za resursima.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="2e5f5-119">Posle toga možete da rezervišete resurs.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="2e5f5-120">Možete i da prevučete i otpustite izabrani red sa dna tabele rasporeda u ćeliju resursa na mreži iznad.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="2e5f5-121">Kada ga spustite, on otvara tablu **Kreiranje rezervacije resursa** sa desne strane.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="2e5f5-122">Izbor opcije **Rezerviši** rezerviše resurs u projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-122">Selecting **Book** books the resource onto the project team.</span></span>

![Tabla Kreiranje rezervacije resursa](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="2e5f5-124">Rezervisanje iz primarnog zahteva</span><span class="sxs-lookup"><span data-stu-id="2e5f5-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="2e5f5-125">Kreiranje projekta u programu Project Service automatski kreira zahtev za resursom pod imenom Primarni zahtev.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="2e5f5-126">To je prazan zahtev koji se koristi za brzo rezervisanje resursa pomoću tabele rasporeda bez generisanja zahteva ili kreiranja zahteva iz početka.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="2e5f5-127">Pošto je zahtev prazan, moraćete da navedete datume, kao i način dodele i sate ako je to primenljivo.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="2e5f5-128">Da biste rezervisali resurs sa primarnim zahtevom, u tabeli rasporeda izaberite karticu **Projekat**. Možda ćete morati da koristite filter kolone za kolonu **Projekat** ukoliko imate više projekata.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="2e5f5-129">![Filteri kolone na tabli rasporeda](media/FAQ-Project-Booking-Schedule-Board-2.png "Snimak ekrana tabele rezervacija i dodela")</span><span class="sxs-lookup"><span data-stu-id="2e5f5-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="2e5f5-130">Izaberite zahtev koji ima samo ime projekta kao svoje ime i čije trajanje iznosi nula (0).</span><span class="sxs-lookup"><span data-stu-id="2e5f5-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="2e5f5-131">Izaberite karticu **Pretraga dostupnosti** koja se pojavljuje u redu.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="2e5f5-132">Na taj način tabela rasporeda ulazi u režim Pomoćnik za zakazivanje i prikazuje dostupne resurse koje je moguće rezervisati za projekat.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="2e5f5-133">Pošto je **Primarni zahtev** prazan zahtev čije trajanje iznosi nula (0), moraćete da podesite trajanje na tabli **Kreiranje rezervacije resursa** prilikom izbora i rezervisanja resursa.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="2e5f5-134">Možete i da izaberete **Primarni zahtev projekta** u dnu tabele rasporeda i da ga prevučete do resursa da biste ga rezervisali.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="2e5f5-135">Pošto je **Primarni zahtev** prazan zahtev čije trajanje iznosi nula (0), moraćete da podesite trajanje na tabli **Kreiranje rezervacije resursa** prilikom izbora i rezervisanja resursa.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="2e5f5-136">Kada rezervišete resurs putem **primarnog zahteva** u tabeli rasporeda, dodajete ga u projektni tim bez ijedne dodele.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="2e5f5-137">Rezervisanje iz novog zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="2e5f5-137">Book from a new resource requirement</span></span>
<span data-ttu-id="2e5f5-138">Obavite sledeće korake da biste obavili rezervaciju iz nove potrebe za resursom.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="2e5f5-139">Idite na **Potrebe za resursima**, a zatim izaberite **Novi** da biste kreirali novu potrebu za resursom.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="2e5f5-140">Na kartici **Projekat** odaberite projekat kako biste povezali zahtev i projekat.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="2e5f5-141">U tabeli rasporeda, ovaj novi zahtev se prikazuje kao **Otvoreni zahtev** koji možete da popunite.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="2e5f5-142">Rezervišite resurs da biste ga dodali u projektni tim.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="2e5f5-143">Sada kada je resurs rezervisan, morate da mu ručno dodelite zadatke.</span><span class="sxs-lookup"><span data-stu-id="2e5f5-143">Now that the resource is booked, you must assign tasks manually.</span></span>

