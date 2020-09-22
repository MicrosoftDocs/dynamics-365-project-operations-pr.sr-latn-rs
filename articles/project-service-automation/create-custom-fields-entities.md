---
title: Kreiranje prilagođenih polja i entiteta
description: Ova tema objašnjava kako se kreiraju skupovi opcija i entiteti u rešenju platforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755231"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="a0639-103">Kreiranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="a0639-103">Create custom fields and entities</span></span> 

<span data-ttu-id="a0639-104">Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet na Power Apps platformi.</span><span class="sxs-lookup"><span data-stu-id="a0639-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="a0639-105">Procedure u ovoj temi bi trebalo da budu završene korišćenjem veb interfejsa aplikacije Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="a0639-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a0639-106">Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju.</span><span class="sxs-lookup"><span data-stu-id="a0639-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="a0639-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci.</span><span class="sxs-lookup"><span data-stu-id="a0639-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="a0639-108">Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.</span><span class="sxs-lookup"><span data-stu-id="a0639-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="a0639-109">Kreiranje prilagođenog rešenja za dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="a0639-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="a0639-110">U aplikaciji PSA, kliknite na **Podešavanja** > **Rešenja**, a zatim kliknite na **Novo** da biste kreirali novo rešenje.</span><span class="sxs-lookup"><span data-stu-id="a0639-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="a0639-111">Imenujte rešenje, **\<ime organizacije > dimenzije za određivanje cena**, unesite preostale zahtevane informacije, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a0639-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Kreiranje prilagođenog rešenja za dimenzije za određivanje cena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="a0639-113">Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="a0639-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="a0639-114">Dimenzija određivanja cena može biti skup opcija ili entitet.</span><span class="sxs-lookup"><span data-stu-id="a0639-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="a0639-115">I jedno i drugo morate da kreirate u rešenju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="a0639-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="a0639-116">Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.</span><span class="sxs-lookup"><span data-stu-id="a0639-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="a0639-117">Dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="a0639-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="a0639-118">U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**.</span><span class="sxs-lookup"><span data-stu-id="a0639-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="a0639-119">U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="a0639-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="a0639-120">Kliknite na **Novi** da biste kreirali novi entitet pod nazivom **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="a0639-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="a0639-121">Unesite preostale potrebne informacije, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a0639-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija standardnog entiteta naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="a0639-123">Dimenzije zasnovane na skupu opcija</span><span class="sxs-lookup"><span data-stu-id="a0639-123">Option set-based dimensions</span></span> 
<span data-ttu-id="a0639-124">Možete kreirati dve dimenzije zasnovane na skupovima opcija.</span><span class="sxs-lookup"><span data-stu-id="a0639-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="a0639-125">Pomoću polja **Radna lokacija resursa** pratite cenu radne lokacije **Kod kuće** i **Na lokaciji** i koristite **Radno vreme resursa** sa vrednostima **Standardno** i **Prekovremeno** da biste primenili proviziju kada se posao završi.</span><span class="sxs-lookup"><span data-stu-id="a0639-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="a0639-126">U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**.</span><span class="sxs-lookup"><span data-stu-id="a0639-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a0639-127">U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**.</span><span class="sxs-lookup"><span data-stu-id="a0639-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="a0639-128">Kliknite na **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a0639-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="a0639-129">Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radna lokacija resursa</span><span class="sxs-lookup"><span data-stu-id="a0639-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="a0639-130">Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radno vreme resursa</span><span class="sxs-lookup"><span data-stu-id="a0639-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="a0639-131">Kreiranje podataka za dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="a0639-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="a0639-132">Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge.</span><span class="sxs-lookup"><span data-stu-id="a0639-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="a0639-133">Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="a0639-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="a0639-134">Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="a0639-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="a0639-135">U aplikaciji PSA, kliknite na **Napredna pretraga**.</span><span class="sxs-lookup"><span data-stu-id="a0639-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="a0639-136">Izaberite entitet **Standardna pozicija**, a zatim kliknite na **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="a0639-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="a0639-137">Biće prikazani svi redovi u entitetu **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="a0639-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="a0639-138">Kliknite na dugme **Novo**.</span><span class="sxs-lookup"><span data-stu-id="a0639-138">Click **New**.</span></span> <span data-ttu-id="a0639-139">U polje **Naziv** unesite „Inženjer sistema“, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a0639-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="a0639-140">Zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="a0639-140">Close the form.</span></span> 
4. <span data-ttu-id="a0639-141">Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.</span><span class="sxs-lookup"><span data-stu-id="a0639-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="a0639-142">Probni podaci za entitet Standardna pozicija</span><span class="sxs-lookup"><span data-stu-id="a0639-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="a0639-143">Dodajte sve zahtevane PSA entitete i srodne komponente u rešenje za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="a0639-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="a0639-144">Moraćete da dodate sledeće Project Service entitete u rešenje za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="a0639-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="a0639-145">Korake u ovoj proceduri koristite da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="a0639-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="a0639-146">U aplikaciji PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput na **\<ime organizacije > dimenzije određivanja cena**.</span><span class="sxs-lookup"><span data-stu-id="a0639-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a0639-147">U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="a0639-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="a0639-148">U dijalogu **Komponente rešenja** izaberite sledeće entitete:</span><span class="sxs-lookup"><span data-stu-id="a0639-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="a0639-149">Stvarno</span><span class="sxs-lookup"><span data-stu-id="a0639-149">Actual</span></span>
- <span data-ttu-id="a0639-150">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="a0639-150">Bookable Resource</span></span>
- <span data-ttu-id="a0639-151">Stavka procene</span><span class="sxs-lookup"><span data-stu-id="a0639-151">Estimate Line</span></span>
- <span data-ttu-id="a0639-152">Detalj stavke fakture</span><span class="sxs-lookup"><span data-stu-id="a0639-152">Invoice Line Detail</span></span>
- <span data-ttu-id="a0639-153">Stavka u glavnoj knjizi</span><span class="sxs-lookup"><span data-stu-id="a0639-153">Journal Line</span></span>
- <span data-ttu-id="a0639-154">Detalj predmeta ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="a0639-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="a0639-155">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="a0639-155">Project Team Member</span></span>
- <span data-ttu-id="a0639-156">Detalj stavke ponude</span><span class="sxs-lookup"><span data-stu-id="a0639-156">Quote Line Detail</span></span>
- <span data-ttu-id="a0639-157">Provizija na cenu uloge</span><span class="sxs-lookup"><span data-stu-id="a0639-157">Role Price Markup</span></span>
- <span data-ttu-id="a0639-158">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="a0639-158">Role Price</span></span> 
- <span data-ttu-id="a0639-159">Stavka vremena</span><span class="sxs-lookup"><span data-stu-id="a0639-159">Time Entry</span></span> 

> ![Dodavanje postojećih entiteta u rešenje za dimenzije određivanja cena](media/Existing-entities-to-PD-solution.png)

> ![Izaberite komponente rešenja](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="a0639-162">Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.</span><span class="sxs-lookup"><span data-stu-id="a0639-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="a0639-163">Kliknite na **Ne** kada se od vas zatraži da uključite zavisne entitete za goreizabrane entitete.</span><span class="sxs-lookup"><span data-stu-id="a0639-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Nemojte da uključujete sve povezane komponente](media/Do-not-include-required.png)


