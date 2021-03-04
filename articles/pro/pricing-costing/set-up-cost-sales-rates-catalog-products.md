---
title: Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno
description: Ova tema pruža informacije o tome kako da postavite stope cena i prodaje za stavke iz kataloga proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764577"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="eb109-103">Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno</span><span class="sxs-lookup"><span data-stu-id="eb109-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="eb109-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="eb109-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="eb109-105">Podešavanje cena za stavke kataloga proizvoda u usluzi Dynamics 365 Project Operations je isto kao i u usluzi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="eb109-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="eb109-106">U usluzi Project Operations, proizvodi se ne mogu proceniti ni koristiti u projektima, tako da cene u katalogu proizvoda ne moraju da se podešavaju u cenovnicima projekata za ponude i ugovore.</span><span class="sxs-lookup"><span data-stu-id="eb109-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="eb109-107">Koristite polje **Cena proizvoda** ponude, ugovora ili naloga da biste podesili cene u katalogu proizvoda.</span><span class="sxs-lookup"><span data-stu-id="eb109-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="eb109-108">Ne podešavajte cene u katalogu proizvoda u cenovniku projekta.</span><span class="sxs-lookup"><span data-stu-id="eb109-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="eb109-109">Cenovnici projekata ekskluzivni su za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="eb109-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="eb109-110">Poslovna logika specifična za aplikaciju kopira cenovnike iz ponude u ugovor.</span><span class="sxs-lookup"><span data-stu-id="eb109-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="eb109-111">Rezultat je cenovnik projekta specifičan za ugovor.</span><span class="sxs-lookup"><span data-stu-id="eb109-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="eb109-112">Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="eb109-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="eb109-113">Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima.</span><span class="sxs-lookup"><span data-stu-id="eb109-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="eb109-114">Budući da nije uključeno kopiranje, to ne utiče na performanse procesa ponude.</span><span class="sxs-lookup"><span data-stu-id="eb109-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
