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
ms.openlocfilehash: 92735262ebc4b48dd1143af57349d77e1fe3061c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124205"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="2396e-103">Veštine i modeli stručnosti</span><span class="sxs-lookup"><span data-stu-id="2396e-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2396e-104">Veštine su karakteristike resursa koje se dele između usluga Dynamics 365 Project Service Automation i Dynamics 365 Field Service (ako postoji).</span><span class="sxs-lookup"><span data-stu-id="2396e-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="2396e-105">Da biste održali spremište veština u usluzi Project Service Automation, idite na **Resursi** \> **Veštine resursa**.</span><span class="sxs-lookup"><span data-stu-id="2396e-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Veštine resursa](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="2396e-107">Koristite modele stručnosti da biste ocenili resurse</span><span class="sxs-lookup"><span data-stu-id="2396e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="2396e-108">Veštine za resurse ocenjuju se prema modelima stručnosti.</span><span class="sxs-lookup"><span data-stu-id="2396e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="2396e-109">Pojedinačne ocene su u modelu stručnosti.</span><span class="sxs-lookup"><span data-stu-id="2396e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="2396e-110">Da biste kreirali model stručnosti, idite na **Resursi** \> **Modeli stručnosti**, a zatim izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="2396e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="2396e-111">U novom modelu ocenjivanja navedite minimalnu vrednost ocenjivanja, maksimalnu vrednost ocenjivanja i entitet koji se ocenjuje.</span><span class="sxs-lookup"><span data-stu-id="2396e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="2396e-112">U podformi **Vrednosti ocena** možete definisati različite vrednosti ocenjivanja, od minimalne do maksimalne.</span><span class="sxs-lookup"><span data-stu-id="2396e-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Definisane su minimalne i maksimalne vrednosti ocenjivanja](media/Resource-Management-image85.png)

<span data-ttu-id="2396e-114">Te vrednosti ocenjivanja su prikazane u filterima **Potrebe za resursima**, **Tabela rasporeda** i **Pomoćnik za zakazivanje**.</span><span class="sxs-lookup"><span data-stu-id="2396e-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
