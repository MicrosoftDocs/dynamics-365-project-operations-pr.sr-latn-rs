---
title: Obezbeđenje novog okruženja
description: Ova tema pruža informacije o načinu obezbeđenja novog Project Operations okruženja.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727807"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="d6b75-103">Obezbeđenje novog okruženja</span><span class="sxs-lookup"><span data-stu-id="d6b75-103">Provision a new environment</span></span>

<span data-ttu-id="d6b75-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="d6b75-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d6b75-105">Ova tema pruža informacije o načinu da obezbedite novo Dynamics 365 Project Operations okruženje za scenarije zasnovane na resursima/bez zaliha.</span><span class="sxs-lookup"><span data-stu-id="d6b75-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="d6b75-106">Omogućavanje Project Operations automatskog obezbeđivanja u LCS projektu</span><span class="sxs-lookup"><span data-stu-id="d6b75-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="d6b75-107">Koristite sledeće korake da omogućite Project Operations automatizovani tok obezbeđivanja za vaš LCS projekat.</span><span class="sxs-lookup"><span data-stu-id="d6b75-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="d6b75-108">Idite na [LCS](https://lcs.dynamics.com/v2) i izaberite pločicu **Pregled upravljanja funkcijama**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="d6b75-109">Na listi **Funkcija pregleda** izaberite **Project Operations Feature** i izaberite **Omogućena funkcija pregleda** kako bi se omogućila usluga Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d6b75-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="d6b75-110">Ovaj korak se izvodi samo jednom po LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="d6b75-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="d6b75-111">Obezbeđivanje Project Operations okruženja</span><span class="sxs-lookup"><span data-stu-id="d6b75-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="d6b75-112">Otvori novu primenu Dynamics 365 Finance [demo okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) ili [sandbox/proizvodnog okruženja](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="d6b75-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="d6b75-113">Prođite kroz čarobnjak **Obezbeđivanje okruženja**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="d6b75-114">Uverite se da je izabrana verzija aplikacije 10.0.13 ili novija.</span><span class="sxs-lookup"><span data-stu-id="d6b75-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="d6b75-115">Da biste obezbedili Project Operations, u delu **Napredna podešavanja** izaberite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="d6b75-116">Omogućite **Common Data Service podešavanje** birajući **Da**, a zatim unesite podatke u obavezna polja:</span><span class="sxs-lookup"><span data-stu-id="d6b75-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="d6b75-117">+Ime</span><span class="sxs-lookup"><span data-stu-id="d6b75-117">Name</span></span>
  - <span data-ttu-id="d6b75-118">Region</span><span class="sxs-lookup"><span data-stu-id="d6b75-118">Region</span></span>
  - <span data-ttu-id="d6b75-119">Jezik</span><span class="sxs-lookup"><span data-stu-id="d6b75-119">Language</span></span>
  - <span data-ttu-id="d6b75-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="d6b75-120">Currency</span></span>
 
5. <span data-ttu-id="d6b75-121">U polju **Common Data Service predložak**, izaberite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="d6b75-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="d6b75-122">Izaberite vrstu okruženja za vašu primenu.</span><span class="sxs-lookup"><span data-stu-id="d6b75-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="d6b75-123">Probno vreme zasnovano na pretplati omogućiće vam da primenite CDS okruženje na 30 dana.</span><span class="sxs-lookup"><span data-stu-id="d6b75-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Podešavanja primene](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="d6b75-125">Izaberite **Slažem se** da biste prihvatili uslove usluge, a zatim izaberite **Gotovo** da se vratite na podešavanja primene.</span><span class="sxs-lookup"><span data-stu-id="d6b75-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Saglasnost za primenu](./media/2DeploymentConsent.png)

7. <span data-ttu-id="d6b75-127">Opcionalno – primenite demo podatke na okruženje.</span><span class="sxs-lookup"><span data-stu-id="d6b75-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="d6b75-128">Idite na **Napredna podešavanja**, izaberite **Prilagodi konfiguraciju SQL baze podataka** i podesite **Navedite skup podataka za bazu podataka aplikacije** na **Demo**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="d6b75-129">Popunite preostala obavezna polja u čarobnjaku i potvrdite primenu.</span><span class="sxs-lookup"><span data-stu-id="d6b75-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="d6b75-130">Vreme za pripremu okruženja varira u zavisnosti od vrste okruženja.</span><span class="sxs-lookup"><span data-stu-id="d6b75-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="d6b75-131">Obezbeđenje može potrajati do šest sati.</span><span class="sxs-lookup"><span data-stu-id="d6b75-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="d6b75-132">Kada se primena uspešno završi, okruženje će se prikazati kao **Primenjeno**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="d6b75-133">Da biste potvrdili da se okruženje uspešno primenilo, izaberite **Prijavi se** i prijavite se u okruženje da biste potvrdili.</span><span class="sxs-lookup"><span data-stu-id="d6b75-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Detalji  okruženja](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="d6b75-135">Primenite ispravke na Finance okruženje</span><span class="sxs-lookup"><span data-stu-id="d6b75-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="d6b75-136">Project Operations zahteva Finance okruženje sa verzijom aplikacije **10.0.13 (10.0.569.20009)** ili novijom.</span><span class="sxs-lookup"><span data-stu-id="d6b75-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="d6b75-137">Možda ćete morati da primenite ispravke kvaliteta u svom Finance okruženju da biste dobili ovu verziju.</span><span class="sxs-lookup"><span data-stu-id="d6b75-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="d6b75-138">U LCS-u, na stranici **Detalji okruženja**, u odeljku **Dostupne ispravke** izaberite **Prikaži ispravku**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Prikaz ispravki](./media/5ViewUpdates.png)

2. <span data-ttu-id="d6b75-140">Na stranici **Binarna ažuriranja** izaberite **Sačuvaj paket.**</span><span class="sxs-lookup"><span data-stu-id="d6b75-140">On the **Binary updates** page, select **Save package.**</span></span>

![Sačuvaj paket](./media/6SavePackage.png)

3. <span data-ttu-id="d6b75-142">Kliknite na **Izaberi sve**, a zatim izaberite **Sačuvaj paket**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-142">Click **Select all** and then select **Save package**.</span></span>

![Pregledajte i sačuvajte ispravke](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="d6b75-144">Unesite naziv i opis paketa, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="d6b75-145">U zavisnosti od internet veze, ovaj postupak može potrajati.</span><span class="sxs-lookup"><span data-stu-id="d6b75-145">Depending on the internet connection, this process might take some time.</span></span>

![Otpremite paket u biblioteku sredstava](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="d6b75-147">Kada se paket sačuva, izaberite **Gotovo** i sačuvajte ovaj paket u biblioteci sredstava u vašem LCS projektu.</span><span class="sxs-lookup"><span data-stu-id="d6b75-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="d6b75-148">Čuvanje i potvrđivanje paketa može potrajati oko 15 minuta.</span><span class="sxs-lookup"><span data-stu-id="d6b75-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="d6b75-149">Da biste primenili ispravku, idite na stranicu **Detalji okruženja** u LCS-u i izaberite **Održavanje** > **Primeni ispravke**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Održavanje okruženja](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="d6b75-151">Na listi ispravki izaberite paket koji ste kreirali i izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Primena ispravki](./media/10ApplyUpdates.png)

<span data-ttu-id="d6b75-153">Servisiranje okruženja će potrajati neko vreme.</span><span class="sxs-lookup"><span data-stu-id="d6b75-153">Environment servicing will take some time.</span></span> <span data-ttu-id="d6b75-154">Po završetku, okruženje će se vratiti u primenjeno stanje.</span><span class="sxs-lookup"><span data-stu-id="d6b75-154">After it is complete, the environment will return to a deployed state.</span></span>

![Primenjeno okruženje](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="d6b75-156">Uspostavite vezu sa dvostrukim upisivanjem</span><span class="sxs-lookup"><span data-stu-id="d6b75-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="d6b75-157">U svom LCS projektu idite na stranicu **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d6b75-158">U odeljku **Common Data Service informacije o okruženju**, izaberite **Poveži sa uslugom CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="d6b75-159">Kada se povezivanje završi, ponovo izaberite **Poveži sa uslugom CDS za aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="d6b75-160">Bićete preusmereni na dvostruko upisivanje u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="d6b75-160">You will be redirected to Dual Write in Finance.</span></span>

![Povezivanje sa uslugom CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="d6b75-162">Izaberite **Primeni rešenje** za pristup entitetima koji će biti mapirani u integraciji.</span><span class="sxs-lookup"><span data-stu-id="d6b75-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Primena rešenja](./media/13ApplySolutions.png)

5. <span data-ttu-id="d6b75-164">Izaberite oba rešenja, **Dynamics 365 Finance and Operations mapa entiteta za dvostruko pisanje** i **Dynamics 365 Project Operations mape entiteta za dvostruko pisanje**, a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Potvrda rešenja](./media/14ConfirmSolutions.png)

<span data-ttu-id="d6b75-166">Kada primenite rešenja, entiteti dvostrukog upisivanja se primenjuju na okruženje.</span><span class="sxs-lookup"><span data-stu-id="d6b75-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Primena rešenja](./media/15ApplyingSolutions.png)

<span data-ttu-id="d6b75-168">Kada se entiteti primene, sva raspoloživa mapiranja se navode u okruženju.</span><span class="sxs-lookup"><span data-stu-id="d6b75-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mape za dvostruko upisivanje](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="d6b75-170">Osvežite entitete podataka nakon ispravke</span><span class="sxs-lookup"><span data-stu-id="d6b75-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="d6b75-171">U usluzi Finance idite na radni prostor **Upravljanje podacima**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-171">In Finance, go to the **Data management** workspace.</span></span>

![Radni prostor za upravljanje podacima](./media/16DataManagement.png)

2. <span data-ttu-id="d6b75-173">Izaberite pločicu **Parametri radnog okvira**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-173">Select the **Framework parameters** tile.</span></span>

![Parametri radnog okvira](./media/17FrameworkParameters.png)

3. <span data-ttu-id="d6b75-175">Na stranici **Podešavanja entiteta**, izaberite **Osveži listu entiteta**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Osveži listu entiteta](./media/18RefreshEntityList.png)

<span data-ttu-id="d6b75-177">Osvežavanje će trajati približno 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="d6b75-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="d6b75-178">Dobićete upozorenje kada se završi.</span><span class="sxs-lookup"><span data-stu-id="d6b75-178">You will receive an alert when it is complete.</span></span>

![Potvrda osvežavanja](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="d6b75-180">Ažuriranje bezbedonosnih podešavanja u usluzi Project Operations za Dataverse</span><span class="sxs-lookup"><span data-stu-id="d6b75-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="d6b75-181">Idite na Project Operations u Dataverse okruženju.</span><span class="sxs-lookup"><span data-stu-id="d6b75-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="d6b75-182">Idite na **Podešavanja** > **Bezbednost** > **Bezbednosne uloge**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="d6b75-183">Na stranici **Bezbedonosne uloge** sa liste uloga izaberite **korisnik aplikacije za dvostruko upisivanje** i izaberite karticu **Prilagođeni entiteti**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="d6b75-184">Proverite da li uloga ima dozvole **Čitanje** i **Priloži u** za:</span><span class="sxs-lookup"><span data-stu-id="d6b75-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="d6b75-185">**Tip deviznog kursa valute**</span><span class="sxs-lookup"><span data-stu-id="d6b75-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="d6b75-186">**Grafikon poslovnih kontakata**</span><span class="sxs-lookup"><span data-stu-id="d6b75-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="d6b75-187">**Fiskalni kalendar**</span><span class="sxs-lookup"><span data-stu-id="d6b75-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="d6b75-188">**Glavna knjiga**</span><span class="sxs-lookup"><span data-stu-id="d6b75-188">**Ledger**</span></span>

5. <span data-ttu-id="d6b75-189">Nakon ažuriranja bezbednosne uloge, idite na **Podešavanja** > **Bezbednost** > **Timovi** i izaberite podrazumevani tim u prikazu timova **Vlasnik lokalnog preduzeća**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="d6b75-190">Izaberite **Upravljanje ulogama** i proverite da li je bezbednosna privilegija **korisnik aplikacije za dvostruko upisivanje** primenjena na ovaj tim.</span><span class="sxs-lookup"><span data-stu-id="d6b75-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="d6b75-191">Pokrenite Project Operations mape dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="d6b75-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="d6b75-192">U svom LCS projektu idite na stranicu **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="d6b75-193">U odeljku **Common Data Service informacije o okruženju**, izaberite **Poveži sa uslugom CDS za aplikacije.**</span><span class="sxs-lookup"><span data-stu-id="d6b75-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="d6b75-194">Kada izaberete vezu, bićete preusmereni na listu entiteta u mapiranjima.</span><span class="sxs-lookup"><span data-stu-id="d6b75-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="d6b75-195">Pokrenite mape kao što je opisano u sledećoj tabeli.</span><span class="sxs-lookup"><span data-stu-id="d6b75-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="d6b75-196">Uverite se da sledite navedeni redosled.</span><span class="sxs-lookup"><span data-stu-id="d6b75-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="d6b75-197">**Mapa entiteta**</span><span class="sxs-lookup"><span data-stu-id="d6b75-197">**Entity Map**</span></span> | <span data-ttu-id="d6b75-198">**Osvežavanje entiteta**</span><span class="sxs-lookup"><span data-stu-id="d6b75-198">**Refresh entity**</span></span> | <span data-ttu-id="d6b75-199">**Početna sinhronizacija**</span><span class="sxs-lookup"><span data-stu-id="d6b75-199">**Initial sync**</span></span> | <span data-ttu-id="d6b75-200">**Master za početnu sinhronizaciju**</span><span class="sxs-lookup"><span data-stu-id="d6b75-200">**Master for initial sync**</span></span> | <span data-ttu-id="d6b75-201">**Preduslovi za pokretanje**</span><span class="sxs-lookup"><span data-stu-id="d6b75-201">**Run prerequisites**</span></span> | <span data-ttu-id="d6b75-202">**Početna sinhronizacija preduslova**</span><span class="sxs-lookup"><span data-stu-id="d6b75-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="d6b75-203">**Uloge projektnih resursa za sva preduzeća (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="d6b75-204">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-204">No</span></span> | <span data-ttu-id="d6b75-205">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-205">Yes</span></span> | <span data-ttu-id="d6b75-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d6b75-206">Common Data Service</span></span> | <span data-ttu-id="d6b75-207">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-207">No</span></span> | <span data-ttu-id="d6b75-208">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-208">N\A</span></span> |
| <span data-ttu-id="d6b75-209">**Pravna lica (cdm\_preduzeća)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="d6b75-210">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-210">No</span></span> | <span data-ttu-id="d6b75-211">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-211">Yes</span></span> | <span data-ttu-id="d6b75-212">Finance and Operations aplikacije</span><span class="sxs-lookup"><span data-stu-id="d6b75-212">Finance and Operations apps</span></span> | <span data-ttu-id="d6b75-213">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-213">No</span></span> | <span data-ttu-id="d6b75-214">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-214">N\A</span></span> |
| <span data-ttu-id="d6b75-215">**Knjiga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="d6b75-216">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-216">No</span></span> | <span data-ttu-id="d6b75-217">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-217">Yes</span></span> | <span data-ttu-id="d6b75-218">Finance and Operations aplikacije</span><span class="sxs-lookup"><span data-stu-id="d6b75-218">Finance and Operations apps</span></span> | <span data-ttu-id="d6b75-219">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-219">Yes</span></span> | <span data-ttu-id="d6b75-220">Da, Finance and Operations aplikacije</span><span class="sxs-lookup"><span data-stu-id="d6b75-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="d6b75-221">**Project Operations stvarne vrednosti integracije (msdyn\_stvarne vrednosti)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="d6b75-222">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-222">No</span></span> | <span data-ttu-id="d6b75-223">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-223">No</span></span> | <span data-ttu-id="d6b75-224">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-224">N\A</span></span> | <span data-ttu-id="d6b75-225">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-225">Yes</span></span> | <span data-ttu-id="d6b75-226">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-226">No</span></span> |
| <span data-ttu-id="d6b75-227">**Predmeti ugovora projekta (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="d6b75-228">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-228">No</span></span> | <span data-ttu-id="d6b75-229">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-229">No</span></span> | <span data-ttu-id="d6b75-230">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-230">N\A</span></span> | <span data-ttu-id="d6b75-231">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-231">No</span></span> | <span data-ttu-id="d6b75-232">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-232">No</span></span> |
| <span data-ttu-id="d6b75-233">**Entitet integracije za odnose transakcija projekta (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="d6b75-234">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-234">No</span></span> | <span data-ttu-id="d6b75-235">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-235">No</span></span> | <span data-ttu-id="d6b75-236">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-236">N\A</span></span> | <span data-ttu-id="d6b75-237">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-237">No</span></span> | <span data-ttu-id="d6b75-238">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-238">N\A</span></span> |
| <span data-ttu-id="d6b75-239">**Project Operations kontrolne tačke predmeta ugovora o integraciji (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="d6b75-240">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-240">No</span></span> | <span data-ttu-id="d6b75-241">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-241">No</span></span> | <span data-ttu-id="d6b75-242">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-242">N\A</span></span> | <span data-ttu-id="d6b75-243">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-243">No</span></span> | <span data-ttu-id="d6b75-244">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-244">N\A</span></span> |
| <span data-ttu-id="d6b75-245">**Project Operations entitet integracije za procene troškova (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="d6b75-246">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-246">No</span></span> | <span data-ttu-id="d6b75-247">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-247">No</span></span> | <span data-ttu-id="d6b75-248">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-248">N\A</span></span> | <span data-ttu-id="d6b75-249">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-249">No</span></span> | <span data-ttu-id="d6b75-250">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-250">N\A</span></span> |
| <span data-ttu-id="d6b75-251">**Project Operations entitet izvoza kategorija troškova projekta (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="d6b75-252">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-252">No</span></span> | <span data-ttu-id="d6b75-253">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-253">No</span></span> | <span data-ttu-id="d6b75-254">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-254">N\A</span></span> | <span data-ttu-id="d6b75-255">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-255">No</span></span> | <span data-ttu-id="d6b75-256">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-256">N\A</span></span> |
| <span data-ttu-id="d6b75-257">**Project Operations entitet izvoza troškova integracije projekta (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="d6b75-258">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-258">Yes</span></span> | <span data-ttu-id="d6b75-259">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-259">No</span></span> | <span data-ttu-id="d6b75-260">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-260">N\A</span></span> | <span data-ttu-id="d6b75-261">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-261">No</span></span> | <span data-ttu-id="d6b75-262">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-262">N\A</span></span> |
| <span data-ttu-id="d6b75-263">**Project Operations entitet integracije za procene sati (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="d6b75-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="d6b75-264">Da</span><span class="sxs-lookup"><span data-stu-id="d6b75-264">Yes</span></span> | <span data-ttu-id="d6b75-265">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-265">No</span></span> | <span data-ttu-id="d6b75-266">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-266">N\A</span></span> | <span data-ttu-id="d6b75-267">No</span><span class="sxs-lookup"><span data-stu-id="d6b75-267">No</span></span> | <span data-ttu-id="d6b75-268">Nije primenjivo</span><span class="sxs-lookup"><span data-stu-id="d6b75-268">N\A</span></span> |


4. <span data-ttu-id="d6b75-269">Da biste osvežili entitet, izaberite naziv mape, a zatim izaberite **Osveži entitete**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Osvežavanje mape](./media/20RefreshMapping.png)

5. <span data-ttu-id="d6b75-271">Kada se osvežavanje završi, pokrenite mapu.</span><span class="sxs-lookup"><span data-stu-id="d6b75-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="d6b75-272">Pre nego što omogućite sledeću mapu, proverite da li je mapa u tabeli u stanju **Pokrenuta**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="d6b75-273">Pokretanje mapa sa većim brojem preduslova može potrajati.</span><span class="sxs-lookup"><span data-stu-id="d6b75-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="d6b75-274">Da biste pokrenuli mapu sa preduslovima, omogućite preklopno dugme **Prikaži povezane mape entiteta**.</span><span class="sxs-lookup"><span data-stu-id="d6b75-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="d6b75-275">Ako tabela pokazuje da **Početna sinhronizacija preduslova** ima vrednost **Ne**, proverite da li je zastavica **Početna sinhronizacija** **isključena** u svim mapama preduslova pre nego što je pokrenete.</span><span class="sxs-lookup"><span data-stu-id="d6b75-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Pokretanje mape](./media/21RunMap.png)

6. <span data-ttu-id="d6b75-277">Potvrdite da su sve mape povezane sa projektom u aktivnom stanju.</span><span class="sxs-lookup"><span data-stu-id="d6b75-277">Validate all project related maps are in the running state.</span></span>

![Sve mape su pokrenute](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="d6b75-279">Primena podataka o konfiguraciji u usluzi CDS za Project Operations (opcionalno)</span><span class="sxs-lookup"><span data-stu-id="d6b75-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="d6b75-280">Ako ste primenili demo podatke na Finance okruženje, pogledajte članak [Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations](resource-apply-pro-setup-config-data.md) za primenu demo podataka na CDS okruženje.</span><span class="sxs-lookup"><span data-stu-id="d6b75-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="d6b75-281">Vaše Project Operations okruženje je sada obezbeđeno i konfigurisano.</span><span class="sxs-lookup"><span data-stu-id="d6b75-281">Your Project Operations environment is now provisioned and configured.</span></span> 
