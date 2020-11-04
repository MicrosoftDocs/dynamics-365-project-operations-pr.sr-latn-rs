---
title: Definisanje veština i stručnosti
description: Ova tema pruža informacije o tome kako da podesite veštine i modele stručnosti za ocenu resursa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083524"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="95fd3-103">Definisanje veština i stručnosti</span><span class="sxs-lookup"><span data-stu-id="95fd3-103">Define skills and proficiencies</span></span>

<span data-ttu-id="95fd3-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="95fd3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95fd3-105">Veštine su karakteristike resursa koje se dele između usluga Dynamics 365 Project Operations i, ako postoji, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="95fd3-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="95fd3-106">Da biste održali spremište veština u usluzi Project Operations, idite na **Resursi** \> **Veštine resursa**.</span><span class="sxs-lookup"><span data-stu-id="95fd3-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="95fd3-107">Koristite modele stručnosti da biste ocenili resurse</span><span class="sxs-lookup"><span data-stu-id="95fd3-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="95fd3-108">Veštine za resurse ocenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="95fd3-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="95fd3-109">Pojedinačne ocene su u modelu stručnosti.</span><span class="sxs-lookup"><span data-stu-id="95fd3-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="95fd3-110">Da biste kreirali model stručnosti, idite na **Resursi** \> **Modeli stručnosti** , a zatim izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="95fd3-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="95fd3-111">U novom modelu ocenjivanja navedite minimalnu vrednost ocenjivanja, maksimalnu vrednost ocenjivanja i entitet koji se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="95fd3-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="95fd3-112">U podformi **Vrednosti ocenjivanja** možete definisati različite vrednosti ocenjivanja, od minimalne do maksimalne.</span><span class="sxs-lookup"><span data-stu-id="95fd3-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="95fd3-113">Te vrednosti ocenjivanja su prikazane u filterima **Potrebe za resursima** , **Tabela rasporeda** i **Pomoćnik za zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="95fd3-113">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
