---
title: Faze projekta
description: Ova tema pruža informacije o stvarnim fazama projekta.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755140"
---
# <a name="project-stages"></a><span data-ttu-id="7a97f-103">Faze projekta</span><span class="sxs-lookup"><span data-stu-id="7a97f-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7a97f-104">Faze projekta ažuriraju se tako da odražavaju status projekta tokom njegovom napretka.</span><span class="sxs-lookup"><span data-stu-id="7a97f-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="7a97f-105">Podrazumevani tok poslovnog procesa automatski ažurira neke faze projekta, dok druge ručno ažurira menadžer projekta.</span><span class="sxs-lookup"><span data-stu-id="7a97f-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="7a97f-106">Sledeće faze su definisane u podrazumevanom toku poslovnog procesa:</span><span class="sxs-lookup"><span data-stu-id="7a97f-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="7a97f-107">Novo</span><span class="sxs-lookup"><span data-stu-id="7a97f-107">New</span></span>
- <span data-ttu-id="7a97f-108">Ponuda</span><span class="sxs-lookup"><span data-stu-id="7a97f-108">Quote</span></span>
- <span data-ttu-id="7a97f-109">Plan</span><span class="sxs-lookup"><span data-stu-id="7a97f-109">Plan</span></span>
- <span data-ttu-id="7a97f-110">Isporuka</span><span class="sxs-lookup"><span data-stu-id="7a97f-110">Deliver</span></span>
- <span data-ttu-id="7a97f-111">Dovršeno</span><span class="sxs-lookup"><span data-stu-id="7a97f-111">Complete</span></span>
- <span data-ttu-id="7a97f-112">Zatvori</span><span class="sxs-lookup"><span data-stu-id="7a97f-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="7a97f-113">Novo</span><span class="sxs-lookup"><span data-stu-id="7a97f-113">New</span></span>

<span data-ttu-id="7a97f-114">Kada kreirate projekat, faza projekta se podešava na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="7a97f-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="7a97f-115">Ako je projekat kreiran iz predloška, možda će imati raspored, procenu i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="7a97f-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="7a97f-116">U suprotnom, to je samo skica projekta, a preostale komponente moraju biti unete.</span><span class="sxs-lookup"><span data-stu-id="7a97f-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="7a97f-117">Ponuda</span><span class="sxs-lookup"><span data-stu-id="7a97f-117">Quote</span></span>

<span data-ttu-id="7a97f-118">Kada povežete projekat sa ponudom ili ga kreirate iz ponude, faza projekta se podešava na **Ponuda**, a procenjeni datum početka i završetka se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="7a97f-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="7a97f-119">Dok je projekat je u fazi **ponude**, kartica **Prodaja** na stranici **Entitet projekta** prikazuje detalje ponude.</span><span class="sxs-lookup"><span data-stu-id="7a97f-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="7a97f-120">Plan</span><span class="sxs-lookup"><span data-stu-id="7a97f-120">Plan</span></span>

<span data-ttu-id="7a97f-121">Kada vam bude odobrena ponuda povezana sa projektom i kada se projekat prebaci u fazu **ugovora**, faza projekta se ažurira na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="7a97f-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="7a97f-122">Dok je projekat u fazi **plana**, na stranici **Entitet projekta** se prikazuju detalji ugovora.</span><span class="sxs-lookup"><span data-stu-id="7a97f-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="7a97f-123">Isporuka</span><span class="sxs-lookup"><span data-stu-id="7a97f-123">Deliver</span></span>

<span data-ttu-id="7a97f-124">Kada je projektni plan završen, a vi ste spremni za početak projekta, menadžer projekta treba da ažurira fazu projekta na **Isporuka** da bi pokazao da je projekat započet.</span><span class="sxs-lookup"><span data-stu-id="7a97f-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="7a97f-125">Dovršeno</span><span class="sxs-lookup"><span data-stu-id="7a97f-125">Complete</span></span> 

<span data-ttu-id="7a97f-126">Kada je posao za projekat završen, menadžer projekta može da ažurira fazu na **Dovršeno**.</span><span class="sxs-lookup"><span data-stu-id="7a97f-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="7a97f-127">Ažuriranjem faze projekta na **Dovršeno**, menadžer projekta pokazuje da je posao završen 100%, ali da je projekat i dalje otvoren tako da se mogu evidentirati bilo kakve stavke vremena ili troškova na čekanju.</span><span class="sxs-lookup"><span data-stu-id="7a97f-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="7a97f-128">Zatvori</span><span class="sxs-lookup"><span data-stu-id="7a97f-128">Close</span></span>

<span data-ttu-id="7a97f-129">Kada se sve transakcije evidentiraju za projekat, menadžer projekta može da ažurira fazu na **Zatvoreno**.</span><span class="sxs-lookup"><span data-stu-id="7a97f-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="7a97f-130">U tom trenutku ne mogu se evidentirati nikakve transakcije i projekt se podešava na „samo za čitanje“.</span><span class="sxs-lookup"><span data-stu-id="7a97f-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
