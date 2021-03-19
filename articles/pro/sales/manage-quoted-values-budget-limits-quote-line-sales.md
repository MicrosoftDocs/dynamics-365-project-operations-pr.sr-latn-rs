---
title: Pregled stavki ponude zasnovane na projektu – jednostavno
description: Ova tema pruža informacije o korišćenju stavki ponude zasnovanim na projektu za rad na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4865c06691fba09eacf5fe6449adfaf542444520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272990"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="6daba-104">Pregled stavki ponude zasnovane na projektu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="6daba-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="6daba-105">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="6daba-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6daba-106">Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju.</span><span class="sxs-lookup"><span data-stu-id="6daba-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6daba-107">Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="6daba-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6daba-108">Način naplate</span><span class="sxs-lookup"><span data-stu-id="6daba-108">Billing Method</span></span>
- <span data-ttu-id="6daba-109">Mapiranje projekata i zadataka</span><span class="sxs-lookup"><span data-stu-id="6daba-109">Project and Task Mapping</span></span>
- <span data-ttu-id="6daba-110">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="6daba-110">Included Transaction classes</span></span>
- <span data-ttu-id="6daba-111">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="6daba-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6daba-112">Podešavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="6daba-112">Chargeability setup</span></span>
- <span data-ttu-id="6daba-113">Procena pomoću detalja stavki ponude</span><span class="sxs-lookup"><span data-stu-id="6daba-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6daba-114">Klijenti stavki ponude</span><span class="sxs-lookup"><span data-stu-id="6daba-114">Quote line Customers</span></span>

<span data-ttu-id="6daba-115">Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="6daba-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6daba-116">Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.</span><span class="sxs-lookup"><span data-stu-id="6daba-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6daba-117">**Polje**</span><span class="sxs-lookup"><span data-stu-id="6daba-117">**Field**</span></span> | <span data-ttu-id="6daba-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="6daba-118">**Description**</span></span> | <span data-ttu-id="6daba-119">**Posledični uticaj**</span><span class="sxs-lookup"><span data-stu-id="6daba-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6daba-120">Imenuj</span><span class="sxs-lookup"><span data-stu-id="6daba-120">Name</span></span> | <span data-ttu-id="6daba-121">Naziv stavke ponude koja bi trebalo da vam pomogne da identifikujete diskretnu komponentu ponude koja se procenjuje.</span><span class="sxs-lookup"><span data-stu-id="6daba-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6daba-122">Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-123">Način naplate</span><span class="sxs-lookup"><span data-stu-id="6daba-123">Billing Method</span></span> | <span data-ttu-id="6daba-124">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="6daba-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6daba-125">Ovo polje uključuje dva glavna modela ugovaranja koje Dynamics 365 Project Operations podržava:</span><span class="sxs-lookup"><span data-stu-id="6daba-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6daba-126">- Fiksna cena</span><span class="sxs-lookup"><span data-stu-id="6daba-126">- Fixed price</span></span></br><span data-ttu-id="6daba-127">- Vreme i materijal.</span><span class="sxs-lookup"><span data-stu-id="6daba-127">- Time and material.</span></span>| <span data-ttu-id="6daba-128">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-129">Project</span><span class="sxs-lookup"><span data-stu-id="6daba-129">Project</span></span> | <span data-ttu-id="6daba-130">Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju.</span><span class="sxs-lookup"><span data-stu-id="6daba-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6daba-131">Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6daba-132">Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6daba-133">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="6daba-134">Obuhvaćeni zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-134">Included Tasks</span></span> | <span data-ttu-id="6daba-135">Označava da li se ova stavka ponude koristi za sve ili neke projektne zadatke za izabrani projekat.</span><span class="sxs-lookup"><span data-stu-id="6daba-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="6daba-136">Ovo polje podložno uređivanju ima sledeće moguće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="6daba-136">This field has the following possible values:</span></span></br><span data-ttu-id="6daba-137">- Svi projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-137">- All project tasks</span></span></br><span data-ttu-id="6daba-138">- Samo izabrani projektni zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-138">- Selected project tasks only</span></span></br><span data-ttu-id="6daba-139">Prazna vrednost u ovom polju je ekvivalentna opciji **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="6daba-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="6daba-140">Kada je na stranici projekta izabrana opcija **Samo izabrani projektni zadaci**, kartica **Postavljanje zadatka za obračun** omogućava vam da izaberete određene zadatke da biste ih povezali sa ovom stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="6daba-141">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-142">Sadrži vreme</span><span class="sxs-lookup"><span data-stu-id="6daba-142">Include Time</span></span> | <span data-ttu-id="6daba-143">Zastavica **Da**/**Ne** označava da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-144">Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-145">Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6daba-146">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-147">Sadrži trošak</span><span class="sxs-lookup"><span data-stu-id="6daba-147">Include Expense</span></span> | <span data-ttu-id="6daba-148">Zastavica **Da**/**Ne** označava da li će cene troškova na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-149">Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-150">Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6daba-151">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-152">Sadrži nadoknadu</span><span class="sxs-lookup"><span data-stu-id="6daba-152">Include Fee</span></span> | <span data-ttu-id="6daba-153">Zastavica **Da**/**Ne** označava da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-154">Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6daba-155">Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6daba-156">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-157">Ponuđeni iznos</span><span class="sxs-lookup"><span data-stu-id="6daba-157">Quoted Amount</span></span> | <span data-ttu-id="6daba-158">Ovo je iznos koji će biti naveden klijentu za sve radove predviđene u ovoj stavci ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="6daba-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6daba-159">U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="6daba-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6daba-160">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6daba-161">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-162">Procenjeni porez</span><span class="sxs-lookup"><span data-stu-id="6daba-162">Estimated Tax</span></span> | <span data-ttu-id="6daba-163">To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6daba-164">Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6daba-165">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-166">Ponuđeni oporezovani iznos</span><span class="sxs-lookup"><span data-stu-id="6daba-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="6daba-167">Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje.</span><span class="sxs-lookup"><span data-stu-id="6daba-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6daba-168">Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*.</span><span class="sxs-lookup"><span data-stu-id="6daba-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6daba-169">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-170">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="6daba-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="6daba-171">Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**.</span><span class="sxs-lookup"><span data-stu-id="6daba-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6daba-172">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6daba-173">Budžet klijenta</span><span class="sxs-lookup"><span data-stu-id="6daba-173">Customer Budget</span></span> | <span data-ttu-id="6daba-174">Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="6daba-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6daba-175">Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari.</span><span class="sxs-lookup"><span data-stu-id="6daba-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6daba-176">Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="6daba-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6daba-177">**1. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je podešeno na **Svi projektni zadaci**, projekat je uključen u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="6daba-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="6daba-178">**2. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni samo u jednu stavku ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="6daba-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6daba-179">**3. pravilo**: Ako je polje **Uključeni zadaci** postavljeno na **Samo izabrani projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni u više stavki ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="6daba-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="6daba-180">**4. pravilo**: Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="6daba-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6daba-181">**5. pravilo**: Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.</span><span class="sxs-lookup"><span data-stu-id="6daba-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="6daba-182">
                    <strong>Mogućnost za poslovanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6daba-183">
                    <strong>Ponuda</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6daba-184">
                    <strong>Stavka ponude</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6daba-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="6daba-186">
                    <strong>Obuhvaćeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6daba-187">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="6daba-188">
                    <strong>Sadrži trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="6daba-189">
                    <strong>Umetanje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6daba-190">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="6daba-191">
                    <strong>Važi / Ne važi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="6daba-192">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6daba-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-193">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-194">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-195">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-196">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-197">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-198">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-199">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-200">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-201">Ne važi</span><span class="sxs-lookup"><span data-stu-id="6daba-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-202">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="6daba-202">Violation of Rule #2.</span></span> <span data-ttu-id="6daba-203">Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="6daba-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-204">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-205">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-206">QL2</span><span class="sxs-lookup"><span data-stu-id="6daba-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-207">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-208">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-209">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-210">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-211">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="6daba-212">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-213">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-214">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-215">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-216">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-217">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-218">No</span><span class="sxs-lookup"><span data-stu-id="6daba-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-219">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-220">Ne važi</span><span class="sxs-lookup"><span data-stu-id="6daba-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-221">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="6daba-221">Violation of Rule #2.</span></span> <span data-ttu-id="6daba-222">Vreme i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.</span><span class="sxs-lookup"><span data-stu-id="6daba-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-223">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-224">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-225">QL2</span><span class="sxs-lookup"><span data-stu-id="6daba-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-226">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-227">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-228">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-229">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-230">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-231">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-232">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-233">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-234">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-235">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-236">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-237">No</span><span class="sxs-lookup"><span data-stu-id="6daba-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-238">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-239">Važeći</span><span class="sxs-lookup"><span data-stu-id="6daba-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="6daba-240">Vreme i naknade za projekat P1 su uključeni u QL1.</span><span class="sxs-lookup"><span data-stu-id="6daba-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="6daba-241">Troškovi za projekat P1 uključeni su u QL2.</span><span class="sxs-lookup"><span data-stu-id="6daba-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="6daba-242">Nema preklapanja u onome što je uključeno u svaku stavku ponude i što je važeće.</span><span class="sxs-lookup"><span data-stu-id="6daba-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-243">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-244">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-245">QL2</span><span class="sxs-lookup"><span data-stu-id="6daba-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-246">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-247">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-248">No</span><span class="sxs-lookup"><span data-stu-id="6daba-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-249">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-250">No</span><span class="sxs-lookup"><span data-stu-id="6daba-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="6daba-251">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-252">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-253">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-254">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-255">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-256">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-257">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-258">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-259">Ne važi</span><span class="sxs-lookup"><span data-stu-id="6daba-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-260">Kršenje gorenavedenog pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="6daba-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="6daba-261">Q1 uključuje vreme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="6daba-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6daba-262">QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i preklapa se sa onim što je uključeno u Q1.</span><span class="sxs-lookup"><span data-stu-id="6daba-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-263">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-264">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-265">QL2</span><span class="sxs-lookup"><span data-stu-id="6daba-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-266">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-267">Prazno</span><span class="sxs-lookup"><span data-stu-id="6daba-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-268">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-269">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-270">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-271">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-272">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-273">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-274">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-275">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-276">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-277">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-278">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-279">Važeći</span><span class="sxs-lookup"><span data-stu-id="6daba-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-280">Po gorenavedenom pravilu br. 3,</span><span class="sxs-lookup"><span data-stu-id="6daba-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="6daba-281">Q1 uključuje vreme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="6daba-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6daba-282">QL2 uključuje vreme, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="6daba-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6daba-283">Jedina dodatna provera valjanosti odnosi se na podskup zadataka na QL1 koji se razlikuju od podskupa zadataka na QL2.</span><span class="sxs-lookup"><span data-stu-id="6daba-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="6daba-284">Ovo osigurava da nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="6daba-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="6daba-285">To sistem radi kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="6daba-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-286">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-287">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-288">QL2</span><span class="sxs-lookup"><span data-stu-id="6daba-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-289">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-290">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="6daba-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-291">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-292">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-293">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="6daba-294">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-295">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-296">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-297">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-298">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="6daba-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-299">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-300">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-301">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6daba-302">Važeći</span><span class="sxs-lookup"><span data-stu-id="6daba-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-303">Na osnovu pravila br. 5, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da obe mogu proceniti iste komponente projekta.</span><span class="sxs-lookup"><span data-stu-id="6daba-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-304">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-305">K2</span><span class="sxs-lookup"><span data-stu-id="6daba-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-306">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-307">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-308">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="6daba-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-309">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-310">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-311">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="6daba-312">O1</span><span class="sxs-lookup"><span data-stu-id="6daba-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-313">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-314">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-315">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-316">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="6daba-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-317">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-318">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-319">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6daba-320">Važeći</span><span class="sxs-lookup"><span data-stu-id="6daba-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6daba-321">Na osnovu pravila br. 4, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da one ne mogu proceniti komponente istog projekta.</span><span class="sxs-lookup"><span data-stu-id="6daba-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="6daba-322">O2</span><span class="sxs-lookup"><span data-stu-id="6daba-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6daba-323">K1</span><span class="sxs-lookup"><span data-stu-id="6daba-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-324">QL1</span><span class="sxs-lookup"><span data-stu-id="6daba-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-325">P1</span><span class="sxs-lookup"><span data-stu-id="6daba-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="6daba-326">Svi projektni zadaci ili prazni</span><span class="sxs-lookup"><span data-stu-id="6daba-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-327">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="6daba-328">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="6daba-329">Da</span><span class="sxs-lookup"><span data-stu-id="6daba-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="6daba-330">Ne važi</span><span class="sxs-lookup"><span data-stu-id="6daba-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]