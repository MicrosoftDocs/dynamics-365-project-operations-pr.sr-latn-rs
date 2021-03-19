---
title: Prosleđivanje zahteva za resursom
description: Generisanu potrebu za resursom možete proslediti kao zahtev za resurs. Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279155"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="e8281-104">Prosleđivanje zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="e8281-104">Submit a resource request</span></span>

<span data-ttu-id="e8281-105">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="e8281-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e8281-106">Generisanu potrebu za resursom možete proslediti kao zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="e8281-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="e8281-107">Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.</span><span class="sxs-lookup"><span data-stu-id="e8281-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="e8281-108">U aplikaciji Dynamics 365 Project Operations, na stranici **Projekti** izaberite karticu **Tim** da biste videli listu resursa koji se mogu rezervisati.</span><span class="sxs-lookup"><span data-stu-id="e8281-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="e8281-109">Sa liste izaberite generički resurs koji ima potrebu za resursom, a zatim kliknite na **Prosledi zahtev**.</span><span class="sxs-lookup"><span data-stu-id="e8281-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="e8281-110">Status zahteva generičkog člana tima će se promeniti u **Prosleđen**.</span><span class="sxs-lookup"><span data-stu-id="e8281-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="e8281-111">Kada se zahtev ispuni, generički resurs se menja imenovanim resursom ako menadžer resursa ispuni zahtev rezervisanjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="e8281-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="e8281-112">U suprotnom, ako menadžer resursa predloži imenovani resurs, generički resurs ostaje u timu i status zahteva će se promeniti u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="e8281-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]