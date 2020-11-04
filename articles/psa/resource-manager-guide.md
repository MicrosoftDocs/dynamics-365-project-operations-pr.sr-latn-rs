---
title: Vodič za menadžera resursa
description: Vodič za upravljanje resursima u aplikaciji Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 4a26a384dfaf6b974ed35105434152e655ff6444
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083788"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="fa918-103">Vodič za menadžera resursa (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fa918-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fa918-104">Mogućnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sistemu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] vam pomažu da pronađete prave resurse u pravo vreme za pravi projekat i da se postarate da se svi resursi efikasno koriste.</span><span class="sxs-lookup"><span data-stu-id="fa918-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="fa918-105">Primenite konsultante preduzeća efikasno sa rezultatima uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fa918-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="fa918-106">One vam pružaju alatke koje su vam potrebne da isplanirate resursa na osnovu zahteva i rasporeda projekata i veština i dostupnosti savetnika.</span><span class="sxs-lookup"><span data-stu-id="fa918-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="fa918-107">Brzo možete da pronađete najviše kvalifikovane savetnike koji su dostupni za rad na projektima i lako možete da vidite kako da ih bolje planirate tokom svakog projekta.</span><span class="sxs-lookup"><span data-stu-id="fa918-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="fa918-108">Planiranje resursa vam pomaže da uradite sledeće:</span><span class="sxs-lookup"><span data-stu-id="fa918-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="fa918-109">Spojite resurse sa projektima, na osnovu toga kako njihove veštine i nivoi stručnosti odgovaraju zahtevima projekta za resurse.</span><span class="sxs-lookup"><span data-stu-id="fa918-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="fa918-110">Spajanje rasporeda resursa sa kalendarom projekta, na osnovu njihove dostupnosti i planiranog slobodnog vremena.</span><span class="sxs-lookup"><span data-stu-id="fa918-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="fa918-111">Kalendar označen bojama pruža vizuelni prikaz dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="fa918-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="fa918-112">Pregledajte kapacitet svakog savetnika i odredite način na koji se koji kapacitet trenutno koristi.</span><span class="sxs-lookup"><span data-stu-id="fa918-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="fa918-113">Ovo vam može pomoći da pronađete gde je consultant možda u premalo ili previše iskorišćen ili radi u okviru svog kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="fa918-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="fa918-114">Dodelite procenat ili određeni broj časova za kapacitet radnika za projekat.</span><span class="sxs-lookup"><span data-stu-id="fa918-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="fa918-115">Pravite grupne rezervacije resursa.</span><span class="sxs-lookup"><span data-stu-id="fa918-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="fa918-116">Uslovno i fiksno rezervisanje resursa i konvertovanje uslovno rezervisanih sati u fiksno rezervisane sate u jednom koraku.</span><span class="sxs-lookup"><span data-stu-id="fa918-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="fa918-117">Automatski formirajte tim za projekat na osnovu resursa definisanih u strukturnoj analizi posla za projekat.</span><span class="sxs-lookup"><span data-stu-id="fa918-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="fa918-118">Ispunite zahteve za resurse (rezervišite, predlažite, nađite zamenske resurse).</span><span class="sxs-lookup"><span data-stu-id="fa918-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="fa918-119">Dodeljujte resurse u skladu sa centralnim (menadžer resursa dodeljuje) ili hibridnim modelom (menadžer resursa i drugi menadžeri mogu da dodele).</span><span class="sxs-lookup"><span data-stu-id="fa918-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="fa918-120">Više informacija o podešavanju centralnog modela upravljanja resursima naspram hibridnog potražite u članku [Konfigurisanje podešavanja dodatnih parametara (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="fa918-121">Možete da upravljate resursima efikasno u raznim projektima i uverite se da su projektima dodeljeni resursi na odgovarajući način.</span><span class="sxs-lookup"><span data-stu-id="fa918-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="fa918-122">Moraćete da izvršite sledeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="fa918-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="fa918-123">[Upravljanje zahtevima za resurse](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="fa918-124">Spojite veštine i stručnost savetnika sa odgovarajućim projektima.</span><span class="sxs-lookup"><span data-stu-id="fa918-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="fa918-125">[Prikaz dostupnosti resursa](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="fa918-126">Proverite dostupnost savetnika u prikazu kalendara.</span><span class="sxs-lookup"><span data-stu-id="fa918-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="fa918-127">[Prikaz ukupne iskorišćenosti resursa](../psa/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="fa918-128">Pogledajte procenat vremena za koje su vaši savetnici trenutno rezervisani.</span><span class="sxs-lookup"><span data-stu-id="fa918-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="fa918-129">[Planirajte resurse za projekat](../psa/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="fa918-130">Planirajte konsultante za projekat.</span><span class="sxs-lookup"><span data-stu-id="fa918-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="fa918-131">Više informacija o prosleđivanju zahteva za resurse za pojedinačne projekte potražite u članku [Podnošenje zahteva za resurse](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fa918-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fa918-132">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="fa918-132">See Also</span></span>  
 <span data-ttu-id="fa918-133">[Pregled usluge Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="fa918-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="fa918-134">[Vodič za administratore](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fa918-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="fa918-135">[Vodič za menadžera za poslovne kontakte](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fa918-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="fa918-136">[Vodič za menadžera projekta](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fa918-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="fa918-137">Vodič za vreme, trošak i saradnju</span><span class="sxs-lookup"><span data-stu-id="fa918-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
