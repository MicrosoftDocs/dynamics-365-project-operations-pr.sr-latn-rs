---
title: Pregled prepoznavanja prihoda
description: Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5f962572c6ec0298d2d91d33f83e4120a498a6f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013773"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="8cdd8-103">Pregled prepoznavanja prihoda</span><span class="sxs-lookup"><span data-stu-id="8cdd8-103">Revenue recognition overview</span></span>

<span data-ttu-id="8cdd8-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="8cdd8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8cdd8-105">U usluzi Dynamics 365 Project Operations, principi prepoznavanja prihoda variraju u zavisnosti od izabranog načina obračuna za projekat ili deo projekta.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="8cdd8-106">Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="8cdd8-107">Preuzete transakcije koristeći način naplate za vreme i materijal</span><span class="sxs-lookup"><span data-stu-id="8cdd8-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="8cdd8-108">Povezani su prepoznavanje troškova i prihoda.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="8cdd8-109">Troškovi transakcije i nefakturisane prodaje knjiže se pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="8cdd8-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="8cdd8-110">Profil troškova i prihoda projekta određuje da li se nefakturisane prodajne transakcije knjiže u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="8cdd8-111">Ako je izabran **Pripadajući prihod**, sistem koristi konta za **WIP prodajnu vrednost** i **Vrednost prodaje ostvarenog prihoda** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="8cdd8-112">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="8cdd8-113">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="8cdd8-113">Transaction type</span></span> | <span data-ttu-id="8cdd8-114">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-114">Debit/Credit</span></span> | <span data-ttu-id="8cdd8-115">Iznos</span><span class="sxs-lookup"><span data-stu-id="8cdd8-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="8cdd8-116">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="8cdd8-116">WIP Sales value</span></span> | <span data-ttu-id="8cdd8-117">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-117">Debit</span></span> | <span data-ttu-id="8cdd8-118">100</span><span class="sxs-lookup"><span data-stu-id="8cdd8-118">100</span></span> |
  | <span data-ttu-id="8cdd8-119">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="8cdd8-119">Accrued revenue sales value</span></span> | <span data-ttu-id="8cdd8-120">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-120">Credit</span></span> | <span data-ttu-id="8cdd8-121">100</span><span class="sxs-lookup"><span data-stu-id="8cdd8-121">100</span></span> |

- <span data-ttu-id="8cdd8-122">Prihod se prepoznaje pri fakturisanju.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="8cdd8-123">Sistem koristi konto **Fakturisani prihod** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="8cdd8-124">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="8cdd8-125">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="8cdd8-125">Transaction type</span></span> | <span data-ttu-id="8cdd8-126">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-126">Debit/Credit</span></span> | <span data-ttu-id="8cdd8-127">Iznos</span><span class="sxs-lookup"><span data-stu-id="8cdd8-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="8cdd8-128">Bilans klijenta</span><span class="sxs-lookup"><span data-stu-id="8cdd8-128">Customer balance</span></span> | <span data-ttu-id="8cdd8-129">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-129">Debit</span></span> | <span data-ttu-id="8cdd8-130">120</span><span class="sxs-lookup"><span data-stu-id="8cdd8-130">120</span></span> |
  | <span data-ttu-id="8cdd8-131">Dugovani porez na promet</span><span class="sxs-lookup"><span data-stu-id="8cdd8-131">Sales tax payable</span></span> | <span data-ttu-id="8cdd8-132">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-132">Credit</span></span> | <span data-ttu-id="8cdd8-133">20</span><span class="sxs-lookup"><span data-stu-id="8cdd8-133">20</span></span> |
  | <span data-ttu-id="8cdd8-134">Fakturisani prihod</span><span class="sxs-lookup"><span data-stu-id="8cdd8-134">Invoiced Revenue</span></span> | <span data-ttu-id="8cdd8-135">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-135">Credit</span></span> | <span data-ttu-id="8cdd8-136">100</span><span class="sxs-lookup"><span data-stu-id="8cdd8-136">100</span></span> |

- <span data-ttu-id="8cdd8-137">Ako je prihod nastao prilikom knjiženja nefakturisane prodaje, sistem će stornirani ostvareni prihod prilikom fakturisanja.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="8cdd8-138">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="8cdd8-138">Transaction type</span></span> | <span data-ttu-id="8cdd8-139">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-139">Debit/Credit</span></span> | <span data-ttu-id="8cdd8-140">Iznos</span><span class="sxs-lookup"><span data-stu-id="8cdd8-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="8cdd8-141">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="8cdd8-141">WIP Sales value</span></span> | <span data-ttu-id="8cdd8-142">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-142">Credit</span></span> | <span data-ttu-id="8cdd8-143">100</span><span class="sxs-lookup"><span data-stu-id="8cdd8-143">100</span></span> |
  | <span data-ttu-id="8cdd8-144">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="8cdd8-144">Accrued revenue sales value</span></span> | <span data-ttu-id="8cdd8-145">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="8cdd8-145">Debit</span></span> | <span data-ttu-id="8cdd8-146">100</span><span class="sxs-lookup"><span data-stu-id="8cdd8-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="8cdd8-147">Preuzete transakcije koristeći način naplate fiksne cene</span><span class="sxs-lookup"><span data-stu-id="8cdd8-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="8cdd8-148">Prepoznavanje troškova i prihoda su zasebni.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="8cdd8-149">Trošak transakcije se knjiži pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="8cdd8-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="8cdd8-150">Nefakturisane prodajne transakcije se ne kreiraju.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="8cdd8-151">Prihod može biti prepoznat tokom fakturisanja ako trošak proizvoda i profil prihoda imaju **Princip korišćen za izračunavanja dovršetka projekta** podešen na **Nije rad na projektu**.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="8cdd8-152">Ovaj način koristite samo za kratkoročne, jednostavne projekte.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="8cdd8-153">Prihod možete priznati pomoću procene prihoda sa fiksnom cenom, bilo sa načinom **Završen ugovor** ili **Priznavanje prihoda po procentu dovršenja**.</span><span class="sxs-lookup"><span data-stu-id="8cdd8-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8cdd8-154">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="8cdd8-154">Additional resources</span></span>
[<span data-ttu-id="8cdd8-155">Članak o konfigurisanju računovodstva za naplative projekte</span><span class="sxs-lookup"><span data-stu-id="8cdd8-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="8cdd8-156">Procena prihoda projekata sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="8cdd8-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="8cdd8-157">Upravljanje procenama prihoda</span><span class="sxs-lookup"><span data-stu-id="8cdd8-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="8cdd8-158">Metodi od troška do dovršetka</span><span class="sxs-lookup"><span data-stu-id="8cdd8-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]