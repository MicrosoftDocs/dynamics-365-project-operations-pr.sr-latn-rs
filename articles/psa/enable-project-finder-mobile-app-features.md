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
ms.openlocfilehash: 5e4f3bf15589181e3095400c131d322184578afa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284645"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Omogućavanje funkcija aplikacije Project Finder Mobile (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Vaši resursi mogu da koriste aplikaciju Project Finder Mobile na telefonu uz [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] da pronalaze nove projekte na kojima će raditi i da ažuriraju skupove veština.  
  
 Aplikacija je dostupna za [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] telefone i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
    
 Da biste omogućili korisnicima pregled zahteva za resurse u projektima i ažuriranje njihovih veština, morate da izaberete opcije u podešavanjima parametara za organizacionu jedinicu.
  
> [!NOTE]
>  Aplikacija Project Finder Mobile radi samo sa sistemom [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], a ne sa lokalnim instalacijama.  
  
1. Idite na **Project Service > Parametri**.  
  
2. Kliknite na postavku parametara koje želite da koristite da biste omogućili funkcije aplikacije Project Finder Mobile.  
  
3. U oblasti **Opšti podaci**, postavite **Zahtevi u pogledu resursa vidljivi resursima** na **Da**.  
  
4. Podesite **Dozvoli da resursi osveže veštine** na **Da**.  
  
   ![ProjectService_ProjectFinderEnable](../psa/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   Ovo je globalno podešavanje. Menadžeri projekta treba da podese da li će pojedinačni projekat biti vidljiv na stranici **Projektni tim** tog projekta.  
  
   ![ProjectService_ProjectTeamVisible](../psa/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Obaveštenja putem e-pošte  
 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] šalje e-poruke koje se odnose na zahteve za resursima sledećim primaocima sledećim terminima:  
  
|Primalac|Događaj|  
|---------------|-----------|  
|Menadžer projekta|- Resurs se prijavljuje za projekat preko aplikacije Project Finder Mobile.|  
|Resurs|- Posao na projektu za koji se resurs prijavio je već ispunjen od strane drugog resursa.<br />- Zahtevi za odobrenje veštine su odobreni ili odbačeni.<br />- Zahtevi za prijavljivanje u projekat su odobreni ili odbačeni.|  
  
## <a name="privacy-notice"></a>Obaveštenje o privatnosti  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Podešavanje resursa](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]