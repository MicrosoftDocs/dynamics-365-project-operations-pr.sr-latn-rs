---
title: Podešavanje resursa projekta
description: Ova tema pruža informacije o podešavanju ili zahtevanju resursa projekta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288756"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="625d4-103">Podešavanje resursa projekta</span><span class="sxs-lookup"><span data-stu-id="625d4-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="625d4-104">Morate postaviti kalendar i povezati ga sa zaposlenim ili radnikom.</span><span class="sxs-lookup"><span data-stu-id="625d4-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="625d4-105">Kalendar se koristi za planiranje projekta i radno vreme resursa koji su rezervisani za projekat.</span><span class="sxs-lookup"><span data-stu-id="625d4-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="625d4-106">Tokom podešavanja kalendara, menadžeri projekata mogu izvršiti nivelisanje resursa kao deo optimizacije resursa.</span><span class="sxs-lookup"><span data-stu-id="625d4-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="625d4-107">Na osnovu kalendarskog rasporeda, resursi se mogu ograničiti.</span><span class="sxs-lookup"><span data-stu-id="625d4-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="625d4-108">Kalendar možete podesiti na stranici **Kalendari**.</span><span class="sxs-lookup"><span data-stu-id="625d4-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="625d4-109">Kada radnika postavite kao resurs projekta, možete da birate između radnika koji rade u kompaniji za koju postavljate resurse.</span><span class="sxs-lookup"><span data-stu-id="625d4-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="625d4-110">Alternativno, možete da izaberete radnike iz drugih kompanija u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="625d4-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="625d4-111">Ti radnici su poznati kao međukompanijski resursi.</span><span class="sxs-lookup"><span data-stu-id="625d4-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="625d4-112">Sledeći postupci objašnjavaju kako da postavite radnika kao resurs projekta u vašoj kompaniji i kako da postavite međukompanijski resurs projekta.</span><span class="sxs-lookup"><span data-stu-id="625d4-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="625d4-113">Postavite radnika kao resurs projekta</span><span class="sxs-lookup"><span data-stu-id="625d4-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="625d4-114">Na stranici **Radnici**, na listi **Radnici**, izaberite radnika kojeg dodajete kao resurs projekta i otvorite zapis radnika.</span><span class="sxs-lookup"><span data-stu-id="625d4-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="625d4-115">U oknu radnji izaberite **Projekat** &gt; **Podešavanje** &gt; **Podešavanje projekta**.</span><span class="sxs-lookup"><span data-stu-id="625d4-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="625d4-116">Izaberite kalendar, a zatim zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="625d4-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="625d4-117">Takođe možete odrediti podrazumevane projekte za resurs kao vrstu prethodnog dodeljivanja.</span><span class="sxs-lookup"><span data-stu-id="625d4-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="625d4-118">Prethodna dodeljivanja se mogu koristiti kada menadžer resursa ili menadžer projekata unapred zna na kojim projektima će resurs raditi.</span><span class="sxs-lookup"><span data-stu-id="625d4-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="625d4-119">Prethodna dodeljivanja se takođe mogu zasnivati na zahtevu sponzora projekta ili klijenta.</span><span class="sxs-lookup"><span data-stu-id="625d4-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="625d4-120">Da biste unapred dodelili projekat, na stranici **Dodela projekata**, na kartici **Projekti**, u listi **Preostali projekti** izaberite odgovarajući projekat.</span><span class="sxs-lookup"><span data-stu-id="625d4-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="625d4-121">Podesite međukompanijski resurs</span><span class="sxs-lookup"><span data-stu-id="625d4-121">Set up an intercompany resource</span></span>

<span data-ttu-id="625d4-122">Kada radnika postavite kao međukompanijski resurs, morate dovršiti podešavanje i u kompaniji zajmodavcu i u kompaniji zajmoprimcu.</span><span class="sxs-lookup"><span data-stu-id="625d4-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="625d4-123">U kompaniji zajmodavcu</span><span class="sxs-lookup"><span data-stu-id="625d4-123">In the lending company</span></span>

1. <span data-ttu-id="625d4-124">U usluzi Finance proverite da li je izabrana kompanija zajmodavac, a zatim dovršite postupak u prethodnom odeljku „Postavljanje radnika kao resursa projekta“.</span><span class="sxs-lookup"><span data-stu-id="625d4-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="625d4-125">Na stranici **Međukompanijsko računovodstvo**, izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="625d4-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="625d4-126">U polju **ID pravnog lica** izaberite kompaniju zajmodavca.</span><span class="sxs-lookup"><span data-stu-id="625d4-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="625d4-127">Popunite preostala polja na odgovarajući način, a zatim izaberite opciju **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="625d4-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="625d4-128">Na stranici **Cena transfera**, izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="625d4-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="625d4-129">U polju **Pravno lice zajmoprimac** izaberite odgovarajuću kompaniju.</span><span class="sxs-lookup"><span data-stu-id="625d4-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="625d4-130">Da biste pozajmljivali kompaniji zajmoprimcu samo one resurse koje ste kreirali na početku ovog odeljka, u polju **Resurs** izaberite ime resursa koji ste kreirali.</span><span class="sxs-lookup"><span data-stu-id="625d4-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="625d4-131">Da biste učinili sve resurse u kompaniji dostupnim kompaniji zajmoprimcu, ostavite polje **Resurs** prazno.</span><span class="sxs-lookup"><span data-stu-id="625d4-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="625d4-132">Na stranici **Parametri upravljanja projektom i računovodstvenom**, na kartici **Međukompanijsko** podesite opciju **Omogući međukompanijsko raspoređivanje resursa vremenske rasporede** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="625d4-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="625d4-133">U kompaniji zajmoprimcu</span><span class="sxs-lookup"><span data-stu-id="625d4-133">In the borrowing company</span></span>

- <span data-ttu-id="625d4-134">Na stranici **Lista resursa**, u filter za pretragu unesite ime resursa koji ste kreirali za kompaniju zajmodavca, da biste proverili da li je ime uključeno u listu resursa za kompaniju zajmoprimca.</span><span class="sxs-lookup"><span data-stu-id="625d4-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="625d4-135">Zahtevanje resursa projekta</span><span class="sxs-lookup"><span data-stu-id="625d4-135">Request project resources</span></span>
<span data-ttu-id="625d4-136">Funkcionalnost za raspoređivanje resursa projekta omogućava da samo menadžeri resursa raspoređuju resurse osoblja na angažovanja ili projekte.</span><span class="sxs-lookup"><span data-stu-id="625d4-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="625d4-137">Da biste omogućili ovu funkcionalnost, izvršite sledeće zadatke ili proverite da li su završeni:</span><span class="sxs-lookup"><span data-stu-id="625d4-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="625d4-138">Podesite sekvence brojeva.</span><span class="sxs-lookup"><span data-stu-id="625d4-138">Set up number sequences.</span></span>
- <span data-ttu-id="625d4-139">Podesite tokove posla upravljanja projektima i računovodstvom.</span><span class="sxs-lookup"><span data-stu-id="625d4-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="625d4-140">Omogućite tokove posla zahteva za resursima.</span><span class="sxs-lookup"><span data-stu-id="625d4-140">Enable resource request workflows.</span></span>

<span data-ttu-id="625d4-141">Nakon završetka prethodnih zadataka, možete izvršiti sledeće zadatke po potrebi:</span><span class="sxs-lookup"><span data-stu-id="625d4-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="625d4-142">Kreirajte zahtev za resursom iz uslovno rezervisanog resursa osoblja.</span><span class="sxs-lookup"><span data-stu-id="625d4-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="625d4-143">Nadgledajte zahteve za resursima.</span><span class="sxs-lookup"><span data-stu-id="625d4-143">Monitor resource requests.</span></span>
- <span data-ttu-id="625d4-144">Ispunite zahteve za resurse.</span><span class="sxs-lookup"><span data-stu-id="625d4-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="625d4-145">Zatražite resurse osoblja iz SAP.</span><span class="sxs-lookup"><span data-stu-id="625d4-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="625d4-146">Rezervišite resurse za projekat bez zahteva za resursima osoblja.</span><span class="sxs-lookup"><span data-stu-id="625d4-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]