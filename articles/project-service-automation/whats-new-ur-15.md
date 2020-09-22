---
title: Šta je novo u izdanju ispravke 15 za Project Service Automation u verziji 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 15 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755163"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="3ae04-103">Project Service Automation u verziji 3, izdanje ispravke 15</span><span class="sxs-lookup"><span data-stu-id="3ae04-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="3ae04-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3ae04-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="3ae04-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="3ae04-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3ae04-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3ae04-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3ae04-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="3ae04-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="3ae04-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3ae04-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3ae04-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 15.</span><span class="sxs-lookup"><span data-stu-id="3ae04-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="3ae04-110">Ova verzija ima broj verzije V3.10.5.28 i opšte je dostupna putem samo-ispravke u januaru 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="3ae04-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="3ae04-111">Izdanje ispravke 15</span><span class="sxs-lookup"><span data-stu-id="3ae04-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="3ae04-112">Poboljšanja</span><span class="sxs-lookup"><span data-stu-id="3ae04-112">Enhancements</span></span>

- <span data-ttu-id="3ae04-113">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="3ae04-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3ae04-114">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="3ae04-114">Bug fixes</span></span>

- <span data-ttu-id="3ae04-115">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="3ae04-115">Time and Expense</span></span>

  - <span data-ttu-id="3ae04-116">Ispravljeno: dodavanje rukovanja greškom prilikom učitavanja u prikazu usklađivanja.</span><span class="sxs-lookup"><span data-stu-id="3ae04-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="3ae04-117">Ispravljeno: čvorište resursa za projekat: preimenovanje stavke **Iznos** radi smanjenja dvosmislenosti.</span><span class="sxs-lookup"><span data-stu-id="3ae04-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="3ae04-118">Ispravljeno: podešavanje prikaza **Kopiranje kolona za stavku vremena** tako da obuhvata tip.</span><span class="sxs-lookup"><span data-stu-id="3ae04-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="3ae04-119">Ispravljeno: uređivanje trajanja stavke vremena u prikazu mreže korišćenjem decimalnih brojeva rezultira nepoznatom greškom kod nekih brojeva.</span><span class="sxs-lookup"><span data-stu-id="3ae04-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="3ae04-120">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="3ae04-120">Project Management</span></span>

  - <span data-ttu-id="3ae04-121">Ispravljeno: padajući meni za **Korišćenje u prikazu praćenja** se sada proširuje na osnovu širine opcija.</span><span class="sxs-lookup"><span data-stu-id="3ae04-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="3ae04-122">Ispravljeno: kada upravljate projektima u vremenskoj zoni +13, proračuni zadataka mogu prikazati netačne rezultate.</span><span class="sxs-lookup"><span data-stu-id="3ae04-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="3ae04-123">Ispravljeno: **Vreme završetka člana tima** je ispravljeno kada se koristi kalendar od 24 sata.</span><span class="sxs-lookup"><span data-stu-id="3ae04-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="3ae04-124">Ispravljeno: ponovo aktiviran **BPF**u glavnom obrascu **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="3ae04-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="3ae04-125">Ispravljeno: izračunavanje zadataka više ne ignoriše jedan dan.</span><span class="sxs-lookup"><span data-stu-id="3ae04-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="3ae04-126">Ispravljeno: novi baner obaveštenja je dodat u obrazac projekta kada se vremenska zona razlikuje između korisnika i projekata.</span><span class="sxs-lookup"><span data-stu-id="3ae04-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="3ae04-127">Sales</span><span class="sxs-lookup"><span data-stu-id="3ae04-127">Sales</span></span>

  - <span data-ttu-id="3ae04-128">Ispravljeno: pronalaženje kategorije procene troškova može da se koristi za filtriranje duplikata.</span><span class="sxs-lookup"><span data-stu-id="3ae04-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="3ae04-129">Ispravljeno: kôd u **PluginDomain.ExecuteInTryCatchBlock(..)** više ne sakriva poreklo izuzetka.</span><span class="sxs-lookup"><span data-stu-id="3ae04-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="3ae04-130">Ispravljeno: više se ne dobija poruka o grešci u stavci **Pronalaženje projekta** u obrascu **Stavka ponude** kada ima preko 1000 projekata.</span><span class="sxs-lookup"><span data-stu-id="3ae04-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="3ae04-131">Ispravljeno: Mreža **Procene** za procene cene rada i cene troškova sada prikazuje ispravan simbol valute.</span><span class="sxs-lookup"><span data-stu-id="3ae04-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="3ae04-132">Ispravljeno: nakon što organizacija ažurira PSA sa izdanja ispravke 14 na izdanje ispravke 15, kartica **Raspored** se više ne pojavljuje kao prazna u obrascu **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="3ae04-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
