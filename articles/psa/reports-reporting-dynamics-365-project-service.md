---
title: Matična stranica za izveštavanje
description: Ova tema pruža informacije o izveštavanju u aplikaciji Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e1a645b157c56066e56b22ea8cf0324fbc1ddd2c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120335"
---
# <a name="reporting-home-page"></a><span data-ttu-id="ea524-103">Matična stranica za izveštavanje</span><span class="sxs-lookup"><span data-stu-id="ea524-103">Reporting home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ea524-104">Microsoft Dynamics 365 Project Service Automation omogućava da organizacije zasnovane na projektima efikasno upravljaju poslovnim operacijama preduzeća.</span><span class="sxs-lookup"><span data-stu-id="ea524-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="ea524-105">Na bilo kojem projektu, članovi tima moraju da upravljaju mogućnostima za poslovanje, daju poslovnu ponudu i planiraju posao, obezbeđuju resurse za projekte, upravljaju poslom prema planu, naplaćuju za posao, a zatim obavljaju ostale poslove kako bi projekat priveli kraju.</span><span class="sxs-lookup"><span data-stu-id="ea524-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="ea524-106">Mogućnost izveštavanja o poslovnim operacijama je ključna za utvrđivanje stanja organizacije i preduzimanje bilo kakvih korektivnih postupaka koji su potrebni.</span><span class="sxs-lookup"><span data-stu-id="ea524-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="ea524-107">PSA koristi Microsoft Dynamics 365 metode i tehnologije izveštavanja za celokupno izveštavanje.</span><span class="sxs-lookup"><span data-stu-id="ea524-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="ea524-108">Još informacija o opcijama za izveštavanje potražite u odeljku [Vodič za pisanje izveštaja za Dynamics 365 Customer Engagement (on-premises), verziju 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="ea524-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="ea524-109">Čarobnjak za izveštaje</span><span class="sxs-lookup"><span data-stu-id="ea524-109">Report Wizard</span></span>

<span data-ttu-id="ea524-110">Čarobnjak za izveštaje omogućava onima koji nisu programeri da kreiraju jednostavne izveštaje.</span><span class="sxs-lookup"><span data-stu-id="ea524-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="ea524-111">Budući da je aplikacija razvijena na postojećoj platformi, iskustvo je isto kao iskustvo dokumentovano u članku [Kreiranje ili izmena izveštaja pomoću čarobnjaka za izveštaje](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="ea524-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="ea524-112">Međutim, koristićete entitete specifične za Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ea524-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="ea524-113">Prilagođeni izveštaji za SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="ea524-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="ea524-114">Ako vaše preduzeće zahteva određeni izveštaj koji se ne može kreirati pomoću čarobnjaka za izveštaje, možete da kreirate prilagođeni izveštaj.</span><span class="sxs-lookup"><span data-stu-id="ea524-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="ea524-115">Morate instalirati Microsoft Visual Studio, uz odgovarajuće Microsoft SQL Server Data Tools i dodatke za kreiranje izveštaja.</span><span class="sxs-lookup"><span data-stu-id="ea524-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="ea524-116">Za više informacija o alatkama i verzijama pogledajte članak [Okruženje za pisanje izveštaja koje koristi SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="ea524-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="ea524-117">Informacije o kreiranju prilagođenog izveštaja potražite u članku [Kreiranje novog izveštaja pomoću usluge SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="ea524-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="ea524-118">Power BI aplikacije za uvide</span><span class="sxs-lookup"><span data-stu-id="ea524-118">Power BI insights apps</span></span>

<span data-ttu-id="ea524-119">Microsoft Power BI i Dynamics 365 zajedno pružaju moćan način rada sa podacima, u vidu aplikacija za uvide.</span><span class="sxs-lookup"><span data-stu-id="ea524-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="ea524-120">Informacije o dostupnosti aplikacija za uvide potražite u članku [Power BI stranica sa aplikacijama za uvide](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="ea524-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ea524-121">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="ea524-121">Additional resources</span></span>
<span data-ttu-id="ea524-122">Za više informacija o izveštavanju u aplikaciji PSA, pogledajte sledeće teme:</span><span class="sxs-lookup"><span data-stu-id="ea524-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="ea524-123">Rad sa Project Service modelom podataka</span><span class="sxs-lookup"><span data-stu-id="ea524-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="ea524-124">Kontrolne table</span><span class="sxs-lookup"><span data-stu-id="ea524-124">Dashboards</span></span>](reports-dashboards.md)

