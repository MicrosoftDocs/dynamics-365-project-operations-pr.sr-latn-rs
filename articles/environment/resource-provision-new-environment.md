---
title: Obezbeđenje novog okruženja
description: Ova tema pruža informacije o načinu obezbeđenja novog Project Operations okruženja.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083467"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="e0cf2-103">Obezbeđenje novog okruženja</span><span class="sxs-lookup"><span data-stu-id="e0cf2-103">Provision a new environment</span></span>

<span data-ttu-id="e0cf2-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="e0cf2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e0cf2-105">Ova tema pruža informacije o načinu obezbeđenja novog Dynamics 365 Project Operations okruženja za scenarije zasnovane na resursima / bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="e0cf2-106">Omogućavanje Project Operations automatskog obezbeđivanja u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="e0cf2-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="e0cf2-107">Koristite sledeće korake da omogućite Project Operations automatizovani tok obezbeđivanja za vaš LCS projekat.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="e0cf2-108">Idite na [LCS](https://lcs.dynamics.com/v2) i izaberite pločicu **Pregled upravljanja funkcijama**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="e0cf2-109">Na listi **Funkcija pregleda** izaberite **Project Operations Feature** i izaberite **Omogućena funkcija pregleda** kako bi se omogućila usluga Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="e0cf2-110">Ovaj korak se izvodi samo jednom po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="e0cf2-111">Obezbeđivanje Project Operations okruženja</span><span class="sxs-lookup"><span data-stu-id="e0cf2-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="e0cf2-112">Otvori novu primenu Dynamics 365 Finance [demo okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili [sandbox/proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="e0cf2-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="e0cf2-113">Prođite kroz čarobnjak **Obezbeđivanje okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="e0cf2-114">Uverite se da je izabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="e0cf2-115">Da biste obezbedili Project Operations, u delu **Napredna podešavanja** izaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="e0cf2-116">Omogućite **Common Data Service podešavanje** birajući **Da** , a zatim unesite podatke u obavezna polja:</span><span class="sxs-lookup"><span data-stu-id="e0cf2-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="e0cf2-117">+Ime</span><span class="sxs-lookup"><span data-stu-id="e0cf2-117">Name</span></span>
  - <span data-ttu-id="e0cf2-118">Region</span><span class="sxs-lookup"><span data-stu-id="e0cf2-118">Region</span></span>
  - <span data-ttu-id="e0cf2-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="e0cf2-119">Language</span></span>
  - <span data-ttu-id="e0cf2-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="e0cf2-120">Currency</span></span>
 
5. <span data-ttu-id="e0cf2-121">U polju **Common Data Service predložak** , izaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="e0cf2-122">Izaberite vrstu okruženja za vašu primenu.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="e0cf2-123">Probno vreme zasnovano na pretplati omogućiće vam da primenite CDS okruženje na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Podešavanja primene](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="e0cf2-125">Izaberite **Slažem se** da biste prihvatili uslove usluge, a zatim izaberite **Gotovo** da se vratite na podešavanja primene.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Saglasnost za primenu](./media/2DeploymentConsent.png)

7. <span data-ttu-id="e0cf2-127">Popunite preostala obavezna polja u čarobnjaku i potvrdite primenu.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="e0cf2-128">Vreme obezbeđivanja okruženja varira u zavisnosti od vrste okruženja.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="e0cf2-129">Obezbeđenje može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="e0cf2-130">Kada se primena uspešno završi, okruženje će se prikazati kao **Primenjeno**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="e0cf2-131">Da biste potvrdili da je okruženje uspešno postavljeno, izaberite **Prijavljivanje** i prijavite se u okruženje da biste potvrdili.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalji  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="e0cf2-133">Primena Project Operations Finance demo podataka (opcionalni korak)</span><span class="sxs-lookup"><span data-stu-id="e0cf2-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="e0cf2-134">Primenite Project Operations Finance demo podatke na 10.0.13 izdanje usluge u okruženju koje se hostuje u oblaku, kao što je opisano u [ovom članku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="e0cf2-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="e0cf2-135">Primenite ispravke na Finance okruženje</span><span class="sxs-lookup"><span data-stu-id="e0cf2-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="e0cf2-136">Project Operations zahteva Finance okruženje sa verzijom aplikacije **10.0.13 (10.0.569.20009)** ili novijom.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="e0cf2-137">Možda ćete morati da primenite ispravke kvaliteta u svom Finance okruženju da biste dobili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="e0cf2-138">U LCS-u, na stranici **Detalji okruženja** , u odeljku **Dostupne ispravke** izaberite **Prikaži ispravku**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ispravki](./media/5ViewUpdates.png)

2. <span data-ttu-id="e0cf2-140">Na stranici **Binarna ažuriranja** izaberite **Sačuvaj paket.**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-140">On the **Binary updates** page, select **Save package.**</span></span>

![Sačuvaj paket](./media/6SavePackage.png)

3. <span data-ttu-id="e0cf2-142">Kliknite na **Izaberi sve** , a zatim izaberite **Sačuvaj paket**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-142">Click **Select all** and then select **Save package**.</span></span>

![Pregledajte i sačuvajte ispravke](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="e0cf2-144">Unesite naziv i opis paketa, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="e0cf2-145">U zavisnosti od internet veze, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-145">Depending on the internet connection, this process might take some time.</span></span>

![Otpremite paket u biblioteku sredstava](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="e0cf2-147">Kada se paket sačuva, izaberite **Gotovo** i sačuvajte ovaj paket u biblioteci sredstava u vašem LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="e0cf2-148">Čuvanje i potvrđivanje paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="e0cf2-149">Da biste primenili ispravku, idite na stranicu **Detalji okruženja** u LCS-u i izaberite **Održavanje** > **Primeni ispravke**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="e0cf2-151">Na listi ispravki izaberite paket koji ste kreirali i izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primena ispravki](./media/10ApplyUpdates.png)

<span data-ttu-id="e0cf2-153">Servisiranje okruženja će potrajati neko vreme.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-153">Environment servicing will take some time.</span></span> <span data-ttu-id="e0cf2-154">Po završetku, okruženje će se vratiti u primenjeno stanje.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-154">After it is complete, the environment will return to a deployed state.</span></span>

![Primenjeno okruženje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="e0cf2-156">Uspostavite vezu sa dvostrukim upisivanjem</span><span class="sxs-lookup"><span data-stu-id="e0cf2-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="e0cf2-157">U svom LCS projektu idite na stranicu **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e0cf2-158">U odeljku **Common Data Service informacije o okruženju** , izaberite **Poveži sa uslugom CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="e0cf2-159">Kada se povezivanje završi, ponovo izaberite **Poveži sa uslugom CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="e0cf2-160">Bićete preusmereni na dvostruko upisivanje u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-160">You will be redirected to Dual Write in Finance.</span></span>

![Povezivanje sa uslugom CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="e0cf2-162">Izaberite **Primeni rešenje** za pristup entitetima koji će biti mapirani u integraciji.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primena rešenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="e0cf2-164">Izaberite oba rešenja, **Dynamics 365 Finance and Operations mapa entiteta za dvostruko upisivanje** i **Dynamics 365 Project Operations mape entiteta dvostrukog upisivanja** , a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Potvrda rešenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="e0cf2-166">Kada primenite rešenja, entiteti dvostrukog upisivanja se primenjuju na okruženje.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primena rešenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="e0cf2-168">Kada se entiteti primene, sva raspoloživa mapiranja se navode u okruženju.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape za dvostruko upisivanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="e0cf2-170">Osvežite entitete podataka nakon ispravke</span><span class="sxs-lookup"><span data-stu-id="e0cf2-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="e0cf2-171">U usluzi Finance idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor za upravljanje podacima](./media/16DataManagement.png)

2. <span data-ttu-id="e0cf2-173">Izaberite pločicu **Parametri radnog okvira**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-173">Select the **Framework parameters** tile.</span></span>

![Parametri radnog okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="e0cf2-175">Na stranici **Podešavanja entiteta** , izaberite **Osveži listu entiteta**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osveži listu entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="e0cf2-177">Osvežavanje će trajati približno 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="e0cf2-178">Dobićete upozorenje kada se završi.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvežavanja](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="e0cf2-180">Pokrenite Project Operations mape dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="e0cf2-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="e0cf2-181">U svom LCS projektu idite na stranicu **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="e0cf2-182">U odeljku **Common Data Service informacije o okruženju** , izaberite **Poveži sa uslugom CDS za aplikacije.**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="e0cf2-183">Kada izaberete vezu, bićete preusmereni na listu entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="e0cf2-184">Pokrenite mape kao što je opisano u sledećoj tabeli.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="e0cf2-185">Uverite se da sledite navedeni redosled.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="e0cf2-186">**Mapa entiteta**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-186">**Entity Map**</span></span> | <span data-ttu-id="e0cf2-187">**Osvežavanje entiteta**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-187">**Refresh entity**</span></span> | <span data-ttu-id="e0cf2-188">**Početna sinhronizacija**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-188">**Initial sync**</span></span> | <span data-ttu-id="e0cf2-189">**Master za početnu sinhronizaciju**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-189">**Master for initial sync**</span></span> | <span data-ttu-id="e0cf2-190">**Preduslovi za pokretanje**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-190">**Run prerequisites**</span></span> | <span data-ttu-id="e0cf2-191">**Početna sinhronizacija preduslova**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="e0cf2-192">**Uloge projektnih resursa za sva preduzeća (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="e0cf2-193">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-193">No</span></span> | <span data-ttu-id="e0cf2-194">Da</span><span class="sxs-lookup"><span data-stu-id="e0cf2-194">Yes</span></span> | <span data-ttu-id="e0cf2-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e0cf2-195">Common Data Service</span></span> | <span data-ttu-id="e0cf2-196">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-196">No</span></span> | <span data-ttu-id="e0cf2-197">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-197">N\A</span></span> |
| <span data-ttu-id="e0cf2-198">**Pravna lica (cdm\_preduzeća)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="e0cf2-199">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-199">No</span></span> | <span data-ttu-id="e0cf2-200">Da</span><span class="sxs-lookup"><span data-stu-id="e0cf2-200">Yes</span></span> | <span data-ttu-id="e0cf2-201">Finance and Operations aplikacije</span><span class="sxs-lookup"><span data-stu-id="e0cf2-201">Finance and Operations apps</span></span> | <span data-ttu-id="e0cf2-202">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-202">No</span></span> | <span data-ttu-id="e0cf2-203">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-203">N\A</span></span> |
| <span data-ttu-id="e0cf2-204">**Project Operations stvarne vrednosti integracije (msdyn\_stvarne vrednosti)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="e0cf2-205">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-205">No</span></span> | <span data-ttu-id="e0cf2-206">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-206">No</span></span> | <span data-ttu-id="e0cf2-207">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-207">N\A</span></span> | <span data-ttu-id="e0cf2-208">Da</span><span class="sxs-lookup"><span data-stu-id="e0cf2-208">Yes</span></span> | <span data-ttu-id="e0cf2-209">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-209">No</span></span> |
| <span data-ttu-id="e0cf2-210">**Predmeti ugovora projekta (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="e0cf2-211">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-211">No</span></span> | <span data-ttu-id="e0cf2-212">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-212">No</span></span> | <span data-ttu-id="e0cf2-213">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-213">N\A</span></span> | <span data-ttu-id="e0cf2-214">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-214">No</span></span> | <span data-ttu-id="e0cf2-215">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-215">No</span></span> |
| <span data-ttu-id="e0cf2-216">**Entitet integracije za odnose transakcija projekta (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="e0cf2-217">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-217">No</span></span> | <span data-ttu-id="e0cf2-218">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-218">No</span></span> | <span data-ttu-id="e0cf2-219">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-219">N\A</span></span> | <span data-ttu-id="e0cf2-220">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-220">No</span></span> | <span data-ttu-id="e0cf2-221">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-221">N\A</span></span> |
| <span data-ttu-id="e0cf2-222">**Project Operations kontrolne tačke predmeta ugovora o integraciji (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="e0cf2-223">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-223">No</span></span> | <span data-ttu-id="e0cf2-224">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-224">No</span></span> | <span data-ttu-id="e0cf2-225">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-225">N\A</span></span> | <span data-ttu-id="e0cf2-226">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-226">No</span></span> | <span data-ttu-id="e0cf2-227">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-227">N\A</span></span> |
| <span data-ttu-id="e0cf2-228">**Project Operations entitet integracije za procene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="e0cf2-229">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-229">No</span></span> | <span data-ttu-id="e0cf2-230">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-230">No</span></span> | <span data-ttu-id="e0cf2-231">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-231">N\A</span></span> | <span data-ttu-id="e0cf2-232">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-232">No</span></span> | <span data-ttu-id="e0cf2-233">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-233">N\A</span></span> |
| <span data-ttu-id="e0cf2-234">**Project Operations entitet izvoza kategorija troškova projekta (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="e0cf2-235">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-235">No</span></span> | <span data-ttu-id="e0cf2-236">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-236">No</span></span> | <span data-ttu-id="e0cf2-237">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-237">N\A</span></span> | <span data-ttu-id="e0cf2-238">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-238">No</span></span> | <span data-ttu-id="e0cf2-239">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-239">N\A</span></span> |
| <span data-ttu-id="e0cf2-240">**Project Operations entitet izvoza troškova integracije projekta (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="e0cf2-241">Da</span><span class="sxs-lookup"><span data-stu-id="e0cf2-241">Yes</span></span> | <span data-ttu-id="e0cf2-242">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-242">No</span></span> | <span data-ttu-id="e0cf2-243">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-243">N\A</span></span> | <span data-ttu-id="e0cf2-244">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-244">No</span></span> | <span data-ttu-id="e0cf2-245">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-245">N\A</span></span> |
| <span data-ttu-id="e0cf2-246">**Project Operations entitet integracije za procene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="e0cf2-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="e0cf2-247">Da</span><span class="sxs-lookup"><span data-stu-id="e0cf2-247">Yes</span></span> | <span data-ttu-id="e0cf2-248">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-248">No</span></span> | <span data-ttu-id="e0cf2-249">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-249">N\A</span></span> | <span data-ttu-id="e0cf2-250">No</span><span class="sxs-lookup"><span data-stu-id="e0cf2-250">No</span></span> | <span data-ttu-id="e0cf2-251">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="e0cf2-251">N\A</span></span> |


4. <span data-ttu-id="e0cf2-252">Da biste osvežili entitet, izaberite naziv mape, a zatim izaberite **Osveži entitete**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvežavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="e0cf2-254">Kada se osvežavanje završi, pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="e0cf2-255">Pre nego što omogućite sledeću mapu, proverite da li je mapa u tabeli u stanju **Pokrenuta**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="e0cf2-256">Pokretanje mapa sa većim brojem preduslova može potrajati.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="e0cf2-257">Da biste pokrenuli mapu sa preduslovima, omogućite preklopno dugme **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="e0cf2-258">Ako tabela pokazuje da **Početna sinhronizacija preduslova** ima vrednost **Ne** , proverite da li je zastavica **Početna sinhronizacija** **isključena** u svim mapama preduslova pre nego što je pokrenete.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="e0cf2-260">Potvrdite da su sve mape povezane sa projektom u aktivnom stanju.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-260">Validate all project related maps are in the running state.</span></span>

![Sve mape su pokrenute](./media/22AllMapsRunning.png)

<span data-ttu-id="e0cf2-262">Vaše Project Operations okruženje je sada obezbeđeno i konfigurisano.</span><span class="sxs-lookup"><span data-stu-id="e0cf2-262">Your Project Operations environment is now provisioned and configured.</span></span>
