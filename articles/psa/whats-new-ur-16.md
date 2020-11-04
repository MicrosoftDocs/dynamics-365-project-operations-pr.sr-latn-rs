---
title: Šta je novo ili promenjeno u izdanju 16 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 16 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083539"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="5b927-103">Project Service Automation izdanje ispravke 16, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="5b927-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="5b927-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5b927-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5b927-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="5b927-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="5b927-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5b927-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5b927-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="5b927-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5b927-108">Za još informacija pogledajte članak [Instaliranje i ispravka željenog rešenja](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="5b927-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="5b927-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 16.</span><span class="sxs-lookup"><span data-stu-id="5b927-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="5b927-110">Ova verzija ima broj verzije V3.10.6.34 i opšte je dostupna putem samo-ispravke u januaru 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="5b927-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="5b927-111">Izdanje ispravke 16</span><span class="sxs-lookup"><span data-stu-id="5b927-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5b927-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="5b927-112">Bug fixes</span></span>

-   <span data-ttu-id="5b927-113">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="5b927-113">Time and Expense</span></span>

    -   <span data-ttu-id="5b927-114">Ispravljeno: Korisnici koji pokušavaju da proslede izbrisane unose vremena i troška za odobrenje će sada primati relevantne poruke o grešci.</span><span class="sxs-lookup"><span data-stu-id="5b927-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="5b927-115">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="5b927-115">Project Management</span></span>

    -   <span data-ttu-id="5b927-116">Ispravljeno: jedinice za obezbeđivanje resursa definisanih za članove tima u šablonima se poštuju, a predlošci se primenjuju na novi projekat.</span><span class="sxs-lookup"><span data-stu-id="5b927-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="5b927-117">Ispravljeno: poboljšano rukovanje ponovnim dodeljivanjem vlasništva nad zapisima.</span><span class="sxs-lookup"><span data-stu-id="5b927-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="5b927-118">Ispravljeno: projekte koji su u procesu kopiranja neće biti dozvoljeno kopirati dok se ne završe sve operacije kopiranja.</span><span class="sxs-lookup"><span data-stu-id="5b927-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="5b927-119">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="5b927-119">Resource Management</span></span>

    -   <span data-ttu-id="5b927-120">Ispravljeno: Produži rezervacije sada ispravno upravlja kratkim trajanjima i više ne kreira nula časova za produžene rezervacije.</span><span class="sxs-lookup"><span data-stu-id="5b927-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="5b927-121">Ispravljeno: prikaz sravnjenja se sada prikazuje kada je vremenska zona projekta +5:30 GMT, a vremenska zona klijenta je drugačija.</span><span class="sxs-lookup"><span data-stu-id="5b927-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="5b927-122">Sales</span><span class="sxs-lookup"><span data-stu-id="5b927-122">Sales</span></span>

    -   <span data-ttu-id="5b927-123">Ispravljeno: kada se ukloni projekat mapiran na predmetu ugovora i mapira se novi projekat, stvarni zapisi o novom projektu nisu bili preispitivani na osnovu pravila za obračun i cena definisanih na liniji ugovora.</span><span class="sxs-lookup"><span data-stu-id="5b927-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="5b927-124">Ovo je ispravljeno u ovom izdanju.</span><span class="sxs-lookup"><span data-stu-id="5b927-124">This has been fixed in this release.</span></span> <span data-ttu-id="5b927-125">Cene i stvarni zapisi projekta koji je skoro mapiran će biti opozvani, pa ponovo kreirani ispravno na osnovu pravila o cenama i naplatama iz predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="5b927-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="5b927-126">Kao posledica ovoga, stvarni zapisi o projektu koji nije mapiran će takođe biti ponovo procenjeni, pa ponovo kreirani.</span><span class="sxs-lookup"><span data-stu-id="5b927-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="5b927-127">Fiksno: dodata je dodatna provera u stavku procene, u polje **Iznos** , kako bi se osiguralo da se nulte vrednosti ne zadržavaju.</span><span class="sxs-lookup"><span data-stu-id="5b927-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="5b927-128">Fiksno: kada se na projektu ažurira trenutno stanje, u glavni obrazac projekta se dodaje dugme za osvežavanje kako bi se korisnicima omogućilo da ponovo sinhronizuju trenutno stanje.</span><span class="sxs-lookup"><span data-stu-id="5b927-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="5b927-129">Fiksno: kada korisnici nadograde sa 2.X na 3.X, dozvoljavaju se projekti čija je vrednost za naziv projekta NULL.</span><span class="sxs-lookup"><span data-stu-id="5b927-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

