---
title: Odredite vrstu primene
description: Ova tema pruža informacije koje vam pomažu da utvrdite pravilan tip primene usluge Project Operations za vaše preduzeće.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401235"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="674c5-103">Odredite vrstu primene</span><span class="sxs-lookup"><span data-stu-id="674c5-103">Determine your deployment type</span></span>

<span data-ttu-id="674c5-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="674c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="674c5-105">Nakon kupovine licence, počnite ovde da biste utvrdili najbolji model primene usluge Dynamics 365 Project Operations pomoću [vođenog toka instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="674c5-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="674c5-106">Kada dovršite vođeni tok instalacije, bićete preusmereni na pravi portal za upravljanje da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="674c5-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="674c5-107">Pogledajte detalje o primeni da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="674c5-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="674c5-108">Postojeći klijenti sistema Dynamics koji koriste Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="674c5-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="674c5-109">Project Operations uključuje mogućnosti koje su isporučene sa uslugom Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="674c5-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="674c5-110">Putanja nadogradnje će biti objavljena za ove klijente u 1. talasu izdanja za 2021. godinu.</span><span class="sxs-lookup"><span data-stu-id="674c5-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="674c5-111">Postojeći klijenti usluge Dynamics 365 Finance koji koriste upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="674c5-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="674c5-112">Postojeći klijenti usluge Finance koji koriste funkcionalnost upravljanja projektima i računovodstva mogu da nastave da je koriste onakvu kakva jeste.</span><span class="sxs-lookup"><span data-stu-id="674c5-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="674c5-113">Pogledajte [Project Operations za scenarije zasnovane na zalihama/proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="674c5-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="674c5-114">Tipovi primene</span><span class="sxs-lookup"><span data-stu-id="674c5-114">Deployment types</span></span>
<span data-ttu-id="674c5-115">Project Operations podržava više mogućnosti primene u skladu sa vašim zahtevima.</span><span class="sxs-lookup"><span data-stu-id="674c5-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="674c5-116">Bez obzira na to da li ste novi ili postojeći klijent sistema Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="674c5-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="674c5-117">Naš [upitnik za primenu](https://aka.ms/provisionprojectoperations) će vam pomoći da odredite odgovarajuću primenu.</span><span class="sxs-lookup"><span data-stu-id="674c5-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="674c5-118">Rezultati će vas voditi prema jednom od sledećih tipova primene:</span><span class="sxs-lookup"><span data-stu-id="674c5-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="674c5-119">Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="674c5-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="674c5-120">Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="674c5-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="674c5-121">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="674c5-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="674c5-122">Project Operations podržavaju scenarije zaliha / proizvodnih naloga i scenarije zasnovane na resursima / bez zaliha u istom okruženju putem konfiguracija na nivou pravnog lica.</span><span class="sxs-lookup"><span data-stu-id="674c5-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="674c5-123">Na primer, Contoso može da koristi mogućnosti skladištenja/naručivanja u svom proizvodnom pogonu u SAD (pravno lice = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="674c5-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="674c5-124">Contoso može da koristi mogućnosti koji nisu zasnovane na zalihama/zasnovane na resursima u objektu Contoso Robotics Arms u Velikoj Britaniji (pravno lice = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="674c5-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="674c5-125">Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="674c5-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="674c5-126">Jednostavna primena uključuje sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="674c5-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="674c5-127">Proces prodaje za projekte koji proširuju iskustva aplikacije Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="674c5-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="674c5-128">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="674c5-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="674c5-129">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="674c5-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="674c5-130">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="674c5-130">Unified resource management</span></span>
- <span data-ttu-id="674c5-131">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="674c5-131">Time tracking</span></span>
- <span data-ttu-id="674c5-132">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="674c5-132">Basic expense</span></span>
- <span data-ttu-id="674c5-133">Izdavanje predračuna i faktura u okruženju klijenta</span><span class="sxs-lookup"><span data-stu-id="674c5-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="674c5-134">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="674c5-134">Deployment steps</span></span>
<span data-ttu-id="674c5-135">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="674c5-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="674c5-136">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](lite-preview-subscription-sign-up.md) i [Obezbeđivanje novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="674c5-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="674c5-137">Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="674c5-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="674c5-138">Project Operations za scenarije resursa / bez zaliha uključuju sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="674c5-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="674c5-139">Proces prodaje za projekte koji proširuju aplikaciju Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="674c5-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="674c5-140">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="674c5-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="674c5-141">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="674c5-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="674c5-142">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="674c5-142">Unified resource management</span></span>
- <span data-ttu-id="674c5-143">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="674c5-143">Time tracking</span></span>
- <span data-ttu-id="674c5-144">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="674c5-144">Basic expense</span></span>
- <span data-ttu-id="674c5-145">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="674c5-145">Full expense</span></span>
- <span data-ttu-id="674c5-146">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="674c5-146">Receipt OCR</span></span>
- <span data-ttu-id="674c5-147">Izdavanje predračuna i faktura u okruženju klijenta</span><span class="sxs-lookup"><span data-stu-id="674c5-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="674c5-148">Priznavanje prihoda za projekte</span><span class="sxs-lookup"><span data-stu-id="674c5-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="674c5-149">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="674c5-149">Deployment steps</span></span>
<span data-ttu-id="674c5-150">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="674c5-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="674c5-151">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](resource-sign-up-preview-subscription.md) i [Obezbeđivanje novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="674c5-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="674c5-152">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="674c5-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="674c5-153">Planiranje projekta korišćenjem SAP</span><span class="sxs-lookup"><span data-stu-id="674c5-153">Project planning using WBS</span></span>
- <span data-ttu-id="674c5-154">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="674c5-154">Resource Management</span></span>
- <span data-ttu-id="674c5-155">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="674c5-155">Time Tracking</span></span>
- <span data-ttu-id="674c5-156">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="674c5-156">Full Expense</span></span>
- <span data-ttu-id="674c5-157">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="674c5-157">Receipt OCR</span></span>
- <span data-ttu-id="674c5-158">Potpuno fakturisanje</span><span class="sxs-lookup"><span data-stu-id="674c5-158">Full Invoicing</span></span>
- <span data-ttu-id="674c5-159">Prepoznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="674c5-159">Revenue Recognition</span></span>
- <span data-ttu-id="674c5-160">Nalozi za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="674c5-160">Production Orders</span></span>
- <span data-ttu-id="674c5-161">Podrška materijala</span><span class="sxs-lookup"><span data-stu-id="674c5-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="674c5-162">Koraci primene</span><span class="sxs-lookup"><span data-stu-id="674c5-162">Deployment steps</span></span>
<span data-ttu-id="674c5-163">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="674c5-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="674c5-164">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Obezbeđivanje novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="674c5-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

