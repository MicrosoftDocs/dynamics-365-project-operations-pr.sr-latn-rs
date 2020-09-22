---
title: Grupe jedinica i jedinice
description: Ova tema pruža informacije o grupama jedinica i jedinicama.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: b5422be3-5bfc-4ee2-b19a-4eca68813ff2
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fc2dde2d9471f8585c190a65f3ad9b32de75af86
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755269"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="abbb3-103">Grupe jedinica i jedinice</span><span class="sxs-lookup"><span data-stu-id="abbb3-103">Unit groups and units</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="abbb3-104">Grupe jedinica i jedinice su osnovni entiteti u sistemu Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="abbb3-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="abbb3-105">Jedinica je jedinica mere, a više jedinica može biti grupisano u grupe jedinica.</span><span class="sxs-lookup"><span data-stu-id="abbb3-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="abbb3-106">Grupa jedinica se ponekad zove raspored jedinice u Dynamics 365 korisničkom sistemu.</span><span class="sxs-lookup"><span data-stu-id="abbb3-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="abbb3-107">Evo nekoliko primera jedinica i grupa jedinica:</span><span class="sxs-lookup"><span data-stu-id="abbb3-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="abbb3-108">**Grupa jedinica**: Razdaljina</span><span class="sxs-lookup"><span data-stu-id="abbb3-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="abbb3-109">**Jedinice**: Milja, kilometar itd.</span><span class="sxs-lookup"><span data-stu-id="abbb3-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="abbb3-110">**Grupa jedinica**: Vreme</span><span class="sxs-lookup"><span data-stu-id="abbb3-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="abbb3-111">**Jedinice**: Čas, dan, sedmica i tako dalje.</span><span class="sxs-lookup"><span data-stu-id="abbb3-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="abbb3-112">Kada podesite više jedinica u grupi jedinica, morate podesiti i faktor konverzije između njih tako što ćete označiti prvu jedinicu koju ste podesili kao podrazumevanu ili primarnu jedinicu za grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="abbb3-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="abbb3-113">Na primer, u grupi jedinica **Vreme**, ako podesite **Čas** kao prvu jedinicu, sistem određuje **Čas** kao podrazumevanu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="abbb3-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="abbb3-114">Ako je **Dan** sledeća jedinica koju podesite, morate podesiti faktor konverzije za jedinicu **Dan** na **Čas.**</span><span class="sxs-lookup"><span data-stu-id="abbb3-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="abbb3-115">Ako zatim dodate treću jedinicu **Sedmica**, morate da podesite faktor konverzije za jedinicu **Sedmica** u odnosu na **Dan** ili **Čas**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="abbb3-116">Sledeća slika prikazuje primer podešavanja jedinice **Dan**, pri čemu polje **Količina** prikazuje broj časova u danu, i **Sedmica**, gde polje **Količina** prikazuje broj dana u nedelji.</span><span class="sxs-lookup"><span data-stu-id="abbb3-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Grupa jedinica: stranica sa informacijama](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="abbb3-118">Korišćenje jedinica i grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-118">Using units and unit groups</span></span>

<span data-ttu-id="abbb3-119">Dynamics 365 Project Service Automation koristi jedinice i grupe jedinica za obradu procena i stavki za troškove i vreme.</span><span class="sxs-lookup"><span data-stu-id="abbb3-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="abbb3-120">Za troškove, svaka kategorija troška ima podrazumevanu grupu jedinica i jedinicu.</span><span class="sxs-lookup"><span data-stu-id="abbb3-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="abbb3-121">Ove vrednosti se unose kao podrazumevane vrednosti u stavkama cenovnika za kategorije troškova.</span><span class="sxs-lookup"><span data-stu-id="abbb3-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="abbb3-122">Na primer, imate kategoriju troška koja se zove **Kilometraža**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="abbb3-123">Ona ima grupu jedinica pod nazivom **Razdaljina** i podrazumevanu jedinicu koja se zove **Kilometar**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="abbb3-124">Ako podesite grupu jedinica **Rastojanje** tako da ima dve jedinice (**Milja** i **Kilometar**), možete podesiti dve cene za kategoriju **Kilometraža** za jedan cenovnik: cena po milji i ceni po kilometru.</span><span class="sxs-lookup"><span data-stu-id="abbb3-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="abbb3-125">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="abbb3-125">Expense category</span></span>  | <span data-ttu-id="abbb3-126">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-126">Unit group</span></span>  | <span data-ttu-id="abbb3-127">Jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-127">Unit</span></span>      | <span data-ttu-id="abbb3-128">Način određivanja cena</span><span class="sxs-lookup"><span data-stu-id="abbb3-128">Pricing method</span></span>  | <span data-ttu-id="abbb3-129">Cena po jedinici</span><span class="sxs-lookup"><span data-stu-id="abbb3-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="abbb3-130">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="abbb3-130">Mileage</span></span>           | <span data-ttu-id="abbb3-131">Udaljenost</span><span class="sxs-lookup"><span data-stu-id="abbb3-131">Distance</span></span>      | <span data-ttu-id="abbb3-132">Milja</span><span class="sxs-lookup"><span data-stu-id="abbb3-132">Mile</span></span>      | <span data-ttu-id="abbb3-133">Cena po jedinici</span><span class="sxs-lookup"><span data-stu-id="abbb3-133">Price per unit</span></span>    | <span data-ttu-id="abbb3-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="abbb3-134">10 USD</span></span>            |
| <span data-ttu-id="abbb3-135">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="abbb3-135">Mileage</span></span>           | <span data-ttu-id="abbb3-136">Udaljenost</span><span class="sxs-lookup"><span data-stu-id="abbb3-136">Distance</span></span>      | <span data-ttu-id="abbb3-137">Kilometar</span><span class="sxs-lookup"><span data-stu-id="abbb3-137">Kilometer</span></span> | <span data-ttu-id="abbb3-138">Cena po jedinici</span><span class="sxs-lookup"><span data-stu-id="abbb3-138">Price per unit</span></span>    |  <span data-ttu-id="abbb3-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="abbb3-139">6 USD</span></span>            |

<span data-ttu-id="abbb3-140">Kada unesete trošak za projekat, sistem određuje cenu kroz kombinaciju kategorije i jedinice po trošku.</span><span class="sxs-lookup"><span data-stu-id="abbb3-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="abbb3-141">Opis troška</span><span class="sxs-lookup"><span data-stu-id="abbb3-141">Expense description</span></span>        | <span data-ttu-id="abbb3-142">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="abbb3-142">Expense category</span></span>  | <span data-ttu-id="abbb3-143">Jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-143">Unit</span></span>  | <span data-ttu-id="abbb3-144">Količina</span><span class="sxs-lookup"><span data-stu-id="abbb3-144">Quantity</span></span>  | <span data-ttu-id="abbb3-145">Cena po jedinici</span><span class="sxs-lookup"><span data-stu-id="abbb3-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="abbb3-146">Vožnja do lokacije klijenta</span><span class="sxs-lookup"><span data-stu-id="abbb3-146">Drive to client location</span></span> | <span data-ttu-id="abbb3-147">Kilometraža</span><span class="sxs-lookup"><span data-stu-id="abbb3-147">Mileage</span></span>             | <span data-ttu-id="abbb3-148">Milja</span><span class="sxs-lookup"><span data-stu-id="abbb3-148">Mile</span></span>  | <span data-ttu-id="abbb3-149">10</span><span class="sxs-lookup"><span data-stu-id="abbb3-149">10</span></span>        | <span data-ttu-id="abbb3-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="abbb3-150">10 USD</span></span>         |

<span data-ttu-id="abbb3-151">Za vreme, svako zaglavlje cenovnika ima polje **Podrazumevana jedinica za vreme**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="abbb3-152">Vrednost se podešava kada kreirate zaglavlje cenovnika.</span><span class="sxs-lookup"><span data-stu-id="abbb3-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="abbb3-153">Ova jedinica se zatim koristi za podešavanje svih cena zasnovanih na ulogama u tom cenovniku.</span><span class="sxs-lookup"><span data-stu-id="abbb3-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="abbb3-154">Stavke procene za polje **Vreme za ponudu** mogu se izraziti u bilo kojoj jedinici vremena.</span><span class="sxs-lookup"><span data-stu-id="abbb3-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="abbb3-155">Međutim, stavke procene u projektima i stavke vremena za projekte mogu da koriste samo jedinicu vremena **Čas**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="abbb3-156">Ako se jedinica u redu "Stavka vremena" ili "Stavka procene" ne podudara sa jedinicom u redu cenovnika za tu ulogu, sistem konvertuje cenu u jedinice koje su definisane u proceni projekta ili u transakciji stvarnih vrednosti projekta.</span><span class="sxs-lookup"><span data-stu-id="abbb3-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="abbb3-157">Sledeći primer prikazuje kako PSA koristi grupu jedinica, jedinice i faktore konverzije.</span><span class="sxs-lookup"><span data-stu-id="abbb3-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="abbb3-158">Jedinice</span><span class="sxs-lookup"><span data-stu-id="abbb3-158">Units</span></span>

   - <span data-ttu-id="abbb3-159">**Grupa jedinica**: Vreme</span><span class="sxs-lookup"><span data-stu-id="abbb3-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="abbb3-160">**Jedinice**: čas</span><span class="sxs-lookup"><span data-stu-id="abbb3-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="abbb3-161">**Dan** - Faktor konverzije: 8 časova</span><span class="sxs-lookup"><span data-stu-id="abbb3-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="abbb3-162">**Sedmica** - Faktor konverzije: 40 časova</span><span class="sxs-lookup"><span data-stu-id="abbb3-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="abbb3-163">Podešavanje cenovnika za projekat A:</span><span class="sxs-lookup"><span data-stu-id="abbb3-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="abbb3-164">**Naziv**: Prodajne cene u UK za 2016</span><span class="sxs-lookup"><span data-stu-id="abbb3-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="abbb3-165">**Podrazumevana jedinica vremena**: dan</span><span class="sxs-lookup"><span data-stu-id="abbb3-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="abbb3-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="abbb3-166">**Currency**: GBP</span></span>

| <span data-ttu-id="abbb3-167">Uloga</span><span class="sxs-lookup"><span data-stu-id="abbb3-167">Role</span></span>      | <span data-ttu-id="abbb3-168">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-168">Unit group</span></span> | <span data-ttu-id="abbb3-169">Jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-169">Unit</span></span> | <span data-ttu-id="abbb3-170">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-170">Organizational unit</span></span> | <span data-ttu-id="abbb3-171">Cena</span><span class="sxs-lookup"><span data-stu-id="abbb3-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="abbb3-172">Programer</span><span class="sxs-lookup"><span data-stu-id="abbb3-172">Developer</span></span> | <span data-ttu-id="abbb3-173">Time</span><span class="sxs-lookup"><span data-stu-id="abbb3-173">Time</span></span>       | <span data-ttu-id="abbb3-174">Day</span><span class="sxs-lookup"><span data-stu-id="abbb3-174">Day</span></span>  | <span data-ttu-id="abbb3-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="abbb3-175">Contoso UK</span></span>          | <span data-ttu-id="abbb3-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="abbb3-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="abbb3-177">Stavka vremena</span><span class="sxs-lookup"><span data-stu-id="abbb3-177">Time entry</span></span>

<span data-ttu-id="abbb3-178">Sledeća tabela prikazuje krajnju transakciju na strani prodaje koju je kreirao PSA za trosatni projekat.</span><span class="sxs-lookup"><span data-stu-id="abbb3-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="abbb3-179">Projekat</span><span class="sxs-lookup"><span data-stu-id="abbb3-179">Project</span></span>   | <span data-ttu-id="abbb3-180">Zadatak</span><span class="sxs-lookup"><span data-stu-id="abbb3-180">Task</span></span>    | <span data-ttu-id="abbb3-181">Uloga</span><span class="sxs-lookup"><span data-stu-id="abbb3-181">Role</span></span>      | <span data-ttu-id="abbb3-182">Količina</span><span class="sxs-lookup"><span data-stu-id="abbb3-182">Quantity</span></span> | <span data-ttu-id="abbb3-183">Jedinica</span><span class="sxs-lookup"><span data-stu-id="abbb3-183">Unit</span></span>  | <span data-ttu-id="abbb3-184">Cena po jedinici</span><span class="sxs-lookup"><span data-stu-id="abbb3-184">Unit price</span></span> | <span data-ttu-id="abbb3-185">Nenaplaćen iznos prodaje</span><span class="sxs-lookup"><span data-stu-id="abbb3-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="abbb3-186">Projekat A</span><span class="sxs-lookup"><span data-stu-id="abbb3-186">Project A</span></span> | <span data-ttu-id="abbb3-187">Dizajn</span><span class="sxs-lookup"><span data-stu-id="abbb3-187">Design</span></span>  | <span data-ttu-id="abbb3-188">Programer</span><span class="sxs-lookup"><span data-stu-id="abbb3-188">Developer</span></span> | <span data-ttu-id="abbb3-189">3</span><span class="sxs-lookup"><span data-stu-id="abbb3-189">3</span></span>        | <span data-ttu-id="abbb3-190">Hour</span><span class="sxs-lookup"><span data-stu-id="abbb3-190">Hour</span></span>  | <span data-ttu-id="abbb3-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="abbb3-191">100 GBP</span></span>    | <span data-ttu-id="abbb3-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="abbb3-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="abbb3-193">Najčešća pitanja o jedinici vremena</span><span class="sxs-lookup"><span data-stu-id="abbb3-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="abbb3-194">Da li PSA obavlja konverziju u različite jedinice u slučaju troška?</span><span class="sxs-lookup"><span data-stu-id="abbb3-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="abbb3-195">Ne.</span><span class="sxs-lookup"><span data-stu-id="abbb3-195">No.</span></span> <span data-ttu-id="abbb3-196">Konverzija jedinice funkcioniše samo za vreme.</span><span class="sxs-lookup"><span data-stu-id="abbb3-196">Unit conversion works only for time.</span></span> <span data-ttu-id="abbb3-197">Za troškove, ako sistem ne može da pronađe cenu za kombinaciju kategorije troška i jedinice, cena je podrazumevano podešena na 0,00.</span><span class="sxs-lookup"><span data-stu-id="abbb3-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="abbb3-198">Zašto PSA konvertuje jedinice vremena?</span><span class="sxs-lookup"><span data-stu-id="abbb3-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="abbb3-199">U nekim zemljama ili regionima postoji zakonski uslov da se stope naplate podešavaju u danima.</span><span class="sxs-lookup"><span data-stu-id="abbb3-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="abbb3-200">Pregovaranje oko cene i popusti tokom ciklusa ponude se obavljaju korišćenjem dnevnih cena za svaku ulogu koju je moguće naplatiti.</span><span class="sxs-lookup"><span data-stu-id="abbb3-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="abbb3-201">Procena rasporeda i stavke vremena se unose u časovima.</span><span class="sxs-lookup"><span data-stu-id="abbb3-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="abbb3-202">Da bi podržao ovu razliku u jedinicama vremena, PSA ih konvertuje.</span><span class="sxs-lookup"><span data-stu-id="abbb3-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="abbb3-203">Da li se jedinice vremena mogu menjati u zavisnosti od procena za projekat?</span><span class="sxs-lookup"><span data-stu-id="abbb3-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="abbb3-204">Ne.</span><span class="sxs-lookup"><span data-stu-id="abbb3-204">No.</span></span> <span data-ttu-id="abbb3-205">Procena rasporeda je trenutno ograničena na časove i ne može se promeniti.</span><span class="sxs-lookup"><span data-stu-id="abbb3-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="abbb3-206">Da li jedinice i grupe jedinica mogu da se uređuju, brišu i dodaju?</span><span class="sxs-lookup"><span data-stu-id="abbb3-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="abbb3-207">Da.</span><span class="sxs-lookup"><span data-stu-id="abbb3-207">Yes.</span></span> <span data-ttu-id="abbb3-208">Sa izuzetkom grupa jedinica **Vreme** i **Čas**, sve jedinice mogu da se brišu ili uređuju i mogu da se dodaju nove jedinice.</span><span class="sxs-lookup"><span data-stu-id="abbb3-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="abbb3-209">U aplikaciji PSA nije moguće izbrisati grupu jedinica **Vreme** i **Čas**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="abbb3-210">Međutim, one mogu da se ažuriraju prevedenim tekstom za polje **Ime**.</span><span class="sxs-lookup"><span data-stu-id="abbb3-210">However, they can be updated with a translated text for the **Name** field.</span></span>
