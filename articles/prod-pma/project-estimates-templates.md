---
title: Sinhronizovanje procena projekta direktno iz usluge Project Service Automation sa uslugom Finance and Operations
description: Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju procene radnih sati i procene troškova projekta direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289476"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="f454a-103">Sinhronizovanje procena projekta direktno iz usluge Project Service Automation sa uslugom Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f454a-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f454a-104">Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju procene radnih sati i procene troškova projekta direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f454a-105">Integracija projektnih zadataka, kategorije transakcija troškova, procene radnih sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="f454a-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="f454a-106">Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.</span><span class="sxs-lookup"><span data-stu-id="f454a-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="f454a-107">Tok podataka iz usluge Project Service Automation u Finance</span><span class="sxs-lookup"><span data-stu-id="f454a-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="f454a-108">Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="f454a-109">Predlošci za integraciju koji su dostupni sa funkcijom Integracija podataka omogućava tok podataka o procenama radnih sati projekta i procenama troškova projekta između iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f454a-110">Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="f454a-111">[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="f454a-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="f454a-112">Procene radnih sati za projekat</span><span class="sxs-lookup"><span data-stu-id="f454a-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f454a-113">Predlošci i zadaci</span><span class="sxs-lookup"><span data-stu-id="f454a-113">Template and tasks</span></span>

<span data-ttu-id="f454a-114">Da biste pristupili dostupnim predlošcima, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za izbor javnih predložaka.</span><span class="sxs-lookup"><span data-stu-id="f454a-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="f454a-115">Sledeći predložak i osnovni zadaci koji se koriste za sinhronizaciju procena radnih sati projekta iz usluge Project Service Automation u Finance:</span><span class="sxs-lookup"><span data-stu-id="f454a-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f454a-116">**Naziv predloška u Integraciji podataka:** Procene radnih sati projekta (iz PSA u Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f454a-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f454a-117">**Naziv zadataka u projektu:**</span><span class="sxs-lookup"><span data-stu-id="f454a-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f454a-118">Odnosi između transakcija</span><span class="sxs-lookup"><span data-stu-id="f454a-118">Transaction relationships</span></span>
    - <span data-ttu-id="f454a-119">Procene troškova</span><span class="sxs-lookup"><span data-stu-id="f454a-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f454a-120">Skup entiteta</span><span class="sxs-lookup"><span data-stu-id="f454a-120">Entity set</span></span>

| <span data-ttu-id="f454a-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f454a-121">Project Service Automation</span></span> | <span data-ttu-id="f454a-122">Finance</span><span class="sxs-lookup"><span data-stu-id="f454a-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="f454a-123">Projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="f454a-123">Project tasks</span></span>              | <span data-ttu-id="f454a-124">Entitet integracije za procene radnih sati projekta</span><span class="sxs-lookup"><span data-stu-id="f454a-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="f454a-125">Tok entiteta</span><span class="sxs-lookup"><span data-stu-id="f454a-125">Entity flow</span></span>

<span data-ttu-id="f454a-126">Procenama radnih sati projekta se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao predviđanja sati projekta.</span><span class="sxs-lookup"><span data-stu-id="f454a-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f454a-127">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="f454a-127">Prerequisites</span></span>

<span data-ttu-id="f454a-128">Da bi mogla da se izvrši sinhronizacija procena radnih sati projekta, morate sinhronizovati projekte, projektne zadatke i kategorije transakcija troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="f454a-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f454a-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="f454a-129">Power Query</span></span>

<span data-ttu-id="f454a-130">U predlošku za procenu radnog vremena projekta morate da koristite Microsoft Power Query za Excel da biste izvršili ove zadatke:</span><span class="sxs-lookup"><span data-stu-id="f454a-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="f454a-131">Postavite ID podrazumevanog modela predviđanja koji će se koristiti kada integracija kreira nova predviđanja sati.</span><span class="sxs-lookup"><span data-stu-id="f454a-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f454a-132">U zadatku filtrirajte sve zapise specifične za resurse koji neće uspeti u integraciji predviđanja radnih sati.</span><span class="sxs-lookup"><span data-stu-id="f454a-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="f454a-133">Filtrirajte sve prazne redove kategorija transakcija.</span><span class="sxs-lookup"><span data-stu-id="f454a-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="f454a-134">Neispunjavanje ovog zadatka može rezultirati netačnim predviđanjima radnih sati.</span><span class="sxs-lookup"><span data-stu-id="f454a-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f454a-135">Podesite podrazumevani ID modela predviđanja</span><span class="sxs-lookup"><span data-stu-id="f454a-135">Set the default forecast model ID</span></span>

<span data-ttu-id="f454a-136">Da biste ažurirali podrazumevani ID modela predviđanja u predlošku, kliknite na strelicu **Mapa** za otvaranje mapiranja.</span><span class="sxs-lookup"><span data-stu-id="f454a-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f454a-137">Zatim izaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="f454a-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f454a-138">Ako koristite podrazumevani predložak procene radnih sati projekta (iz PSA u Fin and Ops), izaberite **Uslov umetanja** u list **Primenjeni koraci**.</span><span class="sxs-lookup"><span data-stu-id="f454a-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="f454a-139">U stavci **Funkcija**, zamenite **O\_forecast** nazivom ID-a modela predviđanja koji treba koristiti uz integraciju.</span><span class="sxs-lookup"><span data-stu-id="f454a-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f454a-140">Podrazumevani predložak sadrži ID modela predviđanja iz demo podataka.</span><span class="sxs-lookup"><span data-stu-id="f454a-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f454a-141">Ako kreirate novi obrazac, morate dodati ovu kolonu.</span><span class="sxs-lookup"><span data-stu-id="f454a-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f454a-142">U usluzi Power Query izaberite **Dodaj uslovnu kolonu** i unesite naziv za novu kolonu, kao što je **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f454a-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f454a-143">Unesite uslov za kolonu, gde, ako Project zadatak nije bez vrednosti, onda \<enter the forecast model ID\>; u suprotnom je bez vrednosti.</span><span class="sxs-lookup"><span data-stu-id="f454a-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="f454a-144">Filtriranje zapisa specifičnih za resurse</span><span class="sxs-lookup"><span data-stu-id="f454a-144">Filter out resource-specific records</span></span>

<span data-ttu-id="f454a-145">Predložak procena radnih sati projekta (iz PSA u Fin and Ops) ima podrazumevani filter koji uklanja sve zapise specifične za resurse.</span><span class="sxs-lookup"><span data-stu-id="f454a-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="f454a-146">Ako kreirate sopstveni obrazac, morate dodati ovaj filter.</span><span class="sxs-lookup"><span data-stu-id="f454a-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f454a-147">Izaberite vezu **Napredni upit i filtriranje** da filtrirate po koloni **msdyn\_islinetask** tako da budu uvršćeni samo **Netačni** zapisi.</span><span class="sxs-lookup"><span data-stu-id="f454a-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="f454a-148">Filtrirajte prazne redove kategorija transakcija</span><span class="sxs-lookup"><span data-stu-id="f454a-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="f454a-149">Morate dodati filter da biste uklonili sve redove koji imaju prazne kategorije transakcija.</span><span class="sxs-lookup"><span data-stu-id="f454a-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="f454a-150">Ovaj zadatak je obavezan, bez obzira na to da li koristite podrazumevani predložak ili kreirate sopstveni predložak.</span><span class="sxs-lookup"><span data-stu-id="f454a-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="f454a-151">Ovaj filter uklanja sve redove rezimea iz usluge Project Service Automation koji mogu prouzrokovati netačna predviđanja radnih sati u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="f454a-152">Izaberite vezu **Napredni upit i filtriranje** da filtrirate prazne zapise u koloni **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="f454a-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f454a-153">Mapiranje predložaka u usluzi Data Integration</span><span class="sxs-lookup"><span data-stu-id="f454a-153">Template mapping in Data integration</span></span>

<span data-ttu-id="f454a-154">Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration.</span><span class="sxs-lookup"><span data-stu-id="f454a-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="f454a-155">Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f454a-156">[![Mapiranje zadataka predložaka u usluzi Data Integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f454a-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="f454a-157">Procene troškova projekta</span><span class="sxs-lookup"><span data-stu-id="f454a-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="f454a-158">Predlošci i zadaci</span><span class="sxs-lookup"><span data-stu-id="f454a-158">Template and tasks</span></span>

<span data-ttu-id="f454a-159">Sledeći predložak i osnovni zadaci koji se koriste za sinhronizaciju procena troškova iz usluge Project Service Automation u Finance:</span><span class="sxs-lookup"><span data-stu-id="f454a-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="f454a-160">**Naziv predloška u Integraciji podataka:** Procene troškova projekta (iz PSA u Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="f454a-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="f454a-161">**Naziv zadataka u projektu:**</span><span class="sxs-lookup"><span data-stu-id="f454a-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="f454a-162">Odnosi između transakcija</span><span class="sxs-lookup"><span data-stu-id="f454a-162">Transaction relationships</span></span> 
    - <span data-ttu-id="f454a-163">Procene troškova</span><span class="sxs-lookup"><span data-stu-id="f454a-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="f454a-164">Skup entiteta</span><span class="sxs-lookup"><span data-stu-id="f454a-164">Entity set</span></span>

| <span data-ttu-id="f454a-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f454a-165">Project Service Automation</span></span> | <span data-ttu-id="f454a-166">Finance</span><span class="sxs-lookup"><span data-stu-id="f454a-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="f454a-167">Veze transakcija</span><span class="sxs-lookup"><span data-stu-id="f454a-167">Transaction Connections</span></span>    | <span data-ttu-id="f454a-168">Entitet integracije za odnose transakcija projekta</span><span class="sxs-lookup"><span data-stu-id="f454a-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="f454a-169">Stavke procene</span><span class="sxs-lookup"><span data-stu-id="f454a-169">Estimate Lines</span></span>             | <span data-ttu-id="f454a-170">Entitet integracije za procene troškova projekta</span><span class="sxs-lookup"><span data-stu-id="f454a-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="f454a-171">Tok entiteta</span><span class="sxs-lookup"><span data-stu-id="f454a-171">Entity flow</span></span>

<span data-ttu-id="f454a-172">Procenama troškova se upravlja u usluzi Project Service Automation i one se sinhronizuju sa uslugom Finance kao predviđanja troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="f454a-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f454a-173">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="f454a-173">Prerequisites</span></span>

<span data-ttu-id="f454a-174">Da bi mogla da se izvrši sinhronizacija procena troškova projekta, morate sinhronizovati projekte, projektne zadatke i kategorije transakcija troškova projekta.</span><span class="sxs-lookup"><span data-stu-id="f454a-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="f454a-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="f454a-175">Power Query</span></span>

<span data-ttu-id="f454a-176">U predlošku za procenu troškova projekta morate da koristite Power Query da biste izvršili sledeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="f454a-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="f454a-177">Filtrirajte da biste uključili samo zapise linija procene troškova.</span><span class="sxs-lookup"><span data-stu-id="f454a-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="f454a-178">Postavite ID podrazumevanog modela predviđanja koji će se koristiti kada integracija kreira nova predviđanja sati.</span><span class="sxs-lookup"><span data-stu-id="f454a-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="f454a-179">Transformišite vrste naplate.</span><span class="sxs-lookup"><span data-stu-id="f454a-179">Transform the billing types.</span></span>
- <span data-ttu-id="f454a-180">Transformišite vrste transakcija.</span><span class="sxs-lookup"><span data-stu-id="f454a-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="f454a-181">Filtrirajte da biste uključili samo linije procene troškova</span><span class="sxs-lookup"><span data-stu-id="f454a-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="f454a-182">Predložak za procenu troškova projekta (iz PSA u Fin and Ops) ima podrazumevani filter koji uključuje samo linije troškova u integraciji.</span><span class="sxs-lookup"><span data-stu-id="f454a-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="f454a-183">Ako kreirate sopstveni obrazac, morate dodati ovaj filter.</span><span class="sxs-lookup"><span data-stu-id="f454a-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="f454a-184">Izaberite zadatak **Odnosi između transakcija**, a zatim kliknite na strelicu **Mapa** da biste otvorili mapiranje.</span><span class="sxs-lookup"><span data-stu-id="f454a-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f454a-185">Izaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="f454a-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="f454a-186">Filtrirajte kolonu **msdyn\_transactiontype1** kolona tako da uključuje samo **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="f454a-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="f454a-187">Podesite podrazumevani ID modela predviđanja</span><span class="sxs-lookup"><span data-stu-id="f454a-187">Set the default forecast model ID</span></span>

<span data-ttu-id="f454a-188">Da biste ažurirali podrazumevani ID modela predviđanja u predlošku, izaberite zadatak **Procene troškova**, a zatim kliknite na strelicu **Mapiraj** da biste otvorili mapiranje.</span><span class="sxs-lookup"><span data-stu-id="f454a-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="f454a-189">Izaberite vezu **Napredni upit i filtriranje**.</span><span class="sxs-lookup"><span data-stu-id="f454a-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="f454a-190">Ako koristite podrazumevani predložak procene troškova projekta (iz PSA u Fin and Ops), u usluzi Power Query izaberite **Uslov umetanja** u odeljku **Primenjeni koraci**.</span><span class="sxs-lookup"><span data-stu-id="f454a-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="f454a-191">U stavci **Funkcija**, zamenite **O\_forecast** nazivom ID-a modela predviđanja koji treba koristiti uz integraciju.</span><span class="sxs-lookup"><span data-stu-id="f454a-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="f454a-192">Podrazumevani predložak sadrži ID modela predviđanja iz demo podataka.</span><span class="sxs-lookup"><span data-stu-id="f454a-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="f454a-193">Ako kreirate novi obrazac, morate dodati ovu kolonu.</span><span class="sxs-lookup"><span data-stu-id="f454a-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="f454a-194">U usluzi Power Query izaberite **Dodaj uslovnu kolonu** i unesite naziv za novu kolonu, kao što je **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="f454a-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="f454a-195">Unesite uslov za kolonu, gde, ako ID linije procene nije bez vrednosti, onda \<enter the forecast model ID\>; u suprotnom je bez vrednosti.</span><span class="sxs-lookup"><span data-stu-id="f454a-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="f454a-196">Transformisanje vrsta naplate</span><span class="sxs-lookup"><span data-stu-id="f454a-196">Transform the billing types</span></span>

<span data-ttu-id="f454a-197">Predložak procene troškova projekta (iz PSA u Fin and Ops) uključuje uslovnu kolonu koja se koristi za transformisanje tipova naplate koji su primljeni iz usluge Project Service Automation tokom integracije.</span><span class="sxs-lookup"><span data-stu-id="f454a-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f454a-198">Ako kreirate sopstveni obrazac, morate dodati ovu uslovnu kolonu.</span><span class="sxs-lookup"><span data-stu-id="f454a-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f454a-199">Izaberite vezu **Napredni upit i filtriranje**, a zatim izaberite **Dodaj uslovnu kolonu**.</span><span class="sxs-lookup"><span data-stu-id="f454a-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f454a-200">Unesite ime za novu kolonu, kao što je **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="f454a-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="f454a-201">Zatim unesite sledeći uslov:</span><span class="sxs-lookup"><span data-stu-id="f454a-201">Then enter the following condition:</span></span>

<span data-ttu-id="f454a-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="f454a-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="f454a-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="f454a-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="f454a-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="f454a-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="f454a-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="f454a-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="f454a-206">Transformisanje vrsta transakcija</span><span class="sxs-lookup"><span data-stu-id="f454a-206">Transform the transaction types</span></span>

<span data-ttu-id="f454a-207">Predložak procene troškova projekta (iz PSA u Fin and Ops) uključuje uslovnu kolonu koja se koristi za transformisanje vrsta transakcija koje su primljene iz usluge Project Service Automation tokom integracije.</span><span class="sxs-lookup"><span data-stu-id="f454a-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="f454a-208">Ako kreirate sopstveni obrazac, morate dodati ovu uslovnu kolonu.</span><span class="sxs-lookup"><span data-stu-id="f454a-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="f454a-209">Izaberite vezu **Napredni upit i filtriranje**, a zatim izaberite **Dodaj uslovnu kolonu**.</span><span class="sxs-lookup"><span data-stu-id="f454a-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="f454a-210">Unesite naziv za novu kolonu, kao što je **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="f454a-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="f454a-211">Zatim unesite sledeći uslov:</span><span class="sxs-lookup"><span data-stu-id="f454a-211">Then enter the following condition:</span></span>

<span data-ttu-id="f454a-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="f454a-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="f454a-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="f454a-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="f454a-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="f454a-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="f454a-215">Mapiranje predložaka u usluzi Data Integration</span><span class="sxs-lookup"><span data-stu-id="f454a-215">Template mapping in Data integration</span></span>

<span data-ttu-id="f454a-216">Sledeće ilustracije prikazuju primere mapiranja zadataka predloška u usluzi Data Integration.</span><span class="sxs-lookup"><span data-stu-id="f454a-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="f454a-217">Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="f454a-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="f454a-218">[![Predložak mapiranja transakcija procene troškova](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f454a-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="f454a-219">[![Predložak mapiranja procena troškova](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="f454a-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]