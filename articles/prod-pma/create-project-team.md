---
title: Kreiranje projektnog tima
description: Ova tema pruža informacije o tome kako da kreirate i upravljate projektnim timovima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083745"
---
# <a name="create-a-project-team"></a><span data-ttu-id="6f329-103">Kreiranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="6f329-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f329-104">Da bi koristio uloge koje su prethodno postavljene u projektu, menadžer projekta mora povezati uloge sa projektom.</span><span class="sxs-lookup"><span data-stu-id="6f329-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="6f329-105">Za projekat se može dodeliti više uloga.</span><span class="sxs-lookup"><span data-stu-id="6f329-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="6f329-106">Da bi se sprečila zabuna, ove uloge se automatski označavaju tokom rezervacije.</span><span class="sxs-lookup"><span data-stu-id="6f329-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="6f329-107">Na primer, ako menadžer projekta zahteva tri softverska inženjera, automatski se generišu tri uloge softverskog inženjera koje imaju oznake **softverski inženjer 1** , **softverski inženjer 2** i **softverski inženjer 3**.</span><span class="sxs-lookup"><span data-stu-id="6f329-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1** , **software engineer 2** , and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="6f329-108">Ako su karakteristike uloge prethodno postavljene za ulogu, one se primenjuju kao filter tokom pretraživanja resursa.</span><span class="sxs-lookup"><span data-stu-id="6f329-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="6f329-109">Dodatne karakteristike se mogu dodati po potrebi za dalje preciziranje pretrage.</span><span class="sxs-lookup"><span data-stu-id="6f329-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="6f329-110">Postavke prikaza takođe se mogu prilagoditi kako bi se dobio bolji prikaz dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="6f329-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="6f329-111">Postoje opcije za prikazivanje raspoloživosti po satima, dnevno, nedeljno, mesečno, kvartalno i godišnje.</span><span class="sxs-lookup"><span data-stu-id="6f329-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="6f329-112">Takođe postoji opcija za prikaz raspoloživog i preostalog kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="6f329-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="6f329-113">Ova opcija je korisna za upravljanje vremenom kada procenjujete dostupno vreme za aktivnosti ili dostupnost resursa.</span><span class="sxs-lookup"><span data-stu-id="6f329-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="6f329-114">Menadžer projekta može odabrati ulogu na stranici, a zatim, ako postoji dostupan resurs koji odgovara zahtevima, izaberite da rezervišete resurs za popunjavanje uloge.</span><span class="sxs-lookup"><span data-stu-id="6f329-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="6f329-115">Imajte na umu da resursi u ovom trenutku ne moraju biti rezervisani u fazi planiranja.</span><span class="sxs-lookup"><span data-stu-id="6f329-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="6f329-116">Kada kreirate SAP, možete zameniti uloge resursima osoblja za projekat.</span><span class="sxs-lookup"><span data-stu-id="6f329-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="6f329-117">Ako se uloge zamene resursima osoblja u SAP-u, podešavanje resursa automatski ažurira spisak i raspored projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="6f329-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="6f329-118">[![Spisak projektnog tima koji uključuje i uloge i stvarne resurse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="6f329-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="6f329-119">Menadžer projekta ima razne mogućnosti za rezervaciju resursa za projekat, kao što su **Preostali kapacitet** , **Pun kapacitet** , **Procenat kapaciteta** i **Navedite radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="6f329-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity** , **Full capacity** , **Capacity percentage** , and **Specify hours**.</span></span> <span data-ttu-id="6f329-120">Ove opcije rezervacije mogu se otkazati u bilo kom trenutku ako se promene dodeljivanja resursa.</span><span class="sxs-lookup"><span data-stu-id="6f329-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="6f329-121">Podržane su dve vrste rezervacija:</span><span class="sxs-lookup"><span data-stu-id="6f329-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="6f329-122">**Fiksna rezervacija** – Rezervacija resursa je odobrena i potvrđena za rad na angažovanju tokom određenog vremena.</span><span class="sxs-lookup"><span data-stu-id="6f329-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="6f329-123">**Uslovna rezervacija** – Rezervacije resursa su uslovno podešene za rad na angažovanju tokom određenog vremena.</span><span class="sxs-lookup"><span data-stu-id="6f329-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="6f329-124">Sledeća procedura objašnjava kako da kreirate projektni tim.</span><span class="sxs-lookup"><span data-stu-id="6f329-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="6f329-125">Kreiranje projektnog tima</span><span class="sxs-lookup"><span data-stu-id="6f329-125">Create a project team</span></span>

1. <span data-ttu-id="6f329-126">Na stranici liste **Svi projekti** izaberite projekat, a zatim izaberite **Uredi**.</span><span class="sxs-lookup"><span data-stu-id="6f329-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="6f329-127">Na kartici **Projektni tim i raspoređivanje** , u polje **Datum završetka rasporeda** unesite datum početka rasporeda uvećan za jedan mesec.</span><span class="sxs-lookup"><span data-stu-id="6f329-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="6f329-128">Na primer, ako je datum početka rasporeda 24. jun 2017. (24.6.2017), Unesite **24.07.2017**.</span><span class="sxs-lookup"><span data-stu-id="6f329-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="6f329-129">Izaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="6f329-129">Select **Add**.</span></span>
4. <span data-ttu-id="6f329-130">U oknu **Dodavanje uloga u projekat** , u polju **Uloga** izaberite **Viši menadžer projekta**.</span><span class="sxs-lookup"><span data-stu-id="6f329-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="6f329-131">Izaberite **Potrebne kompetencije**.</span><span class="sxs-lookup"><span data-stu-id="6f329-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="6f329-132">Na stranici **Odaberite karakteristike** , karakteristike koje ste prethodno postavili za ulogu višeg menadžera projekta su podrazumevano izabrane.</span><span class="sxs-lookup"><span data-stu-id="6f329-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="6f329-133">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="6f329-133">Select **OK**.</span></span>
7. <span data-ttu-id="6f329-134">Na stranici **Dodavanje uloge projektu** , u polju **Broj resursa** unesite **1**.</span><span class="sxs-lookup"><span data-stu-id="6f329-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="6f329-135">U polju **Resurs** , pregled prikazuje sve resurse koji imaju potrebne kompetencije.</span><span class="sxs-lookup"><span data-stu-id="6f329-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="6f329-136">Izaberite **Danijel Goldšmit** , a zatim izaberite **Kreiraj**.</span><span class="sxs-lookup"><span data-stu-id="6f329-136">Select **Daniel Goldschmidt** , and then select **Create**.</span></span>
9. <span data-ttu-id="6f329-137">Na stranici **Projekat** izaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="6f329-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="6f329-138">U oknu **Dodavanje uloga u projekat** , u polju **Uloga** izaberite **Član tima**.</span><span class="sxs-lookup"><span data-stu-id="6f329-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="6f329-139">U polje **Broj resursa** unesite **5**.</span><span class="sxs-lookup"><span data-stu-id="6f329-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="6f329-140">Izaberite **Kreiraj**.</span><span class="sxs-lookup"><span data-stu-id="6f329-140">Select **Create**.</span></span>
12. <span data-ttu-id="6f329-141">Na stranici **Projekti** , izaberite **Popuni resurs**.</span><span class="sxs-lookup"><span data-stu-id="6f329-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="6f329-142">Nadgledajte projektne timove</span><span class="sxs-lookup"><span data-stu-id="6f329-142">Monitor project teams</span></span>
1. <span data-ttu-id="6f329-143">Na stranici **Svi projekti** , izaberite vezu **ID projekta** za projekat **Nadogradnja XYZ faza 2**.</span><span class="sxs-lookup"><span data-stu-id="6f329-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="6f329-144">Na brzoj kartici **Projektni tim i zakazivanje** , uverite se da su navedeni resursi projekta tačni.</span><span class="sxs-lookup"><span data-stu-id="6f329-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
