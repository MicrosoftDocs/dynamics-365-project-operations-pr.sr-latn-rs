---
title: Omogućavanje funkcija aplikacije Project Finder Mobile
description: Kako da omogućite funkcije aplikacije Project Finder Mobile za aplikaciju Project Service
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
ms.openlocfilehash: af267b5adc48b6edec57de196f91e338c058558c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132980"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="19b9a-103">Omogućavanje funkcija aplikacije Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="19b9a-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="19b9a-104">Vaši resursi mogu da koriste aplikaciju Project Finder Mobile na telefonu uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da pronalaze nove projekte na kojima će raditi i da ažuriraju skupove veština.</span><span class="sxs-lookup"><span data-stu-id="19b9a-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skill sets.</span></span>  
  
 <span data-ttu-id="19b9a-105">Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="19b9a-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
  
 <span data-ttu-id="19b9a-106">Treba da podesite nekoliko opcija u postavkama parametara za organizacionu jedinicu da biste omogućili korisnicima pregled zahteva za resursima u projektima i ažuriranje njihovih veština.</span><span class="sxs-lookup"><span data-stu-id="19b9a-106">You need to set a couple of options in the parameters setting for your organizational unit to allow users to view projects' resource requirements and update their skills.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="19b9a-107">Aplikacija Project Finder Mobile radi samo sa sistemom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], a ne sa lokalnim instalacijama.</span><span class="sxs-lookup"><span data-stu-id="19b9a-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="19b9a-108">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="19b9a-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="19b9a-109">Kliknite na postavku parametara koje želite da koristite da biste omogućili funkcije aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="19b9a-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="19b9a-110">U oblasti **Opšti podaci**, postavite **Zahtevi u pogledu resursa vidljivi resursima** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="19b9a-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="19b9a-111">Podesite **Dozvoli da resursi osveže veštine** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="19b9a-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="19b9a-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="19b9a-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="19b9a-113">Ovo je globalno podešavanje.</span><span class="sxs-lookup"><span data-stu-id="19b9a-113">This is a global setting.</span></span> <span data-ttu-id="19b9a-114">Menadžeri projekta treba da podese da li će pojedinačni projekat biti vidljiv na stranici **Projektni tim** tog projekta.</span><span class="sxs-lookup"><span data-stu-id="19b9a-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="19b9a-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="19b9a-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="19b9a-116">Obaveštenja putem e-pošte</span><span class="sxs-lookup"><span data-stu-id="19b9a-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="19b9a-117">šalje e-poruke koje se odnose na zahteve za resursima sledećim primaocima sledećim terminima:</span><span class="sxs-lookup"><span data-stu-id="19b9a-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="19b9a-118">Primalac</span><span class="sxs-lookup"><span data-stu-id="19b9a-118">Recipient</span></span>|<span data-ttu-id="19b9a-119">Događaj</span><span class="sxs-lookup"><span data-stu-id="19b9a-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="19b9a-120">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="19b9a-120">Project manager</span></span>|<span data-ttu-id="19b9a-121">-   Kada je resurs prijavljen za projekat preko aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="19b9a-121">-   When a resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="19b9a-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="19b9a-122">Resource</span></span>|<span data-ttu-id="19b9a-123">-   Kada je posao na projektu za koji se resurs prijavio već ispunjen od strane drugog resursa.</span><span class="sxs-lookup"><span data-stu-id="19b9a-123">-   When the project work the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="19b9a-124">-   Kada njihovi zahtevi za odobrenjem veštine budu odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="19b9a-124">-   When their skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="19b9a-125">-   Kada njihovi zahtevi za prijavljivanje u projekat budu odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="19b9a-125">-   When their project sign up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="19b9a-126">Obaveštenje o privatnosti</span><span class="sxs-lookup"><span data-stu-id="19b9a-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="19b9a-127">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="19b9a-127">See Also</span></span>  
 [<span data-ttu-id="19b9a-128">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="19b9a-128">Set up resources</span></span>](../psa/set-up-resources.md)
