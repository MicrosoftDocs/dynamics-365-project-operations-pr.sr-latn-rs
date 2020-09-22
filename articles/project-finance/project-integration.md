---
title: Integracija usluge Microsoft Project Client
description: Planiranje i održavanje rasporeda projekta može biti složeno, pa menadžeri projekata moraju da koriste alate koji im pomažu u upravljanju ovim zadatkom. Integracija sa uslugom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturne analize posla na projektu.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: c6478e05-50ee-4993-87f4-6ce9cb78f076
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e35e1e54bad659d1329c333479830b680a17cbb0
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755226"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="747ea-104">Integracija usluge Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="747ea-105">Planiranje i održavanje rasporeda projekta može biti složeno, pa menadžeri projekata moraju da koriste alate koji im pomažu u upravljanju ovim zadatkom.</span><span class="sxs-lookup"><span data-stu-id="747ea-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="747ea-106">Integracija sa uslugom Microsoft Project Client pruža podršku za otvaranje i upravljanje strukturne analize posla na projektu.</span><span class="sxs-lookup"><span data-stu-id="747ea-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="747ea-107">Menadžer projekta može objaviti sve promene na strukturnoj analizi posla Dynamics 365 Finance projekta.</span><span class="sxs-lookup"><span data-stu-id="747ea-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="747ea-108">Ako koristite ispravku iz jula (verzija 10.0.4), morate instalirati KB 4054797 i 4055884.</span><span class="sxs-lookup"><span data-stu-id="747ea-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="747ea-109">Konfigurisanje programskog dodatka za Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="747ea-110">Da biste omogućili integraciju sa uslugom Microsoft Project Client, potrebno je da instalirate Microsoft Dynamics 365 programski dodatak u korisnikovoj klijentskoj aplikaciji Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="747ea-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="747ea-111">To se postiže otvaranjem **Radnog prostora za upravljanje projektima**.</span><span class="sxs-lookup"><span data-stu-id="747ea-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="747ea-112">•   Kliknite na **Konfiguriši programski dodatak za klijenta** iz odeljka **Veze** > **Podešavanje** radnog prostora.</span><span class="sxs-lookup"><span data-stu-id="747ea-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="747ea-113">•   Kliknite na **Otvori**, a zatim kliknite na **Pokreni** kada to bude zatraženo.</span><span class="sxs-lookup"><span data-stu-id="747ea-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="747ea-114">Otvorite i uredite postojeću probnu verziju strukturne analize posla u programu Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="747ea-115">Ako projekat u usluzi Dynamics 365 Finance već ima kreiranu strukturnu analizu posla, strukturna analiza posla može se otvoriti u aplikaciji Microsoft Project Client ako je strukturna analiza posla u statusu radne verzije.</span><span class="sxs-lookup"><span data-stu-id="747ea-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="747ea-116">Da biste otvorili stranicu **Projekat**, kliknite na vezu **Otvori u programu Microsoft Project** na kartici **Plan**. Ova stranica se takođe može otvoriti iz aplikacije Microsoft Project Client klikom na **Otvori** na kartici **Microsoft Dynamics 365**. Izaberite **Pravno lice** i **Projekat** sa liste.</span><span class="sxs-lookup"><span data-stu-id="747ea-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="747ea-117">Ako koristite Internet Explorer kao pregledač, moraćete da kliknete na **Sačuvaj** da biste je ručno otvorili sa lokacije na koju se datoteka preuzima.</span><span class="sxs-lookup"><span data-stu-id="747ea-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="747ea-118">Ili kliknite na **Sačuvaj i otvori** da biste otvorili datoteku u programu Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="747ea-119">Nemojte da preimenujete naziv datoteke prilikom čuvanja.</span><span class="sxs-lookup"><span data-stu-id="747ea-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="747ea-120">Pre nego što izvršite bilo kakvu izmenu datoteke koristeći Microsoft Project Client, treba da je proverite. Kliknite na **Proveri** na kartici **Microsoft Dynamics 365**. Ovo će sprečiti druge korisnike da istovremeno uređuju strukturnu analizu posla iz usluge Finance.</span><span class="sxs-lookup"><span data-stu-id="747ea-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="747ea-121">Da biste objavili strukturnu analizu posla nakon dovršavanja bilo kakvih izmena, kliknite na **Prijavi** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="747ea-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="747ea-122">Ako je projektni tim već dodat projektu u usluzi Finance, lista resursa će se popuniti članovima tima.</span><span class="sxs-lookup"><span data-stu-id="747ea-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="747ea-123">Ako projektni tim još nije dodat u projekat, možete odabrati resurse i izgraditi tim unutar aplikacije Microsoft Project Client klikom na dugme **Resursi** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="747ea-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="747ea-124">Sledeći podaci će se sinhronizovati natrag u Finance kao deo procesa prijave:</span><span class="sxs-lookup"><span data-stu-id="747ea-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="747ea-125">•   Naziv zadatka</span><span class="sxs-lookup"><span data-stu-id="747ea-125">•   Task name</span></span>

<span data-ttu-id="747ea-126">•   Datum početka</span><span class="sxs-lookup"><span data-stu-id="747ea-126">•   Start date</span></span>

<span data-ttu-id="747ea-127">•   Datum završetka</span><span class="sxs-lookup"><span data-stu-id="747ea-127">•   Finish date</span></span>

<span data-ttu-id="747ea-128">•   Prethodni zadaci</span><span class="sxs-lookup"><span data-stu-id="747ea-128">•   Predecessors</span></span>

<span data-ttu-id="747ea-129">•   Nazivi resursa</span><span class="sxs-lookup"><span data-stu-id="747ea-129">•   Resource names</span></span>

<span data-ttu-id="747ea-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="747ea-130">•   Category</span></span>

<span data-ttu-id="747ea-131">•   Kategorija resursa</span><span class="sxs-lookup"><span data-stu-id="747ea-131">•   Resource category</span></span>

<span data-ttu-id="747ea-132">•   Radno vreme</span><span class="sxs-lookup"><span data-stu-id="747ea-132">•   Work hours</span></span>

<span data-ttu-id="747ea-133">•   Napomene</span><span class="sxs-lookup"><span data-stu-id="747ea-133">•   Notes</span></span>

<span data-ttu-id="747ea-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="747ea-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="747ea-135">Ako dodate bilo koju drugu kolonu u Microsoft Project Client datoteku, ona neće biti sačuvana u datoteci i neće se prikazati kada se datoteka ponovo otvori.</span><span class="sxs-lookup"><span data-stu-id="747ea-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="747ea-136">Napravite strukturnu analizu posla za postojeći projekat koristeći Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="747ea-137">Da biste kreirali strukturnu analizu posla koristeći Microsoft Project Client, sledite ove korake:</span><span class="sxs-lookup"><span data-stu-id="747ea-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="747ea-138">Otvorite Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="747ea-139">Na kartici **Microsoft Dynamics 365**, kliknite na **Otvori**.</span><span class="sxs-lookup"><span data-stu-id="747ea-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="747ea-140">Izaberite **Pravno lice** za projekat.</span><span class="sxs-lookup"><span data-stu-id="747ea-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="747ea-141">Izaberite **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="747ea-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="747ea-142">Kliknite na **Proveri** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="747ea-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="747ea-143">Kada budete spremni za objavljivanje u Finance, kliknite na **Prijavi** na kartici **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="747ea-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="747ea-144">Zamenite postojeću strukturnu analizu posla za postojeći projekat koristeći Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="747ea-145">Da biste kreirali novu strukturnu analizu posla pomoću aplikacije Microsoft Project Client i zamenili postojeću strukturnu analizu posla za postojeći projekat, sledite ove korake:</span><span class="sxs-lookup"><span data-stu-id="747ea-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="747ea-146">Otvorite Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="747ea-147">Kreirajte raspored u aplikaciji Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="747ea-148">Na kartici **Microsoft Dynamics 365**, kliknite na **Sačuvaj promene** > **Zameni postojeći projekat**.</span><span class="sxs-lookup"><span data-stu-id="747ea-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="747ea-149">Izaberite **Pravno lice** za projekat.</span><span class="sxs-lookup"><span data-stu-id="747ea-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="747ea-150">Izaberite **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="747ea-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="747ea-151">Kliknite na dugme **U redu**.</span><span class="sxs-lookup"><span data-stu-id="747ea-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="747ea-152">Kreirajte novi projekat iz aplikacije Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="747ea-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="747ea-153">Otvorite Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="747ea-154">Kreirajte raspored u aplikaciji Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="747ea-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="747ea-155">Na kartici **Microsoft Dynamics 365**, kliknite na **Sačuvaj promene** > **Sačuvaj u novi projekat**.</span><span class="sxs-lookup"><span data-stu-id="747ea-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="747ea-156">Izaberite **Pravno lice** za projekat.</span><span class="sxs-lookup"><span data-stu-id="747ea-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="747ea-157">Unesite **ID projekta**, ako je neophodno.</span><span class="sxs-lookup"><span data-stu-id="747ea-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="747ea-158">Unesite **Naziv projekta**.</span><span class="sxs-lookup"><span data-stu-id="747ea-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="747ea-159">Izaberite **Tip projekta**, **Grupu projekta** i **ID ugovora o projektu**.</span><span class="sxs-lookup"><span data-stu-id="747ea-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="747ea-160">Alternativno, možete da kreirate novi ugovor o projektu klikom na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="747ea-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="747ea-161">Izaberite **Kalendar** koji ćete koristiti za obezbeđivanje resursa.</span><span class="sxs-lookup"><span data-stu-id="747ea-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="747ea-162">Kliknite na dugme **U redu**.</span><span class="sxs-lookup"><span data-stu-id="747ea-162">Click **OK**.</span></span>
