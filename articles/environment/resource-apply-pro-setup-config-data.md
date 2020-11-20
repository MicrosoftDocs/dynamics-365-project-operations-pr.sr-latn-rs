---
title: Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service
description: Ova tema pruža informacije o tome kako da podesite i primenite podatke o konfiguraciji u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401145"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="ca259-103">Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ca259-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="ca259-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ca259-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ca259-105">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="ca259-105">Prerequisites</span></span>

<span data-ttu-id="ca259-106">Pre nego što započnete konfigurisanje podataka u usluzi Common Data Service (CDS), moraju biti ispunjeni sledeći preduslovi:</span><span class="sxs-lookup"><span data-stu-id="ca259-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="ca259-107">Obezbedite CDS okruženje i Dynamics 365 Finance okruženje za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ca259-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="ca259-108">Informacije o pravnom licu iz usluge Dynamics 365 Finance se dele sa CDS okruženjem.</span><span class="sxs-lookup"><span data-stu-id="ca259-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="ca259-109">To znači da entitet **Kompanija** u CDS-u ima sledeće evidencije preduzeća:</span><span class="sxs-lookup"><span data-stu-id="ca259-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="ca259-110">THPM</span><span class="sxs-lookup"><span data-stu-id="ca259-110">THPM</span></span>
  - <span data-ttu-id="ca259-111">USPM</span><span class="sxs-lookup"><span data-stu-id="ca259-111">USPM</span></span>
  - <span data-ttu-id="ca259-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="ca259-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="ca259-113">Podaci o podešavanju i konfiguraciji instaliranja</span><span class="sxs-lookup"><span data-stu-id="ca259-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="ca259-114">Preuzmite, deblokirajte i raspakujte [Paket podataka za podešavanje i konfiguraciju](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="ca259-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="ca259-115">Idite u fasciklu sa raspakovanim sadržajem i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ca259-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ca259-116">Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="ca259-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ca259-118">Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.</span><span class="sxs-lookup"><span data-stu-id="ca259-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ca259-119">Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="ca259-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ca259-120">Izaberite region vašeg zakupca, unesite svoje akreditive, pa izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="ca259-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ca259-122">Na 3. stranici, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="ca259-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="ca259-123">Na 4. stranici, izaberite zip datoteku *SampleSetupAndConfigData* iz raspakovane fascikle.</span><span class="sxs-lookup"><span data-stu-id="ca259-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Izbor zip datoteke](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. <span data-ttu-id="ca259-126">Kada izaberete zip datoteku, izaberite **Uvoz podataka**.</span><span class="sxs-lookup"><span data-stu-id="ca259-126">After the zip file is selected, select **Import Data**.</span></span>

![Uvezi podatke](./media/5ImportData.png)

10. <span data-ttu-id="ca259-128">Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="ca259-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ca259-129">Po završetku uvoza, izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="ca259-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ca259-130">Potražite u svojoj organizaciji podatke za sledećih 19 entiteta:</span><span class="sxs-lookup"><span data-stu-id="ca259-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="ca259-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="ca259-131">Currency</span></span>
  - <span data-ttu-id="ca259-132">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="ca259-132">Organizational Unit</span></span>
  - <span data-ttu-id="ca259-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ca259-133">Contact</span></span>
  - <span data-ttu-id="ca259-134">Poreska grupa</span><span class="sxs-lookup"><span data-stu-id="ca259-134">Tax Group</span></span>
  - <span data-ttu-id="ca259-135">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="ca259-135">Customer Group</span></span>
  - <span data-ttu-id="ca259-136">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ca259-136">Unit</span></span>
  - <span data-ttu-id="ca259-137">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="ca259-137">Unit Group</span></span>
  - <span data-ttu-id="ca259-138">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="ca259-138">Price List</span></span>
  - <span data-ttu-id="ca259-139">Cenovnik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="ca259-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="ca259-140">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="ca259-140">Invoice Frequency</span></span>
  - <span data-ttu-id="ca259-141">Kategorija resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ca259-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="ca259-142">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="ca259-142">Transaction Category</span></span>
  - <span data-ttu-id="ca259-143">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="ca259-143">Expense Category</span></span>
  - <span data-ttu-id="ca259-144">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="ca259-144">Role Price</span></span>
  - <span data-ttu-id="ca259-145">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="ca259-145">Transaction Category Price</span></span>
  - <span data-ttu-id="ca259-146">Karakteristika</span><span class="sxs-lookup"><span data-stu-id="ca259-146">Characteristic</span></span>
  - <span data-ttu-id="ca259-147">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ca259-147">Bookable Resource</span></span>
  - <span data-ttu-id="ca259-148">Povezivanje kategorije resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ca259-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="ca259-149">Karakteristika resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ca259-149">Bookable Resource Characteristic</span></span>

![Kompletan uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="ca259-151">Ažuriranje Project Operations konfiguracije</span><span class="sxs-lookup"><span data-stu-id="ca259-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="ca259-152">Idite u CE okruženje.</span><span class="sxs-lookup"><span data-stu-id="ca259-152">Navigate to the CE environment.</span></span> <span data-ttu-id="ca259-153">Možete ga pronaći ako otvorite [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/environments), izaberete okruženje, a zatim izaberete **Otvoreno okruženje**.</span><span class="sxs-lookup"><span data-stu-id="ca259-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvoreno okruženje](./media/7OpenEnvironment.png)

2. <span data-ttu-id="ca259-155">Idite na **Projekti** > **Resursi**, a zatim izaberite **Novo** da biste kreirali resurs koji može da se rezerviše za vašeg korisnika.</span><span class="sxs-lookup"><span data-stu-id="ca259-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resursi koji mogu da se rezervišu](./media/8BookableResources.png)

3. <span data-ttu-id="ca259-157">Na kartici **Opšti podaci** izaberite svog administratora.</span><span class="sxs-lookup"><span data-stu-id="ca259-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="ca259-158">Proverite da li se vremenska zona podudara sa onom u kojoj se nalazite.</span><span class="sxs-lookup"><span data-stu-id="ca259-158">Verify that the time zone matches the one you are in.</span></span> 

![Novi resurs koji može da se rezerviše](./media/9NewBookableResource.png)

4. <span data-ttu-id="ca259-160">Na kartici **Zakazivanje**, u polju **Kompanija** odaberite kompaniju **USPM**, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ca259-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kartica „Zakazivanje“](./media/10SchedulingTab.png)

5. <span data-ttu-id="ca259-162">Izaberite karticu **Radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="ca259-162">Select the **Work hours** tab.</span></span>  

![Radno vreme](./media/11WorkHours.png)

6. <span data-ttu-id="ca259-164">Dvaput kliknite bilo koju vrednost u kalendaru i izaberite **Uređivanje** > **Svi događaji u seriji**.</span><span class="sxs-lookup"><span data-stu-id="ca259-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar posla](./media/12WorkCalendar.png)

7. <span data-ttu-id="ca259-166">Promenite radno vreme u radni dan od osam (8) sati, obeležite vikende kao neradne dane i uverite se da vremenska zona odgovara vašoj.</span><span class="sxs-lookup"><span data-stu-id="ca259-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="ca259-167">Izaberite stavku **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="ca259-167">Select **Save and close**.</span></span>

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. <span data-ttu-id="ca259-169">Idite na **Podešavanja** > **Predlošci kalendara** i izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="ca259-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="ca259-171">Unesite naziv, izaberite resurs šablona koji ste kreirali, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ca259-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Čuvanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="ca259-173">Idite na **Parametri** i dvaput kliknite na zapis.</span><span class="sxs-lookup"><span data-stu-id="ca259-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="ca259-175">Ažurirajte sledeća polja:</span><span class="sxs-lookup"><span data-stu-id="ca259-175">Update the following fields:</span></span>

 - <span data-ttu-id="ca259-176">**Podrazumevana kompanija**: USPM</span><span class="sxs-lookup"><span data-stu-id="ca259-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="ca259-177">**Podrazumevana organizaciona jedinica**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="ca259-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="ca259-178">**Učestalost fakturisanja**: Sedmi i poslednji dan</span><span class="sxs-lookup"><span data-stu-id="ca259-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="ca259-179">**Predložak radnog vremena**: Promenite na predložak koji ste kreirali.</span><span class="sxs-lookup"><span data-stu-id="ca259-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="ca259-180">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ca259-180">Select **Save**.</span></span> 

![Ažurirani parametri projekta](./media/17UpdatedProjectParameters.png)
