---
title: Šta je novo u junu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u junu Dynamics 365 Project Operations 2022.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959678"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u junu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.43.0.77
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape sa dva pisanja koje su izmenjene ili dodate u izdanje "Operacije projekta" iz juna 2022.

| Mapa entiteta | Ažurirana verzija | komentara |
| --- | --- | --- |
| Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarelo polje je zastarelo i mapirano u novo polje za praćenje stanja fakture dobavljača. |

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Podizvođača | 2708885 | Otklonjena je poruka o grešci koja se pojavljuje kada korisnik kreira zapis zaglavlja rezervacije resursa koji se može rezervisati, a u kome nije popunjen resurs koji se može rezervisati. |
| Planiranje i praćenje projekta | 2629441 | Ispravljena je logika okidača toka posla da bi se sprečila beskonačna petlja kada se ažuriraju projektni zadaci. |
| Vreme i trošak | 2641209 | Uvoz vremenske stavke iz dodela/rezervacija mora zadržati referencu resursa koja se može rezervisati. |
| Planiranje i praćenje projekta | 2651148 | Zaglavlje projektnog dokumenta mora biti čuvano.|
| Planiranje i praćenje projekta | 2653145 | Dodate provere valjanosti da biste se uverili da nije moguće kreirati zapis projekta koji u imenu ima nevažeće znakove. |
| Vreme i trošak | 2654710 | Ispravljeno je filtriranje na stranici **"Odobrenja** ". |
| Naplata i određivanje cena | 2667805 | Dodate provere valjanosti koje pomažu u sprečavanju kreiranja rezultata fakturisane prodaje ako podrška neželjenim stvarnim prodajama ne postoji. |
| Naplata i određivanje cena | 2668378 | Dodate provere valjanosti koje sprečavaju da se doda prilagođena dimenzija određivanja cena, osim ako se ne popune logičko ime i ime polja. |
| Podizvođača | 2677485 | Ažurirana ciljna verzija reda fakture dobavljača za dvostruko pisanje. |
| Vreme i trošak | 2700428 | Poboljšana logika odobravanja kako bi se osiguralo da drugi skupovi odobravanja za projekat mogu da se obrade čak i ako je jedan od skupova odobravanja zaglavljen u sistemskim poslovima. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u finansijama

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa (LCS) i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
