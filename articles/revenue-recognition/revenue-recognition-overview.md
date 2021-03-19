---
title: Pregled prepoznavanja prihoda
description: Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278885"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="599df-103">Pregled prepoznavanja prihoda</span><span class="sxs-lookup"><span data-stu-id="599df-103">Revenue recognition overview</span></span>

<span data-ttu-id="599df-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="599df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="599df-105">U usluzi Dynamics 365 Project Operations, principi prepoznavanja prihoda variraju u zavisnosti od izabranog načina obračuna za projekat ili deo projekta.</span><span class="sxs-lookup"><span data-stu-id="599df-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="599df-106">Ova tema pruža informacije o prepoznavanju prihoda u usluzi Project Operations.</span><span class="sxs-lookup"><span data-stu-id="599df-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="599df-107">Preuzete transakcije koristeći način naplate za vreme i materijal</span><span class="sxs-lookup"><span data-stu-id="599df-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="599df-108">Povezani su prepoznavanje troškova i prihoda.</span><span class="sxs-lookup"><span data-stu-id="599df-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="599df-109">Troškovi transakcije i nefakturisane prodaje knjiže se pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="599df-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="599df-110">Profil troškova i prihoda projekta određuje da li se nefakturisane prodajne transakcije knjiže u glavnu knjigu.</span><span class="sxs-lookup"><span data-stu-id="599df-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="599df-111">Ako je izabran **Pripadajući prihod**, sistem koristi konta za **WIP prodajnu vrednost** i **Vrednost prodaje ostvarenog prihoda** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="599df-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="599df-112">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="599df-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="599df-113">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="599df-113">Transaction type</span></span> | <span data-ttu-id="599df-114">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-114">Debit/Credit</span></span> | <span data-ttu-id="599df-115">Iznos</span><span class="sxs-lookup"><span data-stu-id="599df-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="599df-116">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="599df-116">WIP Sales value</span></span> | <span data-ttu-id="599df-117">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="599df-117">Debit</span></span> | <span data-ttu-id="599df-118">100</span><span class="sxs-lookup"><span data-stu-id="599df-118">100</span></span> |
  | <span data-ttu-id="599df-119">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="599df-119">Accrued revenue sales value</span></span> | <span data-ttu-id="599df-120">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-120">Credit</span></span> | <span data-ttu-id="599df-121">100</span><span class="sxs-lookup"><span data-stu-id="599df-121">100</span></span> |

- <span data-ttu-id="599df-122">Prihod se prepoznaje pri fakturisanju.</span><span class="sxs-lookup"><span data-stu-id="599df-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="599df-123">Sistem koristi konto **Fakturisani prihod** tokom knjiženja.</span><span class="sxs-lookup"><span data-stu-id="599df-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="599df-124">Sledeće je primer ovog načina.</span><span class="sxs-lookup"><span data-stu-id="599df-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="599df-125">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="599df-125">Transaction type</span></span> | <span data-ttu-id="599df-126">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-126">Debit/Credit</span></span> | <span data-ttu-id="599df-127">Iznos</span><span class="sxs-lookup"><span data-stu-id="599df-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="599df-128">Bilans klijenta</span><span class="sxs-lookup"><span data-stu-id="599df-128">Customer balance</span></span> | <span data-ttu-id="599df-129">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="599df-129">Debit</span></span> | <span data-ttu-id="599df-130">120</span><span class="sxs-lookup"><span data-stu-id="599df-130">120</span></span> |
  | <span data-ttu-id="599df-131">Dugovani porez na promet</span><span class="sxs-lookup"><span data-stu-id="599df-131">Sales tax payable</span></span> | <span data-ttu-id="599df-132">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-132">Credit</span></span> | <span data-ttu-id="599df-133">20</span><span class="sxs-lookup"><span data-stu-id="599df-133">20</span></span> |
  | <span data-ttu-id="599df-134">Fakturisani prihod</span><span class="sxs-lookup"><span data-stu-id="599df-134">Invoiced Revenue</span></span> | <span data-ttu-id="599df-135">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-135">Credit</span></span> | <span data-ttu-id="599df-136">100</span><span class="sxs-lookup"><span data-stu-id="599df-136">100</span></span> |

- <span data-ttu-id="599df-137">Ako je prihod nastao prilikom knjiženja nefakturisane prodaje, sistem će stornirani ostvareni prihod prilikom fakturisanja.</span><span class="sxs-lookup"><span data-stu-id="599df-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="599df-138">Tip transakcije</span><span class="sxs-lookup"><span data-stu-id="599df-138">Transaction type</span></span> | <span data-ttu-id="599df-139">Zaduženje/Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-139">Debit/Credit</span></span> | <span data-ttu-id="599df-140">Iznos</span><span class="sxs-lookup"><span data-stu-id="599df-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="599df-141">Prodajna vrednost za rad na projektu</span><span class="sxs-lookup"><span data-stu-id="599df-141">WIP Sales value</span></span> | <span data-ttu-id="599df-142">Odobrenje</span><span class="sxs-lookup"><span data-stu-id="599df-142">Credit</span></span> | <span data-ttu-id="599df-143">100</span><span class="sxs-lookup"><span data-stu-id="599df-143">100</span></span> |
  | <span data-ttu-id="599df-144">Vrednost prodaje za obračunati prihod</span><span class="sxs-lookup"><span data-stu-id="599df-144">Accrued revenue sales value</span></span> | <span data-ttu-id="599df-145">Zaduženje</span><span class="sxs-lookup"><span data-stu-id="599df-145">Debit</span></span> | <span data-ttu-id="599df-146">100</span><span class="sxs-lookup"><span data-stu-id="599df-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="599df-147">Preuzete transakcije koristeći način naplate fiksne cene</span><span class="sxs-lookup"><span data-stu-id="599df-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="599df-148">Prepoznavanje troškova i prihoda su zasebni.</span><span class="sxs-lookup"><span data-stu-id="599df-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="599df-149">Trošak transakcije se knjiži pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="599df-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="599df-150">Nefakturisane prodajne transakcije se ne kreiraju.</span><span class="sxs-lookup"><span data-stu-id="599df-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="599df-151">Prihod može biti prepoznat tokom fakturisanja ako trošak proizvoda i profil prihoda imaju **Princip korišćen za izračunavanja dovršetka projekta** podešen na **Nije rad na projektu**.</span><span class="sxs-lookup"><span data-stu-id="599df-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="599df-152">Ovaj način koristite samo za kratkoročne, jednostavne projekte.</span><span class="sxs-lookup"><span data-stu-id="599df-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="599df-153">Prihod možete priznati pomoću procene prihoda sa fiksnom cenom, bilo sa načinom **Završen ugovor** ili **Priznavanje prihoda po procentu dovršenja**.</span><span class="sxs-lookup"><span data-stu-id="599df-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="599df-154">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="599df-154">Additional resources</span></span>
[<span data-ttu-id="599df-155">Članak o konfigurisanju računovodstva za naplative projekte</span><span class="sxs-lookup"><span data-stu-id="599df-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="599df-156">Procena prihoda projekata sa fiksnom cenom</span><span class="sxs-lookup"><span data-stu-id="599df-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="599df-157">Upravljanje procenama prihoda</span><span class="sxs-lookup"><span data-stu-id="599df-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="599df-158">Metodi od troška do dovršetka</span><span class="sxs-lookup"><span data-stu-id="599df-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]