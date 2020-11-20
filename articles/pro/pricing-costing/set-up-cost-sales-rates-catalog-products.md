---
title: Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno
description: Ova tema pruža informacije o tome kako da postavite stope cena i prodaje za stavke iz kataloga proizvoda.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176718"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="9ccc5-103">Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno</span><span class="sxs-lookup"><span data-stu-id="9ccc5-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="9ccc5-104">_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="9ccc5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="9ccc5-105">Postavljanje cena za stavke kataloga proizvoda u programu Dynamics 365 Project Operations je isto kao u programu Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="9ccc5-106">Budući da se proizvodi ne mogu proceniti ili koristiti na projektima u usluzi Project Operations, nema potrebe za postavljanjem cena kataloga proizvoda na cenovnike projekata za ponude i ugovore.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="9ccc5-107">Cene kataloga proizvoda treba postaviti u polju **Cena proizvoda** ponude, ugovora ili naloga.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="9ccc5-108">Ne postavljajte cene kataloga proizvoda u cenovnike projekata za ove entitete.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="9ccc5-109">Cenovnici projekata ekskluzivni su za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="9ccc5-110">Postoji specifična poslovna logika koja kopira cenovnike iz ponude u ugovor.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="9ccc5-111">Rezultat je cenovnik projekta specifičan za ugovor.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="9ccc5-112">Operacija kopiranja može odložiti postupak dobijanja ponude ako projektni cenovnik na ponudi postane prevelik.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="9ccc5-113">Cenovnici proizvoda se ne kopiraju da bi se kreirali prilagođeni cenovnici po ugovorima.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="9ccc5-114">To znači da cenovnici proizvoda ne utiču na performanse procesa osvajanja ponuda.</span><span class="sxs-lookup"><span data-stu-id="9ccc5-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
