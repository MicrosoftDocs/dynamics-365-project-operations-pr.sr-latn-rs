---
title: Šta je novo ili promenjeno u izdanju 24 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 24 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146725"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="ac904-103">Project Service Automation izdanje 24 ispravke verzije 3</span><span class="sxs-lookup"><span data-stu-id="ac904-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ac904-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ac904-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ac904-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="ac904-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ac904-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ac904-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ac904-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="ac904-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ac904-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ac904-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ac904-109">U ovoj temi date su funkcije i ispravke koje su nove ili promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 24.</span><span class="sxs-lookup"><span data-stu-id="ac904-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="ac904-110">Ova verzija ima broj V3.10.42.43 i opšte je dostupna putem samostalne ispravke objavljene oktobra 2020.</span><span class="sxs-lookup"><span data-stu-id="ac904-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="ac904-111">Izdanje ispravke 24</span><span class="sxs-lookup"><span data-stu-id="ac904-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ac904-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="ac904-112">Bug fixes</span></span>

<span data-ttu-id="ac904-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ac904-113">**Sales**</span></span>

<span data-ttu-id="ac904-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ac904-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac904-115">Problem prilikom postavljanja podrazumevanog cenovnika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ac904-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="ac904-116">Performanse ostvarene ponude su spore zbog ugrađenog cenovnika i kopija zapisa cena uloga.</span><span class="sxs-lookup"><span data-stu-id="ac904-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="ac904-117">**Ugovor o projektu / čvorište za prodaju** > **Stavka predmeta proizvoda / količina stavke porudžbine** automatski se zaokružuje na najbliži celi broj.</span><span class="sxs-lookup"><span data-stu-id="ac904-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="ac904-118">Podignite sistemske privilegije prilikom čitanja cenovnika.</span><span class="sxs-lookup"><span data-stu-id="ac904-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="ac904-119">Kopirajte polja adrese klijenta **address1_freighttermscode** i **address1_shippingmethodcode** za ponudu/porudžbinu.</span><span class="sxs-lookup"><span data-stu-id="ac904-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="ac904-120">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="ac904-120">**Time and Expense**</span></span>

<span data-ttu-id="ac904-121">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ac904-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac904-122">**Mreža stavke vremena** ne podržava vremensko ponašanje **Samo datum**.</span><span class="sxs-lookup"><span data-stu-id="ac904-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="ac904-123">**Stavka vremena** se ne osvežava automatski.</span><span class="sxs-lookup"><span data-stu-id="ac904-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="ac904-124">Potrebno je ručno osvežavanje.</span><span class="sxs-lookup"><span data-stu-id="ac904-124">A manual refresh is required.</span></span>
- <span data-ttu-id="ac904-125">Nije moguće uvesti stavke vremena iz zadatka kada postoji pauza (0 sati) u dodelama resursa.</span><span class="sxs-lookup"><span data-stu-id="ac904-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="ac904-126">Kada kreirate stavku vremena, podesite da početak bude isti kao **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="ac904-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="ac904-127">Ponovo omogućite grupno uređivanje za unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ac904-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="ac904-128">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="ac904-128">**Resource Management**</span></span>

<span data-ttu-id="ac904-129">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ac904-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac904-130">Pokušaj ažuriranja statusa jednodnevne rezervacije bez zahteva dovešće do izuzetka „null-ref“.</span><span class="sxs-lookup"><span data-stu-id="ac904-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="ac904-131">Greška pri učitavanju **prikaza usaglašenosti**.</span><span class="sxs-lookup"><span data-stu-id="ac904-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="ac904-132">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="ac904-132">**Project Management**</span></span>

<span data-ttu-id="ac904-133">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ac904-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="ac904-134">U **Rasporedu projekta**, pri promeni iz **Ručno** u **Automatski**, automatsko čuvanje se ne dovršava.</span><span class="sxs-lookup"><span data-stu-id="ac904-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="ac904-135">Troškovi troškova ne bi trebalo da se računaju prema odstupanju u odnosu na **Mreža za praćenje projekata**.</span><span class="sxs-lookup"><span data-stu-id="ac904-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="ac904-136">Nedosledno ponašanje za kolone **Oznaka procene** tokom učitavanja u odnosu na promenu tipa **Vremenska faza**.</span><span class="sxs-lookup"><span data-stu-id="ac904-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="ac904-137">Stvarni troškovi projekta možda neće odražavati ukupne iznose iz **stvarnih vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="ac904-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="ac904-138">**Predviđeni datum završetka** na kartici **Rezime** se ne podudara sa **SAP rasporedom**.</span><span class="sxs-lookup"><span data-stu-id="ac904-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="ac904-139">**Ažuriranje stvarnih sati** pri izvlačenju ne radi ispravno.</span><span class="sxs-lookup"><span data-stu-id="ac904-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="ac904-140">Menadžer projekta izvan osnovne **poslovne jedinice** ne može da kreira projekat.</span><span class="sxs-lookup"><span data-stu-id="ac904-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="ac904-141">Promene u zadatku ili kategoriji **procena troškova** ne ostaju sačuvane.</span><span class="sxs-lookup"><span data-stu-id="ac904-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="ac904-142">**Kopija ugovora** kopira rasporede faktura i status pokretanja.</span><span class="sxs-lookup"><span data-stu-id="ac904-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="ac904-143">Dugme **Osveži stvarne vrednosti** pogrešno izračunava rezimirane zadatke.</span><span class="sxs-lookup"><span data-stu-id="ac904-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="ac904-144">Dodatak za Microsoft Project: Ispravljena je greška reference „null“ ako bilo koji član tima ima praznu jedinicu za obezbeđivanje resursa.</span><span class="sxs-lookup"><span data-stu-id="ac904-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

