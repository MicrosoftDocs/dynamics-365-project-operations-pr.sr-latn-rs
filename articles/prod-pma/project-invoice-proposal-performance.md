---
title: Performanse predloga projektnih faktura
description: Ova tema pruža informacije o poboljšanjima performansi predloga projektnih faktura.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269807"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="d34dc-103">Performanse predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="d34dc-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d34dc-104">Kada kreirate novi predlog fakture, možda ćete naići na probleme sa performansama kako se bude povećavao broj projekata i potprojekata.</span><span class="sxs-lookup"><span data-stu-id="d34dc-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="d34dc-105">Da bi se poboljšale performanse, dostupna je funkcija koja smanjuje vreme potrebno za kreiranje novog predloga fakture za knjižene transakcije projekata.</span><span class="sxs-lookup"><span data-stu-id="d34dc-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d34dc-106">Omogućite poboljšanje performansi predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="d34dc-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d34dc-107">Da biste omogućili funkciju poboljšanja performansi predloga projektnih faktura, izvršite sledeće korake.</span><span class="sxs-lookup"><span data-stu-id="d34dc-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="d34dc-108">Idite na **Upravljanje funkcijama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d34dc-109">Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d34dc-110">Izaberite dugme **Omogući odmah**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="d34dc-111">Osvežite pregledač, a zatim napravite novi predlog fakture.</span><span class="sxs-lookup"><span data-stu-id="d34dc-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="d34dc-112">Isključite poboljšanje performansi predloga projektnih faktura</span><span class="sxs-lookup"><span data-stu-id="d34dc-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="d34dc-113">Izvršite sledeće korake da biste isključili funkciju poboljšanja performansi predloga projektnih faktura.</span><span class="sxs-lookup"><span data-stu-id="d34dc-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="d34dc-114">Idite na **Upravljanje funkcijama** > **Sve**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="d34dc-115">Na listi funkcija, pronađite **Poboljšanje performansi predloga projektnih faktura**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="d34dc-116">Izaberite dugme **Onemogući**.</span><span class="sxs-lookup"><span data-stu-id="d34dc-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="d34dc-117">Osvežite pregledač.</span><span class="sxs-lookup"><span data-stu-id="d34dc-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="d34dc-118">Performanse predloga fakture se ne mogu primeniti kada su omogućena pravila obračuna.</span><span class="sxs-lookup"><span data-stu-id="d34dc-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="d34dc-119">Tokom grupnog postupka za kreiranje predloga faktura, broj podzadataka podeliće zadatke na maksimalan broj na osnovu broja ugovora sa transakcijama podložnim fakturisanju, bez obzira na to šta ste uneli.</span><span class="sxs-lookup"><span data-stu-id="d34dc-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="d34dc-120">Na primer, ako unesete **3** za broj podzadataka za kreiranje predloga fakture u paketu, a postoje samo dva ugovora sa transakcijama koje mogu da se fakturišu, kreiraju se samo dva podzadatka.</span><span class="sxs-lookup"><span data-stu-id="d34dc-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
