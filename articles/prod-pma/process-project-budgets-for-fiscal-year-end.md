---
title: Prenos budžeta projekata na kraj fiskalne godine
description: Ovaj članak daje informacije o tome kako preneti preostale iznose budžeta u buduće godine i stvoriti detalje budžetskog registra.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289746"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="c1319-103">Prenos budžeta projekata na kraj fiskalne godine</span><span class="sxs-lookup"><span data-stu-id="c1319-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1319-104">Kada radite na višegodišnjem projektu, možda ćete imati preostali budžet na kraju fiskalne godine.</span><span class="sxs-lookup"><span data-stu-id="c1319-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="c1319-105">Preostale iznose budžeta možete preneti u buduću godinu i stvoriti detalje registra budžeta za iznose na povezanim računima glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="c1319-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="c1319-106">Pre nego što prenesete preostale iznose, pregledajte i analizirajte preostale iznose budžeta.</span><span class="sxs-lookup"><span data-stu-id="c1319-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="c1319-107">Pregledajte i analizirajte preostale iznose budžeta</span><span class="sxs-lookup"><span data-stu-id="c1319-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="c1319-108">Dovršite sledeće korake da biste pregledali iznose budžeta na kraju godine za projekte, ali ne i da biste ih preneli dalje.</span><span class="sxs-lookup"><span data-stu-id="c1319-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="c1319-109">Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**.</span><span class="sxs-lookup"><span data-stu-id="c1319-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c1319-110">Na stranici **Proces prenosa budžeta projekta**, na kartici **Opcije za kraj godine**, potvrdite da opcija **Prenesite preostale iznose budžeta projekta** nije omogućena.</span><span class="sxs-lookup"><span data-stu-id="c1319-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="c1319-111">Na kartici **Parametri** u polju **Godina budžeta projekta** odaberite fiskalnu godinu za koju želite da vidite preostali iznos budžeta.</span><span class="sxs-lookup"><span data-stu-id="c1319-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="c1319-112">U polju **Početna fiskalna godina** odaberite fiskalnu godinu za koju želite da vidite preostali iznos budžeta.</span><span class="sxs-lookup"><span data-stu-id="c1319-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="c1319-113">U polju **Iz modela prognoze** izaberite **Preostali budžet**.</span><span class="sxs-lookup"><span data-stu-id="c1319-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="c1319-114">Da biste uključili projekte koji ispunjavaju izabrane kriterijume i nemaju preostali budžet, izaberite **Pokaži preostalu nulu**.</span><span class="sxs-lookup"><span data-stu-id="c1319-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="c1319-115">Na kartici **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima, a zatim izaberite **Obradi**.</span><span class="sxs-lookup"><span data-stu-id="c1319-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="c1319-116">Da biste dizajnirali upit baze podataka koji učitava određeni skup budžeta u okno, izaberite **Preuzimanje izabranih budžeta**.</span><span class="sxs-lookup"><span data-stu-id="c1319-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="c1319-117">Za više informacija o određenoj liniji u oknu odaberite liniju, a zatim izaberite **Prikaži detalje o budžetu** ili **Prikaži naloge**.</span><span class="sxs-lookup"><span data-stu-id="c1319-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="c1319-118">Prenesite preostale iznose budžeta</span><span class="sxs-lookup"><span data-stu-id="c1319-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="c1319-119">Kada obrađujete preostale iznose budžeta, možete da kreirate transakcije u glavnoj knjizi za iznose koje prenosite dalje.</span><span class="sxs-lookup"><span data-stu-id="c1319-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="c1319-120">Da biste kreirali transakcije glavne knjige, izvršite korake u odeljku [Prenesite budžetske iznose i kreirajte transakcije iz glavne knjige](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="c1319-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="c1319-121">Iznosi budžeta koji se prenose, prebacuju se na model predviđanja koji je izabran na stranici **Modeli predviđanja** kao model prognoze prenosa.</span><span class="sxs-lookup"><span data-stu-id="c1319-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="c1319-122">Prenesite budžetske iznose i kreirajte transakcije iz glavne knjige</span><span class="sxs-lookup"><span data-stu-id="c1319-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="c1319-123">Izaberite **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**.</span><span class="sxs-lookup"><span data-stu-id="c1319-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="c1319-124">Na stranici **Proces prenosa budžeta projekta** izaberite **Kraj godine**, a zatim omogućite **Prenesite preostale iznose budžeta projekta** i **Kreirajte unose u registru budžeta u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="c1319-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="c1319-125">Na kartici **Parametri**, u grupi polja **Parametri projekta** izaberite sledeće:</span><span class="sxs-lookup"><span data-stu-id="c1319-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="c1319-126">**Godina budžeta projekta**: Odaberite početak fiskalne godine za koju želite da vidite preostale iznose budžeta.</span><span class="sxs-lookup"><span data-stu-id="c1319-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="c1319-127">**Profit i gubitak**: Kreirajte transakcije dobiti i gubitka u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c1319-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="c1319-128">**WIP**: Kreirajte transakcije u toku (WIP) u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c1319-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="c1319-129">**Zarada**: Kreirajte transakcije raspodele zarada u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c1319-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="c1319-130">U grupi polja **Glavna knjiga** navedite sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="c1319-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="c1319-131">U polju **Početna fiskalna godina** odaberite fiskalnu godinu na koju želite da prenesete preostale iznose budžeta za projekte.</span><span class="sxs-lookup"><span data-stu-id="c1319-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="c1319-132">Podrazumevana vrednost je godinu dana nakon vrednosti u polju **Godina budžeta projekta**.</span><span class="sxs-lookup"><span data-stu-id="c1319-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="c1319-133">U polju **Period prenosa** odaberite period za koji želite da kreirate detalje budžetskog registra u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c1319-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="c1319-134">Ovo je obično prvi period početne fiskalne godine.</span><span class="sxs-lookup"><span data-stu-id="c1319-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="c1319-135">U grupi polja **Kopiranje iz/u** navedite sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="c1319-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="c1319-136">U polju **Iz modela prognoze** izaberite model predviđanja budžeta projekta povezan sa preostalim iznosima budžeta koje želite da prenesete za projekte.</span><span class="sxs-lookup"><span data-stu-id="c1319-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c1319-137">U polju **Ka modelu budžeta knjige** izaberite model budžeta knjige projekta povezan sa preostalim iznosima budžeta koje želite da prenesete u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="c1319-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="c1319-138">Izaberite **Prenesite valutu prodaje** da biste koristili valutu prodaje projekta za transakcije glavne knjige koje se kreiraju kada prenesete iznose budžeta za projekte.</span><span class="sxs-lookup"><span data-stu-id="c1319-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="c1319-139">Kada opcija nije izabrana, transakcije koriste računovodstvenu valutu.</span><span class="sxs-lookup"><span data-stu-id="c1319-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="c1319-140">Izaberite **Pokaži preostalu nulu** da biste uključili projekte koji nemaju preostali iznos budžeta, ali ispunjavaju ostale kriterijume koje odaberete u projektima prikazanim u donjem oknu.</span><span class="sxs-lookup"><span data-stu-id="c1319-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="c1319-141">Na kartici **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima.</span><span class="sxs-lookup"><span data-stu-id="c1319-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="c1319-142">Ako želite da dizajnirate upit baze podataka koji učitava određeni skup budžeta projekata u okno, izaberite **Preuzimanje izabranih budžeta**.</span><span class="sxs-lookup"><span data-stu-id="c1319-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="c1319-143">Za svaki projekat koji želite da obradite odaberite opciju na početku reda za projekat.</span><span class="sxs-lookup"><span data-stu-id="c1319-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="c1319-144">Da biste izabrali sve ili većinu projekata, izaberite potvrdni znak u gornjem levom uglu.</span><span class="sxs-lookup"><span data-stu-id="c1319-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="c1319-145">Da biste isključili obradu bilo kog projekta, uklonite oznaku za taj projekat.</span><span class="sxs-lookup"><span data-stu-id="c1319-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="c1319-146">Da biste prebacili preostale iznose budžeta za izabrane projekte na izabranu fiskalnu godinu i kreirali detalje budžetskog registra u glavnoj knjizi, izaberite **Obradi**.</span><span class="sxs-lookup"><span data-stu-id="c1319-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="c1319-147">Prenesite budžetske iznose bez kreiranja transakcija iz glavne knjige</span><span class="sxs-lookup"><span data-stu-id="c1319-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="c1319-148">Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Budžeti** > **Prenesi budžete**.</span><span class="sxs-lookup"><span data-stu-id="c1319-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="c1319-149">Na stranici **Proces prenosa budžeta projekta**, u polju **Opcije za kraj godine**, izaberite **Prenesite preostale iznose budžeta projekta**.</span><span class="sxs-lookup"><span data-stu-id="c1319-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="c1319-150">U grupi **Parametri** u polju **Godina budžeta projekta** odaberite fiskalnu godinu za koju želite da vidite preostale iznose budžeta.</span><span class="sxs-lookup"><span data-stu-id="c1319-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="c1319-151">U grupi **Kopiranje iz/u** navedite sledeće informacije:</span><span class="sxs-lookup"><span data-stu-id="c1319-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="c1319-152">U polju **Iz modela prognoze** izaberite model predviđanja budžeta projekta koji je povezan sa preostalim iznosima budžeta koje želite da prenesete za projekte.</span><span class="sxs-lookup"><span data-stu-id="c1319-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="c1319-153">Izaberite **Pokaži preostalu nulu** da biste uključili projekte koji nemaju preostali budžet, ali ispunjavaju druge izabrane kriterijume.</span><span class="sxs-lookup"><span data-stu-id="c1319-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="c1319-154">U grupi **Izaberite budžete** izaberite **Preuzmite sve budžete** da biste učitali sve budžete koji odgovaraju odabranim kriterijumima.</span><span class="sxs-lookup"><span data-stu-id="c1319-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="c1319-155">Da biste dizajnirali upit baze podataka koji učitava određeni skup budžeta projekata u okno, izaberite **Preuzimanje izabranih budžeta**.</span><span class="sxs-lookup"><span data-stu-id="c1319-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="c1319-156">Za svaki projekat koji želite da obradite odaberite opciju na početku reda za projekat.</span><span class="sxs-lookup"><span data-stu-id="c1319-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="c1319-157">Izaberite **Obradi** da biste preneli preostale iznose budžeta za odabrane projekte na izabranu fiskalnu godinu.</span><span class="sxs-lookup"><span data-stu-id="c1319-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]