---
title: Konfigurisanje podešavanja dodatnih parametara
description: Kako da konfigurišete podešavanja dodatnih parametara u usluzi Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755259"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="a1dd8-103">Konfigurisanje podešavanja dodatnih parametara (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a1dd8-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a1dd8-104">Kada konfigurišete stavke u prethodnim temama, treba da podesite dodatne parametre projekta koje ćete koristiti u projektima.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="a1dd8-105">Kada ste prvi put instalirali [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kreirali ste podešavanje parametara da prvo kreirate sve zapise potrebne kako bi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funkcionisao.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="a1dd8-106">Sada je vreme da se vratite i konfigurišete dodatna polja za ova podešavanja.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="a1dd8-107">Moraćete da konfigurišete sledeća podešavanja:</span><span class="sxs-lookup"><span data-stu-id="a1dd8-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="a1dd8-108">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="a1dd8-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="a1dd8-109">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="a1dd8-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="a1dd8-110">Predložak radnog vremena</span><span class="sxs-lookup"><span data-stu-id="a1dd8-110">Work hours template</span></span>  
  
-   <span data-ttu-id="a1dd8-111">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="a1dd8-111">Price list</span></span>  
 
<span data-ttu-id="a1dd8-112">U ovom koraku ćete takođe ukazati na tip dodele resursa koji želite:</span><span class="sxs-lookup"><span data-stu-id="a1dd8-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="a1dd8-113">**Centralni**.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-113">**Central**.</span></span> <span data-ttu-id="a1dd8-114">Samo menadžeri resursa mogu da dodeljuju resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="a1dd8-115">**Hibridni**.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-115">**Hybrid**.</span></span> <span data-ttu-id="a1dd8-116">Menadžeri resursa, menadžeri projekta i menadžeri poslovnog kontakta mogu da dodeljuju resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="a1dd8-117">Da biste podesili parametre projekta:</span><span class="sxs-lookup"><span data-stu-id="a1dd8-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="a1dd8-118">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="a1dd8-119">Kliknite na podešavanje parametara koje želite da konfigurišete (one koje ste kreirali kada ste prvi put instalirali [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) ili kliknite na **Novo** da biste kreirate novi.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="a1dd8-120">U oblasti **Opšti podaci**, podesite sve opcije za parametre projekta.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="a1dd8-121">U oblasti **Cenovnik** kliknite na **+** da biste dodali cenovnik, izaberite cenovnik u padajućoj listi **Cenovnik parametara projekta**, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="a1dd8-122">Kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="a1dd8-123">Zapis parametra projekta mora da se održava kako bi Project Service pravilno funkcionisao.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="a1dd8-124">Ovaj zapis ne bi trebalo brisati.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="a1dd8-125">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="a1dd8-125">See Also</span></span>  
 [<span data-ttu-id="a1dd8-126">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="a1dd8-126">Set up resources</span></span>](../project-service/set-up-resources.md)
