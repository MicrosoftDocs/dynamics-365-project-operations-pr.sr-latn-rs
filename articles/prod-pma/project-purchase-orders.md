---
title: Porudžbenice za projekat
description: Ovaj članak opisuje razne metode pomoću kojih možete da kreirate porudžbenice za projekat. Način koji koristite zavisi od svrhe porudžbenice i od toga kada se kupljene stavke koriste i naplaćuju projektu.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999373"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="dc16e-104">Porudžbenice za projekat</span><span class="sxs-lookup"><span data-stu-id="dc16e-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc16e-105">Ovaj članak opisuje razne metode pomoću kojih možete da kreirate porudžbenice za projekat.</span><span class="sxs-lookup"><span data-stu-id="dc16e-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="dc16e-106">Način koji koristite zavisi od svrhe porudžbenice i od toga kada se kupljene stavke koriste i naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="dc16e-107">Metode za kreiranje porudžbenice</span><span class="sxs-lookup"><span data-stu-id="dc16e-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="dc16e-108">Možete da koristite jedan od sledećih metoda za kreiranje porudžbenice u upravljanju projektima i računovodstvu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="dc16e-109">Svrha porudžbenice određuje kada se porudžbenica koristi i, stoga, kada se stavke naplaćuju projektu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dc16e-110">Metod</span><span class="sxs-lookup"><span data-stu-id="dc16e-110">Method</span></span></th>
<th><span data-ttu-id="dc16e-111">Svrha</span><span class="sxs-lookup"><span data-stu-id="dc16e-111">Purpose</span></span></th>
<th><span data-ttu-id="dc16e-112">Potrošnja stavki</span><span class="sxs-lookup"><span data-stu-id="dc16e-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc16e-113">Kreirajte porudžbenicu direktno iz projekta.</span><span class="sxs-lookup"><span data-stu-id="dc16e-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="dc16e-114">Ovu metodu koristite za kupovinu stavki od spoljnog prodavca za potrošnju na projektu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="dc16e-115">Porudžbenicu možete kreirati na dva načina:</span><span class="sxs-lookup"><span data-stu-id="dc16e-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="dc16e-116">Iz samog projekta.</span><span class="sxs-lookup"><span data-stu-id="dc16e-116">From the project itself.</span></span> <span data-ttu-id="dc16e-117">U ovom slučaju, projekat je već definisan za porudžbenicu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="dc16e-118">Navigacijom do porudžbenice za projekat.</span><span class="sxs-lookup"><span data-stu-id="dc16e-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="dc16e-119">Morate izabrati prodavca i projekat za koji ćete kreirati porudžbenicu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="dc16e-120">Stavke se koriste kada se faktura dobavljača ažurira.</span><span class="sxs-lookup"><span data-stu-id="dc16e-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc16e-121">Kreirajte porudžbenicu direktno iz ulazne porudžbine.</span><span class="sxs-lookup"><span data-stu-id="dc16e-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="dc16e-122">Koristite ovaj metod za kupovinu stavki kada kreirate ulaznu porudžbinu iz projekta.</span><span class="sxs-lookup"><span data-stu-id="dc16e-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="dc16e-123">Stavke se koriste kada se porudžbenica fakturiše klijentu.</span><span class="sxs-lookup"><span data-stu-id="dc16e-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc16e-124">Kreirajte porudžbenicu na osnovu zahteva za stavku.</span><span class="sxs-lookup"><span data-stu-id="dc16e-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="dc16e-125">Koristite ovaj metod za kupovinu stavki kada kreirate zahtev za stavku iz projekta.</span><span class="sxs-lookup"><span data-stu-id="dc16e-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="dc16e-126">Stavke se koriste kada se ažurira otpremnica zahteva.</span><span class="sxs-lookup"><span data-stu-id="dc16e-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="dc16e-127">Kada ažurirate fakturu dobavljača ili otpremnicu, od vas će se zatražiti da ažurirate otpremnicu prema zahtevu za stavku.</span><span class="sxs-lookup"><span data-stu-id="dc16e-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="dc16e-128">Za više informacija pogledajte [Prijem stavki po porudžbenici iz zahteva za stavku](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="dc16e-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]