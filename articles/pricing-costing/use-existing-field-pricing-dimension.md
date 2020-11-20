---
title: Project Operations polja kao dimenzija za određivanje cena
description: Ova tema pruža informacije o korišćenju postojećih polja kao dimenzija za određivanje cena u usluzi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119255"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="c002b-103">Project Operations polja kao dimenzija za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="c002b-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="c002b-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="c002b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c002b-105">Entitet **Stvarne vrednosti** ima mnogo polja koja se mogu koristiti kao dimenzije za određivanja cena za cene zasnovane na resursima.</span><span class="sxs-lookup"><span data-stu-id="c002b-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="c002b-106">Na primer, jedno uobičajeno polje je **Resurs koji se može rezervisati**.</span><span class="sxs-lookup"><span data-stu-id="c002b-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="c002b-107">Manja preduzeća sa manje od 20-30 naplativih resursa mogu da otkriju da je jednostavniji pristup ako imaju stope naplate i troškova specifične za svaki resurs.</span><span class="sxs-lookup"><span data-stu-id="c002b-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="c002b-108">Međutim, kako raste naplativa radna snaga, održavanje stopa secifičnih resursa može postati nerealno.</span><span class="sxs-lookup"><span data-stu-id="c002b-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="c002b-109">Cena resursa i stope naplate počinju da se razlikuju kako se resursi unapređuju, stiču više iskustva ili kako usvajaju drugačiji skup veština.</span><span class="sxs-lookup"><span data-stu-id="c002b-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="c002b-110">Drugi primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="c002b-110">Another example is that of transaction category.</span></span> <span data-ttu-id="c002b-111">Klijenti i primenjivači su koristili kategoriju transakcije da bi klasifikovali posao i pomoću polja određuju cenu i troškove na osnovu kategorije posla.</span><span class="sxs-lookup"><span data-stu-id="c002b-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
