---
title: Sinhronizacija kapaciteta resursa
description: Ova tema pruža informacije o tome kako sinhronizovati kapacitet resursa u kalendarima i projektima.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288589"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="4b957-103">Sinhronizacija kapaciteta resursa</span><span class="sxs-lookup"><span data-stu-id="4b957-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b957-104">Procesi za sinhronizaciju resursa garantuju da će se informacije za kalendar i osnovni kalendar slivati u planiranje resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="4b957-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="4b957-105">Ako se kalendar promeni, procesi izvršavaju potrebna ažuriranja rasporeda resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="4b957-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="4b957-106">Procesi takođe pomažu u poboljšanju performansi, jer su informacije o resursima kalendara unapred sinhronizovane.</span><span class="sxs-lookup"><span data-stu-id="4b957-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="4b957-107">Stoga se ažuriranja podataka o rasporedu resursa dešavaju brže.</span><span class="sxs-lookup"><span data-stu-id="4b957-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="4b957-108">Preporučujemo da procese planirate kao pakete umesto kao jedan po jedan.</span><span class="sxs-lookup"><span data-stu-id="4b957-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="4b957-109">U suprotnom, postoji rizik da će neko zaboraviti sve datume kada su informacije poslednji put sinhronizovane.</span><span class="sxs-lookup"><span data-stu-id="4b957-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="4b957-110">Ako se ne koriste svi datumi, mogu se pojaviti praznine tokom sinhronizacije datuma.</span><span class="sxs-lookup"><span data-stu-id="4b957-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Sinhronizacija kalendara](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="4b957-112">Sinhronizacija zbirnih vrednosti kapaciteta resursa</span><span class="sxs-lookup"><span data-stu-id="4b957-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="4b957-113">Proces sinhronizacije je dizajniran da sinhronizuje sve informacije kalendara resursa.</span><span class="sxs-lookup"><span data-stu-id="4b957-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="4b957-114">Ove informacije uključuju osnovne informacije o kalendaru o svim promenama u tabeli kapaciteta kalendara resursa projekta.</span><span class="sxs-lookup"><span data-stu-id="4b957-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="4b957-115">Ako se u projekat dodaju novi resursi, sinhronizacija garantuje dostupnost ažuriranih informacija kalendara.</span><span class="sxs-lookup"><span data-stu-id="4b957-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="4b957-116">Ova sinhronizacija se može izvršiti u bilo kom trenutku.</span><span class="sxs-lookup"><span data-stu-id="4b957-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="4b957-117">Preporučujemo da koristite paket.</span><span class="sxs-lookup"><span data-stu-id="4b957-117">We recommend that you use a batch.</span></span> <span data-ttu-id="4b957-118">Opcije su dostupne tokom sinhronizacije rezervacija kapaciteta.</span><span class="sxs-lookup"><span data-stu-id="4b957-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="4b957-119">Izaberite **Upravljanje projektima i računovodstvo** &gt; **Periodično** &gt; **Sinhronizacija kapaciteta** &gt; **Sinhronizuj zbirne vrednosti kapaciteta resursa**.</span><span class="sxs-lookup"><span data-stu-id="4b957-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="4b957-120">Podesite opcije u sledećoj tabeli.</span><span class="sxs-lookup"><span data-stu-id="4b957-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="4b957-121">Opcija</span><span class="sxs-lookup"><span data-stu-id="4b957-121">Option</span></span>      | <span data-ttu-id="4b957-122">Opis</span><span class="sxs-lookup"><span data-stu-id="4b957-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="4b957-123">Šifra perioda</span><span class="sxs-lookup"><span data-stu-id="4b957-123">Period code</span></span> | <span data-ttu-id="4b957-124">Opcionalno izaberite šifru intervala datuma glavne knjige da biste postavili datume početka i završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="4b957-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4b957-125">Datum početka</span><span class="sxs-lookup"><span data-stu-id="4b957-125">Start date</span></span>  | <span data-ttu-id="4b957-126">Unesite datum početka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="4b957-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="4b957-127">Datum završetka</span><span class="sxs-lookup"><span data-stu-id="4b957-127">End date</span></span>    | <span data-ttu-id="4b957-128">Unesite datum završetka procesa sinhronizacije za zbirne vrednosti kapaciteta resursa.</span><span class="sxs-lookup"><span data-stu-id="4b957-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="4b957-129">[![Proces sinhronizacije](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="4b957-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]