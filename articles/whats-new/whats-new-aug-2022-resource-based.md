---
title: Šta je novo u avgustu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft Dynamics 365 Project Operations u avgustu 2022.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403874"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u avgustu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.45.0.53
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | 2762089 | Rukovanje greškom tokom zatvaranja ugovora kao izgubljeno ako je automatsko čuvanje onemogućeno u org.|
|Planiranje i praćenje projekta | 2767841 | Telemetrija ažurira scenarije kreiranja ili ažuriranja entiteta projekta.|
|Naplata i određivanje cena | 2771072 | Bez referenci za rukovanje izuzetkom tokom pobedničkog citata.|
|Naplata i određivanje cena | 2844181 |Nije uspelo dobijanje ID-a korelacije i blokiranje kreiranja fakture.|
|Naplata i određivanje cena | 2852836 | Nedostaju međukompanijske stvarne stvari za međukompanijski trošak kreiran i odobren u CE.|


### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u finansijama

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa (LCS) i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
