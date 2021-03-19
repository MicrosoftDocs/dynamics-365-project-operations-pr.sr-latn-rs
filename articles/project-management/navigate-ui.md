---
title: Kretanje kroz korisnički interfejs
description: Ova tema pruža informacije o upravljanju projektima u usluzi Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286760"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="70416-103">Kretanje kroz korisnički interfejs</span><span class="sxs-lookup"><span data-stu-id="70416-103">Navigating the user interface</span></span>

<span data-ttu-id="70416-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="70416-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="70416-105">Pregled</span><span class="sxs-lookup"><span data-stu-id="70416-105">Overview</span></span>

<span data-ttu-id="70416-106">Glavni obrazac projekta je podeljen na nekoliko kartica.</span><span class="sxs-lookup"><span data-stu-id="70416-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="70416-107">Svaka kartica predstavlja različiti nivo detalja u projektu.</span><span class="sxs-lookup"><span data-stu-id="70416-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="70416-108">**Rezime**: Pruža opis projekta i objedinjuje planirane i stvarne performanse projekta.</span><span class="sxs-lookup"><span data-stu-id="70416-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Kartica i polja rezimea](media/navigation7.png)

- <span data-ttu-id="70416-110">**Zadaci**: Pruža detalje u vezi sa strukturnom analizom posla predstavljenom prikazom mreže, prikazom table i gantogramom.</span><span class="sxs-lookup"><span data-stu-id="70416-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Kartica i polja zadatka](media/navigation8.png)

- <span data-ttu-id="70416-112">**Tim**: Pruža detalje u vezi sa učesnicima u projektu.</span><span class="sxs-lookup"><span data-stu-id="70416-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="70416-113">Dodeljena angažovanja svakog člana tima takođe su rezimirana u ovom prikazu.</span><span class="sxs-lookup"><span data-stu-id="70416-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Kartica i polja tima](media/navigation9.png)

- <span data-ttu-id="70416-115">**Dodeljivanje resursa**: Pruža prikaz u vremenu angažovanja za svaki resurs na projektu.</span><span class="sxs-lookup"><span data-stu-id="70416-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Kartica i polja za dodeljivanje resursa](media/navigation10.png)

- <span data-ttu-id="70416-117">**Izmirenje resursa**: Pruža prikaz u vremenu razlika između dodeljivanja svakog imenovanog resursa i njihovih rezervacija.</span><span class="sxs-lookup"><span data-stu-id="70416-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Kartica i polja za sravnjenja resursa](media/navigation11.png)

- <span data-ttu-id="70416-119">**Procene**: Pruža prikaz u vremenu troškova i procene prodaje projekta.</span><span class="sxs-lookup"><span data-stu-id="70416-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Kartica i polja procena](media/navigation12.png)

- <span data-ttu-id="70416-121">**Praćenje**: Pruža prikaz koji pokazuje napredak zadataka u strukturnoj analizi posla za angažovanje, troškove i prodaju.</span><span class="sxs-lookup"><span data-stu-id="70416-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Kartica i polja praćenja](media/navigation13.png)

- <span data-ttu-id="70416-123">**Prodaja**: Pruža duboke veze do ponuda i ugovora povezanih sa projektom.</span><span class="sxs-lookup"><span data-stu-id="70416-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="70416-124">**Procene troškova**: Pruža mrežu koja definiše troškove projekta na osnovu kategorija organizacionih troškova.</span><span class="sxs-lookup"><span data-stu-id="70416-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Kartica i polja procena troškova](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="70416-126">Kontrole mreže</span><span class="sxs-lookup"><span data-stu-id="70416-126">Grid controls</span></span>

<span data-ttu-id="70416-127">Sledi kratak pregled tipičnih kontrola koje se nalaze na različitim karticama za planiranje projekata.</span><span class="sxs-lookup"><span data-stu-id="70416-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="70416-128">Osveži</span><span class="sxs-lookup"><span data-stu-id="70416-128">Refresh</span></span>

<span data-ttu-id="70416-129">**Osveži**: Vraća najnovije podatke sa servera ako je došlo do bilo kakvih promena nakon učitavanja mreže.</span><span class="sxs-lookup"><span data-stu-id="70416-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Dugme „Osveži“](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="70416-131">Grupiši prema</span><span class="sxs-lookup"><span data-stu-id="70416-131">Group by</span></span>

<span data-ttu-id="70416-132">**Grupiši po**: Ažurira grupisanje redova u mreži tako da odražava resurse, uloge ili kategorije na osnovu potreba korisnika.</span><span class="sxs-lookup"><span data-stu-id="70416-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Dugme „Grupiši po“](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="70416-134">Prethodno/Sledeće</span><span class="sxs-lookup"><span data-stu-id="70416-134">Previous/Next</span></span>

<span data-ttu-id="70416-135">**Prethodno**/**Sledeće**: Ažurirajte vidljive vremenske periode na mrežama vremenskih podataka.</span><span class="sxs-lookup"><span data-stu-id="70416-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Dugmad Prethodno i Sledeće](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="70416-137">Vremenska skala</span><span class="sxs-lookup"><span data-stu-id="70416-137">Timescale</span></span>

<span data-ttu-id="70416-138">**Vremenska skala**: Promenite objedinjavanje vremenskih podataka između dana, nedelja, meseci i godina.</span><span class="sxs-lookup"><span data-stu-id="70416-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Dugme „Vremenska skala“](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="70416-140">Razvij</span><span class="sxs-lookup"><span data-stu-id="70416-140">Expand</span></span>

<span data-ttu-id="70416-141">**Proširi**: Prikažite vidljivu mrežu na celom ekranu pružajući više mogućnosti da vidite dodatne uloge.</span><span class="sxs-lookup"><span data-stu-id="70416-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Dugme „Razvij“](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="70416-143">Prikaz u vremenu prema</span><span class="sxs-lookup"><span data-stu-id="70416-143">Time-phase by</span></span>

<span data-ttu-id="70416-144">**Prikaz u vremenu prema**: Ažurirajte grupisanje redova u mreži kako bi se odrazile procene troškova za procene prodaje.</span><span class="sxs-lookup"><span data-stu-id="70416-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="70416-145">Ova kontrola se takođe odnosi na skriptu procene i mrežu praćenja.</span><span class="sxs-lookup"><span data-stu-id="70416-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Dugme „Prikaz u vremenu prema“](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="70416-147">Dodaj kolonu</span><span class="sxs-lookup"><span data-stu-id="70416-147">Add column</span></span>

<span data-ttu-id="70416-148">**Dodaj kolonu**: Omogućava korisniku da definiše vidljive kolone u mreži.</span><span class="sxs-lookup"><span data-stu-id="70416-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="70416-149">Samo unapred pripremljene kolone se mogu dodati u mreže u obrascu **Projektno planiranje**.</span><span class="sxs-lookup"><span data-stu-id="70416-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Dugme „Dodaj kolonu“](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]