---
title: Stavke ponuda zasnovane na proizvodu
description: Ova tema pruža informacije o stavkama ponuda zasnovanim na proizvodu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde88f5f2d00c09129c6a9363c09f6f6ad1dd90
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284105"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="ae5b7-103">Stavke ponuda zasnovane na proizvodu</span><span class="sxs-lookup"><span data-stu-id="ae5b7-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="ae5b7-104">Možete kreirati stavke ponude zasnovane na proizvodu u aplikaciji Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="ae5b7-105">To mogu da budu stavke za unos ili stavke iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="ae5b7-106">Katalog proizvoda</span><span class="sxs-lookup"><span data-stu-id="ae5b7-106">Product catalog</span></span>

<span data-ttu-id="ae5b7-107">Proizvodi u Dynamics 365 katalogu proizvoda imaju podrazumevanu jedinicu i grupu jedinica.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="ae5b7-108">Ako nekoliko proizvoda deli isti skup atributa, možete da kreirate grupu proizvoda koja takođe ima te atribute.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="ae5b7-109">Svi proizvodi iz jedne grupe proizvoda nasljeđuju isti skup atributa.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="ae5b7-110">Na primer, kompanija prodaje licence za pretplatu na razni softver.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="ae5b7-111">Sav softver za pretplatu ima sledeća dva atributa:</span><span class="sxs-lookup"><span data-stu-id="ae5b7-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="ae5b7-112">Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="ae5b7-112">Number of users</span></span> 
- <span data-ttu-id="ae5b7-113">Trajanje pretplate (u mesecima)</span><span class="sxs-lookup"><span data-stu-id="ae5b7-113">Subscription duration (in months)</span></span>

<span data-ttu-id="ae5b7-114">Dobar način za održavanje ove vrste kataloga je kreiranje grupe proizvoda pod imenom **Softver za pretplatu** i sa atributima **Broj korisnika** i **Trajanje pretplate**.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="ae5b7-115">Zatim možete dodati pojedinačne proizvode, kao što su **Dynamics 365 Sales** ili **Dynamics 365 Field Service** u grupu proizvoda **Softver za pretplatu**.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="ae5b7-116">Dodavanje stavki iz kataloga proizvoda u ponudu za projekat</span><span class="sxs-lookup"><span data-stu-id="ae5b7-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="ae5b7-117">Stranica sa ponudom za projekat i stranica ugovora imaju odeljke za dve vrste stavki: stavke zasnovane na projektu i stavke zasnovane na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="ae5b7-118">Za stavke zasnovane na proizvodu, Dynamics 365 se koristi za dodavanje stavki iz kataloga proizvoda u ponudu.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="ae5b7-119">Padajuća lista u okviru stavke ponude ili predmeta ugovora za projekat uključuje sve proizvode i jedinice u cenovniku proizvoda koji je priložen uz ponudu ili ugovor o projektu.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="ae5b7-120">Takođe možete da dodate proizvode koji nisu deo cenovnika proizvoda ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="ae5b7-121">Pored toga, možete odabrati proizvode iz drugih cenovnika ili možete odabrati proizvode direktno iz kataloga proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="ae5b7-122">Kada izaberete proizvode direktno iz kataloga proizvoda, koristi se podrazumevani cenovnik tog proizvoda da biste dobili prodajnu cenu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="ae5b7-123">Ako podrazumevani cenovnik nije podešen, cena se podešava na 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="ae5b7-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="ae5b7-124">Ako se stavka ponude temelji na katalogu proizvoda, možete izmeniti prodajnu cenu direktno u stavci ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="ae5b7-125">Imajte na umu da stavka ponude u sistemu Dynamics 365 ima polje **Određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="ae5b7-126">Dostupne su dve vrednosti:</span><span class="sxs-lookup"><span data-stu-id="ae5b7-126">Two values are available:</span></span>

- <span data-ttu-id="ae5b7-127">Izmena načina određivanja cena</span><span class="sxs-lookup"><span data-stu-id="ae5b7-127">Override pricing</span></span>  
- <span data-ttu-id="ae5b7-128">Koristi podrazumevane cene</span><span class="sxs-lookup"><span data-stu-id="ae5b7-128">Use default</span></span>

<span data-ttu-id="ae5b7-129">Ako ovo polje podesite na **Izmena načina određivanja cena**, Dynamics 365 ne podešava podrazumevanu cenu.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="ae5b7-130">Morate da unesete cenu proizvoda u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="ae5b7-131">Ako ovo polje podesite na **Koristi podrazumevane cene**, Dynamics 365 koristi podrazumevane prodajne cene i zaključava polje radi sprečavanja uređivanja.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="ae5b7-132">Nakon što instalirate PSA, podrazumevane prodajne cene se unose u stavke zasnovane na proizvodima u okviru ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="ae5b7-133">Polje **Određivanje cena** se tada podešava na **Izmeni način određivanja cena** tako da možete da uredite podrazumevanu cenu u stavkama ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Podešavanje izmene načina određivanja cena](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="ae5b7-135">Količinski faktori proizvoda</span><span class="sxs-lookup"><span data-stu-id="ae5b7-135">Quantity factors for products</span></span>

<span data-ttu-id="ae5b7-136">PSA koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="ae5b7-137">Za proizvode zasnovane na pretplati, količina u stavci ponude ili predmetu ugovora o projektu izražena je kao broj korisničkih meseci.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="ae5b7-138">Obično se cena softvera za pretplatu čuva u katalogu kao cena po korisniku mesečno.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="ae5b7-139">Međutim, umesto toga možete koristiti opise drugih perioda.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="ae5b7-140">Tokom procesa prodaje, cena u stavci ponude je obično cena po korisniku, mesečno, do koje se došlo pregovorima i popustima od strane IT agenta prodaje.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="ae5b7-141">Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="ae5b7-142">Količina koja se koristi za izračunavanje količine stavke ponude je proizvod broja korisnika i broja meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="ae5b7-143">Da bi podržao ovu vrstu prodaje, PSA je uveo koncept faktora količine.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="ae5b7-144">Količinski faktori se oslanjaju na atribute proizvoda u sistemu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="ae5b7-145">Kada konfigurišete određene osobine proizvoda, PSA vam omogućava da označite podskup tih svojstava ili sva svojstva kao faktore količine.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="ae5b7-146">PSA potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="ae5b7-147">Kada se proizvod za koji su konfigurisani faktori količine doda u stavku ponude, polje **Količina** u stavci ponude postaje polje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="ae5b7-148">Nakon što unesete vrednosti za svojstva proizvoda koja su količinski faktori, PSA izračunava količinu stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="ae5b7-149">Na primer, Dynamics 365 može imati sledeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="ae5b7-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="ae5b7-150">**Br. korisnika** - Broj korisnika</span><span class="sxs-lookup"><span data-stu-id="ae5b7-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="ae5b7-151">**Br. meseci** - Broj meseci pretplate</span><span class="sxs-lookup"><span data-stu-id="ae5b7-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="ae5b7-152">**SKU proizvoda**</span><span class="sxs-lookup"><span data-stu-id="ae5b7-152">**Product SKU**</span></span> 

<span data-ttu-id="ae5b7-153">Svojstva **Br. korisnika** i **Br. meseci** se mogu označiti kao faktori količine, uređivanjem svojstava u stavci proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ae5b7-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Označavanje broja korisnika i broja meseci kao faktora kvaliteta](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]