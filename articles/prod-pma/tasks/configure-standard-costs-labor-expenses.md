---
title: Konfigurisanje standardne cene rada i troškova
description: Ova tema objašnjava kako da postavite standardnu cenu rada i troškove projekta.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083637"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="8b530-103">Konfigurisanje standardne cene rada i troškova</span><span class="sxs-lookup"><span data-stu-id="8b530-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b530-104">Ova tema objašnjava kako da postavite standardnu cenu rada i troškove projekta.</span><span class="sxs-lookup"><span data-stu-id="8b530-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="8b530-105">Ovaj zadatke koristi USSI skup podataka.</span><span class="sxs-lookup"><span data-stu-id="8b530-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8b530-106">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Cena koštanja (sat)**.</span><span class="sxs-lookup"><span data-stu-id="8b530-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="8b530-107">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8b530-107">Select **New**.</span></span>
3. <span data-ttu-id="8b530-108">U polje **Važeći datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="8b530-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="8b530-109">U polje **Cena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="8b530-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8b530-110">Možete da podesite standardnu cenu koštanja za kategoriju projekta ili možete postaviti cenu koštanja prema broju radnika, broju projekta, kategoriji, datumu ili bilo kojoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="8b530-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="8b530-111">Cena koštanja koja se primenjuje je cena koštanja sa najvišim nivoom detalja.</span><span class="sxs-lookup"><span data-stu-id="8b530-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="8b530-112">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="8b530-112">Select **Save**.</span></span>
6. <span data-ttu-id="8b530-113">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Prodajna cena (sat)**.</span><span class="sxs-lookup"><span data-stu-id="8b530-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="8b530-114">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8b530-114">Select **New**.</span></span>
8. <span data-ttu-id="8b530-115">U polje **Važeći datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="8b530-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="8b530-116">U polju **Rok važenja** izaberite opciju.</span><span class="sxs-lookup"><span data-stu-id="8b530-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="8b530-117">U polje **Cena** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="8b530-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8b530-118">Možete da postavite standardnu prodajnu cenu za transakcije po satu ili za kategoriju projekta.</span><span class="sxs-lookup"><span data-stu-id="8b530-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="8b530-119">Takođe možete da podesite prodajne cene prema broju radnika, broju projekta, kategoriji, datumu transakcije ili bilo kojoj njihovoj kombinaciji.</span><span class="sxs-lookup"><span data-stu-id="8b530-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="8b530-120">Stvarna prodajna cena, koja se primenjuje kada radnik unosi transakciju u dnevnik časova, jeste prodajna cena sa najvišim nivoom detalja.</span><span class="sxs-lookup"><span data-stu-id="8b530-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8b530-121">Na primer, ako su postavljene i opšta prodajna cena i prodajna cena specifična za radnika, koristi se prodajna cena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="8b530-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="8b530-122">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="8b530-122">Select **Save**.</span></span>
12. <span data-ttu-id="8b530-123">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="8b530-123">Close the page.</span></span>
13. <span data-ttu-id="8b530-124">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Cena koštanja (trošak)**.</span><span class="sxs-lookup"><span data-stu-id="8b530-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="8b530-125">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8b530-125">Select **New**.</span></span>
15. <span data-ttu-id="8b530-126">U polje **Važeći datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="8b530-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="8b530-127">U polje **Cena koštanja** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="8b530-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8b530-128">Može se popuniti više polja, ali ovo je minimum potreban za čuvanje zapisa.</span><span class="sxs-lookup"><span data-stu-id="8b530-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="8b530-129">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="8b530-129">Select **Save**.</span></span>
18. <span data-ttu-id="8b530-130">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Prodajna cena (trošak)**.</span><span class="sxs-lookup"><span data-stu-id="8b530-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="8b530-131">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="8b530-131">Select **New**.</span></span>
20. <span data-ttu-id="8b530-132">U polje **Važeći datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="8b530-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="8b530-133">U polju **Rok važenja** izaberite opciju.</span><span class="sxs-lookup"><span data-stu-id="8b530-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="8b530-134">U polje **Cena** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="8b530-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8b530-135">Stvarna prodajna cena, koja se primenjuje kada radnik unosi transakcije u dnevnik troškova, jeste prodajna cena sa najvišim nivoom detalja.</span><span class="sxs-lookup"><span data-stu-id="8b530-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8b530-136">Na primer, ako su postavljene i opšta prodajna cena i prodajna cena specifična za radnika, koristi se prodajna cena specifična za radnika.</span><span class="sxs-lookup"><span data-stu-id="8b530-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="8b530-137">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="8b530-137">Select **Save**.</span></span>

