---
title: Pregled predmeta ugovora zasnovanih na proizvodu – jednostavno
description: Ova tema pruža informacije o predmetima ugovora zasnovanim na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177888"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="b80ab-103">Pregled predmeta ugovora zasnovanih na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="b80ab-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="b80ab-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="b80ab-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b80ab-105">U usluzi Dynamics 365 Project Operations možete kreirati predmete ugovora zasnovane na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="b80ab-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="b80ab-106">To mogu da budu ručno kreirane stavke ili stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b80ab-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="b80ab-107">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="b80ab-107">Product catalog</span></span>

<span data-ttu-id="b80ab-108">Proizvodi u katalogu proizvoda imaju podrazumevanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="b80ab-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="b80ab-109">Ako nekoliko proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe ima te atribute.</span><span class="sxs-lookup"><span data-stu-id="b80ab-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="b80ab-110">Svi proizvodi iz jedne grupe proizvoda nasljeđuju isti skup atributa.</span><span class="sxs-lookup"><span data-stu-id="b80ab-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="b80ab-111">Na primer, kompanija prodaje licence za pretplatu na razne vrste softvera.</span><span class="sxs-lookup"><span data-stu-id="b80ab-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="b80ab-112">Sav softver za pretplatu ima sledeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="b80ab-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="b80ab-113">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="b80ab-113">Number of users</span></span>
- <span data-ttu-id="b80ab-114">Trajanje pretplate (u mesecima)</span><span class="sxs-lookup"><span data-stu-id="b80ab-114">Subscription duration (in months)</span></span>

<span data-ttu-id="b80ab-115">Da biste održali ovu vrstu kataloga, kreirajte porodicu proizvoda koja nosi ime **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="b80ab-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="b80ab-116">Dodajte atribute, **Broj korisnika** i **Trajanje pretplate** porodici proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b80ab-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="b80ab-117">Zatim dodajte pojedinačne proizvode u porodicu proizvoda **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="b80ab-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="b80ab-118">Dodavanje stavki iz kataloga proizvoda u ugovor</span><span class="sxs-lookup"><span data-stu-id="b80ab-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="b80ab-119">Ugovori projekata imaju odeljke za dve vrste stavki, stavke zasnovane na projektu i stavke zasnovane na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="b80ab-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="b80ab-120">Stavke zasnovane na proizvodu uključuju sve proizvode i jedinice u cenovniku proizvoda na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b80ab-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="b80ab-121">Možete da dodate proizvode koji nisu deo cenovnika proizvoda ugovora.</span><span class="sxs-lookup"><span data-stu-id="b80ab-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="b80ab-122">Možete odabrati proizvode iz drugih cenovnika ili direktno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b80ab-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="b80ab-123">Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda za prodajnu cenu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b80ab-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="b80ab-124">Ako podrazumevani cenovnik nije podešen, cena se podešava na 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="b80ab-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="b80ab-125">Ako se predmet ugovora temelji na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="b80ab-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="b80ab-126">Predmet ugovora sadrži polje **Cene** sa dve vrednosti:</span><span class="sxs-lookup"><span data-stu-id="b80ab-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="b80ab-127">**Izmena načina određivanja cena**</span><span class="sxs-lookup"><span data-stu-id="b80ab-127">**Override pricing**</span></span>
- <span data-ttu-id="b80ab-128">**Koristi podrazumevano**</span><span class="sxs-lookup"><span data-stu-id="b80ab-128">**Use default**</span></span>

<span data-ttu-id="b80ab-129">Ako polje **Cene** podesite na **Izmena načina određivanja cena**, podrazumevana cena se ne podešava.</span><span class="sxs-lookup"><span data-stu-id="b80ab-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="b80ab-130">Unesite cenu za proizvod u predmetu ugovora.</span><span class="sxs-lookup"><span data-stu-id="b80ab-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="b80ab-131">Ako polje postavite na **Koristi podrazumevane vrednosti**, koristi se podrazumevana prodajna cena i polje se ne može uređivati.</span><span class="sxs-lookup"><span data-stu-id="b80ab-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="b80ab-132">Nakon što instalirate Project Operations, podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ugovora.</span><span class="sxs-lookup"><span data-stu-id="b80ab-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="b80ab-133">Polje **Određivanje cena** se podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u predmetima ugovora.</span><span class="sxs-lookup"><span data-stu-id="b80ab-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="b80ab-134">Ovo je izmena ponašanja stavki zasnovanih na proizvodima specifična za Project Operations u usluzi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b80ab-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
