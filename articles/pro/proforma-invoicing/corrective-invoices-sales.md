---
title: Ispravljene fakture – jednostavno
description: Ova tema pruža informacije o ispravljenim fakturama u usluzi Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274250"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="319eb-103">Ispravljene fakture – jednostavno</span><span class="sxs-lookup"><span data-stu-id="319eb-103">Corrected invoices - lite</span></span>

<span data-ttu-id="319eb-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="319eb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="319eb-105">Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.</span><span class="sxs-lookup"><span data-stu-id="319eb-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="319eb-106">Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="319eb-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="319eb-107">Ovaj izbor nije dostupan ukoliko se ne potvrdi faktura projekta.</span><span class="sxs-lookup"><span data-stu-id="319eb-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="319eb-108">Iz potvrđene fakture kreira se nova radna verzija fakture.</span><span class="sxs-lookup"><span data-stu-id="319eb-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="319eb-109">Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju.</span><span class="sxs-lookup"><span data-stu-id="319eb-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="319eb-110">Slede neke od ključnih tačaka koje treba razumeti u vezi sa detaljima linije na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="319eb-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="319eb-111">Sve količine su ažurirane na nulu.</span><span class="sxs-lookup"><span data-stu-id="319eb-111">All quantities are updated to zero.</span></span> <span data-ttu-id="319eb-112">Aplikacija pretpostavlja da su sve fakturisane stavke u potpunosti zadužene.</span><span class="sxs-lookup"><span data-stu-id="319eb-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="319eb-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="319eb-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="319eb-114">Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu.</span><span class="sxs-lookup"><span data-stu-id="319eb-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="319eb-115">Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura.</span><span class="sxs-lookup"><span data-stu-id="319eb-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="319eb-116">Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="319eb-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="319eb-117">Prethodno potvrđeni predmeti ugovora zasnovani na proizvodu se ne kopiraju.</span><span class="sxs-lookup"><span data-stu-id="319eb-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="319eb-118">Obrada ispravki na fakturi projekta zasnovanog na proizvodu nije podržana.</span><span class="sxs-lookup"><span data-stu-id="319eb-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="319eb-119">Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.</span><span class="sxs-lookup"><span data-stu-id="319eb-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="319eb-120">Iznosi obustave ili avansa mogu se ispraviti ako je klijentu fakturisan netačan iznos.</span><span class="sxs-lookup"><span data-stu-id="319eb-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="319eb-121">Sravnjenja obustava i avansa mogu se ispraviti ako je korišćen netačan iznos za stavnjenje troškova na prethodno potvrđenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="319eb-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="319eb-122">Podaci o liniji fakture koji predstavljaju ispravke drugih već fakturisanih troškova imaju polje **Ispravka** podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="319eb-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="319eb-123">Fakture koje imaju ispravljene detalje o liniji fakture imaju polje **Ima ispravke** koje je takođe postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="319eb-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="319eb-124">Stvarni troškovi kreirani na potvrdi korektivne fakture:</span><span class="sxs-lookup"><span data-stu-id="319eb-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="319eb-125">Ispod su stvarni troškovi koje je kreirala aplikacija po potvrdi ispravke na osnovu operacija izvršenih na radnoj verziji korektivne fakture pre potvrde.</span><span class="sxs-lookup"><span data-stu-id="319eb-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="319eb-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="319eb-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="319eb-127">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="319eb-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="319eb-128">Potvrdite ispravku fakturisanog avansa ili obustave.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="319eb-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-129">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="319eb-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="319eb-130">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="319eb-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-131">Stvarni iznos stornirane naplaćene prodaje kreira se za iznos na obustavi ili avansu da bi se poništila prvobitna naplaćena prodaja.</span><span class="sxs-lookup"><span data-stu-id="319eb-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-132">Kreira se novi fakturisani stvarni trošak prodaje za ispravljeni iznos ili ispravljenoj liniji fakture na osnovu obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="319eb-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-133">Stvarna nenaplaćena prodaja negativnog iznosa ispravljene linije fakture na osnovu obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="319eb-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="319eb-134">Potvrda ispravke prethodno sravnjene obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="319eb-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-135">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="319eb-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="319eb-136">Ovaj iznos je pozitivan i ima za cilj da poništi negativan iznos nastao prilikom prethodnog sravnjenja.</span><span class="sxs-lookup"><span data-stu-id="319eb-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-137">Stvarni iznos stornirane naplaćene prodaje za iznos na prethodnoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="319eb-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-138">Novi naplaćeni stvarni trošak prodaje za ispravljeni iznos obustave koji se primenjuje na ispravljenu fakturu.</span><span class="sxs-lookup"><span data-stu-id="319eb-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-139">Stvarna nenaplaćena prodaja sa negativnim iznosom sa ispravljene preostale obustave ili avansa, koja će se koristiti za sravnjenje na kasnijim fakturama.</span><span class="sxs-lookup"><span data-stu-id="319eb-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="319eb-140">Fakturisanje punog kredita prethodno fakturisane vremenske transakcije.</span><span class="sxs-lookup"><span data-stu-id="319eb-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-141">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="319eb-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-142">Novi nenaplaćeni stvarni iznos prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="319eb-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="319eb-143">Fakturisanje delimičnog kredita za vremensku transakciju.</span><span class="sxs-lookup"><span data-stu-id="319eb-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-144">Storniranje naplaćene prodaje za sate i iznos fakturisan na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="319eb-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-145">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="319eb-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-146">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="319eb-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="319eb-147">Fakturisanje punog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="319eb-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-148">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="319eb-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-149">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="319eb-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="319eb-150">Fakturisanje delimičnog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="319eb-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-151">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="319eb-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-152">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije ispravljene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="319eb-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-153">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="319eb-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="319eb-154">Fakturisanje punog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="319eb-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-155">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="319eb-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-156">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="319eb-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="319eb-157">Fakturisanje delimičnog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="319eb-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-158">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="319eb-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-159">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene korektivne fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="319eb-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="319eb-160">Fakturisanje punog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="319eb-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-161">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za kontrolnu tačku.</span><span class="sxs-lookup"><span data-stu-id="319eb-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="319eb-162">Faktura kontrolne tačke ili status naplate na predmetu projektnog ugovora ažurira se na **Spremno za fakturisanje**.</span><span class="sxs-lookup"><span data-stu-id="319eb-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="319eb-163">Fakturisanje delimičnog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="319eb-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-164">Nepodržano</span><span class="sxs-lookup"><span data-stu-id="319eb-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="319eb-165">Krediti i ispravke prethodno fakturisanog predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="319eb-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="319eb-166">Nepodržano</span><span class="sxs-lookup"><span data-stu-id="319eb-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]