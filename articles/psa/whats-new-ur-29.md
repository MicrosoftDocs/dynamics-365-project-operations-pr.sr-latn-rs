---
title: Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 29 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664660"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="3ad87-103">Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="3ad87-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3ad87-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3ad87-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3ad87-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="3ad87-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3ad87-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3ad87-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3ad87-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="3ad87-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3ad87-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3ad87-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3ad87-109">U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene u izdanju ispravke 29 za Project Service Automation verzije 3.</span><span class="sxs-lookup"><span data-stu-id="3ad87-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="3ad87-110">Ova verzija ima broj verzije V3.10.47.7 i generalno je dostupna putem samostalnog ažuriranja u februaru 2021.</span><span class="sxs-lookup"><span data-stu-id="3ad87-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="3ad87-111">Izdanje ispravke 29</span><span class="sxs-lookup"><span data-stu-id="3ad87-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3ad87-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="3ad87-112">Bug fixes</span></span>

<span data-ttu-id="3ad87-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="3ad87-113">**Time and Expense**</span></span>

<span data-ttu-id="3ad87-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3ad87-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3ad87-115">Korisnici ne mogu da vide radno vreme zabeleženo neradnim danima u mreži za unos vremena.</span><span class="sxs-lookup"><span data-stu-id="3ad87-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="3ad87-116">Odobreni unosi troškova mogu se uređivati na mreži.</span><span class="sxs-lookup"><span data-stu-id="3ad87-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="3ad87-117">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="3ad87-117">**Project Management**</span></span>

<span data-ttu-id="3ad87-118">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3ad87-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="3ad87-119">Nedostaje logika validacije da bi se osiguralo da sati angažovanja za dodelu resursa ne mogu biti negativni.</span><span class="sxs-lookup"><span data-stu-id="3ad87-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="3ad87-120">Prilagođena radnja, **AssignResourcesForTask** ažurira sva polja, a ne samo promenjena.</span><span class="sxs-lookup"><span data-stu-id="3ad87-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="3ad87-121">Kada kopirate projekat u okruženju sa dodatnim komponentama ili tokovima posla koji su registrovani u događaju **CreateProject**, atribut **msdyn_bulkgenerationstatus** se ne ažurira ako je **CopyWBSToProject** neuspešan.</span><span class="sxs-lookup"><span data-stu-id="3ad87-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="3ad87-122">Kada proširite kalendar projekta, radni dani se ne sortiraju u rastućem redosledu, što dovodi do neuspeha ažuriranja nekih projektnih zadataka.</span><span class="sxs-lookup"><span data-stu-id="3ad87-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="3ad87-123">Promena menadžera projekta na postojećem projektu pokreće podrazumevanu logiku organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="3ad87-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="3ad87-124">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="3ad87-124">**Sales**</span></span>

<span data-ttu-id="3ad87-125">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3ad87-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="3ad87-126">Kartica **Izvršenje ugovora** na stranici **Ugovor** bez upozorenja ne uspeva tokom inicijalizacije kada nema linija ugovora.</span><span class="sxs-lookup"><span data-stu-id="3ad87-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
