---
title: Pregled usluge Project Service Automation
description: Ova tema pruža informacije o rešenju za integraciju usluge Dynamics 365 Project Service Automation sa uslugom Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083721"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="1265a-103">Pregled usluge Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1265a-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1265a-104">Rešenje za integraciju iz Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Dynamics 365 Finance i Dynamics 365 Project Service Automation preko usluge Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="1265a-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="1265a-105">Predlošci integracije koji su dostupni sa funkcijom Integracija podataka omogućavaju tok projekata, ugovore o projektu, predmete ugovora o projektu, kontrolne tačke predmeta ugovora o projektu, projektne zadatke, kategorije transakcija troškova, procene sati i procene troškova iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="1265a-106">Ako koristite verziju 7.3.0, morate instalirati KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="1265a-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="1265a-107">Tada ćete moći da integrišete projekte sa fiksnom cenom.</span><span class="sxs-lookup"><span data-stu-id="1265a-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="1265a-108">Ako koristite verziju 7.3.0, a transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati KB 4345320 da biste te naknade uključili u fakturu projekta.</span><span class="sxs-lookup"><span data-stu-id="1265a-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="1265a-109">Ako koristite verziju 8.0, moći ćete da koristite integraciju projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="1265a-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="1265a-110">Ako koristite verziju 8.0.1 ili noviju, moći ćete da sinhronizujete aktuelne podatke.</span><span class="sxs-lookup"><span data-stu-id="1265a-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="1265a-111">Da biste mogli da integrišete Project Service Automation Finance, morate konfigurisati parametre integracije usluge Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1265a-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="1265a-112">Za više informacija, pogledajte: [Integrisanje parametara usluge Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1265a-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="1265a-113">Ovo rešenje za integraciju omogućava direktnu sinhronizaciju u sledećim scenarijima:</span><span class="sxs-lookup"><span data-stu-id="1265a-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="1265a-114">Održavajte ugovore o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-115">Kreirajte projekte u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-116">Održavajte predmete ugovora o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-117">Održavajte kontrolne tačke predmeta ugovora o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-118">Održavajte projektne zadatke u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-119">Održavajte kategorije transakcija troškova u usluzi Finance i sinhronizujte ih direktno iz usluge Finance u Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="1265a-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="1265a-120">Kreirajte procene časova projekta u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-121">Kreirajte procene troškova projekta u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="1265a-122">Kreirajte aktuelne podatke o vremenu, troškovima i naknadama u usluzi Project Service Automation i kreirajte projektne transakcije u dnevniku Project Service Automation integracije tako da mogu biti proknjiženi u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="1265a-123">Sinhronizacija podataka</span><span class="sxs-lookup"><span data-stu-id="1265a-123">Data synchronization</span></span>

<span data-ttu-id="1265a-124">Sledeća ilustracija prikazuje kako se podaci sinhronizuju kao deo integracije između usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="1265a-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="1265a-125">Trenutno nisu dostupni svi predlošci.</span><span class="sxs-lookup"><span data-stu-id="1265a-125">Not all templates are currently available.</span></span> <span data-ttu-id="1265a-126">Predlošci će biti objavljeni po završetku.</span><span class="sxs-lookup"><span data-stu-id="1265a-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="1265a-127">[![Integracija usluge Project Service Automation sa uslugom Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="1265a-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="1265a-128">Sistemski zahtevi za Finance</span><span class="sxs-lookup"><span data-stu-id="1265a-128">System requirements for Finance</span></span>

<span data-ttu-id="1265a-129">Da biste koristili rešenje za integraciju usluge Project Service Automation u Finance, morate instalirati Enterprise Edition 7.3 sa ispravkom platforme 12 ili novijom.</span><span class="sxs-lookup"><span data-stu-id="1265a-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="1265a-130">Sistemski zahtevi za Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1265a-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="1265a-131">Da biste koristili rešenje za integraciju usluge Project Service Automation u Finance, morate instalirati sledeće komponente:</span><span class="sxs-lookup"><span data-stu-id="1265a-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="1265a-132">Dynamics 365 Project Service Automation verzija 9.0.0.0 ili novija</span><span class="sxs-lookup"><span data-stu-id="1265a-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="1265a-133">Moguće rešenje za gotovinu za Dynamics 365 Sales, verzija 1.14.0.0 (v14) ili novija</span><span class="sxs-lookup"><span data-stu-id="1265a-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="1265a-134">Rešenje Project Service Automation u Finance za Dynamics 365 Project Service Automation verzija 1.0.0.0 ili novija</span><span class="sxs-lookup"><span data-stu-id="1265a-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="1265a-135">Instaliranje rešenja za integraciju usluge Project Service Automation u Finance u vašoj instanci usluge Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="1265a-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="1265a-136">Preuzmite rešenje za integraciju Project Service Automation u Finance iz [Microsoft centra za preuzimanje](https://www.microsoft.com/download/details.aspx?id=57016) i sledite uputstva koja ste dobili uz rešenje.</span><span class="sxs-lookup"><span data-stu-id="1265a-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
