---
title: Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha
description: Ova tema pruža informacije o načinu pretplate i primene usluge Project Operations za scenarije zasnovane na resursima / bez zaliha.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334844"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="63883-103">Prijavljivanje za pretplate na verziju za pregled usluge Project Operations za scenarije resursa / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="63883-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="63883-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="63883-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="63883-105">Ova tema objašnjava kako da se pretplatite na ponudu probne verzije i primeniti Project Operations okruženje za scenarije zasnovane na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="63883-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63883-106">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="63883-106">Prerequisites</span></span>
- <span data-ttu-id="63883-107">Korisnik koji primeni verziju za pregled mora da ima globalna administratorska prava u Azure zakupcu.</span><span class="sxs-lookup"><span data-stu-id="63883-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="63883-108">Zakupca možete kreirati tokom prvog iskorišćavanja ponude.</span><span class="sxs-lookup"><span data-stu-id="63883-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="63883-109">Za primenu Finance okruženja potrebna je važeća Azure pretplata koja će se naplaćivati po okruženju.</span><span class="sxs-lookup"><span data-stu-id="63883-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="63883-110">Možete da koristite postojeću pretplatu u svojim organizacijama ili da koristite [Azure probnu verziju](https://azure.microsoft.com/en-us/free/) da biste započeli.</span><span class="sxs-lookup"><span data-stu-id="63883-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="63883-111">CDS okruženje će biti besplatno za ograničen period od 30 dana.</span><span class="sxs-lookup"><span data-stu-id="63883-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63883-112">Samo jedna osoba, administrator zakupca, u organizaciji treba da izvršava ovaj zadatak.</span><span class="sxs-lookup"><span data-stu-id="63883-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="63883-113">Ako niste pretplatnik na ovo izdanje, sačekajte dok se vaša organizacija ne registruje i ne primite svoje korisničke akreditive.</span><span class="sxs-lookup"><span data-stu-id="63883-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="63883-114">Probne verzije se koriste jednokratno u zakupcu.</span><span class="sxs-lookup"><span data-stu-id="63883-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="63883-115">Probnu verziju možete pokrenuti samo jednom.</span><span class="sxs-lookup"><span data-stu-id="63883-115">You can only run a trial one time.</span></span> <span data-ttu-id="63883-116">Preporučujemo vam da kreirate novog zakupca u svrhu probne verzije.</span><span class="sxs-lookup"><span data-stu-id="63883-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="63883-117">Dynamics 365 Project Operations (CE) – Probna verzija za pregled</span><span class="sxs-lookup"><span data-stu-id="63883-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="63883-118">Pre nego što započnete, uverite se da ste prijavljeni u pregledač sa korisničkim poslovnim nalogom u zakupcu gde želite pregled usluge Project Operations.</span><span class="sxs-lookup"><span data-stu-id="63883-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="63883-119">Iskoristite prvu šifru ponude, **Dynamics 365 Project Operations** ovde [Project Operations probna verzija](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="63883-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="63883-120">Potvrdite porudžbinu.</span><span class="sxs-lookup"><span data-stu-id="63883-120">Confirm your order.</span></span>

  <span data-ttu-id="63883-121">Videćete da je ponuda za potvrdu uspešno iskorišćena.</span><span class="sxs-lookup"><span data-stu-id="63883-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="63883-122">Dynamics 365 Finance probna verzija za pregled</span><span class="sxs-lookup"><span data-stu-id="63883-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="63883-123">Idite na [probnu verziju za pregled usluge Dynamics 365 for Finance](https://aka.ms/trypoche) i ponovite korake iz prethodnog odeljka sa ponudom, Prijavite se za okruženje koje se hostuje u oblaku.</span><span class="sxs-lookup"><span data-stu-id="63883-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="63883-124">Dodeljivanje licenci</span><span class="sxs-lookup"><span data-stu-id="63883-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63883-125">Trebaće vam administrativni pristup Microsoft 365 portalu vaše organizacije da biste izvršili sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="63883-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="63883-126">Idite u [Microsoft 365 centar administracije](https://portal.office.com/) da dodelite licence svojim korisnicima.</span><span class="sxs-lookup"><span data-stu-id="63883-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="63883-127">Na stranici **Aktivni korisnici**, izaberite korisnike kojima želite da dodelite licencu.</span><span class="sxs-lookup"><span data-stu-id="63883-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="63883-128">Proverite da li je izabrana licenca **Dynamics 365 Project Operations**, pa izaberite **Sačuvaj promene**.</span><span class="sxs-lookup"><span data-stu-id="63883-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="63883-129">Ponudu za probnu verziju usluge Finance ne treba dodeliti korisniku.</span><span class="sxs-lookup"><span data-stu-id="63883-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="63883-130">Započnite novi projekat u LCS</span><span class="sxs-lookup"><span data-stu-id="63883-130">Start a new project in LCS</span></span>

<span data-ttu-id="63883-131">Napravite novi LCS projekat kako je opisano u temi [Započnite novi projekat u LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="63883-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="63883-132">Dodajte Azure pretplatu u LCS projekat</span><span class="sxs-lookup"><span data-stu-id="63883-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="63883-133">Da biste dovršili ovaj zadatak, sledite korake u temi [Dodavanje Azure pretplate u LCS projekat](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="63883-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="63883-134">Primenite Finance demo okruženje sa uslugom Project Operations za scenarije resursa / bez zaliha</span><span class="sxs-lookup"><span data-stu-id="63883-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="63883-135">Sledite smernice u temi [Obezbeđenje novog okruženja](resource-provision-new-environment.md) da biste završili primenu.</span><span class="sxs-lookup"><span data-stu-id="63883-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="63883-136">Koristite tip primene [demo okruženje](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) za pregled.</span><span class="sxs-lookup"><span data-stu-id="63883-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="63883-137">Instalirajte podatke o podešavanju i konfiguraciji CDS</span><span class="sxs-lookup"><span data-stu-id="63883-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="63883-138">Instalirajte podatke o podešavanju i konfiguraciji CDS kako je opisano u temi [Podesite i primenite podatke o konfiguraciji u usluzi Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="63883-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="63883-139">Dovršite ovaj korak tek nakon što se primeni demo okruženje usluge Finance i demo podaci budu spremni.</span><span class="sxs-lookup"><span data-stu-id="63883-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
