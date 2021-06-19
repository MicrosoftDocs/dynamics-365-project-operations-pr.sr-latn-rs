---
title: Ažuriranje usluge Project Operations u Finance okruženju
description: Ova tema pruža informacije o tome kako da ažurirate uslugu Project Operations u Dynamics 365 Finance okruženju.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d85a180aa094a048b4422605b25151d10785f67d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011073"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="27593-103">Ažuriranje usluge Project Operations u Finance okruženju</span><span class="sxs-lookup"><span data-stu-id="27593-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="27593-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="27593-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="27593-105">Ova tema pruža informacije o tome kako da ažurirate Dynamics 365 Project Operations u Dynamics 365 Finance okruženju.</span><span class="sxs-lookup"><span data-stu-id="27593-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="27593-106">Postoje tri procedure potrebne za ažuriranje usluge Project Operations na ispravku 5 (Microsoft Dynamics CRM 2011 Update Rollup 5):</span><span class="sxs-lookup"><span data-stu-id="27593-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="27593-107">Uvoz paketa u projekat pregleda</span><span class="sxs-lookup"><span data-stu-id="27593-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="27593-108">Primena ispravke</span><span class="sxs-lookup"><span data-stu-id="27593-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="27593-109">Ažuriranje Dataverse okruženja</span><span class="sxs-lookup"><span data-stu-id="27593-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="27593-110">Uvoz paketa u LCS projekat</span><span class="sxs-lookup"><span data-stu-id="27593-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="27593-111">Prijavite se na [Lifecycle Services (LCS)](https://lcs.dynamics.com/) kao vlasnik projekta ili menadžer okruženja.</span><span class="sxs-lookup"><span data-stu-id="27593-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="27593-112">Sa liste projekata odaberite LCS projekat.</span><span class="sxs-lookup"><span data-stu-id="27593-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="27593-113">Na stranici **Projekat** u grupi **Okruženja** otvorite okruženje koje želite da ažurirate.</span><span class="sxs-lookup"><span data-stu-id="27593-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="27593-114">Proverite da li je okruženje pokrenuto.</span><span class="sxs-lookup"><span data-stu-id="27593-114">Verify that the environment is running.</span></span> <span data-ttu-id="27593-115">Ako nije pokrenuto, pokrenite okruženje.</span><span class="sxs-lookup"><span data-stu-id="27593-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="27593-116">U odeljku **Novo izdanje** pod **Dostupne ispravke** izaberite **Prikaži ispravku** za 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="27593-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Dugme „Prikaži ispravku“](media/view-update.png)

6. <span data-ttu-id="27593-118">Na stranici **Binarna ažuriranja** izaberite **Sačuvaj paket**.</span><span class="sxs-lookup"><span data-stu-id="27593-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="27593-119">Na stranici **Pregled i čuvanje ispravki** izaberite **Sačuvaj paket**.</span><span class="sxs-lookup"><span data-stu-id="27593-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="27593-120">U oknu **Čuvanje paketa u biblioteci sredstava** koji se otvori unesite naziv paketa, a zatim izaberite **Sačuvaj paket**.</span><span class="sxs-lookup"><span data-stu-id="27593-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="27593-121">Kada LCS završi čuvanje paketa, dugme **Gotovo** će biti omogućeno.</span><span class="sxs-lookup"><span data-stu-id="27593-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="27593-122">Izaberite **Gotovo**.</span><span class="sxs-lookup"><span data-stu-id="27593-122">Select **Done**.</span></span> <span data-ttu-id="27593-123">LCS će verifikovati paket.</span><span class="sxs-lookup"><span data-stu-id="27593-123">LCS will verify the package.</span></span> <span data-ttu-id="27593-124">Verifikacija može trajati nekoliko minuta, najviše do sat vremena.</span><span class="sxs-lookup"><span data-stu-id="27593-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="27593-125">Primena ispravke paketa</span><span class="sxs-lookup"><span data-stu-id="27593-125">Apply the package update</span></span>

1. <span data-ttu-id="27593-126">U usluzi LCS, na stranici **Detalji okruženja** izaberite **Održavaj** > **Primeni ispravke**.</span><span class="sxs-lookup"><span data-stu-id="27593-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="27593-127">Na listi izaberite paket koji ste ranije sačuvali, a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="27593-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="27593-128">Izaberite **Da** da biste potvrdili da želite da primenite paket.</span><span class="sxs-lookup"><span data-stu-id="27593-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Potvrdite izbor u dijalogu „Primena paketa“](media/confirm-package-deployment.png)

4. <span data-ttu-id="27593-130">Izaberite **Da** da biste potvrdili da želite da ažurirate aplikaciju.</span><span class="sxs-lookup"><span data-stu-id="27593-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Potvrdite izbor u dijalogu „Ažuriranje aplikacije“](media/confirm-application-update.png)

<span data-ttu-id="27593-132">Pokrenuće se primena i ažuriranje aplikacije.</span><span class="sxs-lookup"><span data-stu-id="27593-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="27593-133">Na stranici **Detalji okruženja**, u gornjem desnom uglu, status okruženja će se ažurirati na **Servisiranje**.</span><span class="sxs-lookup"><span data-stu-id="27593-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="27593-134">Za otprilike dva sata ažuriranje će biti gotovo.</span><span class="sxs-lookup"><span data-stu-id="27593-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="27593-135">Informacije o izdanju aplikacije će se ažurirati na **Microsoft Dynamics 365 for Finance and Operations 10.0.15** a status okruženja će se ažurirati na **Primenjeno**.</span><span class="sxs-lookup"><span data-stu-id="27593-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="27593-136">Ažuriranje Dataverse okruženja</span><span class="sxs-lookup"><span data-stu-id="27593-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="27593-137">Prijavite se u [Power Platform centar administracije](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="27593-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="27593-138">Na listi pronađite i otvorite okruženje koje ste koristili za instaliranje usluge Project Operations.</span><span class="sxs-lookup"><span data-stu-id="27593-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="27593-139">Na stranici **Okruženja** izaberite **Resurs** > **Dynamics 365 aplikacije**.</span><span class="sxs-lookup"><span data-stu-id="27593-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="27593-140">Na listi pronađite **Microsoft Dynamics 365 Project Operations** i u koloni **Status** izaberite **Dostupna ispravka**.</span><span class="sxs-lookup"><span data-stu-id="27593-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="27593-141">Označite polje za potvrdu **Slažem se sa uslovima korišćenja usluge**, a zatim izaberite **Ažuriraj**.</span><span class="sxs-lookup"><span data-stu-id="27593-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="27593-142">Biće instalirana najnovija verzija rešenja.</span><span class="sxs-lookup"><span data-stu-id="27593-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="27593-143">Po završetku instalacije imaćete instaliranu verziju 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="27593-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="27593-144">Konfigurisanje novih funkcija</span><span class="sxs-lookup"><span data-stu-id="27593-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="27593-145">Omogućavanje mapiranja dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="27593-145">Enable dual-write mapping</span></span>

<span data-ttu-id="27593-146">Nakon što dovršite ažuriranje Finance i Dataverse okruženja, možete omogućiti potrebna mapiranja dvostrukog upisivanja.</span><span class="sxs-lookup"><span data-stu-id="27593-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="27593-147">Obavite sledeće procedure da biste omogućili mapiranje dvostrukog upisivanja.</span><span class="sxs-lookup"><span data-stu-id="27593-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="27593-148">Ažuriranje bezbedonosnih podešavanja u Customer Engagement okruženju</span><span class="sxs-lookup"><span data-stu-id="27593-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="27593-149">Osvežavanje entiteta podataka</span><span class="sxs-lookup"><span data-stu-id="27593-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="27593-150">Ažuriranje i pokretanje mapiranja dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="27593-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="27593-151">Ažuriranje bezbedonosnih podešavanja u Dataverse okruženju</span><span class="sxs-lookup"><span data-stu-id="27593-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="27593-152">Sledeće ispravke bezbednosnih privilegija za entitete su potrebne kao deo ažuriranja na Microsoft Dynamics CRM 2011 Update Rollup 5.</span><span class="sxs-lookup"><span data-stu-id="27593-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="27593-153">U okruženju Dataverse idite na **Podešavanja** i u grupi **Sistem** izaberite **Bezbednost**.</span><span class="sxs-lookup"><span data-stu-id="27593-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Podešavanja Dataverse okruženja](media/Picture21.png)

2. <span data-ttu-id="27593-155">Izaberite **Bezbednosne uloge**.</span><span class="sxs-lookup"><span data-stu-id="27593-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="27593-156">Sa liste uloga izaberite **korisnik aplikacije za dvostruko upisivanje** i izaberite karticu **Prilagođeni entiteti**.</span><span class="sxs-lookup"><span data-stu-id="27593-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="27593-157">Proverite da li uloga ima dozvole **Čitanje** i **Priloži u** za:</span><span class="sxs-lookup"><span data-stu-id="27593-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="27593-158">**Tip deviznog kursa valute**</span><span class="sxs-lookup"><span data-stu-id="27593-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="27593-159">**Grafikon poslovnih kontakata**</span><span class="sxs-lookup"><span data-stu-id="27593-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="27593-160">**Fiskalni kalendar**</span><span class="sxs-lookup"><span data-stu-id="27593-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="27593-161">**Glavna knjiga**</span><span class="sxs-lookup"><span data-stu-id="27593-161">**Ledger**</span></span>

5. <span data-ttu-id="27593-162">Nakon ažuriranja bezbednosne uloge, idite na **Podešavanja** > **Bezbednost** > **Timovi**.</span><span class="sxs-lookup"><span data-stu-id="27593-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="27593-163">Proverite da li je uloga **korisnik aplikacije za dvostruko upisivanje** primenjena na tim.</span><span class="sxs-lookup"><span data-stu-id="27593-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="27593-164">Osvežavanje entiteta podataka iz ispravke</span><span class="sxs-lookup"><span data-stu-id="27593-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="27593-165">U Finance okruženju otvorite radni prostor **Upravljanje podacima**, a zatim otvorite stranicu **Parametri okvira**.</span><span class="sxs-lookup"><span data-stu-id="27593-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="27593-166">Na kartici **Podešavanja entiteta** izaberite **Osveži listu entiteta**.</span><span class="sxs-lookup"><span data-stu-id="27593-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="27593-167">Izaberite **Zatvori** da biste potvrdili osvežavanje entiteta.</span><span class="sxs-lookup"><span data-stu-id="27593-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="27593-168">Ovaj postupak će se završiti za oko 20 minuta.</span><span class="sxs-lookup"><span data-stu-id="27593-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="27593-169">Bićete obavešteni kada se osvežavanje završi.</span><span class="sxs-lookup"><span data-stu-id="27593-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="27593-170">Ažuriranje mapiranja dvostrukog upisivanja</span><span class="sxs-lookup"><span data-stu-id="27593-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="27593-171">U radnom prostoru **Upravljanje podacima** izaberite **Dvostruko upisivanje**.</span><span class="sxs-lookup"><span data-stu-id="27593-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="27593-172">Izaberite **Primeni rešenja**, izaberite oba rešenja sa liste, a zatim izaberite **Primeni**.</span><span class="sxs-lookup"><span data-stu-id="27593-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="27593-173">Na stranici **Dvostruko upisivanje** izaberite sledeće mape tabela, a zatim izaberite **Zaustavi**.</span><span class="sxs-lookup"><span data-stu-id="27593-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="27593-174">**Project Operations stvarne vrednosti integracije (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="27593-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="27593-175">**Project Operations integracija kategorija troškova projekata (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="27593-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="27593-176">**Entitet za izvoz troškova projekata za Project Operations stvarne vrednosti integracije (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="27593-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="27593-177">Na stranici **Verzija mape tabele** primenite novu verziju mape na svaki od tri entiteta.</span><span class="sxs-lookup"><span data-stu-id="27593-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="27593-178">Na stranici **Dvostruko upisivanje** izaberite „Pokreni“ da biste ponovo pokrenuli mape.</span><span class="sxs-lookup"><span data-stu-id="27593-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="27593-179">Na listi mapa odaberite mapu **Glavna knjiga (msdyn_ledgers)** sa svim preduslovima i označite polje za potvrdu **Početna sinhronizacija**.</span><span class="sxs-lookup"><span data-stu-id="27593-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="27593-180">U polju **Master za početnu sinhronizaciju** izaberite **Finance and Operations aplikacije**, a zatim izaberite **Pokreni**.</span><span class="sxs-lookup"><span data-stu-id="27593-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sinhronizacija mape glavne knjige](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]