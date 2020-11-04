---
title: Međukompanijski troškovi
description: Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji. U ovoj situaciji možete da koristite funkciju troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao izveden.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083731"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="b9235-104">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="b9235-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9235-105">Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="b9235-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="b9235-106">U ovoj situaciji možete da koristite funkciju troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao izveden.</span><span class="sxs-lookup"><span data-stu-id="b9235-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="b9235-107">Pravno lice koje zapošljava radnika naziva se pravno lice koje pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="b9235-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="b9235-108">Pravno lice za koje radnik snosi troškove naziva se pravno lice kojem se pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="b9235-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="b9235-109">Pre nego što radnik može kreirati i podneti troškove za rad koji se obavlja za drugo pravno lice, u pravnom licu koje pozajmljuje, na stranici **Parametri upravljanja troškovima** izaberite **Omogućite stavke troškova u okviru preduzeća**.</span><span class="sxs-lookup"><span data-stu-id="b9235-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="b9235-110">Poresko knjiženje za međukompanijske troškove</span><span class="sxs-lookup"><span data-stu-id="b9235-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9235-111">Ako u izveštaju o troškovima želite da koristite poreske grupe koje su povezane sa pravnim licem koje pozajmljuje (izvorno pravno lice) umesto sa pravnim licem kojem se pozajmljuje (odredišno pravno lice), moraćete to da konfigurišete u podešavanju poreza na promet u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="b9235-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="b9235-112">Kada je parametar glavne knjige **Pravno lice za poresko knjiženje u okviru preduzeća** podešen na **Izvor** i opcija **Primeni pravila oporezivanja za porez na promet** podešena na **Ne** , koristiće se kombinacija poreza za pravno lice koje pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="b9235-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="b9235-113">Kada je isti parametar postavljen na **Odredište** , koristiće se poreska kombinacija za pravno lice kojem se pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="b9235-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="b9235-114">Za pravna lica u Sjedinjenim Državama, kada je parametar postavljen na **Izvor** , polje **Potraživanje poreza na promet** takođe mora biti konfigurisano na novoj stranici **Grupe za knjiženje glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="b9235-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="b9235-115">Računovodstveni mehanizam će koristiti podatke iz ovog polja za računovodstveno knjiženje u vezi sa porezom.</span><span class="sxs-lookup"><span data-stu-id="b9235-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="b9235-116">Ponašanje je dosledno za stavke troškova objavljene sa projektom ili bez njega.</span><span class="sxs-lookup"><span data-stu-id="b9235-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
