---
title: Kako da dodelim resurs koji može da se rezerviše zadatku u veb aplikaciji
description: Pregled načina na koji možete dodeliti resurse koje je moguće dodeliti.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286310"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="099be-103">Kako da dodeljujete resurs koji može da se rezerviše zadatku u veb aplikaciji (aplikacija Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="099be-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="099be-104">Postoje dva načina dodele resursa zadatku u programu Project Service.</span><span class="sxs-lookup"><span data-stu-id="099be-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="099be-105">Resurs možete da rezervišete kao član tima, a zatim da ga dodelite zadatku.</span><span class="sxs-lookup"><span data-stu-id="099be-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="099be-106">Ili možete da kreirate generičkog člana tima preko dodele uloga na zadacima, generisanja tima, a zatim popunjavanjem zahteva za pravljenje rezervne kopije sa imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="099be-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="099be-107">Imajte u vidu da ako želite da dodelite resurs koji može da se rezerviše zadatku, član tima resursa koji može da se rezerviše mora da ima dovoljno dostupnih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="099be-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="099be-108">Status rezervacije mora da bude tip izvršavanja Fiksno rezerviši i sa statusom Izvršeno.</span><span class="sxs-lookup"><span data-stu-id="099be-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="099be-109">Ako nema dovoljno rezervacija za resurs, Project Service uklanja zadatak i prikazuje sledeću poruku o grešci:</span><span class="sxs-lookup"><span data-stu-id="099be-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="099be-110">*Nije moguće dodeliti resurs zadatku – Sledeće resursi nemaju dovoljno rezervisanih radnih sati za projekat*</span><span class="sxs-lookup"><span data-stu-id="099be-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="099be-111">Rezervišite resurs kao član tima, a zatim dodelite resurs zadatku</span><span class="sxs-lookup"><span data-stu-id="099be-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="099be-112">Sa ovim metodom dodajete resurs u projektni tim, a zatim dodeljujete zadatke resursu u rasporedu projekta.</span><span class="sxs-lookup"><span data-stu-id="099be-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="099be-113">Evo kako to da uradite:</span><span class="sxs-lookup"><span data-stu-id="099be-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="099be-114">U koordinatnoj mreži člana tima dodajte novog člana tima tako što ćete izabrati **Novi**.</span><span class="sxs-lookup"><span data-stu-id="099be-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="099be-115">Na ekranu brzog kreiranja člana tima, izaberite ime resursa koji može da se rezerviše i podesite ulogu.</span><span class="sxs-lookup"><span data-stu-id="099be-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="099be-116">Izaberite datume **Od** i **Do**.</span><span class="sxs-lookup"><span data-stu-id="099be-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="099be-117">![Snimak ekrana dodavanja člana tima](media/FAQ-Resources-to-Tasks2-1.png "Snimak ekrana dodavanja člana tima")</span><span class="sxs-lookup"><span data-stu-id="099be-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="099be-118">Izaberite jedan od sledećih načina dodele za rezervaciju resursa:</span><span class="sxs-lookup"><span data-stu-id="099be-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="099be-119">**Puni kapacitet** rezerviše puni kapacitet resursa za navedene početne i krajnje datume.</span><span class="sxs-lookup"><span data-stu-id="099be-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="099be-120">**Procenat kapaciteta** rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="099be-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="099be-121">**Po satima – Ravnomerno raspoređivanje** rezerviše resurs za određeni broj časova, ravnomerno ih raspoređujući po danu tokom navedenih datuma početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="099be-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="099be-122">**Po satima – Početno opterećenje** rezerviše resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="099be-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="099be-123">Nemojte izabrati **Nijedno** jer on dodaje resurs timu, ali ne kreira nijednu rezervaciju koja troši kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="099be-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="099be-124">Izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="099be-124">Select **Save**.</span></span>

    <span data-ttu-id="099be-125">Imajte u vidu da sati rezervacije moraju da budu dovoljni da pokriju časove angažovanja i periode datuma zadataka kojima dodeljujete ovaj resurs.</span><span class="sxs-lookup"><span data-stu-id="099be-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="099be-126">Ako oni nisu usklađeni, ne možete dodeliti resurs zadatku.</span><span class="sxs-lookup"><span data-stu-id="099be-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="099be-127">Na strukturnoj analizi posla (SAP) za zadatak, kliknite na padajući meni ćelija resursa.</span><span class="sxs-lookup"><span data-stu-id="099be-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="099be-128">Zatim:</span><span class="sxs-lookup"><span data-stu-id="099be-128">Then:</span></span> 

    1. <span data-ttu-id="099be-129">Izaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="099be-129">Select **Add**.</span></span>
    2. <span data-ttu-id="099be-130">Izaberite padajući meni u okviru opcije **Resursi** i izaberite člana tima kojeg ste dodali iznad.</span><span class="sxs-lookup"><span data-stu-id="099be-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="099be-131">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="099be-131">Select **OK**.</span></span> <span data-ttu-id="099be-132">Član tima je sada dodeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="099be-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="099be-133">![Snimak ekrana dodavanja resursa pomoću SAP-a](media/FAQ-Resources-to-Tasks2-2.png "Snimak ekrana dodavanja resursa pomoću SAP-a")</span><span class="sxs-lookup"><span data-stu-id="099be-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="099be-134">U koordinatnoj mreži člana tima, u okviru stavke Dodeljeni časovi videćete agregirane dodeljene radne sate resursa.</span><span class="sxs-lookup"><span data-stu-id="099be-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="099be-135">To će biti manje ili jednako rezervisanim časovima za resurs.</span><span class="sxs-lookup"><span data-stu-id="099be-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="099be-136">![Snimak ekrana dodeljenih časova resursu](media/FAQ-Resources-to-Tasks2-3.png "Snimak ekrana dodeljenih časova resursu")</span><span class="sxs-lookup"><span data-stu-id="099be-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="099be-137">Ako zadatak koji pokušavate da dodelite resursu počinje nakon datuma završetka rezervacija resursa, resurs se neće pojaviti na padajućoj listi.</span><span class="sxs-lookup"><span data-stu-id="099be-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="099be-138">Imajte u vidu da resursu možete da dodelite više časova nego što su njegovi rezervisani časovi ako resurs ima preostali nedodeljeni kapacitet.</span><span class="sxs-lookup"><span data-stu-id="099be-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="099be-139">U tom slučaju, resurs će biti samo delimično dodeljen do njegovih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="099be-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="099be-140">Te preostale nedodeljene sate možete da vidite dodavanjem kolone Časovi bez resursa u strukturnu analizu posla.</span><span class="sxs-lookup"><span data-stu-id="099be-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="099be-141">Ako su resursi dodeljeni svojim rezervisanim časovima (njihovi rezervisani časovi su jednaki njihovim dodeljenim časovima), videćete sledeću poruku o grešci kada pokušate da im dodelite još zadataka:</span><span class="sxs-lookup"><span data-stu-id="099be-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="099be-142">*Nije moguće dodeliti resurs zadatku – Sledeće resursi nemaju dovoljno rezervisanih radnih sati za projekat.*</span><span class="sxs-lookup"><span data-stu-id="099be-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="099be-143">Osim toga, podrazumevani član tima menadžera projekta koji je dodat u tim kada ste kreirali projekat se dodaje bez ikakvih rezervacija i nije mu moguće dodeliti nijedan zadatak.</span><span class="sxs-lookup"><span data-stu-id="099be-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="099be-144">On se neće prikazivati u padajućoj listi resursa za zadatak.</span><span class="sxs-lookup"><span data-stu-id="099be-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="099be-145">Ako želite da dodelite ovaj resurs, potrebno je da ga uklonite iz tima, a zatim ponovo da ga dodate sa načinom dodele koji nije Nijedno.</span><span class="sxs-lookup"><span data-stu-id="099be-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="099be-146">Razlog zbog kog se dodaju timu kada se projekat kreira jeste da bi projekat imao bar jednu podrazumevanu osobu koja odobrava projekat.</span><span class="sxs-lookup"><span data-stu-id="099be-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="099be-147">Kreiranje generičkog člana tima preko dodele uloga za zadatke</span><span class="sxs-lookup"><span data-stu-id="099be-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="099be-148">Ovaj metod osigurava da resursi imaju dovoljno rezervacija za zadatke.</span><span class="sxs-lookup"><span data-stu-id="099be-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="099be-149">Kao prvo, kreirate čuvar mesta ili generički resurs koji opisuje karakteristike imenovanog resursa za kojeg naposletku želite da radi na zadacima generisanjem tima nakon dodele uloga zadacima.</span><span class="sxs-lookup"><span data-stu-id="099be-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="099be-150">Evo kako to da uradite:</span><span class="sxs-lookup"><span data-stu-id="099be-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="099be-151">Na strukturnoj analizi posla, izaberite zadatak.</span><span class="sxs-lookup"><span data-stu-id="099be-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="099be-152">Izaberite ikonu padajućeg liste **Dodeljena uloga** u ćeliji resursa.</span><span class="sxs-lookup"><span data-stu-id="099be-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="099be-153">Izaberite padajuću listu **Uloga** i izaberite ulogu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="099be-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="099be-154">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="099be-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="099be-155">![Snimak ekrana korišćenja SAP-a za dodavanje resursa](media/FAQ-Resources-to-Tasks2-4.png "Snimak ekrana korišćenja SAP-a za dodavanje resursa")</span><span class="sxs-lookup"><span data-stu-id="099be-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="099be-156">Nakon što ste dovršili dodeljivanje uloga zadacima u SAP-u, izaberite **Generisanje projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="099be-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="099be-157">Project Service kreira minimalni broj generičkih članova tima na osnovu uloga, jedinica za određivanje resursa organizacije i kalendara projekta agregiranjem dodela zadatka.</span><span class="sxs-lookup"><span data-stu-id="099be-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="099be-158">![Snimak ekrana generisanja projektnog tima](media/FAQ-Resources-to-Tasks2-5.png "Snimak ekrana generisanja projektnog tima")</span><span class="sxs-lookup"><span data-stu-id="099be-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="099be-159">Na koordinatnoj mreži člana tima videćete resurse tipa Generički resurs sa ulogom i imenom položaja.</span><span class="sxs-lookup"><span data-stu-id="099be-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="099be-160">Ako su potrebna dva resursa za ulogu kako biste dovršili rad, funkcija Generisanje tima kreira dva člana tima i koristi ime položaja kako bi ih razlikovala.</span><span class="sxs-lookup"><span data-stu-id="099be-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="099be-161">![Snimak ekrana dodavanja dva generička resursa](media/FAQ-Resources-to-Tasks2-6.png "Snimak ekrana dodavanja dva generička resursa")</span><span class="sxs-lookup"><span data-stu-id="099be-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="099be-162">Možete otvoriti zahtev za pravljenje rezervne kopije resursa za generičkog člana tima tako što ćete izabrati vezu u okviru opcije Zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="099be-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="099be-163">![Snimak ekrana otvaranja zahteva za pravljenje rezervne kopije resursa](media/FAQ-Resources-to-Tasks2-7.png "Snimak ekrana otvaranja zahteva za pravljenje rezervne kopije resursa")</span><span class="sxs-lookup"><span data-stu-id="099be-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="099be-164">Izaberite stavku **Rezerviši** za generički resurs, a zatim možete da koristite tabelu rasporeda da biste pronašli i rezervisali stvarni resurs.</span><span class="sxs-lookup"><span data-stu-id="099be-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="099be-165">Možete u da prosledite zahtev za ispunjenje po menadžeru resursa tako što ćete izabrati **Prosledi zahtev**.</span><span class="sxs-lookup"><span data-stu-id="099be-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="099be-166">Kada generički resurs bude ispunjen imenovanim resursom, generički resurs se uklanja iz tima, a dodele zadatka iz generičkog resursa se dodeljuju imenovanom resursu koji je ispunio zahtev za resursom generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="099be-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]