---
title: Primena demo podataka na Finance okruženje koje se hostuje u oblaku
description: Ova tema objašnjava kako da primenite demo podatke iz usluge Project Operations na Dynamics 365 Finance okruženje hostovano u oblaku.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365255"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="f81dc-103">Primena demo podataka na Finance okruženje koje se hostuje u oblaku</span><span class="sxs-lookup"><span data-stu-id="f81dc-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="f81dc-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="f81dc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f81dc-105">Ova tema je primenljiva je samo na Microsoft Dynamics 365 Finance verzije 10.0.13 i može se izvoditi samo u okruženju koje se hostuje u oblaku.</span><span class="sxs-lookup"><span data-stu-id="f81dc-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="f81dc-106">Dovršite korake u ovoj temi **PRE NEGO ŠTO** primenite ispravke kvaliteta na okruženje.</span><span class="sxs-lookup"><span data-stu-id="f81dc-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="f81dc-107">U svom LCS projektu, otvorite stranicu **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="f81dc-108">Primetite da sadrži detalje potrebne za povezivanje sa okolinom pomoću protokola udaljene radne površine (RDP).</span><span class="sxs-lookup"><span data-stu-id="f81dc-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Detalji  okruženja](./media/1EnvironmentDetails.png)

<span data-ttu-id="f81dc-110">Prvi skup istaknutih akreditiva su akreditivi lokalnog naloga i sadrže hipervezu do veze sa udaljenom radnom površinom.</span><span class="sxs-lookup"><span data-stu-id="f81dc-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="f81dc-111">Akreditivi uključuju korisničko ime i lozinku administratora okruženja.</span><span class="sxs-lookup"><span data-stu-id="f81dc-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="f81dc-112">Drugi skup akreditiva se koristi za prijavljivanje na SQL Server u ovom okruženju.</span><span class="sxs-lookup"><span data-stu-id="f81dc-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="f81dc-113">Povežite se udaljeno sa okruženjem koristeći hipervezu u odeljku **Lokalni nalozi** i upotrebite **Akreditivi za lokalni nalog** za potvrdu identiteta.</span><span class="sxs-lookup"><span data-stu-id="f81dc-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="f81dc-114">Idite na **Internet Information Services** > **Grupe aplikacija** > **AOSService** i zaustavite uslugu.</span><span class="sxs-lookup"><span data-stu-id="f81dc-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="f81dc-115">U ovom trenutku zaustavljate uslugu da biste mogli da nastavite da zamenjujete SQL bazu podataka.</span><span class="sxs-lookup"><span data-stu-id="f81dc-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zaustavljanje AOS](./media/2StopAOS.png)

4. <span data-ttu-id="f81dc-117">Idite na **Usluge** i zaustavite sledeće dve stavke:</span><span class="sxs-lookup"><span data-stu-id="f81dc-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="f81dc-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span><span class="sxs-lookup"><span data-stu-id="f81dc-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="f81dc-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span><span class="sxs-lookup"><span data-stu-id="f81dc-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zaustavljanje usluga](./media/3StopServices.png)

5. <span data-ttu-id="f81dc-121">Otvorite Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="f81dc-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="f81dc-122">Prijavite se pomoću akreditiva za SQL Server i koristite korisnika axdbadmin i lozinku sa LCS stranice **Detalji okruženja**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="f81dc-124">U pregledaču objekata, izaberite **Baze podataka** i pronađite **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="f81dc-125">Bazu podataka ćete zameniti novom bazom podataka koja se nalazi u [centru za preuzimanje](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="f81dc-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="f81dc-126">Kopirajte zip datoteku u VM u koji ste udaljeno povezani i raspakujte zip sadržaj.</span><span class="sxs-lookup"><span data-stu-id="f81dc-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="f81dc-127">U programu SQL Server Management Studio kliknite desnim tasterom miša na **AxDB**, a zatim izaberite **Zadaci** > **Vraćanje** > **Baza podataka**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Vraćanje baze podataka](./media/5RestoreDatabase.png)

9. <span data-ttu-id="f81dc-129">Izaberite **Izvorni uređaj** i dođite do datoteke izvučene iz zip datoteke koju ste kopirali.</span><span class="sxs-lookup"><span data-stu-id="f81dc-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Izvorni uređaji](./media/6SourceDevice.png)

10. <span data-ttu-id="f81dc-131">Izaberite **Opcije**, a zatim izaberite **Prepiši postojeću bazu podataka** i **Zatvorite postojeće veze sa odredišnom bazom podataka**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="f81dc-132">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-132">Select **OK**.</span></span>

![Vraćanje podešavanja](./media/7RestoreSetting.png)

<span data-ttu-id="f81dc-134">Dobićete potvrdu da je vraćanje AXDB bilo uspešno.</span><span class="sxs-lookup"><span data-stu-id="f81dc-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="f81dc-135">Kada dobijete ovu potvrdu, možete da zatvorite SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="f81dc-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="f81dc-136">Vratite se na **Internet Information Services** > **Grupe aplikacija** > **AOSService** i pokrenite uslugu AOSService.</span><span class="sxs-lookup"><span data-stu-id="f81dc-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="f81dc-137">Idite na **Usluge** i pokrenite dve usluge koje ste ranije zaustavili.</span><span class="sxs-lookup"><span data-stu-id="f81dc-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="f81dc-138">Pronađite alatku AdminUserProvisioning na ovom VM-u.</span><span class="sxs-lookup"><span data-stu-id="f81dc-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="f81dc-139">Potražite K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="f81dc-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="f81dc-140">Pokrenite .ext datoteku koristeći svoju korisničku adresu u polju **Adresa e-pošte**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="f81dc-141">Izaberite **Prosledi**.</span><span class="sxs-lookup"><span data-stu-id="f81dc-141">Select **Submit**.</span></span>

![Obezbeđivanje korisnika-administratora](./media/8AdminUserProvisioning.png)

<span data-ttu-id="f81dc-143">Za ovo je potrebno nekoliko minuta.</span><span class="sxs-lookup"><span data-stu-id="f81dc-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="f81dc-144">Trebalo bi da primite poruku sa potvrdom da je korisnik-administrator uspešno ažuriran.</span><span class="sxs-lookup"><span data-stu-id="f81dc-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="f81dc-145">Na kraju, pokrenite komandnu liniju kao administrator i pokrenite komandu iisreset</span><span class="sxs-lookup"><span data-stu-id="f81dc-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Resetovanje IIS](./media/9IISReset.png)

18. <span data-ttu-id="f81dc-147">Zatvorite sesiju udaljene radne površine i koristite stranicu LCS **Detalji okruženja** da biste se prijavili u okruženje i potvrdili da radi kao što se očekuje.</span><span class="sxs-lookup"><span data-stu-id="f81dc-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
