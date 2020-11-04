---
title: Izveštaji o troškovima i više odobravalaca
description: Ova tema pruža informacije o izveštajima o troškovima za koje je potrebno odobrenje više osoba.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083583"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="48627-103">Izveštaji o troškovima i više odobravalaca</span><span class="sxs-lookup"><span data-stu-id="48627-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="48627-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="48627-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48627-105">U zavisnosti od smernica odobravanja troškova u vašoj organizaciji, podneti izveštaj o troškovima će možda morati da odobri više osoba.</span><span class="sxs-lookup"><span data-stu-id="48627-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="48627-106">Kada uspostavljate proces toka posla za odobravanje izveštaja o troškovima, možete da dodate elemente toka posla koji uključuju zadatke ili korake za jednog davaoca odobrenja za izveštaj o troškovima ili više njih.</span><span class="sxs-lookup"><span data-stu-id="48627-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="48627-107">Na primer, možda ćete zahtevati da sve izveštaje o troškovima odobre dve zasebne osobe, menadžer zaposlenog koji je podneo izveštaj i koordinator za dugovanja.</span><span class="sxs-lookup"><span data-stu-id="48627-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="48627-108">Ako odlučite da zahtevate više davalaca odobrenja za izveštaj o troškovima, možete da dodate elemente toka posla na bilo koji od sledećih načina:</span><span class="sxs-lookup"><span data-stu-id="48627-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="48627-109">Dodajte jedan element odobrenja koji ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="48627-109">Add one approval element that has one step.</span></span> <span data-ttu-id="48627-110">Na primer, korak može zahtevati da se izveštaj o troškovima dodeli grupi korisnika i da ga odobri 50% članova grupe korisnika.</span><span class="sxs-lookup"><span data-stu-id="48627-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="48627-111">Dodajte jedan element odobrenja koji ima više koraka.</span><span class="sxs-lookup"><span data-stu-id="48627-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="48627-112">Na primer, element odobrenja može imati sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="48627-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="48627-113">Direktor zaposlenog koji je podneo izveštaj o troškovima ga odobrava.</span><span class="sxs-lookup"><span data-stu-id="48627-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="48627-114">Službenik za dugovanja verifikuje priznanice i stavke izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="48627-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="48627-115">Vlasnik budžeta odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="48627-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="48627-116">Dodajte više elemenata odobrenja, od kojih svaki ima jedan korak.</span><span class="sxs-lookup"><span data-stu-id="48627-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="48627-117">Na primer, možete dodati zasebni element odobrenja za svaki od sledećih koraka:</span><span class="sxs-lookup"><span data-stu-id="48627-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="48627-118">Menadžer zaposlenog odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="48627-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="48627-119">Vlasnik budžeta odobrava izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="48627-119">The budget owner approves the expense report.</span></span>
