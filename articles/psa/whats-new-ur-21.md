---
title: Šta je novo ili promenjeno u izdanju 21 ispravke za Project Service Automation u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u izdanju 21 ispravke za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126725"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="b1c5d-103">Project Service Automation izdanje ispravke 21, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="b1c5d-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="b1c5d-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b1c5d-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b1c5d-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b1c5d-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b1c5d-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b1c5d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b1c5d-109">U ovoj temi date su funkcije koje su nove ili su promenjene u izdanju 21 ispravke za Project Service Automation u verziji 3.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="b1c5d-110">Broj izrade ove verzije je V 3.10.32.50 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="b1c5d-111">Izdanje ispravke 21</span><span class="sxs-lookup"><span data-stu-id="b1c5d-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b1c5d-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="b1c5d-112">Bug fixes</span></span>

<span data-ttu-id="b1c5d-113">**Vreme i trošak**</span><span class="sxs-lookup"><span data-stu-id="b1c5d-113">**Time and Expense**</span></span>

<span data-ttu-id="b1c5d-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b1c5d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1c5d-115">Prilikom hostovanja **Kontrole mreže stavke vremena** na kontrolnoj tabli, mreža ne koristi punu širinu kontejnera mreže kontrolne table.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="b1c5d-116">Za određene vremenske zone, kontrola mreže **Stavka vremena** ne prikazuje zapise.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="b1c5d-117">Stavke vremena koje su posle 21:00 pojavljuju se pogrešnog dana.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="b1c5d-118">Korisnici ne mogu da pošalju troškove ako kategorija troškova, **Potrebna je priznanica za troškove** nema vrednost.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="b1c5d-119">**Upravljanje resursima**</span><span class="sxs-lookup"><span data-stu-id="b1c5d-119">**Resource Management**</span></span>

<span data-ttu-id="b1c5d-120">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b1c5d-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1c5d-121">Neaktivne rezervacije se prikazuju u prikazu **Sravnjenje**.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="b1c5d-122">Nedostaje validacija generičkog resursa kako bi se osiguralo da postoji važeći status rezervacije.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="b1c5d-123">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="b1c5d-123">**Project Management**</span></span>

<span data-ttu-id="b1c5d-124">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b1c5d-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1c5d-125">Mreže obrasca za **Projekat** (**Dodela resursa**, **Zadatak**, prikaz **Sravnjenje**, **Procene troškova**) se mogu uređivati čak i kada projekat nije aktivan.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="b1c5d-126">Duplirani klijenti se ne mogu objediniti sa klijentima koji su povezani sa potvrđenim ugovorima za projekat.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="b1c5d-127">Kada se doda resurs koji nema važeći kalendar, sistem ne vraća poruku o grešci prilagođenu korisniku.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="b1c5d-128">Dugme **Dodaj zadatak** na mreži zadataka je omogućeno kada je projekat povezan na **programski dodataka za Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="b1c5d-129">Napor nekontrolisano raste kada je zadatak sa kategorijom dodeljen resursu sa ulogom za koju je definisana cena koštanja.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="b1c5d-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="b1c5d-130">**Sales**</span></span>

<span data-ttu-id="b1c5d-131">Uneta su sledeća poboljšanja:</span><span class="sxs-lookup"><span data-stu-id="b1c5d-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="b1c5d-132">**Učestalost fakturisanja** i **Početak naplate** su preseljeni na karticu **Raspored fakturisanja**.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="b1c5d-133">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="b1c5d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="b1c5d-134">**Ukupna prodajna cena** je nula (0) za **Kategoriju**, mada **Uloga** ima ukupnu prodajnu cenu koja nije nula.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="b1c5d-135">Klijenti ne mogu da menjaju vrednost polja **Status fakture** na **Spremno za fakturisanje** kada neki drugi prilagođeni proces ažurira dodatno polje.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="b1c5d-136">Dugme **Osveži stavke fakture** može da kreira više dupliranih stavki ako se više puta izaberu.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="b1c5d-137">Dugme **Ažuriraj cene** ne radi na podformi **Cene uloga** u obrascu **Brzi prikaz**.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="b1c5d-138">Logika **Rešenje prodajnog cenovnika** nepravilno rukuje vremenskim zonama, što rezultira pogrešnim odabirom cenovnika.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="b1c5d-139">**Ukupni stvarni trošak** projekta se može isključiti jednim delom nakon što se odobri jedna stavka vremena.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="b1c5d-140">Logika **Rešenje cena** ne daje poruku o grešci prilagođenu korisniku ako **Vraćena cena uloge** nema vrednosti u poljima **'Primarna jedinica'** i **'Cena u osnovnoj jedinici'**.</span><span class="sxs-lookup"><span data-stu-id="b1c5d-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
