---
title: Razvijte predloške projekata pomoću opcije za kopiranje projekata
description: Ova tema pruža informacije o tome kako kreirati predloške projekata pomoću prilagođene radnje Kopiranje projekta.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083520"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="5dbe3-103">Razvijte predloške projekata pomoću opcije za kopiranje projekata</span><span class="sxs-lookup"><span data-stu-id="5dbe3-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="5dbe3-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="5dbe3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5dbe3-105">Dynamics 365 Project Operations podržava mogućnost kopiranja projekta i vraćanja svih zadataka u generičke resurse koji predstavljaju ulogu.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="5dbe3-106">Klijenti mogu da koriste ovu funkcionalnost za izradu osnovnih predložaka projekata.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="5dbe3-107">Kada odaberete **Kopiraj projekat** , status ciljnog projekta se ažurira.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="5dbe3-108">Koristite **Razlog statusa** da bi se utvrdilo kada je akcija kopiranja završena.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="5dbe3-109">Izbor **Kopiraj projekat** takođe ažurira datum početka projekta na trenutni datum početka ako nije otkriven ciljni datum u ciljnom entitetu projekta.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="5dbe3-110">Prilagođena radnja kopiranja projekta</span><span class="sxs-lookup"><span data-stu-id="5dbe3-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="5dbe3-111">Imenuj</span><span class="sxs-lookup"><span data-stu-id="5dbe3-111">Name</span></span> 

<span data-ttu-id="5dbe3-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="5dbe3-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="5dbe3-113">Ulazni parametri</span><span class="sxs-lookup"><span data-stu-id="5dbe3-113">Input parameters</span></span>
<span data-ttu-id="5dbe3-114">Postoje tri ulazna parametra:</span><span class="sxs-lookup"><span data-stu-id="5dbe3-114">There are three input parameters:</span></span>

| <span data-ttu-id="5dbe3-115">Parametar</span><span class="sxs-lookup"><span data-stu-id="5dbe3-115">Parameter</span></span>          | <span data-ttu-id="5dbe3-116">Tip</span><span class="sxs-lookup"><span data-stu-id="5dbe3-116">Type</span></span>   | <span data-ttu-id="5dbe3-117">Vrednosti</span><span class="sxs-lookup"><span data-stu-id="5dbe3-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="5dbe3-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="5dbe3-118">ProjectCopyOption</span></span>  | <span data-ttu-id="5dbe3-119">String</span><span class="sxs-lookup"><span data-stu-id="5dbe3-119">String</span></span> | <span data-ttu-id="5dbe3-120">**{"removeNamedResources":true}** ili **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="5dbe3-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="5dbe3-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="5dbe3-121">SourceProject</span></span>      | <span data-ttu-id="5dbe3-122">Referentni entitet</span><span class="sxs-lookup"><span data-stu-id="5dbe3-122">Entity Reference</span></span> | <span data-ttu-id="5dbe3-123">Izvorni projekat</span><span class="sxs-lookup"><span data-stu-id="5dbe3-123">Source Project</span></span> |
| <span data-ttu-id="5dbe3-124">Cilj</span><span class="sxs-lookup"><span data-stu-id="5dbe3-124">Target</span></span>             | <span data-ttu-id="5dbe3-125">Referentni entitet</span><span class="sxs-lookup"><span data-stu-id="5dbe3-125">Entity Reference</span></span> | <span data-ttu-id="5dbe3-126">Ciljni projekat</span><span class="sxs-lookup"><span data-stu-id="5dbe3-126">Target Project</span></span> |


- <span data-ttu-id="5dbe3-127">**{"clearTeamsAndAssignments":true}** : Podrazumevano ponašanje za Project za veb i ukloniće sve zadatke i članove tima.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="5dbe3-128">**{"removeNamedResources":true}** Podrazumevano ponašanje za Project Operations i vratiće zadatke na generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="5dbe3-129">Za više podrazumevanih vrednosti radnji pogledajte [Koristite veb API radnje](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="5dbe3-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="5dbe3-130">Navedite polja za kopiranje</span><span class="sxs-lookup"><span data-stu-id="5dbe3-130">Specify fields to copy</span></span> 
<span data-ttu-id="5dbe3-131">Kada je akcija pozvana, **Kopiraj projekat** pogledaće prikaz projekta **Kopirajte kolone projekta** da bi se utvrdilo koja polja treba kopirati kada se projekat kopira.</span><span class="sxs-lookup"><span data-stu-id="5dbe3-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
