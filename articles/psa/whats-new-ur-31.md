---
title: Šta je novo ili promenjeno u izdanju 31 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 31 ispravke za Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999148"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="38258-103">Šta je novo ili promenjeno u izdanju 31 ispravke Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="38258-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="38258-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="38258-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="38258-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="38258-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="38258-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="38258-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="38258-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="38258-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="38258-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="38258-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="38258-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 31.</span><span class="sxs-lookup"><span data-stu-id="38258-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="38258-110">Broj izrade ove verzije je V3.10.52.77 i uglavnom je dostupna putem samostalnog ažuriranja u maju 2021. godine.</span><span class="sxs-lookup"><span data-stu-id="38258-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="38258-111">Izdanje ispravke 31</span><span class="sxs-lookup"><span data-stu-id="38258-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="38258-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="38258-112">Bug fixes</span></span>

<span data-ttu-id="38258-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="38258-113">**Time and Expense**</span></span>

<span data-ttu-id="38258-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="38258-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="38258-115">Komandna dugmad za kontrolu unosa vremena na stranici **Resurs koji može da se rezerviše** su zbunjivala korisnike.</span><span class="sxs-lookup"><span data-stu-id="38258-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="38258-116">Nulti izuzetak reference je generisan u **Project.SetTrackingFields** prilikom odobravanja unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="38258-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="38258-117">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="38258-117">**Resource Management**</span></span>

<span data-ttu-id="38258-118">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="38258-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="38258-119">**Napravite člana tima** ne prikazuje ispravno podešavanje metapodataka za podešavanje rezervacije za **Podrazumevani status poslate rezervacije**.</span><span class="sxs-lookup"><span data-stu-id="38258-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="38258-120">Prilikom nadogradnje sa PSA 1.X to 3.X, proces nadogradnje ne uspeva na **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="38258-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="38258-121">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="38258-121">**Sales**</span></span>

<span data-ttu-id="38258-122">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="38258-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="38258-123">Stvarni prihod pretvara iznose u valutu projekta u mreži za praćenje.</span><span class="sxs-lookup"><span data-stu-id="38258-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="38258-124">Zadana valuta nije jasna prilikom kreiranja redova dnevnika, citata i linija ugovora u scenarijima kada se osnovna valuta organizacije razlikuje od valute projekta.</span><span class="sxs-lookup"><span data-stu-id="38258-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="38258-125">Upit **validacije dnevnika ispravki na čekanju** se ne filtrira prema projektu.</span><span class="sxs-lookup"><span data-stu-id="38258-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="38258-126">Preostala prodaja se na projektu pogrešno izračunava.</span><span class="sxs-lookup"><span data-stu-id="38258-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="38258-127">Ponude zasnovane na kontaktu ne uspevaju kada se kreiraju bez cenovnika.</span><span class="sxs-lookup"><span data-stu-id="38258-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="38258-128">Kada odaberete **Potvrdite fakturu**, ne prikazuje se znak obrade.</span><span class="sxs-lookup"><span data-stu-id="38258-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="38258-129">Kada odaberete **Kreiraj fakturu**, ne prikazuje se znak obrade.</span><span class="sxs-lookup"><span data-stu-id="38258-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="38258-130">Zatvaranje ponude kao izgubljene ne otkazuje rezervacije.</span><span class="sxs-lookup"><span data-stu-id="38258-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







