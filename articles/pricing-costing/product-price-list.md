---
title: Cenovnici proizvoda
description: Ova tema pruža informacije o cenovnicima u kataloškim cenama koji se koriste za ponude za projekat i ugovore.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877507"
---
# <a name="product-price-lists"></a><span data-ttu-id="804ba-103">Cenovnici proizvoda</span><span class="sxs-lookup"><span data-stu-id="804ba-103">Product price lists</span></span>

<span data-ttu-id="804ba-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="804ba-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="804ba-105">U usluzi Project Operations, **cenovnici proizvoda** i povezani entiteti stavke cenovnika podržavaju funkcionalnost određivanja cena proizvoda prema ponudi zasnovanoj na proizvodima i predmetima ugovora.</span><span class="sxs-lookup"><span data-stu-id="804ba-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="804ba-106">Za proizvode koji se koriste na projektima, koriste se zapisi stavki cenovnika za cenovnike projekata.</span><span class="sxs-lookup"><span data-stu-id="804ba-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="804ba-107">Proizvodi treba da budu podešeni tako da u katalogu proizvoda imaju podrazumevane troškove i cenovnike.</span><span class="sxs-lookup"><span data-stu-id="804ba-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="804ba-108">Koristite cenovnik, standardnu cenu i trenutnu cenu da biste konfigurisali podrazumevanu cenu i cenovnik.</span><span class="sxs-lookup"><span data-stu-id="804ba-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="804ba-109">Podrazumevane cene na listi koriste se u stavci ponude ili predmetu ugovora o projektu samo kada sistem ne može da pronađe stavku cenovnika za taj proizvod u cenovniku proizvoda za ponudu ili ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="804ba-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="804ba-110">Cena koštanja stavki kataloga proizvoda može se menjati između ponuda.</span><span class="sxs-lookup"><span data-stu-id="804ba-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="804ba-111">Ova mogućnost je važna, jer ako ne pratite tačno troškove, ne možete da odredite operativni profit od projektnih angažmanima.</span><span class="sxs-lookup"><span data-stu-id="804ba-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="804ba-112">Standardna cena proizvoda se podrazumevano koristi kao cena koštanja.</span><span class="sxs-lookup"><span data-stu-id="804ba-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="804ba-113">Međutim, podrazumevana cena koštanja može se ažurirati u stavci ponude ako za tu ponudu postoji drugačija cena.</span><span class="sxs-lookup"><span data-stu-id="804ba-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="804ba-114">Stavke cenovnika</span><span class="sxs-lookup"><span data-stu-id="804ba-114">Price list items</span></span>

<span data-ttu-id="804ba-115">Možete da dodate proizvode iz kataloga proizvoda u različite cenovnike.</span><span class="sxs-lookup"><span data-stu-id="804ba-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="804ba-116">Stavke cenovnika za proizvode uvek upućuju na određenu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="804ba-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="804ba-117">Cene proizvoda u stavkama cenovnika se mogu konfigurisati kao iznos valute.</span><span class="sxs-lookup"><span data-stu-id="804ba-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="804ba-118">Alternativno, mogu se konfigurisati kao funkcija cenovnika, trenutne cene ili standardne cene.</span><span class="sxs-lookup"><span data-stu-id="804ba-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="804ba-119">Funkcionalnost određivanja cena podržava različite opcije zaokruživanja kada su cene proizvoda konfigurisane kao funkcija cenovnika, standardna cena ili trenutna cena.</span><span class="sxs-lookup"><span data-stu-id="804ba-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="804ba-120">Pored toga što možete iskoristiti više metoda određivanja cena i mogućnosti zaokruživanja, liste popusta možete povezati sa stavkama cenovnika.</span><span class="sxs-lookup"><span data-stu-id="804ba-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="804ba-121">Podrazumevani cenovnik proizvoda</span><span class="sxs-lookup"><span data-stu-id="804ba-121">Default product price list</span></span>
<span data-ttu-id="804ba-122">Svaki zapis klijenta ima polje **Podrazumevani cenovnik**, gde možete odrediti cenovnik koji odgovara valuti klijenta.</span><span class="sxs-lookup"><span data-stu-id="804ba-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="804ba-123">Podrazumevana vrednost se ne unosi u ovo polje automatski.</span><span class="sxs-lookup"><span data-stu-id="804ba-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="804ba-124">Kada postoji prilagođeni ugovor o cenama sa određenim klijentom, ovo polje možete koristiti da biste povezali cenovnik sa tim klijentom.</span><span class="sxs-lookup"><span data-stu-id="804ba-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="804ba-125">Entiteti Mogućnost za poslovanje, Ponuda i Ugovor o projektu koriste sledeći redosled za unošenje podrazumevanih cenovnika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="804ba-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="804ba-126">Isti redosled se koristi za cenovnike projekata.</span><span class="sxs-lookup"><span data-stu-id="804ba-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="804ba-127">Ponuda</span><span class="sxs-lookup"><span data-stu-id="804ba-127">Quote</span></span>
2.  <span data-ttu-id="804ba-128">Mogućnost za poslovanje</span><span class="sxs-lookup"><span data-stu-id="804ba-128">Opportunity</span></span>
3.  <span data-ttu-id="804ba-129">Klijent</span><span class="sxs-lookup"><span data-stu-id="804ba-129">Customer</span></span>
4.  <span data-ttu-id="804ba-130">Globalna podešavanja</span><span class="sxs-lookup"><span data-stu-id="804ba-130">Global settings</span></span> 

<span data-ttu-id="804ba-131">Polje **Proizvod** u stavci ponude podrazumevano navodi sve aktivne proizvode u cenovniku proizvoda za ponudu.</span><span class="sxs-lookup"><span data-stu-id="804ba-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="804ba-132">Ako proizvod nije aktiviran ili je radna verzija proizvoda, on nije naveden, čak i ako je u cenovniku.</span><span class="sxs-lookup"><span data-stu-id="804ba-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="804ba-133">Stavke kataloga proizvoda dodaju se kao stavke fakture na prvoj fakturi koja je kreirana za ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="804ba-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="804ba-134">U radnoj verziji fakture te stavke fakture mogu se izbrisati.</span><span class="sxs-lookup"><span data-stu-id="804ba-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="804ba-135">U tom slučaju, stavke će se pojaviti na narednoj fakturi dok se ne fakturišu ili dok se faktura ne pošalje klijentu.</span><span class="sxs-lookup"><span data-stu-id="804ba-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="804ba-136">Ne možete fakturisati delimičnu količinu stavke fakture za proizvod.</span><span class="sxs-lookup"><span data-stu-id="804ba-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="804ba-137">Kada se fakturišu stavke proizvoda iz projektnog ugovora, kreiraju se stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="804ba-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="804ba-138">Međutim, ove stvarne vrednosti nisu povezane sa srodnim entitetom projekta.</span><span class="sxs-lookup"><span data-stu-id="804ba-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="804ba-139">Drugim rečima, predmeti ugovora zasnovani na proizvodima ne zavise ni od kakve upotrebe zasnovane na projektu.</span><span class="sxs-lookup"><span data-stu-id="804ba-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
