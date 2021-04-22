---
title: Pregled stavki ponude za projekat
description: Ova tema pruža informacije o korišćenju stavki ponude za projekat za rad na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa48a90c275eae1b0c0dbce685ae718dd9674c88
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858049"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="d9445-103">Pregled stavki ponude za projekat</span><span class="sxs-lookup"><span data-stu-id="d9445-103">Project quote lines overview</span></span>

<span data-ttu-id="d9445-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="d9445-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d9445-105">Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju.</span><span class="sxs-lookup"><span data-stu-id="d9445-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d9445-106">Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="d9445-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d9445-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="d9445-107">Billing Method</span></span>
- <span data-ttu-id="d9445-108">Mapiranje projekata</span><span class="sxs-lookup"><span data-stu-id="d9445-108">Project Mapping</span></span>
- <span data-ttu-id="d9445-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="d9445-109">Included Transaction classes</span></span>
- <span data-ttu-id="d9445-110">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="d9445-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d9445-111">Podešavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="d9445-111">Chargeability setup</span></span>
- <span data-ttu-id="d9445-112">Procena pomoću detalja stavki ponude</span><span class="sxs-lookup"><span data-stu-id="d9445-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d9445-113">Klijenti stavki ponude</span><span class="sxs-lookup"><span data-stu-id="d9445-113">Quote line Customers</span></span>

<span data-ttu-id="d9445-114">Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="d9445-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d9445-115">Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="d9445-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d9445-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="d9445-116">**Field**</span></span> | <span data-ttu-id="d9445-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="d9445-117">**Description**</span></span> | <span data-ttu-id="d9445-118">**Posledični uticaj**</span><span class="sxs-lookup"><span data-stu-id="d9445-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d9445-119">Imenuj</span><span class="sxs-lookup"><span data-stu-id="d9445-119">Name</span></span> | <span data-ttu-id="d9445-120">Naziv stavke ponude koja bi trebalo da vam pomogne da identifikujete diskretnu komponentu ponude koja se procenjuje.</span><span class="sxs-lookup"><span data-stu-id="d9445-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d9445-121">Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="d9445-122">Billing Method</span></span> | <span data-ttu-id="d9445-123">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="d9445-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d9445-124">Ovo polje uključuje dva glavna modela ugovaranja koje Dynamics 365 Project Operations podržava:</span><span class="sxs-lookup"><span data-stu-id="d9445-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d9445-125">- Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="d9445-125">- Fixed price</span></span></br><span data-ttu-id="d9445-126">- Vreme i materijal.</span><span class="sxs-lookup"><span data-stu-id="d9445-126">- Time and material.</span></span>| <span data-ttu-id="d9445-127">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-128">Project</span><span class="sxs-lookup"><span data-stu-id="d9445-128">Project</span></span> | <span data-ttu-id="d9445-129">Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju.</span><span class="sxs-lookup"><span data-stu-id="d9445-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d9445-130">Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d9445-131">Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d9445-132">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-133">Sadrži vreme</span><span class="sxs-lookup"><span data-stu-id="d9445-133">Include Time</span></span> | <span data-ttu-id="d9445-134">Zastavica **Da**/**Ne** označava da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-135">Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-136">Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9445-137">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-138">Sadrži trošak</span><span class="sxs-lookup"><span data-stu-id="d9445-138">Include Expense</span></span> | <span data-ttu-id="d9445-139">Zastavica **Da**/**Ne** označava da li će cene troškova na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-140">Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-141">Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9445-142">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-143">Sadrži nadoknadu</span><span class="sxs-lookup"><span data-stu-id="d9445-143">Include Fee</span></span> | <span data-ttu-id="d9445-144">Zastavica **Da**/**Ne** označava da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-145">Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d9445-146">Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d9445-147">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-148">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="d9445-148">Quoted Amount</span></span> | <span data-ttu-id="d9445-149">Ovo je iznos koji će biti naveden klijentu za sve radove predviđene u ovoj stavci ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="d9445-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d9445-150">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="d9445-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d9445-151">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d9445-152">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-153">Procenjeni porez</span><span class="sxs-lookup"><span data-stu-id="d9445-153">Estimated Tax</span></span> | <span data-ttu-id="d9445-154">To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d9445-155">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="d9445-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d9445-156">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-157">Ponuđeni oporezovani iznos</span><span class="sxs-lookup"><span data-stu-id="d9445-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="d9445-158">Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="d9445-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d9445-159">Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="d9445-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d9445-160">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-161">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="d9445-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="d9445-162">Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="d9445-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d9445-163">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d9445-164">Budžet klijenta</span><span class="sxs-lookup"><span data-stu-id="d9445-164">Customer Budget</span></span> | <span data-ttu-id="d9445-165">Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="d9445-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d9445-166">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="d9445-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d9445-167">Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="d9445-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d9445-168">**1. pravilo**: Određena klasa transakcija na izabranom projektu može se uključiti samo u jednu stavku ponude na osnovu projekta.</span><span class="sxs-lookup"><span data-stu-id="d9445-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d9445-169">**2. pravilo**: Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="d9445-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d9445-170">**3. pravilo**: Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="d9445-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d9445-171">
                    <strong>Mogućnost za poslovanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d9445-172">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9445-173">
                    <strong>Stavka ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9445-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9445-175">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d9445-176">
                    <strong>Sadrži trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d9445-177">
                    <strong>Umetanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d9445-178">
                    <strong>naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d9445-179">
                    <strong>Važi / Ne važi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d9445-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d9445-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-181">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-182">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-183">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-184">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-185">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-186">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-187">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-188">Ne važi</span><span class="sxs-lookup"><span data-stu-id="d9445-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-189">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="d9445-189">Violation of Rule #1.</span></span> <span data-ttu-id="d9445-190">Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="d9445-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-191">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-192">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-193">QL2</span><span class="sxs-lookup"><span data-stu-id="d9445-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-194">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-195">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-196">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-197">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-198">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-199">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-200">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-201">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-202">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-203">No</span><span class="sxs-lookup"><span data-stu-id="d9445-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-204">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-205">Ne važi</span><span class="sxs-lookup"><span data-stu-id="d9445-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-206">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="d9445-206">Violation of Rule #1.</span></span> <span data-ttu-id="d9445-207">Vreme i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="d9445-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-208">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-209">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-210">QL2</span><span class="sxs-lookup"><span data-stu-id="d9445-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-211">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-212">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-213">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-214">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-215">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-216">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-217">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-218">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-219">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-220">No</span><span class="sxs-lookup"><span data-stu-id="d9445-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-221">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-222">Važeći</span><span class="sxs-lookup"><span data-stu-id="d9445-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="d9445-223">Vreme i naknade za projekat P1 su uključeni u QL1.</span><span class="sxs-lookup"><span data-stu-id="d9445-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d9445-224">Troškovi za projekat P1 uključeni su u QL2.</span><span class="sxs-lookup"><span data-stu-id="d9445-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d9445-225">Nema preklapanja u onome što je uključeno u svaku stavku ponude, tako da je to važeće.</span><span class="sxs-lookup"><span data-stu-id="d9445-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-226">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-227">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-228">QL2</span><span class="sxs-lookup"><span data-stu-id="d9445-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-229">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-230">No</span><span class="sxs-lookup"><span data-stu-id="d9445-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-231">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-232">No</span><span class="sxs-lookup"><span data-stu-id="d9445-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-233">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-234">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-235">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-236">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-237">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-238">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-239">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-240">Ne važi</span><span class="sxs-lookup"><span data-stu-id="d9445-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-241">Kršenje gorenavedenog pravila br. 1</span><span class="sxs-lookup"><span data-stu-id="d9445-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="d9445-242">Q1 uključuje vreme, troškove i naknade za ceo projekat P1.</span><span class="sxs-lookup"><span data-stu-id="d9445-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d9445-243">QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i preklapa se sa onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="d9445-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-244">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-245">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-246">QL2</span><span class="sxs-lookup"><span data-stu-id="d9445-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-247">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-248">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-249">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-250">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-251">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-252">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-254">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-255">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-256">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-257">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9445-258">Važeći</span><span class="sxs-lookup"><span data-stu-id="d9445-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-259">Na osnovu pravila br. 2, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da obe mogu proceniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="d9445-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-260">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-261">K2</span><span class="sxs-lookup"><span data-stu-id="d9445-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-262">QL1 na Q2</span><span class="sxs-lookup"><span data-stu-id="d9445-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-263">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-264">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-265">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-266">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-267">O1</span><span class="sxs-lookup"><span data-stu-id="d9445-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-268">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-269">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-270">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-271">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-272">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-273">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9445-274">Važeći</span><span class="sxs-lookup"><span data-stu-id="d9445-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d9445-275">Na osnovu pravila br. 3, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da one ne mogu proceniti komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="d9445-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d9445-276">O2</span><span class="sxs-lookup"><span data-stu-id="d9445-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d9445-277">K1</span><span class="sxs-lookup"><span data-stu-id="d9445-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-278">QL1</span><span class="sxs-lookup"><span data-stu-id="d9445-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-279">P1</span><span class="sxs-lookup"><span data-stu-id="d9445-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-280">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d9445-281">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d9445-282">Da</span><span class="sxs-lookup"><span data-stu-id="d9445-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d9445-283">Ne važi</span><span class="sxs-lookup"><span data-stu-id="d9445-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
