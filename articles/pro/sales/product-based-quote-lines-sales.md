---
title: Pregled stavki ponude zasnovane na proizvodu – jednostavno
description: Ova tema pruža informacije o radu sa stavkama ponude zasnovanim na proizvodu.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8b904f9abd3d2505c5397906f63a5ae8ff4be41b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369843"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="06752-103">Pregled stavki ponude zasnovane na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="06752-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="06752-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="06752-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="06752-105">Možete kreirati stavke ponude zasnovane na proizvodu u aplikaciji Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="06752-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="06752-106">Stavke ponude zasnovane na proizvodu možete dodati ručno ili to mogu da budu stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="06752-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="06752-107">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="06752-107">Product catalog</span></span>

<span data-ttu-id="06752-108">Svaki proizvod u katalogu proizvoda ima podrazumevanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="06752-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="06752-109">Ako više proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe deli te atribute.</span><span class="sxs-lookup"><span data-stu-id="06752-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="06752-110">Na primer, kompanija prodaje licence za pretplatu na razne vrste softvera.</span><span class="sxs-lookup"><span data-stu-id="06752-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="06752-111">Sav softver za pretplatu ima sledeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="06752-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="06752-112">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="06752-112">Number of users</span></span>
- <span data-ttu-id="06752-113">Trajanje pretplate, mereno u mesecima</span><span class="sxs-lookup"><span data-stu-id="06752-113">A subscription duration measured in months</span></span>

<span data-ttu-id="06752-114">Da biste održavali ovu vrstu kataloga, kreirajte porodicu proizvoda pod imenom **Softver za pretplatu** i dodajte broj korisnika i trajanje pretplate kao atribute.</span><span class="sxs-lookup"><span data-stu-id="06752-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="06752-115">Zatim možete da dodate pojedinačne proizvode u porodicu proizvoda **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="06752-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="06752-116">Dodavanje stavki iz kataloga proizvoda u ponudu za projekat</span><span class="sxs-lookup"><span data-stu-id="06752-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="06752-117">Stranice **Ponuda za projekat** i **Ugovor za projekat** imaju odeljke za stavke zasnovane na projektu i stavke zasnovane na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="06752-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="06752-118">Za stavke zasnovane na proizvodu, padajuća lista u okviru stavke ponude ili predmeta ugovora za projekat uključuje sve proizvode i jedinice u cenovniku proizvoda.</span><span class="sxs-lookup"><span data-stu-id="06752-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="06752-119">Takođe možete da dodate proizvode koji nisu deo cenovnika proizvoda.</span><span class="sxs-lookup"><span data-stu-id="06752-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="06752-120">Pored toga, možete odabrati proizvode iz drugih cenovnika ili direktno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="06752-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="06752-121">Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda da biste dobili prodajnu cenu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="06752-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="06752-122">Ako podrazumevani cenovnik nije podešen, cena se podešava na nula (0).</span><span class="sxs-lookup"><span data-stu-id="06752-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="06752-123">Kada se stavka ponude zasniva na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u stavci ponude.</span><span class="sxs-lookup"><span data-stu-id="06752-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="06752-124">Stavka ponude u polju **Određivanje cene** sa dve dostupne vrednosti:</span><span class="sxs-lookup"><span data-stu-id="06752-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="06752-125">**Izmena načina određivanja cena**</span><span class="sxs-lookup"><span data-stu-id="06752-125">**Override Pricing**</span></span>
- <span data-ttu-id="06752-126">**Koristi podrazumevano**</span><span class="sxs-lookup"><span data-stu-id="06752-126">**Use Default**</span></span>

<span data-ttu-id="06752-127">Ako izaberete **Izmena načina određivanja cena**, podrazumevana cena se ne postavlja.</span><span class="sxs-lookup"><span data-stu-id="06752-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="06752-128">Umesto toga, morate da unesete cenu proizvoda u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="06752-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="06752-129">Ako izaberete **Koristi podrazumevano**, koristi se podrazumevana prodajna cena i polje se zaključava za uređivanje.</span><span class="sxs-lookup"><span data-stu-id="06752-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="06752-130">Podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ponude.</span><span class="sxs-lookup"><span data-stu-id="06752-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="06752-131">Polje **Određivanje cena** se tada podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u stavkama ponude.</span><span class="sxs-lookup"><span data-stu-id="06752-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="06752-132">Ovo je ponašanje specifično za Project Operations pri izmeni stavki zasnovanih na proizvodima u usluzi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="06752-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]