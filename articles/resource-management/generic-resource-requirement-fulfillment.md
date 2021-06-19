---
title: Ispunjavanje generičkih zahteva za resursima
description: Ova tema pruža informacije o tome kako da rezervišete imenovane resurse u skladu sa potrebama za generičkim resursima.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e36875a0d5dcb24d9669e2ea989c6fc7db7bcd7c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005853"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="1911b-103">Ispunjavanje generičkih zahteva za resursima</span><span class="sxs-lookup"><span data-stu-id="1911b-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="1911b-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="1911b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1911b-105">Možete rezervisati imenovani resurs da biste zamenili generički resurs za kojim postoji potreba.</span><span class="sxs-lookup"><span data-stu-id="1911b-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="1911b-106">Na stranici **Projekti**, izaberite karticu **Tim**.</span><span class="sxs-lookup"><span data-stu-id="1911b-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="1911b-107">Na listi izaberite generički resurs za kojim postoji potreba, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="1911b-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="1911b-108">Ili otvorite potrebu za resursom, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="1911b-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="1911b-109">Na stranici **Pomoćnik za zakazivanje** izaberite imenovani resurs koji ćete rezervisati za projektni tim, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="1911b-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="1911b-110">Kada se rezervacija dovrši i ispuni je imenovani resurs, generički resurs se zamenjuje imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="1911b-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="1911b-111">Dodele u rasporedu se ažuriraju i imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="1911b-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="1911b-112">Popunjavanje generičkog resursa većim brojem imenovanih resursa</span><span class="sxs-lookup"><span data-stu-id="1911b-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="1911b-113">Ispunjavanje zahteva za generički resurs sa više imenovanih resursa je slično dodeljivanju jednog imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="1911b-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="1911b-114">Na primer, postoji zadatak sa trajanjem od pet dana i 120 sati truda.</span><span class="sxs-lookup"><span data-stu-id="1911b-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="1911b-115">Ovaj zadatak ne može da dovrši jedan resurs koji radi sa tipičnim osmočasovnim radnim danom u sedmici od pet radnih dana.</span><span class="sxs-lookup"><span data-stu-id="1911b-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="1911b-116">Zahtev je za 120 sati inženjeringa robotike u toku pet dana, što je 24 časa dnevno.</span><span class="sxs-lookup"><span data-stu-id="1911b-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="1911b-117">Ovo je primer kada je potrebno više imenovanih resursa za ispunjavanje generičkog zahteva za resurse.</span><span class="sxs-lookup"><span data-stu-id="1911b-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="1911b-118">Biće potrebno da rezervišete više resursa da biste ispunili taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="1911b-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="1911b-119">Glavna razlika u ovom scenariju je to što generički resurs ostaje u timu koji je dodeljen zadatku, a rezervisani imenovani članovi tima resursa nisu dodeljeni kao deo pozicije.</span><span class="sxs-lookup"><span data-stu-id="1911b-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="1911b-120">Menadžer projekta može po potrebi da dodeli posao imenovanim resursima.</span><span class="sxs-lookup"><span data-stu-id="1911b-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="1911b-121">Prikaz **Usaglašenost** može da pomogne menadžeru projekta da podeli rezervacije više resursa na zadatke za dodeljivanje.</span><span class="sxs-lookup"><span data-stu-id="1911b-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="1911b-122">Ovo se ne radi automatski jer u svakom scenariju komplikovanijem od običnog primera datog iznad, na primer kada imate skup zadataka koji sačinjavaju zahtev ili kada sistem mora da pretpostavi kako menadžer projekta namerava da dodeli resurse.</span><span class="sxs-lookup"><span data-stu-id="1911b-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="1911b-123">Pošto sistem ne može da razume nameru, pretpostavke će se verovatno razlikovati od predviđenih, pa će doći do netačnog ili nepredvidivog rezultata.</span><span class="sxs-lookup"><span data-stu-id="1911b-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="1911b-124">Predvidiv ishod je da generički resurs ostaje dodeljen dok menadžer projekta namerno ne kreira dodele, uz pomoć prikaza **Usaglašenost**.</span><span class="sxs-lookup"><span data-stu-id="1911b-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]