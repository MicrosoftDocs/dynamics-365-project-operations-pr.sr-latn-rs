---
title: Stavke proizvoda zasnovane na obračunu
description: Ova tema pruža informacije o primeni cene koštanja na stavku ponude zasnovane na proizvodu.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003468"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="bbb2f-103">Stavke proizvoda zasnovane na obračunu</span><span class="sxs-lookup"><span data-stu-id="bbb2f-103">Costing product-based quote lines</span></span>

<span data-ttu-id="bbb2f-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="bbb2f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bbb2f-105">Stavke ponude zasnovane na proizvodu u usluzi Dynamics 365 Project Operations takođe imaju polje **Cena koštanja**.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="bbb2f-106">Ovo polje se koristi za praćenje cene koštanja proizvoda na stavci ponude i za posledične proračune profitabilnosti.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="bbb2f-107">Kada se stavka ponude zasnovana na proizvodu kreira za kataloški proizvod, podrazumevani troškovi stavke ponude zasnovane na proizvodu dolaze iz polja **Standardna cena** u katalogu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="bbb2f-108">Polje standardne cene u katalogu proizvoda podešeno je u osnovnoj valuti organizacije.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="bbb2f-109">Podrazumevana jedinična cena u stavci ponude zasnovane na proizvodu pretvara se u prodajnu valutu u ponudi.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="bbb2f-110">Jedinična cena stavke ponude zasnovane na proizvodu</span><span class="sxs-lookup"><span data-stu-id="bbb2f-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="bbb2f-111">Svrha postojanja jedinične cene u stavci ponude zasnovane na proizvodu je omogućavanje različitih cena za proizvod za svaku prodaju.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="bbb2f-112">To nije tipičan scenario, ali dobavljač ponekad može da snizi cenu proizvoda u zavisnosti od klijenta konačne prodaje.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="bbb2f-113">Na primer:</span><span class="sxs-lookup"><span data-stu-id="bbb2f-113">For example:</span></span>

<span data-ttu-id="bbb2f-114">Fabrikam Robotics instalira robotske ruke na proizvodnim trakama kompanije A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="bbb2f-115">Fabrikam pruža usluge ugradnje, ali robotske ruke su nabavljene od kompanije Trey robotics.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="bbb2f-116">Ako instalacija robotske ruke u kompaniji A Datum Corporation otvori novu industrijsku delatnost za robotske ruke kompanije Trey, tada bi kompanija Trey mogla dati poseban popust za ovaj posao kompaniji Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="bbb2f-117">U ovom slučaju, Fabrikam će kreirati stavku ponude zasnovanu na proizvodu za robotske ruke i uneće posebnu cenu po jedinici za ovu ponudu.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="bbb2f-118">Ta cena se razlikuje od standardne cene robotske ruke kompanije Trey.</span><span class="sxs-lookup"><span data-stu-id="bbb2f-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]