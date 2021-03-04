---
title: Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka
description: Ova tema pruža informacije o tome kako da rezervišete imenovane resurse za projektne timove i dodeljujete ih zadacima.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145375"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="d4866-103">Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka</span><span class="sxs-lookup"><span data-stu-id="d4866-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d4866-104">Možete da dodate imenovani resurs u projektni tim tako što ćete ga direktno rezervisati za tim.</span><span class="sxs-lookup"><span data-stu-id="d4866-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="d4866-105">Da biste to uradili, obavite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="d4866-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="d4866-106">U aplikaciji Project Service Automation idite na **Projekat** i otvorite projekat za koji rezervišete resurse.</span><span class="sxs-lookup"><span data-stu-id="d4866-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="d4866-107">Na stranici **Projekat**, na kartici **Tim** kliknite na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d4866-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Dodavanje člana tima na kartici Tim](media/RM-how-to-1.png)

3. <span data-ttu-id="d4866-109">U dijalogu **Brzo kreiranje člana projektnog tima** izaberite resurs koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="d4866-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="d4866-110">Polje **Uloga** će se popuniti podrazumevanom ulogom resursa ako je ona dodeljena.</span><span class="sxs-lookup"><span data-stu-id="d4866-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="d4866-111">Možete da promenite ulogu ako je potrebno.</span><span class="sxs-lookup"><span data-stu-id="d4866-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="d4866-112">Izaberite datum početka i završetka, odnosno period u kome vam resurs treba i izaberite način dodele kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="d4866-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="d4866-113">Ako želite da član tima bude osoba koja odobrava projekat, izaberite opciju **Da** u polju **Osoba koja odobrava projekat**.</span><span class="sxs-lookup"><span data-stu-id="d4866-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="d4866-114">Ovo će značiti da član tima može da odobri prosleđene stavke za vreme i troškove za ovaj projekat.</span><span class="sxs-lookup"><span data-stu-id="d4866-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="d4866-115">Kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d4866-115">Click **Save**.</span></span>

![Dodavanje člana tima u obrazac za brzo kreiranje](media/RM-how-to-2.png)


<span data-ttu-id="d4866-117">Sada možete dodeliti rezervisani resurs zadacima u projektu.</span><span class="sxs-lookup"><span data-stu-id="d4866-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="d4866-118">Na stranici **Projekat** kliknite na karticu **Raspored** da biste dodelili zadatke novom resursu.</span><span class="sxs-lookup"><span data-stu-id="d4866-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="d4866-119">Birač resursa koji je pokrenut iz polja **Resursi** u mreži zadataka će prikazati članove tima koje možete izabrati.</span><span class="sxs-lookup"><span data-stu-id="d4866-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Dodeljivanje člana tima zadatku na kartici Raspored](media/RM-how-to-3.png)

<span data-ttu-id="d4866-121">U verziji 3 aplikacije Project Service Automation (PSA), rezervisanje resursa i dodeljivanje zadataka nisu tesno povezani.</span><span class="sxs-lookup"><span data-stu-id="d4866-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="d4866-122">To znači da kada koristite birač resursa u rasporedu, možete da dodelite zadatke članovima tima za više sati nego što pokriva njihovo vreme rezervisanja za projekat.</span><span class="sxs-lookup"><span data-stu-id="d4866-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="d4866-123">Možete da vidite razlike između rezervacija članova tima i dodeljenih zadataka na kartici **Tim** ili na kartici **Usaglašavanje resursa**. Takođe možete da usaglasite razlike između rezervacija i dodela resursa na detaljnijem nivou.</span><span class="sxs-lookup"><span data-stu-id="d4866-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Kartica Usaglašavanje resursa](media/RM-how-to-4.png)

<span data-ttu-id="d4866-125">Takođe možete koristiti birač resursa na kartici **Raspored** da biste potražili i izabrali resurse koji mogu da se rezervišu, a koji još nisu deo projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="d4866-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="d4866-126">Oni se prikazuju u biraču resursa kao **Ostali resursi**.</span><span class="sxs-lookup"><span data-stu-id="d4866-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Dodeljivanje resursa koji nije član tima zadatku](media/RM-how-to-5.png)

<span data-ttu-id="d4866-128">Kada to uradite, resurs će biti dodat u tim projekta i dodeljen zadatku, ali se ne generišu rezervacije.</span><span class="sxs-lookup"><span data-stu-id="d4866-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Član tima sa dodelama i bez rezervacija](media/RM-how-to-6.png)

<span data-ttu-id="d4866-130">Možete koristiti mogućnost produženja rezervacije na kartici **Usaglašenost** ili **tabelu rasporeda** da biste rezervisali kapacitet resursa za projekat.</span><span class="sxs-lookup"><span data-stu-id="d4866-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Produženje rezervacije člana tima na kartici Usaglašenost resursa](media/RM-how-to-7.png)

<span data-ttu-id="d4866-132">Nakon što je član tima rezervisan za projekat, možete da koristite održavanje rezervacija ili tabelu rasporeda direktno da biste upravljali rezervacijama.</span><span class="sxs-lookup"><span data-stu-id="d4866-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
