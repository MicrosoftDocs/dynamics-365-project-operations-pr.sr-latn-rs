---
title: Kreiranje i potvrda dnevnika sa ispravkama
description: Ova tema pruža informacije o tome kako da kreirate i potvrdite dnevnik sa ispravkama.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 274f99527804b0db81b26201a22eb5a8cbe86c9a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896973"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="535ae-103">Kreiranje i potvrda dnevnika sa ispravkama</span><span class="sxs-lookup"><span data-stu-id="535ae-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="535ae-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="535ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="535ae-105">Povremeno se može pogrešno uneti stavka vremena ili troška.</span><span class="sxs-lookup"><span data-stu-id="535ae-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="535ae-106">Na primer, konsultant može da odabere pogrešan datum prilikom kreiranja stavke vremena ili može da prenese brojeve prilikom unosa troška.</span><span class="sxs-lookup"><span data-stu-id="535ae-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="535ae-107">Ako konsultant ne može da obavi ažuriranja prosleđenih stavki, administrator može direktno da ispravi stavku za projekat.</span><span class="sxs-lookup"><span data-stu-id="535ae-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="535ae-108">Da biste dovršili procedure u ovoj temi, trebaće vam dozvole administratora.</span><span class="sxs-lookup"><span data-stu-id="535ae-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="535ae-109">Ispravne odobrene stavke vremena</span><span class="sxs-lookup"><span data-stu-id="535ae-109">Correct approved time entries</span></span>     

<span data-ttu-id="535ae-110">Obavite sledeće korake da biste ispravili pojedinačne ili višestruke stavke za projekat.</span><span class="sxs-lookup"><span data-stu-id="535ae-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="535ae-111">U oblasti **Prodaja** izaberite **Transakcije**, a zatim izaberite **Odobreno vreme**.</span><span class="sxs-lookup"><span data-stu-id="535ae-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="535ae-112">Na listi **Odobreno vreme** pronađite i izaberite jednu odobrenu stavku vremena ili više njih da biste ih ispravili.</span><span class="sxs-lookup"><span data-stu-id="535ae-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="535ae-113">Možete koristiti filter da biste pronašli povezane stavke.</span><span class="sxs-lookup"><span data-stu-id="535ae-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="535ae-114">Na primer, možete da filtrirate ID projekta i da izaberete sve odobrene stavke vremena sa tim ID-om projekta.</span><span class="sxs-lookup"><span data-stu-id="535ae-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="535ae-115">Izaberite **Ispravi stavke**.</span><span class="sxs-lookup"><span data-stu-id="535ae-115">Select **Correct entries**.</span></span> <span data-ttu-id="535ae-116">Novi dnevnik ispravki se automatski kreira, sa dodeljenom vrstom **Ispravka vremena**.</span><span class="sxs-lookup"><span data-stu-id="535ae-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="535ae-117">Stake koje ste izabrali se dodaju u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="535ae-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="535ae-118">Na stranici **Nova glavna knjiga** unesite **Opis** za vaš dnevnik ispravki, a zatim izaberite karticu **Ispravke stavki vremena**.</span><span class="sxs-lookup"><span data-stu-id="535ae-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="535ae-119">U odeljku **Nove vrednosti za stavke vremena** po potrebi ažurirajte polja ispravnim informacijama.</span><span class="sxs-lookup"><span data-stu-id="535ae-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="535ae-120">Na primer, možete da promenite dodeljeni projekat ili resurs koji je moguće rezervisati.</span><span class="sxs-lookup"><span data-stu-id="535ae-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="535ae-121">Izaberite **Pregled**.</span><span class="sxs-lookup"><span data-stu-id="535ae-121">Select **Preview**.</span></span> <span data-ttu-id="535ae-122">U dijalogu izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="535ae-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="535ae-123">Na kartici **Stavke u glavnoj knjizi** možete videti listu originalnog trenutnog stanja koje je povezano sa izabranim stavkama vremena koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane.</span><span class="sxs-lookup"><span data-stu-id="535ae-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="535ae-124">Ako je potrebno da se izvrše dodatne ispravke, ponovite korake 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="535ae-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="535ae-125">Sve ispravljene stvarne vrednosti imaće iste vrednosti koje ste izabrali u odeljku **Nove vrednosti za stavke vremena**.</span><span class="sxs-lookup"><span data-stu-id="535ae-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="535ae-126">Ako se ispravke pojave kako se očekuje, izaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="535ae-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="535ae-127">U dijalogu izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="535ae-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="535ae-128">Vratite se na oblast **Prodaja**, izaberite **Projekti**, a zatim otvorite projekat za koji ste upravo ažurirali stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="535ae-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="535ae-129">Na stranici **Projekti**, na kartici **Stvarne vrednosti**, pogledajte promene koje ste izvršili.</span><span class="sxs-lookup"><span data-stu-id="535ae-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="535ae-130">Ako kartica **Aktuelno** nije vidljiva, izaberite **Povezano** > **Stvarne vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="535ae-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="535ae-131">Na listi **Vezani prikaz stvarnih vrednosti** možete videti da su originalne stavke vremena koje su opozvane i dalje navedene, kao što su navedene i odgovarajuće ispravljene stavke vremena.</span><span class="sxs-lookup"><span data-stu-id="535ae-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="535ae-132">Na primer, na sledećoj slici postoje dve stavke čija je količina 8,00 a koje imaju zaduženja navedena u koloni Iznos.</span><span class="sxs-lookup"><span data-stu-id="535ae-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="535ae-133">Uz to, postoje dve stavke čija je količina -8,00 koje prikazuju zadužene iznose u koloni Iznos.</span><span class="sxs-lookup"><span data-stu-id="535ae-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="535ae-134">Ove ispravke svode količinu na nulu.</span><span class="sxs-lookup"><span data-stu-id="535ae-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="535ae-135">Ispravne odobrene stavke troškova</span><span class="sxs-lookup"><span data-stu-id="535ae-135">Correct approved expense entries</span></span>

<span data-ttu-id="535ae-136">Obavite sledeće korake da biste ispravili jednu stavku troškova ili više njih.</span><span class="sxs-lookup"><span data-stu-id="535ae-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="535ae-137">U oblasti **Prodaja** u levom oknu za navigaciju, u okviru **Transakcije**, izaberite **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="535ae-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="535ae-138">Na listi **Odobreni troškovi** izaberite projekat koji želite da ispravite, a zatim izaberite **Ispravi stavke**.</span><span class="sxs-lookup"><span data-stu-id="535ae-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="535ae-139">Kreira se novi dnevnik ispravki sa dodeljenom vrstom **Ispravka troška**.</span><span class="sxs-lookup"><span data-stu-id="535ae-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="535ae-140">Na stranici **Novi dnevnik** unesite **Opis** za ispravku a na kartici **Ispravka troška**, u odeljku **Nove vrednosti za troškove**, izaberite polja podataka koja želite da ispravite za odabrane stavke troška.</span><span class="sxs-lookup"><span data-stu-id="535ae-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="535ae-141">Na primer, možete da dodelite trošak drugom **Projektu** ili da ispravite stavku **Kategorija troška**, **Datum troška** ili **Resurs koji može da se rezerviše**.</span><span class="sxs-lookup"><span data-stu-id="535ae-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="535ae-142">Izaberite **Pregled**.</span><span class="sxs-lookup"><span data-stu-id="535ae-142">Select **Preview**.</span></span> <span data-ttu-id="535ae-143">U dijalogu izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="535ae-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="535ae-144">Proverite ispravke na kartici **Stavke u glavnoj knjizi**. Možete videti listu originalnog trenutnog stanja koje je povezano sa izabranim stavkama troškova koje su opozvane i sa ispravljenim odgovarajućim stavkama koje su kreirane.</span><span class="sxs-lookup"><span data-stu-id="535ae-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="535ae-145">Ako su ispravljene vrednosti prema očekivanju, izaberite **Potvrdi**.</span><span class="sxs-lookup"><span data-stu-id="535ae-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="535ae-146">U dijalogu izaberite **U redu.**</span><span class="sxs-lookup"><span data-stu-id="535ae-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="535ae-147">Ako se vrednosti ne prikazuju kako se očekuje, izaberite **Otkaži** da biste se vratili na listu **Odobreni troškovi**.</span><span class="sxs-lookup"><span data-stu-id="535ae-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="535ae-148">Ponovite korake od 2 do 5.</span><span class="sxs-lookup"><span data-stu-id="535ae-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="535ae-149">Ispravljene stvarne vrednosti imaće iste vrednosti koje ste izabrali u odeljku **Nove vrednosti za troškove**.</span><span class="sxs-lookup"><span data-stu-id="535ae-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="535ae-150">Nakon što potvrdite dnevnik ispravki, vratite se na projekat ili projekte koje ste ažurirali da biste pogledali svoje izmene.</span><span class="sxs-lookup"><span data-stu-id="535ae-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="535ae-151">Na stranici projekta, na kartici **Aktuelno**, pregledajte **Vezani prikaz stvarnih vrednosti**.</span><span class="sxs-lookup"><span data-stu-id="535ae-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="535ae-152">Navedene su izvorne stavke i ispravljene stavke.</span><span class="sxs-lookup"><span data-stu-id="535ae-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="535ae-153">Sledeća slika prikazuje izvorne iznose stavke troška i odgovarajuće ispravljene iznose stavke troška.</span><span class="sxs-lookup"><span data-stu-id="535ae-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


