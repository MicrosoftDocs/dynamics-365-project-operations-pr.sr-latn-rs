---
title: Šta je novo novembra 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u novembru Dynamics 365 Project Operations 2022.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831147"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo novembra 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.58.0.119
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2781818 | Ključ nije pronašao grešku prilikom podrazumevane cene za evidenciju korišćenja materijala. |
| Naplata i određivanje cena | 2922373 | Nije moguće povezati red ponude sa projektom koji je zatvoren kao izgubljena ponuda. |
| Naplata i određivanje cena | 2943206 | **Red ugovora** u polju Entitet projekta treba da bude opcionalan. |
| Naplata i određivanje cena | 2953182 | Poboljšajte poruku o grešci za korektivne fakture.|
| Naplata i određivanje cena | 2959500 | Nije u omogućuje povezivanje reda ponude sa projektnim zadatkom koji je već povezan sa izgubljenom ponudom.|
| Naplata i određivanje cena | 2959560 | Poruka "Ovaj kupac je već na ugovoru o projektu" primljena tokom zatvaranja ponude kao što je dobijeno u određenim lokalnim standardima. |
| Naplata i određivanje cena | 3031727 | Dodeljivanje resursa nije uspelo sa potrebnim poljem "msdyn_Company" nedostaje greška. |
| Naplata i određivanje cena | 3036905 | Preduzeće u vlasništvu nikada nije pokrenuto na ProjektuTeamMember. |
| Upravljanje mogućnostima za poslovanje | 2763519 | Greška "Null reference" u vrednosti EnsureProjectContractAllowsUpdates. |
| Upravljanje mogućnostima za poslovanje | 2783798 | Prilikom uvoza procena projekta u red ponude, nedostaju opisi zadataka za troškove i procenu materijala.|
| Upravljanje mogućnostima za poslovanje | 2988635 | Poboljšavanje opisa msg greške prilikom brisanja kupca u ponudi. |
| Upravljanje mogućnostima za poslovanje | 3001191 | Nije moguće kreirati ponudu iz mogućnosti za poslovanje gde je način naplate naveden kao "null". |
| Nadogradnja | 3012324 | Konverzija projekta nije uspela na projektu sa kontrolnim znakovima kao što je tab u imenu. || Planiranje i praćenje projekta | 2790384 | Vremensko vreme za operaciju "Neobrađeni" je prekratko. |
| Planiranje i praćenje projekta | 3044275 | Nedostaje lokalizacija za: nedostajeProjectSchedulerErrorMessage. |
| Planiranje i praćenje projekta | 3044277 | Koordinatna mreža za ponovno ispravljanje projekta se ne učitava kada je planer neiskvaren.|
| Upravljanje resursima | 2943153 | Ažuriraj karticu "Praćenje" da biste prikaželi dva decimalna mesta za trajanje.|
| Podugovaranje | 2932774 | Greška u čitanju reda fakture dobavljača je netačna. |
| Podugovaranje | 2939556 | Status zaglavlja fakture dobavljača ne bi trebalo da bude podešen na brisanje radne verzije na mreži ako nije aktivan. |
| Vreme i trošak | 2939998 | Uptake new TESA version in ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
