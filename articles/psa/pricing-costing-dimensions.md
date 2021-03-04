---
title: Matična stranica za dimenzije određivanja cena i obračuna troškova
description: Ova tema obezbeđuje pregled dimenzija za određivanje cena.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151315"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="ba7f9-103">Matična stranica za dimenzije određivanja cena i obračuna troškova</span><span class="sxs-lookup"><span data-stu-id="ba7f9-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ba7f9-104">Na dimenzije koje se koriste za određivanje cena i troškova rada u projektnim organizacijama utiču sledeći atributi:</span><span class="sxs-lookup"><span data-stu-id="ba7f9-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="ba7f9-105">Ljudi koji rade posao sličan svom iskustvu, ulozi ili geografskoj lokaciji</span><span class="sxs-lookup"><span data-stu-id="ba7f9-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="ba7f9-106">Posao koji treba obaviti, sličan po složenosti ili dobu dana</span><span class="sxs-lookup"><span data-stu-id="ba7f9-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="ba7f9-107">S obzirom na tipičnu prirodu ovih atributa posla i ljudi koji su potrebni za obavljanje posla, postoje dve vrste vrednosti dimenzija cene koje su dostupne u usluzi Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="ba7f9-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="ba7f9-108">**Skupovi opcija** – Atributi koji predstavljaju fiksna nabrajanja za skup vrednosti.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="ba7f9-109">**Vrednosti zasnovane na entitetima** – Atributi koji mogu imati različit skup vrednosti koje su konačne, ali se vremenom mogu menjati.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="ba7f9-110">Dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="ba7f9-110">Pricing dimensions</span></span>

<span data-ttu-id="ba7f9-111">PSA obavlja isporuku pomoću podrazumevanog skup dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="ba7f9-112">Možete da ih vidite tako što ćete otići na **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="ba7f9-113">U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="ba7f9-114">Ovo će vam omogućiti podešavanje cene i troška za svaku kombinaciju uloge i organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Snimak ekrana Project Service parametara sa markiranom stavkom „Primenljivo na prodaju“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="ba7f9-116">Ako ste koristili unapred definisana polja uloge i organizacionih jedinica kao dimenzije za određivanje cena pre verzije 3 aplikacije PSA, neće biti nikakvih primetnih promena.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="ba7f9-117">Možete da nastavite da koristite Project Service kao i obično.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="ba7f9-118">Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="ba7f9-119">Da biste dobili više informacija, pogledajte sledeće teme, ali imajte na umu da morate da dovršite procedure po dolenavedenom redosledu:</span><span class="sxs-lookup"><span data-stu-id="ba7f9-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="ba7f9-120">Kreiranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="ba7f9-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="ba7f9-121">Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije</span><span class="sxs-lookup"><span data-stu-id="ba7f9-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="ba7f9-122">Podešavanje prilagođenih polja kao dimenzija za određivanje cena </span><span class="sxs-lookup"><span data-stu-id="ba7f9-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="ba7f9-123">Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="ba7f9-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="ba7f9-124">Određivanje cene vremena ljudskog resursa</span><span class="sxs-lookup"><span data-stu-id="ba7f9-124">Pricing human resource time</span></span>
<span data-ttu-id="ba7f9-125">Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="ba7f9-126">Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="ba7f9-127">Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="ba7f9-128">Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji može da se rezerviše** (**bookableresource**) su primeri mogućih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="ba7f9-129">Razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="ba7f9-130">Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, bolje je da kreirate entitet nego skup opcija.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="ba7f9-131">Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina poslovnih korisnika može da dodaje nove redove u tabelu.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="ba7f9-132">Sledeći primer prikazuje kursne stope koje su podešene na osnovu uloge i organizacione jedinice resursa kome pripada resurs.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="ba7f9-133">Stope troškova se obično zasnivaju na grupi ličnih dohodaka zaposlenih i organizacionoj jedinici kojoj pripadaju.</span><span class="sxs-lookup"><span data-stu-id="ba7f9-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="ba7f9-134">U ovom primeru, tabele sa stopama naplate i stopama troškova će izgledati ovako:</span><span class="sxs-lookup"><span data-stu-id="ba7f9-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="ba7f9-135">**Primeri stopa naplate**</span><span class="sxs-lookup"><span data-stu-id="ba7f9-135">**Sample bill rates**</span></span>

| <span data-ttu-id="ba7f9-136">Uloga</span><span class="sxs-lookup"><span data-stu-id="ba7f9-136">Role</span></span>        | <span data-ttu-id="ba7f9-137">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="ba7f9-137">Org Unit</span></span>    |<span data-ttu-id="ba7f9-138">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ba7f9-138">Unit</span></span>      |<span data-ttu-id="ba7f9-139">Cena</span><span class="sxs-lookup"><span data-stu-id="ba7f9-139">Price</span></span>      |<span data-ttu-id="ba7f9-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="ba7f9-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ba7f9-141">Programer</span><span class="sxs-lookup"><span data-stu-id="ba7f9-141">Developer</span></span>   | <span data-ttu-id="ba7f9-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ba7f9-142">Contoso US</span></span>  |<span data-ttu-id="ba7f9-143">Hour</span><span class="sxs-lookup"><span data-stu-id="ba7f9-143">Hour</span></span> | <span data-ttu-id="ba7f9-144">200</span><span class="sxs-lookup"><span data-stu-id="ba7f9-144">200</span></span>|<span data-ttu-id="ba7f9-145">USD</span><span class="sxs-lookup"><span data-stu-id="ba7f9-145">USD</span></span>     |
| <span data-ttu-id="ba7f9-146">Programer</span><span class="sxs-lookup"><span data-stu-id="ba7f9-146">Developer</span></span>   | <span data-ttu-id="ba7f9-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="ba7f9-147">Contoso India</span></span> |<span data-ttu-id="ba7f9-148">Hour</span><span class="sxs-lookup"><span data-stu-id="ba7f9-148">Hour</span></span>|   <span data-ttu-id="ba7f9-149">112</span><span class="sxs-lookup"><span data-stu-id="ba7f9-149">112</span></span>|<span data-ttu-id="ba7f9-150">USD</span><span class="sxs-lookup"><span data-stu-id="ba7f9-150">USD</span></span>     |


<span data-ttu-id="ba7f9-151">**Primeri stopa troškova**</span><span class="sxs-lookup"><span data-stu-id="ba7f9-151">**Sample cost rates**</span></span>

| <span data-ttu-id="ba7f9-152">Grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="ba7f9-152">Salary Band</span></span>     | <span data-ttu-id="ba7f9-153">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="ba7f9-153">Org Unit</span></span>    |<span data-ttu-id="ba7f9-154">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ba7f9-154">Unit</span></span>      |<span data-ttu-id="ba7f9-155">Cena</span><span class="sxs-lookup"><span data-stu-id="ba7f9-155">Price</span></span>      |<span data-ttu-id="ba7f9-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="ba7f9-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="ba7f9-157">Moje preduzeće_Prva grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="ba7f9-157">My company_Band1</span></span> | <span data-ttu-id="ba7f9-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="ba7f9-158">Contoso US</span></span>  |<span data-ttu-id="ba7f9-159">Hour</span><span class="sxs-lookup"><span data-stu-id="ba7f9-159">Hour</span></span> | <span data-ttu-id="ba7f9-160">145</span><span class="sxs-lookup"><span data-stu-id="ba7f9-160">145</span></span>|<span data-ttu-id="ba7f9-161">USD</span><span class="sxs-lookup"><span data-stu-id="ba7f9-161">USD</span></span>     |
| <span data-ttu-id="ba7f9-162">Moje preduzeće_druga grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="ba7f9-162">My company_Band2</span></span> | <span data-ttu-id="ba7f9-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="ba7f9-163">Contoso India</span></span> |<span data-ttu-id="ba7f9-164">Hour</span><span class="sxs-lookup"><span data-stu-id="ba7f9-164">Hour</span></span>|   <span data-ttu-id="ba7f9-165">67</span><span class="sxs-lookup"><span data-stu-id="ba7f9-165">67</span></span>|<span data-ttu-id="ba7f9-166">USD</span><span class="sxs-lookup"><span data-stu-id="ba7f9-166">USD</span></span>     |
