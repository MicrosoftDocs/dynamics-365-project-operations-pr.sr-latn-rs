---
title: Upravljanje vremenskim zonama
description: Kada se projekat kreira, njegova vremenska zona zasniva se na vremenskoj zoni definisanoj u predlošku radnog sata koji se primenjuje.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083518"
---
# <a name="manage-time-zones"></a><span data-ttu-id="33b8c-103">Upravljanje vremenskim zonama</span><span class="sxs-lookup"><span data-stu-id="33b8c-103">Manage time zones</span></span>

<span data-ttu-id="33b8c-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="33b8c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="33b8c-105">Projekti</span><span class="sxs-lookup"><span data-stu-id="33b8c-105">Projects</span></span>

<span data-ttu-id="33b8c-106">Kada se projekat kreira, njegova vremenska zona se zasniva na vremenskoj zoni definisanoj u predlošku radnog sata koji se primenjuje.</span><span class="sxs-lookup"><span data-stu-id="33b8c-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="33b8c-107">Na obrascu **Projekat** , datumi su uvek relativni u odnosu na vremensku zonu korisnika koji je prijavljen na svakoj kartici, osim kartice **Zadatak**. Kada pregledate strukturne analize posla, datumi će se uvek prikazivati u vremenskoj zoni projekta.</span><span class="sxs-lookup"><span data-stu-id="33b8c-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="33b8c-108">Zadaci</span><span class="sxs-lookup"><span data-stu-id="33b8c-108">Tasks</span></span>

<span data-ttu-id="33b8c-109">Kada se zadatak kreira, vreme početka, vreme završetka i broj sati na dan kontrolišu se radnim vremenom projekta.</span><span class="sxs-lookup"><span data-stu-id="33b8c-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="33b8c-110">Na primer, ako se zadatak kreira sa projektom čija je vremenska zona -8 PST i ima radno vreme od 9:00 do 17:00 od ponedeljka do petka, svaki zadatak kreiran bez dodele poštovaće vreme početka i vreme završetka kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="33b8c-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="33b8c-111">Upravljanje resursima pomoću vremenskih zona</span><span class="sxs-lookup"><span data-stu-id="33b8c-111">Manage resources with time zones</span></span>

<span data-ttu-id="33b8c-112">Za tačne i predvidljive rezultate prilikom upotrebe **produženja rezervacije** , postoje dva ključna preduslova koja moraju biti ispunjena:</span><span class="sxs-lookup"><span data-stu-id="33b8c-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="33b8c-113">Korisnik mora da konfiguriše vremensku zonu svog uređaja tako da odgovara vremenskoj zoni definisanoj u sistemskim **podešavanjima personalizacije**.</span><span class="sxs-lookup"><span data-stu-id="33b8c-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Podešavanja vremenske zone u operativnom sistemu Windows 10](media/reconcile-assignments-03.png)

  ![Podešavanja vremenske zone u podešavanjima personalizacije](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="33b8c-116">Resurs koji može da se rezerviše mora imati najmanje jedan minut radnog vremena koji se preklapa sa konturama koje se koriste za definisanje traženog dodatka.</span><span class="sxs-lookup"><span data-stu-id="33b8c-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="33b8c-117">Na primer, sledeći resursi sa radnim vremenom koje pada između 9:00 i 19:00.</span><span class="sxs-lookup"><span data-stu-id="33b8c-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Poređenje kontura resursa](media/reconcile-assignments-05.png)

<span data-ttu-id="33b8c-119">Sledeća tabela prikazuje:</span><span class="sxs-lookup"><span data-stu-id="33b8c-119">The following table shows:</span></span>

- <span data-ttu-id="33b8c-120">Predložak kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="33b8c-120">A project calendar template</span></span>
- <span data-ttu-id="33b8c-121">Resurs A: ovaj resurs ima isti kalendar i nalazi se u istoj vremenskoj zoni kao i projekat.</span><span class="sxs-lookup"><span data-stu-id="33b8c-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="33b8c-122">Početno vreme rezervacije će biti u 9:00.</span><span class="sxs-lookup"><span data-stu-id="33b8c-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="33b8c-123">Resurs B: Ovaj resurs se nalazi u drugoj vremenskoj zoni u odnosu na projekat i počinje u 7:00 u svojoj vremenskoj zoni.</span><span class="sxs-lookup"><span data-stu-id="33b8c-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="33b8c-124">Međutim, rezervacije će početi u 9:00, jer je to najranije vreme početka konture zadatka.</span><span class="sxs-lookup"><span data-stu-id="33b8c-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="33b8c-125">Resursi C i D: Resursi se nalaze u različitim vremenskim zonama, različitim međusobno i u odnosu na projekat, a njihove rezervacije započinju najranije od odgovarajućeg raspoloživog vremena početka.</span><span class="sxs-lookup"><span data-stu-id="33b8c-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="33b8c-126">Entitet</span><span class="sxs-lookup"><span data-stu-id="33b8c-126">Entity</span></span>  |<span data-ttu-id="33b8c-127">Kalendar</span><span class="sxs-lookup"><span data-stu-id="33b8c-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="33b8c-128">Predložak kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="33b8c-128">Project calendar template</span></span>   | ![kalendar projekta](media/reconcile-assignments-06.png) |
|<span data-ttu-id="33b8c-130">Resurs A</span><span class="sxs-lookup"><span data-stu-id="33b8c-130">Resource A</span></span>  | ![Kalendar resursa A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="33b8c-132">Resurs B</span><span class="sxs-lookup"><span data-stu-id="33b8c-132">Resource B</span></span>  |  ![Kalendar resursa B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="33b8c-134">Resurs C</span><span class="sxs-lookup"><span data-stu-id="33b8c-134">Resource C</span></span>  |  ![Kalendar resursa C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="33b8c-136">Resurs D</span><span class="sxs-lookup"><span data-stu-id="33b8c-136">Resource D</span></span>  | ![Kalendar resursa D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="33b8c-138">Kada odete na prikaz **Usaglašavanje** , prikazuju se dodele resursa i pridruženi nedostaci rezervacija.</span><span class="sxs-lookup"><span data-stu-id="33b8c-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Prikaz usklađivanja pre produžetka](media/reconcile-assignments-10.png)

<span data-ttu-id="33b8c-140">Kada se za svaki resurs koristi funkcija proširenog rezervisanja, rezervacije se uspešno produžavaju za svaki resurs, jer se radno vreme svakog resursa preklapa sa konturama nedostatka.</span><span class="sxs-lookup"><span data-stu-id="33b8c-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Prikaz usklađivanja nakon produženja rezervacije](media/reconcile-assignments-11.png) 

<span data-ttu-id="33b8c-142">Primetite da bolji uvid u detalje rezervacije pokazuje razlike u vremenu početka rezervacija.</span><span class="sxs-lookup"><span data-stu-id="33b8c-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="33b8c-143">Rezervacije počinju ne ranije od vremena početka konture dodele i ne ranije od raspoloživog vremena početka resursa.</span><span class="sxs-lookup"><span data-stu-id="33b8c-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nove rezervacije resursa na tabeli rasporeda](media/reconcile-assignments-12.png)
