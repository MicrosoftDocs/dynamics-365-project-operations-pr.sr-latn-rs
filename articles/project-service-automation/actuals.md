---
title: Stvarne vrednosti
description: Ova tema pruža informacije o stvarnim vrednostima projekta.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755228"
---
# <a name="actuals"></a><span data-ttu-id="0f45a-103">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="0f45a-104">Stvarne vrednosti predstavljaju količinu posla koja je završena za projekat.</span><span class="sxs-lookup"><span data-stu-id="0f45a-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="0f45a-105">Stvarne vrednosti projekta mogu da se prate do njegovih izvornih dokumenata.</span><span class="sxs-lookup"><span data-stu-id="0f45a-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="0f45a-106">Ti izvorni dokumenti uključuju vreme, troškove i stavke knjiženja u glavnoj knjizi, kao i fakture.</span><span class="sxs-lookup"><span data-stu-id="0f45a-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kako se stvarne vrednosti projekta prate do izvornih dokumenata](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="0f45a-108">Prosleđivanje stavke vremena</span><span class="sxs-lookup"><span data-stu-id="0f45a-108">Submitting a time entry</span></span>

<span data-ttu-id="0f45a-109">Kod aplikacije PSA, kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0f45a-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0f45a-110">Jedna stavka je za troškove, a druga za nefakturisane prodaje.</span><span class="sxs-lookup"><span data-stu-id="0f45a-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0f45a-111">Kada se stavka vremena prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove.</span><span class="sxs-lookup"><span data-stu-id="0f45a-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="0f45a-112">Logiku za unos podrazumevanih cena možete da pronađete u stavki u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0f45a-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="0f45a-113">Sve vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0f45a-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="0f45a-114">Ova polja uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="0f45a-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="0f45a-115">Polja koja utiču na podrazumevane cene, kao što su **Uloga** i **Organizaciona jedinica** prouzrokuju podrazumevani unos odgovarajuće cene u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0f45a-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="0f45a-116">Ako u stavku vremena dodate prilagođeno polje, a želite da se vrednost polja širi na stvarne vrednosti, kreirajte polje u entitetu Stvarne vrednosti i upotrebite preslikavanja polja da biste kopirali polje iz stavke vremena u stvarnu vrednost.</span><span class="sxs-lookup"><span data-stu-id="0f45a-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="0f45a-117">Prosleđivanje stavke troška</span><span class="sxs-lookup"><span data-stu-id="0f45a-117">Submitting an expense entry</span></span>

<span data-ttu-id="0f45a-118">Kod aplikacije PSA, kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o vremenu i materijalima, kreiraju se dve stavke u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="0f45a-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="0f45a-119">Jedna stavka je za troškove, a druga za nefakturisane prodaje.</span><span class="sxs-lookup"><span data-stu-id="0f45a-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="0f45a-120">Kada se stavka troška prosledi za projekat koji je mapiran na predmet ugovora o fiksnoj ceni, kreira se stavka u glavnoj knjizi samo za troškove.</span><span class="sxs-lookup"><span data-stu-id="0f45a-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="0f45a-121">Logika za unos podrazumevanih cena za troškove temelji se na kategoriji troškova koja je izabrana na stranici **Stavka troškova**.</span><span class="sxs-lookup"><span data-stu-id="0f45a-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="0f45a-122">Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="0f45a-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="0f45a-123">Međutim, za samu cenu, iznos koji je korisnik uneo podrazumevano se podešava direktno na povezanim stavkama troškova u glavnoj knjizi za troškove i prodaju.</span><span class="sxs-lookup"><span data-stu-id="0f45a-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="0f45a-124">U trenutnoj verziji aplikacije PSA, nije dostupna stavka zasnovana na kategoriji podrazumevanih cena po jedinici za stavke troškova.</span><span class="sxs-lookup"><span data-stu-id="0f45a-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="0f45a-125">Korišćenje glavnih knjiga za evidentiranje troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-125">Using journals to record costs</span></span>

<span data-ttu-id="0f45a-126">U aplikaciji PSA, glavne knjige vam omogućavaju da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija.</span><span class="sxs-lookup"><span data-stu-id="0f45a-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="0f45a-127">Glavna knjiga ima zaglavlje, stavke i radnju **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="0f45a-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="0f45a-128">Evo nekoliko scenarija gde možete da koristite glavnu knjigu:</span><span class="sxs-lookup"><span data-stu-id="0f45a-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="0f45a-129">Morate zabeležiti stvarne troškove i prodaju materijala na projektu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="0f45a-130">Morate premestiti stvarne vrednosti transakcija iz drugog sistema u PSA.</span><span class="sxs-lookup"><span data-stu-id="0f45a-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="0f45a-131">Morate da evidentirate troškove ostvarene u drugom sistemu, kao što su troškovi nabavke ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="0f45a-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="0f45a-132">Evidentiranje stvarnih vrednosti na osnovu događaja u projektu</span><span class="sxs-lookup"><span data-stu-id="0f45a-132">Recording actuals based on project events</span></span>

<span data-ttu-id="0f45a-133">PSA beleži finansijske transakcije koje se dešavaju tokom projekta.</span><span class="sxs-lookup"><span data-stu-id="0f45a-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="0f45a-134">Ove transakcije se evidentiraju kao **stvarne vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="0f45a-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="0f45a-135">Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.</span><span class="sxs-lookup"><span data-stu-id="0f45a-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="0f45a-136">**Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta**</span><span class="sxs-lookup"><span data-stu-id="0f45a-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0f45a-137">Događaj</span><span class="sxs-lookup"><span data-stu-id="0f45a-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0f45a-138">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="0f45a-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0f45a-139">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0f45a-140">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0f45a-141">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="0f45a-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0f45a-142">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0f45a-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0f45a-143">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-143">Actuals</span></span></th>
<th><span data-ttu-id="0f45a-144">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0f45a-144">Transaction currency</span></span></th>
<th><span data-ttu-id="0f45a-145">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0f45a-145">Fixed price</span></span></th>
<th><span data-ttu-id="0f45a-146">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0f45a-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f45a-147">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="0f45a-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0f45a-148">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-149">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="0f45a-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0f45a-150">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f45a-151">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f45a-152">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-152">Cost actual</span></span></td>
<td><span data-ttu-id="0f45a-153">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-154">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-155">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="0f45a-156">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-157">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-158">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="0f45a-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0f45a-159">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f45a-160">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f45a-161">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-161">Cost actual</span></span></td>
<td><span data-ttu-id="0f45a-162">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-163">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-164">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-165">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-166">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-167">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-168">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-169">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-170">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f45a-171">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f45a-172">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f45a-173">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-174">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0f45a-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-175">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-176">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-177">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-178">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0f45a-178">Billed sales</span></span></td>
<td><span data-ttu-id="0f45a-179">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f45a-180">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f45a-181">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f45a-182">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-183">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-184">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-185">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-186">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-187">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-188">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-189">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-190">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f45a-191">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0f45a-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f45a-192">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0f45a-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f45a-193">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0f45a-194">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0f45a-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0f45a-195">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="0f45a-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0f45a-196">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-197">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-198">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-199">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0f45a-199">Billed sales</span></span></td>
<td><span data-ttu-id="0f45a-200">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f45a-201">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0f45a-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f45a-202">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0f45a-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f45a-203">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-204">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-205">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-206">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-207">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0f45a-208">**Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta**</span><span class="sxs-lookup"><span data-stu-id="0f45a-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="0f45a-209">Događaj</span><span class="sxs-lookup"><span data-stu-id="0f45a-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="0f45a-210">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="0f45a-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="0f45a-211">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="0f45a-212">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="0f45a-213">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="0f45a-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="0f45a-214">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0f45a-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0f45a-215">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-215">Actuals</span></span></th>
<th><span data-ttu-id="0f45a-216">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0f45a-216">Transaction currency</span></span></th>
<th><span data-ttu-id="0f45a-217">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="0f45a-217">Fixed price</span></span></th>
<th><span data-ttu-id="0f45a-218">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="0f45a-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f45a-219">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="0f45a-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="0f45a-220">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-221">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="0f45a-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="0f45a-222">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="0f45a-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0f45a-223">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f45a-224">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-224">Cost actual</span></span></td>
<td><span data-ttu-id="0f45a-225">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0f45a-226">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0f45a-227">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="0f45a-228">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="0f45a-229">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-230">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="0f45a-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="0f45a-231">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-232">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0f45a-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0f45a-233">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0f45a-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-234">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="0f45a-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0f45a-235">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0f45a-236">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="0f45a-237">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-237">Cost actual</span></span></td>
<td><span data-ttu-id="0f45a-238">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-239">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-240">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-241">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-242">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="0f45a-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-243">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0f45a-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="0f45a-244">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="0f45a-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-245">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="0f45a-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="0f45a-246">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="0f45a-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-247">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-248">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-249">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-250">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f45a-251">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f45a-252">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f45a-253">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-254">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0f45a-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-255">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-256">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="0f45a-257">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-258">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0f45a-258">Billed sales</span></span></td>
<td><span data-ttu-id="0f45a-259">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f45a-260">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="0f45a-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="0f45a-261">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="0f45a-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="0f45a-262">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-263">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-264">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-265">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0f45a-266">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-267">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-268">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-269">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-270">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0f45a-271">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0f45a-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f45a-272">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0f45a-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f45a-273">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="0f45a-274">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="0f45a-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="0f45a-275">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="0f45a-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="0f45a-276">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-277">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="0f45a-278">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="0f45a-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-279">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="0f45a-279">Billed sales</span></span></td>
<td><span data-ttu-id="0f45a-280">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0f45a-281">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="0f45a-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="0f45a-282">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="0f45a-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="0f45a-283">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-284">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="0f45a-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="0f45a-285">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f45a-286">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="0f45a-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="0f45a-287">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="0f45a-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
