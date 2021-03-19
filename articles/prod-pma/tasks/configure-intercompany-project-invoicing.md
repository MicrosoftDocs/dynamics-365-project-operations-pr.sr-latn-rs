---
title: Konfigurisanje fakturisanja međukompanijskih projekata
description: Ova tema pokazuje kako da podesite fakturisanje projekata između dve kompanije u vašoj organizaciji.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288396"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="0a612-103">Konfigurisanje fakturisanja međukompanijskih projekata</span><span class="sxs-lookup"><span data-stu-id="0a612-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a612-104">Ova tema pokazuje kako da podesite fakturisanje projekata između dve kompanije u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0a612-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="0a612-105">Ovaj zadatke koristi USSI skup podataka.</span><span class="sxs-lookup"><span data-stu-id="0a612-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="0a612-106">U oknu za navigaciju idite na **Moduli > Dugovanja > Prodavci > Svi prodavci**.</span><span class="sxs-lookup"><span data-stu-id="0a612-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="0a612-107">Na listi **Svi prodavci** pronađite i izaberite željeni zapis.</span><span class="sxs-lookup"><span data-stu-id="0a612-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="0a612-108">U oknu radnji izaberite **Opšti podaci**.</span><span class="sxs-lookup"><span data-stu-id="0a612-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="0a612-109">Izaberite **Međukompanijski**.</span><span class="sxs-lookup"><span data-stu-id="0a612-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="0a612-110">Podesite **Aktivno** na **Da** kako bi se omogućilo međukompanijsko trgovanje.</span><span class="sxs-lookup"><span data-stu-id="0a612-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="0a612-111">U polje **Kompanija klijenta** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="0a612-112">U polje **Moj poslovni kontakt** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="0a612-113">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="0a612-113">Select **Save**.</span></span>
9. <span data-ttu-id="0a612-114">Zatvorite stranice da biste se vratili na početnu stranicu.</span><span class="sxs-lookup"><span data-stu-id="0a612-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="0a612-115">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Parametri upravljanja projektima i računovodstvom**.</span><span class="sxs-lookup"><span data-stu-id="0a612-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="0a612-116">Izaberite karticu **Međukompanijski**.</span><span class="sxs-lookup"><span data-stu-id="0a612-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="0a612-117">Pomerite klizač na **Da** kako bi se omogućilo međukompanijsko raspoređivanje resursa i vremenski rasporedi.</span><span class="sxs-lookup"><span data-stu-id="0a612-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="0a612-118">Označite izabrani red na listi.</span><span class="sxs-lookup"><span data-stu-id="0a612-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0a612-119">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0a612-119">Select **New**.</span></span>
15. <span data-ttu-id="0a612-120">U polje **Pravno lice zajmoprimac** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="0a612-121">Izaberite polje za potvrdu **Pripadajući prihod**.</span><span class="sxs-lookup"><span data-stu-id="0a612-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="0a612-122">U polje **Podrazumevana kategorija vremenskog rasporeda** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="0a612-123">U polje **Podrazumevana kategorija troška** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="0a612-124">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="0a612-124">Select **Save**.</span></span>
20. <span data-ttu-id="0a612-125">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="0a612-125">Close the page.</span></span>
21. <span data-ttu-id="0a612-126">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Knjiženje > Podešavanje knjiženja u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="0a612-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="0a612-127">U polju **Vrste računa glavne knjige**, izaberite opciju.</span><span class="sxs-lookup"><span data-stu-id="0a612-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="0a612-128">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0a612-128">Select **New**.</span></span>
24. <span data-ttu-id="0a612-129">U polju **Glavni račun** novog reda, navedite željene vrednosti.</span><span class="sxs-lookup"><span data-stu-id="0a612-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="0a612-130">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="0a612-130">Select **Save**.</span></span>
26. <span data-ttu-id="0a612-131">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="0a612-131">Close the page.</span></span>
27. <span data-ttu-id="0a612-132">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Podešavanje > Cene > Cena transfera**.</span><span class="sxs-lookup"><span data-stu-id="0a612-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="0a612-133">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="0a612-133">Select **New**.</span></span>
29. <span data-ttu-id="0a612-134">U polje **Važeći datum** unesite datum.</span><span class="sxs-lookup"><span data-stu-id="0a612-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="0a612-135">U polje **Pravno lice zajmoprimac** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="0a612-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="0a612-136">U polju **Model cene transfera** izaberite opciju.</span><span class="sxs-lookup"><span data-stu-id="0a612-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="0a612-137">U polje **Cena** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="0a612-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="0a612-138">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="0a612-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]