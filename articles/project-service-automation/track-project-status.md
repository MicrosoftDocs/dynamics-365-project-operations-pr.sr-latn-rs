---
title: Pratite status projekta
description: Kako da pratite status projekta u aplikaciji Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755237"
---
# <a name="track-a-projects-status-project-service"></a>Praćenje statusa projekta (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Koristite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] da biste pratili tok projekta za klijenta.  

Kako angažovanje napreduje, faze projekta se ažuriraju tako da odražavaju fazu angažovanja:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Novo**    | Kada kreirate projekat, faza se postavlja na **Novo**. Ako ste kreirali projekat od predloška, u ovoj fazi projekat može imati raspored, procene i podatke o timu. U suprotnom, on će biti u nacrt projekta i potrebno je da ručno unesete ostatak komponenata projekta. |
|  **Ponuda**   |      Kada povežete projekat sa ponudom ili ga kreirate od ponude, faza projekta se postavlja na **Ponuda**, a procenjeni datumi početka i završetka se takođe ažuriraju. Kada je projekat je u fazi ponude, detalji ponude se prikazuju na kartici **Sales** na stranici **Projekat**.      |
|   **Plan**   |                                     Kada vam bude odobrena ponuda povezana sa projektom i kada angažovanje napreduje do faze ugovora, faza projekta se ažurira na **Plan**. Detalji o ugovoru se prikazuju na kartici **Sales** na stranici **Projekat**.                                      |
| **Dovrši** |                    Kada se posao na projektu završi, možete da prebacite fazu na **Dovršeno**. Kada se za fazu projekta podesi dovršavanje, smatra se da je posao dovršen 100%, ali projekat ostaje otvoren radi zavođenja stavki vremena ili troškova.                     |
|  **Zatvori**   |           Kada sve transakcije budu snimljene na projektu i ne očekujete više da se evidentiraju, možete ručno da postavite fazu **Zatvaranja**. Kada se projekat postavi na **Zatvaranje**ne možete više da zavodite transakcije na projektu i projekat će biti samo za čitanje.           |

## <a name="to-track-a-projects-status"></a>Praćenje statusa projekta  

1.  Idite na **Project Service > Projekti**.  

2.  Kliknite na projekat na kome želite da radite.  

3.  Na traci u vrhu ekrana izaberite strelicu nadole pored naziva projekta, a zatim kliknite na **Praćenje projekta**.  

4.  Izaberite **Praćenje angažovanja** ili **Praćenje troškova** u padajućoj listi iznad liste zadataka.  

5.  Kliknite dvaput na bilo koji zadatak da biste ga uredili. Takođe možete premestiti ili promeniti veličinu traka u gantogramu da biste promenili vreme i tok zadatka.  

### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za menadžera projekta](../project-service/project-manager-guide.md)
