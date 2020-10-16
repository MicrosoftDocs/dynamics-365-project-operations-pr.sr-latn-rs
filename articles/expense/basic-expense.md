---
title: Stavka troška (lagana verzija)
description: Ova tema pruža informacije o tome kako raditi sa stavkom troška u jednostavnoj primeni.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965878"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="26c4f-103">Stavka troška (lagana verzija)</span><span class="sxs-lookup"><span data-stu-id="26c4f-103">Expense entry (lite)</span></span>

<span data-ttu-id="26c4f-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="26c4f-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26c4f-105">Osnovno (ili lagano) upravljanje troškovima je sposobnost evidentiranja jednostavnih troškova.</span><span class="sxs-lookup"><span data-stu-id="26c4f-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="26c4f-106">Možete evidentirati troškove na projektu, a zatim će ih davalac odobrenja pregledati i odobriti.</span><span class="sxs-lookup"><span data-stu-id="26c4f-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="26c4f-107">Za više informacija o mogućnostima troškova u usluzi Dynamics 365 Project Operations, pogledajte [Pregled troškova](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26c4f-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="26c4f-108">Obuhvatanje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="26c4f-108">Capture a basic expense</span></span>

<span data-ttu-id="26c4f-109">Možete pokriti svoje troškove kako biste ih mogli dostaviti davaocu odobrenja.</span><span class="sxs-lookup"><span data-stu-id="26c4f-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="26c4f-110">Idite na **Troškovi** i izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="26c4f-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="26c4f-111">Na stranici **Novi trošak**, unesite potrebne informacije o troškovima, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="26c4f-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="26c4f-112">Prosleđivanje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="26c4f-112">Submit a basic expense</span></span>

<span data-ttu-id="26c4f-113">Kada završite sa evidentiranjem svih troškova i budete li spremni da ih odobrite, morate ih prijaviti.</span><span class="sxs-lookup"><span data-stu-id="26c4f-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="26c4f-114">Idite na **Troškovi** i izaberite trošak.</span><span class="sxs-lookup"><span data-stu-id="26c4f-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="26c4f-115">Ili izaberite sve troškove pomoću polja za potvrdu u zaglavlju.</span><span class="sxs-lookup"><span data-stu-id="26c4f-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="26c4f-116">Izaberite **Prosledi**.</span><span class="sxs-lookup"><span data-stu-id="26c4f-116">Select **Submit**.</span></span> <span data-ttu-id="26c4f-117">Sistem obrađuje odabrane stavke, a zatim kreira zahteve za odobrenje troškova.</span><span class="sxs-lookup"><span data-stu-id="26c4f-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="26c4f-118">Opoziv osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="26c4f-118">Recall a basic expense</span></span>

<span data-ttu-id="26c4f-119">Kada greškom prosledite trošak, možete ga opozvati.</span><span class="sxs-lookup"><span data-stu-id="26c4f-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="26c4f-120">Vreme potrebno za opoziv stavke troška zavisi od faze odobrenja.</span><span class="sxs-lookup"><span data-stu-id="26c4f-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="26c4f-121">Ako davalac odobrenja još nije odobrio stavku, opoziv se može izvršiti odmah.</span><span class="sxs-lookup"><span data-stu-id="26c4f-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="26c4f-122">Međutim, ako je stavka već odobrena, od davaoca odobrenja se traži da odobri opoziv i poništi transakcije.</span><span class="sxs-lookup"><span data-stu-id="26c4f-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="26c4f-123">Idite na **Troškovi**, a zatim na listi troškova odaberite trošak koji ćete opozvati.</span><span class="sxs-lookup"><span data-stu-id="26c4f-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="26c4f-124">Izaberite **Opozovi**.</span><span class="sxs-lookup"><span data-stu-id="26c4f-124">Select **Recall**.</span></span> <span data-ttu-id="26c4f-125">Ako stavka troška još nije odobrena, sistem je odmah opoziva.</span><span class="sxs-lookup"><span data-stu-id="26c4f-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="26c4f-126">Ako je stavka troška već odobrena, kreira se zahtev za opoziv da obavesti davaoca odobrenja da želite da stornirate trošak.</span><span class="sxs-lookup"><span data-stu-id="26c4f-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="26c4f-127">Davalac odobrenja će zatim potvrditi da se storniranje može izvršiti i stavka će biti vraćena.</span><span class="sxs-lookup"><span data-stu-id="26c4f-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="26c4f-128">Brisanje osnovnog troška</span><span class="sxs-lookup"><span data-stu-id="26c4f-128">Delete a basic expense</span></span>

<span data-ttu-id="26c4f-129">Troškovi koji još nisu prosleđeni mogu se izbrisati.</span><span class="sxs-lookup"><span data-stu-id="26c4f-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="26c4f-130">Da biste izbrisali trošak koji je već prosleđen, prvo ga morate opozvati.</span><span class="sxs-lookup"><span data-stu-id="26c4f-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="26c4f-131">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="26c4f-131">See also</span></span>

- [<span data-ttu-id="26c4f-132">Pregled odobrenja</span><span class="sxs-lookup"><span data-stu-id="26c4f-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
