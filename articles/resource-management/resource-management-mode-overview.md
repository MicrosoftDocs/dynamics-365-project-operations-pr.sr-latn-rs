---
title: Pregled režima upravljanja resursima
description: Ova tema pruža informacije o funkcionalnosti upravljanja resursima u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930108"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="d8332-103">Pregled režima upravljanja resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-103">Resource management modes overview</span></span>

<span data-ttu-id="d8332-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="d8332-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d8332-105">Dynamics 365 Project Operations podržava dva režima kako biste izvršili ukupan tok rezervacije.</span><span class="sxs-lookup"><span data-stu-id="d8332-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="d8332-106">Režim upravljanja definisan je kao parametar projekta i može se izmeniti ako vaše poslovanje treba promeniti.</span><span class="sxs-lookup"><span data-stu-id="d8332-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="d8332-107">Centralni režim</span><span class="sxs-lookup"><span data-stu-id="d8332-107">Central mode</span></span>
<span data-ttu-id="d8332-108">Za organizacije koje centralizuju dodeljivanje resursa projektima, centralni režim pruža način da menadžeri projekata mogu da definišu zahteve za resursima na nivou projekta.</span><span class="sxs-lookup"><span data-stu-id="d8332-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="d8332-109">Ispunjavanje zahteva za resursima delegira se menadžeru resursa.</span><span class="sxs-lookup"><span data-stu-id="d8332-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="d8332-110">Menadžeri projekata mogu prihvatiti ili odbiti resurse koje predloži menadžer resursa.</span><span class="sxs-lookup"><span data-stu-id="d8332-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centralni režim](./media/resource-management-central.png)

<span data-ttu-id="d8332-112">Da biste upravljali resursima u centralnom režimu, pogledajte:</span><span class="sxs-lookup"><span data-stu-id="d8332-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="d8332-113">Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="d8332-114">Rezervisanje imenovanih resursa iz potrebe za resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="d8332-115">Prosleđivanje zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="d8332-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="d8332-116">Ispunjavanje zahteva za resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="d8332-117">Prihvatanje ili odbacivanje predloženog resursa projekta u zahtevu za resurs</span><span class="sxs-lookup"><span data-stu-id="d8332-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="d8332-118">Hibridni režim</span><span class="sxs-lookup"><span data-stu-id="d8332-118">Hybrid mode</span></span>
<span data-ttu-id="d8332-119">Za organizacije kojima je potrebna fleksibilnost u raspodeli resursa, hibridni režim omogućava menadžerima projekata i menadžerima resursa mogućnost da rezervišu resurse.</span><span class="sxs-lookup"><span data-stu-id="d8332-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibridni režim](./media/resource-management-hybrid.png)

<span data-ttu-id="d8332-121">Pored podržanog procesa centralnog režima, pogledajte sledeće teme da biste upravljali svim ostalim podržanim tokovima rezervacija u hibridnom režimu:</span><span class="sxs-lookup"><span data-stu-id="d8332-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="d8332-122">Rezervisanje resursa direktno u projektu:</span><span class="sxs-lookup"><span data-stu-id="d8332-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="d8332-123">Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka</span><span class="sxs-lookup"><span data-stu-id="d8332-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="d8332-124">Rezervisanje resursa iz zahteva za resursima:</span><span class="sxs-lookup"><span data-stu-id="d8332-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="d8332-125">Dodeljivanje generičkih resursa koji se mogu rezervisati zadatku i generisanje potreba za resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="d8332-126">Rezervisanje imenovanih resursa iz potrebe za resursima</span><span class="sxs-lookup"><span data-stu-id="d8332-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
