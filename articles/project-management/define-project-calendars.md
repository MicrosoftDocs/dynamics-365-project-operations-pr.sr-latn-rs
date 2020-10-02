---
title: Definisanje kalendara projekata
description: Ova tema pruža informacije o korišćenju kalendara projekta za praćenje rasporeda projekata.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 1d44a2d0d8c13fb9e93b9a6da15fb3a7ce8d764c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898025"
---
# <a name="define-project-calendars"></a><span data-ttu-id="ff5a1-103">Definisanje kalendara projekata</span><span class="sxs-lookup"><span data-stu-id="ff5a1-103">Define project calendars</span></span>

<span data-ttu-id="ff5a1-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ff5a1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ff5a1-105">Da biste kreirali raspored projekta, kreirajte predložak kalendara projekta koji definiše broj radnih sati po danu i sve prekide poslovnih aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="ff5a1-106">Da biste kreirali predložak kalendara projekta, radni predložak povezujete sa poljem **Predložak kalendara** za projekat.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="ff5a1-107">Sledite ove korake za kreiranje radnog predloška.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="ff5a1-108">U levom oknu za navigaciju izaberite **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="ff5a1-109">Na stranici liste **Resursi** otvorite zapis korisnika, a zatim izaberite **Prikaži radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="ff5a1-110">Obavezno dozvolite iskačuće prozore na stranici pregledača.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="ff5a1-111">Ovo vam omogućava da vidite radno vreme podešeno za resurs.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="ff5a1-112">Na kartici **Mesečni prikaz** izaberite **Podešavanje**.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="ff5a1-113">Pojaviće se lista sa tri opcije:</span><span class="sxs-lookup"><span data-stu-id="ff5a1-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="ff5a1-114">Novi sedmični raspored</span><span class="sxs-lookup"><span data-stu-id="ff5a1-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="ff5a1-115">Raspored posla za jedan dan</span><span class="sxs-lookup"><span data-stu-id="ff5a1-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="ff5a1-116">Odstupanje u vremenu</span><span class="sxs-lookup"><span data-stu-id="ff5a1-116">Time Off</span></span>

4. <span data-ttu-id="ff5a1-117">Izaberite **Novi sedmični raspored**, a zatim podesite opcije za ovaj raspored resursa.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="ff5a1-118">Možete podesiti periodični sedmični raspored, parametre sata u danu, prekid poslovnih aktivnosti i još mnogo toga.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="ff5a1-119">Podesite opseg datuma, izaberite **Sačuvaj**, a zatim izaberite **Zatvori**.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="ff5a1-120">Vratite se na stranicu liste **Resursi** i odaberite resurs za koji ste odredili radno vreme.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="ff5a1-121">Izaberite **Podesite kalendar kao** da podesite radni predložak.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="ff5a1-122">U dijalog **Radni predložak** unesite ime radnog predloška, a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="ff5a1-123">Sada možete povezati radni predložak sa predloškom kalendara projekta.</span><span class="sxs-lookup"><span data-stu-id="ff5a1-123">You can now associate the work template with a project calendar template.</span></span>
