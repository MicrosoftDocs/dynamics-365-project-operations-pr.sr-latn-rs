---
title: Pregled dimenzija za određivanje cena
description: Ova tema pruža informacije o dimenzija za određivanje cena u usluzi Dynamics 365 Project Operations.
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083687"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="20971-103">Pregled dimenzija za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="20971-103">Pricing dimensions overview</span></span>

<span data-ttu-id="20971-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="20971-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="20971-105">Dimenzije koje se koriste u ljudskim resursima za podešavanje cena i troškova spadaju u dve kategorije:</span><span class="sxs-lookup"><span data-stu-id="20971-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="20971-106">Ljudi</span><span class="sxs-lookup"><span data-stu-id="20971-106">People</span></span>
- <span data-ttu-id="20971-107">Planirani rad</span><span class="sxs-lookup"><span data-stu-id="20971-107">Planned work</span></span>

<span data-ttu-id="20971-108">Zbog toga postoje dve vrste vrednosti dimenzija za određivanje cena koje su dostupne:</span><span class="sxs-lookup"><span data-stu-id="20971-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="20971-109">**Skupovi opcija** : Dimenzije koje predstavljaju fiksna nabrajanja za skup vrednosti.</span><span class="sxs-lookup"><span data-stu-id="20971-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="20971-110">**Vrednosti zasnovane na entitetima** : Dimenzije koje mogu biti različit skup vrednosti.</span><span class="sxs-lookup"><span data-stu-id="20971-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="20971-111">Dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="20971-111">Pricing dimensions</span></span>

<span data-ttu-id="20971-112">Dynamics 365 Project Operations se isporučuje sa podrazumevanim skupom dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="20971-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="20971-113">Ove dimenzije za određivanje cena možete da ih vidite tako što ćete otići na **Project Operations** > **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="20971-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="20971-114">U zapisu parametra, na kartici **Dimenzije za određivanje cena zasnovane na iznosima** proverite da li uloga **msdyn_resourcecategory** i organizaciona jedinica resursa **msdyn_organizationalunit** imaju polja **Primenljivo na prodaju** i **Primenljivo na troškove** podešena na **Da**.</span><span class="sxs-lookup"><span data-stu-id="20971-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="20971-115">Kada su ova polja omogućena, možete da podesite cenu i trošak za svaku kombinaciju uloge i organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="20971-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="20971-116">Ako je potrebno da odredite cenu ili troškove resursa pomoću dodatnih atributa, možete da kreirate prilagođena polja, entitete i dimenzije.</span><span class="sxs-lookup"><span data-stu-id="20971-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="20971-117">Određivanje cene vremena ljudskog resursa</span><span class="sxs-lookup"><span data-stu-id="20971-117">Pricing human resource time</span></span>
<span data-ttu-id="20971-118">Kako organizacija određuje cenu vremena ljudskog resursa je često značajno strateško pitanje koje direktno utiče na profitabilnost organizacije.</span><span class="sxs-lookup"><span data-stu-id="20971-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="20971-119">Sarađujte sa finansijskim timovima i budite mudri kada vaša organizacija bude spremna da utvrdi kako želi da podesi stope naplate i troškova za vreme ljudskog resursa.</span><span class="sxs-lookup"><span data-stu-id="20971-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="20971-120">Druga pitanja koja se tiču formiranja cena podrazumevaju da li ponovo da koristite polja ili entitete koji trenutno nisu dimenzije za određivanje cena, ali se primenjuju kao dimenzija za određivanje cena u vašoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="20971-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="20971-121">Polja kao što su **Kategorija transakcije** ( **msdyn_transactioncategory** ) i **Resurs koji može da se rezerviše** ( **bookableresource** ) su primeri mogućih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="20971-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="20971-122">Razmotrite i da li vaša dimenzija za određivanje cena treba da bude tabela ili skup opcija.</span><span class="sxs-lookup"><span data-stu-id="20971-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="20971-123">Ako predviđate promene vrednosti dimenzije koje će premašiti 10 ili 12, a potrebni su vam dodatni atributi za ove vrednosti, možete da kreirate entitet, a ne skup opcija.</span><span class="sxs-lookup"><span data-stu-id="20971-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="20971-124">Održavanje skupa opcija, kao što je dodavanje ili uklanjanje vrednosti, zahteva administratora ili programera, dok većina korisnika može da dodaje nove redove u tabelu.</span><span class="sxs-lookup"><span data-stu-id="20971-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="20971-125">Sledeći primer prikazuje kursne stope koje su podešene na osnovu uloge i organizacione jedinice resursa kome pripada resurs.</span><span class="sxs-lookup"><span data-stu-id="20971-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="20971-126">Stope troškova se obično zasnivaju na grupi ličnih dohodaka zaposlenih i organizacionoj jedinici kojoj pripadaju.</span><span class="sxs-lookup"><span data-stu-id="20971-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="20971-127">U ovom primeru, tabele sa stopama naplate i stopama troškova će izgledati ovako:</span><span class="sxs-lookup"><span data-stu-id="20971-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="20971-128">**Primeri stopa naplate**</span><span class="sxs-lookup"><span data-stu-id="20971-128">**Sample bill rates**</span></span>

| <span data-ttu-id="20971-129">Uloga</span><span class="sxs-lookup"><span data-stu-id="20971-129">Role</span></span>        | <span data-ttu-id="20971-130">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="20971-130">Org Unit</span></span>    |<span data-ttu-id="20971-131">Jedinica</span><span class="sxs-lookup"><span data-stu-id="20971-131">Unit</span></span>      |<span data-ttu-id="20971-132">Cena</span><span class="sxs-lookup"><span data-stu-id="20971-132">Price</span></span>      |<span data-ttu-id="20971-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="20971-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="20971-134">Programer</span><span class="sxs-lookup"><span data-stu-id="20971-134">Developer</span></span>   | <span data-ttu-id="20971-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="20971-135">Contoso US</span></span>  |<span data-ttu-id="20971-136">Hour</span><span class="sxs-lookup"><span data-stu-id="20971-136">Hour</span></span> | <span data-ttu-id="20971-137">200</span><span class="sxs-lookup"><span data-stu-id="20971-137">200</span></span>|<span data-ttu-id="20971-138">USD</span><span class="sxs-lookup"><span data-stu-id="20971-138">USD</span></span>     |
| <span data-ttu-id="20971-139">Programer</span><span class="sxs-lookup"><span data-stu-id="20971-139">Developer</span></span>   | <span data-ttu-id="20971-140">Contoso India</span><span class="sxs-lookup"><span data-stu-id="20971-140">Contoso India</span></span> |<span data-ttu-id="20971-141">Hour</span><span class="sxs-lookup"><span data-stu-id="20971-141">Hour</span></span>|   <span data-ttu-id="20971-142">112</span><span class="sxs-lookup"><span data-stu-id="20971-142">112</span></span>|<span data-ttu-id="20971-143">USD</span><span class="sxs-lookup"><span data-stu-id="20971-143">USD</span></span>     |


<span data-ttu-id="20971-144">**Primeri stopa troškova**</span><span class="sxs-lookup"><span data-stu-id="20971-144">**Sample cost rates**</span></span>

| <span data-ttu-id="20971-145">Grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="20971-145">Salary Band</span></span>     | <span data-ttu-id="20971-146">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="20971-146">Org Unit</span></span>    |<span data-ttu-id="20971-147">Jedinica</span><span class="sxs-lookup"><span data-stu-id="20971-147">Unit</span></span>      |<span data-ttu-id="20971-148">Cena</span><span class="sxs-lookup"><span data-stu-id="20971-148">Price</span></span>      |<span data-ttu-id="20971-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="20971-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="20971-150">Moje preduzeće_Prva grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="20971-150">My company_Band1</span></span> | <span data-ttu-id="20971-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="20971-151">Contoso US</span></span>  |<span data-ttu-id="20971-152">Hour</span><span class="sxs-lookup"><span data-stu-id="20971-152">Hour</span></span> | <span data-ttu-id="20971-153">145</span><span class="sxs-lookup"><span data-stu-id="20971-153">145</span></span>|<span data-ttu-id="20971-154">USD</span><span class="sxs-lookup"><span data-stu-id="20971-154">USD</span></span>     |
| <span data-ttu-id="20971-155">Moje preduzeće_druga grupa ličnih dohodaka</span><span class="sxs-lookup"><span data-stu-id="20971-155">My company_Band2</span></span> | <span data-ttu-id="20971-156">Contoso India</span><span class="sxs-lookup"><span data-stu-id="20971-156">Contoso India</span></span> |<span data-ttu-id="20971-157">Hour</span><span class="sxs-lookup"><span data-stu-id="20971-157">Hour</span></span>|   <span data-ttu-id="20971-158">67</span><span class="sxs-lookup"><span data-stu-id="20971-158">67</span></span>|<span data-ttu-id="20971-159">USD</span><span class="sxs-lookup"><span data-stu-id="20971-159">USD</span></span>     |
