---
title: Šta je novo ili promenjeno u izdanju 30 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 30 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010443"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="f9166-103">Šta je novo ili promenjeno u izdanju 30 ispravke Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="f9166-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f9166-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f9166-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f9166-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="f9166-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f9166-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="f9166-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f9166-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="f9166-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f9166-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="f9166-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="f9166-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 30.</span><span class="sxs-lookup"><span data-stu-id="f9166-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="f9166-110">Broj izrade ove verzije je V3.10.51.61 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="f9166-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="f9166-111">Izdanje ispravke 30</span><span class="sxs-lookup"><span data-stu-id="f9166-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f9166-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="f9166-112">Bug fixes</span></span>

<span data-ttu-id="f9166-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="f9166-113">**Time and Expense**</span></span>

<span data-ttu-id="f9166-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f9166-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9166-115">Dolazi do greške kada kreirate i sačuvate stavku vremena na stranici **Brzo kreiranje** ako je polje **Uloga** uklonjeno.</span><span class="sxs-lookup"><span data-stu-id="f9166-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="f9166-116">Filter za stavku vremena primenjuje pogrešan operator filtera.</span><span class="sxs-lookup"><span data-stu-id="f9166-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="f9166-117">Kopirani vremenski listovi se ne prikazuju automatski kada izaberete **Kopiranje sedmice** na kontroli stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="f9166-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="f9166-118">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="f9166-118">**Resource Management**</span></span>

<span data-ttu-id="f9166-119">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f9166-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9166-120">Kada produžite rezervaciju, status rezervacije dodeljen fiksnoj rezervaciji je netačan.</span><span class="sxs-lookup"><span data-stu-id="f9166-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="f9166-121">Produženjem rezervacije poštuje se status rezervacije definisan kao **Dodeljeno** u metapodacima podešavanja rezervacije.</span><span class="sxs-lookup"><span data-stu-id="f9166-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="f9166-122">Kada nije naveden važeći status rezervacije, poruka o grešci nije pravilno lokalizovana.</span><span class="sxs-lookup"><span data-stu-id="f9166-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="f9166-123">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="f9166-123">**Project Management**</span></span>

<span data-ttu-id="f9166-124">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f9166-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9166-125">Projekti se ne mogu kreirati u jednoj valuti, a da uključuju povezane zadatke u drugoj valuti.</span><span class="sxs-lookup"><span data-stu-id="f9166-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="f9166-126">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="f9166-126">**Sales**</span></span>

<span data-ttu-id="f9166-127">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="f9166-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="f9166-128">Kada se kopira cenovnik, cene se ne ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="f9166-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="f9166-129">Zatvaranje ponude kao ostvarene ne uspeva kada detalj cene ima vrednost za poreklo.</span><span class="sxs-lookup"><span data-stu-id="f9166-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="f9166-130">Na entitetu **Projektni zadatak**, **Procenjena cena** se preimenuje u **Planirana cena (osnovna)**.</span><span class="sxs-lookup"><span data-stu-id="f9166-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="f9166-131">Izuzetak nulte reference se generiše kada se fakture kreiraju ili izbrišu.</span><span class="sxs-lookup"><span data-stu-id="f9166-131">A null reference exception is generated when invoices are created or deleted.</span></span>
