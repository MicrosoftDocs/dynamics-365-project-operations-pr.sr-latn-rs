---
title: Primena demo podešavanja i podataka o konfiguraciji – jednostavno
description: Ova tema pruža informacije o tome kako da primenite demo podešavanja i podatke o konfiguraciji za Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997168"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="13507-103">Primena demo podešavanja i podataka o konfiguraciji za Project Operations – jednostavno</span><span class="sxs-lookup"><span data-stu-id="13507-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="13507-104">_\*\*Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="13507-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="13507-105">Preduslovi</span><span class="sxs-lookup"><span data-stu-id="13507-105">Prerequisites</span></span>

<span data-ttu-id="13507-106">Pre nego što započnete konfiguraciju, morate imati Common Data Service (CDS) okruženje predviđeno za Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="13507-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="13507-107">Uputstva</span><span class="sxs-lookup"><span data-stu-id="13507-107">Instructions</span></span>

1. <span data-ttu-id="13507-108">Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="13507-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="13507-109">Dođite do fascikle *ProjOpsSampleSetupData - CE only CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="13507-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="13507-110">Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="13507-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="13507-112">Na 2. stranici CMT čarobnjaka izaberite **Microsoft 365** kao **Tip primene**.</span><span class="sxs-lookup"><span data-stu-id="13507-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="13507-113">Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="13507-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="13507-114">Izaberite region vašeg zakupca, unesite svoje akreditive, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="13507-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="13507-116">Na stranici 3, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="13507-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="13507-117">Na stranici 4 izaberite zip datoteku, *SampleSetupAndConfigData* iz raspakovane fascikle, *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="13507-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Komprimovana datoteka](./media/3ZipFile.png)

   ![Izaberite datoteku](./media/4SelectAFile.png)

9. <span data-ttu-id="13507-120">Kada izaberete zip datoteku, izaberite **Uvoz podataka**.</span><span class="sxs-lookup"><span data-stu-id="13507-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="13507-122">Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="13507-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="13507-123">Po završetku izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="13507-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="13507-124">Potražite u svojoj organizaciji podatke za sledećih 18 entiteta:</span><span class="sxs-lookup"><span data-stu-id="13507-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="13507-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="13507-125">Currency</span></span>
    -   <span data-ttu-id="13507-126">Nalog</span><span class="sxs-lookup"><span data-stu-id="13507-126">Account</span></span>
    -   <span data-ttu-id="13507-127">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="13507-127">Organizational Unit</span></span>
    -   <span data-ttu-id="13507-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="13507-128">Contact</span></span>
    -   <span data-ttu-id="13507-129">Jedinica</span><span class="sxs-lookup"><span data-stu-id="13507-129">Unit</span></span>
    -   <span data-ttu-id="13507-130">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="13507-130">Unit Group</span></span>
    -   <span data-ttu-id="13507-131">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="13507-131">Price List</span></span>
    -   <span data-ttu-id="13507-132">Cenovnik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="13507-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="13507-133">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="13507-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="13507-134">Kategorija resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="13507-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="13507-135">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="13507-135">Transaction Category</span></span>
    -   <span data-ttu-id="13507-136">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="13507-136">Expense Category</span></span>
    -   <span data-ttu-id="13507-137">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="13507-137">Role Price</span></span>
    -   <span data-ttu-id="13507-138">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="13507-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="13507-139">Karakteristika</span><span class="sxs-lookup"><span data-stu-id="13507-139">Characteristic</span></span>
    -   <span data-ttu-id="13507-140">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="13507-140">Bookable Resource</span></span>
    -   <span data-ttu-id="13507-141">Povezivanje kategorije resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="13507-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="13507-142">Karakteristika resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="13507-142">Bookable Resource Characteristic</span></span>

    ![Kompletan uvoz](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
