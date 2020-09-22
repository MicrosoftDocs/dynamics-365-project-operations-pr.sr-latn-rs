---
title: Konfigurišite program Project Service Automation
description: Koraci za konfigurisanje aplikacije Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755149"
---
# <a name="configure-project-service"></a><span data-ttu-id="80161-103">Konfigurisanje aplikacije Project Service</span><span class="sxs-lookup"><span data-stu-id="80161-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="80161-104">Pre nego što budete mogli da koristite mogućnosti automatizovanja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sistemu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] za upravljanje poslovnim kontaktima, projektima i resursima, morate da dovršite nekoliko konfiguracionih koraka da biste obezbedili da se rešenje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] podudara sa potrebama organizacije.</span><span class="sxs-lookup"><span data-stu-id="80161-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="80161-105">U ove korake spada sledeće:</span><span class="sxs-lookup"><span data-stu-id="80161-105">These steps include:</span></span>  
  
-   <span data-ttu-id="80161-106">[Podesite vremenske jedinice](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="80161-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="80161-107">Konfigurišite jedinice vremena u katalogu proizvoda koje ćete koristiti kao osnovu za planiranje i naplatu projekata.</span><span class="sxs-lookup"><span data-stu-id="80161-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="80161-108">[Podesite valute i devizne kurseve](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="80161-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="80161-109">Podesite valute koje ćete koristiti za projekte.</span><span class="sxs-lookup"><span data-stu-id="80161-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="80161-110">[Kreirajte organizacione jedinice](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="80161-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="80161-111">Podesite grupe koje vaše preduzeće koristi za podelu poslovanja, bilo po geografiji, poslovnoj funkciji ili drugoj logičkoj podeli.</span><span class="sxs-lookup"><span data-stu-id="80161-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="80161-112">[Podesite učestalosti fakturisanja](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="80161-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="80161-113">Podesite vremenske periode koje želite da koristite za naplatu klijentima.</span><span class="sxs-lookup"><span data-stu-id="80161-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="80161-114">[Konfigurišite kategorije transakcija](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="80161-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="80161-115">Podesite kategorije transakcija za koje vaši savetnici mogu da zaračunaju naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="80161-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="80161-116">[Kreirajte kategorije troškova](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="80161-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="80161-117">Podesite kategorije za koje vaši savetnici mogu da zaračunaju naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="80161-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="80161-118">[Kreirajte stavke kataloga proizvoda](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="80161-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="80161-119">Dodajte proizvode koje prodajete, kao što su softverske licence, u katalog proizvoda.</span><span class="sxs-lookup"><span data-stu-id="80161-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="80161-120">[Kreirajte cenovnik](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="80161-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="80161-121">Konfigurišite različite cenovnike, u zavisnosti od toga koliko želite da naplatite klijentima za svaku ulogu koju njihov projekat zahteva.</span><span class="sxs-lookup"><span data-stu-id="80161-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="80161-122">[Podesite resurse](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="80161-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="80161-123">Dodajte veštine, stručnosti, uloge resursa i ostale informacije o resursima koje vam trebaju za projekte.</span><span class="sxs-lookup"><span data-stu-id="80161-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="80161-124">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="80161-124">See Also</span></span>  
 <span data-ttu-id="80161-125">[Pregled usluge Project Service Automation](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="80161-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="80161-126">[Konfigurišite program Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="80161-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="80161-127">[Vodič za menadžera za poslovne kontakte](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="80161-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="80161-128">[Vodič za menadžera projekta](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="80161-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="80161-129">[Vodič za menadžera resursa](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="80161-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="80161-130">Vodič za vreme, trošak i saradnju</span><span class="sxs-lookup"><span data-stu-id="80161-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
