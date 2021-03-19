---
title: Razumevanje statusa projekta
description: Ova tema pruža informacije o statusu dodeljenom projektima u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fc9b107507008fd2381d3669552d754d2c867a7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286490"
---
# <a name="understand-project-status"></a><span data-ttu-id="63063-103">Razumevanje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="63063-103">Understand project status</span></span>

<span data-ttu-id="63063-104">_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_</span><span class="sxs-lookup"><span data-stu-id="63063-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="63063-105">Odeljak **Status** na stranici **Entitet projekta** pruža rezime stanja ispravnosti projekta na osnovu troškova i angažovanja.</span><span class="sxs-lookup"><span data-stu-id="63063-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="63063-106">Polja rezimea statusa</span><span class="sxs-lookup"><span data-stu-id="63063-106">Status summary fields</span></span>

- <span data-ttu-id="63063-107">Polje **Opšti status projekta** je polje koje može da se uređuje i koje pokazuje opšti status projekta.</span><span class="sxs-lookup"><span data-stu-id="63063-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="63063-108">Ovo polje koristi kodiranje u boji, kao što su zelena, žuta i crvena, da ukaže na povećani rizik.</span><span class="sxs-lookup"><span data-stu-id="63063-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="63063-109">Polje **Komentari** omogućava menadžeru projekta da unese konkretne komentare o statusu.</span><span class="sxs-lookup"><span data-stu-id="63063-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="63063-110">Polje **Datum ažuriranja statusa** nije moguće uređivati.</span><span class="sxs-lookup"><span data-stu-id="63063-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="63063-111">Vrednost u ovom polju je vremenska oznaka koja pokazuje kada je status poslednji put ažuriran.</span><span class="sxs-lookup"><span data-stu-id="63063-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="63063-112">Polja **Performanse rasporeda** i **Performanse troškova** su podešena iz mreže za praćenje.</span><span class="sxs-lookup"><span data-stu-id="63063-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="63063-113">Kada su odstupanja od rasporeda i troškova za osnovni čvor u prikazu **Praćenje angažovanja** pozitivna, ova polja se ažuriraju na **Pre plana**.</span><span class="sxs-lookup"><span data-stu-id="63063-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="63063-114">Kada su odstupanja od rasporeda i troškova za osnovni čvor negativna, ova polja se podešavaju na **Zaostaje za planom**.</span><span class="sxs-lookup"><span data-stu-id="63063-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]