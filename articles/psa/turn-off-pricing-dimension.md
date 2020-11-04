---
title: Isključivanje dimenzije za određivanje cena
description: Ova tema pokazuje kako se podešavaju dimenzije za određivanje cena u rešenju Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083665"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="14d53-103">Isključivanje dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="14d53-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="14d53-104">Možda ćete morati da pregledate i ažurirate svoju strategiju određivanja cena svakih nekoliko godina.</span><span class="sxs-lookup"><span data-stu-id="14d53-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="14d53-105">Sve ispravke koje unesete mogu zahtevati da isključite postojeću dimenziju za određivanje cena i kreirate novu.</span><span class="sxs-lookup"><span data-stu-id="14d53-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="14d53-106">Na primer, možda ste prethodno određivali cenu po **ulozi** , ali ste sada odlučili da to radite prema **radnom iskustvu**.</span><span class="sxs-lookup"><span data-stu-id="14d53-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="14d53-107">Ovo može zahtevati da isključite dimenziju za određivanje cena **Uloga** i da kreirate **Radno iskustvo** kao novu dimenziju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="14d53-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="14d53-108">Dimenzija za određivanje cena, bez obzira na to da li je unapred definisana ili prilagođena, može se isključiti ako polja **Primenljivo na troškove** i **Primenljivo na prodaju** u okviru dimenzije za određivanje cena podesite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="14d53-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="14d53-109">Međutim, kada to uradite, možda ćete dobiti sledeću poruku o grešci.</span><span class="sxs-lookup"><span data-stu-id="14d53-109">However, when you do this, you might receive the following error message.</span></span>

![Greška poslovnog procesa je moguća kada isključujete dimenziju za određivanje cena](media/Business-Process-Error.png)


<span data-ttu-id="14d53-111">Ova poruka o grešci ukazuje na to da postoje zapisi cena koji su prethodno podešeni za dimenziju koja je isključena.</span><span class="sxs-lookup"><span data-stu-id="14d53-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="14d53-112">Sve zapise **Cena uloge** i **Provizija na cenu uloge** koji se odnose na dimenziju morate izbrisati pre nego što se primenjivost dimenzije podesi na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="14d53-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="14d53-113">Ovo pravilo primenjuje se na unapred definisane dimenzije za određivanje cena i sve prilagođene dimenzije za određivanje cena koje ste možda kreirali.</span><span class="sxs-lookup"><span data-stu-id="14d53-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="14d53-114">Razlog ove validacije je što Project Service ima ograničenje da svaki zapis **Cena uloge** mora da ima jedinstvenu kombinaciju dimenzija.</span><span class="sxs-lookup"><span data-stu-id="14d53-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="14d53-115">Na primer, u cenovniku pod nazivom **Stope troška u SAD za 2018** , imate sledeće redove **Cena uloge**.</span><span class="sxs-lookup"><span data-stu-id="14d53-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="14d53-116">Standardna pozicija</span><span class="sxs-lookup"><span data-stu-id="14d53-116">Standard Title</span></span>         | <span data-ttu-id="14d53-117">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="14d53-117">Org Unit</span></span>    |<span data-ttu-id="14d53-118">Jedinica</span><span class="sxs-lookup"><span data-stu-id="14d53-118">Unit</span></span>   |<span data-ttu-id="14d53-119">Cena</span><span class="sxs-lookup"><span data-stu-id="14d53-119">Price</span></span>  |<span data-ttu-id="14d53-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="14d53-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="14d53-121">Inženjer sistema</span><span class="sxs-lookup"><span data-stu-id="14d53-121">Systems Engineer</span></span>|<span data-ttu-id="14d53-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="14d53-122">Contoso US</span></span>|<span data-ttu-id="14d53-123">Hour</span><span class="sxs-lookup"><span data-stu-id="14d53-123">Hour</span></span>| <span data-ttu-id="14d53-124">100.</span><span class="sxs-lookup"><span data-stu-id="14d53-124">100</span></span>|<span data-ttu-id="14d53-125">USD</span><span class="sxs-lookup"><span data-stu-id="14d53-125">USD</span></span>|
| <span data-ttu-id="14d53-126">Viši inženjer sistema</span><span class="sxs-lookup"><span data-stu-id="14d53-126">Senior Systems Engineer</span></span>|<span data-ttu-id="14d53-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="14d53-127">Contoso US</span></span>|<span data-ttu-id="14d53-128">Hour</span><span class="sxs-lookup"><span data-stu-id="14d53-128">Hour</span></span>| <span data-ttu-id="14d53-129">150</span><span class="sxs-lookup"><span data-stu-id="14d53-129">150</span></span>| <span data-ttu-id="14d53-130">USD</span><span class="sxs-lookup"><span data-stu-id="14d53-130">USD</span></span>|


<span data-ttu-id="14d53-131">Kada isključite polje **Standardna pozicija** kao dimenziju za određivanje cena, a Project Service mehanizam za određivanje cena pretražuje cenu, koristiće samo vrednost **Organizaciona jedinica** iz konteksta unosa.</span><span class="sxs-lookup"><span data-stu-id="14d53-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="14d53-132">Ako je **Organizaciona jedinica** konteksta unosa „Contoso US“, rezultat će biti neodređen jer će se oba reda podudarati.</span><span class="sxs-lookup"><span data-stu-id="14d53-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="14d53-133">Da biste izbegli ovaj scenario, kada kreirate zapise **Cena uloge** , Project Service proverava da li je kombinacije dimenzija jedinstvena.</span><span class="sxs-lookup"><span data-stu-id="14d53-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="14d53-134">Ako je dimenzija isključena nakon kreiranja zapisa **Cena uloge** , ovo ograničenje može da se prekrši.</span><span class="sxs-lookup"><span data-stu-id="14d53-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="14d53-135">Zbog toga je neophodno da pre isključivanja dimenzije izbrišete sve redove **Cena uloge** i **Provizija na cenu uloge** u kojima je ta vrednost dimenzije popunjena.</span><span class="sxs-lookup"><span data-stu-id="14d53-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

