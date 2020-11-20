---
title: Zakažite projekat sa strukturnom analizom posla
description: Kako da planirate projekat sa strukturnom analizom posla u aplikaciji Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 04f30f2f2ed93dd1525f1c86a7521cdbf39a77bc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127895"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="98fe0-103">Planirajte projekat sa strukturnom analizom posla (Project Service)</span><span class="sxs-lookup"><span data-stu-id="98fe0-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="98fe0-104">Raspored projekta navodi koji posao treba da se obavi, koji resursi će izvršiti posao i vremenski okvir u kom posao treba da se dovrši.</span><span class="sxs-lookup"><span data-stu-id="98fe0-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="98fe0-105">Raspored projekta odražava sav posao povezan sa završavanjem projekta na vreme.</span><span class="sxs-lookup"><span data-stu-id="98fe0-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="98fe0-106">Jedan od prvih koraka u početnoj fazi projekta je da se napravi raspored projekta.</span><span class="sxs-lookup"><span data-stu-id="98fe0-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="98fe0-107">Da biste uspostavili raspored projekta, potrebno je da kreirate strukturnu analizu posla.</span><span class="sxs-lookup"><span data-stu-id="98fe0-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="98fe0-108">Kreiranje projektne strukture sa strukturnom analizom posla koja vam pomaže da:</span><span class="sxs-lookup"><span data-stu-id="98fe0-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="98fe0-109">Podelite posao u zadatke kojima je lako upravljati</span><span class="sxs-lookup"><span data-stu-id="98fe0-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="98fe0-110">Procenite vreme potrebno za dovršenje zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="98fe0-111">Podesite zavisnosti i trajanje zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="98fe0-112">Odredite uloge koje su potrebne za dovršavanje svakog zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="98fe0-113">Raspored projekta strukturnoj analizi posla ima poznati izgled i osećaj, dovršite sa interaktivnim gantogramom.</span><span class="sxs-lookup"><span data-stu-id="98fe0-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="98fe0-114">Kreiranje strukturne analize posla za projekat</span><span class="sxs-lookup"><span data-stu-id="98fe0-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="98fe0-115">Kreiranje strukturne analize posla za predstavljanje redosled zadataka u projektu</span><span class="sxs-lookup"><span data-stu-id="98fe0-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="98fe0-116">Strukturna analiza posla uključuje zadatke, zahteve za svaki zadatak i informacije o prihodima i troškovima.</span><span class="sxs-lookup"><span data-stu-id="98fe0-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="98fe0-117">U strukturnu analizu posla možete dodati:</span><span class="sxs-lookup"><span data-stu-id="98fe0-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="98fe0-118">Redosled zadataka u hijerarhiji</span><span class="sxs-lookup"><span data-stu-id="98fe0-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="98fe0-119">Druge zadatke, ako ih ima, koji moraju biti dovršeni pre nego što možete pokrenuti zadatak</span><span class="sxs-lookup"><span data-stu-id="98fe0-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="98fe0-120">Početni datum, datum prestanka i trajanje zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="98fe0-121">Broj časova potrebnih za zadatak</span><span class="sxs-lookup"><span data-stu-id="98fe0-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="98fe0-122">Sve potrebne veštine i obrazovanje za radnike</span><span class="sxs-lookup"><span data-stu-id="98fe0-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="98fe0-123">Zaposleni koji su postavljeni na zadatak</span><span class="sxs-lookup"><span data-stu-id="98fe0-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="98fe0-124">Procenjeni prihod i troškovi</span><span class="sxs-lookup"><span data-stu-id="98fe0-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="98fe0-125">Tipovi zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-125">Task types</span></span>  
<span data-ttu-id="98fe0-126">Videćete sledeće vrste zadataka prilikom kreiranja strukturne analize posla:</span><span class="sxs-lookup"><span data-stu-id="98fe0-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="98fe0-127">**Osnovni čvor projekta**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-127">**Project root node**</span></span> | <span data-ttu-id="98fe0-128">Sažetak najvišeg nivoa za zadatak projekta.</span><span class="sxs-lookup"><span data-stu-id="98fe0-128">The top-level summary task for the project.</span></span> <span data-ttu-id="98fe0-129">Svi drugi projektni zadaci se kreiraju u okviru njega.</span><span class="sxs-lookup"><span data-stu-id="98fe0-129">All other project tasks are created under it.</span></span> <span data-ttu-id="98fe0-130">Ime osnovnog zadatka je ime projekta.</span><span class="sxs-lookup"><span data-stu-id="98fe0-130">The name of the root task is the project name.</span></span> <span data-ttu-id="98fe0-131">Trud, datumi i trajanje korenskog čvora se zasnivaju na vrednostima hijerarhije ispod njega.</span><span class="sxs-lookup"><span data-stu-id="98fe0-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="98fe0-132">Nije moguće urediti svojstva korenskog čvora ili izbrišite korenski čvor.</span><span class="sxs-lookup"><span data-stu-id="98fe0-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="98fe0-133">**Rezime ili zadaci spremišta**</span><span class="sxs-lookup"><span data-stu-id="98fe0-133">**Summary or container tasks**</span></span> | <span data-ttu-id="98fe0-134">Zadatak sažetka je zadatak koji ima podzadatke.</span><span class="sxs-lookup"><span data-stu-id="98fe0-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="98fe0-135">Zadatak sažetka nema samostalni trud ili trošak.</span><span class="sxs-lookup"><span data-stu-id="98fe0-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="98fe0-136">Njegov trud i trošak su zbirne vrednosti njegovih podzadataka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="98fe0-137">Možete promeniti ime zadatka sažetka ali ne možete promeniti trud, datume ili vreme trajanja, zato što se oni automatski izračunavaju.</span><span class="sxs-lookup"><span data-stu-id="98fe0-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="98fe0-138">Brisanjem zadatka sažetka briše zadatak i sve njegove podzadatke.</span><span class="sxs-lookup"><span data-stu-id="98fe0-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="98fe0-139">**Zadaci čvora lista**</span><span class="sxs-lookup"><span data-stu-id="98fe0-139">**Leaf node tasks**</span></span> | <span data-ttu-id="98fe0-140">Zadatak čvor lista predstavlja najdetaljniji posao na projektu.</span><span class="sxs-lookup"><span data-stu-id="98fe0-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="98fe0-141">Sadrži procenjeni trud, planirani broj resursa, planirane datume početka i završetka i trajanje.</span><span class="sxs-lookup"><span data-stu-id="98fe0-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="98fe0-142">Hijerarhija zadataka</span><span class="sxs-lookup"><span data-stu-id="98fe0-142">Task hierarchy</span></span>  
 <span data-ttu-id="98fe0-143">Imate sledeće opcije prilikom kreiranja hijerarhije zadataka:</span><span class="sxs-lookup"><span data-stu-id="98fe0-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="98fe0-144">**Dodaj zadatak**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-144">**Add task**.</span></span>   <span data-ttu-id="98fe0-145">Možete da dodate zadatak u položaj koji odaberete u hijerarhiji zadataka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="98fe0-146">Ako ne odaberete položaj, novi zadatak se pojavljuje na kraju.</span><span class="sxs-lookup"><span data-stu-id="98fe0-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="98fe0-147">**Uvlačenje zadatka**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-147">**Indent task**.</span></span>   <span data-ttu-id="98fe0-148">Uvlačenjem zadatka ga činite podređenim zadatku direktno iznad njega.</span><span class="sxs-lookup"><span data-stu-id="98fe0-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="98fe0-149">**Izvlačenje zadatka**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-149">**Outdent task**.</span></span>   <span data-ttu-id="98fe0-150">Izvucite zadatak da biste ga učinili tako da nije više podzadatak njegovog prvobitno nadređenog zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="98fe0-151">**Premesti nagore i Premesti nadole**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-151">**Move up and Move down**.</span></span>   <span data-ttu-id="98fe0-152">Pomeranje zadataka nagore i nadole u hijerarhiji njegovog nadređenog zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="98fe0-153">Premeštanje zadatka nagore ili nadole nema uticaja na njegov trud, trošak, datume ili trajanje.</span><span class="sxs-lookup"><span data-stu-id="98fe0-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="98fe0-154">Atributi zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-154">Task attributes</span></span>  
 <span data-ttu-id="98fe0-155">Ime zadatka opisuje posao koji treba da se dovrši.</span><span class="sxs-lookup"><span data-stu-id="98fe0-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="98fe0-156">Koristite različite atribute zadatka da biste opisali raspored i zahteve zaposlenih na zadatku.</span><span class="sxs-lookup"><span data-stu-id="98fe0-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="98fe0-157">Zakazivanje atributa</span><span class="sxs-lookup"><span data-stu-id="98fe0-157">Schedule attributes</span></span>

 - <span data-ttu-id="98fe0-158">Vrednosti koje dodelite za **Časove truda**, **Broj resursa**, **Datum Početka**, **Datum Završetka**, i **Trajanje** za određivanje rasporeda zadataka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="98fe0-159">**Trud** je procena časova potrebnih za dovršavanje zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="98fe0-160">**Broj resursa** je procena koja menadžera projekta stavlja u zadatak kako bi se pronašao najbolji mogući raspored.</span><span class="sxs-lookup"><span data-stu-id="98fe0-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="98fe0-161">**Trajanje** (u danima) označava broj radnih dana koji će biti potrebni za dovršavanje zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="98fe0-162">Atributi zaposlenih</span><span class="sxs-lookup"><span data-stu-id="98fe0-162">Staffing attributes</span></span>

 - <span data-ttu-id="98fe0-163">**Uloga**, **Resursa organizacione jedinice**, **Broj resursa**, i **Resursa** za opisivanje zahteva zaposlenima za zadatak.</span><span class="sxs-lookup"><span data-stu-id="98fe0-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="98fe0-164">**Uloga** opisuje vrstu resursa potrebnog za obavljanje zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="98fe0-165">**Resurs organizacione jedinice** označava organizacionu jedinicu iz koje su ljudski resursi za taj zadatak; ovo takođe utiče na troškove i procenu prodaje zadatka, pošto se ovo računa za određivanje cene prodaje po jedinici za resurse.</span><span class="sxs-lookup"><span data-stu-id="98fe0-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="98fe0-166">**Resursi** sadrže generičke resurse ili nazvane resurse kada je jedan pronađen.</span><span class="sxs-lookup"><span data-stu-id="98fe0-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="98fe0-167">Zavisnosti zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-167">Task dependencies</span></span>  
 <span data-ttu-id="98fe0-168">Možete da kreirate prethodne odnose između jednog ili više zadataka u strukturnoj analizi posla.</span><span class="sxs-lookup"><span data-stu-id="98fe0-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="98fe0-169">Možete postaviti jednu ili više vrednosti za polje prethodnik na zadacima da biste ukazali na zadatke od kojih će zavisiti.</span><span class="sxs-lookup"><span data-stu-id="98fe0-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="98fe0-170">Kada dodelite prethodnu vrednost zadatku, zadatak možete da pokrenete jedino kada dovršite sve prethodne zadatke.</span><span class="sxs-lookup"><span data-stu-id="98fe0-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="98fe0-171">Podešavanje ove zavisnosti zadatka dovešće do ponovnog preračunavanja datuma planirane početka zadatka kao najnoviji kraj svih njegovih prethodnika.</span><span class="sxs-lookup"><span data-stu-id="98fe0-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="98fe0-172">Povezani uticaj prethodnika na raspored nije ograničen režimom zadatka definisanog u zadatku.</span><span class="sxs-lookup"><span data-stu-id="98fe0-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="98fe0-173">Režim zadatka</span><span class="sxs-lookup"><span data-stu-id="98fe0-173">Task mode</span></span>  
 <span data-ttu-id="98fe0-174">Režim zadatka je jedna od važnih činilaca koji određuju zakazivanje zadataka čvora lista.</span><span class="sxs-lookup"><span data-stu-id="98fe0-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="98fe0-175">Postoje dva režima zadataka za svaki zadatak: režim automatskog zakazivanja i režim ručnog zakazivanja.</span><span class="sxs-lookup"><span data-stu-id="98fe0-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="98fe0-176">**Automatsko zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-176">**Auto scheduling**.</span></span>   <span data-ttu-id="98fe0-177">Kada podesite režim zadatka na Automatsko zakazivanje, mehanizam za zakazivanje zadataka koristi pravila o praćenju atributa zadataka radi utvrđivanja rasporeda za zadatak:</span><span class="sxs-lookup"><span data-stu-id="98fe0-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="98fe0-178">Prethodni zadaci</span><span class="sxs-lookup"><span data-stu-id="98fe0-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="98fe0-179">Angažovanje</span><span class="sxs-lookup"><span data-stu-id="98fe0-179">Effort</span></span>  
  
    -   <span data-ttu-id="98fe0-180">Broj resursa</span><span class="sxs-lookup"><span data-stu-id="98fe0-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="98fe0-181">Datume početka i završetka</span><span class="sxs-lookup"><span data-stu-id="98fe0-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="98fe0-182">**Pravila planiranja**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-182">**Scheduling rules**.</span></span>   <span data-ttu-id="98fe0-183">Datum početka zadatka čvora lista koji nema prethodnih zadataka podrazumevano je zakazan za početak projekta.</span><span class="sxs-lookup"><span data-stu-id="98fe0-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="98fe0-184">Trajanje zadatka čvora lista se uvek izračunava kao broj radnih dana između njegovog početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="98fe0-185">Kada se zadatak automatski zakazuje, mehanizam za planiranje prati pravila ispod:</span><span class="sxs-lookup"><span data-stu-id="98fe0-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="98fe0-186">Datumi početka i završetka zadatka uvek moraju biti radni dani u skladu sa kalendarom za planiranje projekta</span><span class="sxs-lookup"><span data-stu-id="98fe0-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="98fe0-187">Datum početka zadatka koji ima prethodne zadatke je podrazumevano poslednji datum završetka prethodnih zadataka</span><span class="sxs-lookup"><span data-stu-id="98fe0-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="98fe0-188">Trud = Broj osoba \* Trajanje \* časova u standardnom radnom danu kalendara projekta</span><span class="sxs-lookup"><span data-stu-id="98fe0-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="98fe0-189">**Ručno planiranje**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-189">**Manual scheduling**.</span></span>   <span data-ttu-id="98fe0-190">U nekim slučajevima, možda ćete želeti da odstupite od ovih pravila.</span><span class="sxs-lookup"><span data-stu-id="98fe0-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="98fe0-191">U ovim slučajevima, možete postaviti režim zadataka na ručno zakazivanje zadataka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="98fe0-192">Zaustavlja mehanizam za planiranje iz izračunavanja vrednosti za druge atribute zakazivanja.</span><span class="sxs-lookup"><span data-stu-id="98fe0-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="98fe0-193">Podešavanje prethodnih zadataka na zadatke uvek utiče na datum početka zavisnog zadatka.</span><span class="sxs-lookup"><span data-stu-id="98fe0-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="98fe0-194">Kreiranje strukturne analize posla</span><span class="sxs-lookup"><span data-stu-id="98fe0-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="98fe0-195">Idite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="98fe0-196">Kliknite na projekat na kome želite da radite.</span><span class="sxs-lookup"><span data-stu-id="98fe0-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="98fe0-197">Na traci u vrhu ekrana izaberite strelicu nadole pored naziva projekta, a zatim kliknite na Strukturnu analizu posla.</span><span class="sxs-lookup"><span data-stu-id="98fe0-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="98fe0-198">Da biste dodali zadatak, kliknite na dugme **Dodaj Zadatak**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="98fe0-199">Popunite polja za zadatak, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="98fe0-200">Nastavite dodavanje zadataka dok se ne završi strukturna analiza posla.</span><span class="sxs-lookup"><span data-stu-id="98fe0-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="98fe0-201">Prilikom kreiranja strukturne analize posla, možete uraditi sledeće da biste organizovali svoje zadatke:</span><span class="sxs-lookup"><span data-stu-id="98fe0-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="98fe0-202">Izaberite zadatak i kliknite na dugme **Uvuci** da biste ga premestili u drugi zadatak ili Izvuci da biste premestili izvan nivoa.</span><span class="sxs-lookup"><span data-stu-id="98fe0-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="98fe0-203">Izaberite zadatak i kliknite na dugme **Premesti nagore** ili **Premesti nadole** da biste ga premestili nagore ili nadole na listi.</span><span class="sxs-lookup"><span data-stu-id="98fe0-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="98fe0-204">Kliknite na dugme **Sakrij gantogram** da biste sakrili gantogram i kliknite na dugme **Prikaži gantogram** da biste ga ponovo prikazali.</span><span class="sxs-lookup"><span data-stu-id="98fe0-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="98fe0-205">Izaberite drugi period vremena za gantogram u opciji **Vremenska skala**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="98fe0-206">Da biste dodali uloge koje ste naveli u vašu strukturnu analizu posla za članove tima vašeg projekta, kliknite na dugme **Generisanje tima za projekat**.</span><span class="sxs-lookup"><span data-stu-id="98fe0-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="98fe0-207">Kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana kada završite sa unošenjem izmena.</span><span class="sxs-lookup"><span data-stu-id="98fe0-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="98fe0-208">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="98fe0-208">See Also</span></span>  
 [<span data-ttu-id="98fe0-209">Vodič za menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="98fe0-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
