---
title: Šta je novo ili promenjeno u izdanju 15 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 15 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083537"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="9a4db-103">Project Service Automation izdanje ispravke 15, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="9a4db-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="9a4db-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="9a4db-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="9a4db-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="9a4db-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9a4db-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9a4db-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9a4db-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="9a4db-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="9a4db-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9a4db-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9a4db-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 15.</span><span class="sxs-lookup"><span data-stu-id="9a4db-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="9a4db-110">Ova verzija ima broj verzije V3.10.5.28 i opšte je dostupna putem samo-ispravke u januaru 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="9a4db-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="9a4db-111">Izdanje ispravke 15</span><span class="sxs-lookup"><span data-stu-id="9a4db-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="9a4db-112">Poboljšanja</span><span class="sxs-lookup"><span data-stu-id="9a4db-112">Enhancements</span></span>

- <span data-ttu-id="9a4db-113">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="9a4db-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9a4db-114">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="9a4db-114">Bug fixes</span></span>

- <span data-ttu-id="9a4db-115">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="9a4db-115">Time and Expense</span></span>

  - <span data-ttu-id="9a4db-116">Ispravljeno: dodavanje rukovanja greškom prilikom učitavanja u prikazu usklađivanja.</span><span class="sxs-lookup"><span data-stu-id="9a4db-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="9a4db-117">Ispravljeno: čvorište resursa za projekat: preimenovanje stavke **Iznos** radi smanjenja dvosmislenosti.</span><span class="sxs-lookup"><span data-stu-id="9a4db-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="9a4db-118">Ispravljeno: podešavanje prikaza **Kopiranje kolona za stavku vremena** tako da obuhvata tip.</span><span class="sxs-lookup"><span data-stu-id="9a4db-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="9a4db-119">Ispravljeno: uređivanje trajanja stavke vremena u prikazu mreže korišćenjem decimalnih brojeva rezultira nepoznatom greškom kod nekih brojeva.</span><span class="sxs-lookup"><span data-stu-id="9a4db-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="9a4db-120">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="9a4db-120">Project Management</span></span>

  - <span data-ttu-id="9a4db-121">Ispravljeno: padajući meni za **Korišćenje u prikazu praćenja** se sada proširuje na osnovu širine opcija.</span><span class="sxs-lookup"><span data-stu-id="9a4db-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="9a4db-122">Ispravljeno: kada upravljate projektima u vremenskoj zoni +13, proračuni zadataka mogu prikazati netačne rezultate.</span><span class="sxs-lookup"><span data-stu-id="9a4db-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="9a4db-123">Ispravljeno: **Vreme završetka člana tima** je ispravljeno kada se koristi kalendar od 24 sata.</span><span class="sxs-lookup"><span data-stu-id="9a4db-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="9a4db-124">Ispravljeno: ponovo aktiviran **BPF** u glavnom obrascu **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="9a4db-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="9a4db-125">Ispravljeno: izračunavanje zadataka više ne ignoriše jedan dan.</span><span class="sxs-lookup"><span data-stu-id="9a4db-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="9a4db-126">Ispravljeno: novi baner obaveštenja je dodat u obrazac projekta kada se vremenska zona razlikuje između korisnika i projekata.</span><span class="sxs-lookup"><span data-stu-id="9a4db-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="9a4db-127">Sales</span><span class="sxs-lookup"><span data-stu-id="9a4db-127">Sales</span></span>

  - <span data-ttu-id="9a4db-128">Ispravljeno: pronalaženje kategorije procene troškova može da se koristi za filtriranje duplikata.</span><span class="sxs-lookup"><span data-stu-id="9a4db-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="9a4db-129">Ispravljeno: kôd u **PluginDomain.ExecuteInTryCatchBlock(..)** više ne sakriva poreklo izuzetka.</span><span class="sxs-lookup"><span data-stu-id="9a4db-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="9a4db-130">Ispravljeno: više se ne dobija poruka o grešci u stavci **Pronalaženje projekta** u obrascu **Stavka ponude** kada ima preko 1000 projekata.</span><span class="sxs-lookup"><span data-stu-id="9a4db-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="9a4db-131">Ispravljeno: Mreža **Procene** za procene cene rada i cene troškova sada prikazuje ispravan simbol valute.</span><span class="sxs-lookup"><span data-stu-id="9a4db-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="9a4db-132">Ispravljeno: nakon što organizacija ažurira PSA sa izdanja ispravke 14 na izdanje ispravke 15, kartica **Raspored** se više ne pojavljuje kao prazna u obrascu **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="9a4db-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
