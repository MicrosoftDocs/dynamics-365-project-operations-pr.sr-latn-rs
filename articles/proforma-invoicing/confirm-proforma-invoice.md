---
title: Potvrda predračuna
description: Ova tema pruža informacije o potvrđivanju predračuna.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287885"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="149b4-103">Potvrda predračuna</span><span class="sxs-lookup"><span data-stu-id="149b4-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="149b4-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="149b4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="149b4-105">Nakon potvrde predračuna, status fakture projekta se ažurira na **Potvrđeno**.</span><span class="sxs-lookup"><span data-stu-id="149b4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="149b4-106">Kada se faktura potvrdi, postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="149b4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="149b4-107">Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijent, ili kada je faktura označena kao plaćena.</span><span class="sxs-lookup"><span data-stu-id="149b4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="149b4-108">U sledećoj tabeli su navedeni stvarni podaci koje je kreirao sistem.</span><span class="sxs-lookup"><span data-stu-id="149b4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="149b4-109">Ovi stvarni podaci se kreiraju kada se izvrše određene radnje na radnoj verziji fakture projekta pre nego što se ona potvrdi.</span><span class="sxs-lookup"><span data-stu-id="149b4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="149b4-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="149b4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="149b4-111">
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </span><span class="sxs-lookup"><span data-stu-id="149b4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="149b4-112">Fakturisanje vremenske transakcije bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="149b4-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-113">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="149b4-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-114">Naplaćeni stvarni iznos prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="149b4-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="149b4-115">Fakturisanje vremenske transakcije koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="149b4-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-116">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="149b4-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-117">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-118">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="149b4-119">Fakturisanje vremenske transakcije koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="149b4-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-120">Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.</span><span class="sxs-lookup"><span data-stu-id="149b4-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-121">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="149b4-122">Fakturisanje transakcije troškova bez ikakvih izmena na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="149b4-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-123">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="149b4-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-124">Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="149b4-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="149b4-125">Fakturisanje transakcije troškova koja je uređena da bi se smanjila količina.</span><span class="sxs-lookup"><span data-stu-id="149b4-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-126">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="149b4-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-127">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-128">Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="149b4-129">Fakturisanje transakcije troškova koja je uređena da bi se povećala količina.</span><span class="sxs-lookup"><span data-stu-id="149b4-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-130">Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.</span><span class="sxs-lookup"><span data-stu-id="149b4-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-131">Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.</span><span class="sxs-lookup"><span data-stu-id="149b4-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="149b4-132">Fakturisanje naknade.</span><span class="sxs-lookup"><span data-stu-id="149b4-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-133">Storniranje nenaplaćene prodaje za iznos naknade u originalnoj stavci u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="149b4-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-134">Naplaćeni stvarni iznos prodaje za količinu i iznos u originalnoj stavci u glavnoj knjizi za naknadu.</span><span class="sxs-lookup"><span data-stu-id="149b4-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="149b4-135">Fakturisanje kontrolne tačke.</span><span class="sxs-lookup"><span data-stu-id="149b4-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="149b4-136">Naplaćeni stvarni iznos prodaje za iznos kontrolne tačke na originalnoj kontrolnoj tački u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="149b4-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]