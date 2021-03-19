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
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286535"
---
# <a name="resource-estimates"></a><span data-ttu-id="0057f-103">Procene resursa</span><span class="sxs-lookup"><span data-stu-id="0057f-103">Resource estimates</span></span>

<span data-ttu-id="0057f-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="0057f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0057f-105">Procene resursa potiču iz angažovanja u vremenu koje je definisano u strukturnoj analizi posla zajedno sa primenljivim dimenzijama za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="0057f-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="0057f-106">Tipično, proračun je **satnica za svaku ulogu x broj sati.**</span><span class="sxs-lookup"><span data-stu-id="0057f-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="0057f-107">Angažovanje u vremenu za svaki resurs uskladišteno je u zapisu o dodeli resursa.</span><span class="sxs-lookup"><span data-stu-id="0057f-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="0057f-108">Određivanje cena se skladišti u unapred definisanom cenovniku.</span><span class="sxs-lookup"><span data-stu-id="0057f-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="0057f-109">Konverzija jedinica primenjuje se na osnovu važećeg cenovnika.</span><span class="sxs-lookup"><span data-stu-id="0057f-109">Unit conversion is applied based on the applicable price list.</span></span>

![Procene resursa](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="0057f-111">Podrazumevana cena koštanja i valuta troškova</span><span class="sxs-lookup"><span data-stu-id="0057f-111">Default cost price and cost currency</span></span>

<span data-ttu-id="0057f-112">Cene troškova podrazumevano dolaze iz organizacione jedinice.</span><span class="sxs-lookup"><span data-stu-id="0057f-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="0057f-113">Podrazumevana stopa naplate i prodajna valuta</span><span class="sxs-lookup"><span data-stu-id="0057f-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="0057f-114">Prodajne cene se primenjuju jednom po pogodbi.</span><span class="sxs-lookup"><span data-stu-id="0057f-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="0057f-115">Hijerarhija prodajnog cenovnika podrazumevano je sledeća:</span><span class="sxs-lookup"><span data-stu-id="0057f-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="0057f-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="0057f-116">Organization</span></span>
2. <span data-ttu-id="0057f-117">Klijent</span><span class="sxs-lookup"><span data-stu-id="0057f-117">Customer</span></span>
3. <span data-ttu-id="0057f-118">Ponuda/ugovor</span><span class="sxs-lookup"><span data-stu-id="0057f-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]