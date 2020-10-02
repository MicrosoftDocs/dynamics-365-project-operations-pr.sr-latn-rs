---
title: Faze projekta
description: Ova tema pruža informacije o fazama projekta koje su dostupne u usluzi Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897963"
---
# <a name="project-stages"></a><span data-ttu-id="7a5de-103">Faze projekta</span><span class="sxs-lookup"><span data-stu-id="7a5de-103">Project stages</span></span>

<span data-ttu-id="7a5de-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="7a5de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7a5de-105">Faze projekta se dizajniraju tako da odražavaju status projekta tokom njegovog napretka.</span><span class="sxs-lookup"><span data-stu-id="7a5de-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="7a5de-106">Prilagođavanja se mogu koristiti za automatsko ažuriranje faza sa tokovima poslovnih procesa, Power Automate ili proširenja dodatnih komponenti.</span><span class="sxs-lookup"><span data-stu-id="7a5de-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="7a5de-107">Sledeće faze su definisane u podrazumevanom toku poslovnog procesa:</span><span class="sxs-lookup"><span data-stu-id="7a5de-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="7a5de-108">Novi</span><span class="sxs-lookup"><span data-stu-id="7a5de-108">New</span></span>
- <span data-ttu-id="7a5de-109">Ponuda</span><span class="sxs-lookup"><span data-stu-id="7a5de-109">Quote</span></span>
- <span data-ttu-id="7a5de-110">Plan</span><span class="sxs-lookup"><span data-stu-id="7a5de-110">Plan</span></span>
- <span data-ttu-id="7a5de-111">Isporuka</span><span class="sxs-lookup"><span data-stu-id="7a5de-111">Deliver</span></span>
- <span data-ttu-id="7a5de-112">Dovršite</span><span class="sxs-lookup"><span data-stu-id="7a5de-112">Complete</span></span>
- <span data-ttu-id="7a5de-113">Zatvaranje</span><span class="sxs-lookup"><span data-stu-id="7a5de-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="7a5de-114">Novi</span><span class="sxs-lookup"><span data-stu-id="7a5de-114">New</span></span>

<span data-ttu-id="7a5de-115">Kada kreirate projekat, faza projekta se podešava na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="7a5de-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="7a5de-116">Ako je projekat kreiran iz predloška, možda će imati raspored, procenu i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="7a5de-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="7a5de-117">U suprotnom, to je skica projekta, a preostale komponente moraju biti unete.</span><span class="sxs-lookup"><span data-stu-id="7a5de-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="7a5de-118">Ponuda</span><span class="sxs-lookup"><span data-stu-id="7a5de-118">Quote</span></span>

<span data-ttu-id="7a5de-119">Kada povežete projekat sa ponudom ili ga kreirate iz ponude, faza projekta se podešava na **Ponuda**, a procenjeni datum početka i završetka se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="7a5de-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="7a5de-120">Dok je projekat je u fazi **ponude**, kartica **Prodaja** na stranici **Entitet projekta** prikazuje detalje ponude.</span><span class="sxs-lookup"><span data-stu-id="7a5de-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="7a5de-121">Plan</span><span class="sxs-lookup"><span data-stu-id="7a5de-121">Plan</span></span>

<span data-ttu-id="7a5de-122">Kada vam bude odobrena ponuda povezana sa projektom i kada se projekat prebaci u fazu **ugovora**, faza projekta se ažurira na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="7a5de-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="7a5de-123">Dok je projekat u fazi **plana**, na stranici **Entitet projekta** se prikazuju detalji ugovora.</span><span class="sxs-lookup"><span data-stu-id="7a5de-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="7a5de-124">Isporuka</span><span class="sxs-lookup"><span data-stu-id="7a5de-124">Deliver</span></span>

<span data-ttu-id="7a5de-125">Kada je projektni plan završen, a vi ste spremni za početak projekta, menadžer projekta treba da ažurira fazu projekta na **Isporuka** da bi pokazao da je projekat započet.</span><span class="sxs-lookup"><span data-stu-id="7a5de-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="7a5de-126">Dovršeno</span><span class="sxs-lookup"><span data-stu-id="7a5de-126">Complete</span></span> 

<span data-ttu-id="7a5de-127">Kada je posao za projekat završen, menadžer projekta može da ažurira fazu na **Dovršeno**.</span><span class="sxs-lookup"><span data-stu-id="7a5de-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="7a5de-128">Ažuriranjem faze projekta na **Dovršeno**, menadžer projekta pokazuje da je posao završen 100%, ali da je projekat i dalje otvoren tako da se mogu evidentirati bilo kakve stavke vremena ili troškova na čekanju.</span><span class="sxs-lookup"><span data-stu-id="7a5de-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="7a5de-129">Zatvori</span><span class="sxs-lookup"><span data-stu-id="7a5de-129">Close</span></span>

<span data-ttu-id="7a5de-130">Kada se sve transakcije evidentiraju za projekat, menadžer projekta može da ažurira fazu na **Zatvoreno**.</span><span class="sxs-lookup"><span data-stu-id="7a5de-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="7a5de-131">U tom trenutku ne mogu se evidentirati nikakve transakcije i projekt se podešava na „samo za čitanje“.</span><span class="sxs-lookup"><span data-stu-id="7a5de-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
