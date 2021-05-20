---
title: Razmatranja nadogradnje strukturne analize posla
description: Ova tema pruža informacije o nadogradnji strukturne analize posla iz aplikacije Project Service Automation verzije 2.x u verziju 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951361"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="fabfb-103">Razmatranja nadogradnje strukturne analize posla</span><span class="sxs-lookup"><span data-stu-id="fabfb-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fabfb-104">Ova tema pruža informacije o nadogradnji strukturne analize posla iz aplikacije Project Service Automation verzije 2.x u verziju 3.x.</span><span class="sxs-lookup"><span data-stu-id="fabfb-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="fabfb-105">Ova tema definiše ispravno stanje projekta u aplikaciji Project Service Automation (PSA), potrebno za uspešnu nadogradnju.</span><span class="sxs-lookup"><span data-stu-id="fabfb-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="fabfb-106">Postoje i informacije o uobičajenim uslovima blokiranja koji će dovesti do neuspešne nadogradnje.</span><span class="sxs-lookup"><span data-stu-id="fabfb-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="fabfb-107">Više informacija o definisanju projektnih zadataka i njihovim funkcijama u okviru rasporeda projekta potražite u članku [Rasporedi projekata](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="fabfb-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="fabfb-108">Ključni entiteti</span><span class="sxs-lookup"><span data-stu-id="fabfb-108">Key entities</span></span>
<span data-ttu-id="fabfb-109">Za ispravnu strukturnu analizu posla koja je već učitana sa resursima, potrebni su sledeći entiteti:</span><span class="sxs-lookup"><span data-stu-id="fabfb-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="fabfb-110">Projekat</span><span class="sxs-lookup"><span data-stu-id="fabfb-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="fabfb-111">Projektni tim</span><span class="sxs-lookup"><span data-stu-id="fabfb-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="fabfb-112">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="fabfb-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="fabfb-113">Dodele resursa</span><span class="sxs-lookup"><span data-stu-id="fabfb-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="fabfb-114">Zavisnost projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="fabfb-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="fabfb-115">Resursi koji mogu da se rezervišu</span><span class="sxs-lookup"><span data-stu-id="fabfb-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="fabfb-116">Da biste definisali strukturnu analizu posla koju je učitao resurs, morate da dovršite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="fabfb-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="fabfb-117">Kreirajte novi projekat.</span><span class="sxs-lookup"><span data-stu-id="fabfb-117">Create a new project.</span></span> <span data-ttu-id="fabfb-118">Za više informacija o tome kako da kreirate novi projekat, pogledajte [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="fabfb-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="fabfb-119">Kreirajte jedan ili više zadataka.</span><span class="sxs-lookup"><span data-stu-id="fabfb-119">Create one or more tasks.</span></span> <span data-ttu-id="fabfb-120">Za više informacija o tome kako da kreirate novi zadatak, pogledajte [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="fabfb-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="fabfb-121">Definišite zavisne elemente zadatka.</span><span class="sxs-lookup"><span data-stu-id="fabfb-121">Define the task dependencies.</span></span> <span data-ttu-id="fabfb-122">Za još informacija pogledajte [Zavisnost projektnog zadatka](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="fabfb-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="fabfb-123">Dodelite članove projektnog tima projektu.</span><span class="sxs-lookup"><span data-stu-id="fabfb-123">Assign project team members to the project.</span></span> <span data-ttu-id="fabfb-124">Za više informacija, pogledajte [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="fabfb-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="fabfb-125">Dodelite članove projektnog tima zadacima.</span><span class="sxs-lookup"><span data-stu-id="fabfb-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="fabfb-126">Za više informacija, pogledajte [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="fabfb-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="fabfb-127">Odnosi unutar projektnog tima</span><span class="sxs-lookup"><span data-stu-id="fabfb-127">Project team relationships</span></span>

<span data-ttu-id="fabfb-128">Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="fabfb-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="fabfb-129">Svi članovi projektnog tima moraju biti povezani sa resursom koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="fabfb-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="fabfb-130">Svi članovi projektnog tima moraju biti povezani sa istim projektom.</span><span class="sxs-lookup"><span data-stu-id="fabfb-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="fabfb-131">Odnosi u okviru projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="fabfb-131">Project task relationships</span></span>
<span data-ttu-id="fabfb-132">Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="fabfb-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="fabfb-133">Svi povezani zadaci moraju biti povezani sa istim projektom.</span><span class="sxs-lookup"><span data-stu-id="fabfb-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="fabfb-134">Svaki zadatak stavke mora imati nadređeni zadatak.</span><span class="sxs-lookup"><span data-stu-id="fabfb-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="fabfb-135">Svaki zadatak mora imati nadređeni projekat.</span><span class="sxs-lookup"><span data-stu-id="fabfb-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="fabfb-136">Važeći uslovi</span><span class="sxs-lookup"><span data-stu-id="fabfb-136">Valid conditions</span></span>

- <span data-ttu-id="fabfb-137">Trajanje svakog zadatka mora biti duže od sat vremena ili jednako tom vremenu (>=) i kraće od 1.800.000 minuta (1250 dana).\*</span><span class="sxs-lookup"><span data-stu-id="fabfb-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="fabfb-138">Svi zadaci moraju imati datum početka koji nije pre 1.1.2000.\*</span><span class="sxs-lookup"><span data-stu-id="fabfb-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="fabfb-139">Svi zadaci moraju imati datum početka koji je najdalje 17 godina od današnjeg dana.\*</span><span class="sxs-lookup"><span data-stu-id="fabfb-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="fabfb-140">Svi zadaci moraju da imaju datum početka koji je pre datuma završetka ili isti kao taj datum.</span><span class="sxs-lookup"><span data-stu-id="fabfb-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="fabfb-141">Sve vrste transakcija za klasifikacije (Troškovi, Materijal, Porez i Vreme) moraju imati vrednosti za stavke **Podrazumevana jedinica** i **Grupa jedinica**.</span><span class="sxs-lookup"><span data-stu-id="fabfb-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="fabfb-142">Formate datuma sa slovima treba izbegavati.</span><span class="sxs-lookup"><span data-stu-id="fabfb-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="fabfb-143">Potencijalni koraci za ublažavanje</span><span class="sxs-lookup"><span data-stu-id="fabfb-143">Potential mitigation steps</span></span>
- <span data-ttu-id="fabfb-144">Koristite naprednu pretragu za identifikaciju projektnih zadataka koji ne sadrže ID projekta.</span><span class="sxs-lookup"><span data-stu-id="fabfb-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="fabfb-145">Koristite naprednu pretragu da biste identifikovali projektne zadatke gde je zakazano trajanje duže od > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="fabfb-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="fabfb-146">Pre nego što unesete bilo kakve promene podataka, trebalo bi da istražite sva prilagođavanja povezana sa entitetom koja su mogla dovesti do toga da se podaci dovedu u loš status.</span><span class="sxs-lookup"><span data-stu-id="fabfb-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="fabfb-147">Trebalo bi da se pozabavite sa ovim prilagođavanjima pre nego što nastavite sa bilo kakvim ispravkama koje se odnose na podatke.</span><span class="sxs-lookup"><span data-stu-id="fabfb-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="fabfb-148">Za identifikovane zadatke koji su nasleđeni, razmotrite brisanje ovih zadataka ako vam nisu potrebni ili ako bi trebalo biti povezani sa ispravnih nadređenim projektom.</span><span class="sxs-lookup"><span data-stu-id="fabfb-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="fabfb-149">Za sve zadatke u kojima je trajanje duže od 1250 dana, razmotrite dodavanje više zadataka kako biste predstavljali ukupno trajanje, ako je dostupno.</span><span class="sxs-lookup"><span data-stu-id="fabfb-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="fabfb-150">Stavke zabeležene zvezdicom (\*) imaju ograničenja zbog činjenice da upravljanje odnosima sa klijentima (CRM) podržava samo 7320 proširenja ponavljanja.</span><span class="sxs-lookup"><span data-stu-id="fabfb-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="fabfb-151">Ne smete da prekoračite ovo ograničenje.</span><span class="sxs-lookup"><span data-stu-id="fabfb-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="fabfb-152">Odnosi između dodela resursa</span><span class="sxs-lookup"><span data-stu-id="fabfb-152">Resource Assignment relationships</span></span>
<span data-ttu-id="fabfb-153">Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="fabfb-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="fabfb-154">Sve dodele resursa u strukturnoj analizi posla moraju biti povezane sa istim projektom.</span><span class="sxs-lookup"><span data-stu-id="fabfb-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="fabfb-155">Sve dodele resursa u strukturnoj analizi posla moraju biti povezane sa članovima projektnog tima u istom projektu.</span><span class="sxs-lookup"><span data-stu-id="fabfb-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="fabfb-156">Potencijalni koraci za ublažavanje</span><span class="sxs-lookup"><span data-stu-id="fabfb-156">Potential mitigation steps</span></span>
- <span data-ttu-id="fabfb-157">Identifikujte sve zadatke koji spadaju van goreopisanih uslova.</span><span class="sxs-lookup"><span data-stu-id="fabfb-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="fabfb-158">Sve dodele resursa koje više nisu važeće bi trebalo biti obrisane.</span><span class="sxs-lookup"><span data-stu-id="fabfb-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="fabfb-159">Odnosi između zavisnih elemenata projektnog zadatka</span><span class="sxs-lookup"><span data-stu-id="fabfb-159">Project task dependency relationships</span></span>
<span data-ttu-id="fabfb-160">Da biste osigurali uspešnu nadogradnju, sledeći odnosi moraju se pravilno održavati:</span><span class="sxs-lookup"><span data-stu-id="fabfb-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="fabfb-161">Svi zavisni elementi zadatka projekta moraju biti povezani sa istim projektom.</span><span class="sxs-lookup"><span data-stu-id="fabfb-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="fabfb-162">Zadatak ne može da ima isti zavisni element na koji se upućuje više puta.</span><span class="sxs-lookup"><span data-stu-id="fabfb-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]