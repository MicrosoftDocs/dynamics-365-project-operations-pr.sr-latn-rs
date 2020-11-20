---
title: Upravljanje složenim jedinicama, kao što su stavke ponude zasnovane na proizvodu po korisniku mesečno – jednostavno
description: Ova tema pruža informacije o upravljanju složenim jedinicama za stavke ponude zasnovane na proizvodu.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2ee46da2f663ef4f5f8fc7f9f89b6fcfd09a1798
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175593"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="7d581-103">Upravljanje složenim jedinicama, kao što su stavke ponude zasnovane na proizvodu po korisniku mesečno – jednostavno</span><span class="sxs-lookup"><span data-stu-id="7d581-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="7d581-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="7d581-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d581-105">Dynamics 365 Project Operations koristi količinske faktore da podrži prodaju proizvoda zasnovanih na pretplati.</span><span class="sxs-lookup"><span data-stu-id="7d581-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="7d581-106">Za proizvode zasnovane na pretplati, količina stavki ponude ili predmeta ugovora o projektu izražava se kao broj korisnik-meseci.</span><span class="sxs-lookup"><span data-stu-id="7d581-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="7d581-107">Obično se cena softvera za pretplatu čuva u katalogu kao cena po korisniku mesečno.</span><span class="sxs-lookup"><span data-stu-id="7d581-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="7d581-108">Tokom procesa prodaje, cena u stavci ponude je obično cena po korisniku, mesečno, do koje se došlo pregovorima i popustima od strane IT agenta prodaje.</span><span class="sxs-lookup"><span data-stu-id="7d581-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="7d581-109">Svaka pogodba ima različit broj korisnika i različit broj meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="7d581-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="7d581-110">Količina se koristi za izračunavanje stavke ponude je proizvod broja korisnika i broja meseci pretplate.</span><span class="sxs-lookup"><span data-stu-id="7d581-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="7d581-111">Da bi podržala ovu vrstu prodaje, usluga Project Operations uvodi koncept faktora količine.</span><span class="sxs-lookup"><span data-stu-id="7d581-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="7d581-112">Količinski faktori se oslanjaju na atribute proizvoda u sistemu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7d581-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="7d581-113">Kada konfigurišete određene osobine proizvoda, Project Operations vam omogućava da označite podskup tih svojstava ili sva svojstva kao faktore količine.</span><span class="sxs-lookup"><span data-stu-id="7d581-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="7d581-114">Project Operations potvrđuje da se kao faktori količine označavaju samo numerička svojstva ili svojstva proizvoda koja imaju numerički tip podataka.</span><span class="sxs-lookup"><span data-stu-id="7d581-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="7d581-115">Kada u red ponude dodate proizvod sa faktorima količine, polje **Količina** postaje samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="7d581-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="7d581-116">Kada unesete vrednosti za svojstva proizvoda koja su količinski faktori, Project Operations izračunava količinu stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="7d581-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="7d581-117">Na primer, Dynamics 365 Sales može imati sledeća svojstva:</span><span class="sxs-lookup"><span data-stu-id="7d581-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="7d581-118">**Br. korisnika**: broj korisnika</span><span class="sxs-lookup"><span data-stu-id="7d581-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="7d581-119">**Br. meseca**: broj meseci pretplate</span><span class="sxs-lookup"><span data-stu-id="7d581-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="7d581-120">**SKU proizvoda**</span><span class="sxs-lookup"><span data-stu-id="7d581-120">**Product SKU**</span></span>

<span data-ttu-id="7d581-121">Možete označiti **Broj korisnika** i **Broj meseci** kao faktore količine, uređivanjem svojstava u stavci proizvoda.</span><span class="sxs-lookup"><span data-stu-id="7d581-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="7d581-122">Da biste kreirali faktore količine iz svojstava proizvoda, sledite ove korake:</span><span class="sxs-lookup"><span data-stu-id="7d581-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="7d581-123">U levom oknu za navigaciju usluge Project Operations idite na **Prodaja** > **Proizvodi**.</span><span class="sxs-lookup"><span data-stu-id="7d581-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="7d581-124">Otvorite proizvod za koji treba da konfigurišete faktore količine.</span><span class="sxs-lookup"><span data-stu-id="7d581-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="7d581-125">Uverite se da proizvod ima svojstva koja su već konfigurisana.</span><span class="sxs-lookup"><span data-stu-id="7d581-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="7d581-126">Na stranici **Informacije o projektu** za Proizvod, izaberite karticu **Faktori količine**.</span><span class="sxs-lookup"><span data-stu-id="7d581-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="7d581-127">U podformi izaberite **Novi obračun polja**.</span><span class="sxs-lookup"><span data-stu-id="7d581-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="7d581-128">Unesite naziv faktora količine i izaberite vrednost svojstva koje se mapira u obračun polja.</span><span class="sxs-lookup"><span data-stu-id="7d581-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="7d581-129">Sačuvajte i zatvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="7d581-129">Save and close the form.</span></span> <span data-ttu-id="7d581-130">Ponovite ove korake za sva svojstva koja ćete koristiti za izračunavanje količine za stavku ponude zasnovanu na proizvodu.</span><span class="sxs-lookup"><span data-stu-id="7d581-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="7d581-131">Kada za proizvod kreirate stavku ponude zasnovane na proizvodu, količina stavke ponude će biti zaključana.</span><span class="sxs-lookup"><span data-stu-id="7d581-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="7d581-132">Količina će se izračunati kao proizvod vrednosti svojstva koje ste uneli za tu stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="7d581-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
