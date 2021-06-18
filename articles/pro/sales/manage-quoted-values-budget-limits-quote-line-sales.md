---
title: Pregled stavki ponude zasnovane na projektu
description: Ova tema pruža informacije o korišćenju stavki ponude zasnovanim na projektu za rad na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994873"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="71657-103">Pregled stavki ponude zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="71657-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="71657-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="71657-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="71657-105">Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju.</span><span class="sxs-lookup"><span data-stu-id="71657-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="71657-106">Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="71657-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="71657-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="71657-107">Billing Method</span></span>
- <span data-ttu-id="71657-108">Mapiranje projekata i zadataka</span><span class="sxs-lookup"><span data-stu-id="71657-108">Project and Task Mapping</span></span>
- <span data-ttu-id="71657-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="71657-109">Included Transaction classes</span></span>
- <span data-ttu-id="71657-110">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="71657-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="71657-111">Podešavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="71657-111">Chargeability setup</span></span>
- <span data-ttu-id="71657-112">Procena pomoću detalja stavki ponude</span><span class="sxs-lookup"><span data-stu-id="71657-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="71657-113">Klijenti stavki ponude</span><span class="sxs-lookup"><span data-stu-id="71657-113">Quote line Customers</span></span>

<span data-ttu-id="71657-114">Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="71657-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="71657-115">Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="71657-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="71657-116">**Polje**</span><span class="sxs-lookup"><span data-stu-id="71657-116">**Field**</span></span> | <span data-ttu-id="71657-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="71657-117">**Description**</span></span> | <span data-ttu-id="71657-118">**Posledični uticaj**</span><span class="sxs-lookup"><span data-stu-id="71657-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="71657-119">+Ime</span><span class="sxs-lookup"><span data-stu-id="71657-119">Name</span></span> | <span data-ttu-id="71657-120">Naziv ponude koji vam pomaže da prepoznate diskretnu komponentu ponude koja se procenjuje.</span><span class="sxs-lookup"><span data-stu-id="71657-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="71657-121">Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="71657-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-122">Način naplate</span><span class="sxs-lookup"><span data-stu-id="71657-122">Billing Method</span></span> | <span data-ttu-id="71657-123">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="71657-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="71657-124">Ovo polje uključuje dva glavna modela ugovaranja koje Dynamics 365 Project Operations podržava:</span><span class="sxs-lookup"><span data-stu-id="71657-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="71657-125">- Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="71657-125">- Fixed price</span></span></br><span data-ttu-id="71657-126">- Vreme i materijal.</span><span class="sxs-lookup"><span data-stu-id="71657-126">- Time and material.</span></span>| <span data-ttu-id="71657-127">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-128">Project</span><span class="sxs-lookup"><span data-stu-id="71657-128">Project</span></span> | <span data-ttu-id="71657-129">Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju.</span><span class="sxs-lookup"><span data-stu-id="71657-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="71657-130">Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="71657-131">Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="71657-132">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="71657-133">Obuhvaćeni zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-133">Included Tasks</span></span> | <span data-ttu-id="71657-134">Označava da li se ova stavka ponude koristi za sve ili neke projektne zadatke za izabrani projekat.</span><span class="sxs-lookup"><span data-stu-id="71657-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="71657-135">Ovo polje podložno uređivanju ima sledeće moguće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="71657-135">This field has the following possible values:</span></span></br><span data-ttu-id="71657-136">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-136">- All project tasks</span></span></br><span data-ttu-id="71657-137">- Samo izabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-137">- Selected project tasks only</span></span></br><span data-ttu-id="71657-138">Prazna vrednost u ovom polju je ekvivalentna opciji **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="71657-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="71657-139">Kada se na stranici projekta izabere **Samo izabrani projektni zadaci**, kartica **Podešavanje naplate za zadatak** vam omogućava da izaberete određene zadatke da biste ih povezali sa ovom stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="71657-140">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-141">Sadrži vreme</span><span class="sxs-lookup"><span data-stu-id="71657-141">Include Time</span></span> | <span data-ttu-id="71657-142">Vrednost **Da**/**Ne** pokazuje da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-143">Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-144">Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71657-145">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-146">Sadrži trošak</span><span class="sxs-lookup"><span data-stu-id="71657-146">Include Expense</span></span> | <span data-ttu-id="71657-147">Vrednost **Da**/**Ne** pokazuje da li će cena troškova na izabranom projektu biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-148">Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-149">Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71657-150">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-151">Sadrži materijal</span><span class="sxs-lookup"><span data-stu-id="71657-151">Include Material</span></span> | <span data-ttu-id="71657-152">Vrednost **Da**/**Ne** pokazuje da li će cena materijala na izabranom projektu biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-153">Vrednost **Ne** pokazuje da cena materijala neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-154">Vrednost **Da** pokazuje da cena materijala neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71657-155">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-156">Sadrži nadoknadu</span><span class="sxs-lookup"><span data-stu-id="71657-156">Include Fee</span></span> | <span data-ttu-id="71657-157">Vrednost **Da**/**Ne** pokazuje da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-158">Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="71657-159">Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="71657-160">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-161">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="71657-161">Quoted Amount</span></span> | <span data-ttu-id="71657-162">Ovo je iznos koji će biti naveden klijentu za sve radove predviđene na ovoj stavci ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="71657-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="71657-163">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="71657-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="71657-164">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="71657-165">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-166">Procenjeni porez</span><span class="sxs-lookup"><span data-stu-id="71657-166">Estimated Tax</span></span> | <span data-ttu-id="71657-167">To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="71657-168">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="71657-169">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-170">Ponuđeni oporezovani iznos</span><span class="sxs-lookup"><span data-stu-id="71657-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="71657-171">Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="71657-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="71657-172">Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="71657-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="71657-173">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-174">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="71657-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="71657-175">Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="71657-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="71657-176">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="71657-177">Budžet klijenta</span><span class="sxs-lookup"><span data-stu-id="71657-177">Customer Budget</span></span> | <span data-ttu-id="71657-178">Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="71657-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="71657-179">Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.</span><span class="sxs-lookup"><span data-stu-id="71657-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="71657-180">Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="71657-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="71657-181">**1. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je podešeno na **Svi projektni zadaci**, projekat je uključen u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="71657-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="71657-182">**2. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni samo u jednu stavku ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="71657-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="71657-183">**3. pravilo**: Ako je polje **Uključeni zadaci** postavljeno na **Samo izabrani projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni u više stavki ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="71657-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="71657-184">**4. pravilo**: Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="71657-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="71657-185">**5. pravilo**: Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="71657-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="71657-186">
                    <strong>Mogućnost za poslovanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="71657-187">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="71657-188">
                    <strong>Stavka ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="71657-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="71657-190">
                    <strong>Obuhvaćeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="71657-191">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="71657-192">
                    <strong>Sadrži trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="71657-193">
                    <strong>Sadrži materijal</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="71657-194">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="71657-195">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="71657-196">
                    <strong>Važi / Ne važi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="71657-197">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="71657-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-198">O1</span><span class="sxs-lookup"><span data-stu-id="71657-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-199">K1</span><span class="sxs-lookup"><span data-stu-id="71657-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-200">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-201">P1</span><span class="sxs-lookup"><span data-stu-id="71657-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-202">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-203">Da</span><span class="sxs-lookup"><span data-stu-id="71657-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-204">Da</span><span class="sxs-lookup"><span data-stu-id="71657-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-205">Da</span><span class="sxs-lookup"><span data-stu-id="71657-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-206">Da</span><span class="sxs-lookup"><span data-stu-id="71657-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-207">Ne važi</span><span class="sxs-lookup"><span data-stu-id="71657-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-208">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="71657-208">Violation of Rule #2.</span></span> <span data-ttu-id="71657-209">Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="71657-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-210">O1</span><span class="sxs-lookup"><span data-stu-id="71657-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-211">K1</span><span class="sxs-lookup"><span data-stu-id="71657-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-212">QL2</span><span class="sxs-lookup"><span data-stu-id="71657-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-213">P1</span><span class="sxs-lookup"><span data-stu-id="71657-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-214">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-215">Da</span><span class="sxs-lookup"><span data-stu-id="71657-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-216">Da</span><span class="sxs-lookup"><span data-stu-id="71657-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-217">Da</span><span class="sxs-lookup"><span data-stu-id="71657-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-218">Da</span><span class="sxs-lookup"><span data-stu-id="71657-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-219">O1</span><span class="sxs-lookup"><span data-stu-id="71657-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-220">K1</span><span class="sxs-lookup"><span data-stu-id="71657-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-221">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-222">P1</span><span class="sxs-lookup"><span data-stu-id="71657-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-224">Da</span><span class="sxs-lookup"><span data-stu-id="71657-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-225">No</span><span class="sxs-lookup"><span data-stu-id="71657-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-226">Da</span><span class="sxs-lookup"><span data-stu-id="71657-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-227">Da</span><span class="sxs-lookup"><span data-stu-id="71657-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-228">Ne važi</span><span class="sxs-lookup"><span data-stu-id="71657-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-229">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="71657-229">Violation of Rule #2.</span></span> <span data-ttu-id="71657-230">Vreme, materijal i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2</span><span class="sxs-lookup"><span data-stu-id="71657-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-231">O1</span><span class="sxs-lookup"><span data-stu-id="71657-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-232">K1</span><span class="sxs-lookup"><span data-stu-id="71657-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-233">QL2</span><span class="sxs-lookup"><span data-stu-id="71657-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-234">P1</span><span class="sxs-lookup"><span data-stu-id="71657-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-236">Da</span><span class="sxs-lookup"><span data-stu-id="71657-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-237">Da</span><span class="sxs-lookup"><span data-stu-id="71657-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-238">Da</span><span class="sxs-lookup"><span data-stu-id="71657-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-239">Da</span><span class="sxs-lookup"><span data-stu-id="71657-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-240">O1</span><span class="sxs-lookup"><span data-stu-id="71657-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-241">K1</span><span class="sxs-lookup"><span data-stu-id="71657-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-242">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-243">P1</span><span class="sxs-lookup"><span data-stu-id="71657-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-244">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-245">Da</span><span class="sxs-lookup"><span data-stu-id="71657-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-246">No</span><span class="sxs-lookup"><span data-stu-id="71657-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-247">Da</span><span class="sxs-lookup"><span data-stu-id="71657-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-248">Da</span><span class="sxs-lookup"><span data-stu-id="71657-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-249">Važeće</span><span class="sxs-lookup"><span data-stu-id="71657-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-250">Vreme, materijal i naknade za projekat P1 uključeni su u QL1</span><span class="sxs-lookup"><span data-stu-id="71657-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="71657-251">Troškovi za projekat P1 uključeni su u QL2</span><span class="sxs-lookup"><span data-stu-id="71657-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="71657-252">Nema preklapanja u onome što je uključeno u svaku stavku ponude i stoga je važeće.</span><span class="sxs-lookup"><span data-stu-id="71657-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-253">O1</span><span class="sxs-lookup"><span data-stu-id="71657-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-254">K1</span><span class="sxs-lookup"><span data-stu-id="71657-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-255">QL2</span><span class="sxs-lookup"><span data-stu-id="71657-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-256">P1</span><span class="sxs-lookup"><span data-stu-id="71657-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-257">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-258">No</span><span class="sxs-lookup"><span data-stu-id="71657-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-259">Da</span><span class="sxs-lookup"><span data-stu-id="71657-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-260">No</span><span class="sxs-lookup"><span data-stu-id="71657-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-261">No</span><span class="sxs-lookup"><span data-stu-id="71657-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-262">O1</span><span class="sxs-lookup"><span data-stu-id="71657-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-263">K1</span><span class="sxs-lookup"><span data-stu-id="71657-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-264">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-265">P1</span><span class="sxs-lookup"><span data-stu-id="71657-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-266">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-267">Da</span><span class="sxs-lookup"><span data-stu-id="71657-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-268">Da</span><span class="sxs-lookup"><span data-stu-id="71657-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-269">Da</span><span class="sxs-lookup"><span data-stu-id="71657-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-270">Da</span><span class="sxs-lookup"><span data-stu-id="71657-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-271">Ne važi</span><span class="sxs-lookup"><span data-stu-id="71657-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-272">Kršenje pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="71657-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="71657-273">Q1 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1</span><span class="sxs-lookup"><span data-stu-id="71657-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="71657-274">QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i stoga se preklapa sa onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="71657-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-275">O1</span><span class="sxs-lookup"><span data-stu-id="71657-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-276">K1</span><span class="sxs-lookup"><span data-stu-id="71657-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-277">QL2</span><span class="sxs-lookup"><span data-stu-id="71657-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-278">P1</span><span class="sxs-lookup"><span data-stu-id="71657-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-279">Prazno</span><span class="sxs-lookup"><span data-stu-id="71657-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-280">Da</span><span class="sxs-lookup"><span data-stu-id="71657-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-281">Da</span><span class="sxs-lookup"><span data-stu-id="71657-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-282">Da</span><span class="sxs-lookup"><span data-stu-id="71657-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-283">Da</span><span class="sxs-lookup"><span data-stu-id="71657-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-284">O1</span><span class="sxs-lookup"><span data-stu-id="71657-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-285">K1</span><span class="sxs-lookup"><span data-stu-id="71657-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-286">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-287">P1</span><span class="sxs-lookup"><span data-stu-id="71657-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-288">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-289">Da</span><span class="sxs-lookup"><span data-stu-id="71657-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-290">Da</span><span class="sxs-lookup"><span data-stu-id="71657-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-291">Da</span><span class="sxs-lookup"><span data-stu-id="71657-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-292">Da</span><span class="sxs-lookup"><span data-stu-id="71657-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-293">Važeće</span><span class="sxs-lookup"><span data-stu-id="71657-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-294">Po pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="71657-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="71657-295">Q1 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="71657-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="71657-296">QL2 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="71657-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="71657-297">Jedina dodatna provera valjanosti oko podskupa zadataka na QL1 koja se razlikuje od podskupa zadataka na QL2 kako bi se osiguralo da tamo nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="71657-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="71657-298">To sistem radi kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="71657-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-299">O1</span><span class="sxs-lookup"><span data-stu-id="71657-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-300">K1</span><span class="sxs-lookup"><span data-stu-id="71657-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-301">QL2</span><span class="sxs-lookup"><span data-stu-id="71657-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-302">P1</span><span class="sxs-lookup"><span data-stu-id="71657-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-303">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="71657-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-304">Da</span><span class="sxs-lookup"><span data-stu-id="71657-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-305">Da</span><span class="sxs-lookup"><span data-stu-id="71657-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-306">Da</span><span class="sxs-lookup"><span data-stu-id="71657-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-307">Da</span><span class="sxs-lookup"><span data-stu-id="71657-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-308">O1</span><span class="sxs-lookup"><span data-stu-id="71657-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-309">K1</span><span class="sxs-lookup"><span data-stu-id="71657-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-310">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-311">P1</span><span class="sxs-lookup"><span data-stu-id="71657-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-312">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="71657-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-313">Da</span><span class="sxs-lookup"><span data-stu-id="71657-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-314">Da</span><span class="sxs-lookup"><span data-stu-id="71657-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-315">Da</span><span class="sxs-lookup"><span data-stu-id="71657-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-316">Da</span><span class="sxs-lookup"><span data-stu-id="71657-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-317">Važeće</span><span class="sxs-lookup"><span data-stu-id="71657-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-318">Po pravilu br. 5, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da se mogu obe proceniti za iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="71657-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-319">O1</span><span class="sxs-lookup"><span data-stu-id="71657-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-320">K2</span><span class="sxs-lookup"><span data-stu-id="71657-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-321">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-322">P1</span><span class="sxs-lookup"><span data-stu-id="71657-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-323">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="71657-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-324">Da</span><span class="sxs-lookup"><span data-stu-id="71657-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-325">Da</span><span class="sxs-lookup"><span data-stu-id="71657-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-326">Da</span><span class="sxs-lookup"><span data-stu-id="71657-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-327">Da</span><span class="sxs-lookup"><span data-stu-id="71657-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-328">O1</span><span class="sxs-lookup"><span data-stu-id="71657-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-329">K1</span><span class="sxs-lookup"><span data-stu-id="71657-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-330">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-331">P1</span><span class="sxs-lookup"><span data-stu-id="71657-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-332">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="71657-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-333">Da</span><span class="sxs-lookup"><span data-stu-id="71657-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-334">Da</span><span class="sxs-lookup"><span data-stu-id="71657-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-335">Da</span><span class="sxs-lookup"><span data-stu-id="71657-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-336">Da</span><span class="sxs-lookup"><span data-stu-id="71657-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-337">Ne važi</span><span class="sxs-lookup"><span data-stu-id="71657-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="71657-338">Po pravilu br. 4, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da se ne mogu proceniti za iste komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="71657-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="71657-339">O2</span><span class="sxs-lookup"><span data-stu-id="71657-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="71657-340">K1</span><span class="sxs-lookup"><span data-stu-id="71657-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="71657-341">QL1</span><span class="sxs-lookup"><span data-stu-id="71657-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-342">P1</span><span class="sxs-lookup"><span data-stu-id="71657-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="71657-343">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="71657-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="71657-344">Da</span><span class="sxs-lookup"><span data-stu-id="71657-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="71657-345">Da</span><span class="sxs-lookup"><span data-stu-id="71657-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="71657-346">Da</span><span class="sxs-lookup"><span data-stu-id="71657-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="71657-347">Da</span><span class="sxs-lookup"><span data-stu-id="71657-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
