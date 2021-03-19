---
title: Konfigurisanje podešavanja dodatnih parametara
description: Kako da konfigurišete podešavanja dodatnih parametara u usluzi Project Service
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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290781"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="6e9d9-103">Konfigurisanje podešavanja dodatnih parametara (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6e9d9-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6e9d9-104">Kada konfigurišete stavke u prethodnim temama, treba da podesite dodatne parametre projekta koje ćete koristiti u projektima.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="6e9d9-105">Kada ste prvi put instalirali [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kreirali ste podešavanje parametara da prvo kreirate sve zapise potrebne kako bi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] funkcionisao.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="6e9d9-106">Sada je vreme da se vratite i konfigurišete dodatna polja za ova podešavanja.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="6e9d9-107">Moraćete da konfigurišete sledeća podešavanja:</span><span class="sxs-lookup"><span data-stu-id="6e9d9-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="6e9d9-108">Organizaciona jedinica</span><span class="sxs-lookup"><span data-stu-id="6e9d9-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="6e9d9-109">Učestalost fakturisanja</span><span class="sxs-lookup"><span data-stu-id="6e9d9-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="6e9d9-110">Predložak radnog vremena</span><span class="sxs-lookup"><span data-stu-id="6e9d9-110">Work hours template</span></span>  
  
-   <span data-ttu-id="6e9d9-111">Cenovnik</span><span class="sxs-lookup"><span data-stu-id="6e9d9-111">Price list</span></span>  
 
<span data-ttu-id="6e9d9-112">U ovom koraku ćete takođe ukazati na tip dodele resursa koji želite:</span><span class="sxs-lookup"><span data-stu-id="6e9d9-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="6e9d9-113">**Centralni**.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-113">**Central**.</span></span> <span data-ttu-id="6e9d9-114">Samo menadžeri resursa mogu da dodeljuju resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="6e9d9-115">**Hibridni**.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-115">**Hybrid**.</span></span> <span data-ttu-id="6e9d9-116">Menadžeri resursa, menadžeri projekta i menadžeri poslovnog kontakta mogu da dodeljuju resurse projektima.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="6e9d9-117">Da biste podesili parametre projekta:</span><span class="sxs-lookup"><span data-stu-id="6e9d9-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="6e9d9-118">Idite na **Project Service > Parametri**.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="6e9d9-119">Kliknite na podešavanje parametara koje želite da konfigurišete (one koje ste kreirali kada ste prvi put instalirali [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) ili kliknite na **Novo** da biste kreirate novi.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="6e9d9-120">U oblasti **Opšti podaci**, podesite sve opcije za parametre projekta.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="6e9d9-121">U oblasti **Cenovnik** kliknite na **+** da biste dodali cenovnik, izaberite cenovnik u padajućoj listi **Cenovnik parametara projekta**, a zatim kliknite na **Sačuvaj**.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="6e9d9-122">Kliknite na dugme **Sačuvaj** u donjem desnom uglu ekrana.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="6e9d9-123">Zapis parametra projekta mora da se održava kako bi Project Service pravilno funkcionisao.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="6e9d9-124">Ovaj zapis ne bi trebalo brisati.</span><span class="sxs-lookup"><span data-stu-id="6e9d9-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="6e9d9-125">Takođe pogledajte</span><span class="sxs-lookup"><span data-stu-id="6e9d9-125">See Also</span></span>  
 [<span data-ttu-id="6e9d9-126">Podešavanje resursa</span><span class="sxs-lookup"><span data-stu-id="6e9d9-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]