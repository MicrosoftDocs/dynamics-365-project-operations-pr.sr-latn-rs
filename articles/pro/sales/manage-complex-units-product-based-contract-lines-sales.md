---
title: Upravljanje složenim jedinicama za predmete ugovora zasnovane na proizvodima – jednostavno
description: Ova tema pruža informacije o podršci prodaji proizvoda zasnovanih na pretplati.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273350"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="ce3a4-103">Upravljanje složenim jedinicama za predmete ugovora zasnovane na proizvodima – jednostavno</span><span class="sxs-lookup"><span data-stu-id="ce3a4-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="ce3a4-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ce3a4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ce3a4-105">Dynamics 365 Project Operations koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="ce3a4-106">Za proizvode zasnovane na pretplati, količina ugovoru ili predmetu ugovora o projektu izražena je kao broj korisničkih meseci.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="ce3a4-107">Cena softvera za pretplatu se čuva u katalogu kao cena po korisniku mesečno.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="ce3a4-108">Tokom procesa prodaje, cena u predmetu ugovora je obično cena po korisniku mesečno, do koje se došlo pregovorima i popustima od strane agenta prodaje.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="ce3a4-109">Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="ce3a4-110">Količina koja se koristi za izračunavanje iznosa predmeta ugovora je proizvod broja korisnika i broja meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="ce3a4-111">Da bi podržao ovu vrstu prodaje, Project Operations podržava koncept *faktora količine*.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="ce3a4-112">Količinski faktori se oslanjaju na atribute proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="ce3a4-113">Kada konfigurišete određene osobine proizvoda, možete da označite podskup tih svojstava ili sva svojstva kao faktore količine.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="ce3a4-114">Project Operations potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="ce3a4-115">Kada se proizvod sa konfigurisanim faktorima količine doda predmetu ugovora, polje **Količina** postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="ce3a4-116">Kada unesete vrednosti za svojstva proizvoda koja su količinski faktori, Project Operations izračunava količinu predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="ce3a4-117">Na primer, Dynamics 365 Sales može imati sledeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="ce3a4-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="ce3a4-118">**Br. korisnika**: broj korisnika.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="ce3a4-119">**Br. meseci**: broj meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="ce3a4-120">**SKU proizvoda**: Jedinica za čuvanje zaliha (SKU) za proizvod.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="ce3a4-121">Svojstva **Br. korisnika** i **Br. meseci** se mogu označiti kao faktori količine, uređivanjem svojstava u stavci proizvoda.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="ce3a4-122">Da biste kreirali faktore količine iz svojstava proizvoda, obavite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="ce3a4-123">U usluzi **Project Operations** izaberite **Prodaja-proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="ce3a4-124">Otvorite proizvod za koji treba da podesite faktore količine.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="ce3a4-125">Uverite se da proizvod ima svojstva koja su već podešena.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="ce3a4-126">Na stranici **Informacije o projektu** izaberite karticu **Faktori količine**.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="ce3a4-127">U podformi izaberite **Novi obračun polja**.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="ce3a4-128">Unesite naziv **faktora količine** i izaberite vrednost svojstva koje se mapira u obračun polja.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="ce3a4-129">Sačuvajte i zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-129">Save and close the form.</span></span>
7. <span data-ttu-id="ce3a4-130">Ponovite korake 2–6 za sva svojstva koja će zajedno činiti količinu za predmet ugovora zasnovan na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="ce3a4-131">Kada se postave faktori količine, kada korisnik kreira predmet ugovora za ovaj proizvod, količina predmeta ugovora se zaključava.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="ce3a4-132">Količina se zatim izračunava kao proizvod vrednosti svojstva za taj predmet ugovora.</span><span class="sxs-lookup"><span data-stu-id="ce3a4-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]