---
title: Konfigurisanje kategorija projekta
description: Ova tema pruža informacije o podešavanju kategorija projekata.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995188"
---
# <a name="configure-project-categories"></a><span data-ttu-id="43b09-103">Konfigurisanje kategorija projekta</span><span class="sxs-lookup"><span data-stu-id="43b09-103">Configure project categories</span></span>

<span data-ttu-id="43b09-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="43b09-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43b09-105">Usluga Project Operations nudi snažne mogućnosti za kategorizaciju prihoda i troškova na projektima.</span><span class="sxs-lookup"><span data-stu-id="43b09-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="43b09-106">Kategorije pružaju mogućnost izveštavanja o projektnim transakcijama i sprovode knjiženje u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="43b09-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="43b09-107">Sledeći dijagram ilustruje korelaciju između kategorija transakcija, deljenih kategorija i kategorija projekata.</span><span class="sxs-lookup"><span data-stu-id="43b09-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="43b09-108">Kategorije transakcija su osnovno grupisanje za projektne transakcije.</span><span class="sxs-lookup"><span data-stu-id="43b09-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="43b09-109">Unutar te grupacije postoji skup deljenih kategorija koje se mogu deliti između aplikacija i modula.</span><span class="sxs-lookup"><span data-stu-id="43b09-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="43b09-110">Ulazeći još dalje u detalje, kategorije projekata su najosnovniji nivo kategorija.</span><span class="sxs-lookup"><span data-stu-id="43b09-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="43b09-111">Kategorije projekata su specifične za pravno lice, modul i aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="43b09-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelacija između kategorija transakcija, deljenih kategorija i kategorija projekata](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="43b09-113">Kategorije transakcija</span><span class="sxs-lookup"><span data-stu-id="43b09-113">Transaction categories</span></span>

<span data-ttu-id="43b09-114">Kategorije transakcija predstavljaju osnovno grupisanje za projektne transakcije i nisu specifične za preduzeće ili tip transakcije.</span><span class="sxs-lookup"><span data-stu-id="43b09-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="43b09-115">Na primer, Contoso Robotics koristi kategorije Dizajn, Putovanje, Instalacija i Uslužne transakcije za grupisanje projektnih transakcija.</span><span class="sxs-lookup"><span data-stu-id="43b09-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="43b09-116">Kategorije transakcija definisane su u modulu usluge Project Operations.</span><span class="sxs-lookup"><span data-stu-id="43b09-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="43b09-117">Idite na **Podešavanja** \> **Kategorije transakcija** da otvorite obrazac.</span><span class="sxs-lookup"><span data-stu-id="43b09-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="43b09-118">Kreirajte novu kategoriju transakcija bilo izborom **Nova** ili izborom **Uvezi iz Excel tabele**.</span><span class="sxs-lookup"><span data-stu-id="43b09-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="43b09-119">Deljene kategorije</span><span class="sxs-lookup"><span data-stu-id="43b09-119">Shared categories</span></span>

<span data-ttu-id="43b09-120">Dynamics 365 koristi koncept deljenih kategorija za kategorizaciju troškova u različitim aplikacijama, kao što su Dynamics 365 Finance, Dynamics 365 Supply Chain i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="43b09-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="43b09-121">Za svaku kreiranu kategoriju transakcija, Project Operations automatski kreira četiri povezane deljene kategorije: Sati, Troškovi, Naknade i Stavka.</span><span class="sxs-lookup"><span data-stu-id="43b09-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="43b09-122">Možete da pregledate i prilagodite deljene kategorije tako što ćete otići na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Deljene kategorije**.</span><span class="sxs-lookup"><span data-stu-id="43b09-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="43b09-123">Kategorije projekata</span><span class="sxs-lookup"><span data-stu-id="43b09-123">Project categories</span></span>

<span data-ttu-id="43b09-124">Kategorije projekata predstavljaju najosnovniji nivo konfiguracije kategorija i moraju se konfigurisati odvojeno i za svako preduzeće, po računovođi projekta.</span><span class="sxs-lookup"><span data-stu-id="43b09-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="43b09-125">Idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Kategorije projekata**.</span><span class="sxs-lookup"><span data-stu-id="43b09-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="43b09-126">Izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="43b09-126">Select **New**.</span></span>
3. <span data-ttu-id="43b09-127">Izaberite **ID kategorije** deljene kategorije koju ste kreirali u prethodnom odeljku.</span><span class="sxs-lookup"><span data-stu-id="43b09-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="43b09-128">Project Operations omogućava upotrebu samo onih zajedničkih kategorija koje su povezane sa kategorijama transakcija.</span><span class="sxs-lookup"><span data-stu-id="43b09-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="43b09-129">Izaberite grupu kategorija.</span><span class="sxs-lookup"><span data-stu-id="43b09-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="43b09-130">Grupe kategorija</span><span class="sxs-lookup"><span data-stu-id="43b09-130">Category groups</span></span>

<span data-ttu-id="43b09-131">Grupe kategorija koriste se za deljenje svojstava, pre svega profila za knjiženje, između povezanih kategorija projekta.</span><span class="sxs-lookup"><span data-stu-id="43b09-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="43b09-132">Za svaku vrstu transakcije mora postojati najmanje jedna grupa kategorija, a svakoj kategoriji projekta dodeljena je grupa.</span><span class="sxs-lookup"><span data-stu-id="43b09-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="43b09-133">Specifikacije knjiženja u usluzi Project Operations definisane su pravilima profila troškova i prihoda projekta, kategorijama projekata i grupama kategorija.</span><span class="sxs-lookup"><span data-stu-id="43b09-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="43b09-134">Možete da podesite grupe kategorija ako odete na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Kategorije** \> **Grupe kategorija**.</span><span class="sxs-lookup"><span data-stu-id="43b09-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]