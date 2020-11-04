---
title: Dodeljivanje resursa zadatku
description: Ova tema pruža informacije o tome kako dodeliti resurse zadacima.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083769"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="44121-103">Dodeljivanje resursa zadatku</span><span class="sxs-lookup"><span data-stu-id="44121-103">Assign a resource to a task</span></span>

<span data-ttu-id="44121-104">Postoje tri načina dodele resursa zadatku u aplikaciji Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="44121-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="44121-105">Rezervisanje resursa kao člana tima i dodela resursa zadatku</span><span class="sxs-lookup"><span data-stu-id="44121-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="44121-106">Resurs možete da dodate u projektni tim, a zatim da dodeljujete resurs zadacima u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="44121-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="44121-107">Na kartici **Član tima** dodajte novog člana tima tako što ćete izabrati **Novi**.</span><span class="sxs-lookup"><span data-stu-id="44121-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="44121-108">Otvara se tabla za **brzo kreiranje člana tima** , gde možete da izaberete ime resursa koji može da se rezerviše i podesite ulogu.</span><span class="sxs-lookup"><span data-stu-id="44121-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="44121-109">Izaberite jedan od sledećih načina dodele za rezervaciju resursa:</span><span class="sxs-lookup"><span data-stu-id="44121-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="44121-110">**Puni kapacitet** rezerviše puni kapacitet resursa za navedene početne i krajnje datume.</span><span class="sxs-lookup"><span data-stu-id="44121-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="44121-111">**Procenat kapaciteta** rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="44121-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="44121-112">**Ravnomerno raspoređivanje po satima** rezerviše resurs za određeni broj časova, ravnomerno ih raspoređujući po danu tokom navedenih datuma početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="44121-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="44121-113">**Po satima – Početno opterećenje** rezerviše resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="44121-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="44121-114">**Nijedno** dodaje resurs timu, ali ne kreira nijednu rezervaciju koja troši njihov kapacitet.</span><span class="sxs-lookup"><span data-stu-id="44121-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="44121-115">Na mreži **Raspored** za zadatak, izaberite ikonu **Resurs** u ćeliji resursa, a zatim u delu **Članovi tima** izaberite člana tima kojeg ste upravo dodali.</span><span class="sxs-lookup"><span data-stu-id="44121-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="44121-116">Resurs prikazuje rezervisane i dodeljene časove i na karticama **Član tima** i **Usaglašenost**.</span><span class="sxs-lookup"><span data-stu-id="44121-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="44121-117">Sati bi trebalo da budu isti, ali to nije neophodno jer rezervacije i dodele nisu čvrsto povezane.</span><span class="sxs-lookup"><span data-stu-id="44121-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="44121-118">Kartica **Usaglašenost** vam daje detalje kada se razlikuju, kao kada dodelite resursu više časova nego što ste rezervisali.</span><span class="sxs-lookup"><span data-stu-id="44121-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="44121-119">Po potrebi možete da ispravite informacije proširivanjem rezervacije resursa ili promenom dodele.</span><span class="sxs-lookup"><span data-stu-id="44121-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="44121-120">Kreiranje generičkog člana tima preko dodele zadatka</span><span class="sxs-lookup"><span data-stu-id="44121-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="44121-121">Kada kreirate generičkog člana tima preko dodele zadatka, kreirate čuvar mesta ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg naposletku želite da radi na zadacima.</span><span class="sxs-lookup"><span data-stu-id="44121-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="44121-122">Zatim generišete uslov (ili prosleđujete zahtev korišćenjem zahteva) koji se koristi za pretragu i rezervaciju imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="44121-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="44121-123">Na mreži **Raspored** za zadatak, izaberite ikonu **resursa** u ćeliji Resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="44121-124">Unesite ime koje će služiti kao ime čuvara mesta resursa.</span><span class="sxs-lookup"><span data-stu-id="44121-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="44121-125">Na primer, Menadžer programa.</span><span class="sxs-lookup"><span data-stu-id="44121-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="44121-126">Izaberite **Kreiraj** , pa u polju **Brzo kreiranje člana projektnog tima** podesite ulogu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="44121-127">Možete da nastavite sa dodelom zadataka u ovaj resurs čuvara mesta izborom resursa u **biraču resursa** za zadatak.</span><span class="sxs-lookup"><span data-stu-id="44121-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="44121-128">Oni su navedeni u okviru opcije **Članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="44121-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="44121-129">Kada završite sa dodeljivanjem generičkog resursa, izaberite generički resurs na kartici **Tim** , a zatim izaberite **Generiši potrebu** da biste kreirali potrebu za resursom za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="44121-130">Izaberite opciju **Rezerviši** za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="44121-131">Zatim možete da koristite tabelu rasporeda da biste pronašli i rezervisali pravi resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="44121-132">Možete i da prosledite zahtev za ispunjenje od strane menadžera resursa.</span><span class="sxs-lookup"><span data-stu-id="44121-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="44121-133">Kada generički resurs bude ispunjen imenovanim resursom, generički resurs se uklanja iz tima, a dodele zadatka iz generičkog resursa se dodeljuju imenovanom resursu koji je ispunio zahtev za resursom generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="44121-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="44121-134">Dodela imenovanog resursa sa liste svih resursa koji mogu da se rezervišu</span><span class="sxs-lookup"><span data-stu-id="44121-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="44121-135">Možete da koristite polje za pretragu u **biraču resursa** da biste pretraživali sve resurse koji mogu da se rezervišu i da ih dodelite zadatku.</span><span class="sxs-lookup"><span data-stu-id="44121-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="44121-136">Resursi dodeljeni na ovaj način dodaju se u tim bez ikakvih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="44121-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="44121-137">To je slično dodavanju člana tima i odluci da ne izaberete nijednu metodu dodele.</span><span class="sxs-lookup"><span data-stu-id="44121-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="44121-138">Resurs se prikazuju na karticama **Tim** i **Usaglašenost** kao resurs samo sa dodelama i sa nedostatkom rezervacije.</span><span class="sxs-lookup"><span data-stu-id="44121-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="44121-139">Rezervišete ih ako želite da koristite njihovu dostupnost.</span><span class="sxs-lookup"><span data-stu-id="44121-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="44121-140">Na mreži **Raspored** za zadatak, izaberite ikonu **resursa** u ćeliji Resurs.</span><span class="sxs-lookup"><span data-stu-id="44121-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="44121-141">Započnite unos imena.</span><span class="sxs-lookup"><span data-stu-id="44121-141">Start typing a name.</span></span> <span data-ttu-id="44121-142">Prikazuju se rezultati pretrage za ime u **biraču resursa** u okviru opcije **Drugi resursi**.</span><span class="sxs-lookup"><span data-stu-id="44121-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="44121-143">Izaberite resurs koji želite da dodelite zadatku.</span><span class="sxs-lookup"><span data-stu-id="44121-143">Select the resource that you want to assign to the task.</span></span>

