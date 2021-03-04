---
title: Šta je novo ili promenjeno u izdanju 17 ispravke Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 17 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143769"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="91cb5-103">Project Service Automation izdanje ispravke 17, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="91cb5-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="91cb5-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="91cb5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="91cb5-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="91cb5-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="91cb5-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="91cb5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="91cb5-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="91cb5-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="91cb5-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="91cb5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="91cb5-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 17.</span><span class="sxs-lookup"><span data-stu-id="91cb5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="91cb5-110">Ova verzija ima broj verzije V3.10.6.34 i opšte je dostupna putem samo-ispravke u martu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="91cb5-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="91cb5-111">Izdanje ispravke 17</span><span class="sxs-lookup"><span data-stu-id="91cb5-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="91cb5-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="91cb5-112">Bug fixes</span></span>

<span data-ttu-id="91cb5-113">**Opšti problemi**</span><span class="sxs-lookup"><span data-stu-id="91cb5-113">**General**</span></span>

- <span data-ttu-id="91cb5-114">Ispravljeno: ažurirajte Project Service Automation za sprovođenje licenci za članove tima (Čvorište resursa za projekat će uključiti 3.x metapodatke plana usluge za članove tima)</span><span class="sxs-lookup"><span data-stu-id="91cb5-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="91cb5-115">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="91cb5-115">**Time and Expense**</span></span>

- <span data-ttu-id="91cb5-116">Ispravljeno: nemogućnost promene procene troškova iz cene različite od nule u nulu (0).</span><span class="sxs-lookup"><span data-stu-id="91cb5-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="91cb5-117">Promena se ignoriše.</span><span class="sxs-lookup"><span data-stu-id="91cb5-117">The change is ignored.</span></span>

<span data-ttu-id="91cb5-118">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="91cb5-118">**Project Management**</span></span>

- <span data-ttu-id="91cb5-119">Ispravljeno: dodata je provera nultih vrednosti u ime pozicije člana tima.</span><span class="sxs-lookup"><span data-stu-id="91cb5-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="91cb5-120">Ispravljeno: polje **msdyn_userresourceid** polje u entitetu **msdyn_resourceassignment** nije odobreno.</span><span class="sxs-lookup"><span data-stu-id="91cb5-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="91cb5-121">Ispravljeno: nadogradnja sa 2.x na 3.x sada upravlja praznim konturama angažovanja u dodelama zadataka.</span><span class="sxs-lookup"><span data-stu-id="91cb5-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="91cb5-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="91cb5-122">**Sales**</span></span>

- <span data-ttu-id="91cb5-123">Ispravljeno: **Invoice.PreValidateInvoiceUpdate** sada pravilno upravlja scenarijem ponovnog dodeljivanja vlasništva zapisa.</span><span class="sxs-lookup"><span data-stu-id="91cb5-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="91cb5-124">Ispravljeno: kada je klasa transakcije **Vreme**, **UnitGroup** ne može da se uređuje ni za jedan entitet, uključujući **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="91cb5-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="91cb5-125">Međutim, **Jedinica** ne može da se uređuje samo za **JournalLine** i **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="91cb5-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>


