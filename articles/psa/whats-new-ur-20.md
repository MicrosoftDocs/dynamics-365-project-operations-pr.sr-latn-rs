---
title: Šta je novo ili promenjeno u Project Service Automation izdanju ispravke 20 u verziji 3
description: U ovoj temi date su funkcije i ispravke koje su dostupne u Project Service Automation izdanju ispravke 20 u verziji 3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006528"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="13156-103">Project Service Automation izdanje ispravke 20, u verziji 3</span><span class="sxs-lookup"><span data-stu-id="13156-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="13156-104">Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="13156-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="13156-105">Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti.</span><span class="sxs-lookup"><span data-stu-id="13156-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="13156-106">Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="13156-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="13156-107">Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku.</span><span class="sxs-lookup"><span data-stu-id="13156-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="13156-108">Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="13156-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="13156-109">U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 20.</span><span class="sxs-lookup"><span data-stu-id="13156-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="13156-110">Broj izrade ove verzije je V 3.10.31.37 i uglavnom je dostupna putem samostalnog ažuriranja u junu 2020. godine.</span><span class="sxs-lookup"><span data-stu-id="13156-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="13156-111">Izdanje ispravke 20</span><span class="sxs-lookup"><span data-stu-id="13156-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="13156-112">Ispravke grešaka</span><span class="sxs-lookup"><span data-stu-id="13156-112">Bug fixes</span></span>

<span data-ttu-id="13156-113">**Upravljanje projektima**</span><span class="sxs-lookup"><span data-stu-id="13156-113">**Project Management**</span></span>

<span data-ttu-id="13156-114">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="13156-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="13156-115">Uvoz članova projektnog tima metodom raspodele koja zahteva sate rezultira nejasnom porukom o grešci kada su navedeni sati nula.</span><span class="sxs-lookup"><span data-stu-id="13156-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="13156-116">Korisnici dobijaju pogrešnu grešku kada je u polje **Opis** unet maksimalan broj znakova za projektni zadatak.</span><span class="sxs-lookup"><span data-stu-id="13156-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="13156-117">Stranica **preuzimanja Microsoft Dynamics 365 Project Service Automation programskog dodatka** preusmerava se na stranicu za preuzimanje na engleskom kada su podešavanja jezika korisnika postavljena na japanski.</span><span class="sxs-lookup"><span data-stu-id="13156-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="13156-118">Kada dođe do greške na serveru, oznaka sinhronizacije na kartici **Raspored** obrasca **Projekti** ponekad ostaje.</span><span class="sxs-lookup"><span data-stu-id="13156-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="13156-119">Suvišna ažuriranja zadataka se šalju serveru kada je zadatak izmenjen.</span><span class="sxs-lookup"><span data-stu-id="13156-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="13156-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="13156-120">**Sales**</span></span>

<span data-ttu-id="13156-121">Popravljeni su sledeći problemi:</span><span class="sxs-lookup"><span data-stu-id="13156-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="13156-122">Na obrascu **Ugovor**, dvostruki klik na **Kreiraj fakturu** kreira dve fakture za jedan stvarni zapis.</span><span class="sxs-lookup"><span data-stu-id="13156-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="13156-123">U rešenju Internet Explorer 11,korisnici ne mogu da kreiraju stavke troškova.</span><span class="sxs-lookup"><span data-stu-id="13156-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="13156-124">Storniranje troškova i storniranje nefakturisanih stvarnih podataka o prodaji nisu povezani.</span><span class="sxs-lookup"><span data-stu-id="13156-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="13156-125">Dugme **Osveži stvarne troškove** na obrascu **Projekat** ne osvežava stavku **Stvarni sati za zadatak**.</span><span class="sxs-lookup"><span data-stu-id="13156-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="13156-126">Dodatna komponenta **PreValidateProjectTeamMemberCreate** može da kreira duplirane generičke resurse koji mogu da se rezervišu kada je atribut **msdyn_isgenericresourceprojectscoped** podešen na **Netačno**.</span><span class="sxs-lookup"><span data-stu-id="13156-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="13156-127">**Ponovo izračunaj** briše naplative troškove detalja ponude zasnovane na proizvodu i detalje predmeta ugovora.</span><span class="sxs-lookup"><span data-stu-id="13156-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="13156-128">U određenim scenarijima dodatna komponenta **PostEstimateLineUpdate** prikazuje grešku izuzetka nedefinisane reference.</span><span class="sxs-lookup"><span data-stu-id="13156-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="13156-129">Trajanje vremenske faze na **Grafikonu analize profitabilnosti** se ne podudara se sa trajanjem troškova u detaljima linije ponude sa fiksnom cenom na ponudi.</span><span class="sxs-lookup"><span data-stu-id="13156-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="13156-130">Vrednosti za jedinicu i grupu jedinica ne postaju ispravno podrazumevano za kategorije troškova u obrascima **Detalji o predmetu ugovora** i **Detalji stavke ponude**.</span><span class="sxs-lookup"><span data-stu-id="13156-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="13156-131">Liste **Cena koštanja po jedinici za organizaciju** dozvoljavaju preklapanje efikasnosti datuma.</span><span class="sxs-lookup"><span data-stu-id="13156-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="13156-132">Korisnicima nije dozvoljeno da menjaju **OrgUnit** kada tip porudžbine nije zasnovan na radu jer će dovesti do greške izuzetka nepostojeće reference.</span><span class="sxs-lookup"><span data-stu-id="13156-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="13156-133">Pri pokušaju kretanja iz obrasca **Detalji stavke ponude** natrag na karticu **Ponuda**, obrazac se osvežava i prikazuje karticu **Rezime**.</span><span class="sxs-lookup"><span data-stu-id="13156-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]