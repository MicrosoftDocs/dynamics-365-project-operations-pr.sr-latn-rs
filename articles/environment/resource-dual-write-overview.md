---
title: Project Operations integracija dvostrukog upisivanja
description: Ova tema pruža pregled Project Operations integraciji dvostrukog upisivanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998698"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="71fee-103">Pregled Project Operations integracije dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="71fee-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="71fee-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="71fee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="71fee-105">Project Operations koristi [mogućnosti dvostrukog upisivanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizaciju podataka u Microsoft Dataverse i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="71fee-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="71fee-106">Sledeća ilustracija pokazuje kako se podaci sinhronizuju kao deo ove integracije između Dataverse i Finance.</span><span class="sxs-lookup"><span data-stu-id="71fee-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Pregled Project Operations tokova podataka](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="71fee-108">Project Operations u Dataverse pruža moderan korisnički interfejs (UI) i jednostavnu proširivost bez kodiranja/sa malo kodiranja pomoću Power Platform mogućnosti.</span><span class="sxs-lookup"><span data-stu-id="71fee-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="71fee-109">Menadžeri projekata, menadžeri resursa, članovi projektnog tima i osobe koje rade sa klijentima obavljaju svoje aktivnosti u Project Operations u Dataverse.</span><span class="sxs-lookup"><span data-stu-id="71fee-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="71fee-110">Project Operations u Finance pruža podršku projektnom računovodstvu i priznavanju prihoda.</span><span class="sxs-lookup"><span data-stu-id="71fee-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="71fee-111">Project Operations se uključuju u finansijski okvir u Finance za obračun poreza na promet, kurseve valuta, izveštavanje o finansijskoj dimenziji i još mnogo toga.</span><span class="sxs-lookup"><span data-stu-id="71fee-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="71fee-112">Iskustva računovođa na projektu uglavnom se temelje na Finance.</span><span class="sxs-lookup"><span data-stu-id="71fee-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="71fee-113">Project Operations integracija sastoji se od sledeće integracije komponenata:</span><span class="sxs-lookup"><span data-stu-id="71fee-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="71fee-114">Project Operations podešavanje i integracija podataka o konfiguraciji</span><span class="sxs-lookup"><span data-stu-id="71fee-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="71fee-115">Procene i stvarne vrednosti u projektu</span><span class="sxs-lookup"><span data-stu-id="71fee-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="71fee-116">Fakture projekta</span><span class="sxs-lookup"><span data-stu-id="71fee-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="71fee-117">Upravljanje troškovima</span><span class="sxs-lookup"><span data-stu-id="71fee-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="71fee-118">Faktura prodavca</span><span class="sxs-lookup"><span data-stu-id="71fee-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
