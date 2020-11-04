---
title: Korišćenje postojećeg polja u usluzi Project Service kao dimenzije za određivanje cena
description: Ova tema pruža informacije o korišćenju postojećih Project Service polja kao dimenzija za određivanje cena.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083658"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="1456c-103">Korišćenje postojećeg polja u usluzi Project Service kao dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="1456c-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="1456c-104">Project Service Automation (PSA) ima mnoga polja u entitetu **Stvarne vrednosti** koja se mogu koristiti kao dimenzije za određivanje cena zasnovano na resursima u organizacijama koje obavljaju projekte.</span><span class="sxs-lookup"><span data-stu-id="1456c-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="1456c-105">Na primer, jedno uobičajeno polje je **Resurs koji se može rezervisati**.</span><span class="sxs-lookup"><span data-stu-id="1456c-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="1456c-106">Manja preduzeća sa manje od 20-30 naplativih resursa mogu da otkriju da je jednostavniji pristup ako imaju stope naplate i troškova specifične za svaki resurs.</span><span class="sxs-lookup"><span data-stu-id="1456c-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="1456c-107">Međutim, kako se naplativa radna snaga povećava, ovo može postati nerealno za održavanje pošto će troškovi resursa i stope naplate početi da se razlikuju sa unapređenjem resursa, sticanjem većeg iskustva ili različitog spektra veština.</span><span class="sxs-lookup"><span data-stu-id="1456c-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="1456c-108">Budući da ovaj pristup još uvek funkcioniše za preduzeća određene veličine, pogledajte temu [Korišćenje resursa koji se može rezervisati kao dimenzije za određivanje cena](bookable-resource-pricing-dimension.md) da biste razumeli kako se postojeće Project Service polje može koristiti kao dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="1456c-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="1456c-109">Drugi primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="1456c-109">Another example is that of transaction category.</span></span> <span data-ttu-id="1456c-110">Klijenti i primenjivači su koristili kategoriju transakcije u aplikaciji PSA da klasifikuju posao i pomoću polja određuju cenu i troškove na osnovu kategorije posla.</span><span class="sxs-lookup"><span data-stu-id="1456c-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="1456c-111">Više informacija potražite u članku [Korišćenje kategorije transakcije kao dimenzije određivanja cena](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="1456c-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
