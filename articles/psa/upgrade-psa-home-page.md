---
title: Nadogradnja matične stranice
description: Ova tema pokazuje gde možete pronaći važne informacije o novim i izmenjenim funkcijama u aplikaciji Dynamics 365 Project Service Automation i postupak nadogradnje na najnoviju verziju.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa25d069de8098c0e8788c9ebb8aa3426eec5db9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121775"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="0df25-103">Nadogradnja matične stranice</span><span class="sxs-lookup"><span data-stu-id="0df25-103">Upgrade home page</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="0df25-104">Nadogradnja sa aplikacije PSA verzije 2.x ili 1.x na verziju 3.x</span><span class="sxs-lookup"><span data-stu-id="0df25-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="0df25-105">Nove instance</span><span class="sxs-lookup"><span data-stu-id="0df25-105">New instances</span></span>

<span data-ttu-id="0df25-106">Od 17. maja 2019. godine, kada se izabere Project Service Automation tokom obezbeđivanja nove instance, podrazumevano se instalira verzija 3.x.</span><span class="sxs-lookup"><span data-stu-id="0df25-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="0df25-107">Postojeće instance</span><span class="sxs-lookup"><span data-stu-id="0df25-107">Existing instances</span></span>

<span data-ttu-id="0df25-108">Predhodno su klijenti koji imaju instancu aplikacije PSA verzije 2.x, a morali su da je nadograde na verziju 3.x, koja predstavlja PSA verziju zasnovanu na objedinjenom interfejsu klijenta, morali da se obrate Microsoft podršci i dostave detalje o instanci kako bi podrška mogla da omogući instancu za nadogradnju na verziju 3.x.</span><span class="sxs-lookup"><span data-stu-id="0df25-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA , had to contact Microsoft Support and provide the details of thier instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="0df25-109">Od 1. marta 2020. će kupci koji imaju instancu PSA verzije 2.x, a moraju da je nadograde na verziju 3.x, moći da nadograde svoje instance direktno sa portala za administraciju, a da ne moraju da se obrate Microsoft podršci.</span><span class="sxs-lookup"><span data-stu-id="0df25-109">As of March 1st, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="0df25-110">PSA verzije 3.x uključuje značajne promene.</span><span class="sxs-lookup"><span data-stu-id="0df25-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="0df25-111">Razvijen je u okviru objedinjenog interfejsa kako bi pružio poboljšano korisničko iskustvo.</span><span class="sxs-lookup"><span data-stu-id="0df25-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="0df25-112">Redizajnirana aplikacija omogućava dosledan i jedinstven korisnički interfejs i sledi principe prilagodljivog dizajna za optimalni pregled na bilo kojoj veličini ekrana ili uređaju.</span><span class="sxs-lookup"><span data-stu-id="0df25-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="0df25-113">Došlo je i do drugih promena u celoj aplikaciji.</span><span class="sxs-lookup"><span data-stu-id="0df25-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="0df25-114">Neke od oblasti koje su izmenjene uključuju određivanje cena, rezervisanje i dodeljivanje resursa, vremena i troškova, kao i odobrenja.</span><span class="sxs-lookup"><span data-stu-id="0df25-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="0df25-115">Pre nego što započnete postupak nadogradnje, preporučujemo vam da obavite sledeće zadatke:</span><span class="sxs-lookup"><span data-stu-id="0df25-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="0df25-116">Proverite da li su Dynamics 365 Field Service i Project Service Automation instalirani na identifikovanoj instanci.</span><span class="sxs-lookup"><span data-stu-id="0df25-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="0df25-117">Ako su oba rešenja instalirana, trebalo bi da planirate nadogradnju oba pre nego što nastavite sa redovnom upotrebom instance.</span><span class="sxs-lookup"><span data-stu-id="0df25-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="0df25-118">Pažljivo pregledajte sledeće teme.</span><span class="sxs-lookup"><span data-stu-id="0df25-118">Carefully review the following topics.</span></span> <span data-ttu-id="0df25-119">Ako ste svesni promena između verzija i razumete ih, to će vam pomoći u procesu nadogradnje.</span><span class="sxs-lookup"><span data-stu-id="0df25-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="0df25-120">Ove teme pružaju informacije o glavnim promenama u aplikaciji PSA, uz razmatranje nadogradnje i preporuke za planiranje nadogradnje na verziju 3.x.</span><span class="sxs-lookup"><span data-stu-id="0df25-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="0df25-121">Šta je novo ili promenjeno u aplikaciji Project Service Automation verzije 3</span><span class="sxs-lookup"><span data-stu-id="0df25-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="0df25-122">Činjenice koje treba uzeti u obzir prilikom nadogradnje - Project Service Automation verzije 2.x ili 1.x na verziju 3.x</span><span class="sxs-lookup"><span data-stu-id="0df25-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="0df25-123">Nadogradite instancu sandbox okruženja da biste procenili promene u implementaciji pre nadogradnje proizvodne instance.</span><span class="sxs-lookup"><span data-stu-id="0df25-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="0df25-124">Nakon što pregledate prethodno spomenute teme i spremni ste za nadogradnju na PSA verzije 3.x ili verziju zasnovanu na objedinjenom interfejsu klijenta, prosledite zahtev Microsoft podršci kako bi nadogradnja postala dostupna u centru administracije.</span><span class="sxs-lookup"><span data-stu-id="0df25-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="0df25-125">U zahtevu navedite detalje instance.</span><span class="sxs-lookup"><span data-stu-id="0df25-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="0df25-126">Starije verzije aplikacije PSA (PSA verzije 2.x) u novoj instanci</span><span class="sxs-lookup"><span data-stu-id="0df25-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="0df25-127">Od 17. maja 2019. godine, sve nove instance će kao podrazumevanog klijenta imati objedinjeni interfejs klijenta.</span><span class="sxs-lookup"><span data-stu-id="0df25-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="0df25-128">Kako bismo obezbedili usklađenost sa ovom promenom, podrazumevano ćemo obezbediti PSA verzije 3.x i Field Service verzije 8.x jer su ove verzije dizajnirane da funkcionišu sa klijentom UCI (objedinjeni interfejs klijenta).</span><span class="sxs-lookup"><span data-stu-id="0df25-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="0df25-129">Od 1. marta 2020. klijenti sistema Dynamics PSA više neće moći da stvaraju nova okruženja sa starijim PSA verzijama, na primer PSA verzije 2.x ili starije.</span><span class="sxs-lookup"><span data-stu-id="0df25-129">Starting March 1st 2020, customers of Dynamics PSA will no longer be able to create a new environments with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="0df25-130">Svako novo okruženje će biti PSA verzije 3.x.</span><span class="sxs-lookup"><span data-stu-id="0df25-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="0df25-131">Da biste dobili najbolje iskustvo prilikom korišćena starije verzije Field Service i PSA aplikacija, idite na stranicu **Podešavanja sistema** i za polje **Korišćenje samo novog objedinjenog interfejsa (preporučeno)** izaberite **Ne** jer ove verzije nisu dizajnirane da budu ispravno učitane u objedinjeni interfejs klijenta.</span><span class="sxs-lookup"><span data-stu-id="0df25-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="0df25-132">Nakon što isključite objedinjeni interfejs klijenta, ove verzije usluga Field Service i PSA možete otvoriti i pokrenuti pomoću starog veb-klijenta.</span><span class="sxs-lookup"><span data-stu-id="0df25-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
