---
title: Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena
description: Ova tema pruža informacije o tome kako da kreirate prilagođene skupove opcija ili entitete.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083618"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="09c9a-103">Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="09c9a-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="09c9a-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="09c9a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09c9a-105">Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet.</span><span class="sxs-lookup"><span data-stu-id="09c9a-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09c9a-106">Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju.</span><span class="sxs-lookup"><span data-stu-id="09c9a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="09c9a-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci.</span><span class="sxs-lookup"><span data-stu-id="09c9a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="09c9a-108">Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.</span><span class="sxs-lookup"><span data-stu-id="09c9a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="09c9a-109">Kreiranje prilagođenog rešenja za dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="09c9a-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="09c9a-110">Idite na **Podešavanja** > **Rešenja** , a zatim izaberite **Novo** da biste kreirali novo rešenje.</span><span class="sxs-lookup"><span data-stu-id="09c9a-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="09c9a-111">Imenujte rešenje, **\<your organization name> dimenzije za određivanje cena** , unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="09c9a-112">Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="09c9a-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="09c9a-113">Dimenzija određivanja cena može biti skup opcija ili entitet.</span><span class="sxs-lookup"><span data-stu-id="09c9a-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="09c9a-114">I jedno i drugo morate da kreirate u rešenju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="09c9a-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="09c9a-115">Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.</span><span class="sxs-lookup"><span data-stu-id="09c9a-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="09c9a-116">Dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="09c9a-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="09c9a-117">Idite na **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="09c9a-118">U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="09c9a-119">Izaberite **Novo** da biste kreirali novi entitet pod nazivom **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="09c9a-120">Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="09c9a-121">Dimenzije zasnovane na skupu opcija</span><span class="sxs-lookup"><span data-stu-id="09c9a-121">Option set-based dimensions</span></span> 
<span data-ttu-id="09c9a-122">Možete kreirati dve dimenzije zasnovane na skupovima opcija.</span><span class="sxs-lookup"><span data-stu-id="09c9a-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="09c9a-123">Pomoću polja **Radna lokacija resursa** pratite cenu radne lokacije **Kod kuće** i **Na lokaciji** i koristite **Radno vreme resursa** sa vrednostima **Standardno** i **Prekovremeno** da biste primenili proviziju kada se posao završi.</span><span class="sxs-lookup"><span data-stu-id="09c9a-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="09c9a-124">Idite na **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="09c9a-125">U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="09c9a-126">Izaberite **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="09c9a-127">Kreiranje podataka za dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="09c9a-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="09c9a-128">Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge.</span><span class="sxs-lookup"><span data-stu-id="09c9a-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="09c9a-129">Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="09c9a-130">Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="09c9a-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="09c9a-131">Izaberite **Napredna pretraga** , izaberite entitet **Standardni naslov** , a zatim izaberite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="09c9a-132">Biće prikazani svi redovi u entitetu **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="09c9a-133">Izaberite **Novo** , a zatim u polje **Ime** unesite „Inženjer sistema“ i izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="09c9a-134">Zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="09c9a-134">Close the form.</span></span> 
4. <span data-ttu-id="09c9a-135">Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.</span><span class="sxs-lookup"><span data-stu-id="09c9a-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="09c9a-136">Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="09c9a-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="09c9a-137">Moraćete da dodate sledeće entitete u rešenje za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="09c9a-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="09c9a-138">Korake u ovoj proceduri koristite da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="09c9a-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="09c9a-139">Izaberite **Podešavanja** > **Rešenja** , a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="09c9a-140">U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="09c9a-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="09c9a-141">U dijalogu **Komponente rešenja** izaberite sledeće entitete:</span><span class="sxs-lookup"><span data-stu-id="09c9a-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="09c9a-142">Stvarno</span><span class="sxs-lookup"><span data-stu-id="09c9a-142">Actual</span></span>
  - <span data-ttu-id="09c9a-143">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="09c9a-143">Bookable Resource</span></span>
  - <span data-ttu-id="09c9a-144">Stavka procene</span><span class="sxs-lookup"><span data-stu-id="09c9a-144">Estimate Line</span></span>
  - <span data-ttu-id="09c9a-145">Detalj stavke fakture</span><span class="sxs-lookup"><span data-stu-id="09c9a-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="09c9a-146">Stavka u glavnoj knjizi</span><span class="sxs-lookup"><span data-stu-id="09c9a-146">Journal Line</span></span>
  - <span data-ttu-id="09c9a-147">Detalj predmeta ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="09c9a-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="09c9a-148">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="09c9a-148">Project Team Member</span></span>
  - <span data-ttu-id="09c9a-149">Detalj stavke ponude</span><span class="sxs-lookup"><span data-stu-id="09c9a-149">Quote Line Detail</span></span>
  - <span data-ttu-id="09c9a-150">Provizija na cenu uloge</span><span class="sxs-lookup"><span data-stu-id="09c9a-150">Role Price Markup</span></span>
  - <span data-ttu-id="09c9a-151">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="09c9a-151">Role Price</span></span> 
  - <span data-ttu-id="09c9a-152">Stavka vremena</span><span class="sxs-lookup"><span data-stu-id="09c9a-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="09c9a-153">Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.</span><span class="sxs-lookup"><span data-stu-id="09c9a-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="09c9a-154">Izaberite **Ne** kada se od vas zatraži da uključite zavisne entitete za prethodno izabrane entitete.</span><span class="sxs-lookup"><span data-stu-id="09c9a-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

