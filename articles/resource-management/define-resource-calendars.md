---
title: Definisanje kalendara resursa
description: Ova tema pruža informacije o tome kako se definišu kalendari radnog vremena za resurse u usluzi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961936"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="a422d-103">Definisanje kalendara resursa</span><span class="sxs-lookup"><span data-stu-id="a422d-103">Define resource calendars</span></span>

<span data-ttu-id="a422d-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="a422d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a422d-105">Svaki resurs koji može da se rezerviše koji radi na projektu mora imati kalendar radnog vremena da bi se definisala njegova dostupnost.</span><span class="sxs-lookup"><span data-stu-id="a422d-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="a422d-106">Radno vreme resursa može se definisati na dva načina:</span><span class="sxs-lookup"><span data-stu-id="a422d-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="a422d-107">Definišite pojedinačna pravila kalendara za resurs</span><span class="sxs-lookup"><span data-stu-id="a422d-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="a422d-108">Primenite postojeći predložak kalendara za resurs</span><span class="sxs-lookup"><span data-stu-id="a422d-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="a422d-109">Definišite radno vreme resursa</span><span class="sxs-lookup"><span data-stu-id="a422d-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="a422d-110">U meniju **Resursi** izaberite **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="a422d-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="a422d-111">Iz prikaza mreže odaberite primenjiv **Resurs koji može da se rezerviše**.</span><span class="sxs-lookup"><span data-stu-id="a422d-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="a422d-112">Na stranici **Detalji resursa** izaberite karticu **Radno vreme**. Podrazumevano je da kalendar resursa mogu da se rezervišu podrazumeva radno vreme podrazumevanog obrasca radnog vremena koji je definisan za organizaciju.</span><span class="sxs-lookup"><span data-stu-id="a422d-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="a422d-113">Da biste ažurirali radno vreme, kliknite desnim tasterom miša na datum početka predloženog kalendarskog pravila koje treba definisati.</span><span class="sxs-lookup"><span data-stu-id="a422d-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="a422d-114">Pomoću menija kalendara definišite pravilo kalendara za određeni dan, ostatak serije ili ceo kalendar.</span><span class="sxs-lookup"><span data-stu-id="a422d-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="a422d-115">Kada izaberete opciju, možete definisati:</span><span class="sxs-lookup"><span data-stu-id="a422d-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="a422d-116">Dan u nedelji u kome će se primenjivati radno vreme.</span><span class="sxs-lookup"><span data-stu-id="a422d-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="a422d-117">Radno vreme svakog dana.</span><span class="sxs-lookup"><span data-stu-id="a422d-117">The working times within each day.</span></span>
    - <span data-ttu-id="a422d-118">Vremenska zona za pravilo kalendara.</span><span class="sxs-lookup"><span data-stu-id="a422d-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="a422d-119">Ako je primenljivo, za rad se takođe može navesti neradno vreme.</span><span class="sxs-lookup"><span data-stu-id="a422d-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="a422d-120">Primena predloška kalendara na resurs</span><span class="sxs-lookup"><span data-stu-id="a422d-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="a422d-121">U meniju **Resursi** izaberite **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="a422d-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="a422d-122">Iz prikaza mreže izaberite do 25 **resursa koji mogu dase rezervišu** da biste ih ažurirali.</span><span class="sxs-lookup"><span data-stu-id="a422d-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="a422d-123">Izaberite**Podesi kalendar** i pojaviće se dijalog sa listom dostupnih predložaka radnog vremena.</span><span class="sxs-lookup"><span data-stu-id="a422d-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="a422d-124">Izaberite predložak koji želite da koristite, a zatim izaberite dugme **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="a422d-124">Select the template you want to use, and then select **Apply**.</span></span>
