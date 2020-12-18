---
title: Šta je novo ili promenjeno u izdanju 26 ispravke Project Service Automation verzije 3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643280"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="6b687-102">Project Service Automation izdanje ispravke 26, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="6b687-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="6b687-103">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6b687-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6b687-104">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="6b687-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6b687-105">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6b687-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6b687-106">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="6b687-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6b687-107">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6b687-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6b687-108">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 26.</span><span class="sxs-lookup"><span data-stu-id="6b687-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="6b687-109">Ova verzija ima broj verzije V3.10.44.59 i generalno je dostupna putem samostalnog ažuriranja u decembru 2020.</span><span class="sxs-lookup"><span data-stu-id="6b687-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="6b687-110">Izdanje ispravke 26</span><span class="sxs-lookup"><span data-stu-id="6b687-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="6b687-111">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="6b687-111">Bug fixes</span></span>

<span data-ttu-id="6b687-112">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="6b687-112">**Time and Expense**</span></span>

<span data-ttu-id="6b687-113">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="6b687-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="6b687-114">Korisnici mogu da promene zadatak na stavci vremena koja je odobrena/podneta.</span><span class="sxs-lookup"><span data-stu-id="6b687-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="6b687-115">Greška „Referenca objekta nije podešena“ prilikom čuvanja stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="6b687-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="6b687-116">Uvoz stavke vremena iz dodeljivanja resursa kreira stavke vremena sa netačnim vrednostima datuma i vremena.</span><span class="sxs-lookup"><span data-stu-id="6b687-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="6b687-117">Kada su instalirane aplikacije Project Service Automation i Field Service, dugme **Novo** se prikazuje dva puta na komandnoj traci za stavke vremena u aplikaciji Field Service.</span><span class="sxs-lookup"><span data-stu-id="6b687-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="6b687-118">Ćelije **Dozvoli ažuriranja jedinice** i **grupe jedinica** sada rade u mreži **Procene troškova**.</span><span class="sxs-lookup"><span data-stu-id="6b687-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="6b687-119">Obrazac **Ažuriraj uređivanje stavke vremena** uključuje **Vremensku osu**.</span><span class="sxs-lookup"><span data-stu-id="6b687-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="6b687-120">Odobrenje vremena za stavke vremena koje se ne odnose na projekat blokiraju sistem prilikom pretrage za ulogu odobravaoca projekta.</span><span class="sxs-lookup"><span data-stu-id="6b687-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="6b687-121">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="6b687-121">**Resource Management**</span></span>

<span data-ttu-id="6b687-122">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="6b687-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="6b687-123">Dodata je validacija u dodatnoj komponenti **PostProjectCreate** za proveru primarnog zahteva pre njegovog kreiranja.</span><span class="sxs-lookup"><span data-stu-id="6b687-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="6b687-124">Obrazac za brzo kreiranje **Član projektnog tima** daje izuzetak prazne reference ako se polja uklone iz obrasca.</span><span class="sxs-lookup"><span data-stu-id="6b687-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="6b687-125">Generiranje zahteva za 12 sati tokom 1 godine neće uspeti.</span><span class="sxs-lookup"><span data-stu-id="6b687-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="6b687-126">Poboljšana poruka o grešci za izuzetak prazne reference tokom kreiranja zahteva za resursom.</span><span class="sxs-lookup"><span data-stu-id="6b687-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="6b687-127">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="6b687-127">**Project Management**</span></span>

<span data-ttu-id="6b687-128">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="6b687-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="6b687-129">Poboljšana validacija za odgovor na izuzetak prazne reference generisane u dodatnoj komponenti **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="6b687-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="6b687-130">Projekti objavljeni u programskom dodatku za računare usluge Microsoft Project brišu neraspoređene zadatke.</span><span class="sxs-lookup"><span data-stu-id="6b687-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="6b687-131">Dodata je nova validacija kada referenca projekta zadatka nije važeća zbog izuzetka prazne reference u dodatnoj komponenti **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="6b687-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="6b687-132">Mreža člana tima ne prikazuje različite zadatke u zapisu člana tima.</span><span class="sxs-lookup"><span data-stu-id="6b687-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="6b687-133">Dodate su nove poruke za proveru valjanosti i poruke greške zbog izuzetka prazne reference u dodatnoj komponenti **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="6b687-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="6b687-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6b687-134">**Sales**</span></span>

<span data-ttu-id="6b687-135">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="6b687-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="6b687-136">Prilikom izbora stavke zasnovane na projektu u ponudu ili ugovoru, dugme **Predlog** bi trebalo da bude vidljivo samo pri odabiru linije zasnovane na proizvodu povezane sa postojećim proizvodom.</span><span class="sxs-lookup"><span data-stu-id="6b687-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="6b687-137">Podelite privilegiju **Create_Product** iz privilegije **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="6b687-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="6b687-138">Brisanje stavke u faktoru dovodi do neuspele prazne reference na **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="6b687-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
