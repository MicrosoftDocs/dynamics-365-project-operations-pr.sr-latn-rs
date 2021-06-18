---
title: Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena
description: Ova tema pruža informacije o tome kako da kreirate prilagođene skupove opcija ili entitete.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 41c57690fecbc3bee2a1eb5d26f8a6aa56d8bea9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000543"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="33514-103">Kreiranje prilagođenih polja i entiteta kao dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="33514-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="33514-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="33514-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33514-105">Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet za korišćenje kao dimenzije određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="33514-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="33514-106">Za više informacija pogledajte [Pregledu dimenzija određivanja cena](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="33514-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="33514-107">Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju.</span><span class="sxs-lookup"><span data-stu-id="33514-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="33514-108">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi.</span><span class="sxs-lookup"><span data-stu-id="33514-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="33514-109">Ovo će takođe pomoći u ponovnoj upotrebi vašeg posla i olakšati prenos ovih promena na drugu instancu. Nakon što izvršite sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.</span><span class="sxs-lookup"><span data-stu-id="33514-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="33514-110">Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="33514-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="33514-111">Dimenzija određivanja cena može biti skup opcija ili entitet.</span><span class="sxs-lookup"><span data-stu-id="33514-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="33514-112">I jedno i drugo morate da kreirate u rešenju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="33514-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="33514-113">Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.</span><span class="sxs-lookup"><span data-stu-id="33514-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="33514-114">Dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="33514-114">Entity-based dimensions</span></span>
<span data-ttu-id="33514-115">Da biste kreirali dimenzije zasnovane na entitetima, sledite ove korake:</span><span class="sxs-lookup"><span data-stu-id="33514-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="33514-116">Idite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="33514-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="33514-117">U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="33514-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="33514-118">Izaberite **Novo** da biste kreirali novi entitet pod nazivom **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="33514-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="33514-119">Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="33514-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definicija standardnog entiteta naziva](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="33514-121">Dimenzije zasnovane na skupu opcija</span><span class="sxs-lookup"><span data-stu-id="33514-121">Option set-based dimensions</span></span> 
<span data-ttu-id="33514-122">Možete kreirati dve dimenzije zasnovane na skupovima opcija.</span><span class="sxs-lookup"><span data-stu-id="33514-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="33514-123">Koristite **Mesto rada resursa** da biste pratili cenu za rad na lokaciji **Kuća** i za rad **Na lokaciji**.</span><span class="sxs-lookup"><span data-stu-id="33514-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="33514-124">Koristite **Radno vreme resursa** sa vrednostima **Redovno** i **Prekovremeno** da biste primenili proviziju kada je posao završen.</span><span class="sxs-lookup"><span data-stu-id="33514-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="33514-125">Sledeći grafikon daje prikaz dimenzije **Mesto rada resursa**.</span><span class="sxs-lookup"><span data-stu-id="33514-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radna lokacija resursa](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="33514-127">Sledeći grafikon daje prikaz dimenzije **Radno vreme resursa**.</span><span class="sxs-lookup"><span data-stu-id="33514-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radno vreme resursa](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="33514-129">Idite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="33514-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="33514-130">U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**.</span><span class="sxs-lookup"><span data-stu-id="33514-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="33514-131">Izaberite **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="33514-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="33514-132">Kreiranje podataka za dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="33514-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="33514-133">Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge.</span><span class="sxs-lookup"><span data-stu-id="33514-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="33514-134">Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="33514-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="33514-135">Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="33514-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="33514-136">Izaberite **Napredna pretraga**.</span><span class="sxs-lookup"><span data-stu-id="33514-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="33514-137">Izaberite entitet **Standardna pozicija** a, a zatim izaberite **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="33514-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="33514-138">Biće prikazani svi redovi u entitetu **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="33514-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="33514-139">Izaberite **Novo**, a zatim u polje **Ime** unesite „Inženjer sistema“ i izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="33514-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="33514-140">Zatvorite stranicu.</span><span class="sxs-lookup"><span data-stu-id="33514-140">Close the page.</span></span> 
5. <span data-ttu-id="33514-141">Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.</span><span class="sxs-lookup"><span data-stu-id="33514-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Probni podaci za entitet Standardna pozicija](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]