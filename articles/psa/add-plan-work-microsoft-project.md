---
title: Koristite programski dodatak Project Service za planiranje vašeg rada u programu Microsoft Project | MicrosoftDocs
description: Ova tema pruža informacije o dodavanju, konfigurisanju i korišćenju programskog dodatka Microsoft Project u programu Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083710"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="e58ba-103">Koristite programski dodatak Project Service Automation za planiranje vašeg rada u programu Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="e58ba-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="e58ba-104">vam olakšava da obavljate planiranje projekata, uključujući procene.</span><span class="sxs-lookup"><span data-stu-id="e58ba-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="e58ba-105">Možete da definišete rad tako da troškovi, angažovanje i prodajna vrednost budu jasni kada konačan predlog bude prosleđen.</span><span class="sxs-lookup"><span data-stu-id="e58ba-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="e58ba-106">Sada možete da instalirate sistem [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i da poslove planiranja obavljate u poznatom okruženja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="e58ba-107">Koristite robusne mogućnosti planiranja i upravljanja programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], a zatim ažurirajte plan projekta u programu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e58ba-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="e58ba-108">Da biste koristili SharePoint upravljanje dokumentima za skladištenje u vašim [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datotekama za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekte, vaš [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] administrator će morati da uključi upravljanje dokumentima.</span><span class="sxs-lookup"><span data-stu-id="e58ba-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="e58ba-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilan samo sa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional izdanjem.</span><span class="sxs-lookup"><span data-stu-id="e58ba-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="e58ba-110">Preuzmite i instalirajte programski dodatak</span><span class="sxs-lookup"><span data-stu-id="e58ba-110">Download and install the add-in</span></span>  
 <span data-ttu-id="e58ba-111">Pripremite vaše informacije za prijavljivanje u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="e58ba-112">Te informacije će vam biti potrebne da biste se povezali sa programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] na funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="e58ba-113">Iz centra za preuzimanje preuzmite programski dodatak za podržanu verziju usluge of Project Service, verzije [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) ili [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="e58ba-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="e58ba-114">Kliknite na vezu za preuzimanje.</span><span class="sxs-lookup"><span data-stu-id="e58ba-114">Click the download link.</span></span>  

3.  <span data-ttu-id="e58ba-115">Nakon preuzimanja, kliknite na **Da** da biste instalirali programski dodatak.</span><span class="sxs-lookup"><span data-stu-id="e58ba-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="e58ba-116">Konfigurišite programski dodatak</span><span class="sxs-lookup"><span data-stu-id="e58ba-116">Configure the add-in</span></span>  

1. <span data-ttu-id="e58ba-117">Otvorite [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i kliknite na karticu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="e58ba-118">Kliknite na dugme **Poveži**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="e58ba-119">Unesite svoje informacije za prijavljivanje i kliknite na dugme **Prijavi se**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="e58ba-120">Sada možete početi sa korišćenjem programskog dodatka.</span><span class="sxs-lookup"><span data-stu-id="e58ba-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="e58ba-121">Čitanje iz predloška</span><span class="sxs-lookup"><span data-stu-id="e58ba-121">Read from a template</span></span>  
 <span data-ttu-id="e58ba-122">Čitajte iz predloška koji ste kreirali u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i kopirali u program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] da biste započeli planiranje projekta.</span><span class="sxs-lookup"><span data-stu-id="e58ba-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e58ba-123">[Kreiranje predloška za projekat (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="e58ba-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="e58ba-124">Sa kartice **Project Service** kliknite na dugme **Čitanje** > **Predložak Project Service Automation projekta**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="e58ba-125">Sa liste izaberite predložak projekta i kliknite na dugme **Otvori**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="e58ba-126">Podrazumevano, zadaci koji su kopirani iz predloška u projekat su podešeni kao ručno zakazani.</span><span class="sxs-lookup"><span data-stu-id="e58ba-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="e58ba-127">Dodeljivanje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] uloga resursima projekta</span><span class="sxs-lookup"><span data-stu-id="e58ba-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="e58ba-128">Otvorite projekat i kliknite na traku **Zadatak**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="e58ba-129">Kliknite na meni **Gantogram** , a zatim izaberite **Lista resursa**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="e58ba-130">Na listu resursa kliknite na dugme u padajućem meniju **Uloga resursa za Project Service** i odaberite ulogu za Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e58ba-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="e58ba-131">Obezbedite radnu snagu za projekat pomoću resursa</span><span class="sxs-lookup"><span data-stu-id="e58ba-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="e58ba-132">Na kartici „Project Service“ izaberite red i kliknite na dugme **Pronađi resurse**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="e58ba-133">Na ekranu **Rezervacija resursa** izaberite resurs koji želite da koristite za projekat.</span><span class="sxs-lookup"><span data-stu-id="e58ba-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="e58ba-134">Kliknite na dugme **Rezerviši** , a zatim na **U redu**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="e58ba-135">Objavite vaš projekat</span><span class="sxs-lookup"><span data-stu-id="e58ba-135">Publish your project</span></span>  
<span data-ttu-id="e58ba-136">Kada se planiranje projekta završi, sledeći korak je uvoz i objavljivanje projekta u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="e58ba-137">Projekat će se uvesti u funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="e58ba-138">Primenjuju se procesi određivanja cena i generisanja tima.</span><span class="sxs-lookup"><span data-stu-id="e58ba-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="e58ba-139">Otvorite projekat u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da biste videli da li su tim, procene za projekat i strukturna analiza posla generisani.</span><span class="sxs-lookup"><span data-stu-id="e58ba-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="e58ba-140">U sledećoj tabeli je prikazano gde da pronađete rezultate:</span><span class="sxs-lookup"><span data-stu-id="e58ba-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e58ba-141">**Gantogram**</span><span class="sxs-lookup"><span data-stu-id="e58ba-141">**Gantt Chart**</span></span>   | <span data-ttu-id="e58ba-142">Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Strukturna analiza posla**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e58ba-143">**Lista resursa**</span><span class="sxs-lookup"><span data-stu-id="e58ba-143">**Resource Sheet**</span></span> |   <span data-ttu-id="e58ba-144">Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Članovi projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="e58ba-145">**Koristite upotrebu**</span><span class="sxs-lookup"><span data-stu-id="e58ba-145">**Use Usage**</span></span>    |    <span data-ttu-id="e58ba-146">Uvozi u [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ekran **Procene projekta**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="e58ba-147">**Da biste uvozili i objavljivali projekte**</span><span class="sxs-lookup"><span data-stu-id="e58ba-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="e58ba-148">Sa kartice **Project Service** kliknite na **Objavi** > **Novi Project Service Automation projekat**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="e58ba-149">U dijalogu **Objavi u novi projekat u programu Project Service** unesite **Ime projekta** i izaberite **Klijent**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="e58ba-150">Opcionalno označite **Poveži plan projekta sa funkcijom Project Service Automation** da biste povezali datoteku projekta plana sa funkcijom Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e58ba-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="e58ba-151">Izaberite dugme **Objavi**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-151">Click **Publish**.</span></span>  

   <span data-ttu-id="e58ba-152">Povezivanje datoteke projekta sa funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] od datoteke projekta pravi glavnu datoteku i podešava strukturnu analizu posla u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] na samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="e58ba-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="e58ba-153">Da biste uneli izmene u plan projekta, potrebno je da ih napravite u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i da ih objavite kao ispravke za funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="e58ba-154">Uredite projekat koji je uvezen</span><span class="sxs-lookup"><span data-stu-id="e58ba-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="e58ba-155">Da biste uneli promene u plan projekta koji je uvezen u funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], imate dve opcije:</span><span class="sxs-lookup"><span data-stu-id="e58ba-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="e58ba-156">Otvorite glavnu datoteku i izmenite je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="e58ba-157">Opozovite vezu datoteke i uredite je direktno u funkciji Project Service.</span><span class="sxs-lookup"><span data-stu-id="e58ba-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="e58ba-158">Podrazumevano, projekat koji je bio otpremljen iz programa [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] je zaključan i može se uređivati samo u funkciji Project.</span><span class="sxs-lookup"><span data-stu-id="e58ba-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="e58ba-159">Da biste uredili datoteku u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], potrebno je opozvati vezu datoteke.</span><span class="sxs-lookup"><span data-stu-id="e58ba-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="e58ba-160">Uređivanje u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="e58ba-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="e58ba-161">U glavnom meniju kliknite na **Project Service** > **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="e58ba-162">Sa liste projekata otvorite onaj koji ste kreirali u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="e58ba-163">Kliknite na dugme **Otvori u programu MS Project** sa trake.</span><span class="sxs-lookup"><span data-stu-id="e58ba-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="e58ba-164">To će otvoriti povezanu glavnu datoteku u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="e58ba-165">Raskinite vezu datoteke i uredite je u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="e58ba-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="e58ba-166">U glavnom meniju kliknite na **Project Service** > **Projekti**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="e58ba-167">Sa liste projekata otvorite onaj koji ste kreirali u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="e58ba-168">Kliknite na dugme **Raskini vezu sa programom MS Project** sa trake.</span><span class="sxs-lookup"><span data-stu-id="e58ba-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="e58ba-169">Otpremanje datoteke projekta u SharePoint ili Office grupe</span><span class="sxs-lookup"><span data-stu-id="e58ba-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="e58ba-170">Datoteku projekta možete da otpremite u SharePoint i da je pronađete u okviru opcije „Povezani dokumenti“ za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.</span><span class="sxs-lookup"><span data-stu-id="e58ba-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="e58ba-171">Administrator mora da konfiguriše SharePoint upravljanje dokumentima i da ga uključite za entitet Projekat.</span><span class="sxs-lookup"><span data-stu-id="e58ba-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="e58ba-172">Možete i da otpremite datoteku projekta u [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] ako imate podešenu opciju Office grupe.</span><span class="sxs-lookup"><span data-stu-id="e58ba-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="e58ba-173">Otpremanje datoteke za SharePoint</span><span class="sxs-lookup"><span data-stu-id="e58ba-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="e58ba-174">U glavnom meniju kliknite na **Project Service** > **Otpremi**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="e58ba-175">Izaberite **U dokumenta projekta Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="e58ba-176">U dijalogu **Omogući otvaranje u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izaberite **Da** ili **Ne**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="e58ba-177">Ako kliknete na **Da** , moći ćete da izaberete dugme **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u rešenju Project Service Automation, da pokrenete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i učitate datoteku projekta iz SharePoint biblioteke dokumenata.</span><span class="sxs-lookup"><span data-stu-id="e58ba-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="e58ba-178">Ako kliknete na **Ne** , veza za dugme **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće raditi.</span><span class="sxs-lookup"><span data-stu-id="e58ba-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="e58ba-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datoteku možete da pronađete u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u okviru opcije **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.</span><span class="sxs-lookup"><span data-stu-id="e58ba-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="e58ba-180">Otpremanje datoteke za Office grupe</span><span class="sxs-lookup"><span data-stu-id="e58ba-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="e58ba-181">U glavnom meniju kliknite na **Project Service** > **Otpremi**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="e58ba-182">Izaberite **U dokumenta projekta Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="e58ba-183">U dijalogu **Omogući otvaranje u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** izaberite **Da** ili **Ne**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="e58ba-184">Ako kliknete na **Da** , moći ćete da izaberete dugme **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** u rešenju Project Service Automation, da pokrenete [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i učitate datoteku projekta iz SharePoint biblioteke dokumenata.</span><span class="sxs-lookup"><span data-stu-id="e58ba-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="e58ba-185">Ako kliknete na **Ne** , veza za dugme **Otvori u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** neće raditi.</span><span class="sxs-lookup"><span data-stu-id="e58ba-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="e58ba-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] datoteku možete da pronađete u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u okviru opcije **Dokumenti** za određeni [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekat.</span><span class="sxs-lookup"><span data-stu-id="e58ba-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="e58ba-187">Objavite svoje projekte kao predložak</span><span class="sxs-lookup"><span data-stu-id="e58ba-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="e58ba-188">Možete da sačuvate vaš projekat i da ga ponovo upotrebite tako što ćete ga sačuvati ka predložak projekta u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="e58ba-189">Predlošci projekata su planovi projekta koji mogu ponovo da se koriste u funkciji [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="e58ba-190">[Kreiranje predloška za projekat (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="e58ba-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="e58ba-191">Sa kartice **Project Service** kliknite na dugme **Objavi** > **Novi Project Service Automation šablon projekta**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="e58ba-192">U dijalogu **Objavi u novi projekat u predlošku Project Service** unesite **Ime predloška projekta**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="e58ba-193">Opcionalno označite **Poveži plan projekta sa funkcijom Project Service Automation** da biste povezali datoteku projekta sa funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="e58ba-194">Izaberite dugme **Objavi**.</span><span class="sxs-lookup"><span data-stu-id="e58ba-194">Click **Publish**.</span></span>  

<span data-ttu-id="e58ba-195">Povezivanje datoteke projekta sa funkcijom [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] od datoteke projekta pravi glavnu datoteku i podešava strukturnu analizu posla u predlošku za [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] na samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="e58ba-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="e58ba-196">Da biste uneli izmene u plan projekta, potrebno je da ih napravite u programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i da ih objavite kao ispravke za funkciju [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="e58ba-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="e58ba-197">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="e58ba-197">See Also</span></span>  
 [<span data-ttu-id="e58ba-198">Vodič za menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="e58ba-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
