---
title: Šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755165"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="7af45-103">Project Service Automation u verziji 3, izdanje ispravke 13</span><span class="sxs-lookup"><span data-stu-id="7af45-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="7af45-104">Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="7af45-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="7af45-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="7af45-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7af45-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7af45-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7af45-107">Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="7af45-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="7af45-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7af45-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7af45-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 13.</span><span class="sxs-lookup"><span data-stu-id="7af45-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="7af45-110">Ova verzija ima broj verzije V3.10.3.18 i dostupna je prema sledećem planu:</span><span class="sxs-lookup"><span data-stu-id="7af45-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="7af45-111">**Opšta dostupnost (samo-ispravka):** novembar 2019. godine</span><span class="sxs-lookup"><span data-stu-id="7af45-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="7af45-112">**automatska ispravka:** decembar 2019. godine</span><span class="sxs-lookup"><span data-stu-id="7af45-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="7af45-113">Izdanje ispravke 13</span><span class="sxs-lookup"><span data-stu-id="7af45-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="7af45-114">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="7af45-114">Bug fixes</span></span>

- <span data-ttu-id="7af45-115">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="7af45-115">Time and Expense</span></span>

     - <span data-ttu-id="7af45-116">Ispravljeno: funkcija pretrage na stranici **Odobrenje troškova** ne radi prilikom pretraživanja prema svrsi troškova.</span><span class="sxs-lookup"><span data-stu-id="7af45-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="7af45-117">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="7af45-117">Resource Management</span></span>

     - <span data-ttu-id="7af45-118">Ispravljeno: brojevi u sravnjenju su ispravljeni kako bi bili poravnati udesno.</span><span class="sxs-lookup"><span data-stu-id="7af45-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="7af45-119">Ispravljeno: nije moguće dodeliti imenovane resurse zadacima putem kartice **Raspored**.</span><span class="sxs-lookup"><span data-stu-id="7af45-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="7af45-120">Upravljanje projektima</span><span class="sxs-lookup"><span data-stu-id="7af45-120">Project Management</span></span>

     - <span data-ttu-id="7af45-121">Ispravljeno: Izuzetak za referencu na vrednost koje nema prilikom dodeljivanja člana tima kada za **TransactionType** nedostaju informacije o podešavanju za entitete **Unit** i **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="7af45-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="7af45-122">Sales</span><span class="sxs-lookup"><span data-stu-id="7af45-122">Sales</span></span>

     - <span data-ttu-id="7af45-123">Ispravljeno: duplirani zapisi tipa transakcije vraćaju grešku kada se kreiraju zapisi cene uloge.</span><span class="sxs-lookup"><span data-stu-id="7af45-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="7af45-124">Ispravljeno: dodatna dugmad za **Nova mogućnost za poslovanje**, **Ponuda**, **Stavka porudžbine** i **Dodaj proizvod** su vidljiva u komandama za mogućnosti za poslovanje, ponude, proizvode porudžbine i podformi redova zasnovanih na projektu.</span><span class="sxs-lookup"><span data-stu-id="7af45-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


