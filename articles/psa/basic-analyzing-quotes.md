---
title: Analiza ponuda za projekat
description: Ova tema pruža informacije o analizi ponuda za projekat.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6ed900620f92e76d293f6b533b101be94b25cff3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127040"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="b430a-103">Analiza ponuda za projekat</span><span class="sxs-lookup"><span data-stu-id="b430a-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b430a-104">Dynamics 365 Project Service Automation analizira ponude za projekat radi procene profitabilnosti.</span><span class="sxs-lookup"><span data-stu-id="b430a-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="b430a-105">Takođe analizira koliko je ponuda usaglašena sa očekivanjima klijenta o datumu isporuke ili završetka, kao i sa budžetom.</span><span class="sxs-lookup"><span data-stu-id="b430a-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="b430a-106">Analiza isplativosti</span><span class="sxs-lookup"><span data-stu-id="b430a-106">Profitability analysis</span></span>

<span data-ttu-id="b430a-107">Project Service Automation analizira profitabilnost korišćenjem bruto marže i korigovane bruto marže.</span><span class="sxs-lookup"><span data-stu-id="b430a-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="b430a-108">Bruto marže se izračunavaju pomoću sledeće formule:</span><span class="sxs-lookup"><span data-stu-id="b430a-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="b430a-109">Korigovana bruto marža se izračunavaju pomoću sledeće formule:</span><span class="sxs-lookup"><span data-stu-id="b430a-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="b430a-110">Ako se vrednosti bruto marže i korigovane bruto marže značajno razlikuju, veći deo posla u ponudi je klasifikovan kao nenaplativ.</span><span class="sxs-lookup"><span data-stu-id="b430a-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="b430a-111">Analiza očekivanja klijenta</span><span class="sxs-lookup"><span data-stu-id="b430a-111">Analysis of customer expectations</span></span>

<span data-ttu-id="b430a-112">Možete analizirati ponude i generisati grafikone za očekivanja klijenata u vezi sa rasporedom i budžetom ako unesete vrednosti za sledeća polja:</span><span class="sxs-lookup"><span data-stu-id="b430a-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="b430a-113">Polje **Zahtevani datum isporuke** u zaglavlju ponude.</span><span class="sxs-lookup"><span data-stu-id="b430a-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="b430a-114">Polje **Budžet klijenta** za svaku stavku ponude (za stavke zasnovane na projektu i stavke zasnovane na proizvodu).</span><span class="sxs-lookup"><span data-stu-id="b430a-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="b430a-115">Analiza očekivanja klijenata u vezi sa rasporedom se vrši poređenjem najnovijeg datuma završetka detalja stavke ponude sa zahtevanim datumom isporuke za sve stavke ponude u ponudi.</span><span class="sxs-lookup"><span data-stu-id="b430a-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="b430a-116">Analiza očekivanja klijenata u vezi sa budžetom vrši se poređenjem zbira ukupnog budžeta klijenta sa ponuđenim iznosom u svim stavkama ponude.</span><span class="sxs-lookup"><span data-stu-id="b430a-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
