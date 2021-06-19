---
title: Korektivne fakture za projekat
description: Ova tema pruža informacije o tome kako da kreirate i potvrdite korektivne fakture u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004098"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="59d4b-103">Korektivne fakture za projekat</span><span class="sxs-lookup"><span data-stu-id="59d4b-103">Corrective project invoices</span></span>

<span data-ttu-id="59d4b-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="59d4b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="59d4b-105">Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.</span><span class="sxs-lookup"><span data-stu-id="59d4b-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="59d4b-106">Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="59d4b-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="59d4b-107">Ovaj izbor nije dostupan ukoliko se ne potvrdi faktura projekta.</span><span class="sxs-lookup"><span data-stu-id="59d4b-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="59d4b-108">Iz potvrđene fakture kreira se nova radna verzija fakture.</span><span class="sxs-lookup"><span data-stu-id="59d4b-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="59d4b-109">Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju.</span><span class="sxs-lookup"><span data-stu-id="59d4b-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="59d4b-110">Slede neke od ključnih tačaka koje treba razumeti u vezi sa detaljima linije na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="59d4b-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="59d4b-111">Sve količine su ažurirane na nulu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-111">All quantities are updated to zero.</span></span> <span data-ttu-id="59d4b-112">Aplikacija pretpostavlja da su sve fakturisane stavke u potpunosti zadužene.</span><span class="sxs-lookup"><span data-stu-id="59d4b-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="59d4b-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="59d4b-114">Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="59d4b-115">Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura.</span><span class="sxs-lookup"><span data-stu-id="59d4b-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="59d4b-116">Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="59d4b-117">Prethodno potvrđeni predmeti ugovora zasnovani na proizvodu se ne kopiraju.</span><span class="sxs-lookup"><span data-stu-id="59d4b-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="59d4b-118">Obrada ispravki na fakturi projekta zasnovanog na proizvodu nije podržana.</span><span class="sxs-lookup"><span data-stu-id="59d4b-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="59d4b-119">Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.</span><span class="sxs-lookup"><span data-stu-id="59d4b-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="59d4b-120">Iznosi obustave ili avansa mogu se ispraviti ako je klijentu fakturisan netačan iznos.</span><span class="sxs-lookup"><span data-stu-id="59d4b-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="59d4b-121">Sravnjenja obustava i avansa mogu se ispraviti ako je korišćen netačan iznos za stavnjenje troškova na prethodno potvrđenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="59d4b-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59d4b-122">Podaci o liniji fakture koji predstavljaju ispravke drugih već fakturisanih troškova imaju polje **Ispravka** podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="59d4b-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="59d4b-123">Fakture koje imaju ispravljene detalje o liniji fakture imaju polje **Ima ispravke** koje je takođe postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="59d4b-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="59d4b-124">Trenutno stanje kreirano kada je potvrđena korektivna faktura</span><span class="sxs-lookup"><span data-stu-id="59d4b-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="59d4b-125">Sledeća tabela navodi stvarne podatke koji se kreiraju kada se potvrdi faktura sa ispravkom.</span><span class="sxs-lookup"><span data-stu-id="59d4b-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="59d4b-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="59d4b-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="59d4b-127">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="59d4b-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="59d4b-128">Potvrdite ispravku fakturisanog avansa ili obustave.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="59d4b-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-129">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="59d4b-130">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="59d4b-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-131">Stvarni iznos stornirane naplaćene prodaje kreira se za iznos na obustavi ili avansu da bi se poništila prvobitna naplaćena prodaja.</span><span class="sxs-lookup"><span data-stu-id="59d4b-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-132">Kreira se novi fakturisani stvarni trošak prodaje za ispravljeni iznos ili ispravljenoj liniji fakture na osnovu obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="59d4b-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-133">Stvarna nenaplaćena prodaja negativnog iznosa ispravljene linije fakture na osnovu obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="59d4b-134">Potvrda ispravke prethodno sravnjene obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="59d4b-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-135">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="59d4b-136">Ovaj iznos je pozitivan i ima za cilj da poništi negativan iznos nastao prilikom prethodnog sravnjenja.</span><span class="sxs-lookup"><span data-stu-id="59d4b-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-137">Stvarni iznos stornirane naplaćene prodaje za iznos na prethodnoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="59d4b-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-138">Novi naplaćeni stvarni trošak prodaje za ispravljeni iznos obustave koji se primenjuje na ispravljenu fakturu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-139">Stvarna nenaplaćena prodaja sa negativnim iznosom sa ispravljene preostale obustave ili avansa, koja će se koristiti za sravnjenje na kasnijim fakturama.</span><span class="sxs-lookup"><span data-stu-id="59d4b-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="59d4b-140">Fakturisanje punog kredita prethodno fakturisane vremenske transakcije.</span><span class="sxs-lookup"><span data-stu-id="59d4b-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-141">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="59d4b-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-142">Novi nenaplaćeni stvarni iznos prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="59d4b-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="59d4b-143">Fakturisanje delimičnog kredita za vremensku transakciju.</span><span class="sxs-lookup"><span data-stu-id="59d4b-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-144">Storniranje naplaćene prodaje za sate i iznos fakturisan na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="59d4b-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-145">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-146">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="59d4b-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="59d4b-147">Fakturisanje punog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="59d4b-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-148">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="59d4b-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-149">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="59d4b-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="59d4b-150">Fakturisanje delimičnog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="59d4b-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-151">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="59d4b-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-152">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije ispravljene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-153">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="59d4b-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="59d4b-154">Fakturisanje punog kredita prethodno fakturisane materijalne transakcije.</span><span class="sxs-lookup"><span data-stu-id="59d4b-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-155">Storniranje naplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="59d4b-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-156">Nova stvarna vrednost nenaplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="59d4b-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="59d4b-157">Fakturisanje delimičnog kredita za transakciju materijala.</span><span class="sxs-lookup"><span data-stu-id="59d4b-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-158">Storniranje naplaćene prodaje za fakturisanu količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="59d4b-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-159">Nova nefakturisana stvarna prodaja koja se naplaćuje za količinu i iznos na izmenjenom detalju stavke fakture, storniranje ove stavke i ekvivalentni stvarni iznos naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-160">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="59d4b-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="59d4b-161">Fakturisanje punog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="59d4b-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-162">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-163">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="59d4b-164">Fakturisanje delimičnog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="59d4b-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-165">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-166">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene korektivne fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="59d4b-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="59d4b-167">Fakturisanje punog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="59d4b-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-168">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za kontrolnu tačku.</span><span class="sxs-lookup"><span data-stu-id="59d4b-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="59d4b-169">Status fakture na kontrolnoj tački se ažurira iz <b>Proknjižena faktura za klijenta</b> u <b>Spremno za fakturisanje</b>.</span><span class="sxs-lookup"><span data-stu-id="59d4b-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="59d4b-170">Fakturisanje delimičnog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="59d4b-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-171">Nepodržano</span><span class="sxs-lookup"><span data-stu-id="59d4b-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="59d4b-172">Krediti i ispravke prethodno fakturisanog predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="59d4b-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="59d4b-173">Nepodržano</span><span class="sxs-lookup"><span data-stu-id="59d4b-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
