---
title: Održavanje članova tima
description: Ova tema pruža informacije o rezervisanju imenovanih resursa za timove projekta i njihovom dodeljivanju zadacima.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131540"
---
# <a name="maintain-team-members"></a><span data-ttu-id="23f1f-103">Održavanje članova tima</span><span class="sxs-lookup"><span data-stu-id="23f1f-103">Maintain team members</span></span>

<span data-ttu-id="23f1f-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="23f1f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="23f1f-105">Možete da dodate imenovani resurs u projektni tim tako što ćete ga direktno rezervisati za tim.</span><span class="sxs-lookup"><span data-stu-id="23f1f-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="23f1f-106">U usluzi Dynamics 365 Project Operations, idite na **Projekti** i otvorite projekat za koji rezervišete resurse.</span><span class="sxs-lookup"><span data-stu-id="23f1f-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="23f1f-107">Na stranici **Projekat**, na kartici **Tim** izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="23f1f-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="23f1f-108">U dijalogu **Brzo kreiranje člana projektnog tima** izaberite resurs koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="23f1f-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="23f1f-109">Polje **Uloga** će se popuniti podrazumevanom ulogom resursa ako je ona dodeljena.</span><span class="sxs-lookup"><span data-stu-id="23f1f-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="23f1f-110">Možete da promenite ulogu.</span><span class="sxs-lookup"><span data-stu-id="23f1f-110">You can change the role.</span></span> 
4. <span data-ttu-id="23f1f-111">Izaberite datum početka i završetka kada vam je resurs potreban i izaberite način dodele kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="23f1f-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="23f1f-112">U polju **Davalac odobrenja za projekat** izaberite opciju **Da** ako želite da član tima bude davalac odobrenja za projekat.</span><span class="sxs-lookup"><span data-stu-id="23f1f-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="23f1f-113">Član tima može da odobri prosleđene stavke vremena i troškova za ovaj projekat.</span><span class="sxs-lookup"><span data-stu-id="23f1f-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="23f1f-114">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="23f1f-114">Select **Save**.</span></span>

<span data-ttu-id="23f1f-115">Sada možete dodeliti rezervisani resurs zadacima u projektu.</span><span class="sxs-lookup"><span data-stu-id="23f1f-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="23f1f-116">Na stranici **Projekat** kliknite na karticu **Raspored** da biste dodelili zadatke novom resursu.</span><span class="sxs-lookup"><span data-stu-id="23f1f-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="23f1f-117">Birač resursa koji je pokrenut iz polja **Resursi** u mreži zadataka će prikazati članove tima koje možete izabrati.</span><span class="sxs-lookup"><span data-stu-id="23f1f-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="23f1f-118">U usluzi Project Operations, rezervisanja resursa i dodele zadataka nisu usko povezani.</span><span class="sxs-lookup"><span data-stu-id="23f1f-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="23f1f-119">Kada koristite birač resursa u rasporedu, možete da dodelite zadatke članovima tima za više sati nego što pokriva njihovo vreme rezervisanja za projekat.</span><span class="sxs-lookup"><span data-stu-id="23f1f-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="23f1f-120">Razlike između rezervacija i dodela članova tima prikazane su na karticama **Tim** i **Usaglašavanje resursa**.</span><span class="sxs-lookup"><span data-stu-id="23f1f-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="23f1f-121">Razlike između rezervacija i dodele resursa možete uskladiti i na detaljnijem nivou.</span><span class="sxs-lookup"><span data-stu-id="23f1f-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="23f1f-122">Koristite birač resursa na kartici **Raspored** da biste potražili i izabrali resurse koji mogu da se rezervišu, a koji još nisu deo projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="23f1f-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="23f1f-123">Ovi resursi se prikazuju u biraču resursa kao **Ostali resursi**.</span><span class="sxs-lookup"><span data-stu-id="23f1f-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="23f1f-124">Kada to napravite izbor, resurs će biti dodat u projektni tim i dodeljen zadatku, ali se ne generišu rezervacije.</span><span class="sxs-lookup"><span data-stu-id="23f1f-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="23f1f-125">Možete koristiti mogućnost produženja rezervacije na kartici **Usaglašenost** ili **tabelu rasporeda** da biste rezervisali kapacitet resursa za projekat.</span><span class="sxs-lookup"><span data-stu-id="23f1f-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="23f1f-126">Kada se član tima rezerviše za projekat, možete da koristite **Održavanje rezervacija** ili **tabelu rasporeda** direktno da biste upravljali rezervacijama.</span><span class="sxs-lookup"><span data-stu-id="23f1f-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
