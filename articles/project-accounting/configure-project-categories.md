---
title: Konfigurisanje kategorija projekta
description: Ova tema pruža informacije o podešavanju kategorija projekata.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131945"
---
# <a name="configure-project-categories"></a><span data-ttu-id="c6969-103">Konfigurisanje kategorija projekta</span><span class="sxs-lookup"><span data-stu-id="c6969-103">Configure project categories</span></span>

<span data-ttu-id="c6969-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="c6969-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c6969-105">Usluga Project Operations nudi snažne mogućnosti za kategorizaciju prihoda i troškova na projektima.</span><span class="sxs-lookup"><span data-stu-id="c6969-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="c6969-106">Kategorije pružaju mogućnost izveštavanja o projektnim transakcijama i sprovode knjiženje u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="c6969-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="c6969-107">Sledeći dijagram ilustruje korelaciju između kategorija transakcija, deljenih kategorija i kategorija projekata.</span><span class="sxs-lookup"><span data-stu-id="c6969-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="c6969-108">Kategorije transakcija su osnovno grupisanje za projektne transakcije.</span><span class="sxs-lookup"><span data-stu-id="c6969-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="c6969-109">Unutar te grupacije postoji skup deljenih kategorija koje se mogu deliti između aplikacija i modula.</span><span class="sxs-lookup"><span data-stu-id="c6969-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="c6969-110">Ulazeći još dalje u detalje, kategorije projekata su najosnovniji nivo kategorija.</span><span class="sxs-lookup"><span data-stu-id="c6969-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="c6969-111">Kategorije projekata su specifične za pravno lice, modul i aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="c6969-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelacija između kategorija transakcija, deljenih kategorija i kategorija projekata](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="c6969-113">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="c6969-113">Transaction categories</span></span>

<span data-ttu-id="c6969-114">Kategorije transakcija predstavljaju osnovno grupisanje za projektne transakcije i nisu specifične za preduzeće ili tip transakcije.</span><span class="sxs-lookup"><span data-stu-id="c6969-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="c6969-115">Na primer, Contoso Robotics koristi kategorije Dizajn, Putovanje, Instalacija i Uslužne transakcije za grupisanje projektnih transakcija.</span><span class="sxs-lookup"><span data-stu-id="c6969-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="c6969-116">Kategorije transakcija definisane su u modulu usluge Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6969-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="c6969-117">Idite na **Podešavanja** \> **Kategorije transakcija** da otvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="c6969-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="c6969-118">Kreirajte novu kategoriju transakcija bilo izborom **Nova** ili izborom **Uvezi iz Excel tabele**.</span><span class="sxs-lookup"><span data-stu-id="c6969-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="c6969-119">Deljene kategorije</span><span class="sxs-lookup"><span data-stu-id="c6969-119">Shared categories</span></span>

<span data-ttu-id="c6969-120">Dynamics 365 koristi koncept deljenih kategorija za kategorizaciju troškova u različitim aplikacijama, kao što su Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c6969-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="c6969-121">Za svaku kreiranu kategoriju transakcija, Project Operations automatski kreira četiri povezane deljene kategorije: Sati, Troškovi, Naknade i Stavka.</span><span class="sxs-lookup"><span data-stu-id="c6969-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="c6969-122">Možete da pregledate i prilagodite deljene kategorije tako što ćete otići na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Deljene kategorije**.</span><span class="sxs-lookup"><span data-stu-id="c6969-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="c6969-123">Kategorije projekata</span><span class="sxs-lookup"><span data-stu-id="c6969-123">Project categories</span></span>

<span data-ttu-id="c6969-124">Kategorije projekata predstavljaju najosnovniji nivo konfiguracije kategorija i moraju se konfigurisati odvojeno i za svako preduzeće, po računovođi projekta.</span><span class="sxs-lookup"><span data-stu-id="c6969-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="c6969-125">Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Kategorije projekata**.</span><span class="sxs-lookup"><span data-stu-id="c6969-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="c6969-126">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c6969-126">Select **New**.</span></span>
3. <span data-ttu-id="c6969-127">Izaberite **ID kategorije** deljene kategorije koju ste kreirali u prethodnom odeljku.</span><span class="sxs-lookup"><span data-stu-id="c6969-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="c6969-128">Project Operations omogućava upotrebu samo onih zajedničkih kategorija koje su povezane sa kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="c6969-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="c6969-129">Izaberite grupu kategorija.</span><span class="sxs-lookup"><span data-stu-id="c6969-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="c6969-130">Grupe kategorija</span><span class="sxs-lookup"><span data-stu-id="c6969-130">Category groups</span></span>

<span data-ttu-id="c6969-131">Grupe kategorija koriste se za deljenje svojstava, pre svega profila za knjiženje, između povezanih kategorija projekta.</span><span class="sxs-lookup"><span data-stu-id="c6969-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="c6969-132">Za svaku vrstu transakcije mora postojati najmanje jedna grupa kategorija, a svakoj kategoriji projekta dodeljena je grupa.</span><span class="sxs-lookup"><span data-stu-id="c6969-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="c6969-133">Specifikacije knjiženja u usluzi Project Operations definisane su pravilima profila troškova i prihoda projekta, kategorijama projekata i grupama kategorija.</span><span class="sxs-lookup"><span data-stu-id="c6969-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="c6969-134">Možete da podesite grupe kategorija ako odete na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Grupe kategorija**.</span><span class="sxs-lookup"><span data-stu-id="c6969-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
