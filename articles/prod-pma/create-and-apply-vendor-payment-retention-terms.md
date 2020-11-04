---
title: Kreirajte i primenite uslove zadržavanja plaćanja prodavca
description: Ova tema pruža informacije o tome kako podesiti i održavati uslove zadržavanja za plaćanja prodavaca.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083717"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="61ad2-103">Kreirajte i primenite uslove zadržavanja plaćanja prodavca</span><span class="sxs-lookup"><span data-stu-id="61ad2-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="61ad2-104">Postavljanje uslova zadržavanja za plaćanja prodavaca za projekat korisno je kada vaša organizacija želi da zadrži deo uplata izvršenih prodavcu.</span><span class="sxs-lookup"><span data-stu-id="61ad2-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="61ad2-105">Na primer, kada želite da zadržite plaćanje prodavcu dok isporučeni proizvodi ne ispune vaša očekivanja.</span><span class="sxs-lookup"><span data-stu-id="61ad2-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="61ad2-106">Uslovi zadržavanja za plaćanja prodavaca mogu se odrediti kada pregovarate o ugovoru prodavca.</span><span class="sxs-lookup"><span data-stu-id="61ad2-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="61ad2-107">Kreirajte uslove zadržavanja plaćanja prodavca</span><span class="sxs-lookup"><span data-stu-id="61ad2-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="61ad2-108">Možete da unesete procenat plaćanja prodavca za zadržavanje i procenat prethodno zadržanih iznosa koji će se osloboditi.</span><span class="sxs-lookup"><span data-stu-id="61ad2-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="61ad2-109">Iznosi se automatski zadržavaju na fakturama prodavaca sve dok ugovor ne dostigne određeni status završenosti.</span><span class="sxs-lookup"><span data-stu-id="61ad2-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="61ad2-110">Nakon što postavite uslove zadržavanja, možete ih primeniti na bilo koji projekat tog prodavca.</span><span class="sxs-lookup"><span data-stu-id="61ad2-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="61ad2-111">Koristite sledeće korake za postavljanje i održavanje uslova zadržavanja za plaćanja prodavca.</span><span class="sxs-lookup"><span data-stu-id="61ad2-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="61ad2-112">Idite na **Upravljanje projektima i računovodstvo** > **Zadržavanje** > **Uslovi zadržavanja za plaćanja prodavaca**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="61ad2-113">Izaberite **Novo** da biste dodali novi uslov zadržavanja za prodavce.</span><span class="sxs-lookup"><span data-stu-id="61ad2-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="61ad2-114">Vrednost **ID pravila** za novi uslov se automatski unosi.</span><span class="sxs-lookup"><span data-stu-id="61ad2-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="61ad2-115">Unesite kratak opis u polje **Opis** , a na brzoj kartici **Uslovi** izaberite **Dodaj liniju** da biste uneli vrednosti uslova za sledeće:</span><span class="sxs-lookup"><span data-stu-id="61ad2-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="61ad2-116">**Procenat isporučenih jedinica** : Unesite procenat završetka za uslov.</span><span class="sxs-lookup"><span data-stu-id="61ad2-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="61ad2-117">Iznosi se automatski zadržavaju na fakturama prodavaca sve dok faza dovršetka projekta ne bude ista kao navedeni procenat.</span><span class="sxs-lookup"><span data-stu-id="61ad2-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="61ad2-118">Na primer, ako unesete 50,00, iznosi se zadržavaju sve dok projekat ne bude završen 50 odsto.</span><span class="sxs-lookup"><span data-stu-id="61ad2-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="61ad2-119">**Procenat za zadržavanje** : Unesite procenat iznosa fakture dobavljača koji će se zadržati.</span><span class="sxs-lookup"><span data-stu-id="61ad2-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="61ad2-120">Na primer, ako unesete 10,00, tada se zadržava 10 procenata iznosa na fakturi dobavljača sve dok projekat ne dostigne procenat završetka kako je postavljeno u polje **Procenat isporučenih jedinica**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="61ad2-121">**Procenat za oslobađanje** : Izaberite **Dodaj liniju** da biste uneli procenat svih prethodno zadržanih iznosa koji će se osloboditi za izabrani nivo završetka projekta.</span><span class="sxs-lookup"><span data-stu-id="61ad2-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="61ad2-122">Ako imate više od jedne kontrolne tačke za različite nivoe završetka projekta, unesite zasebnu liniju uslova zadržavanja za prodavca za svako pravilo zadržavanja.</span><span class="sxs-lookup"><span data-stu-id="61ad2-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="61ad2-123">Svaka linija može navoditi različiti procenat zadržavanja i drugačiji procenat izdavanja za svaki naznačeni nivo završetka projekta.</span><span class="sxs-lookup"><span data-stu-id="61ad2-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="61ad2-124">Nakon što kreirate uslove zadržavanja za prodavca, možete ih primeniti na projekat.</span><span class="sxs-lookup"><span data-stu-id="61ad2-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="61ad2-125">Primenite uslove zadržavanja za prodavca na projekat</span><span class="sxs-lookup"><span data-stu-id="61ad2-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="61ad2-126">Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti** i otvorite projekat sa stranice liste projekata.</span><span class="sxs-lookup"><span data-stu-id="61ad2-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="61ad2-127">Na brzoj kartici **Ugovori sa prodavcima** izaberite **Dodaj liniju**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="61ad2-128">U polju **Kôd poslovnog kontakta** izaberite jednu od sledećih opcija:</span><span class="sxs-lookup"><span data-stu-id="61ad2-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="61ad2-129">**Tabela** : Uslovi zadržavanja za prodavce se primenjuju na jednog prodavca.</span><span class="sxs-lookup"><span data-stu-id="61ad2-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="61ad2-130">**Grupa** – Uslovi zadržavanja za prodavce važe za sve prodavce u grupi.</span><span class="sxs-lookup"><span data-stu-id="61ad2-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="61ad2-131">**Sve** : Uslovi zadržavanja za prodavce se primenjuju na sve prodavce.</span><span class="sxs-lookup"><span data-stu-id="61ad2-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="61ad2-132">U **polju Dobavljač/grupa prodavaca** , izaberite prodavca ili grupu prodavaca na koje se primenjuju uslovi zadržavanja za prodavce.</span><span class="sxs-lookup"><span data-stu-id="61ad2-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="61ad2-133">Ako ste izabrali **Sve** u prethodnom koraku, ovo polje nije dostupno.</span><span class="sxs-lookup"><span data-stu-id="61ad2-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="61ad2-134">U polju **Uslovi zadržavanja za prodavce** izaberite uslove zadržavanja koje ste kreirali u prethodnom postupku.</span><span class="sxs-lookup"><span data-stu-id="61ad2-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="61ad2-135">Ako projekat takođe ima uslove za plaćanje nakon uplate (PWP) za prodavca, unesite procenat praga za projekat u polje **Procenat PWP praga**.</span><span class="sxs-lookup"><span data-stu-id="61ad2-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="61ad2-136">Uslovi zadržavanja za prodavce se takođe prikazuju na porudžbenicama koje kreirate za prodavca.</span><span class="sxs-lookup"><span data-stu-id="61ad2-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
