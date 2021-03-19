---
title: Šta je novo ili promenjeno u Project Service Automation izdanju ispravke 19 u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u Project Service Automation izdanju ispravke 19 u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280730"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="25f69-103">Project Service Automation izdanje ispravke 19, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="25f69-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="25f69-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="25f69-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="25f69-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="25f69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="25f69-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="25f69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="25f69-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="25f69-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="25f69-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="25f69-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="25f69-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 19.</span><span class="sxs-lookup"><span data-stu-id="25f69-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="25f69-110">Broj izrade ove verzije je V3.10.30.41 i uglavnom je dostupna putem samostalnog ažuriranja u maju 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="25f69-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="25f69-111">Izdanje ispravke 19</span><span class="sxs-lookup"><span data-stu-id="25f69-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="25f69-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="25f69-112">Bug fixes</span></span>

<span data-ttu-id="25f69-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="25f69-113">**Time and Expense**</span></span>

<span data-ttu-id="25f69-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="25f69-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="25f69-115">Greške nastale prilikom uvoza u stavki vremena se ne pojavljuju ispravno.</span><span class="sxs-lookup"><span data-stu-id="25f69-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="25f69-116">Mreža stavke vremena ne podržava ponašanje polja **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="25f69-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="25f69-117">Resursi projekta ne mogu da kreiraju trošak sa projektom.</span><span class="sxs-lookup"><span data-stu-id="25f69-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="25f69-118">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="25f69-118">**Project Management**</span></span>

<span data-ttu-id="25f69-119">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="25f69-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="25f69-120">Drugostepeni podređeni zadatak uzrokuje pogrešnu procenu zalaganja tokom izračunavanja završetka (EAC).</span><span class="sxs-lookup"><span data-stu-id="25f69-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="25f69-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="25f69-121">**Sales**</span></span>

<span data-ttu-id="25f69-122">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="25f69-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="25f69-123">Radnja **Ponovno izračunavanje** ne funkcioniše sa detaljima o troškovima predmeta ugovora ili detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="25f69-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="25f69-124">**Ažuriranje cena** nedostaje za procene troškova.</span><span class="sxs-lookup"><span data-stu-id="25f69-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="25f69-125">Klijenti ne mogu da izaberu prilagođene razloge statusa ugovora sa stranice **Projektni ugovor**.</span><span class="sxs-lookup"><span data-stu-id="25f69-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="25f69-126">Klijenti imaju smanjene performanse kada kreiraju prilagođeni cenovnik iz ponude.</span><span class="sxs-lookup"><span data-stu-id="25f69-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="25f69-127">Klijenti doživljavaju nedoslednost sa podrazumevanim vrednostima za **jedinicu** na stranicama **Detalji stavke ponude** i **Detalji predmeta ugovora**.</span><span class="sxs-lookup"><span data-stu-id="25f69-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="25f69-128">Dodavanje stavki iz kategorije nenaplativih transakcija u naplativi predmet ugovora neće se poštovati tip obračuna **Nije naplativo** kategorije transakcije.</span><span class="sxs-lookup"><span data-stu-id="25f69-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="25f69-129">Klijenti ne mogu da koriste novododate uloge i kategoriju na prethodno kreiranim ugovorima.</span><span class="sxs-lookup"><span data-stu-id="25f69-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="25f69-130">Klijenti imaju smanjene performanse Nepotrebnog umanjenja u PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="25f69-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="25f69-131">Uloge koje su podešene kao nenaplative na listi **Kategorije resursa** trebaju biti dodate na karticu **Naplative uloge** kao **Nenaplative** na predmetu ugovora za projekat.</span><span class="sxs-lookup"><span data-stu-id="25f69-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="25f69-132">Klijenti mogu imati smanjene performanse prilikom kreiranja projekta jer **GetBookableResourceIdFromUser** pribavlja sve kolone resursa koji mogu da se rezervišu umesto samo primarni ID.</span><span class="sxs-lookup"><span data-stu-id="25f69-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="25f69-133">Entitetu **Tip transakcije** nedostaje dodatna komponenta za prethodnu validaciju da spreči korisnike da unose **Jedinice** i **UnitGroups** koje nisu važeće za tipove transakcija.</span><span class="sxs-lookup"><span data-stu-id="25f69-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="25f69-134">Korak **Ukloni** ne radi za uvoz stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="25f69-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]