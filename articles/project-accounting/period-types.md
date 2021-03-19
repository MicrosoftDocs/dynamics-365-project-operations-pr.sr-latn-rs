---
title: Tipovi perioda
description: U ovoj temi se pružaju informacije o tome kako da konfigurišete tipove perioda za procenu prihoda.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287300"
---
# <a name="period-types"></a><span data-ttu-id="319d5-103">Tipovi perioda</span><span class="sxs-lookup"><span data-stu-id="319d5-103">Period types</span></span>

<span data-ttu-id="319d5-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="319d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="319d5-105">Tip perioda definiše koliko se često procenjuje prihod od projekta.</span><span class="sxs-lookup"><span data-stu-id="319d5-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="319d5-106">U ovoj temi se pružaju informacije o tome kako da konfigurišete tipove perioda za procenu prihoda.</span><span class="sxs-lookup"><span data-stu-id="319d5-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="319d5-107">Kreiranje i rad sa tipovima perioda</span><span class="sxs-lookup"><span data-stu-id="319d5-107">Create and work with period types</span></span>
<span data-ttu-id="319d5-108">Da biste kreirali i radili sa tipovima perioda, izvršite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="319d5-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="319d5-109">U Dynamics 365 Finance okruženju, idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Procene** > **Tipovi perioda**.</span><span class="sxs-lookup"><span data-stu-id="319d5-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="319d5-110">Da biste kreirali novi tip perioda, izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="319d5-110">Select **New** to create new period type.</span></span> <span data-ttu-id="319d5-111">Unesite naziv i opis.</span><span class="sxs-lookup"><span data-stu-id="319d5-111">Enter a name and description.</span></span>
3. <span data-ttu-id="319d5-112">U polju **Učestalost**, izaberite vrednost:</span><span class="sxs-lookup"><span data-stu-id="319d5-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="319d5-113">Ako izaberete **sedmica**, **Dvonedeljno**, **Polumesečno**, **Mesec**, **Dan**, **Kvartal** ili **Godina**, kalendar će se koristiti za generisanje perioda.</span><span class="sxs-lookup"><span data-stu-id="319d5-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="319d5-114">Ako izaberete **Period knjige**, periodi knjige iz konfiguracije glavne knjige će se koristiti za generisanje perioda.</span><span class="sxs-lookup"><span data-stu-id="319d5-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="319d5-115">Ako izaberete **Neograničeno**, možete odrediti prilagođene periode.</span><span class="sxs-lookup"><span data-stu-id="319d5-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="319d5-116">Izaberite zapis tipa perioda, a zatim izaberite **Generiši periode** da biste kreirali periode za tip perioda.</span><span class="sxs-lookup"><span data-stu-id="319d5-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="319d5-117">Na osnovu učestalosti perioda koju ste izabrali, možda ćete moći da odredite datum početka ili broj perioda koji treba generisati.</span><span class="sxs-lookup"><span data-stu-id="319d5-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="319d5-118">Izaberite **Periodi** da biste pregledali generisane periode.</span><span class="sxs-lookup"><span data-stu-id="319d5-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]