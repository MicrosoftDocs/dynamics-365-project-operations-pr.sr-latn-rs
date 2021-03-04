---
title: Obezbedite radne procene za projekat tokom prodajnog procesa
description: Kako da obezbedite radne procene za projekat tokom prodajnog procesa u aplikaciji Project Service
author: ruhercul
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
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147985"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="61ae0-103">Obezbedite radne procene za projekat tokom prodajnog procesa (Project Service)</span><span class="sxs-lookup"><span data-stu-id="61ae0-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="61ae0-104">Tokom procesa prodaje, možete praviti procene prodaje odozdo nagore sa predmetima ponude.</span><span class="sxs-lookup"><span data-stu-id="61ae0-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="61ae0-105">Mogućnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sistemu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pružaju više naučni i deterministički način za dobijanje procena prodaje razdvajanjem stavki posla i povezivanjem relevantnih atributa koji doprinose procenama za projekat u strukturnoj analizi posla.</span><span class="sxs-lookup"><span data-stu-id="61ae0-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="61ae0-106">Nakon što uspete da prodate, možete da koristite povezanu strukturnu analizu posla u planu projekta, po potrebi je precizirajući radi uspešnog obavljanja projekta.</span><span class="sxs-lookup"><span data-stu-id="61ae0-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="61ae0-107">Povezivanje projekta sa stavkom ponude</span><span class="sxs-lookup"><span data-stu-id="61ae0-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="61ae0-108">Kada kreirate stavku ponude na osnovu projekta, možete da kreirate novi projekat od stavke ponude.</span><span class="sxs-lookup"><span data-stu-id="61ae0-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="61ae0-109">Zatim možete da koristite predloške projekta koji su ili unapred konfigurisani standardni planovi projekta i finansijske procene uobičajene za vašu organizaciju ili kopije plana projekta i procene iz prošlog projekta.</span><span class="sxs-lookup"><span data-stu-id="61ae0-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="61ae0-110">Kada kreirate projekat, izbor predloška projekta pruža osnovu za preciziranje plana projekta, procena i zahteva za resursima.</span><span class="sxs-lookup"><span data-stu-id="61ae0-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="61ae0-111">Kreiranjem projekta iz ponude, projekat se automatski povezuje sa stavkom ponude.</span><span class="sxs-lookup"><span data-stu-id="61ae0-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="61ae0-112">Komponente procene za projekat</span><span class="sxs-lookup"><span data-stu-id="61ae0-112">Project estimate components</span></span>  
 <span data-ttu-id="61ae0-113">Strukturna analiza posla za projekat obezbeđuje način da podelite rad u zadatke, održavate hijerarhiju zadataka i dodelite procenu truda potrebnog da biste dovršili svaki zadatak.</span><span class="sxs-lookup"><span data-stu-id="61ae0-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="61ae0-114">Takođe možete da povežete uloge sa zadatkom da biste ukazali na procenu tipa resursa koji su potrebni za dovršenje zadatka i rasporeda.</span><span class="sxs-lookup"><span data-stu-id="61ae0-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="61ae0-115">Strukturna analiza posla vam pomaže da odredite procene rada i rasporeda.</span><span class="sxs-lookup"><span data-stu-id="61ae0-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="61ae0-116">Podrazumevano projekat koristi podrazumevane cenovnike koje ste ranije definisali.</span><span class="sxs-lookup"><span data-stu-id="61ae0-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="61ae0-117">Cene troškova i prodaje definisane u cenovnicima pomažu u utvrđivanju finansijskih procena za analizu posla za projekat.</span><span class="sxs-lookup"><span data-stu-id="61ae0-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="61ae0-118">Ako je vaš projekat povezan sa ponudom, a ponude ima neki drugi cenovnik od podrazumevanog, cenovnik ponude se koristi za finansijske procene.</span><span class="sxs-lookup"><span data-stu-id="61ae0-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="61ae0-119">Uvoz procena iz projekta u ponudu</span><span class="sxs-lookup"><span data-stu-id="61ae0-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="61ae0-120">Kada imate procene za projekat u projektu, možete uvoziti ove procene u stavke ponude:</span><span class="sxs-lookup"><span data-stu-id="61ae0-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="61ae0-121">U **Detalji stavke ponude**, kliknite na **Uvezi iz procena**.</span><span class="sxs-lookup"><span data-stu-id="61ae0-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="61ae0-122">Izaberite da li da uvezete procene za projekat grupisane po tipu transakcije, ulozi ili nivou čvora strukturne analize posla.</span><span class="sxs-lookup"><span data-stu-id="61ae0-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="61ae0-123">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="61ae0-123">See Also</span></span>  
 [<span data-ttu-id="61ae0-124">Vodič za menadžera projekta</span><span class="sxs-lookup"><span data-stu-id="61ae0-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
