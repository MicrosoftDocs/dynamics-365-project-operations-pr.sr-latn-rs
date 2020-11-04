---
title: Procena prodaje i troškova projekta kada resurs koji može da se rezerviše ispunjava više uloga u projektu
description: U ovoj temi se pružaju informacije o tome kako se dimenzije cene mogu koristiti za podršku određivanju cena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083632"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="4e521-103">Procena prodaje i troškova projekta kada resurs koji može da se rezerviše ispunjava više uloga u projektu</span><span class="sxs-lookup"><span data-stu-id="4e521-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="4e521-104">Kompanije zasnovane na projektu često imaju potrebu da jedan resurs obavlja više uloga na projektu.</span><span class="sxs-lookup"><span data-stu-id="4e521-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="4e521-105">Cene i troškovi za svaku od ovih uloga mogu se različito odrediti, što znači da vreme istog resursa na projektu može dobiti različitu finansijsku procenu u zavisnosti od naplate i stope troškova za svaku od uloga.</span><span class="sxs-lookup"><span data-stu-id="4e521-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="4e521-106">Project Service Automation omogućava podešavanje vrednosti u zapisu člana tima za imenovani resurs i omogućava različite zamene za svaki od zadataka kojima je dodeljen član tima.</span><span class="sxs-lookup"><span data-stu-id="4e521-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="4e521-107">Sledeći primer objašnjava kako jednostavna izmena ove vrednosti omogućava resursu da ima više uloga u projektu sa različitim troškovima i stopama naplate.</span><span class="sxs-lookup"><span data-stu-id="4e521-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="4e521-108">Kreiranje zadataka</span><span class="sxs-lookup"><span data-stu-id="4e521-108">Create tasks</span></span>
<span data-ttu-id="4e521-109">Napravite dva projektna zadatka po 40 sati, zadatak A i zadatak B. Izaberite zadatak A kao prethodnika zadatka B.</span><span class="sxs-lookup"><span data-stu-id="4e521-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="4e521-110">Podešavanje uloge i organizacione jedinice za generičkog člana projektnog tima</span><span class="sxs-lookup"><span data-stu-id="4e521-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="4e521-111">Na stranici **Raspored** izaberite red **Zadatak** za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="4e521-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="4e521-112">U polju **Resursi** izaberite **Kreiraj** u padajućoj listi.</span><span class="sxs-lookup"><span data-stu-id="4e521-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="4e521-113">Na stranici **Brzo kreiranje člana tima** , navedite atribute generičkog člana tima koji može da izvrši ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="4e521-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="4e521-114">Izaberite odgovarajuću ulogu i organizacionu jedinicu, a zatim izaberite **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="4e521-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="4e521-115">Generički član tima se kreira i dodeljuje ovom zadatku.</span><span class="sxs-lookup"><span data-stu-id="4e521-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="4e521-116">Ponovite ove korake za zadatak B i uverite se da se uloga i organizaciona jedinica generičkog člana tima kreiranog za zadatak B razlikuje od zadatka A.</span><span class="sxs-lookup"><span data-stu-id="4e521-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="4e521-117">Podešavanje uloge i organizacione jedinice za projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="4e521-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="4e521-118">Kada kreirate zadatak A, izaberite zadatak, a zatim izaberite **Uređuj zadatak**.</span><span class="sxs-lookup"><span data-stu-id="4e521-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="4e521-119">Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica** , dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="4e521-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="4e521-120">Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Vođa konsultanata** za ulogu i **Fabrikam US** kao organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="4e521-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="4e521-121">Izaberite zadatak B, a zatim izaberite **Uredi zadatak**.</span><span class="sxs-lookup"><span data-stu-id="4e521-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="4e521-122">Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica** , dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="4e521-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="4e521-123">Uverite se da se vrednosti u poljima **Uloga** i **Organizaciona jedinica** za zadatak B razlikuju od onih za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="4e521-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="4e521-124">Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Tehničar mreže** za ulogu i **Fabrikam US** kao organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="4e521-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="4e521-125">Sačuvajte i zatvorite stranicu **Detalji zadatka**.</span><span class="sxs-lookup"><span data-stu-id="4e521-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="4e521-126">Član tima i procena ponašanja</span><span class="sxs-lookup"><span data-stu-id="4e521-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="4e521-127">Na stranici **Detalji zadatka** , u odeljku **Član tima** , izaberite dva člana generičkog tima, a zatim izaberite **Generiši zahteve**.</span><span class="sxs-lookup"><span data-stu-id="4e521-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="4e521-128">Tako ćete generisati zahteve za resursima.</span><span class="sxs-lookup"><span data-stu-id="4e521-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="4e521-129">Izaberite red člana tima za **Vođa konsultanata** , a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="4e521-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="4e521-130">Tabela rasporeda se otvara i rezerviše resurs za taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="4e521-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="4e521-131">Izaberite red člana tima za **Tehničar mreže** , a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="4e521-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="4e521-132">Tabela rasporeda se otvara i rezerviše isti resurs za taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="4e521-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="4e521-133">Mreža člana tima</span><span class="sxs-lookup"><span data-stu-id="4e521-133">Team Member grid</span></span> 
<span data-ttu-id="4e521-134">Na mreži **Član tima** , uočite da su dva generička zapisa članova tima izbrisana i da su zamenjena jednim resursom.</span><span class="sxs-lookup"><span data-stu-id="4e521-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="4e521-135">Postoji jedan skup vrednosti za taj resurs koji prikazuje zadati skup vrednosti za **ulogu** i **organizacionu jedinicu**.</span><span class="sxs-lookup"><span data-stu-id="4e521-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="4e521-136">Kada proširite red tog zapisa člana tima, na zapisu člana tima možete videti različite zadatke za oba ta zadatka.</span><span class="sxs-lookup"><span data-stu-id="4e521-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="4e521-137">Svaki red zadatka ima vrednosti specifične za zadatak za **ulogu** i **organizacionu jedinicu**.</span><span class="sxs-lookup"><span data-stu-id="4e521-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="4e521-138">Mreža procena</span><span class="sxs-lookup"><span data-stu-id="4e521-138">Estimates grid</span></span> 
<span data-ttu-id="4e521-139">Kada odete na mrežu **Procene** , primetićete da obe dodele za isti resurs imaju različito određene cene.</span><span class="sxs-lookup"><span data-stu-id="4e521-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="4e521-140">Cena dodele resursa zadatku A određuje se korišćenjem vrednosti atributa **Uloga** za **vođu konsultanata**.</span><span class="sxs-lookup"><span data-stu-id="4e521-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="4e521-141">Cena dodele istog resursa zadatku B određuje se korišćenjem vrednosti atributa **Uloga** za **tehničara mreže**.</span><span class="sxs-lookup"><span data-stu-id="4e521-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





