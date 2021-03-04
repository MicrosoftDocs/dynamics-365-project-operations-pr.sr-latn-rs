---
title: Rezervisanje imenovanih resursa iz potrebe za resursima
description: Ova tema pruža informacije o rezervisanju imenovanih resursa u skladu sa potrebama za generičkim resursima.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c7a6370bde434b74d05e342240abd9bba84d34d8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145123"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="54f2b-103">Rezervisanje imenovanih resursa iz potrebe za resursima</span><span class="sxs-lookup"><span data-stu-id="54f2b-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="54f2b-104">Možete rezervisati imenovani resurs da biste zamenili generički resurs za kojim postoji potreba.</span><span class="sxs-lookup"><span data-stu-id="54f2b-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="54f2b-105">U aplikaciji Project Service Automation (PSA), na stranici **Projekti** kliknite na karticu **Tim**.</span><span class="sxs-lookup"><span data-stu-id="54f2b-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="54f2b-106">Sa liste izaberite generički resurs za kojim postoji potreba, a zatim kliknite na **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="54f2b-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="54f2b-107">Ili otvorite potrebu za resursom, a zatim kliknite na **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="54f2b-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervisanje generičkog člana tima](media/RM-how-to-14.png)


3. <span data-ttu-id="54f2b-109">Na stranici **Pomoćnik za zakazivanje** izaberite imenovani resurs koji ćete rezervisati za projektni tim, a zatim kliknite na **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="54f2b-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervisanje generičkog člana tima pomoću pomoćnika za zakazivanje](media/RM-how-to-15.png)

<span data-ttu-id="54f2b-111">Kada se rezervacija dovrši i ispuni je imenovani resurs, generički resurs se zamenjuje imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="54f2b-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Imenovani član tima koji zamenjuje generičkog člana tima](media/RM-how-to-16.png)

<span data-ttu-id="54f2b-113">Dodele u rasporedu se ažuriraju i imenovanim resursom.</span><span class="sxs-lookup"><span data-stu-id="54f2b-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Imenovani član tima dodeljen projektnim zadacima](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="54f2b-115">Popunjavanje generičkog resursa većim brojem imenovanih resursa</span><span class="sxs-lookup"><span data-stu-id="54f2b-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="54f2b-116">Ispunjavanje zahteva za generički resurs sa više imenovanih resursa je slično dodeljivanju jednog imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="54f2b-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="54f2b-117">Na primer, postoji zadatak sa trajanjem od pet dana i 120 sati truda.</span><span class="sxs-lookup"><span data-stu-id="54f2b-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="54f2b-118">Ovaj zadatak ne može da dovrši jedan resurs koji radi sa tipičnim osmočasovnim radnim danom u sedmici od pet radnih dana.</span><span class="sxs-lookup"><span data-stu-id="54f2b-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Zadatak koji treba 120 sati truda tokom perioda od pet dana](media/RM-how-to-21.png)

<span data-ttu-id="54f2b-120">Zahtev je za 120 sati inženjeringa robotike u toku pet dana, što je 24 časa dnevno.</span><span class="sxs-lookup"><span data-stu-id="54f2b-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Zahtev po danu](media/RM-how-to-22.png)

<span data-ttu-id="54f2b-122">Ovo je primer kada je potrebno više imenovanih resursa za ispunjavanje generičkog zahteva za resurse.</span><span class="sxs-lookup"><span data-stu-id="54f2b-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="54f2b-123">Biće potrebno da rezervišete više resursa da biste ispunili taj zahtev.</span><span class="sxs-lookup"><span data-stu-id="54f2b-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervisanje više resursa radi ispunjavanja zahteva](media/RM-how-to-23.png)

<span data-ttu-id="54f2b-125">Glavna razlika u ovom scenariju je to što generički resurs ostaje u timu koji je dodeljen zadatku, a rezervisani imenovani članovi tima resursa nisu dodeljeni kao deo pozicije.</span><span class="sxs-lookup"><span data-stu-id="54f2b-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="54f2b-126">Menadžer projekta može po potrebi da dodeli posao imenovanim resursima.</span><span class="sxs-lookup"><span data-stu-id="54f2b-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="54f2b-127">Prikaz **Usaglašenost** može da pomogne menadžeru projekta da podeli rezervacije više resursa na zadatke za dodeljivanje.</span><span class="sxs-lookup"><span data-stu-id="54f2b-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="54f2b-128">Ovo se ne radi automatski jer u svakom scenariju komplikovanijem od običnog primera datog iznad, na primer kada imate skup zadataka koji sačinjavaju zahtev, sistem mora da pretpostavi kako menadžer projekta namerava da dodeli resurse.</span><span class="sxs-lookup"><span data-stu-id="54f2b-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="54f2b-129">Pošto sistem ne može da razume nameru, postoje šanse da će se pretpostavke razlikovati od predviđenih, pa će doći do netačnog ili nepredvidivog rezultata.</span><span class="sxs-lookup"><span data-stu-id="54f2b-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="54f2b-130">Predvidiv ishod je da generički resurs ostaje dodeljen dok menadžer projekta namerno ne kreira dodele, uz pomoć prikaza **Usaglašenost**.</span><span class="sxs-lookup"><span data-stu-id="54f2b-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


