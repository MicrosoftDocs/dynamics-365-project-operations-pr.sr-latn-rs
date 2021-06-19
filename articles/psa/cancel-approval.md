---
title: Otkazivanje prethodno odobrenih stavki vremena i troškova
description: Ova tema pruža informacije o tome kako se otkazuje odobreno vreme projekta i transakcija troškova.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bf3d146d2b07723b4d2e6e85eafd6f1b23b8b83f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014763"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="9e5b6-103">Otkazivanje prethodno odobrenih stavki vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="9e5b6-103">Cancel previously approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9e5b6-104">U najnovijoj verziji aplikacije Dynamics 365 Project Service Automation, davaoci odobrenja mogu da otkažu stavke za vreme ili troškove koje su prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="9e5b6-105">Otkazivanje prethodno odobrene stavke vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="9e5b6-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="9e5b6-106">Sledite ove korake da biste otkazali stavku vremena ili troškova koju ste prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="9e5b6-107">Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="9e5b6-108">Na stranici liste **Odobrenja** promenite prikaz na **Moja prošla odobrenja**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="9e5b6-109">Prikazuje se lista stavki vremena i troškova koje ste prethodno odobrili.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="9e5b6-110">Izaberite jednu ili više stavki, a zatim **Otkaži odobrenje**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="9e5b6-111">Dobićete poruku upozorenja.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-111">You receive a warning message.</span></span>
4. <span data-ttu-id="9e5b6-112">Da biste otkazali odobrenje, izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="9e5b6-113">Razumevanje uticaja otkazivanja odobrenja stavke vremena ili troškova</span><span class="sxs-lookup"><span data-stu-id="9e5b6-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="9e5b6-114">Kada se odobrenje otkaže, postoji i operativni i finansijski uticaj.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="9e5b6-115">Operativni uticaj</span><span class="sxs-lookup"><span data-stu-id="9e5b6-115">Operational impact</span></span>

<span data-ttu-id="9e5b6-116">Što se tiče operacija, kada se odobrenje otkaže, status zapisa će biti vraćen na **Radna verzija**, a odobravanje se više ne pojavljuje u prikazu **Moja poslednja odobravanja**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="9e5b6-117">Umesto toga, otkazano odobrenje se pojavljuje u prikazu **Stavke vremena za odobrenje** ili **Stavke troškova za odobrenje**, u zavisnosti od toga da li se radi o stavci vremena ili stavci troškova.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="9e5b6-118">Pored toga, status povezane stavke vremena ili troškova se menja u **Prosleđeno**, tako da povezana stavka odgovara odobrenjima koja imaju status **Radna verzija**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="9e5b6-119">Kao davalac odobrenja, možete da uređujete neka od polja odobravanja koja imaju status **Radna verzija**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="9e5b6-120">Ova polja obuhvataju stavke **Vrsta naplate** i **Naplativi sati za stavke vremena**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="9e5b6-121">Nakon što unesete promene, možete ponovo da odobrite zapis.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="9e5b6-122">Druga mogućnost je da odbacite stavku.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="9e5b6-123">Ako odbacite odobravanje stavke vremena, status stavke će biti promenjen u **Vraćena**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="9e5b6-124">Ako odbacite odobravanje stavke troškova, status stavke će biti promenjen u **Odbačena**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="9e5b6-125">Sa funkcionalne strane, i vraćene i odbačene stavke se ponašaju isto kao stavka koja ima status **Radna verzija**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="9e5b6-126">Član projektnog tima može da unese sve potrebne promene u stavku, a zatim da je ponovo prosledi na odobravanje ili da u potpunosti izbriše stavku.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="9e5b6-127">Finansijski uticaj</span><span class="sxs-lookup"><span data-stu-id="9e5b6-127">Financial impact</span></span>

<span data-ttu-id="9e5b6-128">Postoji i finansijski uticaj na projekat kada se odobrenje otkaže.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="9e5b6-129">Prvo, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:</span><span class="sxs-lookup"><span data-stu-id="9e5b6-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="9e5b6-130">Status poravnanja se podešava na **Poravnato**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="9e5b6-131">Status naplate se podešava na **Otkazano**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="9e5b6-132">Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="9e5b6-133">Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="9e5b6-134">Jedine vrednosti koje se ne kopiraju su vrednosti količine.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="9e5b6-135">Umesto toga, ove vrednosti se storniraju.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-135">These values are reversed instead.</span></span> <span data-ttu-id="9e5b6-136">Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="9e5b6-137">Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a status naplate na **Otkazano**.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="9e5b6-138">Nakon ovih izmena, iznos koji se evidentira kao potrošen za projekat i preostali prihodi od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.</span><span class="sxs-lookup"><span data-stu-id="9e5b6-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]