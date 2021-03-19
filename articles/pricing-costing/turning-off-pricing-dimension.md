---
title: Isključivanje dimenzije za određivanje cena
description: Ova tema pruža informacije o isključivanju dimenzija za određivanje cena.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274745"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="3699e-103">Isključivanje dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="3699e-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="3699e-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="3699e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3699e-105">Možda ćete morati da pregledate i ažurirate svoju strategiju određivanja cena svakih nekoliko godina.</span><span class="sxs-lookup"><span data-stu-id="3699e-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="3699e-106">Sve ispravke koje unesete mogu zahtevati da isključite postojeću dimenziju za određivanje cena i kreirate novu.</span><span class="sxs-lookup"><span data-stu-id="3699e-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="3699e-107">Na primer, možda ste prethodno određivali cenu po **ulozi**, ali ste sada odlučili da to radite prema **radnom iskustvu**.</span><span class="sxs-lookup"><span data-stu-id="3699e-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="3699e-108">Ovo može zahtevati da isključite dimenziju za određivanje cena **Uloga** i da kreirate **Radno iskustvo** kao novu dimenziju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="3699e-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="3699e-109">Dimenzija za određivanje cena, bez obzira na to da li je unapred definisana ili prilagođena, može se isključiti ako polja **Primenljivo na troškove** i **Primenljivo na prodaju** u okviru dimenzije za određivanje cena podesite na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="3699e-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="3699e-110">Međutim, kada to učinite, možda ćete dobiti poruku o grešci, **Dimenzija za određivanje cene se ne može ažurirati ili izbrisati ako postoje povezani zapisi cena.**</span><span class="sxs-lookup"><span data-stu-id="3699e-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Greška poslovnog procesa je moguća kada isključujete dimenziju za određivanje cena](media/Business-Process-Error.png)

<span data-ttu-id="3699e-112">Ova poruka o grešci ukazuje na to da postoje zapisi cena koji su prethodno podešeni za dimenziju koja je isključena.</span><span class="sxs-lookup"><span data-stu-id="3699e-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="3699e-113">Sve zapise **Cena uloge** i **Provizija na cenu uloge** koji se odnose na dimenziju morate izbrisati pre nego što se primenjivost dimenzije podesi na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="3699e-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="3699e-114">Ovo pravilo primenjuje se na unapred definisane dimenzije za određivanje cena i sve prilagođene dimenzije za određivanje cena koje ste možda kreirali.</span><span class="sxs-lookup"><span data-stu-id="3699e-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="3699e-115">Razlog ove validacije je što svaki zapis **Cena uloge** mora da ima jedinstvenu kombinaciju dimenzija.</span><span class="sxs-lookup"><span data-stu-id="3699e-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="3699e-116">Na primer, u cenovniku pod nazivom **Stope troška u SAD za 2018**, imate sledeće redove **Cena uloge**.</span><span class="sxs-lookup"><span data-stu-id="3699e-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="3699e-117">Standardna pozicija</span><span class="sxs-lookup"><span data-stu-id="3699e-117">Standard Title</span></span>         | <span data-ttu-id="3699e-118">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="3699e-118">Org Unit</span></span>    |<span data-ttu-id="3699e-119">Jedinica</span><span class="sxs-lookup"><span data-stu-id="3699e-119">Unit</span></span>   |<span data-ttu-id="3699e-120">Cena</span><span class="sxs-lookup"><span data-stu-id="3699e-120">Price</span></span>  |<span data-ttu-id="3699e-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="3699e-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="3699e-122">Inženjer sistema</span><span class="sxs-lookup"><span data-stu-id="3699e-122">Systems Engineer</span></span>|<span data-ttu-id="3699e-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="3699e-123">Contoso US</span></span>|<span data-ttu-id="3699e-124">Hour</span><span class="sxs-lookup"><span data-stu-id="3699e-124">Hour</span></span>| <span data-ttu-id="3699e-125">100.</span><span class="sxs-lookup"><span data-stu-id="3699e-125">100</span></span>|<span data-ttu-id="3699e-126">USD</span><span class="sxs-lookup"><span data-stu-id="3699e-126">USD</span></span>|
| <span data-ttu-id="3699e-127">Viši inženjer sistema</span><span class="sxs-lookup"><span data-stu-id="3699e-127">Senior Systems Engineer</span></span>|<span data-ttu-id="3699e-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="3699e-128">Contoso US</span></span>|<span data-ttu-id="3699e-129">Hour</span><span class="sxs-lookup"><span data-stu-id="3699e-129">Hour</span></span>| <span data-ttu-id="3699e-130">150</span><span class="sxs-lookup"><span data-stu-id="3699e-130">150</span></span>| <span data-ttu-id="3699e-131">USD</span><span class="sxs-lookup"><span data-stu-id="3699e-131">USD</span></span>|


<span data-ttu-id="3699e-132">Kada isključite polje **Standardna pozicija** kao dimenziju za određivanje cena, a mehanizam za određivanje cena pretražuje cenu, koristiće samo vrednost **Organizaciona jedinica** iz konteksta unosa.</span><span class="sxs-lookup"><span data-stu-id="3699e-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="3699e-133">Ako je **Organizaciona jedinica** konteksta unosa „Contoso US“, rezultat će biti neodređen jer će se oba reda podudarati.</span><span class="sxs-lookup"><span data-stu-id="3699e-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="3699e-134">Da biste izbegli ovaj scenario, kada kreirate zapise **Cena uloge**, sistem proverava da li je kombinacija dimenzija jedinstvena.</span><span class="sxs-lookup"><span data-stu-id="3699e-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="3699e-135">Ako je dimenzija isključena nakon kreiranja zapisa **Cena uloge**, ovo ograničenje može da se prekrši.</span><span class="sxs-lookup"><span data-stu-id="3699e-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="3699e-136">Zbog toga je neophodno da pre isključivanja dimenzije izbrišete sve redove **Cena uloge** i **Provizija na cenu uloge** u kojima je ta vrednost dimenzije popunjena.</span><span class="sxs-lookup"><span data-stu-id="3699e-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]