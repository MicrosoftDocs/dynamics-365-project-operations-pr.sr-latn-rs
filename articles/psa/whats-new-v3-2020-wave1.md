---
title: Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3.x talasu 1 za 2020. godinu
description: U ovoj temi date su informacije o tome šta je novo i šta se promenilo u rešenju Project Service Automation u verziji 3 talasu 1 za 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996853"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="86290-103">Šta je novo ili promenjeno u aplikaciji Project Service Automation u verziji 3 talasu 1 za 2020. godinu</span><span class="sxs-lookup"><span data-stu-id="86290-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="86290-104">Tema ističe ključne činjenice koje treba uzeti u obzir prilikom nadogradnje kada prelazite na najnovije izdanje rešenja Project Service Automation (PSA) verzije 3.x talasa 1 za 2020.</span><span class="sxs-lookup"><span data-stu-id="86290-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="86290-105">Stavka vremena</span><span class="sxs-lookup"><span data-stu-id="86290-105">Time entry</span></span>
<span data-ttu-id="86290-106">Iskustvo stavke vremena je prošireno kako bi isporučilo mogućnosti produžetka stavke vremena u više scenarija klijenata.</span><span class="sxs-lookup"><span data-stu-id="86290-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="86290-107">Ovo obuhvata mogućnost dodavanja tipova stavki, koji sada pokreću određeno ponašanje na osnovu naziva plana polja **Podešavanja stavke vremena**, prikazano kao **Izvor vremena**.</span><span class="sxs-lookup"><span data-stu-id="86290-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="86290-108">Novo rešenje, pod nazivom „Time, Expense, Statusing, and Approvals“ (TESA) je dodat kako bi bila podržana ova funkcionalnost.</span><span class="sxs-lookup"><span data-stu-id="86290-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="86290-109">Činjenica koju treba uzeti u obzir prilikom nadogradnje</span><span class="sxs-lookup"><span data-stu-id="86290-109">Upgrade consideration</span></span>
<span data-ttu-id="86290-110">Kako bi ova funkcionalnost bila podržana, uloge u okviru rešenja PSA su ažurirana tako da obuhvataju nove privilegije.</span><span class="sxs-lookup"><span data-stu-id="86290-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="86290-111">Ove privilegije omogućavaju pristup za čitanje novom entitetu, **Podešavanja stavke vremena**.</span><span class="sxs-lookup"><span data-stu-id="86290-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="86290-112">Korisnicima koji zahtevaju mogućnost evidentiranja vremena bi pored postojećih uloga trebalo dodeliti korisničku ulogu **Korisnik stavke vremena**.</span><span class="sxs-lookup"><span data-stu-id="86290-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="86290-113">Ova uloga uključuje novu funkcionalnost i obezbeđuje da stavka vremena i dalje radi.</span><span class="sxs-lookup"><span data-stu-id="86290-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="86290-114">Pored toga, ako imate prilagođene module aplikacija koji sadrže sve obrasce za entitet unosa vremena, moraćete da uklonite **TESA obrazac za brzo kreiranje stavke vremena** iz modula.</span><span class="sxs-lookup"><span data-stu-id="86290-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="86290-115">Trenutno promenjene proširene stavke vremena</span><span class="sxs-lookup"><span data-stu-id="86290-115">Currently extended time entry changes</span></span>
<span data-ttu-id="86290-116">Kako bi se smanjio uticaj na trenutne korisnike stavke vremena, ova promena uloge je jedini suštinski zahtev koji je neophodan kako bi se i dalje koristila stavka vremena.</span><span class="sxs-lookup"><span data-stu-id="86290-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="86290-117">Ako ste kreirali prilagođene prikaze ili odvojena iskustva stavki vremena, morate podesiti polja **Podešavanje stavke vremena** na ispravnu PSA vrednost.</span><span class="sxs-lookup"><span data-stu-id="86290-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]