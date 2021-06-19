---
title: Kreirajte modele predviđanja za budžete projekata
description: Ova tema opisuje kako kreirati model predviđanja za preostale budžete.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006313"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="a768e-103">Kreirajte modele predviđanja za budžete projekata</span><span class="sxs-lookup"><span data-stu-id="a768e-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a768e-104">Ova tema opisuje kako kreirati model predviđanja za preostale budžete.</span><span class="sxs-lookup"><span data-stu-id="a768e-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="a768e-105">Projekat koji podleže budžetskoj kontroli koristi dve vrste budžeta: originalni i preostali.</span><span class="sxs-lookup"><span data-stu-id="a768e-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="a768e-106">Kada kreirate budžet projekta, morate navesti modele predviđanja prvobitnog i preostalog budžeta koji su kreirani na stranici **Modeli predviđanja**.</span><span class="sxs-lookup"><span data-stu-id="a768e-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="a768e-107">Budžeti projekata zasnovani na navedenim modelima kreiraju se kada dodelite budžet projekta.</span><span class="sxs-lookup"><span data-stu-id="a768e-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="a768e-108">Model prognoze koji se koristi za kontrolu budžeta ne može da ima podmodel ili da se koristi kao podmodel.</span><span class="sxs-lookup"><span data-stu-id="a768e-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="a768e-109">Izaberite **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Prognoze**  > **Modeli predviđanja**.</span><span class="sxs-lookup"><span data-stu-id="a768e-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="a768e-110">Izaberite **Novo** da biste kreirali novi model prognoze, a zatim unesite ID broja modela i ime za novi model.</span><span class="sxs-lookup"><span data-stu-id="a768e-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="a768e-111">Podesite opciju **Zaustavljeno** na **Da** kako bi se sprečile bilo kakve promene linija predviđanja za model prognoze.</span><span class="sxs-lookup"><span data-stu-id="a768e-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="a768e-112">Ako linije predviđanja sa kojima je model povezan treba da generišu predviđanja novčanog toka u glavnoj knjizi, postavite **Uključi u predviđanja novčanog toka** na **Da.**</span><span class="sxs-lookup"><span data-stu-id="a768e-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="a768e-113">Da biste koristili datum projekta kao datum fakture, podesite **Datum fakture prognoze** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="a768e-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="a768e-114">U polju **Tip budžeta** izaberite jedan od sledećih tipova modela:</span><span class="sxs-lookup"><span data-stu-id="a768e-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="a768e-115">**Originalni budžet**: Koristite originalne iznose budžeta koji su prosleđeni pri kreiranju i odobravanju početnog budžeta.</span><span class="sxs-lookup"><span data-stu-id="a768e-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="a768e-116">**Preostali budžet**: Koristite preostale iznose budžeta tokom trajanja projekta.</span><span class="sxs-lookup"><span data-stu-id="a768e-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="a768e-117">Stanja u ovom modelu predviđanja smanjuju se stvarnim transakcijama, a povećavaju ili smanjuju revizijama budžeta.</span><span class="sxs-lookup"><span data-stu-id="a768e-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="a768e-118">**Prenos**: Koristite prenosne iznose budžeta za projekat.</span><span class="sxs-lookup"><span data-stu-id="a768e-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="a768e-119">Prenos je opcioni postupak koji se može pokrenuti radi prenosa neiskorišćenih iznosa budžeta iz jedne fiskalne godine u drugu.</span><span class="sxs-lookup"><span data-stu-id="a768e-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="a768e-120">Po potrebi podesite sledeće opcije:</span><span class="sxs-lookup"><span data-stu-id="a768e-120">Set the following options as required:</span></span>

   - <span data-ttu-id="a768e-121">Da biste koristili datum projekta kao datum fakture, omogućite **Datum fakture prognoze**.</span><span class="sxs-lookup"><span data-stu-id="a768e-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="a768e-122">Omogućite **Prognoza pomoću WIP-a** za predviđanje na osnovu posla u toku (WIP), a zatim odaberite tip WIP-a.</span><span class="sxs-lookup"><span data-stu-id="a768e-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="a768e-123">Možete zadržati podrazumevani **Tip budžeta** kao **Nijedan** ili unesite novi tip.</span><span class="sxs-lookup"><span data-stu-id="a768e-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="a768e-124">Tip budžeta ne može se promeniti nakon što promenite zapis.</span><span class="sxs-lookup"><span data-stu-id="a768e-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="a768e-125">Ako promenite podrazumevani tip budžeta, sve ostale opcije postaće nedostupne za ažuriranja i ne možete ponovo koristiti ovaj model predviđanja.</span><span class="sxs-lookup"><span data-stu-id="a768e-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]