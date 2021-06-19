---
title: Potvrda predračuna za projekat
description: Ova tema pruža informacije o potvrđivanju predračuna za projekat u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004143"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="9e230-103">Potvrda predračuna za projekat</span><span class="sxs-lookup"><span data-stu-id="9e230-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="9e230-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="9e230-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9e230-105">Nakon potvrde predračuna, status fakture projekta se ažurira na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="9e230-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9e230-106">Kada se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="9e230-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9e230-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijenti.</span><span class="sxs-lookup"><span data-stu-id="9e230-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="9e230-108">U sledećoj tabeli su navedeni stvarni podaci koje je kreirao sistem.</span><span class="sxs-lookup"><span data-stu-id="9e230-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9e230-109">Ovi stvarni podaci se kreiraju kada se izvrše određene radnje na radnoj verziji fakture projekta pre nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="9e230-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9e230-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e230-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9e230-111">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9e230-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-112">Fakturisanje avansa ili odbitka</span><span class="sxs-lookup"><span data-stu-id="9e230-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-113">Fakturisani stvarni iznos prodaje, <strong>Odbitak</strong> kreira se za iznos na avansu ili obustavi.</span><span class="sxs-lookup"><span data-stu-id="9e230-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-114">Stvarna nenaplaćena prodaja negativnog iznosa obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="9e230-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-115">Nakon potpunog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="9e230-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-116">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="9e230-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9e230-117">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="9e230-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-118">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="9e230-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9e230-119">Nakon delimičnog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="9e230-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-120">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="9e230-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9e230-121">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="9e230-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-122">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="9e230-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-123">Negativna stvarna nenaplaćena prodaja preostalog iznosa obustave ili avansa, koja će se koristiti za sravnjenje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="9e230-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-124">Fakturisanje vremenske transakcije bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="9e230-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-125">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="9e230-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-126">Naplaćeni stvarni iznos prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="9e230-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9e230-127">Fakturisanje vremenske transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-128">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="9e230-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-129">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-130">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-131">Fakturisanje vremenske transakcije koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-132">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="9e230-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-133">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-134">Fakturisanje transakcije troškova bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="9e230-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-135">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="9e230-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-136">Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove</span><span class="sxs-lookup"><span data-stu-id="9e230-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9e230-137">Fakturisanje transakcije troškova koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-138">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="9e230-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-139">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-140">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-141">Fakturisanje transakcije troškova koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-142">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="9e230-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-143">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-144">Fakturisanje transakcije materijala bez ikakvih izmena u radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="9e230-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-145">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="9e230-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-146">Stvarni iznos naplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="9e230-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9e230-147">Fakturisanje materijalne transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-148">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="9e230-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-149">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-150">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-151">Fakturisanje transakcije materijala koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="9e230-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-152">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="9e230-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-153">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="9e230-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9e230-154">Fakturisanje naknade.</span><span class="sxs-lookup"><span data-stu-id="9e230-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-155">Storniranje nenaplaćene prodaje za iznos naknade u originalnoj stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="9e230-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-156">Naplaćeni stvarni iznos prodaje za količinu i iznos u originalnoj stavci u glavnoj knjizi za naknadu.</span><span class="sxs-lookup"><span data-stu-id="9e230-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9e230-157">Fakturisanje kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="9e230-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-158">Naplaćeni stvarni iznos prodaje za iznos kontrolne tačke na originalnoj kontrolnoj tački u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="9e230-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9e230-159">Fakturisanje predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="9e230-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9e230-160">Naplaćeni stvarni iznos prodaje za liniju proizvoda sa količinom i iznosom koji potiču iz predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="9e230-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
