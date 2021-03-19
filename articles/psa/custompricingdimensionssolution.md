---
title: Kreiranje prilagođenih rešenja za dimenzije cene
description: U ovoj temi se objašnjava kako se kreira prilagođeno rešenje prilikom kreiranja prilagođenih dimenzija cene.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d8117d6f6bcedc97264401fc941470f34efb1ae
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285005"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="c900c-103">Kreiranje prilagođenih rešenja za dimenzije cene</span><span class="sxs-lookup"><span data-stu-id="c900c-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="c900c-104">Sve promene prilagođenih dimenzija cene treba da budu u zasebnom rešenju.</span><span class="sxs-lookup"><span data-stu-id="c900c-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="c900c-105">Ova važna najbolja praksa pruža fleksibilnost u budućnosti za ažuriranje ili uklanjanje promena po potrebi, pomoći će pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugoj instanci.</span><span class="sxs-lookup"><span data-stu-id="c900c-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="c900c-106">Kada unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno rešenje** i uvezite ga u druge instance da biste ponovo koristili podešavanje za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="c900c-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="c900c-107">Izaberite **Podešavanja** > **Rešenja**, a zatim izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c900c-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="c900c-108">Imenujte rešenje, **\<your organization name> dimenzije za određivanje cena**, unesite preostale zahtevane informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="c900c-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Kreiranje prilagođenog rešenja za dimenzije za određivanje cena](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c900c-110">Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije cene</span><span class="sxs-lookup"><span data-stu-id="c900c-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="c900c-111">Moraćete da dodate sledeće Project Service entitete u rešenje za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="c900c-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="c900c-112">Dovršite korake u ovoj proceduri da biste napravili neke važne promene šema u rešenju za određivanje cena, tako da entiteti postanu svesni novih dimenzija cene.</span><span class="sxs-lookup"><span data-stu-id="c900c-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="c900c-113">Izaberite **Podešavanja** > **Rešenja**, a zatim dvaput kliknite na **\<your organization name> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="c900c-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="c900c-114">U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="c900c-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="c900c-115">U dijalogu **Komponente rešenja** izaberite sledeće entitete:</span><span class="sxs-lookup"><span data-stu-id="c900c-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="c900c-116">Stvarna vrednost</span><span class="sxs-lookup"><span data-stu-id="c900c-116">Actual</span></span>
- <span data-ttu-id="c900c-117">Resurs koji može da se rezerviše</span><span class="sxs-lookup"><span data-stu-id="c900c-117">Bookable Resource</span></span>
- <span data-ttu-id="c900c-118">Stavka procene</span><span class="sxs-lookup"><span data-stu-id="c900c-118">Estimate Line</span></span>
- <span data-ttu-id="c900c-119">Projektni zadatak</span><span class="sxs-lookup"><span data-stu-id="c900c-119">Project Task</span></span>
- <span data-ttu-id="c900c-120">Detalj stavke fakture</span><span class="sxs-lookup"><span data-stu-id="c900c-120">Invoice Line Detail</span></span>
- <span data-ttu-id="c900c-121">Stavka u glavnoj knjizi</span><span class="sxs-lookup"><span data-stu-id="c900c-121">Journal Line</span></span>
- <span data-ttu-id="c900c-122">Detalj predmeta ugovora za projekat</span><span class="sxs-lookup"><span data-stu-id="c900c-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="c900c-123">Član projektnog tima</span><span class="sxs-lookup"><span data-stu-id="c900c-123">Project Team Member</span></span>
- <span data-ttu-id="c900c-124">Detalj stavke ponude</span><span class="sxs-lookup"><span data-stu-id="c900c-124">Quote Line Detail</span></span>
- <span data-ttu-id="c900c-125">Provizija na cenu uloge</span><span class="sxs-lookup"><span data-stu-id="c900c-125">Role Price Markup</span></span>
- <span data-ttu-id="c900c-126">Cena uloge</span><span class="sxs-lookup"><span data-stu-id="c900c-126">Role Price</span></span> 
- <span data-ttu-id="c900c-127">Stavka vremena</span><span class="sxs-lookup"><span data-stu-id="c900c-127">Time Entry</span></span> 

> ![Dodavanje postojećih entiteta u rešenje za dimenzije određivanja cena](media/Existing-entities-to-PD-solution.png)

> ![Izaberite komponente rešenja](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="c900c-130">Obavezno uključite sve obrasce i prikaze za svaki od izabranih entiteta.</span><span class="sxs-lookup"><span data-stu-id="c900c-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="c900c-131">Kada se od vas zatraži da uključite zavisne entitete za izabrane entitete, izaberite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="c900c-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Nemojte da uključujete sve povezane komponente](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]