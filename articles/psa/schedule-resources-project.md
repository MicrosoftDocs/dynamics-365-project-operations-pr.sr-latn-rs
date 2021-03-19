---
title: Planirajte resurse za projekat
description: Kako da planirate resurse za projekat u aplikaciji Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f0a234f96419bac58cd932a082010da672e7dcb5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282665"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="f14c9-103">Planiranje resursa za projekat (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f14c9-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f14c9-104">Možete da proverite dostupnost resursa da biste dobili ukupan prikaz toga koliko su rezervisani resursi ili možete filtrirati prikaz prema veštinama, timu, lokaciji i ostalim opcijama.</span><span class="sxs-lookup"><span data-stu-id="f14c9-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="f14c9-105">Tabla rasporeda prikazuje listu resursa i njihovu dostupnost.</span><span class="sxs-lookup"><span data-stu-id="f14c9-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="f14c9-106">Izaberite režim prikaza za prikazivanje dostupnosti prema **Satima**, **Danima**, **Nedelji** ili **Mesecu**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="f14c9-107">Pre nego što možete da koristite tabelu rasporeda, važno je da je podesite.</span><span class="sxs-lookup"><span data-stu-id="f14c9-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="f14c9-108">Više informacija potražite u odeljku [Konfigurišite tablu rasporeda (Field Service ili Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="f14c9-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="f14c9-109">Ako koristite stariju verziju, za dostupnost resursa pogledajte [Prikaz dostupnosti resursa](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="f14c9-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="f14c9-110">Da biste koristili funkcionalnost rezervacije tabele rasporeda, geografsko kodiranje i usluge za lokaciju, potrebno je da uključite mape.</span><span class="sxs-lookup"><span data-stu-id="f14c9-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="f14c9-111">U glavnom meniju izaberite **Planiranje resursa** > **Administracija**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="f14c9-112">Kliknite na **Parametri planiranja**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="f14c9-113">Otvorite zapis i pomerite se nadole do odeljka **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="f14c9-114">U polju **Povezivanje sa mapama** odaberite **Da**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="f14c9-115">Prihvatite uslove i sačuvajte zapis.</span><span class="sxs-lookup"><span data-stu-id="f14c9-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="f14c9-116">U glavnom meniju izaberite **Project Service** > **Tabela rasporeda**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="f14c9-117">Odavde, postoji nekoliko načina da ručno zakažete zahtev za rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="f14c9-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="f14c9-118">Izaberite metod koji funkcioniše za vas.</span><span class="sxs-lookup"><span data-stu-id="f14c9-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="f14c9-119">Pronađite dostupne resurse</span><span class="sxs-lookup"><span data-stu-id="f14c9-119">Find available resources</span></span>

1.  <span data-ttu-id="f14c9-120">Na listi **Zahtev za rezervaciju** kliknite desnim tasterom miša na nezakazanu rezervaciju i izaberite jedno od sledećeg:</span><span class="sxs-lookup"><span data-stu-id="f14c9-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="f14c9-121">Odaberite **Pronađi dostupnost – Trenutni resursi** da biste pronašli dostupan resurs sa liste na tabli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="f14c9-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="f14c9-122">Odaberite **Pronađi dostupnost – Svi resursi**, da biste pronašli dostupan resurs u resursima u sistemu</span><span class="sxs-lookup"><span data-stu-id="f14c9-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="f14c9-123">Kada to uradite, filteri će prikazati opcije za izabrani zahtev za rezervaciju.</span><span class="sxs-lookup"><span data-stu-id="f14c9-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="f14c9-124">Kada vidite dostupni termin, kliknite desnim tasterom miša na vremenski interval na tabeli rasporeda i odaberite **Rezerviši ovde**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="f14c9-125">Ili prevucite i ispustite zahtev rezervacije na dostupan vremenski interval.</span><span class="sxs-lookup"><span data-stu-id="f14c9-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="f14c9-126">Rezervišite resurs pomoću dnevnog prikaza i pronađite ko nema dovoljno rezervacija</span><span class="sxs-lookup"><span data-stu-id="f14c9-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="f14c9-127">Na tabeli rasporeda, izaberite **Režim prikaza**, a zatim izaberite **Dani**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="f14c9-128">Ovo prikazuje prikaza koordinatne mreže koliko je sati resurs rezervisan po danu i kojim danima je slobodan.</span><span class="sxs-lookup"><span data-stu-id="f14c9-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="f14c9-129">Kliknite na ime resursa koji želite da rezervišete, a zatim izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="f14c9-130">U dijalogu **Rezervacija resursa (kreiranje)** izaberite projekat za koji želite da rezervišete resurs za zajedno sa metodom rezervacije i vremenima početka i završetka.</span><span class="sxs-lookup"><span data-stu-id="f14c9-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="f14c9-131">Kada završite, izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="f14c9-132">Prikaz tabele rasporeda</span><span class="sxs-lookup"><span data-stu-id="f14c9-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="f14c9-133">Izaberite nezakazani zahtev za rezervaciju sa liste na dnu.</span><span class="sxs-lookup"><span data-stu-id="f14c9-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="f14c9-134">Prevucite zahtev za rezervaciju na dostupni resurs/vremenski interval na tabli rasporeda.</span><span class="sxs-lookup"><span data-stu-id="f14c9-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="f14c9-135">Kada završite, izaberite **Rezerviši**.</span><span class="sxs-lookup"><span data-stu-id="f14c9-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="f14c9-136">Dodatni resursi</span><span class="sxs-lookup"><span data-stu-id="f14c9-136">Additional resources</span></span>  
 [<span data-ttu-id="f14c9-137">Vodič za menadžera resursa</span><span class="sxs-lookup"><span data-stu-id="f14c9-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]