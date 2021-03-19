---
title: Šta je novo ili promenjeno u izdanju 22 ispravke za Project Service Automation u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 22 ispravke za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 389897c2604974a0bf7f221758dd03e1748ffeb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280595"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="ab500-103">Project Service Automation izdanje ispravke 22, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="ab500-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ab500-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ab500-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ab500-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="ab500-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ab500-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ab500-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ab500-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="ab500-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ab500-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ab500-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ab500-109">U ovoj temi date su funkcije koje su nove ili su promenjene u izdanju 22 ispravke za Project Service Automation u verziji 3.</span><span class="sxs-lookup"><span data-stu-id="ab500-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="ab500-110">Broj izrade ove verzije je V 3.10.33.48 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="ab500-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="ab500-111">Izdanje ispravke 22</span><span class="sxs-lookup"><span data-stu-id="ab500-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ab500-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="ab500-112">Bug fixes</span></span>



<span data-ttu-id="ab500-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="ab500-113">**Time and Expense**</span></span>

<span data-ttu-id="ab500-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ab500-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ab500-115">**Stavke vremena** se ne dodaju automatski u raspored stavki vremena nakon uvoza.</span><span class="sxs-lookup"><span data-stu-id="ab500-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="ab500-116">Alatka za biranje datuma na mreži u opciji **Stavke vremena** ne prepoznaje regionalna podešavanja korisnika.</span><span class="sxs-lookup"><span data-stu-id="ab500-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="ab500-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="ab500-117">**Resource Management**</span></span>

<span data-ttu-id="ab500-118">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ab500-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="ab500-119">U ručnom režimu, promene u skicama **Dodela resursa** se ne prepoznaju pri generisanju stavke **Zahtevi za resursom**.</span><span class="sxs-lookup"><span data-stu-id="ab500-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="ab500-120">**Zahtevi za resursom** ne podržavaju statuse prilagođenih zahteva.</span><span class="sxs-lookup"><span data-stu-id="ab500-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="ab500-121">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="ab500-121">**Project Management**</span></span>

<span data-ttu-id="ab500-122">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ab500-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="ab500-123">Dvostrukim klikom na EstimateGridControl neće se pravilno raščlaniti brojevi u holandskom formatu.</span><span class="sxs-lookup"><span data-stu-id="ab500-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="ab500-124">Dodeljeni sati se ne ažuriraju ispravno kada se dodele menjaju pomoću programskog dodatka za Microsoft Project desktop klijent.</span><span class="sxs-lookup"><span data-stu-id="ab500-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="ab500-125">Mreže za praćenje i procene projekata prikazuju pogrešnu šifru valute prodaje kada je valuta ugovora drugačija od valute kupca i ako je organizacija konfigurisana za prikazivanje šifara valuta umesto simbola valute.</span><span class="sxs-lookup"><span data-stu-id="ab500-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="ab500-126">Datum završetka člana tima dodaće jedan dan ako je raspored radnog vremena 24 sata dnevno.</span><span class="sxs-lookup"><span data-stu-id="ab500-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="ab500-127">U Rasporedu projekata, dodavanje Kategorije transakcije zadatku ne pokreće automatsko čuvanje.</span><span class="sxs-lookup"><span data-stu-id="ab500-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="ab500-128">Sledeća greška se prikazuje prilikom dodavanja člana tima u predložak projekta: „Zahtevi za resursima ne mogu biti povezani sa predlošcima projekta“.</span><span class="sxs-lookup"><span data-stu-id="ab500-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="ab500-129">Skripta pravila trake „msdyn.Approval.CanApproveOrReject“ prikazuje grešku vremenskog ograničenja.</span><span class="sxs-lookup"><span data-stu-id="ab500-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="ab500-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ab500-130">**Sales**</span></span>

<span data-ttu-id="ab500-131">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="ab500-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="ab500-132">Poruka o grešci prilikom provere nije prikazana kada je u pretraživanju cenovnika na obrascu/entitetu „Novi cenovnik ponude za projekat“ izabran Cenovnik troškova.</span><span class="sxs-lookup"><span data-stu-id="ab500-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="ab500-133">Zatvaranje dobijene ponude ne prelazi na kreirani ugovor ako je BPF u prilogu ponude u završnoj fazi.</span><span class="sxs-lookup"><span data-stu-id="ab500-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="ab500-134">Storniranje stavke **Nenaplaćena prodaja** je povezano sa prvobitnim troškom kada se opozove unos vremena.</span><span class="sxs-lookup"><span data-stu-id="ab500-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="ab500-135">Nakon odabira dugmeta **Potvrdi**, status fakture se ne menja u **Potvrđeno**, osim ako se faktura osveži.</span><span class="sxs-lookup"><span data-stu-id="ab500-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]