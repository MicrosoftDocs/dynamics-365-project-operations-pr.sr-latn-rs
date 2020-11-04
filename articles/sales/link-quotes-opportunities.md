---
title: Kreiranje ponuda za projekat iz mogućnosti za poslovanje
description: Ova tema pruža informacije o kreiranju ponude za projekat iz mogućnosti za poslovanje.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083492"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="ecf6d-103">Kreiranje ponuda za projekat iz mogućnosti za poslovanje</span><span class="sxs-lookup"><span data-stu-id="ecf6d-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="ecf6d-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="ecf6d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ecf6d-105">Ponude se mogu kreirati iz mogućnosti za poslovanje projekta na sledeće načine:</span><span class="sxs-lookup"><span data-stu-id="ecf6d-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="ecf6d-106">Iz kartice **Ponude** na stranici **Mogućnost za poslovanje projekta**</span><span class="sxs-lookup"><span data-stu-id="ecf6d-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="ecf6d-107">Iz toka procesa prodaje mogućnosti za poslovanje</span><span class="sxs-lookup"><span data-stu-id="ecf6d-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="ecf6d-108">Ažuriranjem reference na mogućnost za poslovanje za postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="ecf6d-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="ecf6d-109">Iz kartice Ponude na stranici Mogućnost za poslovanje projekta</span><span class="sxs-lookup"><span data-stu-id="ecf6d-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="ecf6d-110">Da biste kreirali ponudu za projekat iz mogućnosti za poslovanje, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="ecf6d-111">Otvorite stranicu **Mogućnost za poslovanje projekta** i izaberite karticu **Ponude**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="ecf6d-112">Na podformi **Ponude** , izaberite **+** da biste kreirali novu ponudu za projekat na osnovu mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="ecf6d-113">Svi predmeti mogućnosti za poslovanje i srodni cenovnici projekta kopiraju se u novu ponudu iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="ecf6d-114">Iz toka procesa prodaje mogućnosti za poslovanje</span><span class="sxs-lookup"><span data-stu-id="ecf6d-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="ecf6d-115">Da biste kreirali ponudu iz toka procesa prodaje mogućnosti za poslovanje, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="ecf6d-116">Iz toka procesa prodaje mogućnosti za poslovanje, otvorite mogućnost za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="ecf6d-117">Izaberite fazu **Kvalifikovanje**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="ecf6d-118">Izaberite **Sledeće** , a zatim izaberite **+ Kreiraj** da biste kreirali novu ponudu.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="ecf6d-119">Većina informacija na kartici **Rezime** za ovu novu ponudu podrazumevano će doći iz mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="ecf6d-120">Unesite sve potrebne informacije koje nedostaju ili po potrebi ažurirajte podrazumevane vrednosti na kartici **Rezime** ,</span><span class="sxs-lookup"><span data-stu-id="ecf6d-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="ecf6d-121">Izaberite stavku **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-121">Select **Save**.</span></span> <span data-ttu-id="ecf6d-122">Nova ponuda je kreirana i povezana sa mogućnošću za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="ecf6d-123">Sada možete da vidite informacije o ponudi na kartici **Ponude** na stranici **Mogućnost za poslovanje**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="ecf6d-124">Proces prodaje mogućnosti za poslovanje prelazi u sledeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="ecf6d-125">Ažuriranjem reference na mogućnost za poslovanje za postojeću ponudu</span><span class="sxs-lookup"><span data-stu-id="ecf6d-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="ecf6d-126">Postojeća ponuda se može povezati sa mogućnošću za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="ecf6d-127">Dovršite sledeće korake da biste ažurirali informacije o mogućnosti za poslovanje na postojećoj ponudi.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="ecf6d-128">Otvorite stranicu **Ponuda** i izaberite karticu **Rezime**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="ecf6d-129">U polju **Mogućnost za poslovanje** izaberite mogućnost za poslovanje koju želite da povežete sa ponudom.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="ecf6d-130">Ponudu možete videti u mreži **Ponude** mogućnosti za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="ecf6d-131">Koristeći proces prodaje mogućnosti za poslovanje, mogućnost za poslovanje se može prebaciti u sledeću fazu, **Predloži**.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="ecf6d-132">Kada premestite mogućnost za poslovanje u ovu fazu, možete da izaberete ovu ponudu sa liste ponuda povezanih sa ovom mogućnošću za poslovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="ecf6d-133">Izbor ove ponude ukazuje na to da napredujete sa njom.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="ecf6d-134">Sve ostale ponude povezane sa mogućnošću za poslovanje i dalje će biti dostupne i aktivne dok se jedna od njih ne ostvari.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="ecf6d-135">Proces prodaje možete da vratite u prethodnu fazu **Kvalifikovanje** i da odaberete drugu ponudu za napredovanje.</span><span class="sxs-lookup"><span data-stu-id="ecf6d-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
