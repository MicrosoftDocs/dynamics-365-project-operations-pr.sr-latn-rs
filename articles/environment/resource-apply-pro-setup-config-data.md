---
title: Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations
description: Ova tema pruža informacije o tome kako da podesite i primenite podatke o konfiguraciji u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e72b88a4dae1eb89859fdfd55f6d5e6ee5befcd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083453"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="d5007-103">Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service za Project Operations</span><span class="sxs-lookup"><span data-stu-id="d5007-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="d5007-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="d5007-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d5007-105">Podaci o podešavanju i konfiguraciji instaliranja</span><span class="sxs-lookup"><span data-stu-id="d5007-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="d5007-106">Preuzmite, deblokirajte i raspakujte [Paket podataka za podešavanje i konfiguraciju](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="d5007-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="d5007-107">Idite u fasciklu sa raspakovanim sadržajem i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d5007-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d5007-108">Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke** , a zatim izaberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="d5007-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d5007-110">Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.</span><span class="sxs-lookup"><span data-stu-id="d5007-110">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d5007-111">Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="d5007-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d5007-112">Izaberite region vašeg zakupca, unesite svoje akreditive, pa izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="d5007-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d5007-114">Na 3. stranici, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="d5007-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d5007-115">Na 4. stranici, izaberite zip datoteku *SampleSetupAndConfigData* iz raspakovane fascikle.</span><span class="sxs-lookup"><span data-stu-id="d5007-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Izbor zip datoteke](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. <span data-ttu-id="d5007-118">Kada izaberete zip datoteku, izaberite **Uvoz podataka**.</span><span class="sxs-lookup"><span data-stu-id="d5007-118">After the zip file is selected, select **Import Data**.</span></span>

![Uvezi podatke](./media/5ImportData.png)

10. <span data-ttu-id="d5007-120">Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="d5007-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d5007-121">Po završetku uvoza, izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="d5007-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d5007-122">Potražite u svojoj organizaciji podatke za sledećih 19 entiteta:</span><span class="sxs-lookup"><span data-stu-id="d5007-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="d5007-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="d5007-123">Currency</span></span>
  - <span data-ttu-id="d5007-124">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="d5007-124">Organizational Unit</span></span>
  - <span data-ttu-id="d5007-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="d5007-125">Contact</span></span>
  - <span data-ttu-id="d5007-126">Poreska grupa</span><span class="sxs-lookup"><span data-stu-id="d5007-126">Tax Group</span></span>
  - <span data-ttu-id="d5007-127">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="d5007-127">Customer Group</span></span>
  - <span data-ttu-id="d5007-128">Jedinica</span><span class="sxs-lookup"><span data-stu-id="d5007-128">Unit</span></span>
  - <span data-ttu-id="d5007-129">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="d5007-129">Unit Group</span></span>
  - <span data-ttu-id="d5007-130">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="d5007-130">Price List</span></span>
  - <span data-ttu-id="d5007-131">Cenovnik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="d5007-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="d5007-132">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="d5007-132">Invoice Frequency</span></span>
  - <span data-ttu-id="d5007-133">Kategorija resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="d5007-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="d5007-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="d5007-134">Transaction Category</span></span>
  - <span data-ttu-id="d5007-135">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="d5007-135">Expense Category</span></span>
  - <span data-ttu-id="d5007-136">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="d5007-136">Role Price</span></span>
  - <span data-ttu-id="d5007-137">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="d5007-137">Transaction Category Price</span></span>
  - <span data-ttu-id="d5007-138">Karakteristika</span><span class="sxs-lookup"><span data-stu-id="d5007-138">Characteristic</span></span>
  - <span data-ttu-id="d5007-139">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="d5007-139">Bookable Resource</span></span>
  - <span data-ttu-id="d5007-140">Povezivanje kategorije resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="d5007-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d5007-141">Karakteristika resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="d5007-141">Bookable Resource Characteristic</span></span>

![Kompletan uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d5007-143">Ažuriranje Project Operations konfiguracije</span><span class="sxs-lookup"><span data-stu-id="d5007-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d5007-144">Idite u CE okruženje.</span><span class="sxs-lookup"><span data-stu-id="d5007-144">Navigate to the CE environment.</span></span> <span data-ttu-id="d5007-145">Možete ga pronaći ako otvorite [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/environments), izaberete okruženje, a zatim izaberete **Otvoreno okruženje**.</span><span class="sxs-lookup"><span data-stu-id="d5007-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvoreno okruženje](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d5007-147">Idite na **Projekti** > **Resursi** , a zatim izaberite **Novo** da biste kreirali resurs koji može da se rezerviše za vašeg korisnika.</span><span class="sxs-lookup"><span data-stu-id="d5007-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resursi koji mogu da se rezervišu](./media/8BookableResources.png)

3. <span data-ttu-id="d5007-149">Na kartici **Opšti podaci** izaberite svog administratora.</span><span class="sxs-lookup"><span data-stu-id="d5007-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d5007-150">Proverite da li se vremenska zona podudara sa onom u kojoj se nalazite.</span><span class="sxs-lookup"><span data-stu-id="d5007-150">Verify that the time zone matches the one you are in.</span></span> 

![Novi resurs koji može da se rezerviše](./media/9NewBookableResource.png)

4. <span data-ttu-id="d5007-152">Na kartici **Zakazivanje** , u polju **Kompanija** odaberite kompaniju **USPM** , a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d5007-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kartica „Zakazivanje“](./media/10SchedulingTab.png)

5. <span data-ttu-id="d5007-154">Izaberite karticu **Radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="d5007-154">Select the **Work hours** tab.</span></span>  

![Radno vreme](./media/11WorkHours.png)

6. <span data-ttu-id="d5007-156">Dvaput kliknite bilo koju vrednost u kalendaru i izaberite **Uređivanje** > **Svi događaji u seriji**.</span><span class="sxs-lookup"><span data-stu-id="d5007-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar posla](./media/12WorkCalendar.png)

7. <span data-ttu-id="d5007-158">Promenite radno vreme u radni dan od osam (8) sati, obeležite vikende kao neradne dane i uverite se da vremenska zona odgovara vašoj.</span><span class="sxs-lookup"><span data-stu-id="d5007-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d5007-159">Izaberite stavku **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="d5007-159">Select **Save and close**.</span></span>

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d5007-161">Idite na **Podešavanja** > **Predlošci kalendara** i izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="d5007-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d5007-163">Unesite naziv, izaberite resurs šablona koji ste kreirali, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d5007-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Čuvanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d5007-165">Idite na **Parametri** i dvaput kliknite na zapis.</span><span class="sxs-lookup"><span data-stu-id="d5007-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d5007-167">Ažurirajte sledeća polja:</span><span class="sxs-lookup"><span data-stu-id="d5007-167">Update the following fields:</span></span>

 - <span data-ttu-id="d5007-168">**Podrazumevana kompanija** : USPM</span><span class="sxs-lookup"><span data-stu-id="d5007-168">**Default company** : USPM</span></span>
 - <span data-ttu-id="d5007-169">**Podrazumevana organizaciona jedinica** : Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="d5007-169">**Default Organizational Unit** : Contoso Robotics Global</span></span>
 - <span data-ttu-id="d5007-170">**Učestalost fakturisanja** : Sedmi i poslednji dan</span><span class="sxs-lookup"><span data-stu-id="d5007-170">**Invoice Frequency** : Seventh and Last day</span></span>
 - <span data-ttu-id="d5007-171">**Predložak radnog vremena** : Promenite na predložak koji ste kreirali.</span><span class="sxs-lookup"><span data-stu-id="d5007-171">**Work hour template** : Change to the template you created.</span></span>

13. <span data-ttu-id="d5007-172">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="d5007-172">Select **Save**.</span></span> 

![Ažurirani parametri projekta](./media/17UpdatedProjectParameters.png)
