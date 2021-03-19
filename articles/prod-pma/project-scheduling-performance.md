---
title: Performanse planiranja resursa za projekat
description: Ova tema pruža informacije o tome kako poboljšati performanse planiranja resursa za veliki broj projekata.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289026"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="577e8-103">Performanse planiranja resursa za projekat</span><span class="sxs-lookup"><span data-stu-id="577e8-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="577e8-104">Problemi sa učinkom koji se odnose na planiranje resursa mogu se pojaviti kada broj projekata dostigne više hiljada.</span><span class="sxs-lookup"><span data-stu-id="577e8-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="577e8-105">Da bi se poboljšale performanse planiranja resursa, dostupna je funkcija koja omogućava korisnicima da smanje vreme potrebno za pokretanje obrasca dostupnosti resursa.</span><span class="sxs-lookup"><span data-stu-id="577e8-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="577e8-106">Konkretno, ovo uklanja postupak zbirne sinhronizacije kapaciteta resursa i koristi tabelu **ResProjectResource** za ubrzanje pretraživanja resursa.</span><span class="sxs-lookup"><span data-stu-id="577e8-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="577e8-107">Imajte na umu da se tabela **ResRollup** više neće koristiti.</span><span class="sxs-lookup"><span data-stu-id="577e8-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="577e8-108">Ako postoji zavisnost ili postupka zbirne sinhronizacije kapaciteta resursa ili tabele **ResProjectResource**, nemojte koristiti ovu funkciju.</span><span class="sxs-lookup"><span data-stu-id="577e8-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="577e8-109">Omogućite poboljšanje performansi planiranja resursa</span><span class="sxs-lookup"><span data-stu-id="577e8-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="577e8-110">Da biste omogućili poboljšanje performansi planiranja resursa, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="577e8-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="577e8-111">Idite na **Upravljanje funkcijama** > **Sve**, a na listi funkcija pronađite **Omogući funkciju poboljšanja performansi planiranja resursa projekta**.</span><span class="sxs-lookup"><span data-stu-id="577e8-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="577e8-112">Izaberite dugme **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="577e8-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="577e8-113">Ako ne možete da pronađete funkciju na listi, izaberite **Proveri da li ima ažuriranja** da biste osvežili listu.</span><span class="sxs-lookup"><span data-stu-id="577e8-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="577e8-114">Osvežite pregledač, a zatim idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Resursi projekta** > **Sinhronizujte kapacitet kalendara resursa u svim kompanijama**.</span><span class="sxs-lookup"><span data-stu-id="577e8-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="577e8-115">Podesite **Uklonite postojeće evidencije o kapacitetu** na **Da** da biste uklonili prethodne podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="577e8-116">Ako želite da generišete inkrementalne podatke, podesite ga na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="577e8-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="577e8-117">U polju **Šifra perioda**, izaberite period u kojem treba generisati podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="577e8-118">Ako izaberete šifru perioda, datumi početka i završetka ne moraju biti definisani.</span><span class="sxs-lookup"><span data-stu-id="577e8-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="577e8-119">Ako ostavite polje **Šifra perioda** prazno, odaberite određene datume početka i završetka da biste generisali podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="577e8-120">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="577e8-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="577e8-121">Ovo će distribuirati opšte podatke u tabeli **ResCalendarCapacity** u svim kompanijama u vašem okruženju, tako da grupni posao treba pokrenuti samo u jednom pravnom licu.</span><span class="sxs-lookup"><span data-stu-id="577e8-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="577e8-122">Podaci u ovom grupnom poslu potrebni su za izračunavanje kapaciteta resursa kroz pridruženi kalendar.</span><span class="sxs-lookup"><span data-stu-id="577e8-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="577e8-123">Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Resursi projekta** > **Popunite projektne resurse u svim kompanijama**, a zatim izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="577e8-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="577e8-124">Ovo je skripta za nadogradnju podataka za opšte podatke u tabelama **ResProjectResource**, **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="577e8-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="577e8-125">Vrednosti za polje **PSAPRojSchedRole.RootActivity** takođe se ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="577e8-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="577e8-126">Ako se ovo ne pokrene, primićete upozorenje kada pokušate da izvršite operacije planiranja resursa.</span><span class="sxs-lookup"><span data-stu-id="577e8-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="577e8-127">Isključite poboljšanje performansi planiranja resursa</span><span class="sxs-lookup"><span data-stu-id="577e8-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="577e8-128">Idite na **Upravljanje funkcijama** > **Sve**, pa potražite **Omogući funkciju poboljšanja performansi planiranja resursa projekta**.</span><span class="sxs-lookup"><span data-stu-id="577e8-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="577e8-129">Izaberite funkciju, a zatim odaberite dugme **Onemogući**.</span><span class="sxs-lookup"><span data-stu-id="577e8-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="577e8-130">Osvežite pregledač.</span><span class="sxs-lookup"><span data-stu-id="577e8-130">Refresh your browser.</span></span>
4. <span data-ttu-id="577e8-131">Idite na **Upravljanje projektima i računovodstvo** > **Periodično** > **Sinhronizacija kapaciteta** > **Sinhronizuj zbirne vrednosti kapaciteta resursa**.</span><span class="sxs-lookup"><span data-stu-id="577e8-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="577e8-132">Na stranici **Zbirna sinhronizacija kapaciteta** podesite **Ukloni postojeće evidencije o kapacitetu** na **Da** kako biste uklonili prethodne podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="577e8-133">Ako želite da generišete inkrementalne podatke, podesite ga na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="577e8-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="577e8-134">U polju **Šifra perioda**, izaberite period u kojem treba generisati podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="577e8-135">Ako izaberete šifru perioda, datumi početka i završetka ne moraju biti definisani.</span><span class="sxs-lookup"><span data-stu-id="577e8-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="577e8-136">Ako ostavite polje **Šifra perioda** prazno, odaberite određene datume početka i završetka da biste generisali podatke.</span><span class="sxs-lookup"><span data-stu-id="577e8-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="577e8-137">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="577e8-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="577e8-138">Ovo će distribuirati opšte podatke u tabeli **ResRollup** u svim kompanijama u vašem okruženju, tako da grupni posao treba pokrenuti samo u jednom pravnom licu.</span><span class="sxs-lookup"><span data-stu-id="577e8-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="577e8-139">Ovaj grupni posao potreban je svim prikazima **Dostupnost resursa**.</span><span class="sxs-lookup"><span data-stu-id="577e8-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="577e8-140">Ako se ovaj grupni posao ne pokrene, **ResRollup** podaci će se generisati u hodu, što može potrajati.</span><span class="sxs-lookup"><span data-stu-id="577e8-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]