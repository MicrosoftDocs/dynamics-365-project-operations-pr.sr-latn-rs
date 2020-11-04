---
title: Prosleđivanje zahteva za resursom
description: Generisanu potrebu za resursom možete proslediti kao zahtev za resurs. Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083474"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="84689-104">Prosleđivanje zahteva za resursom</span><span class="sxs-lookup"><span data-stu-id="84689-104">Submit a resource request</span></span>

<span data-ttu-id="84689-105">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="84689-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84689-106">Generisanu potrebu za resursom možete proslediti kao zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="84689-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="84689-107">Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.</span><span class="sxs-lookup"><span data-stu-id="84689-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="84689-108">U usluzi Dynamics 365 Project Operations, na stranici **Projekti** izaberite karticu **Tim** da biste videli listu resursa koji se mogu rezervisati.</span><span class="sxs-lookup"><span data-stu-id="84689-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="84689-109">Sa liste izaberite generički resurs koji ima potrebu za resursom, a zatim kliknite na **Prosledi zahtev**.</span><span class="sxs-lookup"><span data-stu-id="84689-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="84689-110">Status zahteva generičkog člana tima će se promeniti u **Prosleđen**.</span><span class="sxs-lookup"><span data-stu-id="84689-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="84689-111">Kada se zahtev ispuni, generički resurs se menja imenovanim resursom ako menadžer resursa ispuni zahtev rezervisanjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="84689-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="84689-112">U suprotnom, ako menadžer resursa predloži imenovani resurs, generički resurs ostaje u timu i status zahteva će se promeniti u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="84689-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
