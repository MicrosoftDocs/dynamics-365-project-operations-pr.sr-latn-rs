---
title: Prodajne procene i projekti
description: Ova tema pruža informacije o tome kako iskoristiti raspored i procene u procesu prodaje.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120695"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="57d9b-103">Prodajne procene i projekti</span><span class="sxs-lookup"><span data-stu-id="57d9b-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="57d9b-104">Tokom procesa prodaje možete kreirati procene prodaje povezujući projekat s prodajnom ponudom.</span><span class="sxs-lookup"><span data-stu-id="57d9b-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="57d9b-105">Na ovaj način, može da dođe do determinističke procene tokom procesa prodaje, kako bi se iskoristile prednosti zakazivanja projekata i procene.</span><span class="sxs-lookup"><span data-stu-id="57d9b-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="57d9b-106">Ako prodaja prođe, raspored koji je korišćen za procenu prodaje može se koristiti kao osnova za dalje preciziranje projektnog plana.</span><span class="sxs-lookup"><span data-stu-id="57d9b-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="57d9b-107">Povezivanje projekta sa stavkom ponude</span><span class="sxs-lookup"><span data-stu-id="57d9b-107">Linking a project to a quote line</span></span>

<span data-ttu-id="57d9b-108">Kada kreirate stavku ponude zasnovanu na projektu, možete da kreirate novi projekat ili povežete postojeći projekat na stranici **Stavka projekta**.</span><span class="sxs-lookup"><span data-stu-id="57d9b-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Obrazac stavke ponude](media/project-8.png)
 
<span data-ttu-id="57d9b-110">Kada kreirate novi projekat iz detalja stavke ponude, možete iskoristiti predloške projekta.</span><span class="sxs-lookup"><span data-stu-id="57d9b-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="57d9b-111">Predlošci projekata su modeli projekata koji predstavljaju standardne planove projekata i finansijske procene tipične za organizaciju.</span><span class="sxs-lookup"><span data-stu-id="57d9b-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="57d9b-112">Takođe mogu predstavljati kopije projektnih planova i procena iz prošlih projekata.</span><span class="sxs-lookup"><span data-stu-id="57d9b-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Detalji stavke ponude](media/project-9.png)
  
<span data-ttu-id="57d9b-114">Kada kreirate projekat iz ponude, projekat se automatski povezuje sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="57d9b-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="57d9b-115">Komponente procena u projektu</span><span class="sxs-lookup"><span data-stu-id="57d9b-115">Components of estimates in a project</span></span>

<span data-ttu-id="57d9b-116">Raspored vam omogućava da podelite posao na zadatke, održavate hijerarhiju zadataka, odredite koji su resursi potrebni za obavljanje zadatka i dodelite procenu potrebnih aktivnosti za obavljanje zadatka.</span><span class="sxs-lookup"><span data-stu-id="57d9b-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="57d9b-117">Možete definisati radne aktivnosti i procene rasporeda pomoću polja na kartici **Raspored** u okviru stranice **Projekat**.</span><span class="sxs-lookup"><span data-stu-id="57d9b-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="57d9b-118">Pošto je cenovnik povezan sa projektom, finansijske procene se izračunavaju korišćenjem cene koštanja i prodajne cene koje su definisane u cenovniku.</span><span class="sxs-lookup"><span data-stu-id="57d9b-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="57d9b-119">Uvoz procena iz projekta u ponudu</span><span class="sxs-lookup"><span data-stu-id="57d9b-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="57d9b-120">Nakon što definišete procene projekta, možete ih uvesti u stavku ponude.</span><span class="sxs-lookup"><span data-stu-id="57d9b-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="57d9b-121">Na stranici **Detalji stavke ponude** izaberite **Uvoz iz procena** na traci da biste rezimirali procene projekta prema vrsti transakcije, ulozi ili nivou zadatka.</span><span class="sxs-lookup"><span data-stu-id="57d9b-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
