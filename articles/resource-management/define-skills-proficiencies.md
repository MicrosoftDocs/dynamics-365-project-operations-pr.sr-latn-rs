---
title: Definisanje veština i stručnosti
description: Ova tema pruža informacije o tome kako da podesite veštine i modele stručnosti za ocenu resursa.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: d1ef50a3aa297ef439b54d37de629414ca66c820
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279695"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="564ef-103">Definisanje veština i stručnosti</span><span class="sxs-lookup"><span data-stu-id="564ef-103">Define skills and proficiencies</span></span>

<span data-ttu-id="564ef-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="564ef-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="564ef-105">Veštine su karakteristike resursa koje se dele između usluga Dynamics 365 Project Operations i Dynamics 365 Field Service (ako postoji).</span><span class="sxs-lookup"><span data-stu-id="564ef-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="564ef-106">Da biste održali spremište veština u usluzi Project Operations, idite na **Resursi** \> **Veštine resursa**.</span><span class="sxs-lookup"><span data-stu-id="564ef-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="564ef-107">Koristite modele stručnosti da biste ocenili resurse</span><span class="sxs-lookup"><span data-stu-id="564ef-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="564ef-108">Veštine za resurse ocenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="564ef-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="564ef-109">Pojedinačne ocene su u modelu stručnosti.</span><span class="sxs-lookup"><span data-stu-id="564ef-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="564ef-110">Da biste kreirali model stručnosti, idite na **Resursi** \> **Modeli stručnosti**, a zatim izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="564ef-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="564ef-111">U novom modelu ocenjivanja navedite minimalnu vrednost ocenjivanja, maksimalnu vrednost ocenjivanja i entitet koji se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="564ef-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="564ef-112">U podformi **Vrednosti ocena** možete definisati različite vrednosti ocenjivanja, od minimalne do maksimalne.</span><span class="sxs-lookup"><span data-stu-id="564ef-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="564ef-113">Te vrednosti ocenjivanja su prikazane u filterima **Potrebe za resursima**, **Tabela rasporeda** i **Pomoćnik za zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="564ef-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]