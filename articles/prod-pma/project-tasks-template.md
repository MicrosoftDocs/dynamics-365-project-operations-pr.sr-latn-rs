---
title: Sinhronizovanje projektnih zadataka direktno iz usluge Project Service Automation sa uslugom Finance and Operations
description: Ova tema opisuje predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Finance.
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
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288936"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="5b5a4-103">Sinhronizovanje projektnih zadataka direktno iz usluge Project Service Automation sa uslugom Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b5a4-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b5a4-104">Ova tema opisuje predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="5b5a4-105">Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="5b5a4-106">Ako koristite Enterprise Edition 7.3.0, kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="5b5a4-107">Ako morate da resetujete računovodstvene distribucije, preporučili smo da instalirate i KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="5b5a4-108">Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="5b5a4-109">Tok podataka iz usluge Project Service Automation u Finance</span><span class="sxs-lookup"><span data-stu-id="5b5a4-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="5b5a4-110">Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="5b5a4-111">Predložak za integraciju koji je dostupan sa funkcijom Integracija podataka omogućava tok podataka o projektnim zadacima iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5b5a4-112">Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="5b5a4-113">[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="5b5a4-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="5b5a4-114">Predložak i zadatak</span><span class="sxs-lookup"><span data-stu-id="5b5a4-114">Template and task</span></span>

<span data-ttu-id="5b5a4-115">Da biste pristupili predlošku, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za odabir javnih obrazaca.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5b5a4-116">Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka iz usluge Project Service Automation u Finance:</span><span class="sxs-lookup"><span data-stu-id="5b5a4-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="5b5a4-117">**Naziv predloška u Integraciji podataka:** Projektni zadaci (iz PSA u Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="5b5a4-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="5b5a4-118">**Naziv zadatka u projektu:** Projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="5b5a4-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="5b5a4-119">Da bi moglo da dođe do sinhronizacije projektnih zadataka, morate sinhronizovati ugovore o projektu i projekte.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5b5a4-120">Skup entiteta</span><span class="sxs-lookup"><span data-stu-id="5b5a4-120">Entity set</span></span>

| <span data-ttu-id="5b5a4-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5b5a4-121">Project Service Automation</span></span> | <span data-ttu-id="5b5a4-122">Finance</span><span class="sxs-lookup"><span data-stu-id="5b5a4-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="5b5a4-123">Projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="5b5a4-123">Project Tasks</span></span>              | <span data-ttu-id="5b5a4-124">Entitet integracije za projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="5b5a4-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5b5a4-125">Tok entiteta</span><span class="sxs-lookup"><span data-stu-id="5b5a4-125">Entity flow</span></span>

<span data-ttu-id="5b5a4-126">Projektnim zadacima se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao aktivnosti projekta.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="5b5a4-127">Preduslovi i podešavanje mapiranja</span><span class="sxs-lookup"><span data-stu-id="5b5a4-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="5b5a4-128">Da bi moglo da dođe do sinhronizacije projektnih zadataka, morate sinhronizovati ugovore o projektu i projekte.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="5b5a4-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="5b5a4-129">Power Query</span></span>

<span data-ttu-id="5b5a4-130">Morate koristiti Microsoft Power Query za Excel za filtriranje podataka ako je ispunjen ovaj uslov:</span><span class="sxs-lookup"><span data-stu-id="5b5a4-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="5b5a4-131">U projektnom zadatku imate zapise specifične za resurse.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="5b5a4-132">Ako morate da koristite Power Query, sledite ove smernice:</span><span class="sxs-lookup"><span data-stu-id="5b5a4-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="5b5a4-133">Predložak projektnih zadataka (iz PSA u Fin and Ops) ima podrazumevani filter koji iz projektnog zadatka isključuje zapise specifične za resurse postavljanjem filtera na **IsLineTask** na **Netačno**.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="5b5a4-134">Ako kreirate sopstveni obrazac, morate dodati ovaj filter.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5b5a4-135">Mapiranje predložaka u usluzi Data Integration</span><span class="sxs-lookup"><span data-stu-id="5b5a4-135">Template mapping in Data integration</span></span>

<span data-ttu-id="5b5a4-136">Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u integraciji podataka.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="5b5a4-137">Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.</span><span class="sxs-lookup"><span data-stu-id="5b5a4-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="5b5a4-138">[![Mapiranje predložaka](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="5b5a4-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]