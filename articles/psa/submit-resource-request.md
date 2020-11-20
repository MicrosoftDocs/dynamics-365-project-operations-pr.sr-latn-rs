---
title: Prosleđivanje zahteva za resurs
description: Ova tema pruža informacije o prosleđivanju zahteva za resurs projekta.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 50f076b89c5ac7fee4866534cbd47d81f92f3ab3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131301"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="c4229-103">Prosleđivanje zahteva za resurs</span><span class="sxs-lookup"><span data-stu-id="c4229-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c4229-104">Generisanu potrebu za resursom možete proslediti kao zahtev za resurs.</span><span class="sxs-lookup"><span data-stu-id="c4229-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="c4229-105">Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.</span><span class="sxs-lookup"><span data-stu-id="c4229-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="c4229-106">U aplikaciji Project Service Automation (PSA), na stranici **Projekti** kliknite na karticu **Tim** da biste videli listu resursa koji se mogu rezervisati.</span><span class="sxs-lookup"><span data-stu-id="c4229-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="c4229-107">Sa liste izaberite generički resurs koji ima potrebu za resursom, a zatim kliknite na **Prosledi zahtev**.</span><span class="sxs-lookup"><span data-stu-id="c4229-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Prosleđivanje zahteva za resurs](media/RM-how-to-18.png)

<span data-ttu-id="c4229-109">Status zahteva generičkog člana tima će se promeniti u **Prosleđen**.</span><span class="sxs-lookup"><span data-stu-id="c4229-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="c4229-110">Kada menadžer resursa ispuni zahtev, generički resurs će biti zamenjen imenovanim resursom ako menadžer resursa ispuni zahtev rezervisanjem imenovanog resursa.</span><span class="sxs-lookup"><span data-stu-id="c4229-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="c4229-111">U suprotnom, generički resurs će ostati u timu i status zahteva će se promeniti u **Zahteva pregled** ako je menadžer resursa predložio imenovani resurs.</span><span class="sxs-lookup"><span data-stu-id="c4229-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
