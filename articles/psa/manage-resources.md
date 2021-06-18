---
title: Upravljanje resursima
description: Ova tema pruža informacije o tome kako možete da upravljate resursima.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997843"
---
# <a name="manage-resources"></a><span data-ttu-id="44466-103">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="44466-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="44466-104">Dynamics 365 Project Service Automation uključuje kontrolnu tablu menadžera resursa koja pruža vizuelni pregled potražnje i ukupne iskorišćenosti resursa u celoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="44466-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="44466-105">Možete koristiti grafikone na ovoj kontrolnoj tabli da biste vizualizovali sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="44466-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="44466-106">**Potražnja za resursima** - Grafikon **Aktivni zahtevi za resurse** prikazuje resurse koji su prosleđeni.</span><span class="sxs-lookup"><span data-stu-id="44466-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="44466-107">Resursi se objedinjuju po ulozi ili projektu.</span><span class="sxs-lookup"><span data-stu-id="44466-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="44466-108">**Neprosleđena potražnja za resursima** - Grafikon **Nedodeljena potražnja za resursima** prikazuje sve potrebe za resursima koje nisu prosleđene.</span><span class="sxs-lookup"><span data-stu-id="44466-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="44466-109">To pomaže menadžerima resursa da pogledaju potražnju koja nije čvrsta i koja može biti prosleđena putem zahteva za resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="44466-110">**Naplativa ukupna iskorišćenost tokom prošle sedmice** - Grafikon **Ukupna iskorišćenost prema ulozi** prikazuje procenat stvarne ukupne iskorišćenosti prema ulogama u organizaciji u odnosu na ciljanu naplativu ukupnu iskorišćenost po ulozi.</span><span class="sxs-lookup"><span data-stu-id="44466-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="44466-111">Da bi grafikon **Ukupna iskorišćenost prema ulozi** bio dostupan, kreirajte posao koji pokreće tok posla UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="44466-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="44466-112">Ovaj periodičan posao se pokreće svakih sedam dana kako bi se izračunala naplativa ukupna iskorišćenost za prethodnih sedam dana.</span><span class="sxs-lookup"><span data-stu-id="44466-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="44466-113">Rezultati se objedinjuju po ulogama.</span><span class="sxs-lookup"><span data-stu-id="44466-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="44466-114">Upravljanje članovima projektnog tima</span><span class="sxs-lookup"><span data-stu-id="44466-114">Manage project team members</span></span>

<span data-ttu-id="44466-115">Menadžeri projekata mogu koristiti kontrolnu tablu za upravitelje resursima za upravljanje resursima na projektima.</span><span class="sxs-lookup"><span data-stu-id="44466-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="44466-116">Na primer, mogu da dodaju člana tima direktno u projekat i rezervišu člana tima da ispune potrebe za resursima koje je evidentirao generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="44466-117">Dodavanje člana tima direktno u projekat</span><span class="sxs-lookup"><span data-stu-id="44466-117">Add a team member directly to a project</span></span>

<span data-ttu-id="44466-118">Da biste direktno dodali člana tima u projekat, na stranici **Projekti**, na kartici **Tim** odaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="44466-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="44466-119">Pojaviće se dijalog **Brzo kreiranje člana projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="44466-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="44466-120">U ovom dijalogu možete izvršiti ove zadatke:</span><span class="sxs-lookup"><span data-stu-id="44466-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="44466-121">**Rezervisanje imenovanog resursa** - U polju **Resurs koji može da se rezerviše** odaberite ime resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="44466-122">Zatim izaberite ulogu, podesite period i izaberite način dodeljivanja.</span><span class="sxs-lookup"><span data-stu-id="44466-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="44466-123">Imenovani resurs koji ste odabrali dodaje se projektu upotrebom odabranog načina dodele i kalendara resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="44466-124">**Dodavanje generičkog resursa** - Ostavite polje **Resurs koji može da se rezerviše** prazno, a zatim odaberite ulogu, podesite period i izaberite željeni način dodeljivanja.</span><span class="sxs-lookup"><span data-stu-id="44466-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="44466-125">U tim se dodaje generički resurs kao čuvar mesta koji sadrži obrazac potražnje koji se koristi za rezervisanje imenovanih resursa za tim.</span><span class="sxs-lookup"><span data-stu-id="44466-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="44466-126">Zahtev se postavlja prema kalendaru projekta.</span><span class="sxs-lookup"><span data-stu-id="44466-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="44466-127">**Dodavanje imenovanog resursa u tim bez trošenja kapaciteta resursa** - U polju **Resurs koji može da se rezerviše** odaberite resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="44466-128">Zatim izaberite period i izaberite **Nijedan** kao način dodeljivanja.</span><span class="sxs-lookup"><span data-stu-id="44466-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="44466-129">Resurs se dodaje u tim, ali kapacitet resursa se ne troši rezervacijom.</span><span class="sxs-lookup"><span data-stu-id="44466-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="44466-130">Rezervisanje člana tima radi ispunjavanja potrebe za generičkim resursom</span><span class="sxs-lookup"><span data-stu-id="44466-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="44466-131">U aplikaciji PSA možete da rezervišete generički resurs za projektni tim i možete da odredite ulogu, potrebni kapacitet i kako se taj kapacitet distribuira.</span><span class="sxs-lookup"><span data-stu-id="44466-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="44466-132">U okviru potrebe za resursom možete da navedete atribute koji su povezani sa generičkim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="44466-133">Ovi atributi uključuju tražene veštine, željenu organizacionu jedinicu i željene resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="44466-134">Sledite ove korake da biste naveli potrebne veštine generičkog resursa za programera.</span><span class="sxs-lookup"><span data-stu-id="44466-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="44466-135">Na stranici **Projekti** na kartici **Tim** odaberite **Novi** da rezervišete generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Generički resurs rezervisan za tim](media/Resource-Management-image9.png)

2. <span data-ttu-id="44466-137">U prikazu **Svi članovi tima**, u koloni **Potreba za resursom** izaberite vezu da dodate potrebne veštine za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Veza zahteva](media/Resource-Management-image10.png)

3. <span data-ttu-id="44466-139">Na stranici **Potreba za resursom** koja se pojavljuje u mreži **Veštine** odaberite tri tačke (**...**), a zatim izaberite **Dodaj novu karakteristiku zahteva** da dodate potrebne veštine za programera.</span><span class="sxs-lookup"><span data-stu-id="44466-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Komanda za dodavanje nove karakteristike zahteva](media/Resource-Management-image11.png)

4. <span data-ttu-id="44466-141">U dijalogu **Brzo kreiranje karakteristike zahteva** koji se pojavljuje, u polju **Karakteristike** odaberite željenu veštinu.</span><span class="sxs-lookup"><span data-stu-id="44466-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="44466-142">Zatim, u polju **Vrednost ocene** odaberite nivo stručnosti za ovu veštinu.</span><span class="sxs-lookup"><span data-stu-id="44466-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="44466-143">Konačno u polju **Potreba za resursom** podesite potrebu da biste obezbedili resurse iz organizacionih jedinica ili čak imenovanih resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="44466-144">Kada završite, izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="44466-144">When you've finished, select **Save**.</span></span>

    ![Dijalog za brzo kreiranje karakteristika zahteva](media/Resource-Management-image12.png)

5. <span data-ttu-id="44466-146">Na stranici **Potreba za resursom** izaberite **Rezerviši** da biste ispunili potrebu za resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Dugme za rezervisanje na stranici Potreba za resursom](media/Resource-Management-image13.png)

    <span data-ttu-id="44466-148">Takođe možete odabrati generički resurs u mreži **Svi članovi tima**, a zatim izabrati **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="44466-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Dugme za rezervaciju iznad mreže Svi članovi tima](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="44466-150">U ovom primeru, postoji 40 zahtevanih sati, ali nema stvarno rezerviranih sati, jer generički resursi nemaju rezervacije.</span><span class="sxs-lookup"><span data-stu-id="44466-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="44466-151">Uz to, nema dodeljenih sati, jer je generički resurs dodat direktno u tim.</span><span class="sxs-lookup"><span data-stu-id="44466-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="44466-152">Nije dodat dodeljivanjem zadatka.</span><span class="sxs-lookup"><span data-stu-id="44466-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="44466-153">Na stranici **Pomoćnik za zakazivanje** možete filtrirati dostupne resurse prema potrebama koje su navedene u potrebi za resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="44466-154">Resursi su sortirani prema parametrima sortiranja koji su navedeni na tabeli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="44466-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Stranica Pomoćnik za zakazivanje](media/Resource-Management-image15.png)

    <span data-ttu-id="44466-156">Evo nekoliko filtera koji se često koriste:</span><span class="sxs-lookup"><span data-stu-id="44466-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="44466-157">**Karakteristike uz ocenu** - Filtrirajte po veštinama, certifikacijama i drugim kvalitetima resursa, pored ocena stručnosti.</span><span class="sxs-lookup"><span data-stu-id="44466-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="44466-158">**Uloge** - Filtrirajte prema podrazumevanim ulogama koje su dodeljene resursima koji mogu da se rezervišu.</span><span class="sxs-lookup"><span data-stu-id="44466-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="44466-159">**Organizacione jedinice** - Filtrirajte resurse koji mogu da se rezervišu prema organizacionim jedinicama kojima su dodeljeni.</span><span class="sxs-lookup"><span data-stu-id="44466-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="44466-160">Ako niste zadovoljni rezultatima inicijalne pretrage zahteva, možete promeniti kriterijume filtriranja.</span><span class="sxs-lookup"><span data-stu-id="44466-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="44466-161">Proširite okno **Prikaz filtera** sa leve strane, a zatim izaberite **Pretraži** da biste pronašli dodatne resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Okno sa prikazom filtera](media/Resource-Management-image16.png)

7. <span data-ttu-id="44466-163">Da biste promenili način sortiranja rezultata, izaberite **Sortiraj**.</span><span class="sxs-lookup"><span data-stu-id="44466-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Komanda za sortiranje](media/Resource-Management-image17.png)

8. <span data-ttu-id="44466-165">Odaberite resurse u skladu sa potražnjom koja je navedena u zahtevu, kao što je naznačeno u vrhu mreže.</span><span class="sxs-lookup"><span data-stu-id="44466-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="44466-166">Možete izbrisati izbor ćelija u mreži i ostaviti otvoren kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="44466-167">Samo jedan resurs može biti izabran kao rezervisan u određenom trenutku.</span><span class="sxs-lookup"><span data-stu-id="44466-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="44466-168">Izaberite **Rezerviši** da rezervišete izabrani resurs i ostavite tabelu rasporeda otvorenu, tako da možete da izaberete dodatne resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="44466-169">Ili odaberite **Rezerviši i izađi** da rezervišete izabrani resurs i zatvorite tabelu rasporeda.</span><span class="sxs-lookup"><span data-stu-id="44466-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Resurs za rezervaciju](media/Resource-Management-image19.png)

    <span data-ttu-id="44466-171">Dobijate obaveštenje o rezervisanim satima.</span><span class="sxs-lookup"><span data-stu-id="44466-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="44466-172">Pokazatelji potražnje pokazuju koliko je zahtev za rezervaciju ispunjen i koliko još ostaje.</span><span class="sxs-lookup"><span data-stu-id="44466-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="44466-173">Takođe možete videti koliko je potrošeno kapaciteta odabranog resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="44466-174">Izaberite **Proširi** da biste videli više detalja o rezervacijama resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="44466-175">Vratite se na prikaz **Svi članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="44466-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="44466-176">U mreži možete da primetite da je generički resurs zamenjen imenovanim resursom i da je 40 sati navedeno kao rezervirano za taj resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Mreža Ažurirani svi članovi tima](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="44466-178">Nisu prikazani dodeljeni sati jer su rezervisani direktno u timu.</span><span class="sxs-lookup"><span data-stu-id="44466-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="44466-179">Nisu rezervisani korišćenjem dodela zadatka.</span><span class="sxs-lookup"><span data-stu-id="44466-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="44466-180">Dodeljivanje generičkih resursa zadacima i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="44466-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="44466-181">U aplikaciji PSA možete da kreirate zadatke i da im onda dodelite generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="44466-182">Na ovaj način, potražnja za resursima može biti predstavljena čuvarima mesta dok procenjujete svoj raspored i finansijske brojke.</span><span class="sxs-lookup"><span data-stu-id="44466-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="44466-183">Zatim možete da generišete potrebe za generičkim resursima i ispunite ih.</span><span class="sxs-lookup"><span data-stu-id="44466-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="44466-184">Na stranici **Projekti** na kartici **Raspored** odaberite **Dodaj** da kreirate zadatak.</span><span class="sxs-lookup"><span data-stu-id="44466-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Kreiran je novi zadatak](media/Resource-Management-image21.png)

2. <span data-ttu-id="44466-186">U polju **Resursi** izaberite simbol **birača resursa**.</span><span class="sxs-lookup"><span data-stu-id="44466-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="44466-187">Pojavljuje se birač resursa i pokazuje postojeće članove tima za projekat.</span><span class="sxs-lookup"><span data-stu-id="44466-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Birač resursa](media/Resource-Management-image22.png)

3. <span data-ttu-id="44466-189">Unesite ime novog generičkog resursa, a zatim izaberite **Kreiraj**.</span><span class="sxs-lookup"><span data-stu-id="44466-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Uneto je ime novog generičkog resursa](media/Resource-Management-image23.png)

4. <span data-ttu-id="44466-191">U dijalogu **Brzo kreiranje člana projektnog tima** koji se pojavljuje, u polju **Uloga** odaberite ulogu generičkog resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="44466-192">U polju **Jedinica za obezbeđivanje resursa** izaberite organizacionu jedinicu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="44466-193">Zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="44466-193">Then select **Save**.</span></span>

    ![Dijalog za brzo kreiranje člana projektnog tima](media/Resource-Management-image24.png)

    <span data-ttu-id="44466-195">Generički član tima je sada dodeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="44466-195">The generic team member is now assigned to the task.</span></span>

    ![Generički član tima je dodeljen zadatku](media/Resource-Management-image25.png)

    <span data-ttu-id="44466-197">Na kartici **Tim** videćete novog generičkog člana tima.</span><span class="sxs-lookup"><span data-stu-id="44466-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="44466-198">Imajte na umu da ima samo dodeljene sate.</span><span class="sxs-lookup"><span data-stu-id="44466-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="44466-199">Ovi časovi su zbir svih zadataka koji su dodeljeni generičkom članu tima.</span><span class="sxs-lookup"><span data-stu-id="44466-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="44466-200">Generički član tima još uvek nema zahtevane sate niti potrebu za resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Generički član tima na kartici Tim](media/Resource-Management-image26.png)

5. <span data-ttu-id="44466-202">Sada možete dodeliti generičkog člana tima drugim zadacima pomoću birača resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Generički član tima u biraču resursa](media/Resource-Management-image27.png)

    <span data-ttu-id="44466-204">Kada završite sa dodeljivanjem generičkog resursa zadacima, možete da generišete potrebu za generičkim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="44466-205">Na kartici **Tim** izaberite generički resurs, a zatim izaberite **Generiši zahtev**.</span><span class="sxs-lookup"><span data-stu-id="44466-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Komanda za generisanje zahteva](media/Resource-Management-image28.png)

    <span data-ttu-id="44466-207">Kada se zahtev generiše, član generičkog tima će imati zahtevane sate i vezu ka potrebi za resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Veza ka potrebi za resursom](media/Resource-Management-image29.png)

    <span data-ttu-id="44466-209">Kada rezervišete imenovani resurs, generički resurs se uklanja iz tima i zamenjuje imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Generički resurs je zamenjen imenovanim resursom](media/Resource-Management-image30.png)

    <span data-ttu-id="44466-211">Na kartici **Raspored** se dodele generičkim resursima uklanjaju i zamenjuju imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Dodele generičkim resursima su zamenjene imenovanim resursom na kartici Raspored](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="44466-213">Ovo ponašanje se dešava samo kada je imenovani resurs u potpunosti rezervisan za potrebu za generičkim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="44466-214">Kada imenovani resurs delimično zamenjuje potrebu za generičkim resursom ili više imenovanih resursa zamenjuje potrebu za generičkim resursima, generički resurs ostaje dodeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="44466-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="44466-215">Na sledećoj ilustraciji, zadatak od 80 sati je planiran za period od pet dana (16 sati dnevno tokom pet dana) i dodeljen je generičkom resursu koji se zove **Funkcionalni**.</span><span class="sxs-lookup"><span data-stu-id="44466-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![Osamdesetčasovni zadatak za pet dana je dodeljen funkcionalnom generičkom resursu](media/Resource-Management-image32.png)

    <span data-ttu-id="44466-217">Kada generišete zahtev, on je za 80 sati tokom petodnevnog perioda.</span><span class="sxs-lookup"><span data-stu-id="44466-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Zahtev je generisan za 80 sati tokom pet dana](media/Resource-Management-image33.png)

    <span data-ttu-id="44466-219">Budući da dostupni resursi rade samo osam sati dnevno, potrebna su dva resursa da bi se ispunio zahtev.</span><span class="sxs-lookup"><span data-stu-id="44466-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Drugi resurs](media/Resource-Management-image35.png)

    <span data-ttu-id="44466-221">Na kartici **Tim** sada možete videti da generički resurs nema zahtevane sate, ali dodeljeni sati se i dalje pojavljuju zajedno sa dva imenovana resursa koja čine ispunjenje.</span><span class="sxs-lookup"><span data-stu-id="44466-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dva imenovana resursa na kartici Tim](media/Resource-Management-image36.png)

    <span data-ttu-id="44466-223">Na kartici **Raspored** generički resurs ostaje dodeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="44466-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Generički resursi na kartici Raspored](media/Resource-Management-image37.png)

<span data-ttu-id="44466-225">PSA ne dodeljuje oba resursa zadatku, jer bi takvim ponašanjem nastao manje predvidljiv raspored.</span><span class="sxs-lookup"><span data-stu-id="44466-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="44466-226">U ovom jednostavnom primeru lako je podjednako podeliti sate na dva resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="44466-227">Međutim, u složenijim scenarijima koji uključuju više zadataka i više resursa, PSA bi morao da pretpostavi kako treba da rasporedi rezervacije koje su primljene za više resursa u više zadataka.</span><span class="sxs-lookup"><span data-stu-id="44466-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="44466-228">Stoga je u tim scenarijima rukovodilac projekta odgovoran za raščlanjivanje više rezervacija i njihovo dodeljivanje prema potrebi.</span><span class="sxs-lookup"><span data-stu-id="44466-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="44466-229">Da bi dodelio rezervacije, menadžer projekta dodeljuje zadatke iz generičkih resursa imenovanim resursima i zatim koristi prikaz **Usaglašenost** da bi osigurao da dodela funkcioniše sa rezervacijama.</span><span class="sxs-lookup"><span data-stu-id="44466-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="44466-230">Uređivanje potrebe za resursom</span><span class="sxs-lookup"><span data-stu-id="44466-230">Edit a resource requirement</span></span>

<span data-ttu-id="44466-231">Nakon što kreira potrebu za resursom, menadžer projekta ili menadžer resursa možda će želeti da izmeni detalje kako bi precizirao kriterijume za pretragu kada se koristi tabela rasporeda.</span><span class="sxs-lookup"><span data-stu-id="44466-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="44466-232">Da biste uredili potrebu za resursom, sledite ove korake.</span><span class="sxs-lookup"><span data-stu-id="44466-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="44466-233">Na stranici **Projekti** na kartici **Tim** odaberite vezu ka bilo kom zahtevu za generički resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="44466-234">Na stranici **Potreba za resursom** koja se pojavljuje možete ažurirati nekoliko atributa.</span><span class="sxs-lookup"><span data-stu-id="44466-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="44466-235">U nastavku su navedeni neki primeri:</span><span class="sxs-lookup"><span data-stu-id="44466-235">Here are some examples:</span></span>

    - <span data-ttu-id="44466-236">Ime</span><span class="sxs-lookup"><span data-stu-id="44466-236">Name</span></span>
    - <span data-ttu-id="44466-237">Od datuma</span><span class="sxs-lookup"><span data-stu-id="44466-237">From Date</span></span>
    - <span data-ttu-id="44466-238">Do datuma</span><span class="sxs-lookup"><span data-stu-id="44466-238">To Date</span></span>
    - <span data-ttu-id="44466-239">Trajanje</span><span class="sxs-lookup"><span data-stu-id="44466-239">Duration</span></span>
    - <span data-ttu-id="44466-240">Tip resursa</span><span class="sxs-lookup"><span data-stu-id="44466-240">Resource Type</span></span>

<span data-ttu-id="44466-241">Na stranici **Potreba za resursom** menadžer projekta ili menadžer resursa takođe može definisati sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="44466-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="44466-242">Veštine</span><span class="sxs-lookup"><span data-stu-id="44466-242">Skills</span></span>
- <span data-ttu-id="44466-243">Uloge</span><span class="sxs-lookup"><span data-stu-id="44466-243">Roles</span></span>
- <span data-ttu-id="44466-244">Željene postavke resursa</span><span class="sxs-lookup"><span data-stu-id="44466-244">Resource preferences</span></span>
- <span data-ttu-id="44466-245">Željenu organizacionu jedinicu</span><span class="sxs-lookup"><span data-stu-id="44466-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="44466-246">Ažuriranje rezervacija resursa nakon njihovog rezervisanja za projekat</span><span class="sxs-lookup"><span data-stu-id="44466-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="44466-247">Nakon što dodate generički ili imenovani resurs u projektni tim, možete promeniti rezervacije resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="44466-248">Na stranici **Projekti** na kartici **Tim** odaberite člana tima, a zatim izaberite **Održavanje rezervacija**.</span><span class="sxs-lookup"><span data-stu-id="44466-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Tabela rasporeda se otvara za izabranog člana tima](media/Resource-Management-image40.png)

    <span data-ttu-id="44466-250">Pojavljuje se tabela rasporeda i prikazuje rezervacije člana projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="44466-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="44466-251">Proširite evidenciju člana tima da biste videli sate koji su rezervisani za ovaj projekat i druge projekte koji troše kapacitet člana tima.</span><span class="sxs-lookup"><span data-stu-id="44466-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="44466-252">Izaberite i prevucite rezervaciju da biste je proširili ili skratili.</span><span class="sxs-lookup"><span data-stu-id="44466-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="44466-253">Pojaviće se dijalog **Kreiranje rezervacije resursa** koji vam omogućava da podesite rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="44466-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dijalog za kreiranje rezervacije resursa](media/Resource-Management-image41.png)

3. <span data-ttu-id="44466-255">Kliknite desnim tasterom miša na rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="44466-255">Right-click the booking.</span></span> <span data-ttu-id="44466-256">Zatim možete da koristite meni sa prečicama da biste dovršili sledeće radnje:</span><span class="sxs-lookup"><span data-stu-id="44466-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="44466-257">Promenite status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="44466-257">Change the booking status.</span></span>
    - <span data-ttu-id="44466-258">Uredite rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="44466-258">Edit the booking.</span></span>
    - <span data-ttu-id="44466-259">Zamenite resurs u projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="44466-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="44466-260">Promena statusa rezervacije</span><span class="sxs-lookup"><span data-stu-id="44466-260">Change the booking status</span></span>

<span data-ttu-id="44466-261">Možete promeniti bilo koji podrazumevani ili prilagođeni status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="44466-261">You can change any default or custom booking status.</span></span>

![Komanda za promenu statusa](media/Resource-Management-image42.png)

<span data-ttu-id="44466-263">Sledeći statusi su uvršteni u PSA:</span><span class="sxs-lookup"><span data-stu-id="44466-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="44466-264">**Otkazan** - Ovaj status otkazuje rezervaciju resursa i oslobađa kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="44466-265">**Fiksna rezervacija** - Ovaj status troši kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="44466-266">Rezervacija obično ima ovaj status kada se otvorite **Održavanje rezervacija** na mreži **Svi članovi tima** na stranici **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="44466-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="44466-267">**Uslovna rezervacija** - Ovaj status dodaje resurs u tim, ali ne troši njegov kapacitet.</span><span class="sxs-lookup"><span data-stu-id="44466-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="44466-268">Ukazuje da je resurs rezervisan za potencijalni rad, ali još uvek ima kapacitet ako je potreban na drugim poslovima.</span><span class="sxs-lookup"><span data-stu-id="44466-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="44466-269">S obzirom na ukupnu dostupnost resursa, uslovne rezervacije imaju drugačiji status od fiksnih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="44466-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="44466-270">**Predložen** - Ovaj status predstavlja predlog menadžera resursa ili menadžera projekata za resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="44466-271">Predlozi ne troše kapacitet resursa i resurs se ne dodaje projektnom timu.</span><span class="sxs-lookup"><span data-stu-id="44466-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="44466-272">Da bi rezervacija resursa za tim bila fiksna, menadžer projekta mora prihvatiti predlog.</span><span class="sxs-lookup"><span data-stu-id="44466-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="44466-273">Prosledite zahteve za resurse</span><span class="sxs-lookup"><span data-stu-id="44466-273">Submit resource requests</span></span>

<span data-ttu-id="44466-274">Zahtevi za resurse koriste se da prenesu potražnju (potrebe za resursima) koja mora biti ispunjena od strane menadžera resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="44466-275">Za generički resurs koji je već u timu možete direktno da prosledite zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="44466-276">Zahtev za resurs može se ispuniti na dva načina:</span><span class="sxs-lookup"><span data-stu-id="44466-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="44466-277">Menadžer resursa direktno ispunjava zahtev.</span><span class="sxs-lookup"><span data-stu-id="44466-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="44466-278">U ovom slučaju, generički resurs zamenjuje fiksna rezervacija koja ima imenovani resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="44466-279">Menadžer resursa predlaže resurs menadžeru projekata, a menadžer projekta odobrava ili odbacuje predloženi resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="44466-280">Direktno ispunjavanje zahteva za resurse</span><span class="sxs-lookup"><span data-stu-id="44466-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="44466-281">Kada se generiše potreba za resursom, projektni menadžer može da prosledi zahtev za generički resurs ako izabere resurs, a zatim opciju **Prosledi zahtev**.</span><span class="sxs-lookup"><span data-stu-id="44466-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Dugme Prosledi zahtev](media/Resource-Management-image45.png)

<span data-ttu-id="44466-283">Komentari o resursu mogu se dostaviti menadžeru resursa koji ispunjava zahtev.</span><span class="sxs-lookup"><span data-stu-id="44466-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="44466-284">Nakon prosleđivanja zahteva, polje **Status** za člana tima se menja u **Prosleđen**.</span><span class="sxs-lookup"><span data-stu-id="44466-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Unošenje opcionalnih komentara](media/Resource-Management-image46.png)

<span data-ttu-id="44466-286">Kada menadžer resursa ispuni zahtev, generičkog člana tima zamenjuje imenovani resurs u mreži **Svi članovi tima**.</span><span class="sxs-lookup"><span data-stu-id="44466-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Generički član tima zamenjen je imenovanim resursom u mreži Svi članovi tima](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="44466-288">Korišćenje predloga resursa za zahteve za resurse</span><span class="sxs-lookup"><span data-stu-id="44466-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="44466-289">Umesto da direktno rezerviše resurs u zahtevu za resurse, menadžer resursa može da predloži resurs menadžeru projekata.</span><span class="sxs-lookup"><span data-stu-id="44466-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="44466-290">Menadžer resursa mogao bi koristiti ovu opciju kada nije dostupno tačno podudaranje sa potrebama.</span><span class="sxs-lookup"><span data-stu-id="44466-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="44466-291">Kada menadžer resursa predloži resurs, menadžer projekata vidi da je polje **Status** za generičkog člana tima promenjeno u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="44466-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Status generičkog člana tima promenjen je u Zahteva pregled](media/Resource-Management-image48.png)

<span data-ttu-id="44466-293">Da biste pregledali predloženi resurs zajedno sa vizuelizacijom efekta rezervacije predloga, dvaput kliknite na člana tima koji ima status **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="44466-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="44466-294">Zatim izaberite karticu **Predloženi resursi**.</span><span class="sxs-lookup"><span data-stu-id="44466-294">Then select the **Proposed Resources** tab.</span></span>

![Kartica Predloženi resursi](media/Resource-Management-image49.png)

<span data-ttu-id="44466-296">Izaberite **Prihvati sve predloge** da prihvate sve predložene resurse ili **Odbacite sve predloge** da ih odbacite.</span><span class="sxs-lookup"><span data-stu-id="44466-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="44466-297">Ako prihvatite predložene resurse, oni se fiksno rezervišu za projekat kao članovi tima i zamenjuju generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="44466-298">Morate ili prihvatiti ili odbaciti sve predložene resurse.</span><span class="sxs-lookup"><span data-stu-id="44466-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="44466-299">Ne možete ih delimično prihvatiti ni odbaciti.</span><span class="sxs-lookup"><span data-stu-id="44466-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="44466-300">Zamena resursa u projektnom timu</span><span class="sxs-lookup"><span data-stu-id="44466-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="44466-301">Ponekad menadžer projekta mora zameniti rezervisanog člana tima za projekat.</span><span class="sxs-lookup"><span data-stu-id="44466-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="44466-302">Na stranici **Projekti** na kartici **Tim** odaberite resurs kome je potrebna zamena, a zatim izaberite **Održavanje rezervacija**.</span><span class="sxs-lookup"><span data-stu-id="44466-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="44466-303">Proširite resurs za pregled projekata kojima je dodeljen.</span><span class="sxs-lookup"><span data-stu-id="44466-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Resurs je proširen radi prikaza dodeljenih projekata](media/Resource-Management-image50.png)

3. <span data-ttu-id="44466-305">Kliknite desnim tasterom miša na projekat, a zatim izaberite **Zamena resursa**.</span><span class="sxs-lookup"><span data-stu-id="44466-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="44466-306">Ako znate resurs koji želite zameniti trenutnim resursom, odaberite ili unesite ime, a zatim izaberite **Ponovo dodeli**.</span><span class="sxs-lookup"><span data-stu-id="44466-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Određivanje zamenskog resursa](media/Resource-Management-image51.png)

    <span data-ttu-id="44466-308">Alternativno, sledite ove korake da biste potražili resurs:</span><span class="sxs-lookup"><span data-stu-id="44466-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="44466-309">Izaberite **Pronalaženje zamene**.</span><span class="sxs-lookup"><span data-stu-id="44466-309">Select **Find Substitution**.</span></span>

        ![Traženje zamenskog resursa](media/Resource-Management-image52.png)

        <span data-ttu-id="44466-311">Pomoćnik za zakazivanje prikazuje listu dostupnih zamena.</span><span class="sxs-lookup"><span data-stu-id="44466-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="44466-312">U pomoćniku za zakazivanje možete dodatno filtrirati dostupne resurse da biste pronašli odgovarajuću zamenu.</span><span class="sxs-lookup"><span data-stu-id="44466-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Lista dostupnih zamena](media/Resource-Management-image53.png)

    2. <span data-ttu-id="44466-314">Da biste zamenili resurs, odaberite resurs koji želite, a zatim izaberite **Zameni**.</span><span class="sxs-lookup"><span data-stu-id="44466-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Izabran je zamenski resurs](media/Resource-Management-image54.png)

    <span data-ttu-id="44466-316">Rezervacije i dodele zamenjuju se novim resursom.</span><span class="sxs-lookup"><span data-stu-id="44466-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervacije i dodele zamenjuju se novim resursom](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="44466-318">Usaglašavanje rezervacija i dodela članova tima</span><span class="sxs-lookup"><span data-stu-id="44466-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="44466-319">Za članove tima, rezervacije i dodele su labavo povezane.</span><span class="sxs-lookup"><span data-stu-id="44466-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="44466-320">Drugim rečima, resursi mogu imati dodele, ali ne i rezervacije ili mogu imati rezervacije, ali ne i dodele.</span><span class="sxs-lookup"><span data-stu-id="44466-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="44466-321">U idealnom slučaju, rezervacije i dodele treba da se usklade tako da resursi imaju potreban kapacitet da izvrše dodeljene zadatke.</span><span class="sxs-lookup"><span data-stu-id="44466-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="44466-322">Međutim, rezervacije se mogu zasnivati na dostupnosti, a vremenski raspored zadataka može se menjati tokom projekta.</span><span class="sxs-lookup"><span data-stu-id="44466-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="44466-323">Stoga, labava povezanost rezervacija i dodela pruža fleksibilnost.</span><span class="sxs-lookup"><span data-stu-id="44466-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="44466-324">PSA ima karticu **Usaglašenost** koja omogućava menadžerima projekata da usaglase rezervacije članova tima i njihove dodele za projektne timove.</span><span class="sxs-lookup"><span data-stu-id="44466-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Kartica Usaglašenost](media/Resource-Management-image56.png)

<span data-ttu-id="44466-326">Kartica **Usaglašenost** prikazuje rezervacije i dodele sve do nivoa dodele pojedinačnog zadatka za svakog člana tima.</span><span class="sxs-lookup"><span data-stu-id="44466-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="44466-327">Prikazuje sate u ćelijama koji predstavljaju vremenske periode, od meseci, pa sve do dana.</span><span class="sxs-lookup"><span data-stu-id="44466-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="44466-328">Kartica takođe prikazuje ukupni neto iznos projekta, zajedno sa kolonom za ukupnu vrednost.</span><span class="sxs-lookup"><span data-stu-id="44466-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="44466-329">Kartica za svaki resurs izračunava razliku između rezervacija člana tima i ukupnog broja dodeljenih zadataka člana tima.</span><span class="sxs-lookup"><span data-stu-id="44466-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="44466-330">U idealnom slučaju, ta razlika bi trebalo da bude 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="44466-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="44466-331">Drugim rečima, ne bi trebalo da postoji razlika između rezervacija i dodela.</span><span class="sxs-lookup"><span data-stu-id="44466-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="44466-332">Razlike su obojene i zasenčene kako bi se skrenula pažnja na dve pojave:</span><span class="sxs-lookup"><span data-stu-id="44466-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="44466-333">**Nedostatak rezervacija** - Nedostatak rezervacija nastaje kada resurs ima više dodela nego rezervacija.</span><span class="sxs-lookup"><span data-stu-id="44466-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="44466-334">Budući da ovaj kapacitet nije rezervisan, menadžer projekta može da koriguje tu pojavu proširivanjem rezervacija resursa kako bi pokrio deficit.</span><span class="sxs-lookup"><span data-stu-id="44466-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="44466-335">**Prekomerne rezervacije** – Prekomerna rezervacija nastaje kada je resurs rezervisan za projekat, ali nije dodeljen zadacima.</span><span class="sxs-lookup"><span data-stu-id="44466-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="44466-336">Ta pojava može biti prihvatljiva u slučajevima kada je resurs rezervisan za projekat pre dodele zadatka.</span><span class="sxs-lookup"><span data-stu-id="44466-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="44466-337">Međutim, u drugim slučajevima se ne planira dodeljivanje resursa zadacima.</span><span class="sxs-lookup"><span data-stu-id="44466-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="44466-338">U tim slučajevima, menadžer projekta treba da razmotriti otkazivanje rezervacija resursa, tako da se kapacitet može koristiti za drugi projekat.</span><span class="sxs-lookup"><span data-stu-id="44466-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="44466-339">U nekim slučajevima, kada pregledate vreme na višem nivou od nivoa dana (na primer, na mesečnom nivou), možda ćete videti ukupnu razliku koja je nula za neki resurs (drugim rečima, rezervacije = dodele).</span><span class="sxs-lookup"><span data-stu-id="44466-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="44466-340">Međutim, ako pregledate vreme na nivou nedelje, možda ćete videti da postoje dodele od nula sati i rezervacije od 40 sati u prvoj nedelji, ali dodele od 40 sati i rezervacije od nula sati u drugoj nedelji.</span><span class="sxs-lookup"><span data-stu-id="44466-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="44466-341">Sve u svemu, rezervacije i dodele se usklađuju, ali se razlikuju od jedne do druge nedelje.</span><span class="sxs-lookup"><span data-stu-id="44466-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="44466-342">Kada pregledate vreme na višim nivoima, ćelije na kartici **Usaglašenost** imaju indikator koji će vas obavestiti da postoje razlike na nižim nivoima.</span><span class="sxs-lookup"><span data-stu-id="44466-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="44466-343">Duplim klikom na ćeliju možete da je povećate kako biste videli razliku.</span><span class="sxs-lookup"><span data-stu-id="44466-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="44466-344">Zatim možete da kliknite desnim tasterom miša da biste je umanjili. Ako odaberete resurs, a zatim koristite kontrolu **Sledeća razlika** na traci sa alatkama mreže, možete preći na sledeću razliku između rezervacija i dodela za taj resurs.</span><span class="sxs-lookup"><span data-stu-id="44466-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="44466-345">Zatim možete da koristite kontrolu **Prethodna razlika** za povratak.</span><span class="sxs-lookup"><span data-stu-id="44466-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="44466-346">Takođe možete isključiti indikator razlike i ponašanje u navigaciji u delu **Podešavanja**.</span><span class="sxs-lookup"><span data-stu-id="44466-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Indikator razlike](media/Resource-Management-image57.png)

<span data-ttu-id="44466-348">Ako imate dodele zadataka za resurs, ali nema rezervacija, na stranici **Projekti** na kartici **Usaglašenost** izaberite nedostatak rezervacija, a zatim **Produži rezervaciju**.</span><span class="sxs-lookup"><span data-stu-id="44466-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="44466-349">Pojavljuje se dijalog **Produženje rezervacije** i prikazuje rezervaciju koja je potrebna da se reši problem sa nedostatkom resursa.</span><span class="sxs-lookup"><span data-stu-id="44466-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="44466-350">Takođe pokazuje postojeće rezervacije resursa za sve projekte ili druge entitete koji se mogu zakazivati.</span><span class="sxs-lookup"><span data-stu-id="44466-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="44466-351">Ako izaberete **U redu** da biste kreirali rezervaciju za resurs, bez obzira na dostupnost tog resursa, možete prouzrokovati prekomernu rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="44466-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dijalog Produženje rezervacije](media/Resource-Management-image58.png)

<span data-ttu-id="44466-353">Menadžer projekta ili menadžer resursa tada može da koristi tabelu rasporeda kako bi upravljao bilo kojom situacijom u kojoj je resurs prekomerno rezervisan u odnosu na njegov kapacitet.</span><span class="sxs-lookup"><span data-stu-id="44466-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]