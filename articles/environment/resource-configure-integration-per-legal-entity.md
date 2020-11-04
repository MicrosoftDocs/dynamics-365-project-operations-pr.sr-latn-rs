---
title: Konfigurisanje integracije za Project Operations po pravnom licu
description: Ova tema pruža informacije o tome kako da podesite integraciju po pravnom licu u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c0e02ef2d17bf49209369f7adad681d9a5981e2a
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096769"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="853dd-103">Konfigurisanje integracije za Project Operations po pravnom licu</span><span class="sxs-lookup"><span data-stu-id="853dd-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="853dd-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="853dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="853dd-105">Ova tema vas vodi kroz korake potrebne za konfigurisanje usluge Dynamics 365 Project Operations po pravnom licu.</span><span class="sxs-lookup"><span data-stu-id="853dd-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="853dd-106">Omogućite ključne funkcije u usluzi Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="853dd-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="853dd-107">Dovršite sledeće korake da biste omogućili potrebne funkcije.</span><span class="sxs-lookup"><span data-stu-id="853dd-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="853dd-108">U usluzi Dynamics 365 Finance idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="853dd-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="853dd-109">U odeljku **Lista funkcija** , pronađite i omogućite sledeće funkcije:</span><span class="sxs-lookup"><span data-stu-id="853dd-109">In **Feature list** , find and enable the following features:</span></span>
  
    - <span data-ttu-id="853dd-110">**Omogućite više predmeta ugovora za projekat**</span><span class="sxs-lookup"><span data-stu-id="853dd-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="853dd-111">**Omogućite Project Operations u usluzi Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="853dd-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="853dd-112">Ako ne vidite **Ključne funkcije** , proverite da li vaša verzija usluge Finance ispunjava minimalni zahtev za verziju (verzija aplikacije 10.0.13 sa primenjenim svim ispravkama kvaliteta ili novija).</span><span class="sxs-lookup"><span data-stu-id="853dd-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="853dd-113">Izaberite **Proveri da li ima ažuriranja** da biste osvežili listu funkcija.</span><span class="sxs-lookup"><span data-stu-id="853dd-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="853dd-114">Definišite scenario primene usluge Project Operations za pravno lice</span><span class="sxs-lookup"><span data-stu-id="853dd-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="853dd-115">Project Operations možete da omogućite u usluzi Dynamics 365 Customer Engagement na nivou pravnog lica.</span><span class="sxs-lookup"><span data-stu-id="853dd-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="853dd-116">Možete da imate jedno pravno lice koje koristi Project Operations u usluzi Dynamics 365 Customer Engagement za scenarije zasnovane na resursima/koji nisu zasnovani na zalihama.</span><span class="sxs-lookup"><span data-stu-id="853dd-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="853dd-117">U istom okruženju možete imati drugo pravno lice koje koristi Project Operations za scenarije zasnovane na zalihama/porudžbenicama.</span><span class="sxs-lookup"><span data-stu-id="853dd-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="853dd-118">U usluzi Dynamics 365 Finance idite na **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Globalno upravljanje projektima i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="853dd-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="853dd-119">Na listi dostupnih pravnih lica izaberite entitete u kojima će biti omogućeno više predmeta ugovora i funkcije Project Operations u usluzi Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="853dd-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="853dd-120">Nemojte birati pravna lica koja će koristiti Project Operations za scenarije zasnovane na zalihama/porudžbenicama.</span><span class="sxs-lookup"><span data-stu-id="853dd-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="853dd-121">Pravno lice se može odabrati samo ako nema postojeće projekte.</span><span class="sxs-lookup"><span data-stu-id="853dd-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="853dd-122">Konfigurisanje parametara upravljanja projektima i računovodstva</span><span class="sxs-lookup"><span data-stu-id="853dd-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="853dd-123">Svako pravno lice koje koristi Project Operations u usluzi Dynamics 365 Customer Engagement mora da ima skup podrazumevanih parametara.</span><span class="sxs-lookup"><span data-stu-id="853dd-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="853dd-124">Ovi parametri su konfigurisani na kartici **Project Operations** na stranici **Upravljanje projektom i računovodstveni parametri**.</span><span class="sxs-lookup"><span data-stu-id="853dd-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="853dd-125">Parametri su:</span><span class="sxs-lookup"><span data-stu-id="853dd-125">The parameters are:</span></span>

  - <span data-ttu-id="853dd-126">**Podrazumevane vrednosti tipova obračuna** : Project Operations koristi fiksni skup podrazumevanih zadataka tipa naplate koji se moraju mapirati sa svojstvima stavki usluge Finance.</span><span class="sxs-lookup"><span data-stu-id="853dd-126">**Billing type defaults** : Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="853dd-127">Napravite zapis za svaku vrstu obračuna: **Nije navedeno** , **Naplativo** , **Nenaplativo** , **Besplatno** i **Nije dostupno**.</span><span class="sxs-lookup"><span data-stu-id="853dd-127">Create a record for each billing type: **Not specified** , **Chargeable** , **Non-chargeable** , **Complimentary** , and **Not available**.</span></span>
  - <span data-ttu-id="853dd-128">**Podrazumevane kategorije projekata** : Izaberite podrazumevane kategorije projekata koje će se koristiti za svaku vrstu transakcije.</span><span class="sxs-lookup"><span data-stu-id="853dd-128">**Project category defaults** : Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="853dd-129">Ove podrazumevane vrednosti će se koristiti u **Project Operations dnevniku integracije** i u procenama gde nije navedena kategorija transakcije za stvarni projekat.</span><span class="sxs-lookup"><span data-stu-id="853dd-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="853dd-130">**Prognoze** : Izaberite model prognoze koji će se koristiti za procenu vremena i troškova.</span><span class="sxs-lookup"><span data-stu-id="853dd-130">**Forecasts** : Select the forecast model to be used for time and expense estimates.</span></span>
