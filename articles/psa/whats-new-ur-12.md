---
title: Šta je novo ili promenjeno u izdanju 12 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 12 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281090"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="92403-103">Project Service Automation izdanje ispravke 12, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="92403-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="92403-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="92403-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="92403-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="92403-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="92403-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="92403-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="92403-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="92403-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="92403-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="92403-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="92403-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 12.</span><span class="sxs-lookup"><span data-stu-id="92403-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="92403-110">Ova verzija ima broj verzije V3.10.2.34 i opšte je dostupna putem samo-ispravke u oktobru 2019. godine.</span><span class="sxs-lookup"><span data-stu-id="92403-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="92403-111">Izdanje ispravke 12</span><span class="sxs-lookup"><span data-stu-id="92403-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="92403-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="92403-112">Bug fixes</span></span>

- <span data-ttu-id="92403-113">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="92403-113">Time and Expense</span></span>

    - <span data-ttu-id="92403-114">Ispravljeno: Poruke o greškama za stavku vremena su ispravljene sa relevantnijim kontekstom.</span><span class="sxs-lookup"><span data-stu-id="92403-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="92403-115">Ispravljeno: Mreža stavke vremena i raspored ispravno prikazuju vertikalnu traku za listanje kada je to potrebno.</span><span class="sxs-lookup"><span data-stu-id="92403-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="92403-116">Ispravljeno: nije moguće odobriti prosleđene stavke troškova i vremena.</span><span class="sxs-lookup"><span data-stu-id="92403-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="92403-117">Ispravljeno: poruka dijaloga potvrde otkazivanja odobrenja je ispravljena i odražava status odobrenja kada se promeni iz **Odobreno** u **Prosleđeno**.</span><span class="sxs-lookup"><span data-stu-id="92403-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="92403-118">Ispravljeno: polja **Cena**, **Jedinica** i **Količina** su sada zaključana u zapisu troška nakon što je odobren.</span><span class="sxs-lookup"><span data-stu-id="92403-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="92403-119">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="92403-119">Project Management</span></span>

    - <span data-ttu-id="92403-120">Ispravljeno: radnja **Novo** na glavnom obrascu **Član tima** je uklonjena.</span><span class="sxs-lookup"><span data-stu-id="92403-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="92403-121">Ispravljeno: dodele resursa su ispravljene kako bi se uzele u obzir greške u nepreciznom zaokruživanju, koje dovode do pomeranja datuma završetka zadatka.</span><span class="sxs-lookup"><span data-stu-id="92403-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="92403-122">Ispravljeno: u mreži zadataka korisniku će se prikazati relevantne greške na strani servera.</span><span class="sxs-lookup"><span data-stu-id="92403-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="92403-123">Ispravljeno: ime člana tima sada se prikazuje u zadatku birača osoba umesto naziva položaja.</span><span class="sxs-lookup"><span data-stu-id="92403-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="92403-124">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="92403-124">Resource Management</span></span>

    - <span data-ttu-id="92403-125">Ispravljeno: detalji o zahtevima za resursima za projekte kreirane iz predloška sada koriste kalendar projekata.</span><span class="sxs-lookup"><span data-stu-id="92403-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="92403-126">Ispravljeno: veštine i kompetencije sada podrazumevano potiču iz osnovnih podataka uloge u zahtev za resursom koji je kreiran za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="92403-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="92403-127">Sales</span><span class="sxs-lookup"><span data-stu-id="92403-127">Sales</span></span>

    - <span data-ttu-id="92403-128">Ispravljeno: duplirani ID-ovi objekta pronađeni na glavnom obrascu **Ugovor**.</span><span class="sxs-lookup"><span data-stu-id="92403-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="92403-129">Ispravljeno: logika je ispravljena kako bi kartica **Analiza ponude** bila vidljiva tako da prikazuje podešavanje metapodataka kartice.</span><span class="sxs-lookup"><span data-stu-id="92403-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="92403-130">Ispravljeno: računovodstveni datum na stvarnom zapisu sada potiče od datuma unosa vremena/troška, a ne od datuma odobrenja.</span><span class="sxs-lookup"><span data-stu-id="92403-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]