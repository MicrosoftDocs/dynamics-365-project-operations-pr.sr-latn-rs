---
title: Trenutno stanje
description: Ova tema pruža informacije o načinu rada sa stvarnim podacima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126334"
---
# <a name="actuals"></a><span data-ttu-id="c8927-103">Trenutno stanje</span><span class="sxs-lookup"><span data-stu-id="c8927-103">Actuals</span></span> 

<span data-ttu-id="c8927-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="c8927-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c8927-105">Stvarne vrednosti predstavljaju količinu posla koja je završena za projekat.</span><span class="sxs-lookup"><span data-stu-id="c8927-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="c8927-106">Kreirani su kao rezultat stavki vremena i troškova, stavki knjiženja u glavnoj knjizi i faktura.</span><span class="sxs-lookup"><span data-stu-id="c8927-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="c8927-107">Stavke u glavnoj knjizi i vreme predaje</span><span class="sxs-lookup"><span data-stu-id="c8927-107">Journal lines and time submission</span></span>

<span data-ttu-id="c8927-108">Za više informacija o stavci vremena, pogledajte [Pregled unosa vremena](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8927-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c8927-109">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="c8927-109">Time and materials</span></span>

<span data-ttu-id="c8927-110">Kada je stavka vremena koja je prosleđena povezana sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="c8927-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c8927-111">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-111">Fixed price</span></span>

<span data-ttu-id="c8927-112">Kada se prosleđena stavka vremena poveže sa projektom koji se mapiran na predmet ugovora sa fiksnom cenom, sistem kreira jednu stavku u glavnoj knjizi za troškove.</span><span class="sxs-lookup"><span data-stu-id="c8927-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c8927-113">Podrazumevano određivanje cena</span><span class="sxs-lookup"><span data-stu-id="c8927-113">Default pricing</span></span>

<span data-ttu-id="c8927-114">Logika za kreiranje podrazumevanih cena se nalazi u stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c8927-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="c8927-115">Vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c8927-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="c8927-116">Ove vrednosti uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="c8927-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="c8927-117">Polja koja utiču na podrazumevano određivanje cena, kao što su **Uloga** i **Organizaciona jedinica**, koriste se za utvrđivanje odgovarajuće cene u stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c8927-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="c8927-118">Na stavku vremena možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="c8927-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="c8927-119">Ako želite da se vrednost polja širi na stvarne vrednosti, kreirajte polje u entitetu Stvarne vrednosti i upotrebite mapiranja polja da biste kopirali polje iz stavke vremena u stvarnu vrednost.</span><span class="sxs-lookup"><span data-stu-id="c8927-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="c8927-120">Prosleđivanje stavki u glavnoj knjizi i osnovnih troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="c8927-121">Za više informacija o stavci troška, pogledajte [Pregled troškova](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c8927-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="c8927-122">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="c8927-122">Time and materials</span></span>

<span data-ttu-id="c8927-123">Kada se stavka osnovnog troška koja je prosleđena poveže sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="c8927-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="c8927-124">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-124">Fixed price</span></span>

<span data-ttu-id="c8927-125">Kada se prosleđena stavka osnovnog troška poveže sa projektom koji se mapiran na predmet ugovora sa fiksnom cenom, sistem kreira jednu stavku u glavnoj knjizi za troškove.</span><span class="sxs-lookup"><span data-stu-id="c8927-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="c8927-126">Podrazumevano određivanje cena</span><span class="sxs-lookup"><span data-stu-id="c8927-126">Default pricing</span></span>

<span data-ttu-id="c8927-127">Logika unošenja zadatih cena za troškove zasniva se na kategoriji troškova.</span><span class="sxs-lookup"><span data-stu-id="c8927-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="c8927-128">Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="c8927-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="c8927-129">Međutim, iznos koji se unese za samu cenu podrazumevano se podešava direktno na povezanim stavkama troškova u glavnoj knjizi za troškove i prodaju.</span><span class="sxs-lookup"><span data-stu-id="c8927-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="c8927-130">Nije dostupna stavka zasnovana na kategoriji podrazumevanih cena po jedinici za stavke troškova.</span><span class="sxs-lookup"><span data-stu-id="c8927-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="c8927-131">Korišćenje dnevnika za knjiženje za evidentiranje troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-131">Use entry journals to record costs</span></span>

<span data-ttu-id="c8927-132">Možete da koristite dnevnike za knjiženje da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija.</span><span class="sxs-lookup"><span data-stu-id="c8927-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="c8927-133">Dnevnici se mogu koristiti u sledeće svrhe:</span><span class="sxs-lookup"><span data-stu-id="c8927-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="c8927-134">Zabeležite stvarne troškove materijala i prodaje na projektu.</span><span class="sxs-lookup"><span data-stu-id="c8927-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="c8927-135">Premestite stvarne vrednosti transakcija iz drugog sistema u Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c8927-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="c8927-136">Evidentirajte troškove koji su se dogodili u drugom sistemu.</span><span class="sxs-lookup"><span data-stu-id="c8927-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="c8927-137">Ovi troškovi mogu uključivati troškove nabavke ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="c8927-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8927-138">Aplikacija ne potvrđuje tip stavke u glavnoj knjizi ili povezano određivanje cena koje se unosi u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="c8927-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="c8927-139">Stoga samo korisnik koji je potpuno svestan računovodstvenog uticaja koji stvarne vrednosti imaju na projekat treba da koristi dnevnike za knjiženje za kreiranje stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="c8927-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="c8927-140">Zbog uticaja ovog tipa dnevnika, pažljivo birajte ko ima pristup kreiranju dnevnika za knjiženje.</span><span class="sxs-lookup"><span data-stu-id="c8927-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="c8927-141">Evidentiranje stvarnih vrednosti na osnovu događaja u projektu</span><span class="sxs-lookup"><span data-stu-id="c8927-141">Record actuals based on project events</span></span>

<span data-ttu-id="c8927-142">Project Operations beleži finansijske transakcije koje se dešavaju tokom projekta.</span><span class="sxs-lookup"><span data-stu-id="c8927-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="c8927-143">Ove transakcije se evidentiraju kao stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="c8927-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="c8927-144">Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.</span><span class="sxs-lookup"><span data-stu-id="c8927-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="c8927-145">Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta</span><span class="sxs-lookup"><span data-stu-id="c8927-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c8927-146">Događaj</span><span class="sxs-lookup"><span data-stu-id="c8927-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c8927-147">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="c8927-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c8927-148">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c8927-149">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c8927-150">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="c8927-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c8927-151">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c8927-152">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-152">Actuals</span></span></th>
<th><span data-ttu-id="c8927-153">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="c8927-153">Transaction currency</span></span></th>
<th><span data-ttu-id="c8927-154">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-154">Fixed price</span></span></th>
<th><span data-ttu-id="c8927-155">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="c8927-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c8927-156">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="c8927-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c8927-157">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-158">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="c8927-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c8927-159">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8927-160">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8927-161">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-161">Cost actual</span></span></td>
<td><span data-ttu-id="c8927-162">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-163">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-164">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="c8927-165">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-166">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-167">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="c8927-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c8927-168">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8927-169">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8927-170">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-170">Cost actual</span></span></td>
<td><span data-ttu-id="c8927-171">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-172">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-173">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-174">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-175">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-176">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-177">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-178">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-179">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8927-180">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8927-181">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8927-182">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-183">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="c8927-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-184">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-185">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-186">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-187">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="c8927-187">Billed sales</span></span></td>
<td><span data-ttu-id="c8927-188">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8927-189">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8927-190">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8927-191">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-192">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-193">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-194">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-195">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-196">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-197">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-198">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-199">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8927-200">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="c8927-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8927-201">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="c8927-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8927-202">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c8927-203">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="c8927-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c8927-204">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="c8927-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c8927-205">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-206">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-207">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-208">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="c8927-208">Billed sales</span></span></td>
<td><span data-ttu-id="c8927-209">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8927-210">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="c8927-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8927-211">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="c8927-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8927-212">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-213">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-214">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-215">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-216">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="c8927-217">Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta</span><span class="sxs-lookup"><span data-stu-id="c8927-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="c8927-218">Događaj</span><span class="sxs-lookup"><span data-stu-id="c8927-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="c8927-219">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="c8927-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="c8927-220">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="c8927-221">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="c8927-222">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="c8927-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="c8927-223">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c8927-224">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-224">Actuals</span></span></th>
<th><span data-ttu-id="c8927-225">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="c8927-225">Transaction currency</span></span></th>
<th><span data-ttu-id="c8927-226">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="c8927-226">Fixed price</span></span></th>
<th><span data-ttu-id="c8927-227">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="c8927-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c8927-228">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="c8927-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="c8927-229">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-230">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="c8927-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="c8927-231">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="c8927-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="c8927-232">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8927-233">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-233">Cost actual</span></span></td>
<td><span data-ttu-id="c8927-234">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c8927-235">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c8927-236">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="c8927-237">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="c8927-238">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-239">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="c8927-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="c8927-240">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-241">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="c8927-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c8927-242">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="c8927-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-243">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="c8927-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c8927-244">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="c8927-245">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="c8927-246">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-246">Cost actual</span></span></td>
<td><span data-ttu-id="c8927-247">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-248">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-249">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-250">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-251">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="c8927-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-252">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="c8927-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="c8927-253">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="c8927-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-254">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="c8927-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="c8927-255">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="c8927-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-256">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-257">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-258">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-259">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8927-260">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8927-261">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8927-262">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-263">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="c8927-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-264">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-265">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="c8927-266">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-267">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="c8927-267">Billed sales</span></span></td>
<td><span data-ttu-id="c8927-268">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8927-269">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="c8927-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="c8927-270">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="c8927-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="c8927-271">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-272">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-273">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-274">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="c8927-275">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-276">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-277">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-278">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-279">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="c8927-280">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="c8927-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8927-281">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="c8927-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8927-282">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="c8927-283">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="c8927-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="c8927-284">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="c8927-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="c8927-285">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-286">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="c8927-287">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="c8927-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-288">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="c8927-288">Billed sales</span></span></td>
<td><span data-ttu-id="c8927-289">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="c8927-290">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="c8927-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="c8927-291">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="c8927-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="c8927-292">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-293">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="c8927-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="c8927-294">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c8927-295">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="c8927-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="c8927-296">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="c8927-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
