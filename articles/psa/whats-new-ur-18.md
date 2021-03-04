---
title: Šta je novo ili promenjeno u izdanju 18 ispravke za Project Service Automation verzije 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 18 ispravke za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147220"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="0de9f-103">Project Service Automation izdanje ispravke 18, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="0de9f-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="0de9f-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0de9f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="0de9f-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="0de9f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0de9f-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="0de9f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0de9f-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="0de9f-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="0de9f-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0de9f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0de9f-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 18.</span><span class="sxs-lookup"><span data-stu-id="0de9f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="0de9f-110">Broj izrade ove verzije je V3.10.8.12 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="0de9f-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="0de9f-111">Izdanje ispravke 18</span><span class="sxs-lookup"><span data-stu-id="0de9f-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="0de9f-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="0de9f-112">Bug fixes</span></span>

<span data-ttu-id="0de9f-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="0de9f-113">**Time and Expense**</span></span>

- <span data-ttu-id="0de9f-114">Popravljeno: tokovi **Opoziv**, **Zahtev** i **Otkaži odobrenje** izbacuju izuzetke sa nejasnim porukama o greškama.</span><span class="sxs-lookup"><span data-stu-id="0de9f-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="0de9f-115">Popravljeno: Kada **Otkaži odobrenje** ne uspe za trošak, ne izbacuje se relevantna greška izuzetka.</span><span class="sxs-lookup"><span data-stu-id="0de9f-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="0de9f-116">Popravljeno: Mreža stavke vremena pogrešno obrađuje neradne dane u Australiji nakon prebacivanja letnjeg vremena (DST) u oktobru.</span><span class="sxs-lookup"><span data-stu-id="0de9f-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="0de9f-117">Popravljeno: Nepravilna logika podrazumevanih vrednosti sprečava podnošenje troškova.</span><span class="sxs-lookup"><span data-stu-id="0de9f-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="0de9f-118">Popravljeno: Kada odobrenje stavke vremena ne uspe, odobrenje ostaje u statusu **Na čekanju**.</span><span class="sxs-lookup"><span data-stu-id="0de9f-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="0de9f-119">Popravljeno: SQL greške pri masovnim odobrenjima (zastoj / istek vremena).</span><span class="sxs-lookup"><span data-stu-id="0de9f-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="0de9f-120">Popravljeno: Značajni problemi sa performansama u korisničkom iskustvu izazvani ažuriranjem članova tima prilikom odobravanja unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="0de9f-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="0de9f-121">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="0de9f-121">**Project Management**</span></span>

- <span data-ttu-id="0de9f-122">Popravljeno: Obaveštenje o vremenskoj zoni premešteno je sa prikaza **Sravnjenje** na glavni obrazac **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="0de9f-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="0de9f-123">Popravljeno: Predložak kalendara nema ispravne podrazumevane vrednosti kada se otvori novi obrazac projekta.</span><span class="sxs-lookup"><span data-stu-id="0de9f-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="0de9f-124">Popravljeno: Za Chromium pregledače, korisnici ne mogu lako da izaberu prethodne zadatke koje će izbrisati.</span><span class="sxs-lookup"><span data-stu-id="0de9f-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="0de9f-125">Popravljeno: Kreiranje ili kopiranje **projekta iz praznog predloška** preuzima nepovezane dodele.</span><span class="sxs-lookup"><span data-stu-id="0de9f-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="0de9f-126">Popravljeno: U specifičnim rubnim slučajevima, kreiranje novog zadatka iz mreže zadataka dovodi do stvaranja duplikata zapisa.</span><span class="sxs-lookup"><span data-stu-id="0de9f-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="0de9f-127">Popravljeno: U ručnom režimu korisnici ne mogu da ažuriraju datume početka zadatka da budu kasniji od sačuvanog trenutnog datuma.</span><span class="sxs-lookup"><span data-stu-id="0de9f-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="0de9f-128">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="0de9f-128">**Resource Management**</span></span>

- <span data-ttu-id="0de9f-129">Popravljeno: Red podzbira u prikazu **Sravnjenje** pogrešno izračunava odstupanje rezervacija nakon produženja rezervacije.</span><span class="sxs-lookup"><span data-stu-id="0de9f-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="0de9f-130">Popravljeno: Prikaz **Sravnjenje** pogrešno prikazuje dodeljene resurse kada resurs koji je moguće rezervisati ima kalendar koji se ne podudara sa kalendarom projekta.</span><span class="sxs-lookup"><span data-stu-id="0de9f-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="0de9f-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0de9f-131">**Sales**</span></span>

- <span data-ttu-id="0de9f-132">Popravljeno: Kada se stavke vremena ponovo odobre (**Odobri > Otkaži >** Ponovo odobri), kreira se duplikat nenaplative stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="0de9f-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
