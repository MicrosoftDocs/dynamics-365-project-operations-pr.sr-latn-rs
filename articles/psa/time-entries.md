---
title: Kreiranje stavki vremena
description: Ova tema pruža informacije o tome kako da kreirate stavke vremena.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999283"
---
# <a name="create-time-entries"></a><span data-ttu-id="75bf4-103">Kreiranje stavki vremena</span><span class="sxs-lookup"><span data-stu-id="75bf4-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="75bf4-104">U prethodnim verzijama aplikacije Dynamics 365 Project Service Automation, stavke vremena su unošene jednom nedeljno.</span><span class="sxs-lookup"><span data-stu-id="75bf4-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="75bf4-105">U verziji 3 aplikacije Project Service Automation, unose se svakodnevno.</span><span class="sxs-lookup"><span data-stu-id="75bf4-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="75bf4-106">Međutim, nakon što je kreirano nekoliko stavki, možete ih grupno kreirati ili kopirati.</span><span class="sxs-lookup"><span data-stu-id="75bf4-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="75bf4-107">Kreiranje stavke vremena</span><span class="sxs-lookup"><span data-stu-id="75bf4-107">Create a time entry</span></span>

<span data-ttu-id="75bf4-108">Sledite ove korake za kreiranje stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="75bf4-109">Na stranici **Stavke vremena** izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="75bf4-110">U dijalog **Brzo kreiranje stavke vremena** unesite trajanje stavke u minutima, satima ili danima.</span><span class="sxs-lookup"><span data-stu-id="75bf4-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="75bf4-111">Trajanje mora da se unese u nekom od ovih formata: *x* minuta, *x* sati ili *x* dana.</span><span class="sxs-lookup"><span data-stu-id="75bf4-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="75bf4-112">Sati i dani takođe mogu da se unose kao decimalne vrednosti, na primer *x.x* sati ili *x.x* dana.</span><span class="sxs-lookup"><span data-stu-id="75bf4-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="75bf4-113">Izaberite vrstu stavke vremena i projekat za koji je unosite.</span><span class="sxs-lookup"><span data-stu-id="75bf4-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="75bf4-114">U polju **Projektni zadatak** pronađite zadatak za ovu stavku.</span><span class="sxs-lookup"><span data-stu-id="75bf4-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="75bf4-115">Ako kreirate stavku vremena za zadatak koji nije dodeljen korisniku, u polju **Projektni zadatak** izaberite dugme **Pretraži**, odaberite **Promeni prikaz**, a zatim **Svi aktivni zadaci projekta** da biste videli listu svih zadataka.</span><span class="sxs-lookup"><span data-stu-id="75bf4-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="75bf4-116">Unesite opis, ako je potreban opis, a zatim izaberite **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="75bf4-117">Nakon što je stavka vremena kreirana i sačuvana, možete je urediti u mreži za stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="75bf4-118">Mreža za stavke vremena podržava dva formata:</span><span class="sxs-lookup"><span data-stu-id="75bf4-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="75bf4-119">Možete uneti stavke vremena u formatu **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="75bf4-120">Ovaj format se zatim pretvara u sate i decimalne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="75bf4-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="75bf4-121">Možete direktno uneti sate i decimalne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="75bf4-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="75bf4-122">Imajte na umu da decimalne vrednosti sata nisu minuti.</span><span class="sxs-lookup"><span data-stu-id="75bf4-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="75bf4-123">Stoga 1,5 sat predstavlja 1 sat i 30 minuta.</span><span class="sxs-lookup"><span data-stu-id="75bf4-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="75bf4-124">Isto pravilo važi za decimalne vrednosti dana.</span><span class="sxs-lookup"><span data-stu-id="75bf4-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="75bf4-125">Jedan dan ima 24 sata, pa 0,5 dana predstavlja 12 sati.</span><span class="sxs-lookup"><span data-stu-id="75bf4-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="75bf4-126">Grupno kreiranje stavki vremena</span><span class="sxs-lookup"><span data-stu-id="75bf4-126">Bulk create time entries</span></span>

<span data-ttu-id="75bf4-127">Nakon kreiranja nekoliko stavki vremena, možete ih kopirati da biste grupno kreirali dodatne stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="75bf4-128">Na stranici **Stavke vremena** izaberite **Kopiraj nedelju**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="75bf4-129">U grupi polja **Iz perioda** u poljima **Datum početka** i **Datum završetka** definišite opseg datuma iz kojeg treba kopirati stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="75bf4-130">U grupi polja **U period**, u okviru polja **Datum početka**, odredite datum za koji ćete kreirati stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="75bf4-131">Izaberite **Kopiraj** da biste kreirali kopiju stavki vremena koja odgovara danu u nedelji koji je naveden u grupi polja **U period**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="75bf4-132">Na primer, stavka vremena za ponedeljak iz prošle nedelje se kopira u ponedeljak one sedmice koja je navedena u grupi polja **U period**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="75bf4-133">Uvoz podataka za stavke vremena</span><span class="sxs-lookup"><span data-stu-id="75bf4-133">Import data for time entries</span></span>

<span data-ttu-id="75bf4-134">Možete da uvezete podatke iz rezervacija i zadataka za projekte.</span><span class="sxs-lookup"><span data-stu-id="75bf4-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="75bf4-135">Kada uvezete podatke, možete odrediti opseg datuma rezervacija za uvoz, a zatim eksplicitno odabrati rezervacije koje bi trebalo da budu kreirane kao stavke vremena **Radna verzija**.</span><span class="sxs-lookup"><span data-stu-id="75bf4-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="75bf4-136">Mogućnosti grupisanja prema, sortiranja, pretrage i filtriranja</span><span class="sxs-lookup"><span data-stu-id="75bf4-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="75bf4-137">Možete grupisati i filtrirati stavke vremena prema dimenzijama koje su navedene u kolonama.</span><span class="sxs-lookup"><span data-stu-id="75bf4-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="75bf4-138">U polju **Grupiraj prema** odaberite dimenziju za filtriranje stavki vremena.</span><span class="sxs-lookup"><span data-stu-id="75bf4-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="75bf4-139">Takođe možete sortirati zapise stavki vremena rastućim ili opadajućim redosledom koristeći strelicu za sortiranje u nazivima kolona.</span><span class="sxs-lookup"><span data-stu-id="75bf4-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="75bf4-140">Pored toga, stavke možete prikazati ili sakriti tako što ćete kliknuti na dugme **Filter** u nazivu kolone, a zatim u polje **Pretraga** uneti tekst koji treba da se koristi za pretragu stavki vremena prema nazivu projekta, projektnom zadatku, stavci vremena ili resursu.</span><span class="sxs-lookup"><span data-stu-id="75bf4-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]