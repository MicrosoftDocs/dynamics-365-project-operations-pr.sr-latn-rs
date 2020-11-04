---
title: Raspored troškova istrage savezne pomoći
description: Ova tema pruža informacije o Rasporedu troškova istrage savezne pomoći.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083564"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="e5ba1-103">Raspored troškova istrage savezne pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5ba1-104">Prema cirkularnom obaveštenju A-133 Kancelarije za upravljanje i budžet, agencije koje primaju savezna sredstva podležu zahtevima revizije, koje su poznate i kao pojedinačne revizije.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="e5ba1-105">Proces revizije se koristi za redovno izveštavanje o prihodima i rashodima saveznih bespovratnih sredstava.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="e5ba1-106">Deo izveštaja pojedinačne revizije uključuje Raspored troškova istrage savezne pomoći (SEFA).</span><span class="sxs-lookup"><span data-stu-id="e5ba1-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="e5ba1-107">Raspored troškova istrage savezne pomoći uključuje naziv i broj Kataloga savezne domaće pomoći (CFDA), broj bespovratne pomoći, godinu dodele, naziv savezne agencije koja obezbeđuje sredstva i naziv entiteta koji daje odobrenje.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="e5ba1-108">Upit se odnosi na određeni period.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="e5ba1-109">Tipično je taj period isti kao i period finansijskih izveštaja, koji je fiskalna godina.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="e5ba1-110">Upit uključuje grantove koji imaju datume projekcije u odabranom vremenskom rasponu.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="e5ba1-111">Kolona **Agencija koja daje pomoć** u upitu prikazuje klijenta pomoći ili, za prolaznu pomoć, agenciju koja daje pomoć.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="e5ba1-112">Za prolaznu pomoć, kolona **Prolazna agencija** prikazuje klijenta koji je dobio pomoć.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="e5ba1-113">Ako pomoć nije prolazna, kolona **Prolazna agencija** je prazna.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="e5ba1-114">Podešavanje CFDA grupa</span><span class="sxs-lookup"><span data-stu-id="e5ba1-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="e5ba1-115">Morate da postavite CFDA grupe koji se mogu povezati sa CFDA brojevima u Rasporedu troškova istrage savezne pomoći.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="e5ba1-116">Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Katalog grupa savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="e5ba1-117">Da biste kreirali CFDA grupu, izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="e5ba1-118">Unesite naziv grupe.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="e5ba1-119">Izaberite **Sačuvaj** da biste sačuvali promene.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="e5ba1-120">Podesite CFDA brojeve</span><span class="sxs-lookup"><span data-stu-id="e5ba1-120">Set up CFDA numbers</span></span>

<span data-ttu-id="e5ba1-121">Morate da postavite CFDA brojeve koji se mogu dodati u pomoć i uključiti u Raspored troškova istrage savezne pomoći.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="e5ba1-122">Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Katalog brojeva savezne domaće pomoći**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="e5ba1-123">Da biste kreirali CFDA broj, izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="e5ba1-124">U kolonu **Broj** unesite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="e5ba1-125">Pritisnite taster **Tab**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="e5ba1-126">U kolonu **Opis** unesite CFDA naziv.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="e5ba1-127">Pritisnite taster **Tab**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="e5ba1-128">Opcionalno: U polje **Grupa programa** dodajte odgovarajuću CFDA grupu.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="e5ba1-129">Izaberite **Sačuvaj** da biste sačuvali promene.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="e5ba1-130">Postavite pomoć radi izveštavanja o Rasporedu troškova istrage savezne pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="e5ba1-131">Idite na **Upravljanje projektima i računovodstvo \> Pomoć \> Pomoć** , i izaberite postojeću pomoć.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="e5ba1-132">Na brzoj kartici **Podešavanje** , u polju **Katalog savezne domaće pomoći** dodelite CFDA broj.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="e5ba1-133">CFDA broj na pomoći određuje CFDA grupu za izveštavanje.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="e5ba1-134">Na brzoj kartici **Kontakt informacije** unesite informacije o davaocu pomoći prateći ove korake:</span><span class="sxs-lookup"><span data-stu-id="e5ba1-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="e5ba1-135">U polju **Odobri klijenta** unesite klijenta koji je odgovoran za pomoć.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="e5ba1-136">Za postojeću pomoć ove informacije su možda već unete.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="e5ba1-137">Navedite da li je korisnik pomoći donator.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="e5ba1-138">Ako je korisnik pomoći donator, ostavite polje za potvrdu **Prolazno** prazno.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="e5ba1-139">Ako je drugi klijent donator, a korisnik bespovratne pomoći je odgovoran za trošenje i praćenje novca, potvrdite izbor u polju za potvrdu **Prolazno**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="e5ba1-140">Ako ste izabrali polje za potvrdu **Prolazno** u prethodnom koraku, u polje **Agencija koja daje pomoć** polje, unesite klijenta koji je obezbedio pomoć.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="e5ba1-141">Agencija koja daje pomoć i korisnik pomoći ne može biti isti klijent.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="e5ba1-142">Evo primera prolazne pomoći:</span><span class="sxs-lookup"><span data-stu-id="e5ba1-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="e5ba1-143">Savezna vlada finansirala je infrastrukturni projekat za državu.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="e5ba1-144">Savezna vlada dala je novac državi da ga potroši.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="e5ba1-145">U ovom slučaju, savezna vlada je agencija koja daje pomoć, a država je korisnik pomoći.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="e5ba1-146">Kada prvi put uključite funkciju, početni CFDA brojevi će se uneti pomoću postojećih brojeva u pomoći.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="e5ba1-147">Isključite pomoći iz SEFA izveštavanja na osnovu vrste pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="e5ba1-148">Idite na **Upravljanje projektima i računovodstvo \> Podešavanje \> Pomoć \> Vrste pomoći**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="e5ba1-149">Na brzoj kartici **Podrazumevane informacije** izaberite polje za potvrdu **Raspored troškova istrage savezne pomoći**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="e5ba1-150">Izaberite **Sačuvaj** da biste sačuvali promene.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="e5ba1-151">Pokrenite Raspored troškova istrage savezne pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="e5ba1-152">Idite na **Upravljanje projektima i računovodstvo \> Upiti i izveštaji \> Upit za pomoć \> Raspored troškova istrage savezne pomoći**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="e5ba1-153">U odeljku **Parametri** pratite sledeće korake:</span><span class="sxs-lookup"><span data-stu-id="e5ba1-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="e5ba1-154">U polju **Interval datuma** izaberite kôd za interval datuma.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="e5ba1-155">Alternativno, u poljima **Od datuma** i **Do danas** definišite datumski interval.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="e5ba1-156">Opcionalno: Da biste u upit uključili samo obračunate transakcije kao prihod, postavite opciju **Uključite samo obračunate prihode** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="e5ba1-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="e5ba1-157">Kolone</span><span class="sxs-lookup"><span data-stu-id="e5ba1-157">Columns</span></span>

<span data-ttu-id="e5ba1-158">Raspored troškova istrage savezne pomoći uključuje sledeće kolone:</span><span class="sxs-lookup"><span data-stu-id="e5ba1-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="e5ba1-159">Katalog naziva grupa Savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="e5ba1-160">Agencija koja daje pomoć</span><span class="sxs-lookup"><span data-stu-id="e5ba1-160">Grantor agency</span></span>
- <span data-ttu-id="e5ba1-161">Prolazna agencija</span><span class="sxs-lookup"><span data-stu-id="e5ba1-161">Pass-through agency</span></span>
- <span data-ttu-id="e5ba1-162">Naziv pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-162">Grant name</span></span>
- <span data-ttu-id="e5ba1-163">ID pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-163">Grant ID</span></span>
- <span data-ttu-id="e5ba1-164">ID prijave za pomoć</span><span class="sxs-lookup"><span data-stu-id="e5ba1-164">Grant application ID</span></span>
- <span data-ttu-id="e5ba1-165">Katalog Savezne domaće pomoći</span><span class="sxs-lookup"><span data-stu-id="e5ba1-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="e5ba1-166">Priznanice</span><span class="sxs-lookup"><span data-stu-id="e5ba1-166">Receipts</span></span>
- <span data-ttu-id="e5ba1-167">Rashodi</span><span class="sxs-lookup"><span data-stu-id="e5ba1-167">Expenditures</span></span>
