---
title: Pregled prepoznavanja prihoda
description: Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368043"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="701a7-103">Pregled prepoznavanja prihoda</span><span class="sxs-lookup"><span data-stu-id="701a7-103">Revenue recognition overview</span></span>

<span data-ttu-id="701a7-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="701a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="701a7-105">U usluzi Dynamics 365 Project Operations, principi prepoznavanja prihoda variraju u zavisnosti od izabranog načina obračuna za projekat ili deo projekta.</span><span class="sxs-lookup"><span data-stu-id="701a7-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="701a7-106">Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="701a7-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="701a7-107">Preuzete transakcije koristeći način naplate za vreme i materijal</span><span class="sxs-lookup"><span data-stu-id="701a7-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="701a7-108">Povezani su prepoznavanje troškova i prihoda.</span><span class="sxs-lookup"><span data-stu-id="701a7-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="701a7-109">Troškovi transakcije i nefakturisane prodaje knjiže se pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="701a7-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="701a7-110">Profil troškova i prihoda projekta određuje da li se nefakturisane prodajne transakcije knjiže u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="701a7-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="701a7-111">Ako je izabran **Pripadajući prihod**, sistem koristi konta za **WIP prodajnu vrednost** i **Vrednost prodaje ostvarenog prihoda** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="701a7-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="701a7-112">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="701a7-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="701a7-113">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="701a7-113">Transaction type</span></span> | <span data-ttu-id="701a7-114">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-114">Debit/Credit</span></span> | <span data-ttu-id="701a7-115">Iznos</span><span class="sxs-lookup"><span data-stu-id="701a7-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="701a7-116">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="701a7-116">WIP Sales value</span></span> | <span data-ttu-id="701a7-117">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="701a7-117">Debit</span></span> | <span data-ttu-id="701a7-118">100</span><span class="sxs-lookup"><span data-stu-id="701a7-118">100</span></span> |
  | <span data-ttu-id="701a7-119">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="701a7-119">Accrued revenue sales value</span></span> | <span data-ttu-id="701a7-120">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-120">Credit</span></span> | <span data-ttu-id="701a7-121">100</span><span class="sxs-lookup"><span data-stu-id="701a7-121">100</span></span> |

- <span data-ttu-id="701a7-122">Prihod se prepoznaje pri fakturisanju.</span><span class="sxs-lookup"><span data-stu-id="701a7-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="701a7-123">Sistem koristi konto **Fakturisani prihod** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="701a7-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="701a7-124">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="701a7-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="701a7-125">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="701a7-125">Transaction type</span></span> | <span data-ttu-id="701a7-126">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-126">Debit/Credit</span></span> | <span data-ttu-id="701a7-127">Iznos</span><span class="sxs-lookup"><span data-stu-id="701a7-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="701a7-128">Bilans klijenta</span><span class="sxs-lookup"><span data-stu-id="701a7-128">Customer balance</span></span> | <span data-ttu-id="701a7-129">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="701a7-129">Debit</span></span> | <span data-ttu-id="701a7-130">120</span><span class="sxs-lookup"><span data-stu-id="701a7-130">120</span></span> |
  | <span data-ttu-id="701a7-131">Dugovani porez na promet</span><span class="sxs-lookup"><span data-stu-id="701a7-131">Sales tax payable</span></span> | <span data-ttu-id="701a7-132">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-132">Credit</span></span> | <span data-ttu-id="701a7-133">20</span><span class="sxs-lookup"><span data-stu-id="701a7-133">20</span></span> |
  | <span data-ttu-id="701a7-134">Fakturisani prihod</span><span class="sxs-lookup"><span data-stu-id="701a7-134">Invoiced Revenue</span></span> | <span data-ttu-id="701a7-135">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-135">Credit</span></span> | <span data-ttu-id="701a7-136">100</span><span class="sxs-lookup"><span data-stu-id="701a7-136">100</span></span> |

- <span data-ttu-id="701a7-137">Ako je prihod nastao prilikom knjiženja nefakturisane prodaje, sistem će stornirani ostvareni prihod prilikom fakturisanja.</span><span class="sxs-lookup"><span data-stu-id="701a7-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="701a7-138">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="701a7-138">Transaction type</span></span> | <span data-ttu-id="701a7-139">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-139">Debit/Credit</span></span> | <span data-ttu-id="701a7-140">Iznos</span><span class="sxs-lookup"><span data-stu-id="701a7-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="701a7-141">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="701a7-141">WIP Sales value</span></span> | <span data-ttu-id="701a7-142">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="701a7-142">Credit</span></span> | <span data-ttu-id="701a7-143">100</span><span class="sxs-lookup"><span data-stu-id="701a7-143">100</span></span> |
  | <span data-ttu-id="701a7-144">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="701a7-144">Accrued revenue sales value</span></span> | <span data-ttu-id="701a7-145">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="701a7-145">Debit</span></span> | <span data-ttu-id="701a7-146">100</span><span class="sxs-lookup"><span data-stu-id="701a7-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="701a7-147">Preuzete transakcije koristeći način naplate fiksne cene</span><span class="sxs-lookup"><span data-stu-id="701a7-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="701a7-148">Prepoznavanje troškova i prihoda su zasebni.</span><span class="sxs-lookup"><span data-stu-id="701a7-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="701a7-149">Trošak transakcije se knjiži pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="701a7-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="701a7-150">Nefakturisane prodajne transakcije se ne kreiraju.</span><span class="sxs-lookup"><span data-stu-id="701a7-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="701a7-151">Prihod može biti prepoznat tokom fakturisanja ako trošak proizvoda i profil prihoda imaju **Princip korišćen za izračunavanja dovršetka projekta** podešen na **Nije rad na projektu**.</span><span class="sxs-lookup"><span data-stu-id="701a7-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="701a7-152">Ovaj način koristite samo za kratkoročne, jednostavne projekte.</span><span class="sxs-lookup"><span data-stu-id="701a7-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="701a7-153">Prihod možete priznati pomoću procene prihoda sa fiksnom cenom, bilo sa načinom **Završen ugovor** ili **Priznavanje prihoda po procentu dovršenja**.</span><span class="sxs-lookup"><span data-stu-id="701a7-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="701a7-154">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="701a7-154">Additional resources</span></span>
[<span data-ttu-id="701a7-155">Članak o konfigurisanju računovodstva za naplative projekte</span><span class="sxs-lookup"><span data-stu-id="701a7-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="701a7-156">Procena prihoda projekata sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="701a7-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="701a7-157">Upravljanje procenama prihoda</span><span class="sxs-lookup"><span data-stu-id="701a7-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="701a7-158">Metodi od troška do dovršetka</span><span class="sxs-lookup"><span data-stu-id="701a7-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]