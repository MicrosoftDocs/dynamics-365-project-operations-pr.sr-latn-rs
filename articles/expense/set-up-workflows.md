---
title: Podesite tokove posla za upravljanje troškovima
description: Možete da podesite proces toka posla koji se koristi za pregled i odobravanje putnih i troškovnih dokumenata.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276050"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="ebdc9-103">Podesite tokove posla za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="ebdc9-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="ebdc9-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ebdc9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ebdc9-105">Možete da podesite proces toka posla za pregled i odobravanje putnih i troškovnih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="ebdc9-106">Možete da definišete tokove posla za izveštaje o troškovima, putne zahteve i zahteve za gotovinskim avansom.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="ebdc9-107">Tok posla predstavlja poslovni proces i definiše kako dokument prolazi kroz sistem.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="ebdc9-108">Tok posla takođe pokazuje ko mora da izvrši zadatak ili odobri dokument.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ebdc9-109">Postoji nekoliko prednosti korišćenja sistema toka posla u vašoj organizaciji:</span><span class="sxs-lookup"><span data-stu-id="ebdc9-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="ebdc9-110">**Dosledni procesi** : Možete da definišete postupak odobravanja za određene dokumente, kao što su zahtevi za kupovinu i izveštaji o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ebdc9-111">Korišćenje sistema toka posla pomaže u obezbeđivanju obrade i odobravanja dokumenata na dosledan i efikasan način.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="ebdc9-112">**Vidljivost procesa** : Možete pratiti status, istoriju i pokazatelje učinka određene instance toka posla.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ebdc9-113">Ovo vam pomaže da utvrdite da li treba izvršiti promene u toku posla kako biste poboljšali efikasnost.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="ebdc9-114">**Centralizovana radna lista** : Korisnici mogu da vide centralizovanu listu poslova da bi videli zadatke toka posla i odobrenja koja su im dodeljena.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="ebdc9-115">Tipovi toka posla</span><span class="sxs-lookup"><span data-stu-id="ebdc9-115">Workflow types</span></span>

<span data-ttu-id="ebdc9-116">Sledeća tabela navodi tipove tokova posla u kojima možete da kreirate **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="ebdc9-117"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="ebdc9-118"><strong>Koristite ovaj tip za</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="ebdc9-119"><strong>Automatsko odobravanje izveštaja o troškovima</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="ebdc9-120">Kreirajte tokove odobrenja za izveštaje o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="ebdc9-121"><strong>Automatsko objavljivanje izveštaja o troškovima</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="ebdc9-122">Kreirajte tokove automatskog objavljivanja za izveštaje o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="ebdc9-123"><strong>Stavka troška</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="ebdc9-124">Kreirajte tokove odobrenja za stavke u izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="ebdc9-125"><strong>Automatsko objavljivanje stavke troška</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="ebdc9-126">Kreirajte tokove automatskog objavljivanja za stavke u izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="ebdc9-127"><strong>Zahtev za putovanjem</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="ebdc9-128">Kreirajte tokove posla odobrenja za putne zahteve.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="ebdc9-129"><strong>Zahtev za gotovinski avans</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="ebdc9-130">Kreirajte tokove odobrenja za zahteve za gotovinskim avansom.</span><span class="sxs-lookup"><span data-stu-id="ebdc9-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="ebdc9-131"><strong>Povraćaj PDV-a</strong></span><span class="sxs-lookup"><span data-stu-id="ebdc9-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="ebdc9-132">Kreirajte tokove odobrenja za povraćaj poreza na dodatu vrednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="ebdc9-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]