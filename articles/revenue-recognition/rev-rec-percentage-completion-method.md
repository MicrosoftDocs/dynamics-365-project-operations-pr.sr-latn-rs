---
title: Procena prihoda projekata sa fiksnom cenom
description: Ova tema pruža informacije o proceni prihoda sa fiksnom cenom u projektima.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013818"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="16961-103">Procena prihoda projekata sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="16961-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="16961-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="16961-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="16961-105">Kada kreirate predmet projektnog ugovora sa sledećim atributima u usluzi Dynamics 365 Project Operations na platformi Microsoft Dataverse, sistem automatski kreira projekat procene prihoda sa fiksnom cenom.</span><span class="sxs-lookup"><span data-stu-id="16961-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="16961-106">Informacije u ovom projektu zasnivaju se na sledećem:</span><span class="sxs-lookup"><span data-stu-id="16961-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="16961-107">Način obračuna sa fiksnom cenom.</span><span class="sxs-lookup"><span data-stu-id="16961-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="16961-108">Vezani projekat.</span><span class="sxs-lookup"><span data-stu-id="16961-108">An associated project.</span></span>
  - <span data-ttu-id="16961-109">Najmanje jedna kontrolna tačka definisana na kartici **Raspored faktura** na stranici **Predmet projektnog ugovora**.</span><span class="sxs-lookup"><span data-stu-id="16961-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="16961-110">Pregled procena prihoda projekata sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="16961-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="16961-111">Da biste pregledali procene prihoda projekata sa fiksnom cenom, dovršite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="16961-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="16961-112">U Dynamics 365 Finance okruženju, idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Procena prihoda projekata sa fiksnom cenom**.</span><span class="sxs-lookup"><span data-stu-id="16961-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="16961-113">Izaberite projekat koji želite da prikažete i dvaput kliknite na **ID procene projekta** kako biste otvorili zapis i pregledali detalje projekta.</span><span class="sxs-lookup"><span data-stu-id="16961-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="16961-114">RAzvijte karticu **Projekat**. Videćete jedan projekat u mreži **Izabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="16961-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="16961-115">Sistem ovo koristi kao podrazumevani projekat, jer je to projekat povezan sa predmetom projektnog ugovora.</span><span class="sxs-lookup"><span data-stu-id="16961-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="16961-116">Da biste promenili povezivanje, izaberite dodatne projekte i dodajte ih u mrežu **Izabrani projekti**.</span><span class="sxs-lookup"><span data-stu-id="16961-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="16961-117">Ako je u ovoj mreži izabrano više projekata, procenat dovršenja projekta i procene prihoda izračunavaju se zajedno za sve izabrane projekte.</span><span class="sxs-lookup"><span data-stu-id="16961-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="16961-118">Trošak projekta, profil prihoda, predložak troškova i kôd perioda mogu se ručno podesiti.</span><span class="sxs-lookup"><span data-stu-id="16961-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="16961-119">Ako ih ne postavite ručno, vrednosti će biti podrazumevane na prvo izračunavanje procene za projekat koristeći pravila konfigurisana za profile troškova i prihoda projekta.</span><span class="sxs-lookup"><span data-stu-id="16961-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]