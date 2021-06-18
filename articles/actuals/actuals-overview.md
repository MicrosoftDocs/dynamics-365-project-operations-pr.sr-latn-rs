---
title: Trenutno stanje
description: Ova tema pruža informacije o tome kako se radi sa stvarnim podacima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996628"
---
# <a name="actuals"></a><span data-ttu-id="964c1-103">Trenutno stanje</span><span class="sxs-lookup"><span data-stu-id="964c1-103">Actuals</span></span> 

<span data-ttu-id="964c1-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="964c1-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="964c1-105">Trenutno stanje predstavlja pregledani i odobreni finansijski i vremenski raspored projekta.</span><span class="sxs-lookup"><span data-stu-id="964c1-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="964c1-106">Kreira se kao rezultat odobravanja vremena, troškova, stavki upotrebe materijala, stavki dnevnika i faktura.</span><span class="sxs-lookup"><span data-stu-id="964c1-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="964c1-107">Stavke u glavnoj knjizi i vreme predaje</span><span class="sxs-lookup"><span data-stu-id="964c1-107">Journal lines and time submission</span></span>

<span data-ttu-id="964c1-108">Za više informacija o stavci vremena, pogledajte [Pregled unosa vremena](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="964c1-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="964c1-109">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="964c1-109">Time and materials</span></span>

<span data-ttu-id="964c1-110">Kada je stavka vremena koja je prosleđena povezana sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="964c1-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="964c1-111">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-111">Fixed price</span></span>

<span data-ttu-id="964c1-112">Kada se prosleđena stavka vremena poveže sa projektom koji se mapiran na predmet ugovora sa fiksnom cenom, sistem kreira jednu stavku u glavnoj knjizi za troškove.</span><span class="sxs-lookup"><span data-stu-id="964c1-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="964c1-113">Podrazumevano određivanje cena</span><span class="sxs-lookup"><span data-stu-id="964c1-113">Default pricing</span></span>

<span data-ttu-id="964c1-114">Logika za kreiranje podrazumevanih cena se nalazi u stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="964c1-115">Vrednosti polja iz stavke vremena kopiraju se u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="964c1-116">Ove vrednosti uključuju datum transakcije, predmet ugovora na koji je projekat mapiran i valutu koja je rezultat odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="964c1-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="964c1-117">Polja koja utiču na podrazumevane cene, kao što su **Uloga** i **Jedinica za određivanje resursa**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="964c1-118">Na stavku vremena možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="964c1-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="964c1-119">Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="964c1-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="964c1-120">Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija.</span><span class="sxs-lookup"><span data-stu-id="964c1-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="964c1-121">Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="964c1-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="964c1-122">Prosleđivanje stavki u glavnoj knjizi i osnovnih troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="964c1-123">Za više informacija o stavci troška, pogledajte [Pregled troškova](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="964c1-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="964c1-124">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="964c1-124">Time and materials</span></span>

<span data-ttu-id="964c1-125">Kada se stavka osnovnog troška koja je prosleđena poveže sa projektom koji je mapiran u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nenaplaćenu prodaju.</span><span class="sxs-lookup"><span data-stu-id="964c1-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="964c1-126">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-126">Fixed price</span></span>

<span data-ttu-id="964c1-127">Kada se prosleđena stavka troška poveže sa projektom koji se mapira na predmet ugovora o fiksnoj ceni, sistem kreira jednu stavku u glavnoj knjizi za troškove.</span><span class="sxs-lookup"><span data-stu-id="964c1-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="964c1-128">Podrazumevano određivanje cena</span><span class="sxs-lookup"><span data-stu-id="964c1-128">Default pricing</span></span>

<span data-ttu-id="964c1-129">Logika unošenja zadatih cena za troškove zasniva se na kategoriji troškova.</span><span class="sxs-lookup"><span data-stu-id="964c1-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="964c1-130">Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="964c1-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="964c1-131">Polja koja utiču na podrazumevane cene, kao što su **Kategorija transakcije** i **Jedinica**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="964c1-132">Međutim, to funkcioniše samo kada je metoda određivanja cena u cenovniku **Cena po jedinici**.</span><span class="sxs-lookup"><span data-stu-id="964c1-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="964c1-133">Ako je metoda određivanja cena **Po ceni** ili **Provizija preko troškova**, cena koja se unosi kada se kreira stavka troškova koristi se kao trošak, a cena stavke u glavnoj knjizi prodaje izračunava se na osnovu metode određivanja cena.</span><span class="sxs-lookup"><span data-stu-id="964c1-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="964c1-134">Na stavku troškova možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="964c1-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="964c1-135">Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="964c1-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="964c1-136">Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija.</span><span class="sxs-lookup"><span data-stu-id="964c1-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="964c1-137">Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="964c1-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="964c1-138">Stavke u glavnoj knjizi i prosleđivanje evidencije upotrebe materijala</span><span class="sxs-lookup"><span data-stu-id="964c1-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="964c1-139">Za više informacija o stavci troškova, pogledajte [Dnevnik upotrebe materijala](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="964c1-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="964c1-140">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="964c1-140">Time and materials</span></span>

<span data-ttu-id="964c1-141">Kada se prosleđena stavka evidencije upotrebe materijala poveže sa projektom koji se mapira u predmet ugovora o vremenu i materijalima, sistem kreira dve stavke u glavnoj knjizi, jednu za troškove i jednu za nefakturisanu prodaju.</span><span class="sxs-lookup"><span data-stu-id="964c1-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="964c1-142">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-142">Fixed price</span></span>

<span data-ttu-id="964c1-143">Kada se prosleđena stavka evidencije upotrebe materijala poveže sa projektom koji se mapira na predmet ugovora o fiksnoj ceni, sistem kreira jednu stavku u glavnoj knjizi za troškove.</span><span class="sxs-lookup"><span data-stu-id="964c1-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="964c1-144">Podrazumevano određivanje cena</span><span class="sxs-lookup"><span data-stu-id="964c1-144">Default pricing</span></span>

<span data-ttu-id="964c1-145">Logika unošenja zadatih cena materijala zasniva se na kombinaciji proizvoda i jedinice.</span><span class="sxs-lookup"><span data-stu-id="964c1-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="964c1-146">Datum transakcije, predmet ugovora na koji je projekat mapiran i valuta se koriste za određivanje odgovarajućeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="964c1-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="964c1-147">Polja koja utiču na podrazumevane cene, kao što su **ID proizvoda** i **Jedinica**, koriste se za utvrđivanje odgovarajuće cene u stavki u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="964c1-148">Međutim, ovo važi samo za kataloške proizvode.</span><span class="sxs-lookup"><span data-stu-id="964c1-148">However, this only works for catalog products.</span></span> <span data-ttu-id="964c1-149">Za proizvode koji se dodaju ručno, cena koja se unosi kada se kreira stavka evidencije upotrebe materijala koristi se za troškove i prodajnu cenu u stavkama u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="964c1-150">Na stavku **Evidencija upotrebe materijala** možete dodati prilagođeno polje.</span><span class="sxs-lookup"><span data-stu-id="964c1-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="964c1-151">Ako želite da se vrednost polja širi na trenutno stanje, kreirajte polje u tabelama **Trenutno stanje** i **Stavka u glavnoj knjizi**.</span><span class="sxs-lookup"><span data-stu-id="964c1-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="964c1-152">Koristite prilagođeni kôd za širenje izabrane vrednosti polja iz stavku vremena u trenutno stanje putem stavke u glavnoj knjizi koristeći poreklo transakcija.</span><span class="sxs-lookup"><span data-stu-id="964c1-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="964c1-153">Za više informacija o poreklu transakcija i vezama, pogledajte [Povezivanje trenutnog stanja sa originalnim zapisima](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="964c1-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="964c1-154">Korišćenje dnevnika za knjiženje za evidentiranje troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-154">Use entry journals to record costs</span></span>

<span data-ttu-id="964c1-155">Možete da koristite dnevnike za knjiženje da evidentirate troškove ili prihod u klasama materijala, naknade, vremena, troškova ili poreskih transakcija.</span><span class="sxs-lookup"><span data-stu-id="964c1-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="964c1-156">Dnevnici se mogu koristiti u sledeće svrhe:</span><span class="sxs-lookup"><span data-stu-id="964c1-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="964c1-157">Premestite stvarne vrednosti transakcija iz drugog sistema u Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="964c1-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="964c1-158">Evidentirajte troškove koji su se dogodili u drugom sistemu.</span><span class="sxs-lookup"><span data-stu-id="964c1-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="964c1-159">Ovi troškovi mogu uključivati troškove nabavke ili podugovaranja.</span><span class="sxs-lookup"><span data-stu-id="964c1-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="964c1-160">Aplikacija ne potvrđuje tip stavke u glavnoj knjizi ili povezano određivanje cena koje se unosi u stavku u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="964c1-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="964c1-161">Stoga samo korisnik koji je potpuno svestan računovodstvenog uticaja koji stvarne vrednosti imaju na projekat treba da koristi dnevnike za knjiženje za kreiranje stvarnih podataka.</span><span class="sxs-lookup"><span data-stu-id="964c1-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="964c1-162">Zbog uticaja ovog tipa dnevnika, pažljivo birajte ko ima pristup kreiranju dnevnika za knjiženje.</span><span class="sxs-lookup"><span data-stu-id="964c1-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="964c1-163">Evidentiranje stvarnih vrednosti na osnovu događaja u projektu</span><span class="sxs-lookup"><span data-stu-id="964c1-163">Record actuals based on project events</span></span>

<span data-ttu-id="964c1-164">Project Operations beleži finansijske transakcije koje se dešavaju tokom projekta.</span><span class="sxs-lookup"><span data-stu-id="964c1-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="964c1-165">Ove transakcije se evidentiraju kao stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="964c1-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="964c1-166">Sledeće tabele prikazuju različite vrste stvarnih vrednosti koje se kreiraju, zavisno od toga da li je projekat zasnovan na vremenu i materijalima ili projekat sa fiksnom cenom, da li je u fazi predprodaje ili je interni projekat.</span><span class="sxs-lookup"><span data-stu-id="964c1-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="964c1-167">Resurs pripada istoj organizacionoj jedinici kao i ugovorna jedinica projekta</span><span class="sxs-lookup"><span data-stu-id="964c1-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="964c1-168">Događaj</span><span class="sxs-lookup"><span data-stu-id="964c1-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="964c1-169">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="964c1-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="964c1-170">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="964c1-171">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="964c1-172">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="964c1-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="964c1-173">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="964c1-174">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-174">Actuals</span></span></th>
<th><span data-ttu-id="964c1-175">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="964c1-175">Transaction currency</span></span></th>
<th><span data-ttu-id="964c1-176">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-176">Fixed price</span></span></th>
<th><span data-ttu-id="964c1-177">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="964c1-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="964c1-178">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="964c1-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="964c1-179">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-180">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="964c1-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="964c1-181">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="964c1-182">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="964c1-183">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-183">Cost actual</span></span></td>
<td><span data-ttu-id="964c1-184">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-185">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-186">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="964c1-187">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-188">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-189">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="964c1-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="964c1-190">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="964c1-191">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="964c1-192">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-192">Cost actual</span></span></td>
<td><span data-ttu-id="964c1-193">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-194">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-195">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-196">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-197">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-198">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-199">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-200">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-201">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="964c1-202">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="964c1-203">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="964c1-204">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-205">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="964c1-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-206">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-207">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-208">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-209">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="964c1-209">Billed sales</span></span></td>
<td><span data-ttu-id="964c1-210">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="964c1-211">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="964c1-212">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="964c1-213">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-214">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-215">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-216">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-217">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-218">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-219">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-220">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-221">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="964c1-222">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="964c1-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="964c1-223">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="964c1-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="964c1-224">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="964c1-225">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="964c1-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="964c1-226">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="964c1-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="964c1-227">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-228">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-229">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-230">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="964c1-230">Billed sales</span></span></td>
<td><span data-ttu-id="964c1-231">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="964c1-232">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="964c1-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="964c1-233">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="964c1-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="964c1-234">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-235">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-236">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-237">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-238">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="964c1-239">Resurs pripada organizacionoj jedinici koja se razlikuje od ugovorne jedinice projekta</span><span class="sxs-lookup"><span data-stu-id="964c1-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="964c1-240">Događaj</span><span class="sxs-lookup"><span data-stu-id="964c1-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="964c1-241">Projekat koji se može naplatiti ili prodati</span><span class="sxs-lookup"><span data-stu-id="964c1-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="964c1-242">Projekat u fazi predprodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="964c1-243">Interni projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="964c1-244">Vreme i materijali</span><span class="sxs-lookup"><span data-stu-id="964c1-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="964c1-245">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="964c1-246">Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-246">Actuals</span></span></th>
<th><span data-ttu-id="964c1-247">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="964c1-247">Transaction currency</span></span></th>
<th><span data-ttu-id="964c1-248">Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="964c1-248">Fixed price</span></span></th>
<th><span data-ttu-id="964c1-249">Valuta transakcije</span><span class="sxs-lookup"><span data-stu-id="964c1-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="964c1-250">Stavka vremena je kreirana.</span><span class="sxs-lookup"><span data-stu-id="964c1-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="964c1-251">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-252">Stavka vremena je prosleđena.</span><span class="sxs-lookup"><span data-stu-id="964c1-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="964c1-253">Nema aktivnosti u entitetu Stvarne vrednosti</span><span class="sxs-lookup"><span data-stu-id="964c1-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="964c1-254">Vreme je odobreno, a tokom odobravanja ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="964c1-255">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-255">Cost actual</span></span></td>
<td><span data-ttu-id="964c1-256">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="964c1-257">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="964c1-258">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="964c1-259">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="964c1-260">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-261">Nenaplaćene stvarne vrednosti prodaje – Naplativo</span><span class="sxs-lookup"><span data-stu-id="964c1-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="964c1-262">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-263">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="964c1-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="964c1-264">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="964c1-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-265">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="964c1-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="964c1-266">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="964c1-267">Vreme je odobreno, a tokom odobravanja dolazi do smanjenja broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="964c1-268">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-268">Cost actual</span></span></td>
<td><span data-ttu-id="964c1-269">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-270">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-271">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-272">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-273">Stvarna vrednost troškova</span><span class="sxs-lookup"><span data-stu-id="964c1-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-274">Troškovi jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="964c1-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="964c1-275">Valuta jedinice za obezbeđivanje resursa</span><span class="sxs-lookup"><span data-stu-id="964c1-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-276">Prodaja između organizacija</span><span class="sxs-lookup"><span data-stu-id="964c1-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="964c1-277">Ugovorna valuta jedinice</span><span class="sxs-lookup"><span data-stu-id="964c1-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-278">Nenaplaćene stvarne vrednosti prodaje – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-279">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-280">Nenaplaćene stvarne vrednosti prodaje – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-281">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="964c1-282">Faktura je odobrena, a ne može da se promeni ili poveća broj sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="964c1-283">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="964c1-284">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-285">Naplaćena prodaja za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="964c1-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-286">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-287">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="964c1-288">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-289">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="964c1-289">Billed sales</span></span></td>
<td><span data-ttu-id="964c1-290">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="964c1-291">Faktura je odobrena i dolazi do smanjenja broja sati za naplatu.</span><span class="sxs-lookup"><span data-stu-id="964c1-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="964c1-292">Storniranje nenaplaćene prodaje</span><span class="sxs-lookup"><span data-stu-id="964c1-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="964c1-293">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-294">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-295">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-296">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="964c1-297">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-298">Naplaćena prodaja – naplativo za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-299">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-300">Naplaćena prodaja – ne može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-301">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="964c1-302">Faktura se ispravlja da bi se povećala naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="964c1-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="964c1-303">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="964c1-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="964c1-304">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="964c1-305">Storniranje naplaćene prodaje za kontrolnu tačku</span><span class="sxs-lookup"><span data-stu-id="964c1-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="964c1-306">Promena statusa kontrolne tačke sa <strong>Fakturirano</strong> na <strong>Spremno za fakturisanje</strong></span><span class="sxs-lookup"><span data-stu-id="964c1-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="964c1-307">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-308">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="964c1-309">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="964c1-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-310">Naplaćena prodaja</span><span class="sxs-lookup"><span data-stu-id="964c1-310">Billed sales</span></span></td>
<td><span data-ttu-id="964c1-311">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="964c1-312">Faktura se ispravlja da bi se smanjila naplativa količina.</span><span class="sxs-lookup"><span data-stu-id="964c1-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="964c1-313">Naplaćena prodaja – Storniranje</span><span class="sxs-lookup"><span data-stu-id="964c1-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="964c1-314">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-315">Naplaćena prodaja za novu količinu</span><span class="sxs-lookup"><span data-stu-id="964c1-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="964c1-316">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="964c1-317">Nenaplaćena prodaja – može da se naplati za razliku</span><span class="sxs-lookup"><span data-stu-id="964c1-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="964c1-318">Ugovorna valuta za projekat</span><span class="sxs-lookup"><span data-stu-id="964c1-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
