---
title: Definisanje kalendara projekata
description: Ova tema pruža informacije o tome kako primeniti šablon kalendara na projekat za praćenje rasporeda projekata.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999013"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d0c7d-103">Definisanje kalendara projekata</span><span class="sxs-lookup"><span data-stu-id="d0c7d-103">Define project calendars</span></span>

<span data-ttu-id="d0c7d-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="d0c7d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0c7d-105">Da biste kreirali i upravljali projektom, na njega morate primeniti šablon kalendara.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="d0c7d-106">Predložak kalendara definiše sledeće atribute projekta:</span><span class="sxs-lookup"><span data-stu-id="d0c7d-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="d0c7d-107">Radno vreme, uključujući vreme početka i završetka</span><span class="sxs-lookup"><span data-stu-id="d0c7d-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="d0c7d-108">Radni dani</span><span class="sxs-lookup"><span data-stu-id="d0c7d-108">Working days</span></span>
- <span data-ttu-id="d0c7d-109">Izuzeci iz kalendara kao što su neradni dani</span><span class="sxs-lookup"><span data-stu-id="d0c7d-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="d0c7d-110">Šablon kalendara koji se primenjuje na projekat je kopija šablona kalendara definisanog u podešavanjima vaše organizacije.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="d0c7d-111">Ako promenite šablon kalendara, te promene se neće preneti na radno vreme projekta.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="d0c7d-112">Da biste promenili radno vreme projekta, mora se primeniti novi obrazac.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="d0c7d-113">Da biste kreirali šablon kalendara za svoju organizaciju, postoje dva ključna zahteva:</span><span class="sxs-lookup"><span data-stu-id="d0c7d-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="d0c7d-114">Definišite željeno radno vreme šablona pomoću novog ili postojećeg resursa koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="d0c7d-115">Napravite novi šablon kalendara i povežite ga sa resursom koji možete rezervirati.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="d0c7d-116">**Definišite radno vreme šablona**</span><span class="sxs-lookup"><span data-stu-id="d0c7d-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="d0c7d-117">Idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="d0c7d-118">Napravite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="d0c7d-119">Izaberite karticu resursa **Radno vreme** i dovršite uputstva u [Postavite radno vreme za resurs](/dynamics365/field-service/set-work-hours-resource.md) za konfigurisanje pravila kalendara.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="d0c7d-120">**Kreirajte novi predložak kalendara**</span><span class="sxs-lookup"><span data-stu-id="d0c7d-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="d0c7d-121">Idite na **Podešavanja** \> **Šablon kalendara**.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="d0c7d-122">Izaberite **Novo** i unesite ime, opis i resurs šablona.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d0c7d-123">Kada se na resurs navodi šablon kalendara, kopija kalendara resursa pridružuje se šablonu kalendara.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="d0c7d-124">Ako promenite radno vreme kopiranog šablona, te promene se neće preneti na radno vreme kalendara.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="d0c7d-125">Sada možete povezati radni predložak sa predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="d0c7d-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

