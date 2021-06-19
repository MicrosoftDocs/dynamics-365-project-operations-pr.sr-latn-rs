---
title: Rešavanje problema sa radom u mreži podataka
description: Ova tema pruža informacije o rešavanju problema potrebne za rad u mreži zadataka.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213417"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="fc670-103">Rešavanje problema sa radom u mreži podataka</span><span class="sxs-lookup"><span data-stu-id="fc670-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="fc670-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="fc670-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc670-105">Ova tema opisuje kako da rešite probleme na koje biste mogli naići tokom rada sa upravljanjem troškovima.</span><span class="sxs-lookup"><span data-stu-id="fc670-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="fc670-106">Omogućavanje kolačića</span><span class="sxs-lookup"><span data-stu-id="fc670-106">Enable cookies</span></span>

<span data-ttu-id="fc670-107">Project Operations zahteva da nezavisni kolačići budu omogućeni kako bi se prikazivala strukturna analiza posla.</span><span class="sxs-lookup"><span data-stu-id="fc670-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="fc670-108">Kada nezavisni kolačići nisu omogućeni, umesto da vidite zadatke, videćete praznu stranicu kada odaberete karticu **Zadaci** na stranici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="fc670-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Prazna kartica kada nezavisni kolačići nisu omogućeni](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="fc670-110">Zaobilazno rešenje</span><span class="sxs-lookup"><span data-stu-id="fc670-110">Workaround</span></span>
<span data-ttu-id="fc670-111">Za pregledače Microsoft Edge ili Google Chrome, sledeći postupci opisuju kako da ažurirate podešavanja pregledača kako biste omogućili nezavisne kolačiće.</span><span class="sxs-lookup"><span data-stu-id="fc670-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="fc670-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fc670-112">Microsoft Edge</span></span>

1. <span data-ttu-id="fc670-113">Otvorite pregledač Edge.</span><span class="sxs-lookup"><span data-stu-id="fc670-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="fc670-114">U gornjem desnom uglu izaberite **tri tačke** (...), a zatim izaberite **Podešavanja**.</span><span class="sxs-lookup"><span data-stu-id="fc670-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="fc670-115">U delu **Kolačići i dozvole za lokacije** izaberite **Kolačići i podaci o lokacijama**.</span><span class="sxs-lookup"><span data-stu-id="fc670-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="fc670-116">Isključite **Blokiraj kolačiće treće strane**.</span><span class="sxs-lookup"><span data-stu-id="fc670-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="fc670-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="fc670-117">Google Chrome</span></span>

1. <span data-ttu-id="fc670-118">Otvorite pregledač Chrome.</span><span class="sxs-lookup"><span data-stu-id="fc670-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="fc670-119">U gornjem desnom uglu izaberite tri vertikalne tačke, a zatim izaberite **Podešavanja**.</span><span class="sxs-lookup"><span data-stu-id="fc670-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="fc670-120">U delu **Privatnost i bezbednost** izaberite **Kolačići i drugi podaci o lokacijama**.</span><span class="sxs-lookup"><span data-stu-id="fc670-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="fc670-121">Izaberite **Dozvoli sve kolačiće**.</span><span class="sxs-lookup"><span data-stu-id="fc670-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc670-122">Ako blokirate nezavisne kolačiće, svi kolačići i podaci o lokacijama sa drugih lokacija biće blokirani, čak i ako je lokacija dozvoljena na listi izuzetaka.</span><span class="sxs-lookup"><span data-stu-id="fc670-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="fc670-123">PEX krajnja tačka</span><span class="sxs-lookup"><span data-stu-id="fc670-123">PEX Endpoint</span></span>

<span data-ttu-id="fc670-124">Project Operations zahteva da parametar projekta upućuje na PEX krajnju tačku.</span><span class="sxs-lookup"><span data-stu-id="fc670-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="fc670-125">Ova krajnja tačka je potreban za komunikaciju sa uslugom koja se koristi za prikazivanje strukturne analize posla.</span><span class="sxs-lookup"><span data-stu-id="fc670-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="fc670-126">Ako parametar nije omogućen, dobićete grešku „Parametar projekta nije važeći“.</span><span class="sxs-lookup"><span data-stu-id="fc670-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="fc670-127">Zaobilazno rešenje</span><span class="sxs-lookup"><span data-stu-id="fc670-127">Workaround</span></span>
 ![Polje „PEX krajnja tačka“ u parametru projekta](media/projectparameter.png)

1. <span data-ttu-id="fc670-129">Dodajte polje **PEX krajnja tačka** na stranicu **Parametri projekta**.</span><span class="sxs-lookup"><span data-stu-id="fc670-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="fc670-130">Ažurirajte polje sledećom vrednosti: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="fc670-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="fc670-131">Uklonite polje sa stranice **Parametri projekta**.</span><span class="sxs-lookup"><span data-stu-id="fc670-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="fc670-132">Privilegije za projekat za veb</span><span class="sxs-lookup"><span data-stu-id="fc670-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="fc670-133">Project Operations se oslanja na eksternu uslugu zakazivanja.</span><span class="sxs-lookup"><span data-stu-id="fc670-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="fc670-134">Usluga zahteva da korisnik ima nekoliko uloga dodeljenih za čitanje i pisanje u entitete povezane sa strukturnom analizom posla.</span><span class="sxs-lookup"><span data-stu-id="fc670-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="fc670-135">Ti entiteti uključuju projektne zadatke, dodeljivanje resursa i zavisne elemente zadataka.</span><span class="sxs-lookup"><span data-stu-id="fc670-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="fc670-136">Ako korisnik ne može da prikaže strukturnu analizu posla kada dođe na karticu **Zadaci**, to je verovatno zato što Project Operations nije omogućen.</span><span class="sxs-lookup"><span data-stu-id="fc670-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="fc670-137">Korisnik može da dobije grešku za bezbedonosnu ulogu ili grešku povezanu sa uskraćivanjem pristupa.</span><span class="sxs-lookup"><span data-stu-id="fc670-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="fc670-138">Zaobilazno rešenje</span><span class="sxs-lookup"><span data-stu-id="fc670-138">Workaround</span></span>

1. <span data-ttu-id="fc670-139">Idite na **Podešavanja > Bezbednost > Korisnici > Korisnici aplikacija**.</span><span class="sxs-lookup"><span data-stu-id="fc670-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Čitač aplikacije](media/applicationuser.jpg)
   
2. <span data-ttu-id="fc670-141">Dvaput kliknite na zapis korisnika aplikacije da biste proverili sledeće:</span><span class="sxs-lookup"><span data-stu-id="fc670-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="fc670-142">Korisnik ima pristup projektu.</span><span class="sxs-lookup"><span data-stu-id="fc670-142">The user has access to the project.</span></span> <span data-ttu-id="fc670-143">Ova verifikacija se obično obavlja tako što se osigurava da korisnik ima bezbednosnu ulogu **Menadžer projekta**.</span><span class="sxs-lookup"><span data-stu-id="fc670-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="fc670-144">Korisnik aplikacije Microsoft Project postoji i pravilno je konfigurisan.</span><span class="sxs-lookup"><span data-stu-id="fc670-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="fc670-145">Ako ovaj korisnik ne postoji, možete kreirati zapis novog korisnika.</span><span class="sxs-lookup"><span data-stu-id="fc670-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="fc670-146">Izaberite **Novi korisnici**.</span><span class="sxs-lookup"><span data-stu-id="fc670-146">Select **New Users**.</span></span> <span data-ttu-id="fc670-147">Promenite obrazac za unos u **Korisnik aplikacije**, a zatim dodajte **ID aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="fc670-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Detalji o korisniku aplikacije](media/applicationuserdetails.jpg)

4. <span data-ttu-id="fc670-149">Proverite da li je korisniku dodeljena ispravna licenca i da li je usluga omogućena u detaljima planova usluge licence.</span><span class="sxs-lookup"><span data-stu-id="fc670-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="fc670-150">Proverite da li korisnik može da otvori project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="fc670-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="fc670-151">Proverite kroz parametre projekta da li sistem pokazuje na ispravnu krajnju tačku projekta.</span><span class="sxs-lookup"><span data-stu-id="fc670-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="fc670-152">Proverite da li je kreiran korisnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="fc670-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="fc670-153">Primenite sledeće bezbednosne uloge na korisnika:</span><span class="sxs-lookup"><span data-stu-id="fc670-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="fc670-154">Korisnik usluge Dataverse</span><span class="sxs-lookup"><span data-stu-id="fc670-154">Dataverse User</span></span>
  - <span data-ttu-id="fc670-155">Project Operations sistem</span><span class="sxs-lookup"><span data-stu-id="fc670-155">Project Operations System</span></span>
  - <span data-ttu-id="fc670-156">Projektni sistem</span><span class="sxs-lookup"><span data-stu-id="fc670-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="fc670-157">Greška pri ažuriranju strukturne analize posla</span><span class="sxs-lookup"><span data-stu-id="fc670-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="fc670-158">Kada se obavi jedno ili više ažuriranja strukturne analize posla, promene na kraju ne uspeju i nisu sačuvane.</span><span class="sxs-lookup"><span data-stu-id="fc670-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="fc670-159">Dolazi do greške u mreži rasporeda uz napomenu da „Nedavna promena koju ste uneli nije mogla biti sačuvana“.</span><span class="sxs-lookup"><span data-stu-id="fc670-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="fc670-160">Zaobilazno rešenje</span><span class="sxs-lookup"><span data-stu-id="fc670-160">Workaround</span></span>

1. <span data-ttu-id="fc670-161">Proverite da li je korisniku dodeljena ispravna licenca i da li je usluga omogućena u detaljima planova usluge licence.</span><span class="sxs-lookup"><span data-stu-id="fc670-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="fc670-162">Proverite da li korisnik može da otvori project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="fc670-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="fc670-163">Proverite da li sistem pokazuje na ispravnu krajnju tačku projekta.</span><span class="sxs-lookup"><span data-stu-id="fc670-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="fc670-164">Proverite da li je kreiran korisnik projektne aplikacije.</span><span class="sxs-lookup"><span data-stu-id="fc670-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="fc670-165">Primenite sledeće bezbednosne uloge na korisnika:</span><span class="sxs-lookup"><span data-stu-id="fc670-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="fc670-166">Dataverse korisnik ili osnovni korisnik</span><span class="sxs-lookup"><span data-stu-id="fc670-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="fc670-167">Project Operations sistem</span><span class="sxs-lookup"><span data-stu-id="fc670-167">Project Operations System</span></span>
  - <span data-ttu-id="fc670-168">Projektni sistem</span><span class="sxs-lookup"><span data-stu-id="fc670-168">Project System</span></span>
  - <span data-ttu-id="fc670-169">Project Operations sistem dvostrukog upisivanja (ova uloga je potrebna ako primenjujete resurs/scenario koji nije zasnovan na zalihama usluge Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="fc670-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
