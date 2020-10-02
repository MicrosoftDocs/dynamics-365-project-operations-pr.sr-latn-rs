---
title: Konfigurisanje automatskog kreiranja fakture
description: Ova tema pruža informacije o najnovijim načinima konfigurisanja sistema za automatsko generisanje faktura.
author: rumant
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898143"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="e7b78-103">Konfigurisanje automatskog kreiranja fakture</span><span class="sxs-lookup"><span data-stu-id="e7b78-103">Configure automated invoice creation</span></span>

<span data-ttu-id="e7b78-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="e7b78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e7b78-105">Dovršite sledeće korake da biste konfigurisali automatsko pokretanje faktura usluzi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e7b78-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="e7b78-106">Idite do stavke **Podešavanja** \> **Grupni poslovi**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="e7b78-107">Kreirajte grupni posao i imenujte ga **Kreiranje faktura u usluzi Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="e7b78-108">Naziv grupnog posla mora da sadrži termin „kreiranje faktura“.</span><span class="sxs-lookup"><span data-stu-id="e7b78-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="e7b78-109">U polju **Vrsta posla** izaberite **Nijedna**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="e7b78-110">Podrazumevano se opcije **Dnevna učestalost** i **Je aktivna** podešavaju na **Da**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="e7b78-111">Izaberite **Pokreni tok posla**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-111">Select **Run Workflow**.</span></span> <span data-ttu-id="e7b78-112">U dijalogu **Pronalaženje zapisa** ćete videti tri toka posla:</span><span class="sxs-lookup"><span data-stu-id="e7b78-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="e7b78-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="e7b78-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="e7b78-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="e7b78-114">ProcessRunner</span></span>
    - <span data-ttu-id="e7b78-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="e7b78-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="e7b78-116">Izaberite **ProcessRunCaller**, a zatim **Dodaj**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="e7b78-117">U sledećem dijalogu izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="e7b78-118">Tok posla **Hibernacija** prati tok posla **Proces**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="e7b78-119">Možete izabrati i **ProcessRunner** u koraku 5.</span><span class="sxs-lookup"><span data-stu-id="e7b78-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="e7b78-120">Nakon toga, kada izaberete **U redu**, tok posla **Proces** će biti praćen tokom posla **Hibernacija**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="e7b78-121">Tokovi posla **ProcessRunCaller** i **ProcessRunner** kreiraju fakture.</span><span class="sxs-lookup"><span data-stu-id="e7b78-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="e7b78-122">**ProcessRunCaller** poziva **ProcessRunner**.</span><span class="sxs-lookup"><span data-stu-id="e7b78-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="e7b78-123">**ProcessRunner** je tok posla koji zapravo kreira fakture.</span><span class="sxs-lookup"><span data-stu-id="e7b78-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="e7b78-124">On prolazi kroz sve predmete ugovora za koje se moraju kreirati fakture i kreira fakture za te predmete.</span><span class="sxs-lookup"><span data-stu-id="e7b78-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="e7b78-125">Da bi odredio predmete ugovora za koje fakture moraju biti kreirane, posao traži datume pokretanja fakture za predmete ugovora.</span><span class="sxs-lookup"><span data-stu-id="e7b78-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="e7b78-126">Ako predmeti ugovora koji pripadaju jednom ugovoru imaju isti datum pokretanja fakture, transakcije se kombinuju u jednu fakturu koja ima dve stavke fakture.</span><span class="sxs-lookup"><span data-stu-id="e7b78-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="e7b78-127">Ako ne postoje transakcije za koje treba kreirati fakture, posao preskače kreiranje fakture.</span><span class="sxs-lookup"><span data-stu-id="e7b78-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="e7b78-128">Nakon što se **ProcessRunner** pokrene, on poziva **ProcessRunCaller**, obezbeđuje vreme završetka i zatvara se.</span><span class="sxs-lookup"><span data-stu-id="e7b78-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="e7b78-129">**ProcessRunCaller** zatim pokreće tajmer koji će biti pokrenut tokom perioda od 24 časa od određenog vremena završetka.</span><span class="sxs-lookup"><span data-stu-id="e7b78-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="e7b78-130">Na kraju tajmera **ProcessRunCaller** se zatvara.</span><span class="sxs-lookup"><span data-stu-id="e7b78-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="e7b78-131">Posao grupne obrade za kreiranje faktura je periodični posao.</span><span class="sxs-lookup"><span data-stu-id="e7b78-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="e7b78-132">Ako se ova grupna obrada pokreće više puta, kreira se više instanci posla i izazivaju greške.</span><span class="sxs-lookup"><span data-stu-id="e7b78-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="e7b78-133">Zbog toga bi trebalo samo jednom da pokrenete grupnu obradu i trebalo bi da je ponovo pokrenete samo ako prestane da radi.</span><span class="sxs-lookup"><span data-stu-id="e7b78-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="e7b78-134">Grupno fakturisanje se izvodi samo za predmete ugovora o projektu koji su konfigurisani prema rasporedima faktura.</span><span class="sxs-lookup"><span data-stu-id="e7b78-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="e7b78-135">Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="e7b78-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="e7b78-136">Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma.</span><span class="sxs-lookup"><span data-stu-id="e7b78-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="e7b78-137">Isto se odnosi i na predmet ugovora zasnovan na projektu.</span><span class="sxs-lookup"><span data-stu-id="e7b78-137">The same applies to a project-based contract line.</span></span>     
