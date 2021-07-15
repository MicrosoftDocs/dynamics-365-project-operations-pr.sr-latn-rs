---
title: Pregled ukupne iskorišćenosti resursa
description: Ova tema pruža informacije o prikazu ukupne iskorišćenosti resursa u usluzi Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367953"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="44f9b-103">Pregled ukupne iskorišćenosti resursa</span><span class="sxs-lookup"><span data-stu-id="44f9b-103">Resource utilization overview</span></span>

<span data-ttu-id="44f9b-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="44f9b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44f9b-105">Resursi mogu imati ciljanu naplativu ukupnu iskorišćenost.</span><span class="sxs-lookup"><span data-stu-id="44f9b-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="44f9b-106">Ukupna iskorišćenost se definiše kao atribut podrazumevane uloge resursa ili je podešena u zapisu pojedinačnog resursa koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="44f9b-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="44f9b-107">Izračunavanje ukupne iskorišćenosti temelji se na stvarnim satima koje su resursi prijavili korišćenjem odobrenih stavki vremena.</span><span class="sxs-lookup"><span data-stu-id="44f9b-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="44f9b-108">Sledeće formule se koriste za izračunavanje ukupne iskorišćenosti:</span><span class="sxs-lookup"><span data-stu-id="44f9b-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="44f9b-109">Naplativa ukupna iskorišćenost = naplativi stvarni sati ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="44f9b-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="44f9b-110">Nenaplativa ukupna iskorišćenost = Stvarno vreme sa ID-om vrste naplate = Nenaplativo, dopunsko ili nedostupno ÷ Kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="44f9b-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="44f9b-111">Interno = Stvarno vreme bez prodajnog ugovora ÷ Kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="44f9b-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="44f9b-112">Kapacitet resursa = Radno vreme resursa – Van kancelarije – Neradni dani</span><span class="sxs-lookup"><span data-stu-id="44f9b-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="44f9b-113">Možete pronaći prikaz **Ukupna iskorišćenost resursa** u oknu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="44f9b-114">Svaka ćelija u mreži predstavlja procenat naplative ukupne iskorišćenosti resursa u nekom periodu, kao što je dan, nedelja ili mesec.</span><span class="sxs-lookup"><span data-stu-id="44f9b-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="44f9b-115">Sledeće formule se koriste za bojenje ćelija:</span><span class="sxs-lookup"><span data-stu-id="44f9b-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="44f9b-116">**Zelena**: Naplativa ukupna iskorišćenost >= Ciljna ukupna iskorišćenost resursa</span><span class="sxs-lookup"><span data-stu-id="44f9b-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="44f9b-117">**Žuta**: Ciljna ukupna iskorišćenost – 20 <= Naplativa ukupna iskorišćenost < Ciljna ukupna iskorišćenost</span><span class="sxs-lookup"><span data-stu-id="44f9b-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="44f9b-118">**Crvena**: Naplativa ukupna iskorišćenost < Ciljna ukupna iskorišćenost – 20</span><span class="sxs-lookup"><span data-stu-id="44f9b-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="44f9b-119">Zbog toga što je prikaz **Ukupna iskorišćenost resursa** zasnovana na tabeli rasporeda, za filtriranje rezultata možete koristiti mogućnosti filtriranja tabele rasporeda.</span><span class="sxs-lookup"><span data-stu-id="44f9b-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="44f9b-120">Mreža zahteva da podesite ciljnu ukupnu iskorišćenost za ulogu ili pojedinačni resurs.</span><span class="sxs-lookup"><span data-stu-id="44f9b-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="44f9b-121">Da biste to podesili, idite na stavku **Resursi** > **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="44f9b-122">Uz to, svakom resursu koji se može rezervisati mora se dodeliti podrazumevana uloga.</span><span class="sxs-lookup"><span data-stu-id="44f9b-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="44f9b-123">Idite na **Resursi** > **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="44f9b-124">Na kartici **Project Service** potvrdite da je definisana uloga resursa i da je polje **Da li je podrazumevano** za tu ulogu podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="44f9b-125">Možete dodati dodatne uloge za koje važi **Da li je podrazumevano** = **Ne**.</span><span class="sxs-lookup"><span data-stu-id="44f9b-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="44f9b-126">Uloga gde se **Da li je podrazumevano** = **Da** koristi za procenu ukupne iskorišćenosti resursa u odnosu na ciljnu iskorišćenost za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="44f9b-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="44f9b-127">Na kartici **Project Service** možete podesiti i pojedinačnu ciljnu ukupnu iskorišćenost za resurs.</span><span class="sxs-lookup"><span data-stu-id="44f9b-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="44f9b-128">Kalkulacija ukupne iskorišćenosti zatim koristi tu ciljnu ukupnu iskorišćenost za procenu cilja resursa umesto cilja podrazumevane uloge resursa.</span><span class="sxs-lookup"><span data-stu-id="44f9b-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="44f9b-129">Ukupna iskorišćenost se prikazuje za resurs samo ako je taj resurs odobrio naplativo vreme tokom perioda koji je prikazan na mreži.</span><span class="sxs-lookup"><span data-stu-id="44f9b-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]