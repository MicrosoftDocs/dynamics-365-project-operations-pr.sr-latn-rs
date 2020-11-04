---
title: Stavke ponude zasnovane na projektu
description: Ova tema pruža informacije o korišćenju stavki ponude zasnovanim na projektu za rad na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083447"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="db50e-103">Stavke ponude zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="db50e-103">Project-based quote lines</span></span>

<span data-ttu-id="db50e-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="db50e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="db50e-105">Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju.</span><span class="sxs-lookup"><span data-stu-id="db50e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="db50e-106">Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="db50e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="db50e-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="db50e-107">Billing Method</span></span>
- <span data-ttu-id="db50e-108">Mapiranje projekata</span><span class="sxs-lookup"><span data-stu-id="db50e-108">Project Mapping</span></span>
- <span data-ttu-id="db50e-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="db50e-109">Included Transaction classes</span></span>
- <span data-ttu-id="db50e-110">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="db50e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="db50e-111">Podešavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="db50e-111">Chargeability setup</span></span>
- <span data-ttu-id="db50e-112">Procena pomoću detalja stavki ponude</span><span class="sxs-lookup"><span data-stu-id="db50e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="db50e-113">Klijenti stavki ponude</span><span class="sxs-lookup"><span data-stu-id="db50e-113">Quote line Customers</span></span>

<span data-ttu-id="db50e-114">Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="db50e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="db50e-115">Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="db50e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="db50e-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="db50e-116">**Field**</span></span> | <span data-ttu-id="db50e-117">**Relevantnost, svrha i smernice**</span><span class="sxs-lookup"><span data-stu-id="db50e-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="db50e-118">**Posledični uticaj**</span><span class="sxs-lookup"><span data-stu-id="db50e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="db50e-119">+Ime</span><span class="sxs-lookup"><span data-stu-id="db50e-119">Name</span></span> | <span data-ttu-id="db50e-120">Naziv stavke ponude koja bi trebalo da vam pomogne da identifikujete diskretnu komponentu ponude koja se procenjuje.</span><span class="sxs-lookup"><span data-stu-id="db50e-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="db50e-121">Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="db50e-122">Billing Method</span></span> | <span data-ttu-id="db50e-123">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="db50e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="db50e-124">Ovo polje obuhvata dva glavna modela ugovaranja koje podržava Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="db50e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="db50e-125">- Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="db50e-125">- Fixed price</span></span></br><span data-ttu-id="db50e-126">- Vreme i materijal.</span><span class="sxs-lookup"><span data-stu-id="db50e-126">- Time and material.</span></span>| <span data-ttu-id="db50e-127">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-128">Project</span><span class="sxs-lookup"><span data-stu-id="db50e-128">Project</span></span> | <span data-ttu-id="db50e-129">Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju.</span><span class="sxs-lookup"><span data-stu-id="db50e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="db50e-130">Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="db50e-131">Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="db50e-132">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-133">Sadrži vreme</span><span class="sxs-lookup"><span data-stu-id="db50e-133">Include Time</span></span> | <span data-ttu-id="db50e-134">Zastavica **Da**/**Ne** označava da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-135">Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-136">Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db50e-137">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-138">Sadrži trošak</span><span class="sxs-lookup"><span data-stu-id="db50e-138">Include Expense</span></span> | <span data-ttu-id="db50e-139">Zastavica **Da**/**Ne** označava da li će cene troškova na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-140">Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-141">Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db50e-142">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-143">Sadrži nadoknadu</span><span class="sxs-lookup"><span data-stu-id="db50e-143">Include Fee</span></span> | <span data-ttu-id="db50e-144">Zastavica **Da**/**Ne** označava da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-145">Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="db50e-146">Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="db50e-147">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-148">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="db50e-148">Quoted Amount</span></span> | <span data-ttu-id="db50e-149">Ovo je iznos koji će biti naveden klijentu za sve radove predviđene u ovoj stavci ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="db50e-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="db50e-150">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="db50e-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="db50e-151">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="db50e-152">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-153">Procenjeni porez</span><span class="sxs-lookup"><span data-stu-id="db50e-153">Estimated Tax</span></span> | <span data-ttu-id="db50e-154">To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="db50e-155">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="db50e-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="db50e-156">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-157">Ponuđeni oporezovani iznos</span><span class="sxs-lookup"><span data-stu-id="db50e-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="db50e-158">Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="db50e-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="db50e-159">Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="db50e-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="db50e-160">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-161">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="db50e-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="db50e-162">Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="db50e-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="db50e-163">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="db50e-164">Budžet klijenta</span><span class="sxs-lookup"><span data-stu-id="db50e-164">Customer Budget</span></span> | <span data-ttu-id="db50e-165">Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="db50e-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="db50e-166">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="db50e-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="db50e-167">Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="db50e-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="db50e-168">**1. pravilo** : Određena klasa transakcija na izabranom projektu može se uključiti samo u jednu stavku ponude na osnovu projekta.</span><span class="sxs-lookup"><span data-stu-id="db50e-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="db50e-169">**2. pravilo** : Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="db50e-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="db50e-170">**3. pravilo** : Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="db50e-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="db50e-171">
                    <strong>Mogućnost za poslovanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="db50e-172">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db50e-173">
                    <strong>Stavka ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db50e-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="db50e-175">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="db50e-176">
                    <strong>Sadrži trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="db50e-177">
                    <strong>Umetanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="db50e-178">
                    <strong>naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="db50e-179">
                    <strong>Važi / Ne važi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="db50e-180">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="db50e-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-181">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-182">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-183">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-184">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-185">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-186">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-187">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-188">Ne važi</span><span class="sxs-lookup"><span data-stu-id="db50e-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-189">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="db50e-189">Violation of Rule #1.</span></span> <span data-ttu-id="db50e-190">Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="db50e-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-191">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-192">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-193">QL2</span><span class="sxs-lookup"><span data-stu-id="db50e-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-194">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-195">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-196">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-197">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-197">Yes</span></span> </p>
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
<span data-ttu-id="db50e-198">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-199">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-200">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-201">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-202">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-203">No</span><span class="sxs-lookup"><span data-stu-id="db50e-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-204">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-205">Ne važi</span><span class="sxs-lookup"><span data-stu-id="db50e-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-206">Kršenje pravila br. 1.</span><span class="sxs-lookup"><span data-stu-id="db50e-206">Violation of Rule #1.</span></span> <span data-ttu-id="db50e-207">Vreme i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="db50e-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-208">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-209">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-210">QL2</span><span class="sxs-lookup"><span data-stu-id="db50e-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-211">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-212">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-213">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-214">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-214">Yes</span></span> </p>
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
<span data-ttu-id="db50e-215">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-216">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-217">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-218">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-219">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-220">No</span><span class="sxs-lookup"><span data-stu-id="db50e-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-221">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-222">Važeći</span><span class="sxs-lookup"><span data-stu-id="db50e-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="db50e-223">Vreme i naknade za projekat P1 su uključeni u QL1.</span><span class="sxs-lookup"><span data-stu-id="db50e-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="db50e-224">Troškovi za projekat P1 uključeni su u QL2.</span><span class="sxs-lookup"><span data-stu-id="db50e-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="db50e-225">Nema preklapanja u onome što je uključeno u svaku stavku ponude, tako da je to važeće.</span><span class="sxs-lookup"><span data-stu-id="db50e-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-226">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-227">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-228">QL2</span><span class="sxs-lookup"><span data-stu-id="db50e-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-229">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-230">No</span><span class="sxs-lookup"><span data-stu-id="db50e-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-231">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-232">No</span><span class="sxs-lookup"><span data-stu-id="db50e-232">No</span></span> </p>
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
<span data-ttu-id="db50e-233">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-234">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-235">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-236">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-237">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-238">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-239">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-240">Ne važi</span><span class="sxs-lookup"><span data-stu-id="db50e-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-241">Kršenje gorenavedenog pravila br. 1</span><span class="sxs-lookup"><span data-stu-id="db50e-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="db50e-242">Q1 uključuje vreme, troškove i naknade za ceo projekat P1.</span><span class="sxs-lookup"><span data-stu-id="db50e-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="db50e-243">QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i preklapa se sa onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="db50e-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-244">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-245">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-246">QL2</span><span class="sxs-lookup"><span data-stu-id="db50e-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-247">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-248">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-249">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-250">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-250">Yes</span></span> </p>
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
<span data-ttu-id="db50e-251">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-252">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-253">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-254">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-255">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-256">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-257">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db50e-258">Važeći</span><span class="sxs-lookup"><span data-stu-id="db50e-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-259">Na osnovu pravila br. 2, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da obe mogu proceniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="db50e-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-260">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-261">K2</span><span class="sxs-lookup"><span data-stu-id="db50e-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-262">QL1 na Q2</span><span class="sxs-lookup"><span data-stu-id="db50e-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-263">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-264">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-265">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-266">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-266">Yes</span></span> </p>
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
<span data-ttu-id="db50e-267">O1</span><span class="sxs-lookup"><span data-stu-id="db50e-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-268">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-269">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-270">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-271">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-272">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-273">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db50e-274">Važeći</span><span class="sxs-lookup"><span data-stu-id="db50e-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="db50e-275">Na osnovu pravila br. 3, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da one ne mogu proceniti komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="db50e-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="db50e-276">O2</span><span class="sxs-lookup"><span data-stu-id="db50e-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="db50e-277">K1</span><span class="sxs-lookup"><span data-stu-id="db50e-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-278">QL1</span><span class="sxs-lookup"><span data-stu-id="db50e-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-279">P1</span><span class="sxs-lookup"><span data-stu-id="db50e-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-280">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="db50e-281">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="db50e-282">Da</span><span class="sxs-lookup"><span data-stu-id="db50e-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="db50e-283">Ne važi</span><span class="sxs-lookup"><span data-stu-id="db50e-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

