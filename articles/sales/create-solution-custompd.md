---
title: Kreiranje rešenja za prilagođene dimenzije određivanja cena
description: Ova tema pruža informacije o tome kako da kreirate rešenja za prilagođene dimenzije određivanja cena.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514019"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="4b5fd-103">Kreiranje rešenja za prilagođene dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="4b5fd-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="4b5fd-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="4b5fd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="4b5fd-105">Sve promene prilagođenih dimenzija cene treba da budu u zasebnom rešenju.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="4b5fd-106">Ova važna najbolja praksa omogućava fleksibilnost za ažuriranje ili uklanjanje promena po potrebi, pomaže pri ponovnoj upotrebi posla i olakšava prilagođavanje ovih promena drugim instancama.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="4b5fd-107">Nakon što unesete sve potrebne promene, izvezite ovo rešenje kao **Kompletno** rešenje, pa ga uvezete u druge instance da biste ga ponovo koristili.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="4b5fd-108">Kreiranje rešenja za prilagođene dimenzije određivanja cena</span><span class="sxs-lookup"><span data-stu-id="4b5fd-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="4b5fd-109">Izaberite **Podešavanja** > **Rešenja**, a zatim izaberite **Novo**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="4b5fd-110">Imenujte rešenje, *<your organization name> dimenzije za određivanje cena*.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="4b5fd-111">Unesite preostale potrebne informacije, a zatim izaberite **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Kreiranje rešenja za prilagođene dimenzije za određivanje cena](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="4b5fd-113">Dodajte sve zahtevane entitete i srodne komponente u rešenje za dimenzije cene</span><span class="sxs-lookup"><span data-stu-id="4b5fd-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="4b5fd-114">Dodajte sledeće Project Service entitete u svoje rešenje za određivanje cena da biste uneli važne promene u šemi u rešenju za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="4b5fd-115">Nakon što završite ovaj postupak, entiteti će prepoznati nove dimenzije za određivanje cena.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="4b5fd-116">Izaberite **Podešavanja** > **Rešenja**, a zatim kliknite dvaput na **<*naziv vaše organizacije*> dimenzije za određivanje cena**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="4b5fd-117">U levom oknu za navigaciju istraživača rešenja izaberite **Dodaj postojeće** > **Entiteti**.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="4b5fd-118">U dijalogu **Komponente rešenja** izaberite sledeće entitete:</span><span class="sxs-lookup"><span data-stu-id="4b5fd-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="4b5fd-119">**Stvarna vrednost**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-119">**Actual**</span></span>
   - <span data-ttu-id="4b5fd-120">**Resurs koji može da se rezerviše**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="4b5fd-121">**Stavka procene**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-121">**Estimate Line**</span></span>
   - <span data-ttu-id="4b5fd-122">**Projektni zadatak**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-122">**Project Task**</span></span>
   - <span data-ttu-id="4b5fd-123">**Detalj stavke fakture**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="4b5fd-124">**Stavka u glavnoj knjizi**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-124">**Journal Line**</span></span>
   - <span data-ttu-id="4b5fd-125">**Detalj predmeta ugovora za projekat**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="4b5fd-126">**Član projektnog tima**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-126">**Project Team Member**</span></span>
   - <span data-ttu-id="4b5fd-127">**Detalj stavke ponude**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="4b5fd-128">**Provizija na cenu uloge**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="4b5fd-129">**Cena uloge**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-129">**Role Price**</span></span>
   - <span data-ttu-id="4b5fd-130">**Stavka vremena**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-130">**Time Entry**</span></span>
 
   ![Dodavanje rešenja sa prilagođenom dimenzijom određivanja cena postojećim entitetima](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="4b5fd-132">Za svaki entitet, pregledajte komponente koje se dodaju i konačnu listu sredstava entiteta za svaki entitet.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="4b5fd-133">Uključite sve obrasce i prikaze za svaki od izabranih entiteta.</span><span class="sxs-lookup"><span data-stu-id="4b5fd-133">Include all forms and views for each of the selected entities.</span></span>

  ![Dodati entiteti](./media/solution-component-selection.png)


5.  <span data-ttu-id="4b5fd-135">Kada se od vas zatraži da uključite bilo koji zavisni entitet za izabrane entitete, izaberite **Ne, ne uključuj obavezne komponente.**</span><span class="sxs-lookup"><span data-stu-id="4b5fd-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Uključivanje zavisnih entiteta](./media/Do-not-include-required.png)
