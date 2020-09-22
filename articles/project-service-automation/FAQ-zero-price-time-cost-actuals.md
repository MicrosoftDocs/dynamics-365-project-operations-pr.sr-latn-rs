---
title: Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o ceni za utrošeno vreme?
description: Rešavanje problema zbog čega se cena podrazumevano vraća na 0 u stvarnim podacima o ceni za utrošeno vreme.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: 597d75b7-fadf-4947-8d52-95425ff90324
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 448c6c0569a40e1d7cb133561435811ecedb4356
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755270"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="25658-103">Zašto se cena podrazumevano vraća na nulu u stvarnim podacima o ceni za utrošeno vreme?</span><span class="sxs-lookup"><span data-stu-id="25658-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="25658-104">Ova najčešća pitanja se odnose na stvarne podatke gde je klasa transakcije podešena na Vreme, a gde je vrsta transakcije Trošak.</span><span class="sxs-lookup"><span data-stu-id="25658-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="25658-105">Slede tri provere koje će vam olakšati da rešite zbog čega se cena podrazumevano vraća na vrednost 0 u stvarnim podacima o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="25658-106">Provera 1: Identifikujte cenovnik koštanja za projekat</span><span class="sxs-lookup"><span data-stu-id="25658-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="25658-107">Pronađite projekat iz polja Projekat za stvarni podatak, a zatim idite na stranicu projekta.</span><span class="sxs-lookup"><span data-stu-id="25658-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="25658-108">Kliknite na vezu jedinice ugovaranja u polju.</span><span class="sxs-lookup"><span data-stu-id="25658-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="25658-109">Na stranici Jedinica ugovaranja proverite da li jedinica ugovaranja ima cenovnik u mreži Cenovnici koštanja.</span><span class="sxs-lookup"><span data-stu-id="25658-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="25658-110">Ako postoji više od jednog cenovnika, izolovali ste problem.</span><span class="sxs-lookup"><span data-stu-id="25658-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="25658-111">Project Service podržava samo jedan cenovnik po organizacionoj jedinici.</span><span class="sxs-lookup"><span data-stu-id="25658-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="25658-112">Uklonite sve cenovnike iz ovog entiteta sve dok ne ostane samo jedan priložen cenovnik u mreži Cenovnici koštanja za organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="25658-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="25658-113">Ako organizacionoj jedinici nije priložen nijedan cenovnik, zabeležite valutu organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="25658-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="25658-114">Idite u Project Service, a zatim na stavku Parametri i otvorite karticu Cenovnici. Proverite da li postoje cenovnici čiji je kontekst podešen na Cena, a da se valuta podudara sa valutom organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="25658-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="25658-115">Ako ne postoje cenovnici koji ispunjavaju kriterijume, izolovali ste problem.</span><span class="sxs-lookup"><span data-stu-id="25658-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="25658-116">Uverite se da imate bar jedan cenovnik čiji je kontekst podešen na Cena i čija se valuta podudara sa valutom organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="25658-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="25658-117">Ako postoji više cenovnika koji ispunjavaju kriterijume, nastavite sa čitanjem ovog dokumenta kako biste obavili dodatne provere.</span><span class="sxs-lookup"><span data-stu-id="25658-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="25658-118">Provera 2: Da li je bilo koji od cenovnika identifikovanih iznad važeći za određeni datum stvarnog podatka o ceni za utrošeno vreme?</span><span class="sxs-lookup"><span data-stu-id="25658-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="25658-119">Da bi Project Service razmotrio cenovnik za podrazumevanu cenu, taj cenovnik treba da bude primenjiv za datum na stvarnom podatku o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="25658-120">Proverite sledeće da biste proverili da li su cenovnici identifikovani iznad primenjivi:</span><span class="sxs-lookup"><span data-stu-id="25658-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="25658-121">Proverite da li su datumi početka i završetka na kartici Opšti podaci za priložene cenovnike prazni.</span><span class="sxs-lookup"><span data-stu-id="25658-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="25658-122">Ako su datumi početka i završetka na cenovnicima identifikovanim gore prazni, izolovali ste problem.</span><span class="sxs-lookup"><span data-stu-id="25658-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="25658-123">Zabeležite polje datuma početka na stvarnom podatku o ceni za utrošeno vreme i proverite da li je neki od identifikovanih cenovnika primenjiv za taj datum.</span><span class="sxs-lookup"><span data-stu-id="25658-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="25658-124">Na primer, datum stvarnog podatka o ceni za utrošeno vreme bi trebalo da pada unutar datuma početka i završetka u cenovniku.</span><span class="sxs-lookup"><span data-stu-id="25658-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="25658-125">Ako ne postoji nijedan cenovnik koji pokriva taj datum na stvarnom podatku o ceni za utrošeno vreme, izolovali ste problem.</span><span class="sxs-lookup"><span data-stu-id="25658-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="25658-126">Izmenite datume početka i završetka za cenovnik da biste osigurali da cenovnik pokriva datum stvarnog podatka o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="25658-127">Ako postoji više cenovnika koji pokrivaju taj datum na stvarnom podatku o ceni za utrošeno vreme, izolovali ste problem.</span><span class="sxs-lookup"><span data-stu-id="25658-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="25658-128">Ovo možete da ispravite uređivanjem datuma početka i završetka cenovnika, tako da postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="25658-129">Ako postoji samo jedan cenovnik koji pokriva datum stvarnog podatka o ceni za utrošeno vreme, pređite na sledeću proveru u dokumentu.</span><span class="sxs-lookup"><span data-stu-id="25658-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="25658-130">Nakon što ste obavili potrebne popravke, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o ceni za utrošeno vreme prikazuje važeću cenu.</span><span class="sxs-lookup"><span data-stu-id="25658-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="25658-131">Proverite 3: Da li postoji cena u cenovniku za dimenzije formiranja cene na stvarnoj podatku o ceni za utrošeno vreme?</span><span class="sxs-lookup"><span data-stu-id="25658-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="25658-132">Ako ste uspešno dovršili proveru 1 i proveru 2, trebalo bi sada da imate samo jedan cenovnik koji je primenljiv za datum stvarnog podatka o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="25658-133">Otvorite ovaj cenovnik i idite do kartice Cene uloga. Uverite se da postoji red u mreži za dimenzije obrazovanja cena u stvarnom podatku o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="25658-134">Ako u mreži uloge cene ne postoji red za dimenzije obrazovanja cene na stvarnom podatku o ceni za utrošeno vreme, onda ste izolovali problem.</span><span class="sxs-lookup"><span data-stu-id="25658-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="25658-135">Kreirajte red u mreži Cene uloga za dimenzije određivanja cena na stvarnom podatku o ceni za utrošeno vreme.</span><span class="sxs-lookup"><span data-stu-id="25658-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="25658-136">Nakon što to uradite, ponovo kreirajte unos utrošenog vremena, odobrite ga i potvrdite da stvarni podatak o ceni za utrošeno vreme prikazuje važeću cenu.</span><span class="sxs-lookup"><span data-stu-id="25658-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="25658-137">Ako i dalje ne vidite važeću cenu u stvarnom podatku o ceni za utrošeno vreme nakon što obavite gorenavedene tri provere, pošaljite tiket podršci.</span><span class="sxs-lookup"><span data-stu-id="25658-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



