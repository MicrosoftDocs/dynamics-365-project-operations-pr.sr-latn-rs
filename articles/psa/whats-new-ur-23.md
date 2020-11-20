---
title: Šta je novo ili promenjeno u izdanju 23 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 23 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131135"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="76e63-103">Project Service Automation izdanje 23 ispravke verzije 3</span><span class="sxs-lookup"><span data-stu-id="76e63-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="76e63-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="76e63-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="76e63-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="76e63-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="76e63-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="76e63-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="76e63-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="76e63-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="76e63-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="76e63-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="76e63-109">U ovoj temi date su funkcije i ispravke koje su nove ili promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 23.</span><span class="sxs-lookup"><span data-stu-id="76e63-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="76e63-110">Ova verzija ima broj V3.10.34.30 i opšte je dostupna putem samostalne ispravke objavljene avgusta 2020.</span><span class="sxs-lookup"><span data-stu-id="76e63-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="76e63-111">Izdanje ispravke 23</span><span class="sxs-lookup"><span data-stu-id="76e63-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="76e63-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="76e63-112">Bug fixes</span></span>

<span data-ttu-id="76e63-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="76e63-113">**Time and Expense**</span></span>

<span data-ttu-id="76e63-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="76e63-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="76e63-115">Rukujte graničnim slučajem u funkciji **Izbriši člana projektnog tima** da biste pružili smislen izuzetak.</span><span class="sxs-lookup"><span data-stu-id="76e63-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="76e63-116">Uvoz zadatka rezultira praznim ekranom za uklanjanje.</span><span class="sxs-lookup"><span data-stu-id="76e63-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="76e63-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="76e63-117">**Resource Management**</span></span>

<span data-ttu-id="76e63-118">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="76e63-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="76e63-119">**Kartica resursa mreže za ukupnu iskorišćenost resursa** prikazuje netačne podatke kada je vremenska skala duža od pet dana.</span><span class="sxs-lookup"><span data-stu-id="76e63-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="76e63-120">Kada klijenti kreiraju resurs koji može da se rezerviše, dodatna komponenta povremeno ne uspeva automatski da doda resurs u Microsoft Office 365 grupu.</span><span class="sxs-lookup"><span data-stu-id="76e63-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="76e63-121">Prikaz **Usaglašenost** netačno prikazuje ručne konture u prikazu **Nedelja** ili **Mesec**.</span><span class="sxs-lookup"><span data-stu-id="76e63-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="76e63-122">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="76e63-122">**Project Management**</span></span>

<span data-ttu-id="76e63-123">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="76e63-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="76e63-124">Prekomerni broj entiteta **RetrieveMultiple za podešavanja korisnika** uzrokuju pogoršane performanse za odobravanje projekata i druge operacije.</span><span class="sxs-lookup"><span data-stu-id="76e63-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="76e63-125">Pronalaženje resursa mreže **Planiranje zadataka** ograničeno je na prikazivanje do pet članova tima iz projektnog tima.</span><span class="sxs-lookup"><span data-stu-id="76e63-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="76e63-126">Pronalaženje resursa mreže **Planiranje zadataka** ne filtrira neaktivne resurse.</span><span class="sxs-lookup"><span data-stu-id="76e63-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="76e63-127">Ručni režim ne radi kako se očekuje u strukturnoj analizi posla na planiranju projekta.</span><span class="sxs-lookup"><span data-stu-id="76e63-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="76e63-128">Mreža **Planiranje zadataka** pokazuje **Neaktivne kategorije transakcija**.</span><span class="sxs-lookup"><span data-stu-id="76e63-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="76e63-129">Mreža **Dodeljivanje resursa** se nepravilno zaokružuje kada zadatak ima više dodela.</span><span class="sxs-lookup"><span data-stu-id="76e63-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="76e63-130">Vrednosti zaokruživanja razlikuju se između planiranih troškova i stvarnih troškova za jedan zadatak.</span><span class="sxs-lookup"><span data-stu-id="76e63-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="76e63-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="76e63-131">**Sales**</span></span>

<span data-ttu-id="76e63-132">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="76e63-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="76e63-133">Dupli klik na **Preuzmi sve kategorije transakcija** kreira više linija.</span><span class="sxs-lookup"><span data-stu-id="76e63-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
