---
title: Omogućavanje funkcija aplikacije Project Finder Mobile
description: Kako da omogućite funkcije aplikacije Project Finder Mobile za aplikaciju Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 749c5682dc2e639843a0a8a085fe8af65502d433
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083587"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="3bd1f-103">Omogućavanje funkcija aplikacije Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3bd1f-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3bd1f-104">Vaši resursi mogu da koriste aplikaciju Project Finder Mobile na telefonu uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da pronalaze nove projekte na kojima će raditi i da ažuriraju skupove veština.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="3bd1f-105">Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="3bd1f-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="3bd1f-106">Treba da podesite nekoliko opcija u postavkama parametara za organizacionu jedinicu da biste omogućili korisnicima pregled zahteva za resursima u projektima i ažuriranje njihovih veština.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="3bd1f-107">Aplikacija Project Finder Mobile radi samo sa sistemom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], a ne sa lokalnim instalacijama.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="3bd1f-108">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="3bd1f-109">Kliknite na postavku parametara koje želite da koristite da biste omogućili funkcije aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="3bd1f-110">U oblasti **Opšti podaci** , postavite **Zahtevi u pogledu resursa vidljivi resursima** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="3bd1f-111">Podesite **Dozvoli da resursi osveže veštine** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="3bd1f-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="3bd1f-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="3bd1f-113">Ovo je globalno podešavanje.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-113">This is a global setting.</span></span> <span data-ttu-id="3bd1f-114">Menadžeri projekta treba da podese da li će pojedinačni projekat biti vidljiv na stranici **Projektni tim** tog projekta.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="3bd1f-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="3bd1f-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="3bd1f-116">Obaveštenja putem e-pošte</span><span class="sxs-lookup"><span data-stu-id="3bd1f-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="3bd1f-117">šalje e-poruke koje se odnose na zahteve za resursima sledećim primaocima sledećim terminima:</span><span class="sxs-lookup"><span data-stu-id="3bd1f-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="3bd1f-118">Primalac</span><span class="sxs-lookup"><span data-stu-id="3bd1f-118">Recipient</span></span>|<span data-ttu-id="3bd1f-119">Događaj</span><span class="sxs-lookup"><span data-stu-id="3bd1f-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="3bd1f-120">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="3bd1f-120">Project manager</span></span>|<span data-ttu-id="3bd1f-121">-   Kada je resurs prijavljen za projekat preko aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="3bd1f-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="3bd1f-122">Resource</span></span>|<span data-ttu-id="3bd1f-123">-   Kada je posao na projektu za koji se resurs prijavio već ispunjen od strane drugog resursa.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="3bd1f-124">-   Kada njihovi zahtevi za odobrenjem veštine budu odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="3bd1f-125">-   Kada njihovi zahtevi za prijavljivanje u projekat budu odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="3bd1f-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="3bd1f-126">Obaveštenje o privatnosti</span><span class="sxs-lookup"><span data-stu-id="3bd1f-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="3bd1f-127">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="3bd1f-127">See Also</span></span>  
 [<span data-ttu-id="3bd1f-128">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="3bd1f-128">Set up resources</span></span>](../psa/set-up-resources.md)
