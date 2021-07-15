---
title: Šta je novo ili promenjeno u izdanju 33 ispravke usluge Project Service Automation verzije 3
description: U ovoj temi navedene su funkcije i ispravke koje su dostupne u izdanju 33 ispravke usluge Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334593"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="3c879-103">Šta je novo ili promenjeno u izdanju 33 ispravke usluge Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="3c879-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3c879-104">Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3c879-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="3c879-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="3c879-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3c879-106">Kompatibilna je sa sistemom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3c879-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3c879-107">Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku.</span><span class="sxs-lookup"><span data-stu-id="3c879-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="3c879-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3c879-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3c879-109">U ovoj temi navedene su funkcije koje su nove ili promenjene u izdanju 33 usluge Project Service Automation verzije 3.</span><span class="sxs-lookup"><span data-stu-id="3c879-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="3c879-110">Ova verzija ima broj verzije 3.10.54.98 i opšte je dostupna putem samostalnog ažuriranja u julu 2021.</span><span class="sxs-lookup"><span data-stu-id="3c879-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="3c879-111">Izdanje ispravke 33</span><span class="sxs-lookup"><span data-stu-id="3c879-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3c879-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="3c879-112">Bug fixes</span></span>

<span data-ttu-id="3c879-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="3c879-113">**Time and Expense**</span></span>

<span data-ttu-id="3c879-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3c879-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="3c879-115">Dva zaključana polja, **msdyn_description** i **msdyn_externaldescription** mogu se uređivati nakon prosleđivanja.</span><span class="sxs-lookup"><span data-stu-id="3c879-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="3c879-116">Poruka o grešci se javlja ako se kreira trošak koji nije povezan sa projektom.</span><span class="sxs-lookup"><span data-stu-id="3c879-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="3c879-117">Kada se kreira stavka vremena, uloga resursa je podrazumevano neaktivna.</span><span class="sxs-lookup"><span data-stu-id="3c879-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="3c879-118">Stavke u glavnoj knjizi povezane sa opozvanim i izbrisanim troškovima se ne brišu.</span><span class="sxs-lookup"><span data-stu-id="3c879-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="3c879-119">Na **obrascu za brzo kreiranje stavke vremena**, ažurirajte prikaz **Lista projektnih zadataka** da biste podrazumevano prikazani datum promenili u datum početka zadatka.</span><span class="sxs-lookup"><span data-stu-id="3c879-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="3c879-120">Kada kreirate unos vremena sa kartice **Povezano** resursa koji može da se rezerviše, stavka vremena se pogrešno kreira za prijavljenog korisnika umesto za nadređeni resurs koji može da se rezerviše.</span><span class="sxs-lookup"><span data-stu-id="3c879-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="3c879-121">Nova polja se dodaju u dijalog **Grupno odobravanje MDD**.</span><span class="sxs-lookup"><span data-stu-id="3c879-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="3c879-122">**Planiranje projekta**</span><span class="sxs-lookup"><span data-stu-id="3c879-122">**Project planning**</span></span>

<span data-ttu-id="3c879-123">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3c879-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="3c879-124">Spore performanse kreiranja projekata kada se predlošci radnog vremena projekta primenjuju sa složenim kalendarima.</span><span class="sxs-lookup"><span data-stu-id="3c879-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="3c879-125">Kada je datum početka veći od datuma završetka, na predlošku projekta kopiranja prikazuje se greška zbog razlika u vremenskoj komponenti svakog polja.</span><span class="sxs-lookup"><span data-stu-id="3c879-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="3c879-126">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="3c879-126">**Resource management**</span></span>

<span data-ttu-id="3c879-127">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3c879-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="3c879-128">U upitu o ukupnoj iskorišćenosti resursa koristi se netačan parametar, a XML dovodi do netačnih rezultata filtera na mreži **Ukupna iskorišćenost resursa**.</span><span class="sxs-lookup"><span data-stu-id="3c879-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="3c879-129">Potvrda **Produžetak rezervacija** prikazuje netačan datum završetka za rezervacije.</span><span class="sxs-lookup"><span data-stu-id="3c879-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="3c879-130">**Prodaja**</span><span class="sxs-lookup"><span data-stu-id="3c879-130">**Sales**</span></span>

<span data-ttu-id="3c879-131">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="3c879-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="3c879-132">Poruka o grešci se javlja ako se kreira cena kategorije sa vrednostima koje nedostaju.</span><span class="sxs-lookup"><span data-stu-id="3c879-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="3c879-133">Javlja se poruka o grešci ako se kreira kontrolna tačka predmeta ugovora bez stavke porudžbine.</span><span class="sxs-lookup"><span data-stu-id="3c879-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
