---
title: Uvoz i održavanje transakcija kreditnim karticama
description: Ova tema objašnjava kako da uvedete i održavate transakcije kreditne kartice povezane sa troškovima. Ove transakcije se mogu podesiti tako da se automatski uvoze po redovnom rasporedu ili se mogu ručno uvesti po potrebi.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005178"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="7d62f-104">Uvoz i održavanje transakcija kreditnim karticama</span><span class="sxs-lookup"><span data-stu-id="7d62f-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="7d62f-105">Transakcije povezane sa troškovima kreditne kartice mogu se podesiti tako da se automatski uvoze po redovnom rasporedu.</span><span class="sxs-lookup"><span data-stu-id="7d62f-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="7d62f-106">Osim toga, transakcije se mogu ručno uvesti po potrebi.</span><span class="sxs-lookup"><span data-stu-id="7d62f-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="7d62f-107">Transakcije kreditnom karticom se uvoze preko entiteta podataka transakcija kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="7d62f-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="7d62f-108">Za više informacija o entitetima podataka pogledajte [Entiteti podataka](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span><span class="sxs-lookup"><span data-stu-id="7d62f-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="7d62f-109">Uvoz transakcija kreditnom karticom</span><span class="sxs-lookup"><span data-stu-id="7d62f-109">Import credit card transactions</span></span>

1. <span data-ttu-id="7d62f-110">Na stranici **Transakcije kreditnim karticama** izaberite **Uvezi transakcije**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="7d62f-111">Ako prvi put otvarate upravljanje podacima, sistem mora da ažurira listu entiteta podataka pre nego što možete da nastavite.</span><span class="sxs-lookup"><span data-stu-id="7d62f-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="7d62f-112">U polju **Naziv** unesite jedinstveni opis posla uvoza.</span><span class="sxs-lookup"><span data-stu-id="7d62f-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="7d62f-113">U polju **Format izvornih podataka** izaberite format datoteke koja sadrži transakcije kreditnom karticom za uvoz.</span><span class="sxs-lookup"><span data-stu-id="7d62f-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="7d62f-114">Izaberite **Otpremi**, a zatim pronađite i izaberite datoteku za uvoz.</span><span class="sxs-lookup"><span data-stu-id="7d62f-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="7d62f-115">Nakon što je datoteka otpremljena, potvrdite mapiranje datoteke transakcije kreditne kartice i kolona entiteta podataka transakcija kreditnom karticom izborom veze **Prikaži mapu** na pločici.</span><span class="sxs-lookup"><span data-stu-id="7d62f-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="7d62f-116">Ako postoje greške u mapiranju ili ako morate da promenite mapiranje, napravite promene u mapiranju sa kartice **Vizuelizacija mapiranja** ili **Detalji mapiranja**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="7d62f-117">Da biste automatizovali transakcije kreditnom karticom, izaberite **Kreiraj periodičan posao sa podacima**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="7d62f-118">Zatim možete podesiti ponavljanje koje definiše koliko često treba uvoziti transakcije kreditnim karticama.</span><span class="sxs-lookup"><span data-stu-id="7d62f-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="7d62f-119">Kada završite, izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="7d62f-120">Da biste sada uvezli izabranu datoteku, izaberite **Uvezi**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="7d62f-121">Ako se tokom uvoza pojave greške, možete pregledati evidenciju izvršenja ili podatke o pripremi da biste videli greške koje morate ispraviti da biste garantovali uspešan uvoz.</span><span class="sxs-lookup"><span data-stu-id="7d62f-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="7d62f-122">Ako morate uvesti više od jednog formata datoteke, morate stvoriti zasebne poslove uvoza za svaki tip formata.</span><span class="sxs-lookup"><span data-stu-id="7d62f-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="7d62f-123">Ponovo dodelite transakcije kreditnom karticom otkazanim zaposlenima</span><span class="sxs-lookup"><span data-stu-id="7d62f-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="7d62f-124">Nakon ukidanja evidencije zaposlenog, onemogućen je njegov Active Directory Domain Services (AD DS) nalog.</span><span class="sxs-lookup"><span data-stu-id="7d62f-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="7d62f-125">Međutim, možda postoje aktivne transakcije kreditnim karticama koje se i dalje moraju trošiti i nadoknaditi.</span><span class="sxs-lookup"><span data-stu-id="7d62f-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="7d62f-126">Na stranici **Transakcije kreditnim karticama** možete dodeliti zaposlenog bilo kojoj transakciji kreditnom karticom za koju je povezani zaposleni ukinut.</span><span class="sxs-lookup"><span data-stu-id="7d62f-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="7d62f-127">Izaberite jednu ili više transakcija kreditnom karticom, a zatim izaberite **Ponovo dodelite transakcije**.</span><span class="sxs-lookup"><span data-stu-id="7d62f-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="7d62f-128">Zatim možete da izaberete drugog zaposlenog kome ćete dodeliti transakcije kreditnom karticom.</span><span class="sxs-lookup"><span data-stu-id="7d62f-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="7d62f-129">Nakon što se transakcije sa kreditnom karticom prerasporede, mogu se odabrati za izveštaj o troškovima i platiti kroz uobičajeni postupak za nadoknadu troškova.</span><span class="sxs-lookup"><span data-stu-id="7d62f-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]