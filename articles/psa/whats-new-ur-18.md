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
ms.openlocfilehash: b35c2f8f67e1bb75493a8787f1c4d8c2baf74d51
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280775"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="07a73-103">Project Service Automation izdanje ispravke 18, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="07a73-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="07a73-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="07a73-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="07a73-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="07a73-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="07a73-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="07a73-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="07a73-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="07a73-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="07a73-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="07a73-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="07a73-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 18.</span><span class="sxs-lookup"><span data-stu-id="07a73-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="07a73-110">Broj izrade ove verzije je V3.10.8.12 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="07a73-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="07a73-111">Izdanje ispravke 18</span><span class="sxs-lookup"><span data-stu-id="07a73-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="07a73-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="07a73-112">Bug fixes</span></span>

<span data-ttu-id="07a73-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="07a73-113">**Time and Expense**</span></span>

- <span data-ttu-id="07a73-114">Popravljeno: tokovi **Opoziv**, **Zahtev** i **Otkaži odobrenje** izbacuju izuzetke sa nejasnim porukama o greškama.</span><span class="sxs-lookup"><span data-stu-id="07a73-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="07a73-115">Popravljeno: Kada **Otkaži odobrenje** ne uspe za trošak, ne izbacuje se relevantna greška izuzetka.</span><span class="sxs-lookup"><span data-stu-id="07a73-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="07a73-116">Popravljeno: Mreža stavke vremena pogrešno obrađuje neradne dane u Australiji nakon prebacivanja letnjeg vremena (DST) u oktobru.</span><span class="sxs-lookup"><span data-stu-id="07a73-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="07a73-117">Popravljeno: Nepravilna logika podrazumevanih vrednosti sprečava podnošenje troškova.</span><span class="sxs-lookup"><span data-stu-id="07a73-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="07a73-118">Popravljeno: Kada odobrenje stavke vremena ne uspe, odobrenje ostaje u statusu **Na čekanju**.</span><span class="sxs-lookup"><span data-stu-id="07a73-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="07a73-119">Popravljeno: SQL greške pri masovnim odobrenjima (zastoj / istek vremena).</span><span class="sxs-lookup"><span data-stu-id="07a73-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="07a73-120">Popravljeno: Značajni problemi sa performansama u korisničkom iskustvu izazvani ažuriranjem članova tima prilikom odobravanja unosa vremena.</span><span class="sxs-lookup"><span data-stu-id="07a73-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="07a73-121">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="07a73-121">**Project Management**</span></span>

- <span data-ttu-id="07a73-122">Popravljeno: Obaveštenje o vremenskoj zoni premešteno je sa prikaza **Sravnjenje** na glavni obrazac **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="07a73-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="07a73-123">Popravljeno: Predložak kalendara nema ispravne podrazumevane vrednosti kada se otvori novi obrazac projekta.</span><span class="sxs-lookup"><span data-stu-id="07a73-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="07a73-124">Popravljeno: Za Chromium pregledače, korisnici ne mogu lako da izaberu prethodne zadatke koje će izbrisati.</span><span class="sxs-lookup"><span data-stu-id="07a73-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="07a73-125">Popravljeno: Kreiranje ili kopiranje **projekta iz praznog predloška** preuzima nepovezane dodele.</span><span class="sxs-lookup"><span data-stu-id="07a73-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="07a73-126">Popravljeno: U specifičnim rubnim slučajevima, kreiranje novog zadatka iz mreže zadataka dovodi do stvaranja duplikata zapisa.</span><span class="sxs-lookup"><span data-stu-id="07a73-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="07a73-127">Popravljeno: U ručnom režimu korisnici ne mogu da ažuriraju datume početka zadatka da budu kasniji od sačuvanog trenutnog datuma.</span><span class="sxs-lookup"><span data-stu-id="07a73-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="07a73-128">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="07a73-128">**Resource Management**</span></span>

- <span data-ttu-id="07a73-129">Popravljeno: Red podzbira u prikazu **Sravnjenje** pogrešno izračunava odstupanje rezervacija nakon produženja rezervacije.</span><span class="sxs-lookup"><span data-stu-id="07a73-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="07a73-130">Popravljeno: Prikaz **Sravnjenje** pogrešno prikazuje dodeljene resurse kada resurs koji je moguće rezervisati ima kalendar koji se ne podudara sa kalendarom projekta.</span><span class="sxs-lookup"><span data-stu-id="07a73-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="07a73-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="07a73-131">**Sales**</span></span>

- <span data-ttu-id="07a73-132">Popravljeno: Kada se stavke vremena ponovo odobre (**Odobri > Otkaži >** Ponovo odobri), kreira se duplikat nenaplative stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="07a73-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]