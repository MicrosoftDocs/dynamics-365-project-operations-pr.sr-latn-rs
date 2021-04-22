---
title: Deaktiviranje cenovnika
description: Ova tema objašnjava kako da deaktivirate ili uklonite neiskorišćene ili stare cenovnike.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701968"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="cdc9c-103">Deaktiviranje cenovnika</span><span class="sxs-lookup"><span data-stu-id="cdc9c-103">Deactivate price lists</span></span> 

<span data-ttu-id="cdc9c-104">_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="cdc9c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cdc9c-105">Da biste uklonili stare ili neiskorišćene cenovnike iz usluge Dynamics 365 Project Operations, postoje dva koraka koja morate izvršiti.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="cdc9c-106">Uklonite ili izbrišite cenovnik sa određenih stranica.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="cdc9c-107">Deaktivirajte ili izbrišite cenovnik iz aktivnih cenovnika na stranici **Cenovnici**.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="cdc9c-108">Morate obaviti oba koraka da biste u potpunosti uklonili cenovnik.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="cdc9c-109">Nije dovoljno da obavite samo 2. korak, a to je direktno brisanje ili deaktiviranje cenovnika iz prikaza Aktivni cenovnici.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="cdc9c-110">Morate izbrisati i povezivanje ovog cenovnika sa svih mesta pomenutih u 1. koraku.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="cdc9c-111">Brisanje cenovnika sa određenih stranica</span><span class="sxs-lookup"><span data-stu-id="cdc9c-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="cdc9c-112">Da biste izbrisali cenovnik iz usluge Project Operations, idite na sledeće stranice:</span><span class="sxs-lookup"><span data-stu-id="cdc9c-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="cdc9c-113">Stranica **Parametri projekta** > kartica **Cenovnici**</span><span class="sxs-lookup"><span data-stu-id="cdc9c-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="cdc9c-114">Stranica **Organizaciona jedinica** > mreža **Cenovnici**</span><span class="sxs-lookup"><span data-stu-id="cdc9c-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="cdc9c-115">Stranica **Poslovni kontakt** > mreža **Cenovnici projekta**</span><span class="sxs-lookup"><span data-stu-id="cdc9c-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="cdc9c-116">Stranica **Ponude za projekat** > mreža **Cenovnici projekta**: Ovo se odnosi na sve aktivne ponude za projekat.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="cdc9c-117">Stranica **Ugovori o projektu** > mreža **Cenovnici projekta**: Ovo se odnosi na sve aktivne ugovore o projektu.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="cdc9c-118">Za svaku stranicu, morate izabrati cenovnik koji želite da izbrišete, a zatim izaberite **Izbriši**.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="cdc9c-119">Brisanje ili deaktiviranje cenovnika sa stranice Cenovnici</span><span class="sxs-lookup"><span data-stu-id="cdc9c-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="cdc9c-120">Da biste izbrisali cenovnik iz aktivnih cenovnika, idite na **Prodaja** > **Klijenti** > **Cenovnici**.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="cdc9c-121">Izaberite cenovnik koji želite da izbrišete, a zatim izaberite **Izbriši**.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="cdc9c-122">Ako se cenovnik koristi u bilo kojoj transakciji, nećete moći da ga izbrišete.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="cdc9c-123">Ako se to dogodi, možete deaktivirati cenovnik tako da se ne prikazuje ni u jednom prikazu.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="cdc9c-124">Da biste deaktivirali cenovnik, ponovo izaberite cenovnik, a zatim izaberite **Deaktiviraj**.</span><span class="sxs-lookup"><span data-stu-id="cdc9c-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
