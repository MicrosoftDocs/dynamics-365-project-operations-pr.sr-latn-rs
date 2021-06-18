---
title: Kreiranje prilagođenih polja i entiteta
description: Ova tema objašnjava kako se kreiraju skupovi opcija i entiteti u rešenju platforme Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998968"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="d4a16-103">Kreiranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="d4a16-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d4a16-104">Obavite sledeće korake kada želite da kreirate prilagođeni skup opcija ili entitet na Power Apps platformi.</span><span class="sxs-lookup"><span data-stu-id="d4a16-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="d4a16-105">Procedure u ovoj temi bi trebalo da budu završene korišćenjem veb interfejsa aplikacije Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="d4a16-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4a16-106">Preporučuje se da se sve promene dimenzije prilagođene cene unose u odvojenom rešenju.</span><span class="sxs-lookup"><span data-stu-id="d4a16-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="d4a16-107">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci.</span><span class="sxs-lookup"><span data-stu-id="d4a16-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d4a16-108">Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje cena.</span><span class="sxs-lookup"><span data-stu-id="d4a16-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="d4a16-109">Kreiranje prilagođenih polja i skupova opcija u rešenju za dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="d4a16-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="d4a16-110">Dimenzija određivanja cena može biti skup opcija ili entitet.</span><span class="sxs-lookup"><span data-stu-id="d4a16-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="d4a16-111">I jedno i drugo morate da kreirate u rešenju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="d4a16-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="d4a16-112">Koraci u ovoj proceduri objašnjavaju kako da kreirate dimenzije zasnovane na entitetima i dimenzije zasnovane na skupu opcija.</span><span class="sxs-lookup"><span data-stu-id="d4a16-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="d4a16-113">Dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="d4a16-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="d4a16-114">U PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="d4a16-115">U levom oknu za navigaciju istraživača rešenja izaberite **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="d4a16-116">Kliknite na **Novi** da biste kreirali novi entitet pod nazivom **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="d4a16-117">Unesite preostale potrebne informacije, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definicija standardnog entiteta naziva](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="d4a16-119">Dimenzije zasnovane na skupu opcija</span><span class="sxs-lookup"><span data-stu-id="d4a16-119">Option set-based dimensions</span></span> 
<span data-ttu-id="d4a16-120">Možete kreirati dve dimenzije zasnovane na skupovima opcija.</span><span class="sxs-lookup"><span data-stu-id="d4a16-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="d4a16-121">Pomoću polja **Radna lokacija resursa** pratite cenu radne lokacije **Kod kuće** i **Na lokaciji** i koristite **Radno vreme resursa** sa vrednostima **Standardno** i **Prekovremeno** da biste primenili proviziju kada se posao završi.</span><span class="sxs-lookup"><span data-stu-id="d4a16-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="d4a16-122">U PSA kliknite na **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije cene**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d4a16-123">U levom oknu za navigaciju istraživača rešenja izaberite **Skupovi opcija**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="d4a16-124">Kliknite na **Novo** da biste kreirali novi skup opcija, unesite preostale zahtevane informacije, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="d4a16-125">Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radna lokacija resursa</span><span class="sxs-lookup"><span data-stu-id="d4a16-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="d4a16-126">Dimenzija određivanja cena zasnovana na skupu opcija pod nazivom Radno vreme resursa</span><span class="sxs-lookup"><span data-stu-id="d4a16-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="d4a16-127">Kreiranje podataka za dimenzije zasnovane na entitetima</span><span class="sxs-lookup"><span data-stu-id="d4a16-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="d4a16-128">Možete ručno kreirati podatke za dimenzije zasnovane na entitetima ili korišćenjem Microsoft Excel poziva za uvoz ili usluge.</span><span class="sxs-lookup"><span data-stu-id="d4a16-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="d4a16-129">Koristite korake iz ove procedure da biste kreirali dve standardne pozicije, **Inženjer sistema** i **Viši inženjer sistema** iz dimenzije zasnovane na entitetima **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="d4a16-130">Ako je obim podataka koje želite da kreirate mali, kao u sledećem primeru, možete da koristite standardni obrazac.</span><span class="sxs-lookup"><span data-stu-id="d4a16-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="d4a16-131">U aplikaciji PSA, kliknite na **Napredna pretraga**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="d4a16-132">Izaberite entitet **Standardna pozicija**, a zatim kliknite na **Rezultati**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="d4a16-133">Biće prikazani svi redovi u entitetu **Standardna pozicija**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="d4a16-134">Kliknite na dugme **Novo**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-134">Click **New**.</span></span> <span data-ttu-id="d4a16-135">U polje **Naziv** unesite „Inženjer sistema“, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d4a16-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="d4a16-136">Zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="d4a16-136">Close the form.</span></span> 
4. <span data-ttu-id="d4a16-137">Ponovite korake 1-3 da biste kreirali još jednu standardnu poziciji „Viši inženjer sistema“.</span><span class="sxs-lookup"><span data-stu-id="d4a16-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="d4a16-138">Probni podaci za entitet Standardna pozicija</span><span class="sxs-lookup"><span data-stu-id="d4a16-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]