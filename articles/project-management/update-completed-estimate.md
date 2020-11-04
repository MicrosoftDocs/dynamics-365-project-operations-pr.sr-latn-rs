---
title: Ažuriranje procene po završetku
description: Ova tema pruža informacije o ažuriranju projekcije angažovanja na projektu.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16393133a5de17308caceb069d7bca670caa04c8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083763"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="fc6c6-103">Ažuriranje procene po završetku</span><span class="sxs-lookup"><span data-stu-id="fc6c6-103">Update estimate at completion</span></span>

<span data-ttu-id="fc6c6-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="fc6c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fc6c6-105">Uobičajeno je da menadžer projekta revidira originalne procene zadatka.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="fc6c6-106">Ponovne projekcije projekata predstavljaju način na koji menadžer projekta percipira procene, s obzirom na trenutni status projekta.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="fc6c6-107">Međutim, ne preporučujemo da menadžeri projekta menjaju osnovne vrednosti zato što osnovne vrednosti projekta predstavljaju uspostavljen izvor istine za raspored projekta i procenu troškova, a svi zainteresovani za projekat su je prihvatili.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="fc6c6-108">Postoje dva načina na koje menadžer projekta može ponovo da projektuje angažovanje na zadacima:</span><span class="sxs-lookup"><span data-stu-id="fc6c6-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="fc6c6-109">Izmenite podrazumevanu procenu završetka (ETC) novom procenom stvarnog preostalog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="fc6c6-110">Izmenite podrazumevani procenat napretka novom procenom stvarnog napretka zadatka.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="fc6c6-111">Svaki od ovih pristupa dovodi do toga da se ponovo izračunaju ETC, procena završetka (EAC) i procenat napretka zadatka, kao i odstupanje od projektovanog angažovanja na zadatku.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="fc6c6-112">EAC, ETC i procenat napretka u rezimiranim zadacima se ponovo izračunavaju i stvaraju novu projekciju odstupanja od angažovanja.</span><span class="sxs-lookup"><span data-stu-id="fc6c6-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
