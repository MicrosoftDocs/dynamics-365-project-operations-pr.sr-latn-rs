---
title: Potvrda predračuna za projekat
description: Ova tema pruža informacije o potvrđivanju predračuna za projekat u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 144c1b6a49951af8be0c619f41808e7617e59c92
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867104"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="e0c32-103">Potvrda predračuna za projekat</span><span class="sxs-lookup"><span data-stu-id="e0c32-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="e0c32-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="e0c32-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="e0c32-105">Nakon potvrde predračuna, status fakture projekta se ažurira na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="e0c32-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="e0c32-106">Kada se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="e0c32-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijenti.</span><span class="sxs-lookup"><span data-stu-id="e0c32-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="e0c32-108">U sledećoj tabeli su navedeni stvarni podaci koje je kreirao sistem.</span><span class="sxs-lookup"><span data-stu-id="e0c32-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="e0c32-109">Ovi stvarni podaci se kreiraju kada se izvrše određene radnje na radnoj verziji fakture projekta pre nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e0c32-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e0c32-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e0c32-111">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e0c32-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-112">Fakturisanje avansa ili odbitka</span><span class="sxs-lookup"><span data-stu-id="e0c32-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-113">Fakturisani stvarni iznos prodaje, <strong>Odbitak</strong> kreira se za iznos na avansu ili obustavi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-114">Stvarna nenaplaćena prodaja negativnog iznosa obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-115">Nakon potpunog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-116">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e0c32-117">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="e0c32-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-118">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e0c32-119">Nakon delimičnog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-120">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="e0c32-121">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="e0c32-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-122">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-123">Negativna stvarna nenaplaćena prodaja preostalog iznosa obustave ili avansa, koja će se koristiti za sravnjenje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="e0c32-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-124">Fakturisanje vremenske transakcije bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="e0c32-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-125">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="e0c32-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-126">Naplaćeni stvarni iznos prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="e0c32-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e0c32-127">Fakturisanje vremenske transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-128">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="e0c32-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-129">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-130">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-131">Fakturisanje vremenske transakcije koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-132">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="e0c32-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-133">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-134">Fakturisanje transakcije troškova bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="e0c32-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-135">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="e0c32-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-136">Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove</span><span class="sxs-lookup"><span data-stu-id="e0c32-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e0c32-137">Fakturisanje transakcije troškova koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-138">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="e0c32-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-139">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-140">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-141">Fakturisanje transakcije troškova koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-142">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="e0c32-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-143">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-144">Fakturisanje transakcije materijala bez ikakvih izmena u radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="e0c32-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-145">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="e0c32-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-146">Stvarni iznos naplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="e0c32-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e0c32-147">Fakturisanje materijalne transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-148">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju vremena.</span><span class="sxs-lookup"><span data-stu-id="e0c32-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-149">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-150">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-151">Fakturisanje transakcije materijala koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="e0c32-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-152">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.</span><span class="sxs-lookup"><span data-stu-id="e0c32-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-153">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="e0c32-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e0c32-154">Fakturisanje naknade.</span><span class="sxs-lookup"><span data-stu-id="e0c32-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-155">Storniranje nenaplaćene prodaje za iznos naknade u originalnoj stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="e0c32-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-156">Naplaćeni stvarni iznos prodaje za količinu i iznos u originalnoj stavci u glavnoj knjizi za naknadu.</span><span class="sxs-lookup"><span data-stu-id="e0c32-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e0c32-157">Fakturisanje kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="e0c32-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-158">Naplaćeni stvarni iznos prodaje za iznos kontrolne tačke na originalnoj kontrolnoj tački u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="e0c32-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e0c32-159">Fakturisanje predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="e0c32-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e0c32-160">Naplaćeni stvarni iznos prodaje za liniju proizvoda sa količinom i iznosom koji potiču iz predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="e0c32-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
