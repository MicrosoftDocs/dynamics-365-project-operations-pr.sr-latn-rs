---
title: Prijem stavki po narudžbenici iz zahteva za stavku
description: Ovaj tema objašnjava kako da primite stavke na narudžbenici iz zahteva za stavku.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083747"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="aa8bd-103">Prijem stavki po narudžbenici iz zahteva za stavku</span><span class="sxs-lookup"><span data-stu-id="aa8bd-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa8bd-104">Ovaj tema objašnjava kako da primite stavke na narudžbenici iz zahteva za stavku.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="aa8bd-105">Korišćenjem zahteva za stavku umesto transakcije sa stavkom, možete da planirate isporuku neposredno pre nego što se stavka stvarno koristi, kreirate narudžbenicu, stavku uključite u okvir trgovinskog sporazuma i uključite zahtev za stavku u planiranje proizvodnje.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="aa8bd-106">Ovaj zadatke koristi USSI skup podataka.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="aa8bd-107">U oknu za navigaciju, idite na **Moduli > Upravljanje projektima i računovodstvo > Projekti > Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="aa8bd-108">Na listi, izaberite vezu u željenom redu.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="aa8bd-109">U oknu radnji, izaberite **Plan**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="aa8bd-110">Izaberite **Zahtevi za stavku**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="aa8bd-111">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-111">Select **New**.</span></span>
6. <span data-ttu-id="aa8bd-112">U novom redu unesite ili izaberite vrednost u polju **Broj stavke**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="aa8bd-113">U polje **Količina** unesite broj.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="aa8bd-114">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-114">Select **Save**.</span></span>
9. <span data-ttu-id="aa8bd-115">U oknu radnji izaberite **Upravljaj**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="aa8bd-116">Izaberite **Funkcije**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-116">Select **Functions**.</span></span>
11. <span data-ttu-id="aa8bd-117">Izaberite **Kreiranje porudžbenice**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="aa8bd-118">Izaberite polje za potvrdu **Uključi sve**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="aa8bd-119">U polju **Poslovni kontakt prodavca** unesite ili izaberite vrednost.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="aa8bd-120">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-120">Select **OK**.</span></span>
15. <span data-ttu-id="aa8bd-121">U oknu za navigaciju idite na **Moduli > Dugovanja > Porudžbenice > Sve porudžbenice**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="aa8bd-122">Na listi, izaberite vezu u željenom redu.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="aa8bd-123">U oknu radnji izaberite **Kupi**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="aa8bd-124">Izaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="aa8bd-125">U oknu radnji izaberite **Prijem**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="aa8bd-126">Izaberite **Prijem proizvoda**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="aa8bd-127">U polju **Prijem proizvoda** , otkucajte vrednost.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="aa8bd-128">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="aa8bd-128">Select **OK**.</span></span>

