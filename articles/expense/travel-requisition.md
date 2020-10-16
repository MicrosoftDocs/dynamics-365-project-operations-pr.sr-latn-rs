---
title: Zahtevi za putovanje
description: Ova tema pruža informacije o zahtevima za putovanje.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906312"
---
# <a name="travel-requisitions"></a><span data-ttu-id="96e28-103">Zahtevi za putovanje</span><span class="sxs-lookup"><span data-stu-id="96e28-103">Travel requisitions</span></span>

<span data-ttu-id="96e28-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="96e28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="96e28-105">Zahtev za putovanje navodi troškove koji će nastati u svrhu putovanja.</span><span class="sxs-lookup"><span data-stu-id="96e28-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="96e28-106">Zahtev za putovanje se podnosi na uvid i može se koristiti za odobravanje troškova.</span><span class="sxs-lookup"><span data-stu-id="96e28-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="96e28-107">Možda ćete morati da predate zahtev za putovanje pre nego što nastane bilo kakav trošak koji se naplaćuje organizaciji.</span><span class="sxs-lookup"><span data-stu-id="96e28-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="96e28-108">Ovaj uslov se primenjuje, bez obzira na to da li naplaćujete troškove na kreditnoj kartici preduzeća, trošite gotovinu koju ste dobili kao akontaciju ili ćete plaćati troškove iz svog džepa koje će vam organizacija nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="96e28-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="96e28-109">Zahtevi za putovanje i smernice mogu se koristiti za lakše upravljanje troškovima organizacije.</span><span class="sxs-lookup"><span data-stu-id="96e28-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="96e28-110">Na primer, ako vaša organizacija radi na projektu sa fiksnom cenom koji zahteva putovanje, putni troškovi članova projektnog tima moraju se uklapati u budžet projekta.</span><span class="sxs-lookup"><span data-stu-id="96e28-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="96e28-111">Zahtevanjem da se putni troškovi odobre pre nego što nastanu, organizacija može da pomogne da projekat ostane u okviru budžeta.</span><span class="sxs-lookup"><span data-stu-id="96e28-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="96e28-112">Konfigurisanje</span><span class="sxs-lookup"><span data-stu-id="96e28-112">Configuration</span></span> 

<span data-ttu-id="96e28-113">Zahtevi za putovanje mogu se konfigurisati kao „obavezni“ omogućavanjem parametra „Prethodno odobrenje putovanja je obavezno“ u parametrima upravljanja troškovima.</span><span class="sxs-lookup"><span data-stu-id="96e28-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="96e28-114">Kreiranje i prosleđivanje zahteva za putovanje</span><span class="sxs-lookup"><span data-stu-id="96e28-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="96e28-115">Idite na **Moji troškovi: Zahtev za putovanje** i izaberite **Novi zahtev za putovanje**.</span><span class="sxs-lookup"><span data-stu-id="96e28-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="96e28-116">Unesite svrhu i odredište za zahtev.</span><span class="sxs-lookup"><span data-stu-id="96e28-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="96e28-117">U polje **Opis putovanja** unesite sve dodatne informacije.</span><span class="sxs-lookup"><span data-stu-id="96e28-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="96e28-118">Za svaki od očekivanih troškova, poput leta, obroka ili iznajmljivanja automobila, napravite stavku troška.</span><span class="sxs-lookup"><span data-stu-id="96e28-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="96e28-119">Uključite procenjeni datum, procenjeni iznos i valutu za svaki trošak.</span><span class="sxs-lookup"><span data-stu-id="96e28-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="96e28-120">Kada završite sa dodavanjem očekivanih troškova, izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="96e28-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="96e28-121">Kada budete spremni da predate zahtev za putovanje, izaberite **Tok posla** > **Prosledi**.</span><span class="sxs-lookup"><span data-stu-id="96e28-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="96e28-122">Odobrene zahteve za putovanje možete pregledati u odeljku **Moji troškovi: Zahtev za putovanje**.</span><span class="sxs-lookup"><span data-stu-id="96e28-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="96e28-123">Prikaz dostupnih zahteva za putovanje</span><span class="sxs-lookup"><span data-stu-id="96e28-123">View available travel requisitions</span></span>

<span data-ttu-id="96e28-124">Sve svoje zahteve za putovanje možete pregledati u odeljku **Moji troškovi: Zahtevi za putovanje**.</span><span class="sxs-lookup"><span data-stu-id="96e28-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="96e28-125">Odobravanje zahteva za putovanje</span><span class="sxs-lookup"><span data-stu-id="96e28-125">Approve travel requisitions</span></span>

<span data-ttu-id="96e28-126">Izaberite zahtev za putovanje koji želite da odobrite, a zatim izaberite **Tok posla** > **Odobri**.</span><span class="sxs-lookup"><span data-stu-id="96e28-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="96e28-127">Pošaljite izveštaj o troškovima koristeći odobreni zahtev za putovanje</span><span class="sxs-lookup"><span data-stu-id="96e28-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="96e28-128">Napravite novi izveštaj o troškovima i u zaglavlju izveštaja o troškovima i sa liste odobrenih putnih zahteva izaberite **Mapiraj na zahtev za putovanje**.</span><span class="sxs-lookup"><span data-stu-id="96e28-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="96e28-129">Polje **Iznos zahteva za putovanje** se automatski ažurira u zaglavlju izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="96e28-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="96e28-130">Dodajte svaki trošak nastao tokom putovanja.</span><span class="sxs-lookup"><span data-stu-id="96e28-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="96e28-131">Ako je polje **Unapred ovlašćeno** omogućeno, usklađeni iznos i odobreni iznos za određenu kategoriju troškova će se ažurirati.</span><span class="sxs-lookup"><span data-stu-id="96e28-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="96e28-132">Kada mapirate izveštaj o troškovima u odobreni zahtev za putovanje, iznos transakcije ne može biti veći od odobrenog iznosa.</span><span class="sxs-lookup"><span data-stu-id="96e28-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
