---
title: Šta je novo ili promenjeno u izdanju 28 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 28 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150640"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d4f09-103">Šta je novo ili promenjeno u izdanju 28 ispravke Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="d4f09-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d4f09-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d4f09-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d4f09-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="d4f09-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d4f09-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d4f09-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d4f09-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="d4f09-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d4f09-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d4f09-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d4f09-109">U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene u izdanju ispravke 28 za Project Service Automation verzije 3. Ova verzija ima broj verzije V3.10.46.32 i postala je opšte dostupna putem samostalne ispravke u januaru 2021.</span><span class="sxs-lookup"><span data-stu-id="d4f09-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d4f09-110">Izdanje ispravke 28</span><span class="sxs-lookup"><span data-stu-id="d4f09-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d4f09-111">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="d4f09-111">Bug fixes</span></span>

<span data-ttu-id="d4f09-112">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="d4f09-112">**Time and Expense**</span></span>

<span data-ttu-id="d4f09-113">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d4f09-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d4f09-114">Korisnici mogu da koriste **Masovno uređivanje** za ažuriranje zapisa vremena koji su odobreni i poslati.</span><span class="sxs-lookup"><span data-stu-id="d4f09-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d4f09-115">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="d4f09-115">**Project Management**</span></span>

<span data-ttu-id="d4f09-116">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d4f09-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d4f09-117">U slučajevima kada se GUID zadatka tumači kao broj, zadaci se ne mogu otvoriti za uređivanje pomoću opcije **Uredi zadatak** u traci na stranici **Strukturna analiza posla**.</span><span class="sxs-lookup"><span data-stu-id="d4f09-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d4f09-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d4f09-118">**Sales**</span></span>

<span data-ttu-id="d4f09-119">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="d4f09-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d4f09-120">Izuzetak prazne reference se generiše kada se poziva dodatna komponenta **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="d4f09-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d4f09-121">**Označi kao spremno za fakturisanje** u mreži kontrolnih tačaka samo delimično ažurira atribute, osim atributa **InvoiceStatus**, koji se ažurira.</span><span class="sxs-lookup"><span data-stu-id="d4f09-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

