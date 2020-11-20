---
title: Jedinice i grupe jedinica
description: Ova tema pruža informacije o tome kako da kreirate jedinice i grupe jedinica u sistemu Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f588e41d001befeac87bb6a4e28a83cf5cfa865
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131045"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="49cfc-103">Jedinice i grupe jedinica</span><span class="sxs-lookup"><span data-stu-id="49cfc-103">Units and unit groups</span></span>

<span data-ttu-id="49cfc-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="49cfc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="49cfc-105">Jedinice su količine ili mere u kojima prodajete proizvode ili usluge.</span><span class="sxs-lookup"><span data-stu-id="49cfc-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="49cfc-106">Na primer, ako prodajete pribor za baštovanstvo, možda prodajete seme u jedinicama paketa, kutija i paleta.</span><span class="sxs-lookup"><span data-stu-id="49cfc-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="49cfc-107">Grupa jedinica je kolekcija različitih jedinica.</span><span class="sxs-lookup"><span data-stu-id="49cfc-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="49cfc-108">Da biste dovršili korake u ovoj temi, uverite se da vam je dodeljena uloga Administrator sistema ili Menadžer za Sales Professional ili da imate ekvivalentne dozvole.</span><span class="sxs-lookup"><span data-stu-id="49cfc-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="49cfc-109">Kreiranje grupe jedinica</span><span class="sxs-lookup"><span data-stu-id="49cfc-109">Create a unit group</span></span>

1. <span data-ttu-id="49cfc-110">Na mapi lokacije, izaberite **Jedinice**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="49cfc-111">Izaberite **Novo** i u dijalogu **Kreiranje grupe jedinica** unesite naziv jedinice.</span><span class="sxs-lookup"><span data-stu-id="49cfc-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="49cfc-112">U polju **Primarna jedinica** unesite najnižu zajedničku mernu jedinicu u kojoj će se proizvod prodavati.</span><span class="sxs-lookup"><span data-stu-id="49cfc-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="49cfc-113">Na primer, možete uneti „komad“ ili „unca“.</span><span class="sxs-lookup"><span data-stu-id="49cfc-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="49cfc-114">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="49cfc-115">Dodavanje jedinica u grupu jedinica</span><span class="sxs-lookup"><span data-stu-id="49cfc-115">Add units to a unit group</span></span>

1. <span data-ttu-id="49cfc-116">Otvorite grupu jedinica i na kartici **Povezano** izaberite **Jedinice**.</span><span class="sxs-lookup"><span data-stu-id="49cfc-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="49cfc-117">Videćete da je primarna jedinica već dodata.</span><span class="sxs-lookup"><span data-stu-id="49cfc-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="49cfc-118">Izaberite **Dodaj novu jedinicu** i na stranici **Brzo kreiranje: jedinica**, u polju **Naziv**, unesite naziv jedinice.</span><span class="sxs-lookup"><span data-stu-id="49cfc-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="49cfc-119">U polju **Količina** unesite količinu koju želite da jedinica sadrži.</span><span class="sxs-lookup"><span data-stu-id="49cfc-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="49cfc-120">Na primer, ako kutija sadrži dva komada, unesite „2“.</span><span class="sxs-lookup"><span data-stu-id="49cfc-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="49cfc-121">U polju **Osnovna jedinica** izaberite osnovnu jedinicu da biste uspostavili najnižu mernu jedinicu za jedinicu.</span><span class="sxs-lookup"><span data-stu-id="49cfc-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="49cfc-122">Na primer, možete odabrati „Komad“.</span><span class="sxs-lookup"><span data-stu-id="49cfc-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="49cfc-123">Izaberite **Sačuvaj**:</span><span class="sxs-lookup"><span data-stu-id="49cfc-123">Select **Save**:</span></span>
