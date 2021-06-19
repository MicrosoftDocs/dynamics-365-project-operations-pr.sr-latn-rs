---
title: Šta je novo ili promenjeno u izdanju 32 ispravke usluge Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 32 ispravke usluge Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129683"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="639c3-103">Šta je novo ili promenjeno u izdanju 32 ispravke usluge Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="639c3-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="639c3-104">Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="639c3-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="639c3-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="639c3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="639c3-106">Kompatibilna je sa sistemom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="639c3-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="639c3-107">Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku.</span><span class="sxs-lookup"><span data-stu-id="639c3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="639c3-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="639c3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="639c3-109">U ovoj temi navedene su funkcije koje su nove ili promenjene u izdanju 32 ispravke usluge Project Service Automation verzije 3.</span><span class="sxs-lookup"><span data-stu-id="639c3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="639c3-110">Ova verzija ima broj verzije 3.10.53.108 i opšte je dostupna putem samostalnog ažuriranja u junu 2021.</span><span class="sxs-lookup"><span data-stu-id="639c3-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="639c3-111">Izdanje ispravke 32</span><span class="sxs-lookup"><span data-stu-id="639c3-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="639c3-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="639c3-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="639c3-113">Opšte</span><span class="sxs-lookup"><span data-stu-id="639c3-113">General</span></span>

- <span data-ttu-id="639c3-114">Kada glavna nadogradnja ne uspe, treba blokirati samo glavne ulazne tačke aplikacije kako bi se osiguralo da deljeni entiteti i dalje budu dostupni.</span><span class="sxs-lookup"><span data-stu-id="639c3-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="639c3-115">Vreme i trošak</span><span class="sxs-lookup"><span data-stu-id="639c3-115">Time and Expense</span></span>

<span data-ttu-id="639c3-116">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="639c3-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="639c3-117">**TimeEntriesImportFromResourceAssignment** ne održava vremena početka i završetka isečaka konture dodele resursa.</span><span class="sxs-lookup"><span data-stu-id="639c3-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="639c3-118">Kada izaberete **Otvori stavku** na mreži **Stavka vremena**, možda ćete biti sprečeni da izaberete druge obrasce.</span><span class="sxs-lookup"><span data-stu-id="639c3-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="639c3-119">Dok uvozite zadatke u stavke vremena, upit klijentskog koda može da generiše dugu URL adresu koja ne uspeva u upitu.</span><span class="sxs-lookup"><span data-stu-id="639c3-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="639c3-120">U mreži **Stavka vremena**, kada se vrednost izbriše iz ćelije, fokus ne ostaje u mreži.</span><span class="sxs-lookup"><span data-stu-id="639c3-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="639c3-121">Dugme **Odbaci** je uklonjeno iz prikaza **Odobrenja obrade** za moderna odobrenja.</span><span class="sxs-lookup"><span data-stu-id="639c3-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="639c3-122">Na stabilnost i performanse grupnog odobravanja stavke vremena utiču zastoji i neuspeh u odgovarajućem rukovanju prilagođavanjima koja su povezana sa entitetom **Stavka vremena**.</span><span class="sxs-lookup"><span data-stu-id="639c3-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="639c3-123">Planiranje projekta</span><span class="sxs-lookup"><span data-stu-id="639c3-123">Project Planning</span></span>

- <span data-ttu-id="639c3-124">Izuzetak nulte reference se generiše kada ažurirate projekat koji ima nultu vrednost u polju **Jedinica ugovaranja**.</span><span class="sxs-lookup"><span data-stu-id="639c3-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="639c3-125">**Osveži ukupne vrednosti projekata** pogrešno izračunava preostali trošak i preostalu prodaju u projektu.</span><span class="sxs-lookup"><span data-stu-id="639c3-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="639c3-126">Prekomerni proračuni cena utiču na performanse povezane sa ažuriranjima na konturama dodele resursa.</span><span class="sxs-lookup"><span data-stu-id="639c3-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="639c3-127">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="639c3-127">Resource Management</span></span>

<span data-ttu-id="639c3-128">Sledeći problem je ispravljen:</span><span class="sxs-lookup"><span data-stu-id="639c3-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="639c3-129">Kada je kapacitet kalendara resursa koji može da se rezerviše veći od 1, Project Service Automation pogrešno prepoznaje kapacitet kao 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="639c3-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="639c3-130">Stoga se u prikazu rasporeda javlja beskonačna petlja.</span><span class="sxs-lookup"><span data-stu-id="639c3-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="639c3-131">Prodaja</span><span class="sxs-lookup"><span data-stu-id="639c3-131">Sales</span></span>

<span data-ttu-id="639c3-132">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="639c3-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="639c3-133">Kada se kreira stavka u glavnoj knjizi koja ima prilagođeni tip transakcije, javlja se sledeći izuzetak nulte reference: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="639c3-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="639c3-134">Uloge i kategorije koje su deaktivirane pre kopiranja ponude ne bi trebalo dodavati ulogama koje se naplaćuju i kategorijama novokopirane ponude.</span><span class="sxs-lookup"><span data-stu-id="639c3-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="639c3-135">Datum dokumenta i datum obračuna nisu usklađeni sa datumom početka koji je naveden u detaljima stavke fakture koja se kreira direktno na radnoj verziji fakture.</span><span class="sxs-lookup"><span data-stu-id="639c3-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="639c3-136">Izuzeci od nulte reference se generišu u scenarijima koji su povezani sa deaktivacijom uloga i kategorija pre kopiranja ponude.</span><span class="sxs-lookup"><span data-stu-id="639c3-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="639c3-137">Radnja **Ažuriranje cena** na stranici **Projekti** ne ažurira procene troškova i procene materijala.</span><span class="sxs-lookup"><span data-stu-id="639c3-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
