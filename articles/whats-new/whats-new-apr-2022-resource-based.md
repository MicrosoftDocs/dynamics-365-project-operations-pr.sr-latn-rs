---
title: Šta je novo u aprilu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ova tema pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u aprilu Dynamics 365 Project Operations 2022.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613353"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u aprilu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.41.0.45
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.26

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Kategorije nabavki se mogu koristiti u izlaznim porudžbinama projekta i neobrađenim fakturama dobavljača. Više informacija potražite u članku Korišćenje [kategorija nabavki sa izlaznim porudžbinama projekta i fakturama dobavljača na čekanju](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape sa dvostrukim pisanjem koje su izmenjene ili dodate u izdanju projektnih operacija u martu 2022.

| Mapa entiteta | Ažurirana verzija | komentara |
| -------------- | ------------------- | ------------|
| Project Operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Ova mapa podržava korišćenje kategorija nabavki sa izlaznim porudžbinama i neobrađenim fakturama dobavljača. |

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| ------------ | ---------------- | -------------- |
| Vreme i trošak | 2573900 | Funkcija **"Moderno** odobravanje" podrazumevano mora biti omogućena. |
| Naplata i određivanje cena | 2603313 | Otklonjena je greška u dupliranju zapisa koja je sprečila da se dodaju redovi ponude i ugovora koji imaju proizvod. |
| Primena i konfiguracija | 2611368 | Korisnici moraju biti u mogućnosti da dodaju do pet prilagođenih entiteta rešenju pomoću modernog dizajnera aplikacija. |
| Vreme i trošak | 2628285 | Otklonjen je problem koji je uticao na mogućnost postavljanje ispravne kategorije resursa tokom uvoza stavke vremena. |
| Upravljanje mogućnostima za poslovanje| 2628815 | Ažurirajte ograničenje znaka opisa detalja reda ponude tako da se podudara sa ograničenjem znakova teme zadatka, tako da uvoz uspe za zadatke u kojima je tema duža od 100 znakova. |
| Vreme i trošak| 2629547 | Polje **Prosleđeno odobravanjem** projekta mora da ukaže korisniku koji je prosledio zapis. |
| Vreme i trošak| 2629865 | Polje Kopiraj **kategoriju** za zadatke prilikom kopiranja projekata. |
| Vreme i trošak| 2636463 | Popravili filtere na odobrenjima u savremenim obrascima za odobravanje. |
| Planiranje i praćenje projekta | 2648300 | Otklonjen je problem koji sprečava menjanje vlasnika projekta. |
| Naplata i određivanje cena | 2563000 | Redovi naloga za neželjenu prodaju u kojima se valuta razlikuje od valute ugovora ne smeju biti dozvoljeni. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u Dynamics 365 Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa (LCS) i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
