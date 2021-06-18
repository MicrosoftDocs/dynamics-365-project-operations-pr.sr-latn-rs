---
title: Sinhronizujte kategorije troškova projekta između usluga Finance and Operations i Project Service Automation
description: Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju kategorija zadataka projekta između usluga Microsoft Dynamics 365 Finance i Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999868"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="51eb4-103">Sinhronizujte kategorije troškova projekta između usluga Finance and Operations i Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51eb4-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="51eb4-104">Ova tema opisuje predloške i osnovne zadatke koji se koriste za sinhronizaciju kategorija zadataka projekta između usluga Dynamics 365 Finance i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="51eb4-105">Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="51eb4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="51eb4-106">Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.</span><span class="sxs-lookup"><span data-stu-id="51eb4-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="51eb4-107">Ako koristite Enterprise Edition 7.3.0, kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="51eb4-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="51eb4-108">Ako morate da resetujete računovodstvene distribucije, preporučujemo da instalirate i KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="51eb4-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="51eb4-109">Tok podataka za Project Service Automation i Finance</span><span class="sxs-lookup"><span data-stu-id="51eb4-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="51eb4-110">Rešenje za integraciju usluga Project Service Automation i Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="51eb4-111">Predlošci za integraciju koji su dostupni sa funkcijom Integracija podataka omogućava tok podataka o kategorijama projektnih zadataka između usluga Finance i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="51eb4-112">Ako se kategorije troškova projekta savladaju u usluzi Finance, tok integracije je prvi iz usluge Finance u Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="51eb4-113">ID-ovi integracije kategorija troškova projekta se zatim ažuriraju sinhronizacijom iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="51eb4-114">Ako se kategorije troškova projekta savladaju u usluzi Project Service Automation, tok integracije je prvi iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="51eb4-115">Kategorije projekata moraju već biti konfigurisane u usluzi Finance pre sinhronizacije iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="51eb4-116">Zatim sinhronizujte iz usluge Finance nazad u Project Service Automation, a zatim ponovo iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="51eb4-117">Na ovaj način garantujete da će se kategorije povezati i da se neće napraviti duplikati.</span><span class="sxs-lookup"><span data-stu-id="51eb4-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="51eb4-118">Kategorije troškova projekta obično se savladavaju u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="51eb4-119">Međutim, ako nije takav slučaj ili ako su kategorije troškova već kreirane u usluzi Project Service Automation, prvo morate sinhronizovati pomoću predloška kategorija transakcija troškova (iz PSA u Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="51eb4-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="51eb4-120">Zatim sinhronizujte pomoću predloška kategorija transakcija troškova projekta (iz Fin and Ops u PSA).</span><span class="sxs-lookup"><span data-stu-id="51eb4-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="51eb4-121">Zatim bi trebalo da još jednom pokrenete sinhronizaciju iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="51eb4-122">Ako prvo izvršite sinhronizaciju iz usluge Project Service Automation, u usluzi Finance moraju biti ispunjeni sledeći zahtevi:</span><span class="sxs-lookup"><span data-stu-id="51eb4-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="51eb4-123">Deljena kategorija koja se podudara sa kategorijom projekta koja je postavljena u usluzi Project Service Automation mora postojati i mora biti omogućena i za **Projekat** i za **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="51eb4-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="51eb4-124">Za svako pravno lice u usluzi Finance sa kojim se mora integrisati, moraju postojati sledeće kategorije projekata:</span><span class="sxs-lookup"><span data-stu-id="51eb4-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="51eb4-125">**Kategorija projekta** postoji.</span><span class="sxs-lookup"><span data-stu-id="51eb4-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="51eb4-126">**Koristi u trošku** je omogućeno.</span><span class="sxs-lookup"><span data-stu-id="51eb4-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="51eb4-127">**Aktivno u dnevniku** je omogućeno.</span><span class="sxs-lookup"><span data-stu-id="51eb4-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="51eb4-128">**Tip transakcije** je podešen na **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="51eb4-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="51eb4-129">Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="51eb4-130">[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="51eb4-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="51eb4-131">Sinhronizacija kategorije troškova projekta iz usluge Finance u Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51eb4-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="51eb4-132">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="51eb4-132">Template and task</span></span>

<span data-ttu-id="51eb4-133">Da biste pristupili predlošku, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za odabir javnih obrazaca.</span><span class="sxs-lookup"><span data-stu-id="51eb4-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="51eb4-134">Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju kategorija troškova projekta iz usluge Finance u Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="51eb4-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="51eb4-135">**Naziv predloška u usluzi Data Integration:** Kategorije transakcija troškova projekta (iz Fin and Ops u PSA)</span><span class="sxs-lookup"><span data-stu-id="51eb4-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="51eb4-136">**Naziv zadatka u projektu:** Sinhronizujte kategorije sa PSA</span><span class="sxs-lookup"><span data-stu-id="51eb4-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="51eb4-137">Skup entiteta</span><span class="sxs-lookup"><span data-stu-id="51eb4-137">Entity set</span></span>

| <span data-ttu-id="51eb4-138">Finance</span><span class="sxs-lookup"><span data-stu-id="51eb4-138">Finance</span></span>                           | <span data-ttu-id="51eb4-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51eb4-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="51eb4-140">Entitet integracije za kategorije</span><span class="sxs-lookup"><span data-stu-id="51eb4-140">Integration entity for categories</span></span> | <span data-ttu-id="51eb4-141">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="51eb4-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="51eb4-142">Tok entiteta</span><span class="sxs-lookup"><span data-stu-id="51eb4-142">Entity flow</span></span>

<span data-ttu-id="51eb4-143">Kategorijama projektnih zadataka se upravlja u usluzi Finance i oni se sinhronizuju sa uslugom Project Service Automation kao kategorija transakcija.</span><span class="sxs-lookup"><span data-stu-id="51eb4-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="51eb4-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="51eb4-144">Power Query</span></span>

<span data-ttu-id="51eb4-145">Kada se sinhronizujete sa uslugom Project Service Automation, morate da koristite Microsoft Power Query za Excel da biste postavili vrstu naplate za kategoriju transakcija.</span><span class="sxs-lookup"><span data-stu-id="51eb4-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="51eb4-146">Predložak kategorija transakcija troškova projekta (iz Fin and Ops u PSA) pružaju podrazumevanu kolonu i mapiranje.</span><span class="sxs-lookup"><span data-stu-id="51eb4-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="51eb4-147">Ako kreirate sopstveni predložak, morate dodati uslovnu kolonu u Power Query.</span><span class="sxs-lookup"><span data-stu-id="51eb4-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="51eb4-148">Pratite ove korake.</span><span class="sxs-lookup"><span data-stu-id="51eb4-148">Follow these steps.</span></span>

1. <span data-ttu-id="51eb4-149">Kliknite na strelicu da biste otvorili mapiranje zadatka kategorija projektnih troškova u predlošku kategorija transakcija troškova projekta (iz Fin and Ops u PSA).</span><span class="sxs-lookup"><span data-stu-id="51eb4-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="51eb4-150">Kliknite na vezu **Napredni upit i filtriranje** da biste otvorili Power Query.</span><span class="sxs-lookup"><span data-stu-id="51eb4-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="51eb4-151">Izaberite **Dodaj uslovnu kolonu**.</span><span class="sxs-lookup"><span data-stu-id="51eb4-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="51eb4-152">Unesite ime za novu kolonu, kao što je **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="51eb4-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="51eb4-153">Unesite sledeći uslov: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="51eb4-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="51eb4-154">Kliknite na **U redu** na koloni.</span><span class="sxs-lookup"><span data-stu-id="51eb4-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="51eb4-155">Obavezno mapirajte ovu novu kolonu na stranicu za mapiranje.</span><span class="sxs-lookup"><span data-stu-id="51eb4-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="51eb4-156">Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration.</span><span class="sxs-lookup"><span data-stu-id="51eb4-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="51eb4-157">Mapiranje prikazuje informacije o polju koje će se sinhronizovati iz usluge Finance u Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="51eb4-158">[![Mapiranje kategorije troškova projekta sa Project Service Automation predloškom](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="51eb4-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="51eb4-159">Sinhronizacija kategorije troškova projekta iz usluge Project Service Automation u Finance</span><span class="sxs-lookup"><span data-stu-id="51eb4-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="51eb4-160">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="51eb4-160">Template and task</span></span>

<span data-ttu-id="51eb4-161">Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju kategorija troškova projekta iz usluge Project Service Automation u Finance:</span><span class="sxs-lookup"><span data-stu-id="51eb4-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="51eb4-162">**Naziv predloška u usluzi Data Integration:** Kategorije transakcija troškova projekta (iz PSA u Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="51eb4-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="51eb4-163">**Naziv zadatka u projektu:** Sinhronizujte kategorije sa Fin Ops</span><span class="sxs-lookup"><span data-stu-id="51eb4-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="51eb4-164">Skup entiteta</span><span class="sxs-lookup"><span data-stu-id="51eb4-164">Entity set</span></span>

| <span data-ttu-id="51eb4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="51eb4-165">Project Service Automation</span></span> | <span data-ttu-id="51eb4-166">Finance</span><span class="sxs-lookup"><span data-stu-id="51eb4-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="51eb4-167">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="51eb4-167">Transaction categories</span></span>     | <span data-ttu-id="51eb4-168">Entitet integracije za kategorije</span><span class="sxs-lookup"><span data-stu-id="51eb4-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="51eb4-169">Tok entiteta</span><span class="sxs-lookup"><span data-stu-id="51eb4-169">Entity flow</span></span>

<span data-ttu-id="51eb4-170">Kategorijama projektnih zadataka se upravlja u usluzi Finance i oni se sinhronizuju sa uslugom Project Service Automation kao kategorija transakcija.</span><span class="sxs-lookup"><span data-stu-id="51eb4-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="51eb4-171">Povratna sinhronizacija u Finance ažurira kategoriju projekta u usluzi Finance sa ID-om integracije iz usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51eb4-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="51eb4-172">Mapiranje predložaka u usluzi Data Integration</span><span class="sxs-lookup"><span data-stu-id="51eb4-172">Template mapping in Data integration</span></span>

<span data-ttu-id="51eb4-173">Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u usluzi Data Integration.</span><span class="sxs-lookup"><span data-stu-id="51eb4-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="51eb4-174">Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="51eb4-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="51eb4-175">[![Mapiranje usluge Project Service Automation sa Finance predloškom](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="51eb4-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]