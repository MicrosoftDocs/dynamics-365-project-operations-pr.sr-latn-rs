---
title: Matična stranica za dimenzije određivanja cena i obračuna troškova
description: Ova tema obezbeđuje pregled dimenzija za određivanje cena.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755147"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="0a883-103">Matična stranica za dimenzije određivanja cena i obračuna troškova</span><span class="sxs-lookup"><span data-stu-id="0a883-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="0a883-104">Dimenzije koje se koriste u ljudskim resursima za podešavanje cena i troškova spadaju u dve kategorije:</span><span class="sxs-lookup"><span data-stu-id="0a883-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="0a883-105">Ljudi</span><span class="sxs-lookup"><span data-stu-id="0a883-105">People</span></span>
- <span data-ttu-id="0a883-106">Planirani rad</span><span class="sxs-lookup"><span data-stu-id="0a883-106">Planned work</span></span>

<span data-ttu-id="0a883-107">Zbog toga postoje dve vrste vrednosti dimenzija za određivanje cena koje su dostupne u aplikaciji Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="0a883-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="0a883-108">**Skupovi opcija** - Dimenzije koje predstavljaju fiksna nabrajanja za skup vrednosti.</span><span class="sxs-lookup"><span data-stu-id="0a883-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="0a883-109">**Vrednosti zasnovane na entitetima** - Dimenzije koje mogu biti različit skup vrednosti.</span><span class="sxs-lookup"><span data-stu-id="0a883-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="0a883-110">Dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="0a883-110">Pricing dimensions</span></span>

<span data-ttu-id="0a883-111">PSA obavlja isporuku pomoću podrazumevanog skup dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="0a883-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="0a883-112">Možete da ih vidite tako što ćete otići na **Project Service** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="0a883-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="0a883-113">U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="0a883-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="0a883-114">Ovo će vam omogućiti podešavanje cene i troška za svaku kombinaciju uloge i organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="0a883-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Snimak ekrana Project Service parametara sa markiranom stavkom „Primenljivo na prodaju“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="0a883-116">Ako ste koristili unapred definisana polja uloge i organizacionih jedinica kao dimenzije za određivanje cena pre verzije 3 aplikacije PSA, neće biti nikakvih primetnih promena.</span><span class="sxs-lookup"><span data-stu-id="0a883-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="0a883-117">Možete da nastavite da koristite Project Service kao i obično.</span><span class="sxs-lookup"><span data-stu-id="0a883-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="0a883-118">Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije.</span><span class="sxs-lookup"><span data-stu-id="0a883-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="0a883-119">Da biste dobili više informacija, pogledajte sledeće teme, ali imajte na umu da morate da dovršite procedure po dolenavedenom redosledu:</span><span class="sxs-lookup"><span data-stu-id="0a883-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="0a883-120">Kreiranje prilagođenih polja i entiteta</span><span class="sxs-lookup"><span data-stu-id="0a883-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="0a883-121">Dodavanje prilagođenih polja u podešavanje cena i entitete transakcije</span><span class="sxs-lookup"><span data-stu-id="0a883-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="0a883-122">Podešavanje prilagođenih polja kao dimenzija za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="0a883-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="0a883-123">Ažuriranje atributa dodatnih komponenti tako da uključuju nove dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="0a883-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="0a883-124">Određivanje cene vremena ljudskog resursa</span><span class="sxs-lookup"><span data-stu-id="0a883-124">Pricing human resource time</span></span>
<span data-ttu-id="0a883-125">Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="0a883-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="0a883-126">Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.</span><span class="sxs-lookup"><span data-stu-id="0a883-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="0a883-127">Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="0a883-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="0a883-128">Polja kao što su **Kategorija transakcije** (**msdyn_transactioncategory**) i **Resurs koji može da se rezerviše** (**bookableresource**) su primeri mogućih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="0a883-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="0a883-129">Trebalo bi da razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija.</span><span class="sxs-lookup"><span data-stu-id="0a883-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="0a883-130">Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, možete da kreirate entitet, a ne skup opcija.</span><span class="sxs-lookup"><span data-stu-id="0a883-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="0a883-131">Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina korisnika može da dodaje nove redove u tabelu.</span><span class="sxs-lookup"><span data-stu-id="0a883-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="0a883-132">Sledeći primer prikazuje kursne stope koje su podešene na osnovu uloge i organizacione jedinice resursa kome pripada resurs.</span><span class="sxs-lookup"><span data-stu-id="0a883-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="0a883-133">Stope troškova se obično zasnivaju na grupi ličnih dohodaka zaposlenih i organizacionoj jedinici kojoj pripadaju.</span><span class="sxs-lookup"><span data-stu-id="0a883-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="0a883-134">U ovom primeru, tabele sa stopama naplate i stopama troškova će izgledati ovako:</span><span class="sxs-lookup"><span data-stu-id="0a883-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="0a883-135">**Primeri stopa naplate**</span><span class="sxs-lookup"><span data-stu-id="0a883-135">**Sample bill rates**</span></span>

| <span data-ttu-id="0a883-136">Uloga</span><span class="sxs-lookup"><span data-stu-id="0a883-136">Role</span></span>        | <span data-ttu-id="0a883-137">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="0a883-137">Org Unit</span></span>    |<span data-ttu-id="0a883-138">Jedinica</span><span class="sxs-lookup"><span data-stu-id="0a883-138">Unit</span></span>      |<span data-ttu-id="0a883-139">Cena</span><span class="sxs-lookup"><span data-stu-id="0a883-139">Price</span></span>      |<span data-ttu-id="0a883-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="0a883-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0a883-141">Programer</span><span class="sxs-lookup"><span data-stu-id="0a883-141">Developer</span></span>   | <span data-ttu-id="0a883-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0a883-142">Contoso US</span></span>  |<span data-ttu-id="0a883-143">Hour</span><span class="sxs-lookup"><span data-stu-id="0a883-143">Hour</span></span> | <span data-ttu-id="0a883-144">200</span><span class="sxs-lookup"><span data-stu-id="0a883-144">200</span></span>|<span data-ttu-id="0a883-145">USD</span><span class="sxs-lookup"><span data-stu-id="0a883-145">USD</span></span>     |
| <span data-ttu-id="0a883-146">Programer</span><span class="sxs-lookup"><span data-stu-id="0a883-146">Developer</span></span>   | <span data-ttu-id="0a883-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0a883-147">Contoso India</span></span> |<span data-ttu-id="0a883-148">Hour</span><span class="sxs-lookup"><span data-stu-id="0a883-148">Hour</span></span>|   <span data-ttu-id="0a883-149">112</span><span class="sxs-lookup"><span data-stu-id="0a883-149">112</span></span>|<span data-ttu-id="0a883-150">USD</span><span class="sxs-lookup"><span data-stu-id="0a883-150">USD</span></span>     |


<span data-ttu-id="0a883-151">**Primeri stopa troškova**</span><span class="sxs-lookup"><span data-stu-id="0a883-151">**Sample cost rates**</span></span>

| <span data-ttu-id="0a883-152">Grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="0a883-152">Salary Band</span></span>     | <span data-ttu-id="0a883-153">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="0a883-153">Org Unit</span></span>    |<span data-ttu-id="0a883-154">Jedinica</span><span class="sxs-lookup"><span data-stu-id="0a883-154">Unit</span></span>      |<span data-ttu-id="0a883-155">Cena</span><span class="sxs-lookup"><span data-stu-id="0a883-155">Price</span></span>      |<span data-ttu-id="0a883-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="0a883-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="0a883-157">Moje preduzeće_Prva grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="0a883-157">My company_Band1</span></span> | <span data-ttu-id="0a883-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="0a883-158">Contoso US</span></span>  |<span data-ttu-id="0a883-159">Hour</span><span class="sxs-lookup"><span data-stu-id="0a883-159">Hour</span></span> | <span data-ttu-id="0a883-160">145</span><span class="sxs-lookup"><span data-stu-id="0a883-160">145</span></span>|<span data-ttu-id="0a883-161">USD</span><span class="sxs-lookup"><span data-stu-id="0a883-161">USD</span></span>     |
| <span data-ttu-id="0a883-162">Moje preduzeće_druga grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="0a883-162">My company_Band2</span></span> | <span data-ttu-id="0a883-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="0a883-163">Contoso India</span></span> |<span data-ttu-id="0a883-164">Hour</span><span class="sxs-lookup"><span data-stu-id="0a883-164">Hour</span></span>|   <span data-ttu-id="0a883-165">67</span><span class="sxs-lookup"><span data-stu-id="0a883-165">67</span></span>|<span data-ttu-id="0a883-166">USD</span><span class="sxs-lookup"><span data-stu-id="0a883-166">USD</span></span>     |
