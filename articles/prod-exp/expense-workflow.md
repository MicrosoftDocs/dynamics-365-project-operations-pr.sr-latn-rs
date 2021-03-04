---
title: Tok posla za upravljanje troškovima
description: Ova tema objašnjava kako možete da koristite sistem tokova posla u usluzi Microsoft Dynamics 365 Finance, da biste uspostavili postupak pregleda izveštaja o troškovima u upravljanju troškovima.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960579"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="ba186-103">Tok posla za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="ba186-103">Expense management workflow</span></span>

<span data-ttu-id="ba186-104">Možete da koristite sistem tokova posla da biste uspostavili postupak pregleda izveštaja o troškovima u upravljanju troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="ba186-105">Možete da podesite tok posla koji koristi sledeće kriterijume da biste odredili ko odobrava izveštaje o troškovima:</span><span class="sxs-lookup"><span data-stu-id="ba186-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="ba186-106">Hijerarhija izveštavanja zaposlenih i unapred definisana ograničenja odobrenja</span><span class="sxs-lookup"><span data-stu-id="ba186-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="ba186-107">Odobravanje na više nivoa koje podržava privremene i konačne davaoce odobrenja</span><span class="sxs-lookup"><span data-stu-id="ba186-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="ba186-108">Finansijske dimenzije i projektna odgovornost</span><span class="sxs-lookup"><span data-stu-id="ba186-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="ba186-109">Dodeljivanje određenim korisnicima ili grupama korisnika</span><span class="sxs-lookup"><span data-stu-id="ba186-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="ba186-110">Odobravanja tokova posla mogu se kreirati za izveštaje o troškovima, zahteva za putovanje, akontacije i povraćaj poreza na dodatu vrednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="ba186-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="ba186-111">**Primer**</span><span class="sxs-lookup"><span data-stu-id="ba186-111">**Example**</span></span>

<span data-ttu-id="ba186-112">Sledeći postupak je primer toka posla za upravljanje troškovima za izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="ba186-113">Zaposleni kreira i čuva izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="ba186-114">Zaposleni prosleđuje izveštaj o troškovima na odobrenje.</span><span class="sxs-lookup"><span data-stu-id="ba186-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="ba186-115">Davalac odobrenja se identifikuje na osnovu pravila koja su definisana prilikom podešavanja toka posla.</span><span class="sxs-lookup"><span data-stu-id="ba186-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="ba186-116">Davalac odobrenja dobija obaveštenje da je izveštaj o troškovima spreman za odobrenje.</span><span class="sxs-lookup"><span data-stu-id="ba186-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="ba186-117">Davalac odobrenja pregleda izveštaj o troškovima i potvrđuje da su ispunjeni sledeći uslovi:</span><span class="sxs-lookup"><span data-stu-id="ba186-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="ba186-118">Troškovi ne krše nijednu smernicu troškova.</span><span class="sxs-lookup"><span data-stu-id="ba186-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="ba186-119">Ako trošak krši smernice, davalac odobrenja potvrđuje da izveštaj o troškovima sadrži valjano poslovno opravdanje.</span><span class="sxs-lookup"><span data-stu-id="ba186-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="ba186-120">Elektronski računi su priloženi izveštaju o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="ba186-121">Davalac odobrenja odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="ba186-122">Izveštaj o troškovima dodeljuje se koordinatoru za dugovanja na knjiženje.</span><span class="sxs-lookup"><span data-stu-id="ba186-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="ba186-123">Dolazi do jednog od sledećih koraka, u zavisnosti od toga da li je konfigurisano automatsko knjiženje:</span><span class="sxs-lookup"><span data-stu-id="ba186-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="ba186-124">Ako je konfigurisano automatsko knjiženje, izveštaj o troškovima se obrađuje za plaćanje i ažurira se status izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="ba186-125">Ako automatsko knjiženje nije konfigurisano, koordinator dugovanja verifikuje da su predati svi originalni računi i da su računi usklađeni sa troškovima u izveštaju o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ba186-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="ba186-126">Sve šifre poreza koje su unete u izveštaj o troškovima takođe moraju biti verifikovane kao tačne.</span><span class="sxs-lookup"><span data-stu-id="ba186-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="ba186-127">Nakon što se ovi zahtevi provere, izveštaj o troškovima se knjiži.</span><span class="sxs-lookup"><span data-stu-id="ba186-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="ba186-128">Nakon što se proknjiži izveštaj o troškovima, odobrava se plaćanje za izveštaj o troškovima, a zaposlenom se nadoknađuje.</span><span class="sxs-lookup"><span data-stu-id="ba186-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
