---
title: Odredite vrstu primene
description: Ova tema pruža informacije koje vam pomažu da utvrdite pravilan tip primene usluge Project Operations za vaše preduzeće.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083584"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="e77d9-103">Odredite vrstu primene</span><span class="sxs-lookup"><span data-stu-id="e77d9-103">Determine your deployment type</span></span>

<span data-ttu-id="e77d9-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="e77d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e77d9-105">Nakon kupovine licence, počnite ovde da biste utvrdili najbolji model primene usluge Dynamics 365 Project Operations pomoću [vođenog toka instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e77d9-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="e77d9-106">Kada dovršite vođeni tok instalacije, bićete preusmereni na pravi portal za upravljanje da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="e77d9-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="e77d9-107">Pogledajte detalje o primeni da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="e77d9-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="e77d9-108">Postojeći klijenti sistema Dynamics koji koriste Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e77d9-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="e77d9-109">Project Operations uključuje mogućnosti koje su isporučene sa uslugom Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="e77d9-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="e77d9-110">Putanja nadogradnje biće izdata za ove klijente u budućnosti.</span><span class="sxs-lookup"><span data-stu-id="e77d9-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="e77d9-111">Postojeći klijenti usluge Dynamics 365 Finance koji koriste upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="e77d9-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="e77d9-112">Postojeći klijenti usluge Finance koji koriste funkcionalnost upravljanja projektima i računovodstva mogu da nastave da koriste ovo kako jeste.</span><span class="sxs-lookup"><span data-stu-id="e77d9-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="e77d9-113">Pogledajte [Project Operations za scenarije zasnovane na zalihama/proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="e77d9-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="e77d9-114">Tipovi primene</span><span class="sxs-lookup"><span data-stu-id="e77d9-114">Deployment types</span></span>
<span data-ttu-id="e77d9-115">Project Operations podržava više mogućnosti primene u skladu sa vašim zahtevima.</span><span class="sxs-lookup"><span data-stu-id="e77d9-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="e77d9-116">Bez obzira na to da li ste novi ili postojeći klijent sistema Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="e77d9-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="e77d9-117">Naš [upitnik za primenu](https://aka.ms/provisionprojectoperations) će vam pomoći da odredite odgovarajuću primenu.</span><span class="sxs-lookup"><span data-stu-id="e77d9-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="e77d9-118">Rezultati će vas voditi prema jednom od sledećih tipova primene:</span><span class="sxs-lookup"><span data-stu-id="e77d9-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="e77d9-119">Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="e77d9-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="e77d9-120">Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="e77d9-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="e77d9-121">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="e77d9-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="e77d9-122">Project Operations podržavaju scenarije zaliha / proizvodnih naloga i scenarije zasnovane na resursima / bez zaliha u istom okruženju putem konfiguracija na nivou pravnog lica.</span><span class="sxs-lookup"><span data-stu-id="e77d9-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="e77d9-123">Na primer, Contoso može da koristi mogućnosti skladištenja/naručivanja u svom proizvodnom pogonu u SAD (pravno lice = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="e77d9-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="e77d9-124">Contoso može da koristi mogućnosti koji nisu zasnovane na zalihama/zasnovane na resursima u objektu Contoso Robotics Arms u Velikoj Britaniji (pravno lice = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="e77d9-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="e77d9-125">Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="e77d9-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="e77d9-126">Jednostavna primena uključuje sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="e77d9-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="e77d9-127">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="e77d9-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e77d9-128">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="e77d9-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e77d9-129">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="e77d9-129">Unified Resource Management</span></span>
- <span data-ttu-id="e77d9-130">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="e77d9-130">Time Tracking</span></span>
- <span data-ttu-id="e77d9-131">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="e77d9-131">Basic Expense</span></span>
- <span data-ttu-id="e77d9-132">Predlog fakture</span><span class="sxs-lookup"><span data-stu-id="e77d9-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="e77d9-133">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="e77d9-133">Deployment steps</span></span>
<span data-ttu-id="e77d9-134">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e77d9-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e77d9-135">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](lite-preview-subscription-sign-up.md) i [Obezbeđivanje novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="e77d9-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="e77d9-136">Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="e77d9-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="e77d9-137">Project Operations za scenarije resursa / bez zaliha uključuju sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="e77d9-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="e77d9-138">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="e77d9-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="e77d9-139">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="e77d9-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="e77d9-140">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="e77d9-140">Unified Resource Management</span></span>
- <span data-ttu-id="e77d9-141">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="e77d9-141">Time Tracking</span></span>
- <span data-ttu-id="e77d9-142">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="e77d9-142">Basic Expense</span></span>
- <span data-ttu-id="e77d9-143">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="e77d9-143">Full Expense</span></span>
- <span data-ttu-id="e77d9-144">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="e77d9-144">Receipt OCR</span></span>
- <span data-ttu-id="e77d9-145">Potpuno fakturisanje</span><span class="sxs-lookup"><span data-stu-id="e77d9-145">Full Invoicing</span></span>
- <span data-ttu-id="e77d9-146">Prepoznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="e77d9-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="e77d9-147">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="e77d9-147">Deployment steps</span></span>
<span data-ttu-id="e77d9-148">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e77d9-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e77d9-149">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](resource-sign-up-preview-subscription.md) i [Obezbeđivanje novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e77d9-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="e77d9-150">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="e77d9-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="e77d9-151">Planiranje projekta korišćenjem SAP</span><span class="sxs-lookup"><span data-stu-id="e77d9-151">Project planning using WBS</span></span>
- <span data-ttu-id="e77d9-152">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="e77d9-152">Resource Management</span></span>
- <span data-ttu-id="e77d9-153">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="e77d9-153">Time Tracking</span></span>
- <span data-ttu-id="e77d9-154">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="e77d9-154">Full Expense</span></span>
- <span data-ttu-id="e77d9-155">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="e77d9-155">Receipt OCR</span></span>
- <span data-ttu-id="e77d9-156">Potpuno fakturisanje</span><span class="sxs-lookup"><span data-stu-id="e77d9-156">Full Invoicing</span></span>
- <span data-ttu-id="e77d9-157">Prepoznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="e77d9-157">Revenue Recognition</span></span>
- <span data-ttu-id="e77d9-158">Nalozi za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="e77d9-158">Production Orders</span></span>
- <span data-ttu-id="e77d9-159">Podrška materijala</span><span class="sxs-lookup"><span data-stu-id="e77d9-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="e77d9-160">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="e77d9-160">Deployment steps</span></span>
<span data-ttu-id="e77d9-161">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="e77d9-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="e77d9-162">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Obezbeđivanje novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="e77d9-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

