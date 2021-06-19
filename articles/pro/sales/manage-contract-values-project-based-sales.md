---
title: Pregled predmeta ugovora zasnovanih na projektu
description: Ova tema pruža informacije o radu sa predmetima ugovora zasnovanim na projektu.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8af32b0475650db9c5862ea23d185588a631ade6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003153"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="11d3c-103">Pregled predmeta ugovora zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="11d3c-103">Project-based contract lines overview</span></span>

<span data-ttu-id="11d3c-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="11d3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="11d3c-105">Predmeti ugovora zasnovani na projektu u usluzi Dynamics 365 Project Operations dizajnirani su tako da drže ugovore o proceni i obračunu za određene komponente projektnog rada na angažmanu.</span><span class="sxs-lookup"><span data-stu-id="11d3c-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="11d3c-106">Struktura stavke ugovora zasnovane na projektu proširena je za procene projekata i scenarije naplate sa sledećim konceptima:</span><span class="sxs-lookup"><span data-stu-id="11d3c-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="11d3c-107">Način naplate</span><span class="sxs-lookup"><span data-stu-id="11d3c-107">Billing method</span></span>
- <span data-ttu-id="11d3c-108">Mapiranje projekata i zadataka</span><span class="sxs-lookup"><span data-stu-id="11d3c-108">Project and task mapping</span></span>
- <span data-ttu-id="11d3c-109">Uključene klase transakcija</span><span class="sxs-lookup"><span data-stu-id="11d3c-109">Included transaction classes</span></span>
- <span data-ttu-id="11d3c-110">Ograničenje koje ne sme da se prekorači</span><span class="sxs-lookup"><span data-stu-id="11d3c-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="11d3c-111">Podešavanje naplativosti</span><span class="sxs-lookup"><span data-stu-id="11d3c-111">Chargeability setup</span></span>
- <span data-ttu-id="11d3c-112">Procene korišćenjem detalja o predmeta ugovora</span><span class="sxs-lookup"><span data-stu-id="11d3c-112">Estimates using contract line details</span></span>
- <span data-ttu-id="11d3c-113">Klijenti predmeta ugovora</span><span class="sxs-lookup"><span data-stu-id="11d3c-113">Contract line customers</span></span>

<span data-ttu-id="11d3c-114">Sledeća tabela uključuje polja na kartici **Opšti podaci** predmeta ugovora zasnovanih na projektu koji pomažu u postavljanju osnove za detaljnu, osnovnu procenu i aranžmane za obračun za projektni rad.</span><span class="sxs-lookup"><span data-stu-id="11d3c-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="11d3c-115">Polje</span><span class="sxs-lookup"><span data-stu-id="11d3c-115">Field</span></span> | <span data-ttu-id="11d3c-116">Opis</span><span class="sxs-lookup"><span data-stu-id="11d3c-116">Description</span></span> | <span data-ttu-id="11d3c-117">Posledični uticaj</span><span class="sxs-lookup"><span data-stu-id="11d3c-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="11d3c-118">**Ime**</span><span class="sxs-lookup"><span data-stu-id="11d3c-118">**Name**</span></span> | <span data-ttu-id="11d3c-119">Naziv predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-119">Name of the contract line.</span></span> <span data-ttu-id="11d3c-120">Ovo identifikuje diskretnu komponentu ugovora koja se procenjuje.</span><span class="sxs-lookup"><span data-stu-id="11d3c-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="11d3c-121">Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajuće vrednosti stavke ponude zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="11d3c-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="11d3c-122">Ime kopirano u stavku fakture za projekat koja se kreira iz ovog predmeta ugovora kada se kreira faktura.</span><span class="sxs-lookup"><span data-stu-id="11d3c-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="11d3c-123">**Način naplate**</span><span class="sxs-lookup"><span data-stu-id="11d3c-123">**Billing Method**</span></span> | <span data-ttu-id="11d3c-124">Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="11d3c-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="11d3c-125">Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja koja podržava usluga Project Operations:</span><span class="sxs-lookup"><span data-stu-id="11d3c-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="11d3c-126">- **Fiksna cena**</span><span class="sxs-lookup"><span data-stu-id="11d3c-126">- **Fixed Price**</span></span></br><span data-ttu-id="11d3c-127">- **Vreme i materijal**</span><span class="sxs-lookup"><span data-stu-id="11d3c-127">- **Time and Material**</span></span> | <span data-ttu-id="11d3c-128">Na osnovu načina naplate navedenog predmeta ugovora, stvarna transakcija će biti obrađena.</span><span class="sxs-lookup"><span data-stu-id="11d3c-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="11d3c-129">Ako predmet ugovora na koji se poziva stvarna vrednost ima način naplate vremena i materijala, kreiraju se zapisi stvarnih vrednosti troškova i nenaplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="11d3c-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="11d3c-130">Ako predmet ugovora na koji se poziva stvarna vrednost ima način obračuna sa fiksnom cenom, kreiraće se samo stvarni trošak.</span><span class="sxs-lookup"><span data-stu-id="11d3c-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="11d3c-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="11d3c-131">**Project**</span></span> | <span data-ttu-id="11d3c-132">Koristite ovo polje za identifikovanje projekta koji će se koristiti za izvođenje radova na ovom angažmanu.</span><span class="sxs-lookup"><span data-stu-id="11d3c-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="11d3c-133">Ova vrednost će se koristiti zajedno sa **Obuhvaćeni zadaci** i **Obuhvaćene klase transakcija** da se reši referenca na predmet ugovora na stvarnom ili procenjenom zapisu stavke.</span><span class="sxs-lookup"><span data-stu-id="11d3c-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="11d3c-134">**Obuhvaćeni zadaci**</span><span class="sxs-lookup"><span data-stu-id="11d3c-134">**Included Tasks**</span></span> | <span data-ttu-id="11d3c-135">Označava da li ova linija ugovora uključuje sve projektne zadatke za izabrani projekat ili samo podskup zadataka.</span><span class="sxs-lookup"><span data-stu-id="11d3c-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="11d3c-136">Ovo je skup opcija koji ima sledeće moguće vrednosti:</span><span class="sxs-lookup"><span data-stu-id="11d3c-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="11d3c-137">- **Svi projektni zadaci**</span><span class="sxs-lookup"><span data-stu-id="11d3c-137">- **All Project Tasks**</span></span></br><span data-ttu-id="11d3c-138">- **Samo izabrani projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="11d3c-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="11d3c-139">Prazna vrednost u ovom polju jednaka je odabiru **Svi projektni zadaci**.</span><span class="sxs-lookup"><span data-stu-id="11d3c-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="11d3c-140">Ako je izabrana opcija **Samo izabrani zadaci**, možete izabrati određene zadatke i povezati ih sa ovim predmetom ugovora na kartici **Podešavanje zadatka za obračun** na stranici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="11d3c-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="11d3c-141">Vrednost će se koristiti zajedno sa klasama **Projekat** i **Uključene klase transakcija** da se razreši referenca na predmet ugovora na stvarnoj vrednosti ili zapisu predmeta procene.</span><span class="sxs-lookup"><span data-stu-id="11d3c-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="11d3c-142">**Sadrži vreme**</span><span class="sxs-lookup"><span data-stu-id="11d3c-142">**Include Time**</span></span> | <span data-ttu-id="11d3c-143">Vrednost **Da**/**Ne** pokazuje da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="11d3c-144">Vrednost **Ne** označava da vremenske transakcije ili troškovi rada neće biti uključeni u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="11d3c-145">Vrednost **Da** ukazuje na to da hoće.</span><span class="sxs-lookup"><span data-stu-id="11d3c-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="11d3c-146">Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke.</span><span class="sxs-lookup"><span data-stu-id="11d3c-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="11d3c-147">**Sadrži trošak**</span><span class="sxs-lookup"><span data-stu-id="11d3c-147">**Include Expense**</span></span> | <span data-ttu-id="11d3c-148">Vrednost **Da**/**Ne** pokazuje da li će cena troškova na izabranom projektu biti uključena u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="11d3c-149">Vrednost **Ne** označava da cena troškova na izabranom projektu neće biti uključena u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="11d3c-150">Vrednost **Da** ukazuje na to da hoće.</span><span class="sxs-lookup"><span data-stu-id="11d3c-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="11d3c-151">Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke.</span><span class="sxs-lookup"><span data-stu-id="11d3c-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="11d3c-152">**Sadrži materijale**</span><span class="sxs-lookup"><span data-stu-id="11d3c-152">**Include Materials**</span></span> | <span data-ttu-id="11d3c-153">Vrednost **Da**/**Ne** pokazuje da li će cena materijala na izabranom projektu biti uključena u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="11d3c-154">Vrednost **Ne** pokazuje da cena materijala neće biti uključena u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="11d3c-155">Vrednost **Da** ukazuje na to da hoće.</span><span class="sxs-lookup"><span data-stu-id="11d3c-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="11d3c-156">Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke.</span><span class="sxs-lookup"><span data-stu-id="11d3c-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="11d3c-157">**Sadrži nadoknadu**</span><span class="sxs-lookup"><span data-stu-id="11d3c-157">**Include Fee**</span></span> | <span data-ttu-id="11d3c-158">Vrednost **Da**/**Ne** pokazuje da li će naknade na izabranom projektu biti uključene u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="11d3c-159">Vrednost **Ne** označava da naknade neće biti uključene u ovaj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="11d3c-160">Vrednost **Da** ukazuje na to da hoće.</span><span class="sxs-lookup"><span data-stu-id="11d3c-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="11d3c-161">Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke.</span><span class="sxs-lookup"><span data-stu-id="11d3c-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="11d3c-162">**Ugovoreni iznos**</span><span class="sxs-lookup"><span data-stu-id="11d3c-162">**Contracted Amount**</span></span> | <span data-ttu-id="11d3c-163">Na predmetu ugovora sa fiksnom cenom, ovaj iznos je ugovorena vrednost koja će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="11d3c-164">Na predmetu ugovora za vreme i materijal, ovaj iznos je procenjena vrednost onoga što će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="11d3c-165">Za projektni ugovor koji je kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude.</span><span class="sxs-lookup"><span data-stu-id="11d3c-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="11d3c-166">Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa u detaljima linije ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="11d3c-167">Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa na detaljima stavki.</span><span class="sxs-lookup"><span data-stu-id="11d3c-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="11d3c-168">U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje iznosa pre oporezivanja na periodičnim kontrolnim tačkama obračuna.</span><span class="sxs-lookup"><span data-stu-id="11d3c-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="11d3c-169">**Procenjeni porez**</span><span class="sxs-lookup"><span data-stu-id="11d3c-169">**Estimated Tax**</span></span> | <span data-ttu-id="11d3c-170">Korisnik može da uređuje ovo polje kako bi uneo procenjeni iznos poreza u predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="11d3c-171">Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa poreza u detaljima predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="11d3c-172">Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa poreza na detaljima stavki.</span><span class="sxs-lookup"><span data-stu-id="11d3c-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="11d3c-173">U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje poreza na periodičnim kontrolnim tačkama obračuna.</span><span class="sxs-lookup"><span data-stu-id="11d3c-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="11d3c-174">**Ugovoreni iznos sa porezom**</span><span class="sxs-lookup"><span data-stu-id="11d3c-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="11d3c-175">Iznos predmeta ugovora sa porezom.</span><span class="sxs-lookup"><span data-stu-id="11d3c-175">The contract line amount after tax.</span></span> <span data-ttu-id="11d3c-176">Ovo polje je samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**.</span><span class="sxs-lookup"><span data-stu-id="11d3c-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="11d3c-177">U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje periodičnih kontrolnih tačaka obračuna.</span><span class="sxs-lookup"><span data-stu-id="11d3c-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="11d3c-178">**Ograničenje koje ne sme da se prekorači**</span><span class="sxs-lookup"><span data-stu-id="11d3c-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="11d3c-179">Korisnik može da uređuje ovo polje i ono je dostupno samo na predmetima ugovora zasnovanim na projektu čiji način obračuna je postavljen na vreme i materijal.</span><span class="sxs-lookup"><span data-stu-id="11d3c-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="11d3c-180">Korisnik može da uređuje ovo polje.</span><span class="sxs-lookup"><span data-stu-id="11d3c-180">The user can edit this field.</span></span> <span data-ttu-id="11d3c-181">Kada se stvarna vrednost za vreme i materijal odnosi na ovaj predmet ugovora za vreme i materijal, iznos na stvarnoj vrednosti se procenjuje prema ograničenju koje ne sme da se premaši na predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="11d3c-182">Ova procena se završava nakon što se obračunaju već potrošeni i preuzeti iznosi.</span><span class="sxs-lookup"><span data-stu-id="11d3c-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="11d3c-183">**Budžet klijenta**</span><span class="sxs-lookup"><span data-stu-id="11d3c-183">**Customer Budget**</span></span> | <span data-ttu-id="11d3c-184">Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja na stavki ponude ako je ugovor kreiran iz ponude.</span><span class="sxs-lookup"><span data-stu-id="11d3c-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="11d3c-185">Ovo polje se koristi samo za informacije i nema nikakav dalji značaj.</span><span class="sxs-lookup"><span data-stu-id="11d3c-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="11d3c-186">Pravila za validaciju za opcije na kartici Opšti podaci za predmete ugovora zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="11d3c-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="11d3c-187">Pravilo 1: Ako je polje **Uključeni zadaci** prazno ili podešeno na **Svi projektni zadaci**, svi zadaci projekta su uključeni u predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="11d3c-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="11d3c-188">Pravilo 2: Kada je polje **Uključeni zadaci** prazno ili je izričito postavljeno na **Svi projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni samo u jedan predmet ugovora zasnovan na projektu.</span><span class="sxs-lookup"><span data-stu-id="11d3c-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="11d3c-189">Pravilo 3: Kada je polje **Uključeni zadaci** postavljeno na **Samo izabrani projektni zadaci**, projekat i određena klasa transakcija mogu da se uključe u više predmeta ugovora zasnovanih na projektu.</span><span class="sxs-lookup"><span data-stu-id="11d3c-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="11d3c-190">
                    <strong>Ugovor</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="11d3c-191">
                    <strong>Predmet ugovora</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="11d3c-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="11d3c-193">
                    <strong>Obuhvaćeni zadaci</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="11d3c-194">
                    <strong>Sadrži vreme</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="11d3c-195">
                    <strong>Sadrži trošak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="11d3c-196">
                    <strong>Sadrži materijale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="11d3c-197">
                    <strong>Uvrsti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="11d3c-198">
                    <strong>Naknada</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="11d3c-199">
                    <strong>Važi / Ne važi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="11d3c-200">
                    <strong>Razlog</strong>
                </span><span class="sxs-lookup"><span data-stu-id="11d3c-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-201">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-202">CL1</span><span class="sxs-lookup"><span data-stu-id="11d3c-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-203">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-204">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-205">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-206">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-207">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-208">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-209">Ne važi</span><span class="sxs-lookup"><span data-stu-id="11d3c-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-210">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="11d3c-210">Violation of Rule #2.</span></span> <span data-ttu-id="11d3c-211">Vreme, troškovi, materijali i naknade na projektu P1 uključeni su u oba predmeta ugovora CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="11d3c-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-212">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-213">CL2</span><span class="sxs-lookup"><span data-stu-id="11d3c-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-214">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-215">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-216">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-217">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-218">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-219">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-220">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-221">CL1</span><span class="sxs-lookup"><span data-stu-id="11d3c-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-222">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-223">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-224">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-225">No</span><span class="sxs-lookup"><span data-stu-id="11d3c-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-226">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-227">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-228">Ne važi</span><span class="sxs-lookup"><span data-stu-id="11d3c-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-229">Kršenje pravila br. 2.</span><span class="sxs-lookup"><span data-stu-id="11d3c-229">Violation of Rule #2.</span></span> <span data-ttu-id="11d3c-230">Vreme, troškovi, materijali i naknade na projektu P1 uključeni su u oba predmeta ugovora CL1 i CL2.</span><span class="sxs-lookup"><span data-stu-id="11d3c-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-231">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-232">CL2</span><span class="sxs-lookup"><span data-stu-id="11d3c-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-233">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-234">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-235">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-236">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-237">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-238">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-239">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-240">CL1</span><span class="sxs-lookup"><span data-stu-id="11d3c-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-241">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-242">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-243">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-244">No</span><span class="sxs-lookup"><span data-stu-id="11d3c-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-245">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-246">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-247">Važeće</span><span class="sxs-lookup"><span data-stu-id="11d3c-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-248">Vreme, materijali i naknade za projekat P1 uključeni su u CL1.</span><span class="sxs-lookup"><span data-stu-id="11d3c-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="11d3c-249">Troškovi za projekat P1 uključeni su u CL2.</span><span class="sxs-lookup"><span data-stu-id="11d3c-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="11d3c-250">Nema preklapanja u onome što je uključeno u svaki predmet ugovora i stoga je važeće.</span><span class="sxs-lookup"><span data-stu-id="11d3c-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-251">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-252">CL2</span><span class="sxs-lookup"><span data-stu-id="11d3c-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-253">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-254">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-255">No</span><span class="sxs-lookup"><span data-stu-id="11d3c-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-256">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-257">No</span><span class="sxs-lookup"><span data-stu-id="11d3c-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-258">No</span><span class="sxs-lookup"><span data-stu-id="11d3c-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-259">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-260">CL1</span><span class="sxs-lookup"><span data-stu-id="11d3c-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-261">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-262">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="11d3c-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-263">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-264">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-265">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-266">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-267">Ne važi</span><span class="sxs-lookup"><span data-stu-id="11d3c-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-268">Kršenje pravila br. 2</span><span class="sxs-lookup"><span data-stu-id="11d3c-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="11d3c-269">C1 uključuje vreme, materijale, troškove i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="11d3c-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="11d3c-270">CL2 uključuje vreme, materijale, troškove i naknade za ceo projekat P1 i stoga se preklapa sa onim što je uključeno u C1.</span><span class="sxs-lookup"><span data-stu-id="11d3c-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-271">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-272">CL2</span><span class="sxs-lookup"><span data-stu-id="11d3c-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-273">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-274">Prazno</span><span class="sxs-lookup"><span data-stu-id="11d3c-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-275">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-276">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-277">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-278">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-279">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-280">CL1</span><span class="sxs-lookup"><span data-stu-id="11d3c-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-281">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-282">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="11d3c-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-283">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-284">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-285">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-286">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-287">Važeće</span><span class="sxs-lookup"><span data-stu-id="11d3c-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="11d3c-288">Po pravilu br. 3</span><span class="sxs-lookup"><span data-stu-id="11d3c-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="11d3c-289">C1 uključuje vreme, troškove, materijale i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="11d3c-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="11d3c-290">CL2 uključuje vreme, troškove, materijale i naknade za podskup zadataka na projektu P1.</span><span class="sxs-lookup"><span data-stu-id="11d3c-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="11d3c-291">Jedina dodatna provera valjanosti oko podskupa zadataka na CL1 razlikuje se od podskupa zadataka na CL2 kako bi se osiguralo da tamo nema preklapanja.</span><span class="sxs-lookup"><span data-stu-id="11d3c-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="11d3c-292">To sistem radi kada su zadaci povezani.</span><span class="sxs-lookup"><span data-stu-id="11d3c-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="11d3c-293">C1</span><span class="sxs-lookup"><span data-stu-id="11d3c-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="11d3c-294">CL2</span><span class="sxs-lookup"><span data-stu-id="11d3c-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-295">P1</span><span class="sxs-lookup"><span data-stu-id="11d3c-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="11d3c-296">Samo izabrani zadaci</span><span class="sxs-lookup"><span data-stu-id="11d3c-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-297">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="11d3c-298">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-299">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="11d3c-300">Da</span><span class="sxs-lookup"><span data-stu-id="11d3c-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
