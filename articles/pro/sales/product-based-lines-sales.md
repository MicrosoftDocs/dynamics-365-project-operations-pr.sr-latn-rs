---
title: Stavke mogućnosti za poslovanje zasnovane na proizvodu – jednostavno
description: Ova tema pruža informacije o stavkama predmeta mogućnosti za poslovanje zasnovanim na proizvodu u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176357"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="6fe50-103">Stavke mogućnosti za poslovanje zasnovane na proizvodu – jednostavno</span><span class="sxs-lookup"><span data-stu-id="6fe50-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="6fe50-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="6fe50-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6fe50-105">Predmeti mogućnosti za poslovanje zasnovani na proizvodu su stavke u mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="6fe50-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="6fe50-106">Ove stavke se isporučuju klijentu kao posebne stavke na eventualnoj fakturi bez ikakvih drugih usluga sa dodatom vrednošću.</span><span class="sxs-lookup"><span data-stu-id="6fe50-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="6fe50-107">Povezana potrošnja i korišćenje se ne prate na zadacima bilo kojih povezanih projekata.</span><span class="sxs-lookup"><span data-stu-id="6fe50-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="6fe50-108">Stavke zasnovane na proizvodima mogu biti artikli iz kataloga ili ručno dodati proizvodi.</span><span class="sxs-lookup"><span data-stu-id="6fe50-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="6fe50-109">Većina funkcionalnosti predmeta mogućnosti za poslovanje zasnovanih na proizvodu prati funkcionalnost koju pruža aplikacija Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6fe50-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="6fe50-110">Za više informacija o predmetima mogućnosti za poslovanje zasnovanim na proizvodu, pogledajte [Dodavanje proizvoda u mogućnost za poslovanje](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="6fe50-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="6fe50-111">Jedan koncept o predmetima mogućnosti za poslovanje zasnovanim na proizvodu koji je specifičan za mogućnosti za poslovanje zasnovane na projektima jeste **Budžet klijenta**.</span><span class="sxs-lookup"><span data-stu-id="6fe50-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="6fe50-112">Koristite ovo polje za praćenje iznosa koji je klijent spreman da plati za stavku porudžbine.</span><span class="sxs-lookup"><span data-stu-id="6fe50-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="6fe50-113">Ako je metoda prihoda rezimea mogućnosti za poslovanje postavljena na **Sistemski izračunato**, vrednosti budžeta klijenata u stavkama zasnovanim na proizvodu i projektu se sabiraju kako bi se izračunao procenjeni prihod.</span><span class="sxs-lookup"><span data-stu-id="6fe50-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
