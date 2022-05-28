---
title: Šta je novo u maju 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ova tema pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u maju Dynamics 365 Project Operations 2022.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710171"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u maju 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.42.0.70
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta
### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje resursima | 2634019 | Poboljšane poruke o greškama za poslovne provere valjanosti prilikom dodavanja generičkih članova tima kao resursa. |
| Planiranje i praćenje projekta | 2648515 | Ograničene ispravke **ID-a**, **stanja** i **statusa** u entitetima za planiranje. |
| Naplata i određivanje cena | 2653167 | Znak za **razdvajanje** decimala koordinatne mreže "Procene" mora da prati postavke oblikovanja u opciji **"Lične opcije"**. |
| Naplata i određivanje cena| 2662251 | Vrednosti u poljima **"Ispravljena** jedinica" **i "Grupa** jedinica" podrazumevane prilikom kreiranja zapisa u procenama materijala. |
| Naplata i određivanje cena| 2571408 | Neželjene aktuele prodaje su pečatirane ID-om proforma fakture prilikom kreiranja radne fakture. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa (LCS) i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
