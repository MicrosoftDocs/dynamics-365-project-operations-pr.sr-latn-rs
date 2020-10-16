---
title: Primena demo podešavanja i podataka o konfiguraciji
description: Ova tema pruža informacije o tome kako da primenite demo podešavanja i podatke o konfiguraciji za Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949047"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="7ce83-103">Primenite demo podešavanja i podatke o konfiguraciji za jednostavnu primenu usluge Project Operations – od pogodbe do profakture</span><span class="sxs-lookup"><span data-stu-id="7ce83-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="7ce83-104">_\*\*Jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="7ce83-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="7ce83-105">Preuzmite [Paket glavnih podataka](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="7ce83-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="7ce83-106">Idite u fasciklu *ProjOpsDemoDataSetupAndMaster - Integrated CMT* i pokrenite izvršnu datoteku *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7ce83-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7ce83-107">Na 1. stranici Common Data Service čarobnjaka za konfigurisanje migracije (CMT) izaberite **Uvezi podatke**, a zatim izaberite **Nastavi**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migracija konfiguracije](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7ce83-109">Na 2. stranici CMT čarobnjaka izaberite **Office 365** kao **Tip primene**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7ce83-110">Izaberite polja za potvrdu **Prikaži listu dostupnih organizacija** i **Prikaži napredno**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7ce83-111">Izaberite region vašeg zakupca, unesite svoje akreditive, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prijavljivanje u konfiguraciju](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7ce83-113">Na stranici 3, sa liste organizacija u zakupcu, izaberite u koju organizaciju želite da uvezete demo podatke, a zatim izaberite **Prijavljivanje**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="7ce83-114">Na 4. stranici izaberite zip datoteku *MasterAndSetupData* iz raspakovane fascikle *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="7ce83-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Komprimovana datoteka](./media/3ZipFile.png)

![Izbor datoteke](./media/4SelectAFile.png)

9. <span data-ttu-id="7ce83-117">Kada izaberete zip datoteku, izaberite **Uvoz podataka**.</span><span class="sxs-lookup"><span data-stu-id="7ce83-117">After the zip file is selected, select **Import Data**.</span></span>

![Uvoz podataka](./media/5ImportData.png)

10. <span data-ttu-id="7ce83-119">Uvoz će trajati otprilike od dva do deset minuta, u zavisnosti od brzine vaše mreže.</span><span class="sxs-lookup"><span data-stu-id="7ce83-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7ce83-120">Po završetku izađite iz CMT čarobnjaka.</span><span class="sxs-lookup"><span data-stu-id="7ce83-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7ce83-121">Potražite u svojoj organizaciji podatke za sledećih 20 entiteta:</span><span class="sxs-lookup"><span data-stu-id="7ce83-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="7ce83-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="7ce83-122">Currency</span></span>
- <span data-ttu-id="7ce83-123">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="7ce83-123">Organizational Unit</span></span>
- <span data-ttu-id="7ce83-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7ce83-124">Contact</span></span>
- <span data-ttu-id="7ce83-125">Poreska grupa</span><span class="sxs-lookup"><span data-stu-id="7ce83-125">Tax Group</span></span>
- <span data-ttu-id="7ce83-126">Grupa klijenata</span><span class="sxs-lookup"><span data-stu-id="7ce83-126">Customer Group</span></span>
- <span data-ttu-id="7ce83-127">Jedinica</span><span class="sxs-lookup"><span data-stu-id="7ce83-127">Unit</span></span>
- <span data-ttu-id="7ce83-128">Grupa jedinica</span><span class="sxs-lookup"><span data-stu-id="7ce83-128">Unit Group</span></span>
- <span data-ttu-id="7ce83-129">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="7ce83-129">Price List</span></span>
- <span data-ttu-id="7ce83-130">Cenovnik parametara projekta</span><span class="sxs-lookup"><span data-stu-id="7ce83-130">Project Parameter Price List</span></span>
- <span data-ttu-id="7ce83-131">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="7ce83-131">Invoice Frequency</span></span>
- <span data-ttu-id="7ce83-132">Detalj o učestalosti fakturisanja</span><span class="sxs-lookup"><span data-stu-id="7ce83-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="7ce83-133">Kategorija resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="7ce83-133">Bookable Resource Category</span></span>
- <span data-ttu-id="7ce83-134">Kategorija transakcije</span><span class="sxs-lookup"><span data-stu-id="7ce83-134">Transaction Category</span></span>
- <span data-ttu-id="7ce83-135">Kategorija troška</span><span class="sxs-lookup"><span data-stu-id="7ce83-135">Expense Category</span></span>
- <span data-ttu-id="7ce83-136">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="7ce83-136">Role Price</span></span>
- <span data-ttu-id="7ce83-137">Cena kategorije transakcije</span><span class="sxs-lookup"><span data-stu-id="7ce83-137">Transaction Category Price</span></span>
- <span data-ttu-id="7ce83-138">Karakteristika</span><span class="sxs-lookup"><span data-stu-id="7ce83-138">Characteristic</span></span>
- <span data-ttu-id="7ce83-139">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="7ce83-139">Bookable Resource</span></span>
- <span data-ttu-id="7ce83-140">Povezivanje kategorije resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="7ce83-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="7ce83-141">Karakteristika resursa koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="7ce83-141">Bookable Resource Characteristic</span></span>

![Kompletan uvoz](./media/6CompleteImport.png)
