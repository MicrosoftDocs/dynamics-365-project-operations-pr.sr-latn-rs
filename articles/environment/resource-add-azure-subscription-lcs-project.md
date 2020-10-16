---
title: Dodajte Azure pretplatu u LCS projekat
description: Ova tema pruža informacije o tome kako da povežete svoju Azure pretplatu sa LCS projektom.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0b5703542ac58adcc710890d9676dd0090a82f25
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949051"
---
# <a name="add-an-azure-subscription-to-lcs-project"></a><span data-ttu-id="a35e8-103">Dodajte Azure pretplatu u LCS projekat</span><span class="sxs-lookup"><span data-stu-id="a35e8-103">Add an Azure subscription to LCS project</span></span>

<span data-ttu-id="a35e8-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="a35e8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a35e8-105">Okruženja u hostu u oblaku moraju se primeniti pomoću postojeće Azure pretplate.</span><span class="sxs-lookup"><span data-stu-id="a35e8-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="a35e8-106">Ova tema objašnjava kako da povežete svoju postojeću Azure pretplatu sa LCS projektom.</span><span class="sxs-lookup"><span data-stu-id="a35e8-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="a35e8-107">Dajte pristanak administratora</span><span class="sxs-lookup"><span data-stu-id="a35e8-107">Grant admin consent</span></span>

1. <span data-ttu-id="a35e8-108">U vašem LCS projektu, u odeljku **Okruženja**, izaberite **Microsoft Azure podešavanja**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Podešavanja za Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="a35e8-110">Na stranici **Podešavanja projekta**, na kartici **Azure konektori**, izaberite **Odobri**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="a35e8-111">To omogućava da se okruženja primene na ovaj projekat.</span><span class="sxs-lookup"><span data-stu-id="a35e8-111">This allows environments to be deployed to this project.</span></span>

![Azure konektori](./media/2AzureConnectors.png)

3. <span data-ttu-id="a35e8-113">Ponovo izaberite **Odobri** da biste pružili pristanak administratora.</span><span class="sxs-lookup"><span data-stu-id="a35e8-113">Select **Authorize** again to provide admin consent.</span></span>

![Dajte pristanak administratora](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="a35e8-115">Prihvatite zahtev za dozvole.</span><span class="sxs-lookup"><span data-stu-id="a35e8-115">Accept the permissions request.</span></span>

![Prihvatite zahtev za dozvole](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="a35e8-117">Ovlašćenje je sada završeno.</span><span class="sxs-lookup"><span data-stu-id="a35e8-117">The authorization is now complete.</span></span> 

![Odobrenje je uspešno](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="a35e8-119">Omogućite pristup usluge Dynamics Deployment Services vašoj Azure pretplati</span><span class="sxs-lookup"><span data-stu-id="a35e8-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="a35e8-120">Idite na [Microsoft Azure obračun](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i izaberite svoju pretplatu.</span><span class="sxs-lookup"><span data-stu-id="a35e8-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="a35e8-121">Usluga Dynamics Deployment Services treba da pristupi ovoj pretplati da bi mogla da primeni okruženja.</span><span class="sxs-lookup"><span data-stu-id="a35e8-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Detalji pretplate na uslugu Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="a35e8-123">Izaberite **Kontrola pristupa (IAM)** u oknu za navigaciju, a zatim izaberite **Dodajte dodeljivanje uloga**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="a35e8-124">U klizaču sa desne strane izaberite **Uloga saradnika** i na priloženoj listi pronađite i izaberite **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="a35e8-125">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-125">Select **Save**.</span></span>

![Pristup pretplati](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="a35e8-127">Dodavanje konektora za pretplatu u LCS projekat</span><span class="sxs-lookup"><span data-stu-id="a35e8-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="a35e8-128">U vašem LCS projektu, na stranici **Microsoft Azure podešavanja** izaberite **Dodaj** da biste dodali novi konektor.</span><span class="sxs-lookup"><span data-stu-id="a35e8-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="a35e8-129">Unesite svoj ID Azure pretplate.</span><span class="sxs-lookup"><span data-stu-id="a35e8-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="a35e8-130">ID Azure pretplate možete pronaći u [Azure portalu](https://ms.portal.azure.com/), u odeljku  **Podešavanja**  u donjem levom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="a35e8-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="a35e8-131">U polju **Konfiguriši da se koristi Azure Resource Manager**, izaberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="a35e8-132">Uverite se da se Azure domen zakupca AAD pretplate podudara sa Azure pretplatom u vlasništvu domena koju koristite, pa izaberite **Sledeći**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="a35e8-133">Na ekranu **Microsoft Azure podešavanje**, izaberite **Sledeći** za potvrdu.</span><span class="sxs-lookup"><span data-stu-id="a35e8-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="a35e8-134">Ako na ovom ekranu dobijete grešku, vratite se u odeljak [Omogućite pristup usluzi Dynamics Deployment Services u Azure pretplatu](#provide) u ovoj temi i uverite se da ste završili sve korake.</span><span class="sxs-lookup"><span data-stu-id="a35e8-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="a35e8-135">Preuzmite Azure certifikat za upravljanje u lokalnu fasciklu na računaru, a zatim ga otpremite na portal za upravljanje uslugom Azure tako što ćete otići na **Podešavanja** > **Sertifikati o upravljanju**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="a35e8-136">Ovaj certifikat će omogućiti LCS da komunicira sa platformom Azure u vaše ime.</span><span class="sxs-lookup"><span data-stu-id="a35e8-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="a35e8-137">Ovaj korak možete preskočiti ako vaš korisnik ima pristup pretplati.</span><span class="sxs-lookup"><span data-stu-id="a35e8-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="a35e8-138">Izaberite **Sledeće**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-138">Select  **Next**.</span></span>
8. <span data-ttu-id="a35e8-139">Izaberite Azure region za primenu i izaberite centar podataka koji je blizu mesta gde planirate da koristite ovaj sistem.</span><span class="sxs-lookup"><span data-stu-id="a35e8-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="a35e8-140">Izaberite **Poveži se**.</span><span class="sxs-lookup"><span data-stu-id="a35e8-140">Select  **Connect**.</span></span>

<span data-ttu-id="a35e8-141">Uspešno ste povezali svoju Azure pretplatu.</span><span class="sxs-lookup"><span data-stu-id="a35e8-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="a35e8-142">Sada možete da primenite Dynamics 365 Finance okruženja hostovana u oblaku.</span><span class="sxs-lookup"><span data-stu-id="a35e8-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>


