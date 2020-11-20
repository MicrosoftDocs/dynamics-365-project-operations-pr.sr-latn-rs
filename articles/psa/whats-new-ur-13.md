---
title: Šta je novo ili promenjeno u izdanju 13 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3.
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
ms.openlocfilehash: bcb05b640966e760a7a74a306a3f0a39594baed8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121640"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="a7989-103">Project Service Automation izdanje ispravke 13, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="a7989-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="a7989-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a7989-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a7989-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="a7989-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a7989-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a7989-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a7989-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="a7989-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a7989-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a7989-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a7989-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 13.</span><span class="sxs-lookup"><span data-stu-id="a7989-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="a7989-110">Ova verzija ima broj verzije V3.10.3.18 i dostupna je prema sledećem planu:</span><span class="sxs-lookup"><span data-stu-id="a7989-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="a7989-111">**Opšta dostupnost (samo-ispravka):** novembar 2019. godine</span><span class="sxs-lookup"><span data-stu-id="a7989-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="a7989-112">**automatska ispravka:** decembar 2019. godine</span><span class="sxs-lookup"><span data-stu-id="a7989-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="a7989-113">Izdanje ispravke 13</span><span class="sxs-lookup"><span data-stu-id="a7989-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="a7989-114">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="a7989-114">Bug fixes</span></span>

- <span data-ttu-id="a7989-115">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="a7989-115">Time and Expense</span></span>

     - <span data-ttu-id="a7989-116">Ispravljeno: funkcija pretrage na stranici **Odobrenje troškova** ne radi prilikom pretraživanja prema svrsi troškova.</span><span class="sxs-lookup"><span data-stu-id="a7989-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="a7989-117">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="a7989-117">Resource Management</span></span>

     - <span data-ttu-id="a7989-118">Ispravljeno: brojevi u sravnjenju su ispravljeni kako bi bili poravnati udesno.</span><span class="sxs-lookup"><span data-stu-id="a7989-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="a7989-119">Ispravljeno: nije moguće dodeliti imenovane resurse zadacima putem kartice **Raspored**.</span><span class="sxs-lookup"><span data-stu-id="a7989-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="a7989-120">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="a7989-120">Project Management</span></span>

     - <span data-ttu-id="a7989-121">Ispravljeno: Izuzetak za referencu na vrednost koje nema prilikom dodeljivanja člana tima kada za **TransactionType** nedostaju informacije o podešavanju za entitete **Unit** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="a7989-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="a7989-122">Sales</span><span class="sxs-lookup"><span data-stu-id="a7989-122">Sales</span></span>

     - <span data-ttu-id="a7989-123">Ispravljeno: duplirani zapisi tipa transakcije vraćaju grešku kada se kreiraju zapisi cene uloge.</span><span class="sxs-lookup"><span data-stu-id="a7989-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="a7989-124">Ispravljeno: Dodatna dugmad za stavke **Nova mogućnost za poslovanje**, **Ponuda**, **Stavka porudžbine** i **Dodavanje proizvoda** su vidljiva u komandama za mogućnosti za poslovanje, ponude, naručivanje proizvoda i podforme za stavke zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="a7989-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>


