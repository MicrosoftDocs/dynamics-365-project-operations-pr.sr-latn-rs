---
title: Šta je novo ili promenjeno u izdanju 25 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju 25 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280460"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="5e301-103">Šta je novo ili promenjeno u izdanju 25 ispravke Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="5e301-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5e301-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5e301-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5e301-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="5e301-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5e301-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5e301-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5e301-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="5e301-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="5e301-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5e301-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5e301-109">U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene za Project Service Automation verzije 3, izdanje 25 ispravke. Ova verzija ima broj verzije V 3.10.43.76 i postala je opšte dostupna putem samostalne ispravke u oktobru 2020.</span><span class="sxs-lookup"><span data-stu-id="5e301-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="5e301-110">Izdanje ispravke 25</span><span class="sxs-lookup"><span data-stu-id="5e301-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5e301-111">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="5e301-111">Bug fixes</span></span>

<span data-ttu-id="5e301-112">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="5e301-112">**Time and Expense**</span></span>

<span data-ttu-id="5e301-113">Sledeći problem je ispravljen:</span><span class="sxs-lookup"><span data-stu-id="5e301-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="5e301-114">Grafikon stavke vremena koji prikazuje dodatne podatke na osnovu prevelikog intervala koji se preuzima.</span><span class="sxs-lookup"><span data-stu-id="5e301-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="5e301-115">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="5e301-115">**Resource Management**</span></span>

<span data-ttu-id="5e301-116">Sledeći problem je ispravljen:</span><span class="sxs-lookup"><span data-stu-id="5e301-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="5e301-117">Dodat je Package Deployer kôd za preskakanje uvoza zakrpe za uslugu Universal Resource Scheduling ako zakrpa više verzije već postoji.</span><span class="sxs-lookup"><span data-stu-id="5e301-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="5e301-118">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="5e301-118">**Project Management**</span></span>

<span data-ttu-id="5e301-119">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="5e301-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="5e301-120">Ispravljene su razlike u zaokruživanju i kursnoj listi koje su dovodile do netačnih planiranih troškova u mreži za praćenje projekta.</span><span class="sxs-lookup"><span data-stu-id="5e301-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="5e301-121">Podrška mogućnosti prikazivanja dve ili više mreža za reakcije na obrascu **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="5e301-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="5e301-122">Obezbeđena je validacija koja rešava problem sa mogućnošću dodeljivanja zadatka nakon datuma završetka kalendara, što je dovodilo do neuspele dodele resursa.</span><span class="sxs-lookup"><span data-stu-id="5e301-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="5e301-123">Poboljšano je rukovanje greškama za rešavanje izuzetka prazne reference generisane iz sledećeg:</span><span class="sxs-lookup"><span data-stu-id="5e301-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="5e301-124">Dodatna komponenta **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="5e301-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="5e301-125">**PreValidateProjectTaskCreate** kada se projektni zadatak kreira bez povezanog projekta</span><span class="sxs-lookup"><span data-stu-id="5e301-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="5e301-126">Dodatna komponenta **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="5e301-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="5e301-127">Dodatna komponenta **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="5e301-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="5e301-128">Dodatna komponenta **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="5e301-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="5e301-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="5e301-129">**Sales**</span></span>

<span data-ttu-id="5e301-130">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="5e301-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="5e301-131">Poboljšano je rukovanje greškama za rešavanje problema izuzetka prazne reference generisane iz **Kopiranje projekta: Procene za HelperResource Management**.</span><span class="sxs-lookup"><span data-stu-id="5e301-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="5e301-132">**Nije spremno za fakturisanje** na stranici **Neizvršavanje naplate vremena i materijala** ne briše status naplate.</span><span class="sxs-lookup"><span data-stu-id="5e301-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="5e301-133">Ispravljena su pogrešno označena dugmad **Cene** na karticama **Cena uloge** i **Stavke kataloga**.</span><span class="sxs-lookup"><span data-stu-id="5e301-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]