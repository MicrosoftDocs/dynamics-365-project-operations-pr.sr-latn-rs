---
title: Cena za predmete ugovora zasnovane na proizvodu – jednostavno
description: Ova tema pruža informacije o kreiranju
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003558"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="427e4-103">Cena za predmete ugovora zasnovane na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="427e4-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="427e4-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="427e4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="427e4-105">Predmeti ugovora zasnovanih na proizvodima u usluzi Dynamics 365 Project Operations uključuju polje **Cena koštanja** u kome se čuva cena koštanja proizvoda za proračune profitabilnosti distribucije.</span><span class="sxs-lookup"><span data-stu-id="427e4-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="427e4-106">Kada se za proizvod iz kataloga kreira predmet ugovora zasnovan na proizvodu, troškovi u redu se podrazumevano podešavaju iz polja **Standardni troškovi** u katalogu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="427e4-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="427e4-107">Polje **Standardna cena** u katalogu proizvoda podešeno je u osnovnoj valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="427e4-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="427e4-108">Kada jedinični trošak podrazumeva predmet ugovora, on se pretvara u valutu prodaje na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="427e4-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="427e4-109">Jedinična cena predmeta ugovora zasnovanog na proizvodu</span><span class="sxs-lookup"><span data-stu-id="427e4-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="427e4-110">Postojanje jedinične cene u predmetu ugovora zasnovanog na proizvodu omogućava različite cene za proizvod za svaku prodaju jedinice.</span><span class="sxs-lookup"><span data-stu-id="427e4-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="427e4-111">Iako nisu uvek neophodni, postoje određeni scenariji u kojima dobavljač može sniziti troškove proizvoda za klijenta.</span><span class="sxs-lookup"><span data-stu-id="427e4-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="427e4-112">Razmotrite sledeći scenario:</span><span class="sxs-lookup"><span data-stu-id="427e4-112">Consider the following scenario:</span></span>

<span data-ttu-id="427e4-113">Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="427e4-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="427e4-114">Fabrikam pruža usluge ugradnje, ali ruke robota su iz kompanije Trey Research.</span><span class="sxs-lookup"><span data-stu-id="427e4-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="427e4-115">Ako instalacija robotske ruke u kompaniji Adatum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey Research, tada bi kompanija Trey Research mogla dati poseban popust za ovaj posao kompaniji Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="427e4-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="427e4-116">U ovom slučaju, Fabrikam kreira predmet ugovora zasnovan na proizvodu za ruke robota.</span><span class="sxs-lookup"><span data-stu-id="427e4-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="427e4-117">Za ovaj ugovor se unosi cena po jedinici.</span><span class="sxs-lookup"><span data-stu-id="427e4-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="427e4-118">Cena se razlikuje od cene za ruke robota kompanije Trey Research.</span><span class="sxs-lookup"><span data-stu-id="427e4-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]