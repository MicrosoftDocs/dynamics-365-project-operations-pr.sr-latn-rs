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
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281585"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="faa59-103">Korišćenje postojećeg polja u usluzi Project Service kao dimenzije za određivanje cena</span><span class="sxs-lookup"><span data-stu-id="faa59-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="faa59-104">Project Service Automation (PSA) ima mnoga polja u entitetu **Stvarne vrednosti** koja se mogu koristiti kao dimenzije za određivanje cena zasnovano na resursima u organizacijama koje obavljaju projekte.</span><span class="sxs-lookup"><span data-stu-id="faa59-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="faa59-105">Na primer, jedno uobičajeno polje je **Resurs koji se može rezervisati**.</span><span class="sxs-lookup"><span data-stu-id="faa59-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="faa59-106">Manja preduzeća sa manje od 20-30 naplativih resursa mogu da otkriju da je jednostavniji pristup ako imaju stope naplate i troškova specifične za svaki resurs.</span><span class="sxs-lookup"><span data-stu-id="faa59-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="faa59-107">Međutim, kako se naplativa radna snaga povećava, određene stope mogu postati nerealne za održavanje pošto će troškovi resursa i stope naplate početi da se razlikuju sa unapređenjem resursa, sticanjem većeg iskustva ili različitog spektra veština.</span><span class="sxs-lookup"><span data-stu-id="faa59-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="faa59-108">Budući da ovaj pristup još uvek funkcioniše za preduzeća određene veličine, pogledajte članak [Korišćenje resursa koji se može rezervisati kao dimenzije za određivanje cena](bookable-resource-pricing-dimension.md) da biste razumeli kako se postojeće Project Service polje može koristiti kao dimenzija za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="faa59-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="faa59-109">Drugi primer je kategorija transakcije.</span><span class="sxs-lookup"><span data-stu-id="faa59-109">Another example is that of transaction category.</span></span> <span data-ttu-id="faa59-110">Klijenti i primenjivači su koristili kategoriju transakcije u aplikaciji PSA da klasifikuju posao i pomoću polja određuju cenu i troškove na osnovu kategorije posla.</span><span class="sxs-lookup"><span data-stu-id="faa59-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="faa59-111">Više informacija potražite u članku [Korišćenje kategorije transakcije kao dimenzije određivanja cena](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="faa59-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]