---
title: Model bezbednosti
description: U ovoj temi date su informacije o bezbednosnom modelu u usluzi Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951226"
---
# <a name="security-model"></a><span data-ttu-id="c6aea-103">Model bezbednosti</span><span class="sxs-lookup"><span data-stu-id="c6aea-103">Security Model</span></span>

<span data-ttu-id="c6aea-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="c6aea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c6aea-105">Microsoft Dynamics 365 Project Operations sadrži jedinstveni bezbednosni model koji omogućava model poslovne bezbednosti zasnovan na ulogama koji sarađuje sa Microsoft Office grupama.</span><span class="sxs-lookup"><span data-stu-id="c6aea-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="c6aea-106">Bezbednosne uloge</span><span class="sxs-lookup"><span data-stu-id="c6aea-106">Security roles</span></span>
<span data-ttu-id="c6aea-107">Izložene mogućnosti usluge Project Operations uključuju sledeće uloge:</span><span class="sxs-lookup"><span data-stu-id="c6aea-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="c6aea-108">Uloga</span><span class="sxs-lookup"><span data-stu-id="c6aea-108">Role</span></span>                          | <span data-ttu-id="c6aea-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c6aea-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="c6aea-110">Scope</span><span class="sxs-lookup"><span data-stu-id="c6aea-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="c6aea-111">Menadžer obuke</span><span class="sxs-lookup"><span data-stu-id="c6aea-111">Practice manager</span></span>              | <span data-ttu-id="c6aea-112">Podržava izveštavanje između projekata.</span><span class="sxs-lookup"><span data-stu-id="c6aea-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="c6aea-113">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-113">Business unit</span></span>              |
| <span data-ttu-id="c6aea-114">Davalac odobrenja za projekat</span><span class="sxs-lookup"><span data-stu-id="c6aea-114">Project approver</span></span>              | <span data-ttu-id="c6aea-115">Odobrava vreme i troškove u odnosu na projekat.</span><span class="sxs-lookup"><span data-stu-id="c6aea-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="c6aea-116">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-116">Business unit</span></span> |
| <span data-ttu-id="c6aea-117">Administrator naplate projekta</span><span class="sxs-lookup"><span data-stu-id="c6aea-117">Project billing administrator</span></span> | <span data-ttu-id="c6aea-118">Izrađuje predlog fakture.</span><span class="sxs-lookup"><span data-stu-id="c6aea-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="c6aea-119">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-119">Business unit</span></span> |
| <span data-ttu-id="c6aea-120">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="c6aea-120">Project manager</span></span>               | <span data-ttu-id="c6aea-121">Izrađuje plan projekta i zahteva resurse.</span><span class="sxs-lookup"><span data-stu-id="c6aea-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="c6aea-122">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-122">Business unit</span></span> |
| <span data-ttu-id="c6aea-123">Resurs za projekat</span><span class="sxs-lookup"><span data-stu-id="c6aea-123">Project resource</span></span>              | <span data-ttu-id="c6aea-124">Članovi tima koji mogu da rezervišu i prijave vreme.</span><span class="sxs-lookup"><span data-stu-id="c6aea-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="c6aea-125">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-125">Business unit</span></span>|
| <span data-ttu-id="c6aea-126">Menadžer resursa</span><span class="sxs-lookup"><span data-stu-id="c6aea-126">Resource manager</span></span>              | <span data-ttu-id="c6aea-127">Sve funkcije upravljanja resursima, poput ispunjavanja zahteva za resursima i rezervacija, razdvojene su da bi podržale hibridnu konfiguraciju menadžera projekata + menadžera resursa i jedinstvenu i centralizovanu ulogu menadžera resursa.</span><span class="sxs-lookup"><span data-stu-id="c6aea-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="c6aea-128">Poslovna jedinica</span><span class="sxs-lookup"><span data-stu-id="c6aea-128">Business unit</span></span> |


<span data-ttu-id="c6aea-129">Microsoft Project za veb uključuje sledeće uloge:</span><span class="sxs-lookup"><span data-stu-id="c6aea-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="c6aea-130">Uloga</span><span class="sxs-lookup"><span data-stu-id="c6aea-130">Role</span></span>           | <span data-ttu-id="c6aea-131">Opis</span><span class="sxs-lookup"><span data-stu-id="c6aea-131">Description</span></span>                                                                                                        | <span data-ttu-id="c6aea-132">Scope</span><span class="sxs-lookup"><span data-stu-id="c6aea-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="c6aea-133">Korisnik projekta</span><span class="sxs-lookup"><span data-stu-id="c6aea-133">Project user</span></span>   | <span data-ttu-id="c6aea-134">Korisnik koji sarađuje u programu Project   koji može da kreira sopstvene projekte i pregleda sve projekte koji se dele sa   njim.</span><span class="sxs-lookup"><span data-stu-id="c6aea-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="c6aea-135">Korisnik</span><span class="sxs-lookup"><span data-stu-id="c6aea-135">User</span></span>   |
| <span data-ttu-id="c6aea-136">Projektni sistem</span><span class="sxs-lookup"><span data-stu-id="c6aea-136">Project system</span></span> | <span data-ttu-id="c6aea-137">Uloga koja se koristi za kontekst   aplikacije.</span><span class="sxs-lookup"><span data-stu-id="c6aea-137">Role used for application   context.</span></span> <span data-ttu-id="c6aea-138">Klijenti ne bi trebalo da koriste ovu sistemsku ulogu.</span><span class="sxs-lookup"><span data-stu-id="c6aea-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="c6aea-139">Globalni</span><span class="sxs-lookup"><span data-stu-id="c6aea-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="c6aea-140">Provođenje bezbednosti</span><span class="sxs-lookup"><span data-stu-id="c6aea-140">Security enforcement</span></span>
<span data-ttu-id="c6aea-141">Radnje koje se izvode na nivou projekta izvode se u kontekstu prijavljenog korisnika.</span><span class="sxs-lookup"><span data-stu-id="c6aea-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="c6aea-142">To znači da je za kreiranje, otvaranje ili brisanje projekta od korisnika potrebno da ima pristup dostupan u CDS-u.</span><span class="sxs-lookup"><span data-stu-id="c6aea-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="c6aea-143">Pristup CDS-u se može odobriti putem bilo kog od mogućih mehanizama uključenih u platformu.</span><span class="sxs-lookup"><span data-stu-id="c6aea-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="c6aea-144">Na primer, korisnik sa većim opsegom može pristupiti projektu ili ako je izvršena eksplicitna akcija deljenja projekta koja korisniku odobrava pristup.</span><span class="sxs-lookup"><span data-stu-id="c6aea-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="c6aea-145">Važno je to uzeti u obzir prilikom kreiranja projekata u usluzi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6aea-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="c6aea-146">Savremena grupna saradnja sa uslugom Project Operations</span><span class="sxs-lookup"><span data-stu-id="c6aea-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="c6aea-147">Project za veb i Project Operations podržavaju savremene grupe za saradnju.</span><span class="sxs-lookup"><span data-stu-id="c6aea-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="c6aea-148">Korisnici dodati u projekat putem grupe mogu da uređuju plan projekta.</span><span class="sxs-lookup"><span data-stu-id="c6aea-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="c6aea-149">Project za veb automatski dodaje korisnike u grupu po dodeljivanju.</span><span class="sxs-lookup"><span data-stu-id="c6aea-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="c6aea-150">Grupe omogućavaju zajednički rad na dozvolama projekta i pratećim artefaktima za saradnju.</span><span class="sxs-lookup"><span data-stu-id="c6aea-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="c6aea-151">Sledeći dijagram prikazuje događaje i promene stanja koji se dešavaju tokom procesa grupnog dodeljivanja.</span><span class="sxs-lookup"><span data-stu-id="c6aea-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="c6aea-152">Usluga Project Operations ne kreira grupu implicitnom akcijom, već samo eksplicitnom akcijom pritiska grupa.</span><span class="sxs-lookup"><span data-stu-id="c6aea-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="c6aea-153">Pretraga članova grupe u dijalogu **Upravljanje grupama** ograničena je na one koji su postavljeni kao deo bezbednosne grupe okruženja.</span><span class="sxs-lookup"><span data-stu-id="c6aea-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="c6aea-154">Više informacija potražite u članku [Kontrola korisničkog pristupa okruženjima: bezbednosne grupe i licence](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="c6aea-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Grupni režim](./media/groupsmode.png)

1. <span data-ttu-id="c6aea-156">Projekat se kreira i njegov vlasnik je korisnik koji ga je kreirao.</span><span class="sxs-lookup"><span data-stu-id="c6aea-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="c6aea-157">Vlasnik projekta je obavešten o timu.</span><span class="sxs-lookup"><span data-stu-id="c6aea-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="c6aea-158">Tim-vlasnik se mapira u navedenu ili kreiranu Office grupu.</span><span class="sxs-lookup"><span data-stu-id="c6aea-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="c6aea-159">Prvobitni vlasnik projekta se dodaje u Office grupu.</span><span class="sxs-lookup"><span data-stu-id="c6aea-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="c6aea-160">Preporuka za primenu</span><span class="sxs-lookup"><span data-stu-id="c6aea-160">Deployment recommendation</span></span>
<span data-ttu-id="c6aea-161">Kako se model saradnje Office grupe razvija, funkcionalnost će biti dodavana kako bi se pružala detaljnija kontrola tokom vremena.</span><span class="sxs-lookup"><span data-stu-id="c6aea-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="c6aea-162">Klijenti koji danas primenjuju Project Operations podstiču se da se usredsrede na tradicionalni Microsoft Dynamics 365 model bezbednosti.</span><span class="sxs-lookup"><span data-stu-id="c6aea-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="c6aea-163">Za više informacija, pogledajte [Bezbednost u usluzi Common Data Service](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="c6aea-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="c6aea-164">Project Operations i Microsoft Dynamics 365 Finance bezbednost</span><span class="sxs-lookup"><span data-stu-id="c6aea-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="c6aea-165">Usluga Project Operations uključuje sledeće uloge:</span><span class="sxs-lookup"><span data-stu-id="c6aea-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="c6aea-166">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="c6aea-166">Project manager</span></span>
- <span data-ttu-id="c6aea-167">Računovođa projekta</span><span class="sxs-lookup"><span data-stu-id="c6aea-167">Project accountant</span></span>

<span data-ttu-id="c6aea-168">Više informacija o bezbednosti u usluzi Finance potražite u odeljku [Bezbednost zasnovana na ulogama](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="c6aea-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]