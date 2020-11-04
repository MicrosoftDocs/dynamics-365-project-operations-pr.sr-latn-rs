---
title: Razumevanje statusa projekta
description: Ova tema pruža informacije o statusu dodeljenom projektima u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083452"
---
# <a name="understand-project-status"></a><span data-ttu-id="4b301-103">Razumevanje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="4b301-103">Understand project status</span></span>

<span data-ttu-id="4b301-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="4b301-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4b301-105">Odeljak **Status** na stranici **Entitet projekta** pruža rezime stanja ispravnosti projekta na osnovu troškova i angažovanja.</span><span class="sxs-lookup"><span data-stu-id="4b301-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="4b301-106">Polja rezimea statusa</span><span class="sxs-lookup"><span data-stu-id="4b301-106">Status summary fields</span></span>

- <span data-ttu-id="4b301-107">Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta.</span><span class="sxs-lookup"><span data-stu-id="4b301-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="4b301-108">Ovo polje koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="4b301-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="4b301-109">Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="4b301-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="4b301-110">Polje **Datum ažuriranja statusa** nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="4b301-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="4b301-111">Vrednost u ovom polju je vremenska oznaka koja pokazuje kada je status poslednji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="4b301-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="4b301-112">Polja **Performanse rasporeda** i **Performanse troškova** se podešavaju u mreži za praćenje.</span><span class="sxs-lookup"><span data-stu-id="4b301-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="4b301-113">Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, možete ova se ažuriraju na **Pre plana**.</span><span class="sxs-lookup"><span data-stu-id="4b301-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="4b301-114">Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, ova polja se podešavaju na **Zaostaje za planom**.</span><span class="sxs-lookup"><span data-stu-id="4b301-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
