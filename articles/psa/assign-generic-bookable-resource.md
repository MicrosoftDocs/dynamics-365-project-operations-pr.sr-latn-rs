---
title: Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i projektnom timu
description: Ova tema pruža informacije o rezervisanju generičkih resursa za zadatke i timove projekta.
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
ms.openlocfilehash: 19761b3e570ad664522e832069a8ac50fffead64
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127085"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="0b9cb-103">Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="0b9cb-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0b9cb-104">Pored rezervisanja i dodeljivanja imenovanih ili stvarnih resursa projektu, možete da dodelite generičke resurse projektnim zadacima.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="0b9cb-105">Ti resursi mogu da posluže kao čuvari mesta za imenovane resurse dok ne budete spremni da kao angažovane osobe na projektu koristite imenovane resurse.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="0b9cb-106">U aplikaciji Project Service Automation (PSA) otvorite stranicu **Projekat** i na kartici **Raspored** unesite ime uloge generičkog resursa u ćeliju rasporeda **Resurs**.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="0b9cb-107">Možete i da kliknete na ikonu **Resurs** u ćeliji da biste otvorili birač resursa, a zatim uneli ime generičkog resursa koji želite da kreirate.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Kreiranje i dodeljivanje generičkog člana tima](media/RM-how-to-9.png)

<span data-ttu-id="0b9cb-109">Tako ćete otvoriti tablu **Brzo kreiranje člana projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="0b9cb-110">Unesite ulogu i organizacionu jedinicu generičkog člana tima resursa, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Brzo kreiranje generičkog člana tima](media/RM-how-to-10.png)

3. <span data-ttu-id="0b9cb-112">Nakon što ste kreirali novog generičkog člana tima resursa, on će biti dodeljen zadatku.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="0b9cb-113">Možete nastaviti da dodeljujete taj generički resurs drugim zadacima u rasporedu zadataka.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Dodeljivanje postojećeg generičkog člana tima zadacima](media/RM-how-to-11.png)

4. <span data-ttu-id="0b9cb-115">Nakon što ste dodelili generički resurs, možete da generišete potrebu za resursom i da je ispunite direktnim rezervisanjem ili prosleđivanjem zahteva za resurs menadžeru resursa.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generisanje zahteva za generičkog člana tima](media/RM-how-to-12.png)

<span data-ttu-id="0b9cb-117">U mreži za članove tima, pored toga što možete da koristite birač resursa kao što je pomenuto gore, moći ćete direktno da dodate generičke resurse.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="0b9cb-118">Resursi se dodaju pomoću potreba za resursima koje se zasnivaju na datumu početka/završetka i metodi dodele koja je navedena u tabli **Brzo kreiranje člana projektnog tima**.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="0b9cb-119">Možete videti razliku ako direktno dodate generičkog člana tima, a zatim dodelite još zadataka generičkom resursu od broja sati koje taj resurs može da pokrije.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="0b9cb-120">Kliknite na **Generiši zahtev** da biste ponovo generisali zahtev i balansirali zahtevane sate u odnosu na dodeljene zadatke.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="0b9cb-121">Takođe možete da kliknete na vezu **Potreba za resursom** u mreži tima da biste otvorili zahtev i dodali veštine, željene resurse itd.</span><span class="sxs-lookup"><span data-stu-id="0b9cb-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Zahtev za resursima](media/RM-how-to-13.png)

