---
title: Šta je novo u junu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Microsoft Dynamics 365 Project Operations za jun 2022. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031348"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u junu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.43.0.77 ili 4.43.0.119
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape dvostrukog pisanja koje su izmenjene ili dodate u izdanju Project Operations od juna 2022. godine.

| Mapa entiteta | Ažurirana verzija | komentara |
| --- | --- | --- |
| Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarelo je neodobreno polje i mapirano u novo polje za praćenje statusa fakture dobavljača. |

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Podugovaranje | 2708885 | Otklonjena je poruka o grešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji može da se rezerviše, a u kome nije popunjen resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika okidača toka posla da bi se sprečila beskonačna petlja kada se ažuriraju projektni zadaci. |
| Vreme i trošak | 2641209 | Uvozi stavki vremena iz dodela/rezervacija mora zadržati referencu na resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti zaštićeno.|
| Planiranje i praćenje projekta | 2653145 | Dodate su provere ispravnosti da se osiguralo da nije moguće kreirati zapis projekta koji u nazivu ima nevažeće znakove. |
| Vreme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **Odobrenja**. |
| Naplata i određivanje cena | 2667805 | Dodate su provere ispravnosti kojima se sprečava kreiranje stvarnih vrednosti naplaćene prodaje ako podrška stvarnih vrednosti nenaplaćene prodaje ne postoji. |
| Naplata i određivanje cena | 2668378 | Dodate su provere ispravnosti koje sprečavaju da se doda prilagođena dimenzija određivanja cena, osim ako se ne popune logičko ime i naziv polja. |
| Podugovaranje | 2677485 | Ažurirana ciljna verzija redova na fakturi dobavljača za dvostruko upisivanje. |
| Vreme i trošak | 2700428 | Poboljšana je logika odobrenja kako bi se osiguralo da drugi skupovi odobrenja za projekat mogu da se obrade čak i ako je jedan od skupova odobrenja zaglavljen u sistemskim poslovima. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
