---
title: Šta je novo u avgustu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Microsoft Dynamics 365 Project Operations za avgust 2022. za scenarije zasnovane na resursima/bez zaliha.
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

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.45.0.53
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | 2762089 | Greška pri rukovanju tokom zatvaranja ugovora kao neostvarenog ako je automatsko čuvanje onemogućeno u organizaciji.|
|Planiranje i praćenje projekta | 2767841 | Telemetrija ažurira scenarije kreiranja ili ažuriranja entiteta projekta.|
|Naplata i određivanje cena | 2771072 | Obrada izuzetka nulte reference tokom osvajanja ponude.|
|Naplata i određivanje cena | 2844181 |Nije uspelo dobijanje ID-a korelacije i blokiranje kreiranja fakture.|
|Naplata i određivanje cena | 2852836 | Nedostaju međukompanijske stvarne vrednosti za međukompanijski trošak kreiran i odobren u CE.|


### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
