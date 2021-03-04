---
title: Predlaganje resursa za projekte
description: Ova tema pruža informacije o predlaganju resursa za projekte.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147535"
---
# <a name="propose-project-resources"></a><span data-ttu-id="3bf6c-103">Predlaganje resursa za projekte</span><span class="sxs-lookup"><span data-stu-id="3bf6c-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3bf6c-104">Menadžeri resursa mogu da predlože resurs menadžeru projekata korišćenjem zahteva za resurs.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="3bf6c-105">Iz mreže zahteva ili samog zahteva izaberite **Pronađi resurse**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="3bf6c-106">Na stranici **Pomoćnik za zakazivanje** izaberite resurs, a zatim u oknu **Kreiranje rezervacije resursa**, u polju **Status rezervacije**, izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Predloženi resurs je izabran](media/Resource-Management-image62.png)

<span data-ttu-id="3bf6c-108">Dolazi do sledećih izmena statusa:</span><span class="sxs-lookup"><span data-stu-id="3bf6c-108">The following status updates occur:</span></span>

- <span data-ttu-id="3bf6c-109">Na stranici **Pomoćnik za zakazivanje** indikatori statusa se ažuriraju kako bi ukazali da je rezervacija predložena, a da resurs nije fiksno rezervisan.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indikatori statusa za predloženu rezervaciju na stranici Pomoćnik za zakazivanje](media/Resource-Management-image63.png)

- <span data-ttu-id="3bf6c-111">U zahtevu za resurs se status menja u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Status zahteva za resurs je promenjen u Zahteva pregled](media/Resource-Management-image64.png)

- <span data-ttu-id="3bf6c-113">Na kartici **Tim** u okviru projekta, vrednost generičkog člana tima **Status zahteva** se menja u **Zahteva pregled**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Status zahteva za generičkog člana tima je promenjen u Zahteva pregled na kartici Tim](media/Resource-Management-image48.png)

<span data-ttu-id="3bf6c-115">Menadžer projekta može predlog prihvatiti ili odbaciti.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="3bf6c-116">Kada menadžeri resursa obrađuju zahteve za resurse, mogu koristiti bilo koji od sledećih pristupa:</span><span class="sxs-lookup"><span data-stu-id="3bf6c-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="3bf6c-117">Mogu da predlažu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za ispunjavanje zahtevanih sati.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="3bf6c-118">Predloženi sati se zatim dele na više resursa koji mogu da zadovolje zahtevane sate.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="3bf6c-119">U ovom scenariju, sati se ne mogu preklapati.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="3bf6c-120">Mogu da predlažu manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="3bf6c-121">U ovom scenariju, kapacitet predloženog resursa je manji od zahtevanih sati koje je naveo podnosilac zahteva.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="3bf6c-122">Stoga, kada podnosilac zahteva prihvati predložene resurse, kreira se potreba za neispunjenim resursom da bi se evidentirala preostala potražnja.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="3bf6c-123">Mogu da rezervišu više resursa da bi zadovoljili potražnju ako nije dostupan nijedan resurs za obavljanje posla.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="3bf6c-124">Mogu da rezervišu manje resursa nego što je potrebno.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-124">Book fewer resources than are required.</span></span> <span data-ttu-id="3bf6c-125">U ovom scenariju, broj rezervisanih sati je manji od broja zahtevanih sati.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="3bf6c-126">Sistem vas upućuje da predložite resurse umesto rezervacija, tako da podnosilac zahteva može da proveri i prati preostalu potražnju.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="3bf6c-127">Naplativa ukupna iskorišćenost</span><span class="sxs-lookup"><span data-stu-id="3bf6c-127">Billable utilization</span></span>

<span data-ttu-id="3bf6c-128">Resursi mogu imati ciljanu naplativu ukupnu iskorišćenost.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="3bf6c-129">Ona je definisana kao atribut podrazumevane uloge resursa ili je podešena u zapisu pojedinačnog resursa koji se može rezervisati.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="3bf6c-130">Izračunavanje ukupne iskorišćenosti temelji se na stvarnim satima koje su resursi prijavili korišćenjem odobrenih stavki vremena.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="3bf6c-131">Sledeće formule se koriste za izračunavanje ukupne iskorišćenosti:</span><span class="sxs-lookup"><span data-stu-id="3bf6c-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="3bf6c-132">Naplativa ukupna iskorišćenost = naplativi stvarni sati ÷ kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="3bf6c-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="3bf6c-133">Nenaplativa ukupna iskorišćenost = Stvarno vreme sa ID-om vrste naplate = Nenaplativo, dopunsko ili nedostupno ÷ Kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="3bf6c-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="3bf6c-134">Interno = Stvarno vreme bez prodajnog ugovora ÷ Kapacitet resursa</span><span class="sxs-lookup"><span data-stu-id="3bf6c-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="3bf6c-135">Kapacitet resursa = Radno vreme resursa – Van kancelarije – Neradni dani</span><span class="sxs-lookup"><span data-stu-id="3bf6c-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="3bf6c-136">Možete pronaći prikaz **Ukupna iskorišćenost resursa** u oknu **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Prikaz ukupne iskorišćenosti resursa](media/Resource-Management-image65.png)

<span data-ttu-id="3bf6c-138">Svaka ćelija u mreži predstavlja procenat naplative ukupne iskorišćenosti resursa u nekom periodu, kao što je dan, nedelja ili mesec.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="3bf6c-139">Sledeće formule se koriste za bojenje ćelija:</span><span class="sxs-lookup"><span data-stu-id="3bf6c-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="3bf6c-140">**Zelena:** Naplativa ukupna iskorišćenost \>= ciljna ukupna iskorišćenost resursa</span><span class="sxs-lookup"><span data-stu-id="3bf6c-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="3bf6c-141">**Žuta:** ciljna ukupna iskorišćenost – 20 \<= naplativa ukupna iskorišćenost \< ciljna ukupna iskorišćenost</span><span class="sxs-lookup"><span data-stu-id="3bf6c-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="3bf6c-142">**Crvena:** naplativa ukupna iskorišćenost \< ciljna ukupna iskorišćenost – 20</span><span class="sxs-lookup"><span data-stu-id="3bf6c-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="3bf6c-143">Zbog toga što je prikaz **Ukupna iskorišćenost resursa** zasnovana na tabeli rasporeda, za filtriranje rezultata možete koristiti mogućnosti filtriranja tabele rasporeda.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="3bf6c-144">Mreža zahteva da podesite ciljnu ukupnu iskorišćenost za ulogu ili pojedinačni resurs.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="3bf6c-145">Da biste to podesili, idite na stavku **Resursi** \> **Uloge resursa**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="3bf6c-146">Uz to, svakom resursu koji se može rezervisati mora se dodeliti podrazumevana uloga.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="3bf6c-147">Idite na **Resursi** \> **Resursi**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="3bf6c-148">Na kartici **Project Service** potvrdite da je definisana uloga resursa i da je polje **Je podrazumevano** za tu ulogu podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="3bf6c-149">Ako **Je podrazumevano = Ne**, možete dodati dodatne uloge.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="3bf6c-150">Uloga gde **Je podrazumevano = Da** koristi se za procenu ukupne iskorišćenosti resursa u odnosu na ciljnu iskorišćenost za tu ulogu.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Podrazumevani skup uloga](media/Resource-Management-image67.png)

<span data-ttu-id="3bf6c-152">Na kartici **Project Service** možete podesiti i pojedinačnu ciljnu ukupnu iskorišćenost za resurs.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="3bf6c-153">Kalkulacija ukupne iskorišćenosti zatim koristi tu ciljnu ukupnu iskorišćenost za procenu cilja resursa umesto cilja podrazumevane uloge resursa.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="3bf6c-154">Ukupna iskorišćenost je prikazana za resurs samo ako je taj resurs odobrio naplativo vreme tokom perioda koji je prikazan na mreži.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="3bf6c-155">Dostupnosti resursa</span><span class="sxs-lookup"><span data-stu-id="3bf6c-155">Resource availability</span></span>

<span data-ttu-id="3bf6c-156">Od presudnog je značaja da menadžeri resursa mogu da pregledaju dostupnost resursa i ažuriraju rezervacije.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="3bf6c-157">U nekim slučajevima, ne postoji formalna potražnja (zahtev za resurs), ali menadžer resursa mora da odgovori na neplaniranu potražnju koja dolazi preko kanala poput e-pošte, telefonskog poziva ili trenutne poruke.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="3bf6c-158">Menadžeri resursa koriste tablu rasporeda za ažuriranje resursa i rezervacija.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="3bf6c-159">Radno vreme resursa koristi se kao osnova za izračunavanje dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="3bf6c-160">Rezervacije resursa troše kapacitet resursa.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-160">Resource bookings consume the capacity of the resources.</span></span>

![Tabela rasporeda](media/Resource-Management-image68.png)

<span data-ttu-id="3bf6c-162">Tabela rasporeda koristi boje i senčenja da bi prikazala rezervacije, dostupnost i prebukiranost, kao i status rezervacija.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="3bf6c-163">Postavka u podešavanjima tabele rasporeda omogućava vam da prikažete legendu.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="3bf6c-164">Ako se strelica usmerena udesno pojavi pored pojedinačnog resursa koji se može rezervisati u tabeli rasporeda, resurs se može proširiti i pokazati detalje posla za koji je resurs rezervisan.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Resurs koji može da se rezerviše je proširen u tabeli rasporeda](media/Resource-Management-image69.png)

<span data-ttu-id="3bf6c-166">Pošto Dynamics 365 Project Service Automation koristi Universal Resource Scheduling mehanizam, ako ste instalirali i Dynamics 365 Field Service, možete pregledati detalje o rezervacijama resursa za projekte, radnim nalozima i bilo kojim drugim entitetima za koje ste proširili zakazivanje.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Detalji o rezervacijama resursa za projekte i radnim nalozima](media/Resource-Management-image70.png)

<span data-ttu-id="3bf6c-168">Da biste videli više detalja o pojedinačnom resursu, kliknite desnim tasterom miša na resurs da biste otvorili karticu resursa.</span><span class="sxs-lookup"><span data-stu-id="3bf6c-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Kartica resursa](media/Resource-Management-image71.png)
