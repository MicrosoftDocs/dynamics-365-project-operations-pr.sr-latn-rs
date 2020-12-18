---
title: Podrazumevane vrednosti finansijske dimenzije
description: Ova tema pruža informacije o načinu postavljanja podrazumevanih vrednosti finansijskih dimenzija.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642380"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="fbb78-103">Podrazumevane vrednosti finansijske dimenzije</span><span class="sxs-lookup"><span data-stu-id="fbb78-103">Financial dimension defaults</span></span>

<span data-ttu-id="fbb78-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_</span><span class="sxs-lookup"><span data-stu-id="fbb78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="fbb78-105">Dynamics 365 Project Operations koristi radni okvir za [finansijske dimenzije](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) u usluzi Dynamics 365 Finance kako bi pružio dodatni uvid u transakcije potknjige i glavne knjige.</span><span class="sxs-lookup"><span data-stu-id="fbb78-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="fbb78-106">Podrazumevane finansijske dimenzije mogu se postaviti na osnovu klijenta, izvora finansiranja projekta, kontrolne tačke, predmeta ugovora za projekat ili projekta.</span><span class="sxs-lookup"><span data-stu-id="fbb78-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="fbb78-107">Definisanje podrazumevanih finansijskih dimenzija za klijenta</span><span class="sxs-lookup"><span data-stu-id="fbb78-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="fbb78-108">Podrazumevane vrednosti za dimenziju klijenta navedene su u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb78-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="fbb78-109">Dovršite sledeće korake da biste podesili podrazumevane vrednosti dimenzija.</span><span class="sxs-lookup"><span data-stu-id="fbb78-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="fbb78-110">Idite na **Potraživanja** > **Klijenti** > **Svi klijenti**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="fbb78-111">Na stranici **Klijenti**, na kartici **Finansijske dimenzije**, podesite vrednosti finansijskih dimenzija za određenog klijenta.</span><span class="sxs-lookup"><span data-stu-id="fbb78-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="fbb78-112">Definisanje podrazumevanih finansijskih dimenzija za ugovore za projekat</span><span class="sxs-lookup"><span data-stu-id="fbb78-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="fbb78-113">Ugovori za projekat se kreiraju i održavaju u usluzi Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="fbb78-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="fbb78-114">Atributi računovodstva za ugovore za projekat postavljeni su u modul **Upravljanje projektima i računovodstvo** u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb78-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="fbb78-115">Podesite finansijske dimenzije za izvor finansiranja projekta</span><span class="sxs-lookup"><span data-stu-id="fbb78-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="fbb78-116">Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Ugovori za projekat**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="fbb78-117">Izaberite zapis koji želite da ažurirate, a zatim na kartici **Ugovor o projektu** izaberite **Prikaži podrazumevano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="fbb78-118">Proširite **Srodne informacije** i izaberite karticu **Izvori finansiranja**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="fbb78-119">Podesite podrazumevane vrednosti finansijskih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="fbb78-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="fbb78-120">Imajte u vidu da se podrazumevane vrednosti finansijskih dimenzija uzimaju sa naloga klijenta.</span><span class="sxs-lookup"><span data-stu-id="fbb78-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="fbb78-121">Podesite finansijske dimenzije za predmet ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="fbb78-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="fbb78-122">Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Ugovori za projekat**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="fbb78-123">Izaberite zapis koji želite da ažurirate, a zatim na kartici **Ugovor o projektu** izaberite **Prikaži podrazumevano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="fbb78-124">Proširite **Srodne informacije** i izaberite karticu **Predmeti ugovora**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="fbb78-125">Podesite podrazumevane vrednosti finansijskih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="fbb78-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="fbb78-126">Podrazumevane finansijske dimenzije su primenljive i mogu se koristiti samo sa predmetima ugovora sa fiksnom cenom (kontrolnom tačkom).</span><span class="sxs-lookup"><span data-stu-id="fbb78-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="fbb78-127">Ove podrazumevane vrednosti se koriste za povezane transakcije za poslovnog klijenta na projektu i stavke faktura.</span><span class="sxs-lookup"><span data-stu-id="fbb78-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="fbb78-128">Definisanje podrazumevanih finansijskih dimenzija za projekte</span><span class="sxs-lookup"><span data-stu-id="fbb78-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="fbb78-129">Projekti se kreiraju i održavaju u usluzi CDS.</span><span class="sxs-lookup"><span data-stu-id="fbb78-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="fbb78-130">Atributi računovodstva za projekat postavljeni su u modul **Upravljanje projektima i računovodstvo** u usluzi Finance.</span><span class="sxs-lookup"><span data-stu-id="fbb78-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="fbb78-131">Idite na **Upravljanje projektima i računovodstvo** > **Projekti** > **Svi projekti**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="fbb78-132">Izaberite zapis koji želite da ažurirate, a zatim na kartici **Projekat** izaberite **Prikaži podrazumevano računovodstvo**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="fbb78-133">Proširite **Srodne informacije** i izaberite karticu **Podešavanje**.</span><span class="sxs-lookup"><span data-stu-id="fbb78-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="fbb78-134">Podesite podrazumevane vrednosti finansijskih dimenzija.</span><span class="sxs-lookup"><span data-stu-id="fbb78-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="fbb78-135">Imajte u vidu da se podrazumevane vrednosti finansijskih dimenzija uzimaju sa naloga klijenta.</span><span class="sxs-lookup"><span data-stu-id="fbb78-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="fbb78-136">Ako je projekat povezan sa predmetom ugovora sa više klijenata ugovora za projekat, primarni klijent se koristi za podrazumevane finansijske dimenzije.</span><span class="sxs-lookup"><span data-stu-id="fbb78-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="fbb78-137">Podrazumevane finansijske dimenzije projekta koriste se za postavljanje podrazumevanih vrednosti stavke u glavnoj knjizi za transakcije vremena, troškova i naknada u **Project Operations dnevniku integracije** i na povezanim stavkama fakture projekta.</span><span class="sxs-lookup"><span data-stu-id="fbb78-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
