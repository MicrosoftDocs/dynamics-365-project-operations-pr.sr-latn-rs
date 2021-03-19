---
title: Veštine i modeli stručnosti
description: Ova tema pruža informacije o tome kako da koristite veštine i modele stručnosti.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 82eeab4c9682e5b777da4e66f6c4f3f1afb3c19b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282980"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="32d9d-103">Veštine i modeli stručnosti</span><span class="sxs-lookup"><span data-stu-id="32d9d-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="32d9d-104">Veštine su karakteristike resursa koje se dele između usluga Dynamics 365 Project Service Automation i Dynamics 365 Field Service (ako postoji).</span><span class="sxs-lookup"><span data-stu-id="32d9d-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="32d9d-105">Da biste održali spremište veština u usluzi Project Service Automation, idite na **Resursi** \> **Veštine resursa**.</span><span class="sxs-lookup"><span data-stu-id="32d9d-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Veštine resursa](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="32d9d-107">Koristite modele stručnosti da biste ocenili resurse</span><span class="sxs-lookup"><span data-stu-id="32d9d-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="32d9d-108">Veštine za resurse ocenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="32d9d-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="32d9d-109">Pojedinačne ocene su u modelu stručnosti.</span><span class="sxs-lookup"><span data-stu-id="32d9d-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="32d9d-110">Da biste kreirali model stručnosti, idite na **Resursi** \> **Modeli stručnosti**, a zatim izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="32d9d-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="32d9d-111">U novom modelu ocenjivanja navedite minimalnu vrednost ocenjivanja, maksimalnu vrednost ocenjivanja i entitet koji se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="32d9d-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="32d9d-112">U podformi **Vrednosti ocena** možete definisati različite vrednosti ocenjivanja, od minimalne do maksimalne.</span><span class="sxs-lookup"><span data-stu-id="32d9d-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definisane su minimalne i maksimalne vrednosti ocenjivanja](media/Resource-Management-image85.png)

<span data-ttu-id="32d9d-114">Te vrednosti ocenjivanja su prikazane u filterima **Potrebe za resursima**, **Tabela rasporeda** i **Pomoćnik za zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="32d9d-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]