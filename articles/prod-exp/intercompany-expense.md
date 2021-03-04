---
title: Interni troškovi u okviru preduzeća
description: Ova tema pruža informacije o načinu korišćenja troškova u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960849"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="6318d-103">Međukompanijski troškovi</span><span class="sxs-lookup"><span data-stu-id="6318d-103">Intercompany expenses</span></span>

<span data-ttu-id="6318d-104">Radnik koji je zaposlen u jednom pravnom licu u organizaciji može obavljati posao za drugo pravno lice u istoj organizaciji.</span><span class="sxs-lookup"><span data-stu-id="6318d-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="6318d-105">Možete da koristite troškove u okviru preduzeća za dodeljivanje troškova radnika pravnom licu za koje je posao obavljen.</span><span class="sxs-lookup"><span data-stu-id="6318d-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="6318d-106">Pravno lice koje zapošljava radnika naziva se pravno lice koje pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="6318d-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="6318d-107">Pravno lice za koje radnik snosi troškove naziva se pravno lice kojem se pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="6318d-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="6318d-108">Da bi radnik mogao da kreira i preda troškove u okviru preduzeća, morate omogućiti redove troškova u okviru preduzeća.</span><span class="sxs-lookup"><span data-stu-id="6318d-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="6318d-109">Za pravno lice koje pozajmljuje novac, na stranici **Parametri upravljanja troškovima** izaberite **Omogući redove troškova u okviru preduzeća**.</span><span class="sxs-lookup"><span data-stu-id="6318d-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="6318d-110">Poresko knjiženje za međukompanijske troškove</span><span class="sxs-lookup"><span data-stu-id="6318d-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6318d-111">Da biste u izveštaju o troškovima mogli da koristite poreske grupe koje su povezane sa pravnim licem koje pozajmljuje novac (izvor) umesto sa pravnim licem koje se zadužuje (odredište), morate da omogućite funkcionalnost u podešavanju poreza na promet u glavnoj knjizi.</span><span class="sxs-lookup"><span data-stu-id="6318d-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="6318d-112">Kada je parametar **Pravno lice za knjiženje poreza u okviru preduzeća** podešen na **Izvor**, a parametar **Primeni pravila oporezivanja poreza na promet** je podešen na **Ne**, koristi se poreska kombinacija za pravno lice koje pozajmljuje novac.</span><span class="sxs-lookup"><span data-stu-id="6318d-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="6318d-113">Kada je isti parametar postavljen na **Odredište**, koristiće se poreska kombinacija za pravno lice kojem se pozajmljuje.</span><span class="sxs-lookup"><span data-stu-id="6318d-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="6318d-114">Za pravna lica u Sjedinjenim Državama, kada je parametar postavljen na **Izvor**, polje **Potraživanje poreza na promet** takođe mora biti konfigurisano na novoj stranici **Grupe za knjiženje glavne knjige**.</span><span class="sxs-lookup"><span data-stu-id="6318d-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="6318d-115">Računovodstveni mehanizam će koristiti podatke iz ovog polja za računovodstveni unos u vezi sa porezom.</span><span class="sxs-lookup"><span data-stu-id="6318d-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="6318d-116">Ponašanje je dosledno za stavke troškova objavljene sa projektom ili bez njega.</span><span class="sxs-lookup"><span data-stu-id="6318d-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
