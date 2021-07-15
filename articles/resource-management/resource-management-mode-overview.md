---
title: Pregled režima upravljanja resursima
description: U ovoj temi date su informacije o funkciji upravljanja resursima u usluzi Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367908"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="a790d-103">Pregled režima upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-103">Resource management modes overview</span></span>

<span data-ttu-id="a790d-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="a790d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a790d-105">Dynamics 365 Project Operations podržava dva režima kako biste izvršavali ukupan tok rezervacije.</span><span class="sxs-lookup"><span data-stu-id="a790d-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="a790d-106">Režim upravljanja definisan je kao parametar projekta i može se izmeniti ako vaše poslovanje treba promeniti.</span><span class="sxs-lookup"><span data-stu-id="a790d-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="a790d-107">Centralni režim</span><span class="sxs-lookup"><span data-stu-id="a790d-107">Central mode</span></span>
<span data-ttu-id="a790d-108">Za organizacije koje centralizuju dodeljivanje resursa projektima, centralni režim pruža način da menadžeri projekata mogu da definišu zahteve za resursima na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="a790d-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="a790d-109">Ispunjavanje zahteva za resursima delegira se menadžeru resursa.</span><span class="sxs-lookup"><span data-stu-id="a790d-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="a790d-110">Menadžeri projekata mogu prihvatiti ili odbiti resurse koje predloži menadžer resursa.</span><span class="sxs-lookup"><span data-stu-id="a790d-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centralni režim](./media/resource-management-central.png)

<span data-ttu-id="a790d-112">Da biste upravljali resursima u centralnom režimu, pogledajte:</span><span class="sxs-lookup"><span data-stu-id="a790d-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="a790d-113">Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a790d-114">Rezervisanje imenovanih resursa iz potrebe za resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="a790d-115">Prosleđivanje zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="a790d-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="a790d-116">Ispunjavanje zahteva za resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="a790d-117">Prihvatanje ili odbacivanje predloženog resursa projekta u zahtevu za resurs</span><span class="sxs-lookup"><span data-stu-id="a790d-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="a790d-118">Hibridni režim</span><span class="sxs-lookup"><span data-stu-id="a790d-118">Hybrid mode</span></span>
<span data-ttu-id="a790d-119">Za organizacije kojima je potrebna fleksibilnost u raspodeli resursa, hibridni režim omogućava menadžerima projekata i menadžerima resursa mogućnost da rezervišu resurse.</span><span class="sxs-lookup"><span data-stu-id="a790d-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibridni režim](./media/resource-management-hybrid.png)

<span data-ttu-id="a790d-121">Pored podržanog procesa centralnog režima, pogledajte sledeće teme da biste upravljali svim ostalim podržanim tokovima rezervacija u hibridnom režimu:</span><span class="sxs-lookup"><span data-stu-id="a790d-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="a790d-122">Rezervisanje resursa direktno u projektu:</span><span class="sxs-lookup"><span data-stu-id="a790d-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="a790d-123">Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka</span><span class="sxs-lookup"><span data-stu-id="a790d-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="a790d-124">Rezervisanje resursa iz zahteva za resursima:</span><span class="sxs-lookup"><span data-stu-id="a790d-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="a790d-125">Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a790d-126">Rezervisanje imenovanih resursa iz potrebe za resursima</span><span class="sxs-lookup"><span data-stu-id="a790d-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]