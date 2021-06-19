---
title: Procena prodaje i troškova za projekat kada resurs koji može da se rezerviše ispunjava više uloga u projektu
description: Ova tema pruža informacije o tome kako dimenzije određivanja cena mogu da se koriste za podršku procenama cena i troškova za resurs koji ispunjava više uloga u projektu.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5b2b57f5268a92168952b6da5123886df70cd4e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013278"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="7bc2d-103">Procena prodaje i troškova za projekat kada resurs koji može da se rezerviše ispunjava više uloga u projektu</span><span class="sxs-lookup"><span data-stu-id="7bc2d-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7bc2d-104">Kompanije zasnovane na projektima često imaju potrebu da jedan resurs obavlja više uloga u projektu.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="7bc2d-105">Cene i troškovi za svaku od ovih uloga mogu se različito odrediti, što znači da vreme istog resursa na projektu može dobiti različitu finansijsku procenu u zavisnosti od naplate i stope troškova za svaku od uloga.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="7bc2d-106">Project Service Automation omogućava podešavanje vrednosti u zapisu člana tima za imenovani resurs i omogućava različite zamene za svaki od zadataka kojima je dodeljen član tima.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="7bc2d-107">Sledeći primer objašnjava kako jednostavna izmena ove vrednosti omogućava resursu da ima više uloga u projektu sa različitim troškovima i stopama naplate.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="7bc2d-108">Kreiranje zadataka</span><span class="sxs-lookup"><span data-stu-id="7bc2d-108">Create tasks</span></span>
<span data-ttu-id="7bc2d-109">Napravite dva projektna zadatka po 40 sati, zadatak A i zadatak B. Izaberite zadatak A kao prethodnika zadatka B.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="7bc2d-110">Podešavanje uloge i organizacione jedinice za generičkog člana projektnog tima</span><span class="sxs-lookup"><span data-stu-id="7bc2d-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="7bc2d-111">Na stranici **Raspored** izaberite red **Zadatak** za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="7bc2d-112">U polju **Resursi** izaberite **Kreiraj** u padajućoj listi.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="7bc2d-113">Na stranici **Brzo kreiranje člana tima**, navedite atribute generičkog člana tima koji može da izvrši ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="7bc2d-114">Izaberite odgovarajuću ulogu i organizacionu jedinicu, a zatim izaberite **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="7bc2d-115">Generički član tima se kreira i dodeljuje ovom zadatku.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="7bc2d-116">Ponovite ove korake za zadatak B i uverite se da se uloga i organizaciona jedinica generičkog člana tima kreiranog za zadatak B razlikuje od zadatka A.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="7bc2d-117">Podešavanje uloge i organizacione jedinice za projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="7bc2d-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="7bc2d-118">Kada kreirate zadatak A, izaberite zadatak, a zatim izaberite **Uređuj zadatak**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="7bc2d-119">Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica**, dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="7bc2d-120">Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Vođa konsultanata** za ulogu i **Fabrikam US** kao organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="7bc2d-121">Izaberite zadatak B, a zatim izaberite **Uredi zadatak**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="7bc2d-122">Na stranici **Detalji zadatka** pronađite polja **Uloga** i **Organizaciona jedinica**, dodajte vrednosti potrebne za resurs koji bi izvršio ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="7bc2d-123">Uverite se da se vrednosti u poljima **Uloga** i **Organizaciona jedinica** razlikuju za zadatak B od vrednosti za zadatak A.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="7bc2d-124">Ako dovršavate ove scenarije koristeći Project Service Automation demo podatke, izaberite **Tehničar mreže** za ulogu i **Fabrikam US** kao organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="7bc2d-125">Sačuvajte i zatvorite stranicu **Detalji zadatka**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="7bc2d-126">Član tima i ponašanje procena</span><span class="sxs-lookup"><span data-stu-id="7bc2d-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="7bc2d-127">Na stranici **Detalji zadatka**, u odeljku **Član tima**, izaberite dva člana generičkog tima, a zatim izaberite **Generiši zahteve**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="7bc2d-128">Izaberite red člana tima za **Vođa konsultanata**, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="7bc2d-129">Tabela rasporeda se otvara i rezerviše resurs za taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="7bc2d-130">Izaberite red člana tima za **Tehničar mreže**, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="7bc2d-131">Tabela rasporeda se otvara i rezerviše isti resurs za taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="7bc2d-132">Mreža člana tima</span><span class="sxs-lookup"><span data-stu-id="7bc2d-132">Team Member grid</span></span> 
<span data-ttu-id="7bc2d-133">Na mreži **Član tima**, uočite da su dva generička zapisa članova tima izbrisana i da su zamenjena jednim resursom.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="7bc2d-134">Postoji jedan skup vrednosti za taj resurs koji prikazuje zadati skup vrednosti za **ulogu** i **organizacionu jedinicu**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="7bc2d-135">Kada proširite red tog zapisa člana tima, na zapisu člana tima možete videti različite zadatke za oba ta zadatka.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="7bc2d-136">Svaki red zadatka ima vrednosti specifične za zadatak za **ulogu** i **organizacionu jedinicu**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="7bc2d-137">Mreža procena</span><span class="sxs-lookup"><span data-stu-id="7bc2d-137">Estimates grid</span></span> 
<span data-ttu-id="7bc2d-138">Kada odete na mrežu **Procene**, primetićete da obe dodele za isti resurs imaju različito određene cene.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="7bc2d-139">Cena dodele resursa zadatku A određuje se korišćenjem vrednosti atributa **Uloga** za **vođu konsultanata**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="7bc2d-140">Cena dodele istog resursa zadatku B određuje se korišćenjem vrednosti atributa **Uloga** za **tehničara mreže**.</span><span class="sxs-lookup"><span data-stu-id="7bc2d-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]