---
title: Tipovi primene
description: Ova tema pruža informacije koje vam pomažu da utvrdite pravilan tip primene usluge Project Operations za vaše preduzeće.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949048"
---
# <a name="deployment-types"></a><span data-ttu-id="6e940-103">Tipovi primene</span><span class="sxs-lookup"><span data-stu-id="6e940-103">Deployment types</span></span>

<span data-ttu-id="6e940-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="6e940-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e940-105">Nakon kupovine licence, počnite ovde da biste utvrdili najbolji model primene usluge Dynamics 365 Project Operations pomoću [vođenog toka instalacije](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e940-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="6e940-106">Kada dovršite vođeni tok instalacije, bićete preusmereni na pravi portal za upravljanje da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="6e940-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="6e940-107">Pogledajte detalje o primeni u nastavku da biste dovršili instalaciju.</span><span class="sxs-lookup"><span data-stu-id="6e940-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="6e940-108">Postojeći klijenti sistema Dynamics koji koriste Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="6e940-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="6e940-109">Project Operations uključuje mogućnosti koje su isporučene sa uslugom Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="6e940-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="6e940-110">Putanja nadogradnje biće izdata za ove klijente u budućnosti.</span><span class="sxs-lookup"><span data-stu-id="6e940-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="6e940-111">Postojeći klijenti usluge Dynamics 365 Finance koji koriste upravljanje projektima i računovodstvo</span><span class="sxs-lookup"><span data-stu-id="6e940-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="6e940-112">Postojeći klijenti usluge Finance koji koriste funkcionalnost upravljanja projektima i računovodstva mogu da nastave da koriste ovo kako jeste.</span><span class="sxs-lookup"><span data-stu-id="6e940-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="6e940-113">Pogledajte [Project Operations za scenarije zasnovane na zalihama/proizvodnji](#pma).</span><span class="sxs-lookup"><span data-stu-id="6e940-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="6e940-114">Project Operations podržava više mogućnosti primene u skladu sa vašim zahtevima.</span><span class="sxs-lookup"><span data-stu-id="6e940-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="6e940-115">Bez obzira na to da li ste novi ili postojeći klijent sistema Dynamics 365, Project Operations može podržati vaše potrebe.</span><span class="sxs-lookup"><span data-stu-id="6e940-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="6e940-116">Naš [upitnik za primenu](https://aka.ms/provisionprojectoperations) će vam pomoći da odredite odgovarajuću primenu.</span><span class="sxs-lookup"><span data-stu-id="6e940-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="6e940-117">Rezultati će vas voditi prema jednom od sledećih tipova primene:</span><span class="sxs-lookup"><span data-stu-id="6e940-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="6e940-118">Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="6e940-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="6e940-119">Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="6e940-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="6e940-120">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="6e940-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="6e940-121">Project Operations podržavaju scenarije zaliha / proizvodnih naloga i scenarije zasnovane na resursima / bez zaliha u istom okruženju putem konfiguracija na nivou pravnog lica.</span><span class="sxs-lookup"><span data-stu-id="6e940-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="6e940-122">Na primer, Contoso može iskoristiti mogućnosti zaliha / naloga za proizvodnju u njihovom proizvodnom pogonu u SAD (pravno lice = Contoso Manufacturing United States) i mogućnosti zasnovane na resursima / bez zaliha u njihovom Contoso servisu za robotske ruke u Velikoj Britaniji (pravno lice = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="6e940-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="6e940-123"><a name="lite"><a/>Jednostavna primena – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="6e940-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="6e940-124">Jednostavna primena uključuje sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="6e940-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="6e940-125">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="6e940-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6e940-126">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="6e940-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6e940-127">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="6e940-127">Unified Resource Management</span></span>
- <span data-ttu-id="6e940-128">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="6e940-128">Time Tracking</span></span>
- <span data-ttu-id="6e940-129">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="6e940-129">Basic Expense</span></span>
- <span data-ttu-id="6e940-130">Predlog fakture</span><span class="sxs-lookup"><span data-stu-id="6e940-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e940-131">Koraci primene:</span><span class="sxs-lookup"><span data-stu-id="6e940-131">Deployment steps:</span></span>
<span data-ttu-id="6e940-132">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e940-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e940-133">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](lite-preview-subscription-sign-up.md) i [Obezbeđivanje novog okruženja](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="6e940-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="6e940-134"><a name="integrated"><a/>Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama</span><span class="sxs-lookup"><span data-stu-id="6e940-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="6e940-135">Project Operations za scenarije resursa / bez zaliha uključuju sledeće mogućnosti:</span><span class="sxs-lookup"><span data-stu-id="6e940-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="6e940-136">Planiranje projekata koristeći Microsoft Project za veb</span><span class="sxs-lookup"><span data-stu-id="6e940-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="6e940-137">Višedimenzionalno određivanje cena</span><span class="sxs-lookup"><span data-stu-id="6e940-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="6e940-138">Objedinjeno upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="6e940-138">Unified Resource Management</span></span>
- <span data-ttu-id="6e940-139">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="6e940-139">Time Tracking</span></span>
- <span data-ttu-id="6e940-140">Osnovni trošak</span><span class="sxs-lookup"><span data-stu-id="6e940-140">Basic Expense</span></span>
- <span data-ttu-id="6e940-141">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="6e940-141">Full Expense</span></span>
- <span data-ttu-id="6e940-142">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="6e940-142">Receipt OCR</span></span>
- <span data-ttu-id="6e940-143">Potpuno fakturisanje</span><span class="sxs-lookup"><span data-stu-id="6e940-143">Full Invoicing</span></span>
- <span data-ttu-id="6e940-144">Prepoznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="6e940-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e940-145">Koraci primene:</span><span class="sxs-lookup"><span data-stu-id="6e940-145">Deployment steps:</span></span>
<span data-ttu-id="6e940-146">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e940-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e940-147">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](resource-sign-up-preview-subscription.md) i [Obezbeđivanje novog okruženja](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="6e940-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="6e940-148">Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="6e940-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="6e940-149">Planiranje projekta korišćenjem SAP</span><span class="sxs-lookup"><span data-stu-id="6e940-149">Project planning using WBS</span></span>
- <span data-ttu-id="6e940-150">Upravljanje resursima</span><span class="sxs-lookup"><span data-stu-id="6e940-150">Resource Management</span></span>
- <span data-ttu-id="6e940-151">Praćenje vremena</span><span class="sxs-lookup"><span data-stu-id="6e940-151">Time Tracking</span></span>
- <span data-ttu-id="6e940-152">Puni trošak</span><span class="sxs-lookup"><span data-stu-id="6e940-152">Full Expense</span></span>
- <span data-ttu-id="6e940-153">OCR priznanice</span><span class="sxs-lookup"><span data-stu-id="6e940-153">Receipt OCR</span></span>
- <span data-ttu-id="6e940-154">Potpuno fakturisanje</span><span class="sxs-lookup"><span data-stu-id="6e940-154">Full Invoicing</span></span>
- <span data-ttu-id="6e940-155">Prepoznavanje prihoda</span><span class="sxs-lookup"><span data-stu-id="6e940-155">Revenue Recognition</span></span>
- <span data-ttu-id="6e940-156">Nalozi za proizvodnju</span><span class="sxs-lookup"><span data-stu-id="6e940-156">Production Orders</span></span>
- <span data-ttu-id="6e940-157">Podrška materijala</span><span class="sxs-lookup"><span data-stu-id="6e940-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="6e940-158">Koraci primene:</span><span class="sxs-lookup"><span data-stu-id="6e940-158">Deployment steps:</span></span>
<span data-ttu-id="6e940-159">Odredite najbolji model primene usluge Project Operations pomoću [upitnika za primenu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="6e940-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="6e940-160">Za ovo raspoređivanje, pogledajte članak [Prijava za pretplate na pregled](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) i [Obezbeđivanje novog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6e940-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



