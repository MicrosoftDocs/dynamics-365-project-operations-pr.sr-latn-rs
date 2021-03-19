---
title: Obrada priznanica za troškove
description: Ova tema pruža informacije o obradi priznanica pomoću optičkog prepoznavanja znakova (OCR). Ova funkcija je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima u usluzi Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271820"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8a244-104">Obrada priznanica za troškove</span><span class="sxs-lookup"><span data-stu-id="8a244-104">Expense receipt processing</span></span>

<span data-ttu-id="8a244-105">Unos troškova je poboljšan uvođenjem obradu priznanica putem optičkog prepoznavanja znakova (OCR).</span><span class="sxs-lookup"><span data-stu-id="8a244-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8a244-106">Ova funkcija je dizajnirana da poboljša korisničko iskustvo prilikom kreiranja izveštaja o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8a244-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8a244-107">Ključne funkcije</span><span class="sxs-lookup"><span data-stu-id="8a244-107">Key features</span></span>

- <span data-ttu-id="8a244-108">Sa priznanice se izdvajaju ime trgovca, datum i ukupan iznos.</span><span class="sxs-lookup"><span data-stu-id="8a244-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8a244-109">Funkcija pokušava da uskladi nevezane priznanice sa nevezanim transakcijama troškova.</span><span class="sxs-lookup"><span data-stu-id="8a244-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8a244-110">Korisnici iz priznanica mogu da kreiraju ručno unete transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="8a244-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8a244-111">Primeri upotrebe</span><span class="sxs-lookup"><span data-stu-id="8a244-111">Usage examples</span></span>

<span data-ttu-id="8a244-112">Da biste automatski priložili priznanice koje uključuju transakcije kreditnom karticom kada se kreira izveštaj o troškovima, izvršite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="8a244-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8a244-113">Otvorite radni prostor **Upravljanje troškovima**.</span><span class="sxs-lookup"><span data-stu-id="8a244-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8a244-114">Na kartici **Priznanice** proverite da li postoje nepriložene priznanice.</span><span class="sxs-lookup"><span data-stu-id="8a244-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8a244-115">Takođe možete da otpremite priznanice na karticu **Priznanice**.</span><span class="sxs-lookup"><span data-stu-id="8a244-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8a244-116">Na kartici **Troškovi** proverite da li postoje nepriloženi troškovi.</span><span class="sxs-lookup"><span data-stu-id="8a244-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8a244-117">Obično ih administrator troškova uvozi od dobavljača kreditne kartice.</span><span class="sxs-lookup"><span data-stu-id="8a244-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8a244-118">Izaberite **Novi izveštaj o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="8a244-118">Select **New expense report**.</span></span> <span data-ttu-id="8a244-119">Obratite pažnju da i sada možete da uključite troškove i priznanice kada kreirate izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8a244-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8a244-120">Ako dodate i troškove i račune, aktiviraće se automatsko upoređivanje priznanice i troškova.</span><span class="sxs-lookup"><span data-stu-id="8a244-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8a244-121">Da biste stvorili trošak ili uporedili trošak sa priznanice, izvršite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="8a244-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8a244-122">Na izveštaju o troškovima, na kartici **Priznanice**, priložite priznanicu izborom stavke **Dodaj priznanice**.</span><span class="sxs-lookup"><span data-stu-id="8a244-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8a244-123">Ispod otpremljene slike priznanice videćete opcije **Kreiraj** i **Uporedi**.</span><span class="sxs-lookup"><span data-stu-id="8a244-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8a244-124">Izaberite **Kreiraj** da biste kreirali ručno unete transakcije troškova i popunili vrednosti koje su izdvojene iz priznanice.</span><span class="sxs-lookup"><span data-stu-id="8a244-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8a244-125">Ako izaberete **Uporedi**, sistem pokušava da postojeći trošak uskladi sa priznanicom.</span><span class="sxs-lookup"><span data-stu-id="8a244-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8a244-126">Instalacija</span><span class="sxs-lookup"><span data-stu-id="8a244-126">Installation</span></span>

<span data-ttu-id="8a244-127">Ova funkcija radi u kombinaciji sa funkcijom **Redizajnirani izveštaji o troškovima** koja vam pomaže da pojednostavite iskustvo sa troškovima.</span><span class="sxs-lookup"><span data-stu-id="8a244-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8a244-128">Ova funkcija je dostupna samo za okruženja 2. nivoa i viših, a to su Sandbox i Proizvodnja.</span><span class="sxs-lookup"><span data-stu-id="8a244-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8a244-129">Da biste koristili ove napredne mogućnosti troškova, instalirajte programski dodatak Usluga upravljanja troškovima za Microsoft Dynamics 365 Finance i uključite funkcije u vašoj instanci.</span><span class="sxs-lookup"><span data-stu-id="8a244-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8a244-130">Programskom dodatku možete pristupiti iz svog projekta u usluzi Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8a244-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8a244-131">Prijavite se na LCS i otvorite željeno okruženje.</span><span class="sxs-lookup"><span data-stu-id="8a244-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8a244-132">Idi na stavku **Svi detalji**.</span><span class="sxs-lookup"><span data-stu-id="8a244-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8a244-133">Izaberite **Održavanje** ili se pomerite nadole do brze kartice **Programski dodaci za životnu sredinu**.</span><span class="sxs-lookup"><span data-stu-id="8a244-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8a244-134">Izaberite stavku **Instalirajte novi programski dodatak**.</span><span class="sxs-lookup"><span data-stu-id="8a244-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8a244-135">Izaberite stavku **Usluga upravljanja troškovima**.</span><span class="sxs-lookup"><span data-stu-id="8a244-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8a244-136">Sledite uputstva za instalaciju i prihvatite odredbe i uslove.</span><span class="sxs-lookup"><span data-stu-id="8a244-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8a244-137">Izaberite **Instaliraj**.</span><span class="sxs-lookup"><span data-stu-id="8a244-137">Select **Install**.</span></span>

<span data-ttu-id="8a244-138">U radnom prostoru **Upravljanje funkcijama** uključite sledeće funkcije:</span><span class="sxs-lookup"><span data-stu-id="8a244-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8a244-139">Ponovno osmišljeni izveštaji o troškovima</span><span class="sxs-lookup"><span data-stu-id="8a244-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8a244-140">Automatsko podudaranje i kreiranje troškova iz priznanice</span><span class="sxs-lookup"><span data-stu-id="8a244-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8a244-141">Kada uključite ove funkcije, dešavaju se sledeće radnje:</span><span class="sxs-lookup"><span data-stu-id="8a244-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8a244-142">Postojeći radni prostor **Upravljanje troškovima** se zamenjuje novim radnim prostorom.</span><span class="sxs-lookup"><span data-stu-id="8a244-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8a244-143">Dodata je nova stavka menija za vidljivost polja troškova.</span><span class="sxs-lookup"><span data-stu-id="8a244-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8a244-144">Još uvek možete otvoriti prethodnu stranicu **Izveštaji o troškovima** odlaskom na **Upravljanje troškovima > Moji troškovi > Izveštaji o troškovima**.</span><span class="sxs-lookup"><span data-stu-id="8a244-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8a244-145">Tokovi posla i sva odobrenja vas i dalje vode na postojeću stranicu sa izveštajima o troškovima.</span><span class="sxs-lookup"><span data-stu-id="8a244-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8a244-146">Priznanice će se obrađivati putem Microsoft Azure Cognitive Services, a metapodaci će biti izdvojeni i dodati.</span><span class="sxs-lookup"><span data-stu-id="8a244-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8a244-147">Dodata je opcija koja vam omogućava da napravite izveštaj o troškovima koji uključuje odgovarajuće nepriložene priznanice.</span><span class="sxs-lookup"><span data-stu-id="8a244-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8a244-148">Opcija koja se dodaje izveštajima o troškovima omogućava vam da kreirate liniju troškova iz priznanica ili pokušate da uporedite postojeću priznanicu sa postojećom linijom troškova.</span><span class="sxs-lookup"><span data-stu-id="8a244-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8a244-149">Za više informacija o redizajniranoj funkciji izveštaja o troškovima pogledajte [Redizajnirani izveštaji o troškovima](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8a244-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8a244-150">Najčešća pitanja</span><span class="sxs-lookup"><span data-stu-id="8a244-150">Frequently asked questions</span></span>

<span data-ttu-id="8a244-151">**Da li Microsoft koristi moje podatke za svoje modele?**</span><span class="sxs-lookup"><span data-stu-id="8a244-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8a244-152">Ne, Microsoft je izgradio opšti model mašinskog učenja za uslugu obrade priznanica.</span><span class="sxs-lookup"><span data-stu-id="8a244-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8a244-153">Ovaj model se ne zasniva na priznanicama koje otpremite.</span><span class="sxs-lookup"><span data-stu-id="8a244-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8a244-154">**Gde je ova funkcija dostupna i obrađena?**</span><span class="sxs-lookup"><span data-stu-id="8a244-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8a244-155">Trenutno su podržane Sjedinjene Države.</span><span class="sxs-lookup"><span data-stu-id="8a244-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8a244-156">**Gde odlaze moje priznanice?**</span><span class="sxs-lookup"><span data-stu-id="8a244-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8a244-157">Finansije će kontaktirati Cognitive Services da bi izvukli podatke sa terena.</span><span class="sxs-lookup"><span data-stu-id="8a244-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8a244-158">Cognitive Services će zadržati kopiju vaše priznanice i do 24 sata dok traje obrada.</span><span class="sxs-lookup"><span data-stu-id="8a244-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8a244-159">Po završetku obrade, Cognitive Services će ukloniti priznanicu.</span><span class="sxs-lookup"><span data-stu-id="8a244-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8a244-160">Priznanice se i dalje čuvaju u Finansijama.</span><span class="sxs-lookup"><span data-stu-id="8a244-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8a244-161">Za više informacija pogledajte [Omogućite razumevanje priznanice sa novom sposobnošću prepoznavanja obrazaca](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8a244-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]