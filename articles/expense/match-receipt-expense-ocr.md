---
title: Snimite priznanicu pomoću usluge OCR
description: Ova tema pruža informacije o obradi priznanica pomoću optičkog prepoznavanja znakova (OCR).
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
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499868"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="ec180-103">Snimite priznanicu pomoću usluge OCR</span><span class="sxs-lookup"><span data-stu-id="ec180-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="ec180-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ec180-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec180-105">Unos troškova je poboljšan uvođenjem obradu priznanica putem optičkog prepoznavanja znakova (OCR).</span><span class="sxs-lookup"><span data-stu-id="ec180-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="ec180-106">Ova funkcionalnost je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ec180-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="ec180-107">Ključne funkcije</span><span class="sxs-lookup"><span data-stu-id="ec180-107">Key features</span></span>

- <span data-ttu-id="ec180-108">Sistem izdvaja ime trgovca, datum i ukupan iznos sa priznanice.</span><span class="sxs-lookup"><span data-stu-id="ec180-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="ec180-109">Sistem će pokušati da uskladi nevezane priznanice sa nevezanim transakcijama troškova.</span><span class="sxs-lookup"><span data-stu-id="ec180-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="ec180-110">Iz priznanica možete da kreirate ručno unete transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="ec180-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="ec180-111">Priložite priznanice uz izveštaj o troškovima</span><span class="sxs-lookup"><span data-stu-id="ec180-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="ec180-112">Da biste automatski priložili priznanice koje uključuju transakcije kreditnom karticom kada se kreira izveštaj o troškovima, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="ec180-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="ec180-113">Otvorite radni prostor **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ec180-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="ec180-114">Na kartici **Priznanice** proverite da li postoje nepriložene priznanice.</span><span class="sxs-lookup"><span data-stu-id="ec180-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="ec180-115">Takođe možete da otpremite priznanice na karticu **Priznanice**.</span><span class="sxs-lookup"><span data-stu-id="ec180-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="ec180-116">Na kartici **Troškovi** proverite da li postoje nepriloženi troškovi.</span><span class="sxs-lookup"><span data-stu-id="ec180-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="ec180-117">Obično ih administrator troškova uvozi od dobavljača kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="ec180-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="ec180-118">Izaberite **Novi izveštaj o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ec180-118">Select **New expense report**.</span></span> <span data-ttu-id="ec180-119">Obratite pažnju da i sada možete da uključite troškove i priznanice kada kreirate izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ec180-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="ec180-120">Ako dodate i troškove i račune, aktiviraće se automatsko upoređivanje priznanice i troškova.</span><span class="sxs-lookup"><span data-stu-id="ec180-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="ec180-121">Kreirajte ili uporedite priznanice sa izveštajem o troškovima</span><span class="sxs-lookup"><span data-stu-id="ec180-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="ec180-122">Da biste stvorili trošak ili uporedili trošak sa priznanice, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="ec180-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="ec180-123">Na izveštaju o troškovima, na kartici **Priznanice**, priložite priznanicu izborom stavke **Dodaj priznanice**.</span><span class="sxs-lookup"><span data-stu-id="ec180-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="ec180-124">Ispod otpremljene slike priznanice videćete opcije **Kreiraj** i **Uporedi**.</span><span class="sxs-lookup"><span data-stu-id="ec180-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="ec180-125">Izaberite **Kreiraj** da biste kreirali ručno unete transakcije troškova i popunili vrednosti koje su izdvojene iz priznanice.</span><span class="sxs-lookup"><span data-stu-id="ec180-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="ec180-126">Ako izaberete **Uporedi**, sistem pokušava da postojeći trošak uskladi sa priznanicom.</span><span class="sxs-lookup"><span data-stu-id="ec180-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="ec180-127">Instalacija</span><span class="sxs-lookup"><span data-stu-id="ec180-127">Installation</span></span>

<span data-ttu-id="ec180-128">Da biste koristili ove napredne mogućnosti troškova, instalirajte programski dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite funkcije u vašoj instanci.</span><span class="sxs-lookup"><span data-stu-id="ec180-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="ec180-129">Programskom dodatku možete pristupiti iz svog projekta u usluzi Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ec180-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="ec180-130">Prijavite se na LCS i otvorite željeno okruženje.</span><span class="sxs-lookup"><span data-stu-id="ec180-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="ec180-131">Idi na stavku **Svi detalji**.</span><span class="sxs-lookup"><span data-stu-id="ec180-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="ec180-132">Izaberite **Održavanje** ili se pomerite nadole do brze kartice **Programski dodaci za životnu sredinu**.</span><span class="sxs-lookup"><span data-stu-id="ec180-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="ec180-133">Izaberite stavku **Instalirajte novi programski dodatak**.</span><span class="sxs-lookup"><span data-stu-id="ec180-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="ec180-134">Izaberite stavku **Usluga upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ec180-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="ec180-135">Sledite uputstva za instalaciju i prihvatite odredbe i uslove.</span><span class="sxs-lookup"><span data-stu-id="ec180-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="ec180-136">Izaberite **Instaliraj**.</span><span class="sxs-lookup"><span data-stu-id="ec180-136">Select **Install**.</span></span>

<span data-ttu-id="ec180-137">U radnom prostoru **Upravljanje funkcijama** uključite sledeće funkcije:</span><span class="sxs-lookup"><span data-stu-id="ec180-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="ec180-138">Ponovno osmišljeni izveštaji o troškovima</span><span class="sxs-lookup"><span data-stu-id="ec180-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="ec180-139">Automatsko podudaranje i kreiranje troškova iz priznanice</span><span class="sxs-lookup"><span data-stu-id="ec180-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="ec180-140">Kada uključite ove funkcije, dešavaju se sledeće radnje:</span><span class="sxs-lookup"><span data-stu-id="ec180-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="ec180-141">Postojeći radni prostor **Upravljanje troškovima** se zamenjuje novim radnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="ec180-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="ec180-142">Dodata je nova stavka menija za vidljivost polja troškova.</span><span class="sxs-lookup"><span data-stu-id="ec180-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="ec180-143">Još uvek možete otvoriti prethodnu stranicu **Izveštaji o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izveštaji o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="ec180-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="ec180-144">Tokovi posla i sva odobrenja vas i dalje vode na postojeću stranicu sa izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="ec180-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="ec180-145">Priznanice će se obrađivati putem Microsoft Azure Cognitive Services, a metapodaci će biti izdvojeni i dodati.</span><span class="sxs-lookup"><span data-stu-id="ec180-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="ec180-146">Dodata je opcija koja vam omogućava da napravite izveštaj o troškovima koji uključuje odgovarajuće nepriložene priznanice.</span><span class="sxs-lookup"><span data-stu-id="ec180-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="ec180-147">Opcija koja se dodaje izveštajima o troškovima omogućava vam da kreirate liniju troškova iz priznanica ili pokušate da uporedite postojeću priznanicu sa postojećom linijom troškova.</span><span class="sxs-lookup"><span data-stu-id="ec180-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ec180-148">Najčešća pitanja</span><span class="sxs-lookup"><span data-stu-id="ec180-148">Frequently asked questions</span></span>

<span data-ttu-id="ec180-149">**Da li Microsoft koristi moje podatke za svoje modele?**</span><span class="sxs-lookup"><span data-stu-id="ec180-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="ec180-150">Ne, Microsoft je izgradio opšti model mašinskog učenja za uslugu obrade priznanica.</span><span class="sxs-lookup"><span data-stu-id="ec180-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="ec180-151">Ovaj model se ne zasniva na priznanicama koje otpremite.</span><span class="sxs-lookup"><span data-stu-id="ec180-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="ec180-152">**Gde je ova funkcija dostupna i obrađena?**</span><span class="sxs-lookup"><span data-stu-id="ec180-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="ec180-153">Trenutno su podržane Sjedinjene Države.</span><span class="sxs-lookup"><span data-stu-id="ec180-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="ec180-154">**Gde odlaze moje priznanice?**</span><span class="sxs-lookup"><span data-stu-id="ec180-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="ec180-155">Finansije će kontaktirati Cognitive Services da bi izvukli podatke sa terena.</span><span class="sxs-lookup"><span data-stu-id="ec180-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="ec180-156">Cognitive Services će zadržati kopiju vaše priznanice i do 24 sata dok traje obrada.</span><span class="sxs-lookup"><span data-stu-id="ec180-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="ec180-157">Po završetku obrade, Cognitive Services će ukloniti priznanicu.</span><span class="sxs-lookup"><span data-stu-id="ec180-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="ec180-158">Priznanice se i dalje čuvaju u Finansijama.</span><span class="sxs-lookup"><span data-stu-id="ec180-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="ec180-159">Za više informacija pogledajte [Omogućite razumevanje priznanice sa novom sposobnošću prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="ec180-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
