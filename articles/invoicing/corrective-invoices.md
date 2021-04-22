---
title: Kreiranje korektivnih faktura zasnovanih na projektu
description: Ova tema pruža informacije o korektivnim fakturama u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788892"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="433a3-103">Kreiranje korektivnih faktura zasnovanih na projektu</span><span class="sxs-lookup"><span data-stu-id="433a3-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="433a3-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="433a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="433a3-105">Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.</span><span class="sxs-lookup"><span data-stu-id="433a3-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="433a3-106">Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="433a3-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="433a3-107">Ovaj izbor nije dostupan ukoliko se ne potvrdi faktura projekta.</span><span class="sxs-lookup"><span data-stu-id="433a3-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="433a3-108">Iz potvrđene fakture kreira se nova radna verzija fakture.</span><span class="sxs-lookup"><span data-stu-id="433a3-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="433a3-109">Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju.</span><span class="sxs-lookup"><span data-stu-id="433a3-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="433a3-110">Slede neke ključne tačke koje će vam pomoći da razumete više o detaljima stavki na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="433a3-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="433a3-111">Sve količine su ažurirane na nulu.</span><span class="sxs-lookup"><span data-stu-id="433a3-111">All quantities are updated to zero.</span></span> <span data-ttu-id="433a3-112">To pretpostavlja da su sve fakturisane stavke u potpunosti zadužene.</span><span class="sxs-lookup"><span data-stu-id="433a3-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="433a3-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="433a3-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="433a3-114">Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu.</span><span class="sxs-lookup"><span data-stu-id="433a3-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="433a3-115">Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura.</span><span class="sxs-lookup"><span data-stu-id="433a3-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="433a3-116">Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="433a3-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="433a3-117">Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.</span><span class="sxs-lookup"><span data-stu-id="433a3-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="433a3-118">Iznosi obustave ili avansa mogu se ispraviti ako je klijentu fakturisan netačan iznos.</span><span class="sxs-lookup"><span data-stu-id="433a3-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="433a3-119">Sravnjenja obustava i avansa mogu se ispraviti ako je korišćen netačan iznos za stavnjenje troškova na prethodno potvrđenoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="433a3-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="433a3-120">Detalji stavke fakture koje predstavljaju ispravke za druge već fakturisane troškove sadrže polje **Ispravka** podešeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="433a3-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="433a3-121">Fakture koje imaju ispravljene detalje o liniji fakture imaju polje **Ima ispravke** koje je takođe postavljeno na **Da**.</span><span class="sxs-lookup"><span data-stu-id="433a3-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="433a3-122">Trenutno stanje kreirano na potvrdi korektivne fakture</span><span class="sxs-lookup"><span data-stu-id="433a3-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="433a3-123">Sledeća tabela navodi stvarne podatke koji se kreiraju kada se potvrdi faktura sa ispravkom.</span><span class="sxs-lookup"><span data-stu-id="433a3-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="433a3-124">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="433a3-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="433a3-125">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="433a3-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="433a3-126">Potvrdite ispravku fakturisanog avansa ili obustave.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="433a3-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-127">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="433a3-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="433a3-128">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="433a3-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-129">Stvarni iznos stornirane naplaćene prodaje kreira se za iznos na obustavi ili avansu da bi se poništila prvobitna naplaćena prodaja.</span><span class="sxs-lookup"><span data-stu-id="433a3-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-130">Kreira se novi fakturisani stvarni trošak prodaje za ispravljeni iznos ili ispravljenoj liniji fakture na osnovu obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="433a3-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-131">Stvarna nenaplaćena prodaja negativnog iznosa ispravljene linije fakture na osnovu obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="433a3-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="433a3-132">Potvrda ispravke prethodno sravnjene obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="433a3-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-133">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="433a3-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="433a3-134">Ovaj iznos je pozitivan i ima za cilj da poništi negativan iznos nastao prilikom prethodnog sravnjenja.</span><span class="sxs-lookup"><span data-stu-id="433a3-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-135">Stvarni iznos stornirane naplaćene prodaje za iznos na prethodnoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="433a3-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-136">Novi naplaćeni stvarni trošak prodaje za ispravljeni iznos obustave koji se primenjuje na ispravljenu fakturu.</span><span class="sxs-lookup"><span data-stu-id="433a3-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-137">Stvarna nenaplaćena prodaja sa negativnim iznosom sa ispravljene preostale obustave ili avansa, koja će se koristiti za sravnjenje na kasnijim fakturama.</span><span class="sxs-lookup"><span data-stu-id="433a3-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="433a3-138">Fakturisanje punog kredita prethodno fakturisane vremenske transakcije.</span><span class="sxs-lookup"><span data-stu-id="433a3-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-139">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="433a3-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-140">Novi nenaplaćeni stvarni iznos prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="433a3-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="433a3-141">Fakturisanje delimičnog kredita za vremensku transakciju.</span><span class="sxs-lookup"><span data-stu-id="433a3-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-142">Storniranje naplaćene prodaje za sate i iznos fakturisan na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="433a3-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-143">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="433a3-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-144">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="433a3-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="433a3-145">Fakturisanje punog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="433a3-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-146">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="433a3-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-147">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="433a3-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="433a3-148">Fakturisanje delimičnog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="433a3-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-149">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="433a3-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-150">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije ispravljene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="433a3-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-151">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="433a3-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="433a3-152">Fakturisanje punog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="433a3-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-153">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="433a3-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-154">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="433a3-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="433a3-155">Fakturisanje delimičnog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="433a3-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-156">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="433a3-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-157">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene korektivne fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="433a3-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="433a3-158">Fakturisanje punog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="433a3-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-159">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za kontrolnu tačku.</span><span class="sxs-lookup"><span data-stu-id="433a3-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="433a3-160">Status fakture na kontrolnoj tački se ažurira iz <b>Proknjižena faktura za klijenta</b> u <b>Spremno za fakturisanje</b>.</span><span class="sxs-lookup"><span data-stu-id="433a3-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="433a3-161">Fakturisanje delimičnog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="433a3-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="433a3-162">Nepodržano</span><span class="sxs-lookup"><span data-stu-id="433a3-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
