---
title: Korektivne fakture zasnovane na projektu
description: Ova tema pruža informacije o tome kako da kreirate i potvrdite korektivne fakture zasnovane na projektu u usluzi Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012288"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="2c88c-103">Korektivne fakture zasnovane na projektu</span><span class="sxs-lookup"><span data-stu-id="2c88c-103">Corrective project-based invoices</span></span>

<span data-ttu-id="2c88c-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="2c88c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2c88c-105">Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.</span><span class="sxs-lookup"><span data-stu-id="2c88c-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="2c88c-106">Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**.</span><span class="sxs-lookup"><span data-stu-id="2c88c-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2c88c-107">Ovaj izbor nije dostupan osim ako faktura projekta nije potvrđena ili ako faktura zasnovana na projektu sadrži avanse ili obustave ili usaglašavanje avansa ili obustava.</span><span class="sxs-lookup"><span data-stu-id="2c88c-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="2c88c-108">Iz potvrđene fakture kreira se nova radna verzija fakture.</span><span class="sxs-lookup"><span data-stu-id="2c88c-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="2c88c-109">Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju.</span><span class="sxs-lookup"><span data-stu-id="2c88c-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="2c88c-110">Slede neke od ključnih tačaka koje treba razumeti u vezi sa detaljima linije na novoj ispravljenoj fakturi:</span><span class="sxs-lookup"><span data-stu-id="2c88c-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="2c88c-111">Sve količine su ažurirane na nulu.</span><span class="sxs-lookup"><span data-stu-id="2c88c-111">All quantities are updated to zero.</span></span> <span data-ttu-id="2c88c-112">Dynamics 365 Project Operations pretpostavlja da su sve fakturisane stavke u potpunosti zadužene.</span><span class="sxs-lookup"><span data-stu-id="2c88c-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="2c88c-113">Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="2c88c-114">Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu.</span><span class="sxs-lookup"><span data-stu-id="2c88c-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="2c88c-115">Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura.</span><span class="sxs-lookup"><span data-stu-id="2c88c-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="2c88c-116">Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="2c88c-117">Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.</span><span class="sxs-lookup"><span data-stu-id="2c88c-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="2c88c-118">Za detalje o stavki fakture koje predstavljaju ispravke za druge već fakturisane troškove, polje **Ispravka** se postavlja na **Da**.</span><span class="sxs-lookup"><span data-stu-id="2c88c-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="2c88c-119">Za fakture imaju ispravljene detalje stavki fakture, polje **Ima ispravke** se postavlja na **Da**.</span><span class="sxs-lookup"><span data-stu-id="2c88c-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="2c88c-120">Trenutno stanje kreirano kada je potvrđena korektivna faktura</span><span class="sxs-lookup"><span data-stu-id="2c88c-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="2c88c-121">Sledeća tabela navodi stvarne podatke koji se kreiraju kada se potvrdi faktura sa ispravkom.</span><span class="sxs-lookup"><span data-stu-id="2c88c-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2c88c-122">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2c88c-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2c88c-123">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2c88c-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c88c-124">Fakturisanje punog kredita prethodno fakturisane vremenske transakcije.</span><span class="sxs-lookup"><span data-stu-id="2c88c-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-125">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="2c88c-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-126">Novi nenaplaćeni stvarni iznos prodaje za sate i iznos na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="2c88c-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c88c-127">Fakturisanje delimičnog kredita za vremensku transakciju.</span><span class="sxs-lookup"><span data-stu-id="2c88c-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-128">Storniranje naplaćene prodaje za sate i iznos fakturisan na originalnom detalju linije fakture za vreme.</span><span class="sxs-lookup"><span data-stu-id="2c88c-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-129">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-130">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="2c88c-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c88c-131">Fakturisanje punog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="2c88c-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-132">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="2c88c-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-133">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="2c88c-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c88c-134">Fakturisanje delimičnog kredita prethodno fakturisane transakcije troškova.</span><span class="sxs-lookup"><span data-stu-id="2c88c-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-135">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za trošak.</span><span class="sxs-lookup"><span data-stu-id="2c88c-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-136">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije ispravljene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-137">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="2c88c-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c88c-138">Fakturisanje punog kredita prethodno fakturisane materijalne transakcije.</span><span class="sxs-lookup"><span data-stu-id="2c88c-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-139">Storniranje naplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="2c88c-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-140">Nova stvarna vrednost nenaplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="2c88c-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2c88c-141">Fakturisanje delimičnog kredita za transakciju materijala.</span><span class="sxs-lookup"><span data-stu-id="2c88c-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-142">Storniranje naplaćene prodaje za fakturisanu količinu i iznos na detaljima stavki originalne fakture za materijal.</span><span class="sxs-lookup"><span data-stu-id="2c88c-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-143">Nova nefakturisana stvarna prodaja koja se naplaćuje za količinu i iznos na izmenjenom detalju stavke fakture, storniranje ove stavke i ekvivalentni stvarni iznos naplaćene prodaje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-144">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.</span><span class="sxs-lookup"><span data-stu-id="2c88c-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c88c-145">Fakturisanje punog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="2c88c-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-146">Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="2c88c-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-147">Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="2c88c-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2c88c-148">Fakturisanje delimičnog kredita prethodno fakturisane transakcije naknade.</span><span class="sxs-lookup"><span data-stu-id="2c88c-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-149">Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za naknadu.</span><span class="sxs-lookup"><span data-stu-id="2c88c-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-150">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene korektivne fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="2c88c-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2c88c-151">Fakturisanje punog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="2c88c-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-152">Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za kontrolnu tačku.</span><span class="sxs-lookup"><span data-stu-id="2c88c-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="2c88c-153">Status fakture na kontrolnoj tački se ažurira iz <b>Proknjižena faktura za klijenta</b> u <b>Spremno za fakturisanje</b>.</span><span class="sxs-lookup"><span data-stu-id="2c88c-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2c88c-154">Fakturisanje delimičnog kredita prethodno fakturisane kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="2c88c-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2c88c-155">Ovaj scenario nije podržan.</span><span class="sxs-lookup"><span data-stu-id="2c88c-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
