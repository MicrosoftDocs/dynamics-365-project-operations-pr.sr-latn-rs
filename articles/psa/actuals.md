---
title: Pregled trenutnog stanja
description: Ova tema pruža informacije o stvarnim vrednostima projekta.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129785"
---
# <a name="actuals-overview"></a><span data-ttu-id="0c5eb-103">Pregled trenutnog stanja</span><span class="sxs-lookup"><span data-stu-id="0c5eb-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0c5eb-104">Stvarne vrednosti predstavljaju količinu posla koja je završena za projekat.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0c5eb-105">Stvarne vrednosti projekta mogu da se prate do njegovih izvornih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0c5eb-106">Ti izvorni dokumenti uključuju vreme, troškove i stavke knjiženja u glavnoj knjizi, kao i fakture.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se stvarne vrednosti projekta prate do izvornih dokumenata](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0c5eb-108">Prosleđivanje stavke vremena</span><span class="sxs-lookup"><span data-stu-id="0c5eb-108">Submitting a time entry</span></span>

<span data-ttu-id="0c5eb-109">Kod aplikacije PSA, kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0c5eb-110">Jedna stavka je za troškove, a druga za nefakturisane prodaje.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0c5eb-111">Kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0c5eb-112">Logiku za unos podrazumevanih cena možete da pronađete u stavki u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0c5eb-113">Sve vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0c5eb-114">Ova polja uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0c5eb-115">Polja koja utiču na podrazumevane cene, kao što su **Uloga** i **Organizaciona jedinica** prouzrokuju podrazumevani unos odgovarajuće cene u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0c5eb-116">Ako u stavku vremena dodate prilagođeno polje, a želite da se vrednost polja širi na stvarne vrednosti, kreirajte polje u entitetu Stvarne vrednosti i upotrebite preslikavanja polja da biste kopirali polje iz stavke vremena u stvarnu vrednost.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0c5eb-117">Prosleđivanje stavke troška</span><span class="sxs-lookup"><span data-stu-id="0c5eb-117">Submitting an expense entry</span></span>

<span data-ttu-id="0c5eb-118">Kod aplikacije PSA, kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0c5eb-119">Jedna stavka je za troškove, a druga za nefakturisane prodaje.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0c5eb-120">Kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0c5eb-121">Logika za unos podrazumevanih cena za troškove temelji se na kategoriji troškova koja je izabrana na stranici **Stavka troškova**.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0c5eb-122">Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0c5eb-123">Međutim, za samu cenu, iznos koji je korisnik uneo podrazumevano se podešava direktno na povezanim stavkama troškova u glavnoj knjizi za troškove i prodaju.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0c5eb-124">U trenutnoj verziji aplikacije PSA, nije dostupna stavka zasnovana na kategoriji podrazumevanih cena po jedinici za stavke troškova.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="0c5eb-125">Korišćenje ulaznih glavnih knjiga za evidentiranje troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="0c5eb-126">U aplikaciji PSA, ulazne glavne knjige vam omogućavaju da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0c5eb-127">Glavna knjiga ima zaglavlje, stavke i radnju **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0c5eb-128">Evo nekoliko scenarija gde možete da koristite glavnu knjigu:</span><span class="sxs-lookup"><span data-stu-id="0c5eb-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0c5eb-129">Morate zabeležiti stvarne troškove i prodaju materijala na projektu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0c5eb-130">Morate premestiti stvarne vrednosti transakcija iz drugog sistema u PSA.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0c5eb-131">Morate da evidentirate troškove ostvarene u drugom sistemu, kao što su troškovi nabavke ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c5eb-132">Korišćenje ulaznih glavnih knjiga za kreiranje stvarnih podataka treba da radi samo korisnik koji je u potpunosti svestan računovodstvenog uticaja koji stvarni ljudi imaju na projekat.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="0c5eb-133">To je zato što aplikacija ne potvrđuje valjanost tipa stavke u glavnoj knjizi ili srodnu cenu koja se unosi u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="0c5eb-134">Zbog uticaja ovog tipa glavne knjige, budite oprezni po pitanju kome je omogućen pristup kreiranja ulaznih glavnih knjiga.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0c5eb-135">Evidentiranje stvarnih vrednosti na osnovu događaja u projektu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-135">Recording actuals based on project events</span></span>

<span data-ttu-id="0c5eb-136">PSA beleži finansijske transakcije koje se dešavaju tokom projekta.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0c5eb-137">Ove transakcije se evidentiraju kao **stvarne vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0c5eb-138">Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0c5eb-139">**Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta**</span><span class="sxs-lookup"><span data-stu-id="0c5eb-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0c5eb-140">Događaj</span><span class="sxs-lookup"><span data-stu-id="0c5eb-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0c5eb-141">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="0c5eb-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0c5eb-142">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0c5eb-143">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0c5eb-144">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="0c5eb-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0c5eb-145">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0c5eb-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0c5eb-146">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-146">Actuals</span></span></th>
<th><span data-ttu-id="0c5eb-147">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0c5eb-147">Transaction currency</span></span></th>
<th><span data-ttu-id="0c5eb-148">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0c5eb-148">Fixed price</span></span></th>
<th><span data-ttu-id="0c5eb-149">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0c5eb-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0c5eb-150">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0c5eb-151">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-152">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0c5eb-153">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c5eb-154">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c5eb-155">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-155">Cost actual</span></span></td>
<td><span data-ttu-id="0c5eb-156">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-157">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-158">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0c5eb-159">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-160">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-161">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0c5eb-162">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c5eb-163">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c5eb-164">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-164">Cost actual</span></span></td>
<td><span data-ttu-id="0c5eb-165">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-166">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-167">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-168">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-169">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-170">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-171">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-172">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-173">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c5eb-174">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c5eb-175">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c5eb-176">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-177">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-178">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-179">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-180">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-181">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0c5eb-181">Billed sales</span></span></td>
<td><span data-ttu-id="0c5eb-182">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c5eb-183">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c5eb-184">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c5eb-185">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-186">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-187">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-188">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-189">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-190">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-191">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-192">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-193">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c5eb-194">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c5eb-195">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c5eb-196">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0c5eb-197">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0c5eb-198">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="0c5eb-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0c5eb-199">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-200">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-201">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-202">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0c5eb-202">Billed sales</span></span></td>
<td><span data-ttu-id="0c5eb-203">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c5eb-204">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c5eb-205">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c5eb-206">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-207">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-208">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-209">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-210">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0c5eb-211">**Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta**</span><span class="sxs-lookup"><span data-stu-id="0c5eb-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0c5eb-212">Događaj</span><span class="sxs-lookup"><span data-stu-id="0c5eb-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0c5eb-213">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="0c5eb-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0c5eb-214">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0c5eb-215">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0c5eb-216">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="0c5eb-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0c5eb-217">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0c5eb-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0c5eb-218">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-218">Actuals</span></span></th>
<th><span data-ttu-id="0c5eb-219">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0c5eb-219">Transaction currency</span></span></th>
<th><span data-ttu-id="0c5eb-220">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0c5eb-220">Fixed price</span></span></th>
<th><span data-ttu-id="0c5eb-221">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0c5eb-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0c5eb-222">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0c5eb-223">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-224">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0c5eb-225">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0c5eb-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0c5eb-226">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c5eb-227">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-227">Cost actual</span></span></td>
<td><span data-ttu-id="0c5eb-228">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0c5eb-229">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0c5eb-230">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0c5eb-231">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0c5eb-232">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-233">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0c5eb-234">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-235">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0c5eb-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0c5eb-236">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0c5eb-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-237">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="0c5eb-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0c5eb-238">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0c5eb-239">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0c5eb-240">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-240">Cost actual</span></span></td>
<td><span data-ttu-id="0c5eb-241">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-242">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-243">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-244">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-245">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0c5eb-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-246">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0c5eb-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0c5eb-247">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0c5eb-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-248">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="0c5eb-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0c5eb-249">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0c5eb-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-250">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-251">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-252">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-253">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c5eb-254">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c5eb-255">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c5eb-256">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-257">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-258">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-259">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0c5eb-260">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-261">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0c5eb-261">Billed sales</span></span></td>
<td><span data-ttu-id="0c5eb-262">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c5eb-263">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0c5eb-264">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0c5eb-265">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-266">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-267">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-268">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0c5eb-269">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-270">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-271">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-272">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-273">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0c5eb-274">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c5eb-275">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c5eb-276">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0c5eb-277">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0c5eb-278">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="0c5eb-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0c5eb-279">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-280">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0c5eb-281">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0c5eb-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-282">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0c5eb-282">Billed sales</span></span></td>
<td><span data-ttu-id="0c5eb-283">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0c5eb-284">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0c5eb-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0c5eb-285">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0c5eb-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0c5eb-286">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-287">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0c5eb-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0c5eb-288">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0c5eb-289">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0c5eb-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0c5eb-290">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0c5eb-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
