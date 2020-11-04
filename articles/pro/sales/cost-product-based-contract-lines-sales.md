---
title: Obračun troškova za predmete ugovora zasnovane na proizvodima
description: Ova tema pruža informacije o kreiranju
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4083811"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="b2651-103">Obračun troškova za predmete ugovora zasnovane na proizvodima</span><span class="sxs-lookup"><span data-stu-id="b2651-103">Costing product-based contract lines</span></span>

<span data-ttu-id="b2651-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="b2651-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b2651-105">Predmeti ugovora zasnovani na proizvodima u programu Dynamics 365 Project Operations uključuju polje **Cena koštanja** , u kome se čuva cena koštanja proizvoda za proračun profitabilnosti na nižem nivou.</span><span class="sxs-lookup"><span data-stu-id="b2651-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="b2651-106">Kada se predmet ugovora zasnovan na proizvodu kreira za kataloški proizvod, podrazumevani troškovi predmeta ugovora zasnovanog na proizvodu dolaze iz polja **Standardna cena** u katalogu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="b2651-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="b2651-107">Polje **Standardna cena** u katalogu proizvoda podešeno je u osnovnoj valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="b2651-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="b2651-108">Kada jedinični trošak podrazumeva predmet ugovora, on se pretvara u valutu prodaje na ugovoru.</span><span class="sxs-lookup"><span data-stu-id="b2651-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="b2651-109">Jedinična cena predmeta ugovora zasnovanog na proizvodu</span><span class="sxs-lookup"><span data-stu-id="b2651-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="b2651-110">Postojanje jedinične cene u predmetu ugovora zasnovanog na proizvodu omogućava različite cene za proizvod za svaku prodaju jedinice.</span><span class="sxs-lookup"><span data-stu-id="b2651-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="b2651-111">Iako nisu uvek neophodni, postoje određeni scenariji u kojima dobavljač može sniziti troškove proizvoda za klijenta.</span><span class="sxs-lookup"><span data-stu-id="b2651-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="b2651-112">Razmotrite sledeći scenario:</span><span class="sxs-lookup"><span data-stu-id="b2651-112">Consider the following scenario:</span></span>

<span data-ttu-id="b2651-113">Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="b2651-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="b2651-114">Fabrikam pruža usluge ugradnje, ali robotske ruke su nabavljene od kompanije Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b2651-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="b2651-115">Ako instalacija robotske ruke u kompaniji Adatum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey Research, tada bi kompanija Trey Research mogla dati poseban popust za ovaj posao kompaniji Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="b2651-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="b2651-116">U ovom slučaju, Fabrikam kreira predmet ugovora zasnovan na proizvodu za robotske ruke i unosi jedinični trošak za ovaj ugovor koji se razlikuje od standardnog troška robotskih ruku kompanije Trey Research.</span><span class="sxs-lookup"><span data-stu-id="b2651-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
