---
title: Opozivanje odobrenih stavki vremena ili troškova
description: Ova tema pruža informacije o tome kako se opozivaju prethodno odobreno vreme ili transakcija troškova.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120560"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="a1b16-103">Opozivanje odobrenih stavki vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="a1b16-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a1b16-104">Član projektnog tima ili druga osoba koja prosleđuje stavku vremena ili troškova može je opozvati nakon što je odobrena.</span><span class="sxs-lookup"><span data-stu-id="a1b16-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="a1b16-105">Proces opozivanja odobrene stavke vremena ili troškova ima dva koraka:</span><span class="sxs-lookup"><span data-stu-id="a1b16-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="a1b16-106">Podnosilac zahteva opozivanje.</span><span class="sxs-lookup"><span data-stu-id="a1b16-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="a1b16-107">Davalac odobrenja odobrava opoziv.</span><span class="sxs-lookup"><span data-stu-id="a1b16-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="a1b16-108">Zatražite opozivanje</span><span class="sxs-lookup"><span data-stu-id="a1b16-108">Request a recall</span></span>

<span data-ttu-id="a1b16-109">Sledite ove korake da biste zatražili opozivanje odobrene stavke vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="a1b16-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="a1b16-110">Za stavke vremena, idite na **Projekti** \> **Moj posao** \> **Stavka vremena**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="a1b16-111">–ili–</span><span class="sxs-lookup"><span data-stu-id="a1b16-111">–or–</span></span>

    <span data-ttu-id="a1b16-112">Za stavke troškova, idite na **Projekti** \> **Moj posao** \> **Troškovi**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="a1b16-113">Za stavke vremena odaberite sve stavke za određenu kombinaciju projekta i zadatka.</span><span class="sxs-lookup"><span data-stu-id="a1b16-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="a1b16-114">Alternativno, u mreži odaberite pojedinačne ćelije za vreme za određeni datum i projekat.</span><span class="sxs-lookup"><span data-stu-id="a1b16-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="a1b16-115">–ili–</span><span class="sxs-lookup"><span data-stu-id="a1b16-115">–or–</span></span>

    <span data-ttu-id="a1b16-116">Za stavke troškova odaberite red za stavku troška da biste je opozvali.</span><span class="sxs-lookup"><span data-stu-id="a1b16-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="a1b16-117">Izaberite **Opozovi**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-117">Select **Recall**.</span></span> <span data-ttu-id="a1b16-118">Pojavljuje se dijalog za potvrdu.</span><span class="sxs-lookup"><span data-stu-id="a1b16-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="a1b16-119">Ako su odabrane stavke vremena i troškova već odobrene, od vas će se tražiti da unesete razlog opoziva.</span><span class="sxs-lookup"><span data-stu-id="a1b16-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="a1b16-120">Unesite razlog opoziva, a zatim izaberite **U redu** da potvrdite operaciju.</span><span class="sxs-lookup"><span data-stu-id="a1b16-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="a1b16-121">Sistem šalje osobi koja je odobrila stavke zahtev za odobrenje opoziva.</span><span class="sxs-lookup"><span data-stu-id="a1b16-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b16-122">Iako se odobrene stavke vremena i troškova mogu opozvati, ako je odobreno vreme ili trošak već fakturisan klijentu, zahtev za opoziv ne može da se kreira.</span><span class="sxs-lookup"><span data-stu-id="a1b16-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="a1b16-123">Korisnik koji pokuša da kreira zahtev za opoziv dobiće poruku u kojoj stoji da se vreme ili trošak ne mogu opozvati jer su već fakturisani.</span><span class="sxs-lookup"><span data-stu-id="a1b16-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="a1b16-124">Odobravanje ili odbacivanje zahteva za opoziv</span><span class="sxs-lookup"><span data-stu-id="a1b16-124">Approve or reject a recall request</span></span>

<span data-ttu-id="a1b16-125">Sledite ove korake da biste odobrili ili odbacili zahtev za opoziv.</span><span class="sxs-lookup"><span data-stu-id="a1b16-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="a1b16-126">Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="a1b16-127">Na stranici liste **Odobrenja** promenite prikaz na **Opozovi zahteve za odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="a1b16-128">Prikazuje se lista prosleđenih zahteva za opoziv.</span><span class="sxs-lookup"><span data-stu-id="a1b16-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="a1b16-129">Izaberite jednu ili više stavki, a zatim **Odobri** ili **Odbaci**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="a1b16-130">Ako ste izabrali **Odobri**, dobijate poruku upozorenja koja objašnjava efekat odobrenja.</span><span class="sxs-lookup"><span data-stu-id="a1b16-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="a1b16-131">Izaberite **U redu** da biste potvrdili operaciju.</span><span class="sxs-lookup"><span data-stu-id="a1b16-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="a1b16-132">Zahtev za opoziv je odobren.</span><span class="sxs-lookup"><span data-stu-id="a1b16-132">The recall request is approved.</span></span>

    <span data-ttu-id="a1b16-133">–ili–</span><span class="sxs-lookup"><span data-stu-id="a1b16-133">–or–</span></span>

    <span data-ttu-id="a1b16-134">Ako ste izabrali **Odbaci**, zahtev za opoziv je odbijen.</span><span class="sxs-lookup"><span data-stu-id="a1b16-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b16-135">Kao i u slučaju zahtevanja opoziva, kada se opoziv odobri, sistem proverava da li ima bilo kakvih aktivnosti fakturisanja u stavkama vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="a1b16-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="a1b16-136">Ako je stavka već fakturisana ili je u radnoj verziji fakture, davalac odobrenja će dobiti poruku o grešci u kojoj stoji da se opoziv vremena ili troška ne može odobriti jer je već fakturisan.</span><span class="sxs-lookup"><span data-stu-id="a1b16-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="a1b16-137">Efekat zahteva za opoziv</span><span class="sxs-lookup"><span data-stu-id="a1b16-137">Impact of a recall request</span></span>

<span data-ttu-id="a1b16-138">Kada se odobrenje opozove, postoji i operativni i finansijski uticaj.</span><span class="sxs-lookup"><span data-stu-id="a1b16-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="a1b16-139">Operativni uticaj</span><span class="sxs-lookup"><span data-stu-id="a1b16-139">Operational impact</span></span>

<span data-ttu-id="a1b16-140">Ako je zahtev za opoziv odobren, zapis odobrenja označava se kao **Odbačen**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="a1b16-141">Status stavke se menja u **Vraćena** ili **Odbačena**, u zavisnosti da li je to stavka vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="a1b16-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="a1b16-142">Član projektnog tima može pregledati stavke, uređivati i zatim ponovo prosleđivati stavke ili ih u potpunosti brisati.</span><span class="sxs-lookup"><span data-stu-id="a1b16-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="a1b16-143">Ako se zahtev za opoziv odbaci, status stavke ostaje **Odobrena** i stavku ne može da uređuje član projektnog tima niti davalac odobrenja za projekat.</span><span class="sxs-lookup"><span data-stu-id="a1b16-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="a1b16-144">Finansijski uticaj</span><span class="sxs-lookup"><span data-stu-id="a1b16-144">Financial impact</span></span>

<span data-ttu-id="a1b16-145">Ako se zahtev za opoziv odobri, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:</span><span class="sxs-lookup"><span data-stu-id="a1b16-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="a1b16-146">Polje **Status poravnanja** se ažurira na **Poravnato**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="a1b16-147">Polje **Status naplate** se ažurira na **Otkazano**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="a1b16-148">Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="a1b16-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="a1b16-149">Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti.</span><span class="sxs-lookup"><span data-stu-id="a1b16-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="a1b16-150">Jedine vrednosti koje se ne kopiraju su vrednosti količine.</span><span class="sxs-lookup"><span data-stu-id="a1b16-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="a1b16-151">Umesto toga, ove vrednosti se storniraju.</span><span class="sxs-lookup"><span data-stu-id="a1b16-151">These values are reversed instead.</span></span> <span data-ttu-id="a1b16-152">Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="a1b16-153">Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a polje **Status naplate** na **Otkazano**.</span><span class="sxs-lookup"><span data-stu-id="a1b16-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="a1b16-154">Zbog ovih izmena, evidentirana potrošnja za projekat i preostali prihod od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.</span><span class="sxs-lookup"><span data-stu-id="a1b16-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="a1b16-155">Ako se zahtev za opoziv odbaci, nema finansijskog uticaja na projekat.</span><span class="sxs-lookup"><span data-stu-id="a1b16-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="a1b16-156">Promene zapisa stavke vremena</span><span class="sxs-lookup"><span data-stu-id="a1b16-156">Changes to time entry records</span></span>

<span data-ttu-id="a1b16-157">Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke vremena kada su opozvane.</span><span class="sxs-lookup"><span data-stu-id="a1b16-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Promene statusa stavke vremena](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="a1b16-159">Promene zapisa stavke troškova</span><span class="sxs-lookup"><span data-stu-id="a1b16-159">Changes to expense entry records</span></span>

<span data-ttu-id="a1b16-160">Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke troškova kada su opozvane.</span><span class="sxs-lookup"><span data-stu-id="a1b16-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Promene statusa stavke troškova](media/ExpenseEntryStateTransitions.png)
