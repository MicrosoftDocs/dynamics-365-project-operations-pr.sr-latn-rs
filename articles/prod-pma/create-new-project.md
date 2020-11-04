---
title: Kreirajte novi projekat
description: Ova tema pruža informacije o tome kako da kreirate nov projekat.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083715"
---
# <a name="create-a-new-project"></a><span data-ttu-id="7ef1a-103">Kreirajte novi projekat</span><span class="sxs-lookup"><span data-stu-id="7ef1a-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ef1a-104">Obavite sledeće korake da biste kreirali novi projekat.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="7ef1a-105">Na stranici **Menadžment projekta** izaberite **Novi projekat** i unesite sledeće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="7ef1a-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="7ef1a-106">**Tip projekta:** Vreme i materijal</span><span class="sxs-lookup"><span data-stu-id="7ef1a-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="7ef1a-107">**Naziv projekta:** Nadogradnja XYZ faza 2</span><span class="sxs-lookup"><span data-stu-id="7ef1a-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="7ef1a-108">**Grupa projekata:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="7ef1a-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="7ef1a-109">**ID ugovora o projektu:** 00000002</span><span class="sxs-lookup"><span data-stu-id="7ef1a-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="7ef1a-110">Izaberite **Kreirajte projekat**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="7ef1a-111">Dodeljivanje resursa projektu</span><span class="sxs-lookup"><span data-stu-id="7ef1a-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="7ef1a-112">Na stranici **Radnici** , na listi **Radnici** , izaberite zapis za radnika za kojeg ste prethodno podesili kompetencije i otvorite zapis radnika.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="7ef1a-113">U oknu radnji, na kartici **Projekat** , u grupi **Podešavanje** izaberite **Dodeli projekte**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="7ef1a-114">Na stranici **Dodele projekata za validaciju resursa** , na kartici **Projekti** , u polju **Dodaj projekat izabranim projektima** , filtrirajte prema projektu **Nadogradnja XYZ faza 2**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="7ef1a-115">U oknu **Preostali projekti** , izaberite projekat, a zatim izaberite dugme sa strelicom da biste ga dodali u okno **Izabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="7ef1a-116">Takođe možete da dodelite kategorije za resurs po potrebi.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="7ef1a-117">Tip kategorije je ili **Trošak** ili **Prihod**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="7ef1a-118">Tip kategorije određuje vaša organizacija.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-118">The category type is determined by your organization.</span></span> <span data-ttu-id="7ef1a-119">Ako za resurs nisu dodeljene kategorije, Finance traži podrazumevanu kategoriju cena po satu za troškove i prihod.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="7ef1a-120">Podešavanje karakteristika i uloga resursa projekta</span><span class="sxs-lookup"><span data-stu-id="7ef1a-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="7ef1a-121">Menadžer projekta može koristiti funkcionalnost resursa za projekat da bi kreirao uloge potrebne za projekat.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="7ef1a-122">Uloge se mogu koristiti ako su potvrđeni resursi i dalje nepoznati kada se resursi rezervišu.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="7ef1a-123">Uloge se mogu privremeno rezervisati kao planirani resursi, tako da možete nastaviti faze planiranja projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="7ef1a-124">[![Primer uloge](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="7ef1a-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="7ef1a-125">**Scenario:** Contoso je angažovan da završi projekat Vreme i materijal koji ima odobrenu povelju projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="7ef1a-126">Mlađi menadžer projekta još uvek dovršava opseg projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="7ef1a-127">Menadžer resursa trenutno identifikuje određene resurse koji će biti rezervisani za rad na novom projektu.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="7ef1a-128">Zbog kritične prirode projekta, sponzor projekta zatražio je starijeg menadžera projekta kao jednu od uloga.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="7ef1a-129">Menadžer resursa mora nabaviti novi resurs i definisati ulogu u sistemu u slučaju da mlađi menadžer projekta zahteva informacije o resursima tokom planiranja projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="7ef1a-130">Sledeći koraci pokazuju kako menadžer resursa može da postavi ulogu višeg menadžera projekta i poveže karakteristike resursa sa njom.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="7ef1a-131">Kasnije se uloga može koristiti za traženje dostupnih resursa koji odgovaraju traženim kompetencijama resursa.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="7ef1a-132">Na stranici **Podešavanje uloga** izaberite **Nova** i unesite sledeće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="7ef1a-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="7ef1a-133">**ID uloge:** Viši menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="7ef1a-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="7ef1a-134">**Opis:** Viši menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="7ef1a-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="7ef1a-135">Izaberite **Kreiraj**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-135">Select **Create**.</span></span>
3. <span data-ttu-id="7ef1a-136">Izaberite ulogu **Viši menadžer projekta** , a zatim izaberite **Konfiguriši karakteristike**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="7ef1a-137">U polju **Tip karakteristike** , izaberite **Veština**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="7ef1a-138">U polju **Dostupne karakteristike** , unesite veštinu za traženje.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="7ef1a-139">U polju **Tip karakteristike** , izaberite **Certifikat**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="7ef1a-140">U polju **Dostupne karakteristike** , unesite tip certifikata za traženje.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="7ef1a-141">Dodeljivanje resursa projektu</span><span class="sxs-lookup"><span data-stu-id="7ef1a-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="7ef1a-142">Na stranici **Svi projekti** izaberite projekat **Nadogradnja XYZ faza 2**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="7ef1a-143">Na kartici **Projektni tim i raspoređivanje** , izaberite **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="7ef1a-144">U polju **Uloga** izaberite **Član tima**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="7ef1a-145">Izaberite **Rezerviši iz kalendara**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="7ef1a-146">Na stranici **Dostupnost resursa** izaberite **Pogledajte podešavanja**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="7ef1a-147">Na stranici **Prilagodite postavke prikaza** , unesite sledeće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="7ef1a-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="7ef1a-148">**Format za prikaz opsega datuma:** Dan</span><span class="sxs-lookup"><span data-stu-id="7ef1a-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="7ef1a-149">**Prikaži opise dostupnosti:** Da</span><span class="sxs-lookup"><span data-stu-id="7ef1a-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="7ef1a-150">**Prikaži preostali kapacitet:** Da</span><span class="sxs-lookup"><span data-stu-id="7ef1a-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="7ef1a-151">Izaberite resurs u listi resursa.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="7ef1a-152">Izaberite **Fiksna rezervacija** i **Puni kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="7ef1a-153">Dodeljivanje resursa podrazumevanoj ulozi</span><span class="sxs-lookup"><span data-stu-id="7ef1a-153">Assign a resource to a default role</span></span>

<span data-ttu-id="7ef1a-154">Da bi pomogli menadžerima projekata ili resursa da dalje dubinski pretražuju resurse koji mogu biti rezervisani za projekat.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="7ef1a-155">Podrazumevanu ulogu možete povezati sa postojećim ili novostečenim resursom.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="7ef1a-156">Na primer, kada je Danijel zaposlen, imao je iskustvo i veštine da popuni ulogu poslovnog analitičara.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="7ef1a-157">Menadžer resursa dodelio je ovu ulogu Danijelu kao podrazumevanu.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="7ef1a-158">Stoga je menadžer resursa dodao Danijela u skup poslovnih analitičara koji su dostupni za rad na projektima.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="7ef1a-159">Tokom rezervacije resursa, menadžeri projekata mogu filtrirati resurse uloga koji su dostupni za rad na projektima.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="7ef1a-160">Ove informacije mogu da koriste kao jedan kriterijum kada obavljaju analizu odluka prema više kriterijuma tokom popunjavanja resursa.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="7ef1a-161">Oni takođe mogu da dodaju druge karakteristike resursa u filter za traženje resursa koji imaju specifične veštine, obrazovanje i iskustvo za dati projekat.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="7ef1a-162">**Scenario:** Odobreni projekat je započeo, a uloga višeg menadžera projekta bila je rezervisana kao planirani resurs tokom faze planiranja projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="7ef1a-163">Menadžer resursa je sada nabavio resurs za ispunjavanje uloge višeg menadžera projekta.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="7ef1a-164">Na stranici **Lista resursa** , izaberite **Danijel Goldšmit**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="7ef1a-165">Na stranici **Uloga resursa** izaberite **Nova** i unesite sledeće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="7ef1a-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="7ef1a-166">**Stupa na snagu:** Unesite trenutni datum.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="7ef1a-167">**Isticanje:** Unesite **Nikad**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="7ef1a-168">**Uloga:** Unesite **Viši menadžer projekta**.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="7ef1a-169">Izaberite **Sačuvaj** , a zatim zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="7ef1a-170">Na kartici **Kompetencije** , dodajte veštinu **Menadžment projekta** i **PMP** certifikat.</span><span class="sxs-lookup"><span data-stu-id="7ef1a-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
