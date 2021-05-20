---
title: Kreiranje predloška za radne sate
description: Ova tema opisuje kako da kreirate predloške za radne sate u aplikaciji Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981272"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="97e5a-103">Kreiranje predloška radnih sati (Project Service)</span><span class="sxs-lookup"><span data-stu-id="97e5a-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="97e5a-104">Da biste kreirali i upravljali projektom, na njega morate primeniti šablon kalendara.</span><span class="sxs-lookup"><span data-stu-id="97e5a-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="97e5a-105">Predložak kalendara definiše sledeće atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="97e5a-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="97e5a-106">Radno vreme, uključujući vreme početka i završetka</span><span class="sxs-lookup"><span data-stu-id="97e5a-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="97e5a-107">Radni dani</span><span class="sxs-lookup"><span data-stu-id="97e5a-107">Working days</span></span>
- <span data-ttu-id="97e5a-108">Izuzeci iz kalendara kao što su neradni dani</span><span class="sxs-lookup"><span data-stu-id="97e5a-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="97e5a-109">Šablon kalendara koji se primenjuje na projekat je kopija šablona kalendara definisanog u podešavanjima vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="97e5a-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="97e5a-110">Ako promenite šablon kalendara, te promene se neće preneti na radno vreme projekta.</span><span class="sxs-lookup"><span data-stu-id="97e5a-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="97e5a-111">Da biste promenili radno vreme projekta, mora se primeniti novi obrazac.</span><span class="sxs-lookup"><span data-stu-id="97e5a-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="97e5a-112">Da biste kreirali šablon kalendara za svoju organizaciju, postoje dva ključna zahteva:</span><span class="sxs-lookup"><span data-stu-id="97e5a-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="97e5a-113">Definišite željeno radno vreme šablona pomoću novog ili postojećeg resursa koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="97e5a-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="97e5a-114">Napravite novi šablon kalendara i povežite ga sa resursom koji možete rezervirati.</span><span class="sxs-lookup"><span data-stu-id="97e5a-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="97e5a-115">**Definišite radno vreme šablona**</span><span class="sxs-lookup"><span data-stu-id="97e5a-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="97e5a-116">Idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="97e5a-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="97e5a-117">Napravite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.</span><span class="sxs-lookup"><span data-stu-id="97e5a-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="97e5a-118">Izaberite karticu resursa **Radno vreme** i dovršite uputstva u [Postavite radno vreme za resurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) za konfigurisanje pravila kalendara.</span><span class="sxs-lookup"><span data-stu-id="97e5a-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="97e5a-119">**Kreirajte novi predložak kalendara**</span><span class="sxs-lookup"><span data-stu-id="97e5a-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="97e5a-120">Idite na **Podešavanja** \> **Šablon kalendara**.</span><span class="sxs-lookup"><span data-stu-id="97e5a-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="97e5a-121">Izaberite **Novo** i unesite ime, opis i resurs šablona.</span><span class="sxs-lookup"><span data-stu-id="97e5a-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="97e5a-122">Kada se na resurs navodi šablon kalendara, kopija kalendara resursa pridružuje se šablonu kalendara.</span><span class="sxs-lookup"><span data-stu-id="97e5a-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="97e5a-123">Ako promenite radno vreme kopiranog šablona, te promene se neće preneti na radno vreme kalendara.</span><span class="sxs-lookup"><span data-stu-id="97e5a-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="97e5a-124">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="97e5a-124">See Also</span></span>  
 [<span data-ttu-id="97e5a-125">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="97e5a-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
