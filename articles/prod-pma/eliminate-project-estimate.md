---
title: Eliminisanje procene za projekat
description: Ova tema pruža informacije o eliminisanju procene projekta nakon što je završena.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270695"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="94593-103">Eliminisanje procene za projekat</span><span class="sxs-lookup"><span data-stu-id="94593-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94593-104">Procene projekta pružaju finansijski prikaz za posao koji je procenjen i zakazan za projekat.</span><span class="sxs-lookup"><span data-stu-id="94593-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="94593-105">Da biste radili sa procenama za projekat, morate priložiti projekat projektu za procenu.</span><span class="sxs-lookup"><span data-stu-id="94593-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="94593-106">Projekt procene uvek se zasniva na postojećem projektu, međutim više projekata može se odnositi na jedan projekat procene.</span><span class="sxs-lookup"><span data-stu-id="94593-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="94593-107">Za procenu projekata mogu se priložiti samo projekti sa fiksnom cenom i investicioni projekti, koji moraju pripadati istoj projektnoj grupi kao i projekat procene.</span><span class="sxs-lookup"><span data-stu-id="94593-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="94593-108">Da bi se eliminisao projekt procene, on mora biti potpun.</span><span class="sxs-lookup"><span data-stu-id="94593-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="94593-109">Sledeći koraci objašnjavaju kako eliminisati procenu.</span><span class="sxs-lookup"><span data-stu-id="94593-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="94593-110">Idite na **Upravljanje projektima i računovodstvo** > **Svi projekti** i otvorite projekat.</span><span class="sxs-lookup"><span data-stu-id="94593-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="94593-111">Na kartici **Upravljanje** izaberite **Procene** i na stranici **Procena** izaberite stranicu **Eliminisanje**.</span><span class="sxs-lookup"><span data-stu-id="94593-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="94593-112">Na stranici **Eliminišite procenu** na kartici **Opšti podaci** postavite sledeće opcije:</span><span class="sxs-lookup"><span data-stu-id="94593-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="94593-113">**Šifra perioda**: Izaberite šifru perioda da biste izabrali odgovarajuće procene projekata.</span><span class="sxs-lookup"><span data-stu-id="94593-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="94593-114">**Datum procene**: Izaberite odgovarajući datum procene za eliminisanje.</span><span class="sxs-lookup"><span data-stu-id="94593-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="94593-115">**Eliminišite WIP upozorenja**: Omogućite ovu opciju da biste pružili obaveštenje kada će procena koja je povezana sa radom u toku (WIP) biti uklonjena.</span><span class="sxs-lookup"><span data-stu-id="94593-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="94593-116">Kada ova opcija nije omogućena, uklanjanje se ne može nastaviti ako postoje neprocenjene transakcije.</span><span class="sxs-lookup"><span data-stu-id="94593-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="94593-117">Ova opcija je dostupna samo kada se eliminacija primenjuje na procenjeni projekat.</span><span class="sxs-lookup"><span data-stu-id="94593-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="94593-118">Nije dostupna ako koristite periodična objavljivanja.</span><span class="sxs-lookup"><span data-stu-id="94593-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="94593-119">Ovo podešavanje radi sa podešavanjima na kartici **Procena**, na stranici **Parametri projekta**, u grupi polja **Dozvolite eliminaciju kada postoje neprocenjene transakcije**.</span><span class="sxs-lookup"><span data-stu-id="94593-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="94593-120">**Postavite fazu na Završeno**: Omogućite ovu opciju da biste postavili fazu procene projekta na **Završeno** nakon što pokrenete eliminaciju.</span><span class="sxs-lookup"><span data-stu-id="94593-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="94593-121">**Odštampajte listu procena**: Izaberite informacije koje će biti uključene kada se odštampa lista procena.</span><span class="sxs-lookup"><span data-stu-id="94593-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="94593-122">**Prikaži Infolog**: Omogućite ovu opciju za prikaz Infolog-a.</span><span class="sxs-lookup"><span data-stu-id="94593-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="94593-123">**Datum knjiženja**: Izaberite datum knjiženja procene u knjizi.</span><span class="sxs-lookup"><span data-stu-id="94593-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="94593-124">Izaberite **U redu**.</span><span class="sxs-lookup"><span data-stu-id="94593-124">Select **OK**.</span></span>
5. <span data-ttu-id="94593-125">Nakon završetka postupka eliminacije, projekat sa eliminisanom procenom prikazuje se sa negativnom vrednošću.</span><span class="sxs-lookup"><span data-stu-id="94593-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="94593-126">Ako niste nameravali da eliminišete procenu, možete da izaberete eliminisanu procenu i izaberete **Opozovi eliminaciju**.</span><span class="sxs-lookup"><span data-stu-id="94593-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]