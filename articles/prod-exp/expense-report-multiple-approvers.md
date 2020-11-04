---
title: Više davalaca odobrenja na izveštaju o troškovima
description: Ova tema pruža informacije o izveštajima o troškovima za koje je potrebno odobrenje više osoba.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083736"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="c67fb-103">Više davalaca odobrenja na izveštaju o troškovima</span><span class="sxs-lookup"><span data-stu-id="c67fb-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c67fb-104">U zavisnosti od smernica odobravanja troškova u vašoj organizaciji, izveštaj o troškovima koji je podneo neki zaposleni možda će morati da odobri više osoba.</span><span class="sxs-lookup"><span data-stu-id="c67fb-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="c67fb-105">Kada uspostavljate proces toka posla za odobravanje izveštaja o troškovima, možete da dodate elemente toka posla koji uključuju zadatke ili korake za jednog davaoca odobrenja za izveštaj o troškovima ili više njih.</span><span class="sxs-lookup"><span data-stu-id="c67fb-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="c67fb-106">Na primer, možda ćete zahtevati da sve izveštaje o troškovima prvo odobri menadžer zaposlenog koji je podneo izveštaj, a zatim koordinator za dugovanja.</span><span class="sxs-lookup"><span data-stu-id="c67fb-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="c67fb-107">Ako odlučite da zahtevate više davalaca odobrenja za izveštaj o troškovima, možete da dodate elemente toka posla na bilo koji od sledećih načina:</span><span class="sxs-lookup"><span data-stu-id="c67fb-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="c67fb-108">Dodajte jedan element odobrenja koji ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="c67fb-108">Add one approval element that has one step.</span></span> <span data-ttu-id="c67fb-109">Na primer, korak može zahtevati da se izveštaj o troškovima dodeli grupi korisnika i da ga odobri 50% članova grupe korisnika.</span><span class="sxs-lookup"><span data-stu-id="c67fb-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="c67fb-110">Dodajte jedan element odobrenja koji ima više koraka.</span><span class="sxs-lookup"><span data-stu-id="c67fb-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="c67fb-111">Na primer, element odobrenja može imati sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="c67fb-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="c67fb-112">Direktor zaposlenog koji je podneo izveštaj o troškovima ga odobrava.</span><span class="sxs-lookup"><span data-stu-id="c67fb-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="c67fb-113">Službenik za dugovanja verifikuje priznanice i stavke izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="c67fb-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="c67fb-114">Vlasnik budžeta odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="c67fb-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="c67fb-115">Dodajte više elemenata odobrenja, od kojih svaki ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="c67fb-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="c67fb-116">Na primer, možete dodati zasebni element odobrenja za svaki od sledećih koraka:</span><span class="sxs-lookup"><span data-stu-id="c67fb-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="c67fb-117">Menadžer zaposlenog odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="c67fb-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="c67fb-118">Vlasnik budžeta odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="c67fb-118">The budget owner approves the expense report.</span></span>
