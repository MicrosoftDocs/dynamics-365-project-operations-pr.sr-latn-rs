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
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755100"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogućavanje funkcija aplikacije Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši resursi mogu da koriste aplikaciju Project Finder Mobile na telefonu uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da pronalaze nove projekte na kojima će raditi i da ažuriraju skupove veština.  
  
 Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Treba da podesite nekoliko opcija u postavkama parametara za organizacionu jedinicu da biste omogućili korisnicima pregled zahteva za resursima u projektima i ažuriranje njihovih veština.  
  
> [!NOTE]
>  Aplikacija Project Finder Mobile radi samo sa sistemom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], a ne sa lokalnim instalacijama.  
  
1. Idite na **Project Service > Parametri**.  
  
2. Kliknite na postavku parametara koje želite da koristite da biste omogućili funkcije aplikacije Project Finder Mobile.  
  
3. U oblasti **Opšti podaci**, postavite **Zahtevi u pogledu resursa vidljivi resursima** na **Da**.  
  
4. Podesite **Dozvoli da resursi osveže veštine** na **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ovo je globalno podešavanje. Menadžeri projekta treba da podese da li će pojedinačni projekat biti vidljiv na stranici **Projektni tim** tog projekta.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Obaveštenja putem e-pošte  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] šalje e-poruke koje se odnose na zahteve za resursima sledećim primaocima sledećim terminima:  
  
|Primalac|Događaj|  
|---------------|-----------|  
|Menadžer projekta|-   Kada je resurs prijavljen za projekat preko aplikacije Project Finder Mobile.|  
|Resurs|-   Kada je posao na projektu za koji se resurs prijavio već ispunjen od strane drugog resursa.<br />-   Kada njihovi zahtevi za odobrenjem veštine budu odobreni ili odbačeni.<br />-   Kada njihovi zahtevi za prijavljivanje u projekat budu odobreni ili odbačeni.|  
  
## <a name="privacy-notice"></a>Obaveštenje o privatnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Podešavanje resursa](../project-service/set-up-resources.md)
