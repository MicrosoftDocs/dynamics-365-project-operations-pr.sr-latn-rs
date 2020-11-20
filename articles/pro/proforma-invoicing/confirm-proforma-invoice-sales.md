---
title: Potvrđivanje predračuna – jednostavno
description: Ova tema pruža informacije o potvrđivanju predračuna u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176538"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="ce5e5-103">Potvrđivanje predračuna – jednostavno</span><span class="sxs-lookup"><span data-stu-id="ce5e5-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="ce5e5-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ce5e5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ce5e5-105">Nakon potvrde predračuna, status fakture projekta se ažurira na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="ce5e5-106">Kada se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="ce5e5-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijent, ili ukoliko je faktura označena kao plaćena.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="ce5e5-108">U sledećoj tabeli su navedeni stvarni podaci koje je kreirao sistem.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="ce5e5-109">Ovi stvarni podaci se kreiraju kada se izvrše određene radnje na radnoj verziji fakture projekta pre nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="ce5e5-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ce5e5-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="ce5e5-111">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="ce5e5-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-112">Fakturisanje avansa ili odbitka</span><span class="sxs-lookup"><span data-stu-id="ce5e5-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-113">Fakturisani stvarni iznos prodaje, <strong>Odbitak</strong> kreira se za iznos na avansu ili obustavi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-114">Stvarna nenaplaćena prodaja negativnog iznosa obustave ili avansa, koja će se koristiti za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-115">Nakon potpunog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-116">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ce5e5-117">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-118">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ce5e5-119">Nakon delimičnog sravnjenja obustave ili avansa na fakturi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-120">Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="ce5e5-121">Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-122">Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-123">Negativna stvarna nenaplaćena prodaja preostalog iznosa obustave ili avansa, koja će se koristiti za sravnjenje na budućim fakturama.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-124">Fakturisanje vremenske transakcije bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-125">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-126">Naplaćeni stvarni iznos prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ce5e5-127">Fakturisanje vremenske transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-128">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-129">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-130">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-131">Fakturisanje vremenske transakcije koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-132">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-133">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-134">Fakturisanje transakcije troškova bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-135">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-136">Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove</span><span class="sxs-lookup"><span data-stu-id="ce5e5-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="ce5e5-137">Fakturisanje transakcije troškova koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-138">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-139">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-140">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-141">Fakturisanje transakcije troškova koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-142">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-143">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="ce5e5-144">Fakturisanje naknade.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-145">Storniranje nenaplaćene prodaje za iznos naknade u originalnoj stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-146">Naplaćeni stvarni iznos prodaje za količinu i iznos u originalnoj stavci u glavnoj knjizi za naknadu.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ce5e5-147">Fakturisanje kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-148">Naplaćeni stvarni iznos prodaje za iznos kontrolne tačke na originalnoj kontrolnoj tački u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="ce5e5-149">Fakturisanje predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="ce5e5-150">Naplaćeni stvarni iznos prodaje za liniju proizvoda sa količinom i iznosom koji potiču iz predmeta ugovora zasnovanog na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="ce5e5-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
