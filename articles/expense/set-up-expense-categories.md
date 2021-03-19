---
title: Podešavanje kategorija troškova
description: Ova tema pruža informacije o tome kako da postavite kategorije troškova i deljene kategorije za izveštaje o troškovima.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276140"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="7ca8a-103">Podešavanje kategorija troškova</span><span class="sxs-lookup"><span data-stu-id="7ca8a-103">Set up expense categories</span></span>

<span data-ttu-id="7ca8a-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="7ca8a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7ca8a-105">Kada zaposleni kreiraju izveštaje o troškovima, svaki trošak koji evidentiraju mora biti povezan sa kategorijom troškova.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="7ca8a-106">Kategorije troškova su izvedene iz deljenih kategorija koje se mogu deliti između pravnih lica u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="7ca8a-107">U zavisnosti od toga kako je vaša organizacija definisana, ove kategorije troškova mogu se deliti i u drugim oblastima.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="7ca8a-108">Na osnovu definicije vaše organizacije i smernica tima za primenu, morate da odredite da li će se kategorije koje se koriste u upravljanju troškovima koristiti samo u upravljanju troškovima ili treba da se dele u drugim oblastima.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="7ca8a-109">Ove kategorije se mogu deliti između upravljanja projektima i računovodstva i upravljanja troškovima ili između upravljanja projektima i računovodstva i proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="7ca8a-110">Međutim, oni ne mogu da se dele između troškova upravljanja i proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="7ca8a-111">Pre nego što započnete postupak podešavanja, za svaku kategoriju troškova moraju se doneti sledeće odluke:</span><span class="sxs-lookup"><span data-stu-id="7ca8a-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="7ca8a-112">Šta je to kategorija troškova?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-112">What is the expense category?</span></span> <span data-ttu-id="7ca8a-113">Primeri uključuju kategorije za letove, hotele ili kilometražu.</span><span class="sxs-lookup"><span data-stu-id="7ca8a-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="7ca8a-114">Može li se kategorija troškova takođe koristiti u upravljanju projektima i računovodstvu?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="7ca8a-115">Ako može, morate doneti i sledeće odluke:</span><span class="sxs-lookup"><span data-stu-id="7ca8a-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7ca8a-116">Koji računi troškova će se koristiti za sledeće troškove?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="7ca8a-117">Cena</span><span class="sxs-lookup"><span data-stu-id="7ca8a-117">Cost</span></span>
        - <span data-ttu-id="7ca8a-118">Raspodela zarada</span><span class="sxs-lookup"><span data-stu-id="7ca8a-118">Payroll allocation</span></span>
        - <span data-ttu-id="7ca8a-119">Prihodi u toku – vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="7ca8a-119">WIP-cost value</span></span>
        - <span data-ttu-id="7ca8a-120">Stavka troškova</span><span class="sxs-lookup"><span data-stu-id="7ca8a-120">Cost-item</span></span>
        - <span data-ttu-id="7ca8a-121">Prihodi u toku – vrednost troškova – stavka</span><span class="sxs-lookup"><span data-stu-id="7ca8a-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="7ca8a-122">Obračunati gubitak</span><span class="sxs-lookup"><span data-stu-id="7ca8a-122">Accrued loss</span></span>
        - <span data-ttu-id="7ca8a-123">Prihodi u toku – obračunati gubitak</span><span class="sxs-lookup"><span data-stu-id="7ca8a-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="7ca8a-124">Koji računi prihoda će se koristiti za sledeće izvore prihoda?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="7ca8a-125">Fakturisani prihod</span><span class="sxs-lookup"><span data-stu-id="7ca8a-125">Invoiced revenue</span></span>
        - <span data-ttu-id="7ca8a-126">Obračunati prihod – Vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="7ca8a-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="7ca8a-127">Prihodi u toku – vrednost prodaje</span><span class="sxs-lookup"><span data-stu-id="7ca8a-127">WIP-sales value</span></span>
        - <span data-ttu-id="7ca8a-128">Obračunati prihod – proizvodnja</span><span class="sxs-lookup"><span data-stu-id="7ca8a-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="7ca8a-129">Prihodi u toku – proizvodnja</span><span class="sxs-lookup"><span data-stu-id="7ca8a-129">WIP-production</span></span>
        - <span data-ttu-id="7ca8a-130">Obračunati prihod – dobitak</span><span class="sxs-lookup"><span data-stu-id="7ca8a-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="7ca8a-131">Prihodi u toku – dobitak</span><span class="sxs-lookup"><span data-stu-id="7ca8a-131">WIP-profit</span></span>
        - <span data-ttu-id="7ca8a-132">Obračunati prihod – pretplata</span><span class="sxs-lookup"><span data-stu-id="7ca8a-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="7ca8a-133">Prihodi u toku – pretplata</span><span class="sxs-lookup"><span data-stu-id="7ca8a-133">WIP-subscription</span></span>

- <span data-ttu-id="7ca8a-134">Šta je to tip troška?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-134">What is the expense type?</span></span>
- <span data-ttu-id="7ca8a-135">Koji je podrazumevani način plaćanja za kategoriju troška?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="7ca8a-136">Moraju li se detaljno deliti troškovi u kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="7ca8a-137">Koji je glavni podrazumevani račun za kategoriju troška?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="7ca8a-138">Koja je podrazumevana grupa poreza na promet proizvoda za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="7ca8a-139">Da li su dozvoljeni dodatni načini plaćanja za kategoriju troškova?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="7ca8a-140">Ako jesu, koji su to?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-140">If so, what are they?</span></span>
- <span data-ttu-id="7ca8a-141">Postoje li potkategorije u ovoj kategoriji troškova?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="7ca8a-142">Ako postoje potkategorije, morate doneti i sledeće odluke:</span><span class="sxs-lookup"><span data-stu-id="7ca8a-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="7ca8a-143">Da li je neka od potkategorija izuzeta od povraćaja poreza?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="7ca8a-144">Koja je grupa poreza na promet proizvoda za potkategorije?</span><span class="sxs-lookup"><span data-stu-id="7ca8a-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]