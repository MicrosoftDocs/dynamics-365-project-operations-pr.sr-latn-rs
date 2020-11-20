---
title: Konfigurišite program Project Service Automation
description: Koraci za konfigurisanje aplikacije Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129200"
---
# <a name="configure-project-service"></a><span data-ttu-id="44297-103">Konfigurisanje aplikacije Project Service</span><span class="sxs-lookup"><span data-stu-id="44297-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="44297-104">Pre nego što budete mogli da koristite mogućnosti automatizovanja [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sistemu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] za upravljanje poslovnim kontaktima, projektima i resursima, morate da dovršite nekoliko konfiguracionih koraka da biste obezbedili da se rešenje [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] podudara sa potrebama organizacije.</span><span class="sxs-lookup"><span data-stu-id="44297-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="44297-105">U ove korake spada sledeće:</span><span class="sxs-lookup"><span data-stu-id="44297-105">These steps include:</span></span>  
  
-   <span data-ttu-id="44297-106">[Podesite vremenske jedinice](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="44297-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="44297-107">Konfigurišite jedinice vremena u katalogu proizvoda koje ćete koristiti kao osnovu za planiranje i naplatu projekata.</span><span class="sxs-lookup"><span data-stu-id="44297-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="44297-108">[Podesite valute i devizne kurseve](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="44297-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="44297-109">Podesite valute koje ćete koristiti za projekte.</span><span class="sxs-lookup"><span data-stu-id="44297-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="44297-110">[Kreirajte organizacione jedinice](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="44297-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="44297-111">Podesite grupe koje vaše preduzeće koristi za podelu poslovanja, bilo po geografiji, poslovnoj funkciji ili drugoj logičkoj podeli.</span><span class="sxs-lookup"><span data-stu-id="44297-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="44297-112">[Podesite učestalosti fakturisanja](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="44297-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="44297-113">Podesite vremenske periode koje želite da koristite za naplatu klijentima.</span><span class="sxs-lookup"><span data-stu-id="44297-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="44297-114">[Konfigurišite kategorije transakcija](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="44297-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="44297-115">Podesite kategorije transakcija za koje vaši savetnici mogu da zaračunaju naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="44297-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="44297-116">[Kreirajte kategorije troškova](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="44297-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="44297-117">Podesite kategorije za koje vaši savetnici mogu da zaračunaju naplative i nenaplative troškove.</span><span class="sxs-lookup"><span data-stu-id="44297-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="44297-118">[Kreirajte stavke kataloga proizvoda](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="44297-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="44297-119">Dodajte proizvode koje prodajete, kao što su softverske licence, u katalog proizvoda.</span><span class="sxs-lookup"><span data-stu-id="44297-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="44297-120">[Kreirajte cenovnik](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="44297-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="44297-121">Konfigurišite različite cenovnike, u zavisnosti od toga koliko želite da naplatite klijentima za svaku ulogu koju njihov projekat zahteva.</span><span class="sxs-lookup"><span data-stu-id="44297-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="44297-122">[Podesite resurse](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="44297-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="44297-123">Dodajte veštine, stručnosti, uloge resursa i ostale informacije o resursima koje vam trebaju za projekte.</span><span class="sxs-lookup"><span data-stu-id="44297-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="44297-124">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="44297-124">See Also</span></span>  
 <span data-ttu-id="44297-125">[Pregled usluge Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="44297-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="44297-126">[Konfigurišite program Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="44297-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="44297-127">[Vodič za menadžera za poslovne kontakte](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44297-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="44297-128">[Vodič za menadžera projekta](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44297-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="44297-129">[Vodič za menadžera resursa](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="44297-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="44297-130">Vodič za vreme, trošak i saradnju</span><span class="sxs-lookup"><span data-stu-id="44297-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
