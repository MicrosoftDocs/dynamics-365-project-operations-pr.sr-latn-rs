---
title: Project Operations polja kao dimenzija za određivanje cena
description: Ova tema pruža informacije o upotrebi polja kao dimenzija za određivanje cena u usluzi Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004503"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="eae40-103">Project Operations polja kao dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="eae40-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="eae40-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="eae40-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eae40-105">Entitet **Stvarne vrednosti** ima mnogo polja koja se mogu koristiti kao dimenzije za određivanja cena za cene zasnovane na resursima.</span><span class="sxs-lookup"><span data-stu-id="eae40-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="eae40-106">Na primer, jedno uobičajeno polje je **Resurs koji se može rezervisati**.</span><span class="sxs-lookup"><span data-stu-id="eae40-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="eae40-107">Manja preduzeća sa manje od 20-30 naplativih resursa mogu da otkriju da je jednostavniji pristup ako imaju stope naplate i troškova specifične za svaki resurs.</span><span class="sxs-lookup"><span data-stu-id="eae40-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="eae40-108">Međutim, kako raste naplativa radna snaga, održavanje stopa secifičnih resursa može postati nerealno.</span><span class="sxs-lookup"><span data-stu-id="eae40-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="eae40-109">Cena resursa i stope naplate počinju da se razlikuju kako se resursi unapređuju, stiču više iskustva ili kako usvajaju drugačiji skup veština.</span><span class="sxs-lookup"><span data-stu-id="eae40-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="eae40-110">Drugi primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="eae40-110">Another example is that of transaction category.</span></span> <span data-ttu-id="eae40-111">Klijenti i primenjivači su koristili kategoriju transakcije da bi klasifikovali posao i pomoću polja određuju cenu i troškove na osnovu kategorije posla.</span><span class="sxs-lookup"><span data-stu-id="eae40-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]