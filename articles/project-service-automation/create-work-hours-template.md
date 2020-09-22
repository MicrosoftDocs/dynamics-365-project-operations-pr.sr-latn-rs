---
title: Kreirajte predložak za radne sate
description: Kako da kreirate predloške za radne sate u aplikaciji Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755193"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="ddcb2-103">Kreiranje predloška radnih sati (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ddcb2-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ddcb2-104">Da biste mogli da pravite rasporede projekta, morate da podesite kalendar projekta koji definiše broj radnih sati koje bi trebalo da obavite po danu u rasporedu i sve prekide poslovnih aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="ddcb2-105">To možete da uradite pomoću predloška za radne sate, koji sadrži detalje o radnim satima po danu, slobodnim dana i svim drugim prekidima poslovnih aktivnosti.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="ddcb2-106">Kada kreirate projekat, povezujete predložak rada sa kalendarom projekta da biste primenili raspored na projekat.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="ddcb2-107">Postoje dva načina da kreirate predložak za radne sate:</span><span class="sxs-lookup"><span data-stu-id="ddcb2-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="ddcb2-108">Kreirajte predložak za radne sate na osnovu kalendara resursa.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="ddcb2-109">Kreirajte novi predložak za radne sate.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="ddcb2-110">Da biste kreirali predložak za radne sate na osnovu kalendara resursa</span><span class="sxs-lookup"><span data-stu-id="ddcb2-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="ddcb2-111">Idite na **Project Service > Resursi**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="ddcb2-112">Izaberite resurs na kome želite da zasnujete radno vreme.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="ddcb2-113">Kliknite na dugme **Sačuvaj kalendar kao**, unesite ime za predložak za radne sate i kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="ddcb2-114">Kada završite sa promenom opcija, kliknite na **Sačuvaj i zatvori**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="ddcb2-115">Kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="ddcb2-116">Da biste kreirali novi predložak za radne sate.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="ddcb2-117">Idite u opciju **Project Service > Predlošci za radne sate**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="ddcb2-118">Kliknite na dugme **Novo**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="ddcb2-119">Unesite ime za predložak radnih časova.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="ddcb2-120">Izaberite resurs na kome ćete zasnovati radno vreme, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="ddcb2-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ddcb2-121">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="ddcb2-121">See Also</span></span>  
 [<span data-ttu-id="ddcb2-122">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="ddcb2-122">Set up resources</span></span>](../project-service/set-up-resources.md)
