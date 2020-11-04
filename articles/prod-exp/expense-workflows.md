---
title: Podešavanje tokova posla za upravljanje troškovima
description: Možete da podesite proces toka posla za pregled i odobravanje putnih i troškovnih dokumenata.
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083734"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="b4dc8-103">Podešavanje tokova posla za upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="b4dc8-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4dc8-104">Možete da podesite proces toka posla koji se koristi za pregled i odobravanje putnih i troškovnih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="b4dc8-105">Dokumenti za koje možete da definišete tokove posla obuhvataju izveštaje o troškovima, putne zahteve i zahteve za gotovinskim avansom.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="b4dc8-106">Tok posla predstavlja poslovni proces.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-106">A workflow represents a business process.</span></span> <span data-ttu-id="b4dc8-107">Definiše kako dokument prolazi kroz sistem i ukazuje na to ko mora da dovrši zadatak ili odobri dokument.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b4dc8-108">Postoji nekoliko prednosti korišćenja sistema toka posla u vašoj organizaciji:</span><span class="sxs-lookup"><span data-stu-id="b4dc8-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="b4dc8-109">**Dosledni procesi** – Možete da definišete postupak odobravanja za određene dokumente, kao što su zahtevi za kupovinu i izveštaji o troškovima.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b4dc8-110">Korišćenje sistema toka posla pomaže u obezbeđivanju obrade i odobravanja dokumenata na dosledan i efikasan način.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="b4dc8-111">Vidljivost procesa – Možete pratiti status, istoriju i pokazatelje učinka određene instance toka posla.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b4dc8-112">Ovo vam pomaže da utvrdite da li treba izvršiti promene u toku posla kako biste poboljšali efikasnost.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="b4dc8-113">Centralizovana radna lista – Korisnici mogu da vide centralizovanu listu poslova da bi videli zadatke toka posla i odobrenja koja su im dodeljena.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="b4dc8-114">**Tipovi tokova posla koje možete kreirati**</span><span class="sxs-lookup"><span data-stu-id="b4dc8-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="b4dc8-115">Sledeća tabela navodi tipove tokova posla u kojima možete da kreirate u odeljku **Trošak**.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="b4dc8-116"><strong>Tip</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="b4dc8-117"><strong>Koristite ovaj tip za</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="b4dc8-118"><strong>Izveštaj o troškovima</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="b4dc8-119">Kreirajte tokove odobrenja za izveštaje o troškovima.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="b4dc8-120"><strong>Automatsko objavljivanje izveštaja o troškovima</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="b4dc8-121">Kreirajte tokove automatskog objavljivanja za izveštaje o troškovima.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="b4dc8-122"><strong>Stavka troška</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="b4dc8-123">Kreirajte tokove odobrenja za stavke u izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="b4dc8-124"><strong>Automatsko objavljivanje stavke troška</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="b4dc8-125">Kreirajte tokove automatskog objavljivanja za stavke u izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="b4dc8-126"><strong>Zahtev za putovanjem</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="b4dc8-127">Kreirajte tokove posla odobrenja za putne zahteve.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="b4dc8-128"><strong>Zahtev za gotovinski avans</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="b4dc8-129">Kreirajte tokove odobrenja za zahteve za gotovinskim avansom.</span><span class="sxs-lookup"><span data-stu-id="b4dc8-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="b4dc8-130"><strong>Povraćaj PDV-a</strong></span><span class="sxs-lookup"><span data-stu-id="b4dc8-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="b4dc8-131">Kreirajte tokove odobrenja za povraćaj poreza na dodatu vrednost (PDV).</span><span class="sxs-lookup"><span data-stu-id="b4dc8-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

