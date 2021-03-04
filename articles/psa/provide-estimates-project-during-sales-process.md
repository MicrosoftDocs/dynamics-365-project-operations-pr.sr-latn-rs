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
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Obezbedite radne procene za projekat tokom prodajnog procesa (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Tokom procesa prodaje, možete praviti procene prodaje odozdo nagore sa predmetima ponude. Mogućnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] u sistemu [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] pružaju više naučni i deterministički način za dobijanje procena prodaje razdvajanjem stavki posla i povezivanjem relevantnih atributa koji doprinose procenama za projekat u strukturnoj analizi posla.  
  
 Nakon što uspete da prodate, možete da koristite povezanu strukturnu analizu posla u planu projekta, po potrebi je precizirajući radi uspešnog obavljanja projekta.  
  
## <a name="link-a-project-to-a-quote-line"></a>Povezivanje projekta sa stavkom ponude  
 Kada kreirate stavku ponude na osnovu projekta, možete da kreirate novi projekat od stavke ponude. Zatim možete da koristite predloške projekta koji su ili unapred konfigurisani standardni planovi projekta i finansijske procene uobičajene za vašu organizaciju ili kopije plana projekta i procene iz prošlog projekta. Kada kreirate projekat, izbor predloška projekta pruža osnovu za preciziranje plana projekta, procena i zahteva za resursima. Kreiranjem projekta iz ponude, projekat se automatski povezuje sa stavkom ponude.  
  
## <a name="project-estimate-components"></a>Komponente procene za projekat  
 Strukturna analiza posla za projekat obezbeđuje način da podelite rad u zadatke, održavate hijerarhiju zadataka i dodelite procenu truda potrebnog da biste dovršili svaki zadatak. Takođe možete da povežete uloge sa zadatkom da biste ukazali na procenu tipa resursa koji su potrebni za dovršenje zadatka i rasporeda.  
  
 Strukturna analiza posla vam pomaže da odredite procene rada i rasporeda. Podrazumevano projekat koristi podrazumevane cenovnike koje ste ranije definisali. Cene troškova i prodaje definisane u cenovnicima pomažu u utvrđivanju finansijskih procena za analizu posla za projekat.  
  
 Ako je vaš projekat povezan sa ponudom, a ponude ima neki drugi cenovnik od podrazumevanog, cenovnik ponude se koristi za finansijske procene.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Uvoz procena iz projekta u ponudu  
 Kada imate procene za projekat u projektu, možete uvoziti ove procene u stavke ponude:  
  
-   U **Detalji stavke ponude**, kliknite na **Uvezi iz procena**. 

-   Izaberite da li da uvezete procene za projekat grupisane po tipu transakcije, ulozi ili nivou čvora strukturne analize posla.  
  
### <a name="see-also"></a>Takođe pogledajte  
 [Vodič za menadžera projekta](../psa/project-manager-guide.md)
