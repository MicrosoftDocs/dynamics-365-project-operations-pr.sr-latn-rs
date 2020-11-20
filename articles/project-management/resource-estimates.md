---
title: Procene resursa
description: Ova tema pruža informacije o tome kako se izračunavaju procene resursa u usluzi Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127394"
---
# <a name="resource-estimates"></a><span data-ttu-id="96226-103">Procene resursa</span><span class="sxs-lookup"><span data-stu-id="96226-103">Resource estimates</span></span>

<span data-ttu-id="96226-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="96226-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="96226-105">Procene resursa potiču iz angažovanja u vremenu koje je definisano u strukturnoj analizi posla zajedno sa primenljivim dimenzijama za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="96226-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="96226-106">Tipično, proračun je **satnica za svaku ulogu x broj sati.**</span><span class="sxs-lookup"><span data-stu-id="96226-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="96226-107">Angažovanje u vremenu za svaki resurs uskladišteno je u zapisu o dodeli resursa.</span><span class="sxs-lookup"><span data-stu-id="96226-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="96226-108">Određivanje cena se skladišti u unapred definisanom cenovniku.</span><span class="sxs-lookup"><span data-stu-id="96226-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="96226-109">Konverzija jedinica primenjuje se na osnovu važećeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="96226-109">Unit conversion is applied based on the applicable price list.</span></span>

![Procene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="96226-111">Podrazumevana cena koštanja i valuta troškova</span><span class="sxs-lookup"><span data-stu-id="96226-111">Default cost price and cost currency</span></span>

<span data-ttu-id="96226-112">Cene troškova podrazumevano dolaze iz organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="96226-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="96226-113">Podrazumevana stopa naplate i prodajna valuta</span><span class="sxs-lookup"><span data-stu-id="96226-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="96226-114">Prodajne cene se primenjuju jednom po pogodbi.</span><span class="sxs-lookup"><span data-stu-id="96226-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="96226-115">Hijerarhija prodajnog cenovnika podrazumevano je sledeća:</span><span class="sxs-lookup"><span data-stu-id="96226-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="96226-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="96226-116">Organization</span></span>
2. <span data-ttu-id="96226-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="96226-117">Customer</span></span>
3. <span data-ttu-id="96226-118">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="96226-118">Quote/contract</span></span>
