---
title: Omogućavanje funkcija aplikacije Project Finder Mobile
description: Kako da omogućite funkcije aplikacije Project Finder Mobile za aplikaciju Project Service
author: JohnPBurrows
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: 1b70182125d607aa17528ef3dc4ea2345b76acd1
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144565"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a><span data-ttu-id="d5649-103">Omogućavanje funkcija aplikacije Project Finder Mobile (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d5649-103">Enable Project Finder Mobile app features (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d5649-104">Vaši resursi mogu da koriste aplikaciju Project Finder Mobile na telefonu uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da pronalaze nove projekte na kojima će raditi i da ažuriraju skupove veština.</span><span class="sxs-lookup"><span data-stu-id="d5649-104">Your resources can use the Project Finder Mobile app on their phone with [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to find new projects to work on and update their skillsets.</span></span>  
  
 <span data-ttu-id="d5649-105">Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span><span class="sxs-lookup"><span data-stu-id="d5649-105">The app is available for [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] phones, and [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].</span></span>  
    
 <span data-ttu-id="d5649-106">Da biste omogućili korisnicima pregled zahteva za resurse u projektima i ažuriranje njihovih veština, morate da izaberete opcije u podešavanjima parametara za organizacionu jedinicu.</span><span class="sxs-lookup"><span data-stu-id="d5649-106">To allow users to view project resource requirements and update skills, options must be selected in the parameter settings for your organizational unit.</span></span>
  
> [!NOTE]
>  <span data-ttu-id="d5649-107">Aplikacija Project Finder Mobile radi samo sa sistemom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], a ne sa lokalnim instalacijama.</span><span class="sxs-lookup"><span data-stu-id="d5649-107">The Project Finder Mobile app only works with [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], not with on-premises installations.</span></span>  
  
1. <span data-ttu-id="d5649-108">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="d5649-108">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="d5649-109">Kliknite na postavku parametara koje želite da koristite da biste omogućili funkcije aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="d5649-109">Click the parameters setting you want to use for allowing the Project Finder Mobile app features.</span></span>  
  
3. <span data-ttu-id="d5649-110">U oblasti **Opšti podaci**, postavite **Zahtevi u pogledu resursa vidljivi resursima** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="d5649-110">In the **General** area, set **Resource requirements visible to resources** to **Yes**.</span></span>  
  
4. <span data-ttu-id="d5649-111">Podesite **Dozvoli da resursi osveže veštine** na **Da**.</span><span class="sxs-lookup"><span data-stu-id="d5649-111">Set **Allow skill update by resource** to **Yes**.</span></span>  
  
   <span data-ttu-id="d5649-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span><span class="sxs-lookup"><span data-stu-id="d5649-112">![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")</span></span>  
  
   <span data-ttu-id="d5649-113">Ovo je globalno podešavanje.</span><span class="sxs-lookup"><span data-stu-id="d5649-113">This is a global setting.</span></span> <span data-ttu-id="d5649-114">Menadžeri projekta treba da podese da li će pojedinačni projekat biti vidljiv na stranici **Projektni tim** tog projekta.</span><span class="sxs-lookup"><span data-stu-id="d5649-114">Project managers can set whether an individual project will be visible on that project's **Project Team** page.</span></span>  
  
   <span data-ttu-id="d5649-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span><span class="sxs-lookup"><span data-stu-id="d5649-115">![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")</span></span>  
  
## <a name="email-notifications"></a><span data-ttu-id="d5649-116">Obaveštenja putem e-pošte</span><span class="sxs-lookup"><span data-stu-id="d5649-116">Email notifications</span></span>  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="d5649-117">šalje e-poruke koje se odnose na zahteve za resursima sledećim primaocima sledećim terminima:</span><span class="sxs-lookup"><span data-stu-id="d5649-117">sends emails regarding resource requests to the following recipients at the following times:</span></span>  
  
|<span data-ttu-id="d5649-118">Primalac</span><span class="sxs-lookup"><span data-stu-id="d5649-118">Recipient</span></span>|<span data-ttu-id="d5649-119">Događaj</span><span class="sxs-lookup"><span data-stu-id="d5649-119">Event</span></span>|  
|---------------|-----------|  
|<span data-ttu-id="d5649-120">Menadžer projekta</span><span class="sxs-lookup"><span data-stu-id="d5649-120">Project manager</span></span>|<span data-ttu-id="d5649-121">- Resurs se prijavljuje za projekat preko aplikacije Project Finder Mobile.</span><span class="sxs-lookup"><span data-stu-id="d5649-121">- A resource signs up for a project with the Project Finder Mobile app.</span></span>|  
|<span data-ttu-id="d5649-122">Resurs</span><span class="sxs-lookup"><span data-stu-id="d5649-122">Resource</span></span>|<span data-ttu-id="d5649-123">- Posao na projektu za koji se resurs prijavio je već ispunjen od strane drugog resursa.</span><span class="sxs-lookup"><span data-stu-id="d5649-123">- The project work that the resource has signed up for has already been fulfilled by another resource.</span></span><br /><span data-ttu-id="d5649-124">- Zahtevi za odobrenje veštine su odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="d5649-124">- The skill approval request has been approved or rejected.</span></span><br /><span data-ttu-id="d5649-125">- Zahtevi za prijavljivanje u projekat su odobreni ili odbačeni.</span><span class="sxs-lookup"><span data-stu-id="d5649-125">- The project sign-up request has been approved or rejected.</span></span>|  
  
## <a name="privacy-notice"></a><span data-ttu-id="d5649-126">Obaveštenje o privatnosti</span><span class="sxs-lookup"><span data-stu-id="d5649-126">Privacy notice</span></span>  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a><span data-ttu-id="d5649-127">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="d5649-127">See Also</span></span>  
 [<span data-ttu-id="d5649-128">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="d5649-128">Set up resources</span></span>](../psa/set-up-resources.md)
