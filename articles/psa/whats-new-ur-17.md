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
ms.openlocfilehash: 12df166e1bd1b5f0e11d79dc24122fb1ed7e6e6c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280820"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="e5a0e-103">Project Service Automation izdanje ispravke 17, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="e5a0e-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e5a0e-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e5a0e-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="e5a0e-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e5a0e-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e5a0e-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e5a0e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e5a0e-109">U ovoj temi date su funkcije i ispravke koje su nove ili su promenjene u rešenju PSA u verziji 3, izdanje ispravke 17.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="e5a0e-110">Ova verzija ima broj verzije V3.10.6.34 i opšte je dostupna putem samo-ispravke u martu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="e5a0e-111">Izdanje ispravke 17</span><span class="sxs-lookup"><span data-stu-id="e5a0e-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e5a0e-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="e5a0e-112">Bug fixes</span></span>

<span data-ttu-id="e5a0e-113">**Opšti problemi**</span><span class="sxs-lookup"><span data-stu-id="e5a0e-113">**General**</span></span>

- <span data-ttu-id="e5a0e-114">Ispravljeno: ažurirajte Project Service Automation za sprovođenje licenci za članove tima (Čvorište resursa za projekat će uključiti 3.x metapodatke plana usluge za članove tima)</span><span class="sxs-lookup"><span data-stu-id="e5a0e-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="e5a0e-115">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="e5a0e-115">**Time and Expense**</span></span>

- <span data-ttu-id="e5a0e-116">Ispravljeno: nemogućnost promene procene troškova iz cene različite od nule u nulu (0).</span><span class="sxs-lookup"><span data-stu-id="e5a0e-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="e5a0e-117">Promena se ignoriše.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-117">The change is ignored.</span></span>

<span data-ttu-id="e5a0e-118">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="e5a0e-118">**Project Management**</span></span>

- <span data-ttu-id="e5a0e-119">Ispravljeno: dodata je provera nultih vrednosti u ime pozicije člana tima.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="e5a0e-120">Ispravljeno: polje **msdyn_userresourceid** polje u entitetu **msdyn_resourceassignment** nije odobreno.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="e5a0e-121">Ispravljeno: nadogradnja sa 2.x na 3.x sada upravlja praznim konturama angažovanja u dodelama zadataka.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="e5a0e-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e5a0e-122">**Sales**</span></span>

- <span data-ttu-id="e5a0e-123">Ispravljeno: **Invoice.PreValidateInvoiceUpdate** sada pravilno upravlja scenarijem ponovnog dodeljivanja vlasništva zapisa.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="e5a0e-124">Ispravljeno: kada je klasa transakcije **Vreme**, **UnitGroup** ne može da se uređuje ni za jedan entitet, uključujući **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="e5a0e-125">Međutim, **Jedinica** ne može da se uređuje samo za **JournalLine** i **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e5a0e-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]