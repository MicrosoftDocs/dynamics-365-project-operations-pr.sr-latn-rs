---
title: Project Operations polja kao dimenzija za određivanje cena
description: Ova tema pruža informacije o korišćenju postojećih polja kao dimenzija za određivanje cena u usluzi Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896433"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="106be-103">Project Operations polja kao dimenzija za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="106be-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="106be-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="106be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="106be-105">Entitet **Stvarne vrednosti** ima mnogo polja koja se mogu koristiti kao dimenzije za određivanja cena za cene zasnovane na resursima.</span><span class="sxs-lookup"><span data-stu-id="106be-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="106be-106">Na primer, jedno uobičajeno polje je **Resurs koji se može rezervisati**.</span><span class="sxs-lookup"><span data-stu-id="106be-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="106be-107">Manja preduzeća sa manje od 20-30 naplativih resursa mogu da otkriju da je jednostavniji pristup ako imaju stope naplate i troškova specifične za svaki resurs.</span><span class="sxs-lookup"><span data-stu-id="106be-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="106be-108">Međutim, kako raste naplativa radna snaga, održavanje stopa secifičnih resursa može postati nerealno.</span><span class="sxs-lookup"><span data-stu-id="106be-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="106be-109">Cena resursa i stope naplate počinju da se razlikuju kako se resursi unapređuju, stiču više iskustva ili kako usvajaju drugačiji skup veština.</span><span class="sxs-lookup"><span data-stu-id="106be-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="106be-110">Drugi primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="106be-110">Another example is that of transaction category.</span></span> <span data-ttu-id="106be-111">Klijenti i primenjivači su koristili kategoriju transakcije da bi klasifikovali posao i pomoću polja određuju cenu i troškove na osnovu kategorije posla.</span><span class="sxs-lookup"><span data-stu-id="106be-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>