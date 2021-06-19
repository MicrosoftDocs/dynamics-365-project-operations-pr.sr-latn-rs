---
title: Pratite status projekta
description: Kako da pratite status projekta u aplikaciji Project Service
author: ruhercul
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
ms.openlocfilehash: 2385f7e52f3b5051b76daa9169f98bd73487e22d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014403"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="c7467-103">Praćenje statusa projekta (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c7467-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c7467-104">Koristite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] da biste pratili tok projekta za klijenta.</span><span class="sxs-lookup"><span data-stu-id="c7467-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="c7467-105">Kako angažovanje napreduje, faze projekta se ažuriraju tako da odražavaju fazu angažovanja:</span><span class="sxs-lookup"><span data-stu-id="c7467-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="c7467-106">**Novo**</span><span class="sxs-lookup"><span data-stu-id="c7467-106">**New**</span></span>    | <span data-ttu-id="c7467-107">Kada kreirate projekat, faza se postavlja na **Novo**.</span><span class="sxs-lookup"><span data-stu-id="c7467-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="c7467-108">Ako ste kreirali projekat od predloška, u ovoj fazi projekat može imati raspored, procene i podatke o timu.</span><span class="sxs-lookup"><span data-stu-id="c7467-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="c7467-109">U suprotnom, on će biti u nacrt projekta i potrebno je da ručno unesete ostatak komponenata projekta.</span><span class="sxs-lookup"><span data-stu-id="c7467-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="c7467-110">**Ponuda**</span><span class="sxs-lookup"><span data-stu-id="c7467-110">**Quote**</span></span>   |      <span data-ttu-id="c7467-111">Kada povežete projekat sa ponudom ili ga kreirate od ponude, faza projekta se postavlja na **Ponuda**, a procenjeni datumi početka i završetka se takođe ažuriraju.</span><span class="sxs-lookup"><span data-stu-id="c7467-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="c7467-112">Kada je projekat je u fazi ponude, detalji ponude se prikazuju na kartici **Sales** na stranici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="c7467-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="c7467-113">**Plan**</span><span class="sxs-lookup"><span data-stu-id="c7467-113">**Plan**</span></span>   |                                     <span data-ttu-id="c7467-114">Kada vam bude odobrena ponuda povezana sa projektom i kada angažovanje napreduje do faze ugovora, faza projekta se ažurira na **Plan**.</span><span class="sxs-lookup"><span data-stu-id="c7467-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="c7467-115">Detalji o ugovoru se prikazuju na kartici **Sales** na stranici **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="c7467-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="c7467-116">**Dovrši**</span><span class="sxs-lookup"><span data-stu-id="c7467-116">**Complete**</span></span> |                    <span data-ttu-id="c7467-117">Kada se posao na projektu završi, možete da prebacite fazu na **Dovršeno**.</span><span class="sxs-lookup"><span data-stu-id="c7467-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="c7467-118">Kada se za fazu projekta podesi dovršavanje, smatra se da je posao dovršen 100%, ali projekat ostaje otvoren radi zavođenja stavki vremena ili troškova.</span><span class="sxs-lookup"><span data-stu-id="c7467-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="c7467-119">**Zatvori**</span><span class="sxs-lookup"><span data-stu-id="c7467-119">**Close**</span></span>   |           <span data-ttu-id="c7467-120">Kada sve transakcije budu snimljene na projektu i ne očekujete više da se evidentiraju, možete ručno da postavite fazu **Zatvaranja**.</span><span class="sxs-lookup"><span data-stu-id="c7467-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="c7467-121">Kada se projekat postavi na **Zatvaranje** ne možete više da zavodite transakcije na projektu i projekat će biti samo za čitanje.</span><span class="sxs-lookup"><span data-stu-id="c7467-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="c7467-122">Praćenje statusa projekta</span><span class="sxs-lookup"><span data-stu-id="c7467-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="c7467-123">Idite na **Project Service > Projekti**.</span><span class="sxs-lookup"><span data-stu-id="c7467-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="c7467-124">Kliknite na projekat na kome želite da radite.</span><span class="sxs-lookup"><span data-stu-id="c7467-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="c7467-125">Na traci u vrhu ekrana izaberite strelicu nadole pored naziva projekta, a zatim kliknite na **Praćenje projekta**.</span><span class="sxs-lookup"><span data-stu-id="c7467-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="c7467-126">Izaberite **Praćenje angažovanja** ili **Praćenje troškova** u padajućoj listi iznad liste zadataka.</span><span class="sxs-lookup"><span data-stu-id="c7467-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="c7467-127">Kliknite dvaput na bilo koji zadatak da biste ga uredili.</span><span class="sxs-lookup"><span data-stu-id="c7467-127">Double-click any task to edit it.</span></span> <span data-ttu-id="c7467-128">Takođe možete premestiti ili promeniti veličinu traka u gantogramu da biste promenili vreme i tok zadatka.</span><span class="sxs-lookup"><span data-stu-id="c7467-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="c7467-129">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="c7467-129">See Also</span></span>  
 [<span data-ttu-id="c7467-130">Vodič za menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="c7467-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]