---
title: Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service
description: Ova tema pruža informacije o tome kako da podesite i primenite podatke o konfiguraciji u usluzi Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001308"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="ebf11-103">Podešavanje i primena podataka o konfiguraciji u usluzi Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ebf11-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="ebf11-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="ebf11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="ebf11-105">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="ebf11-105">Prerequisites</span></span>

<span data-ttu-id="ebf11-106">Pre nego što počnete da konfigurišete podatke u usluzi Common Data Service (CDS), moraju biti ispunjeni sledeći preduslovi:</span><span class="sxs-lookup"><span data-stu-id="ebf11-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="ebf11-107">Obezbedite CDS okruženje i Dynamics 365 Finance okruženje za Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ebf11-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="ebf11-108">Informacije o pravnom licu iz usluge Dynamics 365 Finance se dele sa CDS okruženjem.</span><span class="sxs-lookup"><span data-stu-id="ebf11-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="ebf11-109">To znači da entitet **Kompanija** u CDS-u ima sledeće evidencije preduzeća:</span><span class="sxs-lookup"><span data-stu-id="ebf11-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="ebf11-110">THPM</span><span class="sxs-lookup"><span data-stu-id="ebf11-110">THPM</span></span>
  - <span data-ttu-id="ebf11-111">USPM</span><span class="sxs-lookup"><span data-stu-id="ebf11-111">USPM</span></span>
  - <span data-ttu-id="ebf11-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="ebf11-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="ebf11-113">Podaci o podešavanju i konfiguraciji instaliranja</span><span class="sxs-lookup"><span data-stu-id="ebf11-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="ebf11-114">Preuzmite, deblokirajte i raspakujte [Paket podataka za podešavanje i konfiguraciju](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="ebf11-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="ebf11-115">Idite u fasciklu sa raspakovanim sadržajem i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ebf11-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ebf11-116">Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ebf11-118">Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ebf11-119">Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ebf11-120">Izaberite region vašeg zakupca, unesite svoje akreditive, pa izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ebf11-122">Na 3. stranici, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="ebf11-123">Na 4. stranici, izaberite zip datoteku *SampleSetupAndConfigData* iz raspakovane fascikle.</span><span class="sxs-lookup"><span data-stu-id="ebf11-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Izbor zip datoteke](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. <span data-ttu-id="ebf11-126">Kada izaberete zip datoteku, izaberite **Uvoz podataka**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-126">After the zip file is selected, select **Import Data**.</span></span>

![Uvezi podatke](./media/5ImportData.png)

10. <span data-ttu-id="ebf11-128">Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="ebf11-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ebf11-129">Po završetku uvoza, izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="ebf11-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ebf11-130">Potražite u svojoj organizaciji podatke za sledećih 26 entiteta:</span><span class="sxs-lookup"><span data-stu-id="ebf11-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="ebf11-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="ebf11-131">Currency</span></span>
  - <span data-ttu-id="ebf11-132">Grafikon poslovnih kontakata</span><span class="sxs-lookup"><span data-stu-id="ebf11-132">Chart of Accounts</span></span>
  - <span data-ttu-id="ebf11-133">Fiskalni kalendar</span><span class="sxs-lookup"><span data-stu-id="ebf11-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="ebf11-134">Vrste deviznih kurseva valuta</span><span class="sxs-lookup"><span data-stu-id="ebf11-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="ebf11-135">Dan za plaćanje</span><span class="sxs-lookup"><span data-stu-id="ebf11-135">Payment Day</span></span>
  - <span data-ttu-id="ebf11-136">Raspored plaćanja</span><span class="sxs-lookup"><span data-stu-id="ebf11-136">Payment Schedule</span></span>
  - <span data-ttu-id="ebf11-137">Uslovi plaćanja</span><span class="sxs-lookup"><span data-stu-id="ebf11-137">Payment Term</span></span>
  - <span data-ttu-id="ebf11-138">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="ebf11-138">Organizational Unit</span></span>
  - <span data-ttu-id="ebf11-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="ebf11-139">Contact</span></span>
  - <span data-ttu-id="ebf11-140">Poreska grupa</span><span class="sxs-lookup"><span data-stu-id="ebf11-140">Tax Group</span></span>
  - <span data-ttu-id="ebf11-141">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="ebf11-141">Customer Group</span></span>
  - <span data-ttu-id="ebf11-142">Grupa prodavaca</span><span class="sxs-lookup"><span data-stu-id="ebf11-142">Vendor Group</span></span>
  - <span data-ttu-id="ebf11-143">Jedinica</span><span class="sxs-lookup"><span data-stu-id="ebf11-143">Unit</span></span>
  - <span data-ttu-id="ebf11-144">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="ebf11-144">Unit Group</span></span>
  - <span data-ttu-id="ebf11-145">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="ebf11-145">Price List</span></span>
  - <span data-ttu-id="ebf11-146">Cenovnik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="ebf11-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="ebf11-147">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="ebf11-147">Invoice Frequency</span></span>
  - <span data-ttu-id="ebf11-148">Kategorija resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ebf11-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="ebf11-149">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="ebf11-149">Transaction Category</span></span>
  - <span data-ttu-id="ebf11-150">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="ebf11-150">Expense Category</span></span>
  - <span data-ttu-id="ebf11-151">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="ebf11-151">Role Price</span></span>
  - <span data-ttu-id="ebf11-152">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="ebf11-152">Transaction Category Price</span></span>
  - <span data-ttu-id="ebf11-153">Karakteristika</span><span class="sxs-lookup"><span data-stu-id="ebf11-153">Characteristic</span></span>
  - <span data-ttu-id="ebf11-154">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ebf11-154">Bookable Resource</span></span>
  - <span data-ttu-id="ebf11-155">Povezivanje kategorije resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ebf11-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="ebf11-156">Karakteristika resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="ebf11-156">Bookable Resource Characteristic</span></span>

![Kompletan uvoz](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="ebf11-158">Ažuriranje Project Operations konfiguracije</span><span class="sxs-lookup"><span data-stu-id="ebf11-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="ebf11-159">Idite u CE okruženje.</span><span class="sxs-lookup"><span data-stu-id="ebf11-159">Navigate to the CE environment.</span></span> <span data-ttu-id="ebf11-160">Možete ga pronaći ako otvorite [Power Platform centar administracije](https://admin.powerplatform.microsoft.com/environments), izaberete okruženje, a zatim izaberete **Otvoreno okruženje**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvoreno okruženje](./media/7OpenEnvironment.png)

2. <span data-ttu-id="ebf11-162">Idite na **Projekti** > **Resursi**, a zatim izaberite **Novo** da biste kreirali resurs koji može da se rezerviše za vašeg korisnika.</span><span class="sxs-lookup"><span data-stu-id="ebf11-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Resursi koji mogu da se rezervišu](./media/8BookableResources.png)

3. <span data-ttu-id="ebf11-164">Na kartici **Opšti podaci** izaberite svog administratora.</span><span class="sxs-lookup"><span data-stu-id="ebf11-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="ebf11-165">Proverite da li se vremenska zona podudara sa onom u kojoj se nalazite.</span><span class="sxs-lookup"><span data-stu-id="ebf11-165">Verify that the time zone matches the one you are in.</span></span> 

![Novi resurs koji može da se rezerviše](./media/9NewBookableResource.png)

4. <span data-ttu-id="ebf11-167">Na kartici **Zakazivanje**, u polju **Kompanija** odaberite kompaniju **USPM**, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Kartica „Zakazivanje“](./media/10SchedulingTab.png)

5. <span data-ttu-id="ebf11-169">Izaberite karticu **Radno vreme**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-169">Select the **Work hours** tab.</span></span>  

![Radno vreme](./media/11WorkHours.png)

6. <span data-ttu-id="ebf11-171">Dvaput kliknite bilo koju vrednost u kalendaru i izaberite **Uređivanje** > **Svi događaji u seriji**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalendar posla](./media/12WorkCalendar.png)

7. <span data-ttu-id="ebf11-173">Promenite radno vreme u radni dan od osam (8) sati, obeležite vikende kao neradne dane i uverite se da vremenska zona odgovara vašoj.</span><span class="sxs-lookup"><span data-stu-id="ebf11-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="ebf11-174">Izaberite stavku **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-174">Select **Save and close**.</span></span>

![Ažuriranje kalendara](./media/13UpdateCalendar.png)

9. <span data-ttu-id="ebf11-176">Idite na **Podešavanja** > **Predlošci kalendara** i izaberite **Novi**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Predlošci kalendara](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="ebf11-178">Unesite naziv, izaberite resurs šablona koji ste kreirali, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Čuvanje predloška kalendara](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="ebf11-180">Idite na **Parametri** i dvaput kliknite na zapis.</span><span class="sxs-lookup"><span data-stu-id="ebf11-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametri projekta](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="ebf11-182">Ažurirajte sledeća polja:</span><span class="sxs-lookup"><span data-stu-id="ebf11-182">Update the following fields:</span></span>

 - <span data-ttu-id="ebf11-183">**Podrazumevana kompanija**: USPM</span><span class="sxs-lookup"><span data-stu-id="ebf11-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="ebf11-184">**Podrazumevana organizaciona jedinica**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="ebf11-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="ebf11-185">**Učestalost fakturisanja**: Sedmi i poslednji dan</span><span class="sxs-lookup"><span data-stu-id="ebf11-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="ebf11-186">**Predložak radnog vremena**: Promenite na predložak koji ste kreirali.</span><span class="sxs-lookup"><span data-stu-id="ebf11-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="ebf11-187">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ebf11-187">Select **Save**.</span></span> 

![Ažurirani parametri projekta](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
