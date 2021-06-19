---
title: Podešavanje integracije kreditne kartice
description: Ova tema objašnjava kako se radi sa transakcijama kreditnom karticom povezanim sa troškovima.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3555e894e206c2aafb30b0df1e52efadd69b0713
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001847"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="de71a-103">Podešavanje integracije kreditne kartice</span><span class="sxs-lookup"><span data-stu-id="de71a-103">Set up credit card integration</span></span>

<span data-ttu-id="de71a-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="de71a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="de71a-105">Transakcije povezane sa troškovima kreditne kartice mogu se podesiti tako da se automatski uvoze po redovnom rasporedu.</span><span class="sxs-lookup"><span data-stu-id="de71a-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="de71a-106">Osim toga, transakcije se mogu ručno uvesti po potrebi.</span><span class="sxs-lookup"><span data-stu-id="de71a-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="de71a-107">Transakcije kreditnom karticom se uvoze preko entiteta podataka transakcija kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="de71a-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="de71a-108">Uvoz transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="de71a-108">Import credit card transactions</span></span>

<span data-ttu-id="de71a-109">Da biste uvezli transakcije kreditnom karticom, sledite ove korake:</span><span class="sxs-lookup"><span data-stu-id="de71a-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="de71a-110">Na stranici **Transakcije kreditnim karticama** izaberite **Uvezi transakcije**.</span><span class="sxs-lookup"><span data-stu-id="de71a-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="de71a-111">Ako prvi put otvarate upravljanje podacima, sistem mora da ažurira listu entiteta podataka pre nego što možete da nastavite.</span><span class="sxs-lookup"><span data-stu-id="de71a-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="de71a-112">U polje **Naziv** unesite jedinstveni opis posla uvoza.</span><span class="sxs-lookup"><span data-stu-id="de71a-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="de71a-113">U polju **Format izvornih podataka** izaberite format datoteke koja sadrži transakcije kreditnom karticom za uvoz.</span><span class="sxs-lookup"><span data-stu-id="de71a-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="de71a-114">Izaberite **Otpremi**, a zatim pronađite i izaberite datoteku za uvoz.</span><span class="sxs-lookup"><span data-stu-id="de71a-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="de71a-115">Kada otpremite datoteku, potvrdite mapiranje datoteke transakcije kreditne kartice i kolone entiteta podataka transakcija kreditnom karticom izborom veze **Prikaži mapu** na pločici.</span><span class="sxs-lookup"><span data-stu-id="de71a-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="de71a-116">Ako postoje greške u mapiranju ili ako morate da promenite mapiranje, napravite promene u mapiranju sa kartice **Vizuelizacija mapiranja** ili **Detalji mapiranja**.</span><span class="sxs-lookup"><span data-stu-id="de71a-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="de71a-117">Da biste automatizovali transakcije kreditnom karticom, izaberite **Kreiraj periodičan posao sa podacima**.</span><span class="sxs-lookup"><span data-stu-id="de71a-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="de71a-118">Zatim možete podesiti ponavljanje koje definiše koliko često treba uvoziti transakcije kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="de71a-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="de71a-119">Kada završite, izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="de71a-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="de71a-120">Da biste sada uvezli izabranu datoteku, izaberite **Uvezi**.</span><span class="sxs-lookup"><span data-stu-id="de71a-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="de71a-121">Ako se tokom uvoza pojave greške, možete pregledati evidenciju izvršenja ili pripremne podatke da biste videli greške koje morate ispraviti da biste obezbedili uspešan uvoz.</span><span class="sxs-lookup"><span data-stu-id="de71a-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="de71a-122">Ako treba da uvezete više od jednog formata datoteke, morate kreirati zasebne poslove uvoza za svaki tip formata.</span><span class="sxs-lookup"><span data-stu-id="de71a-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="de71a-123">Ponovo dodelite transakcije kreditnom karticom otkazanim zaposlenima</span><span class="sxs-lookup"><span data-stu-id="de71a-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="de71a-124">Nakon ukidanja evidencije zaposlenog, onemogućen je njegov Active Directory Domain Services (AD DS) nalog.</span><span class="sxs-lookup"><span data-stu-id="de71a-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="de71a-125">Međutim, možda postoje aktivne transakcije kreditnim karticama koje se i dalje moraju trošiti i nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="de71a-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="de71a-126">Na stranici **Transakcije kreditnim karticama** možete ponovo dodeliti zaposlenog za bilo koju transakciju kreditnom karticom u kojoj je povezani zaposleni prekinut.</span><span class="sxs-lookup"><span data-stu-id="de71a-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="de71a-127">Izaberite jednu ili više transakcija kreditnom karticom, a zatim izaberite **Ponovo dodelite transakcije**.</span><span class="sxs-lookup"><span data-stu-id="de71a-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="de71a-128">Zatim možete da izaberete drugog zaposlenog kome ćete dodeliti transakcije kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="de71a-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="de71a-129">Nakon što se transakcije sa kreditnom karticom prerasporede, mogu se odabrati za izveštaj o troškovima i platiti kroz uobičajeni postupak za nadoknadu troškova.</span><span class="sxs-lookup"><span data-stu-id="de71a-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="de71a-130">Brisanje transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="de71a-130">Delete credit card transactions</span></span> 

<span data-ttu-id="de71a-131">Ponekad, nakon uvoza transakcija kreditnom karticom, određene transakcije možda treba izbrisati.</span><span class="sxs-lookup"><span data-stu-id="de71a-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="de71a-132">To je možda zato što su transakcije duplikati ili što podaci možda nisu tačni.</span><span class="sxs-lookup"><span data-stu-id="de71a-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="de71a-133">Administratori mogu da koriste funkciju **„Brisanje transakcija kreditnom karticom“** za odabir i brisanje transakcija kreditnom karticom koje **nisu priložene** na izveštaj o troškovima.</span><span class="sxs-lookup"><span data-stu-id="de71a-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="de71a-134">Idite na stranicu **Periodični zadaci** > **Brisanje transakcija kreditnom karticom**.</span><span class="sxs-lookup"><span data-stu-id="de71a-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="de71a-135">Izaberite **Filter** i navedite informacije za identifikaciju zapisa koje treba uključiti.</span><span class="sxs-lookup"><span data-stu-id="de71a-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="de71a-136">Izaberite **U redu** da biste izbrisali zapise.</span><span class="sxs-lookup"><span data-stu-id="de71a-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
