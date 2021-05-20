---
title: Performanse predloga projektnih faktura
description: Ova tema pruža informacije o poboljšanjima performansi predloga projektnih faktura.
author: Yowelle
manager: AnnBe
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1641d5f731029fdbdc16c4b652cc752a583058c6
ms.sourcegitcommit: 68d52fc983861114e654ffc8d2472b4db9b48981
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920319"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="f3e60-103">Performanse predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="f3e60-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3e60-104">Kada kreirate novi predlog fakture, možda ćete naići na probleme sa performansama kako se bude povećavao broj projekata i potprojekata.</span><span class="sxs-lookup"><span data-stu-id="f3e60-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="f3e60-105">Da bi se poboljšale performanse, dostupna je funkcija koja smanjuje vreme potrebno za kreiranje novog predloga fakture za knjižene transakcije projekata.</span><span class="sxs-lookup"><span data-stu-id="f3e60-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f3e60-106">Omogućite poboljšanje performansi predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="f3e60-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f3e60-107">Da biste omogućili funkciju poboljšanja performansi predloga projektnih faktura, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="f3e60-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="f3e60-108">Idite na **Upravljanje funkcijama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f3e60-109">Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f3e60-110">Izaberite dugme **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="f3e60-111">Osvežite pregledač, a zatim napravite novi predlog fakture.</span><span class="sxs-lookup"><span data-stu-id="f3e60-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="f3e60-112">Isključite poboljšanje performansi predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="f3e60-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="f3e60-113">Izvršite sledeće korake da biste isključili funkciju poboljšanja performansi predloga projektnih faktura.</span><span class="sxs-lookup"><span data-stu-id="f3e60-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="f3e60-114">Idite na **Upravljanje funkcijama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="f3e60-115">Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="f3e60-116">Izaberite dugme **Onemogući**.</span><span class="sxs-lookup"><span data-stu-id="f3e60-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="f3e60-117">Osvežite pregledač.</span><span class="sxs-lookup"><span data-stu-id="f3e60-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="f3e60-118">Performanse predloga fakture ne može se primeniti kada su omogućena pravila obračuna ili su pokrenute grupne obrade.</span><span class="sxs-lookup"><span data-stu-id="f3e60-118">Invoice proposal performance can't be applied when billing rules are enabled or batch processes are running.</span></span>
