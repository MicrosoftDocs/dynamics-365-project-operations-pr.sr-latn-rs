---
title: Prikaz naplative ukupne iskorišćenosti resursa
description: Ova tema pruža informacije o prikazu ukupne iskorišćenosti resursa.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1c123854209b3cb5c310e3bbcb242c9219279a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992851"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="7a85d-103">Prikaz naplative ukupne iskorišćenosti resursa</span><span class="sxs-lookup"><span data-stu-id="7a85d-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="7a85d-104">**Prikaz ukupne iskorišćenosti** na stranici **Ukupna iskorišćenost resursa u aplikaciji Project Service** prikazuje naplativu ukupnu iskorišćenost svakog resursa koji može da se rezerviše.</span><span class="sxs-lookup"><span data-stu-id="7a85d-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="7a85d-105">Pošto je prikaz zasnovan na tabeli rasporeda, pronaćićete dosta istih funkcija.</span><span class="sxs-lookup"><span data-stu-id="7a85d-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Snimak ekrana prikaza ukupne iskorišćenosti](media/FAQ-utilization-1.png)
 

<span data-ttu-id="7a85d-107">Izračunavanje naplative ukupne iskorišćenosti funkcioniše na sledeći način:</span><span class="sxs-lookup"><span data-stu-id="7a85d-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="7a85d-108">Naplativa ukupna iskorišćenost = (naplativi stvarni sati) / (kapacitet resursa).</span><span class="sxs-lookup"><span data-stu-id="7a85d-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="7a85d-109">Ćelije predstavljaju izračunatu naplativu ukupnu iskorišćenost za izabrani period (dani, sedmice ili meseci).</span><span class="sxs-lookup"><span data-stu-id="7a85d-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="7a85d-110">Boje u svakoj ćeliji prikazuju naplativu ukupnu iskorišćenost za resurs u poređenju sa njegovom ciljnom naplativom ukupnom iskorišćenošću.</span><span class="sxs-lookup"><span data-stu-id="7a85d-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="7a85d-111">Ciljna ukupna iskorišćenost može biti podešena za podrazumevanu ulogu resursa ili za samog pojedinačnog resursa.</span><span class="sxs-lookup"><span data-stu-id="7a85d-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="7a85d-112">Izračunavanje prvo gleda pojedinca za cilj, a zatim podrazumevanu ulogu resursa.</span><span class="sxs-lookup"><span data-stu-id="7a85d-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="7a85d-113">Podešavanje cilja za resurs</span><span class="sxs-lookup"><span data-stu-id="7a85d-113">Set target on a resource</span></span>

1. <span data-ttu-id="7a85d-114">Idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7a85d-115">Izaberite resurs da biste otvorili zapis.</span><span class="sxs-lookup"><span data-stu-id="7a85d-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="7a85d-116">Na kartici **Project Service** možete podesiti ciljnu ukupnu iskorišćenost resursa.</span><span class="sxs-lookup"><span data-stu-id="7a85d-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Snimak ekrana korišćenja kartice Project Service za podešavanje ciljne ukupne iskorišćenosti](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="7a85d-118">Podešavanje ciljne ukupne iskorišćenosti za ulogu</span><span class="sxs-lookup"><span data-stu-id="7a85d-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="7a85d-119">Idite na **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="7a85d-120">Izaberite ulogu i otvorite zapis.</span><span class="sxs-lookup"><span data-stu-id="7a85d-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="7a85d-121">Podesite ciljnu ukupnu iskorišćenost za ulogu.</span><span class="sxs-lookup"><span data-stu-id="7a85d-121">Set the target utilization for the role.</span></span>

> ![Snimak ekrana korišćenja uloga resursa za podešavanje ciljne ukupne iskorišćenosti](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="7a85d-123">Izračunavanje naplative ukupne iskorišćenosti resursa</span><span class="sxs-lookup"><span data-stu-id="7a85d-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="7a85d-124">Da biste izračunali naplativu ukupnu iskorišćenost za resurs, potrebno je da ispunite neke preduslove.</span><span class="sxs-lookup"><span data-stu-id="7a85d-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="7a85d-125">Podešavanje podrazumevane uloge za pojedinačni resurs</span><span class="sxs-lookup"><span data-stu-id="7a85d-125">Set default role for individual resource</span></span>

<span data-ttu-id="7a85d-126">Prvo, ciljna ukupna iskorišćenost mora biti podešena za ulogu pojedinačnog resursa ili za ulogu resursa.</span><span class="sxs-lookup"><span data-stu-id="7a85d-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="7a85d-127">Ako koristite uloge resursa za ciljeve, svaki pojedinačni resurs mora da ima podrazumevanu ulogu.</span><span class="sxs-lookup"><span data-stu-id="7a85d-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="7a85d-128">Da biste to podesili, idite na stavku **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7a85d-129">Izaberite resurs, otvorite zapis, a zatim izaberite karticu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="7a85d-130">U mreži **Uloga resursa**, uverite se da postoji jedna uloga za resurs, a **Je podrazumevano** podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="7a85d-131">Promena tipa naplate za ulogu resursa</span><span class="sxs-lookup"><span data-stu-id="7a85d-131">Change billing type for resource role</span></span>

<span data-ttu-id="7a85d-132">Uloge resursa moraju biti podešene tako da imaju tip naplate **Naplativ**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="7a85d-133">Idite na **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="7a85d-134">Otvorite zapis koji želite da ažurirate, a zatim podesite podrazumevani tip naplate na **Naplativo**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="7a85d-135">Podešavanje radnog vremena za ulogu resursa</span><span class="sxs-lookup"><span data-stu-id="7a85d-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="7a85d-136">Resurs mora da ima radno vreme za izračunavanje kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="7a85d-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="7a85d-137">Idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="7a85d-138">Izaberite resurs da biste otvorili zapis, a zatim izaberite **Prikaži radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="7a85d-139">Možete masovno da ispravite listu resursa primenom **predloška za radno vreme** sa prikaza **liste resursa**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="7a85d-140">Rešavanje problema sa naplativim stvarnim satima</span><span class="sxs-lookup"><span data-stu-id="7a85d-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="7a85d-141">Izvor naplativih stvarnih sati je entitet **Stvarne vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="7a85d-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="7a85d-142">Stvarne vrednosti čiji je tip naplate **Naplativo** su obuhvaćene u izračunavanje i zato morate da imate projekte u kojima su stvarne vrednosti naplative.</span><span class="sxs-lookup"><span data-stu-id="7a85d-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="7a85d-143">Ako ne vidite naplativu ukupnu iskorišćenost, evo nekih stvari koje možete da proverite:</span><span class="sxs-lookup"><span data-stu-id="7a85d-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="7a85d-144">Resurs ima radne časove koji su definisani za kapacitet.</span><span class="sxs-lookup"><span data-stu-id="7a85d-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="7a85d-145">Resurs ima pojedinačno definisani cilj ukupne iskorišćenosti ili mu je dodeljena podrazumevana uloga.</span><span class="sxs-lookup"><span data-stu-id="7a85d-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="7a85d-146">Za ulogu je definisan cilj ukupne iskorišćenosti.</span><span class="sxs-lookup"><span data-stu-id="7a85d-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="7a85d-147">Stvarne vrednosti imaju tip naplate **Naplativo** za period za koji očekujete izračunavanje ukupne iskorišćenosti.</span><span class="sxs-lookup"><span data-stu-id="7a85d-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="7a85d-148">Proverite sledeće stvari ako vidite stvarne vrednosti čiji tipovi naplate nisu naplativi:</span><span class="sxs-lookup"><span data-stu-id="7a85d-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="7a85d-149">Uloga korišćena za stvarne troškove ima podrazumevani tip naplate koji se razlikuje od tipa „Naplativo“.</span><span class="sxs-lookup"><span data-stu-id="7a85d-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="7a85d-150">Uloge za predmet ugovora za projekat koji podržava projekat je podešena na nenaplativo.</span><span class="sxs-lookup"><span data-stu-id="7a85d-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="7a85d-151">Projekat nema povezani predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="7a85d-151">The project does not have an associated contract line.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]