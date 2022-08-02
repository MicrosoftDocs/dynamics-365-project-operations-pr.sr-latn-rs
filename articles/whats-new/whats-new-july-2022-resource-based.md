---
title: Šta je novo u julu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u julu Dynamics 365 Project Operations 2022.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183932"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u julu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.44.0.22
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Primena i konfiguracija | 2761472 | Rešava se greška u instalaciji operacija projekta. |
| Naplata i određivanje cena | 2746940 | Ime reda podizvođaka treba da ima maksimalnu dužinu od 100 znakova. |
| Naplata i određivanje cena | 2739162 | Klijenti moraju biti u mogućnosti da vide dugmad na glavnoj traci u stvarnom prikazu koordinatne mreže. |
| Planiranje i praćenje projekta | 2730318 | Ažurirana provera valjanosti za znakove koji nisu podržani u temi projekta. |
| Naplata i određivanje cena | 2705361 | Prekretnica fakturisanih prodajnih stvarnih podataka mora biti uključena u polja praćenja projekta. |
| Naplata i određivanje cena | 2675880 | Sprečavanje da projekat bude povezan sa redom ugovora koji nije zasnovan na poslu. |
| Naplata i određivanje cena | 2664396 | Ako je cenovnik ponude sačuvan bez ponude, mora doći do greške koja navodi da ponuda ne može biti prazna. |
| Naplata i određivanje cena | 2184019 | Kartica " **Naplata zasnovana na zadatku** " ne bi trebalo da bude prikazana za projekte koji nemaju prateći ugovor ili ponudu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u finansijama

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa (LCS) i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije su podrazumevano uključene u predstojećem izdanju

Sledeća tabela navodi funkcije koje su podrazumevano uključene u verziji 10.0.29. Većina funkcija koje su automatski uključene može biti isključena u upravljanju [funkcijama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ubuduće, neke funkcije koje su automatski uključene mogu biti uklonjene iz upravljanja funkcijama i postati obavezne. Ova promena obezbeđuje da klijenti koriste trenutnu funkcionalnost, tako da poboljšanja mogu da se nadograde na trenutnoj funkcionalnosti dok se dodaju. Funkcije nikada neće biti automatski omogućene za manje od godinu dana, osim ako nisu utvrđene da su od suštinskog značaja.

| Ime funkcije | Omogući datum | Dodata funkcija | Stanje funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogući korekciju satne transakcije na osnovu promene raspodele pravila finansiranja | 16. septembar 2022. | 7. oktobar 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Funkcija za storniranje fakture za akontaciju/avansnu uplatu izlazne porudžbine | 16. septembar 2022. | 6. oktobar 2021. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Brisanje redova predloga fakture prilikom korišćenja operacija projekta za scenarije zasnovane na resursima/ nefakturisane | 16. septembar 2022. | 6. oktobar 2021. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Koriguj računovodstvo na proknjiženoj projektne transakcije | 16. septembar 2022. | 10. maj 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Omogući podrazumevano podešavanje računovodstva za projekat | 16. septembar 2022. | 19. februar 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Omogućite više predmeta ugovora za projekat | 16. septembar 2022. | 29. jun 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Učinite dnevnike "Sat projekta" samo za čitanje ako trenutni status odobravanja ne dozvoljava uređivanje | 16. septembar 2022. | 6. oktobar 2021. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Omogući sinhronizaciju redova prodaje iz redova nabavke kada se ažuriraju redovi nabavke i kada je uključen parametar upravljanja promenom izlazne porudžbine | 16. septembar 2022. | 7. oktobar 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Omogući projektne operacije na Dynamics 365 Customer Engagement | 16. septembar 2022. | 29. jun 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |
| Funkcija korekcije transakcije projekta | 16. septembar 2022. | 13. jul 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje projektima i računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcije koje postaju obavezne u predstojećem izdanju

Sledeća tabela navodi funkcije koje su obavezne od verzije 10.0.29 pa nadalje.

| Ime funkcije | Omogući datum | Dodata funkcija | Stanje funkcije | Modul |
| --- | --- | --- | --- | --- |
| Izračunavanje počinjene vrednosti na izvoru finansiranja bez zaokruživanja kursa valute | 16. septembar 2022. | 14. jun 2020. | Obavezno | Upravljanje projektima i računovodstvo |
| Omogući knjiženje korekcije projekta sa istim kontima knjige kao i originalna transakcija | 16. septembar 2022. | 14. jun 2020. | Obavezno | Upravljanje projektima i računovodstvo |
| Detalj iznosa ugovora o projektu | 16. septembar 2022. | 31. avgust 2019. | Obavezno | Upravljanje projektima i računovodstvo |
| Omogući sortiranje po resursu tokom kreiranja predloga projektne fakture | 16. septembar 2022. | 31. avgust 2019. | Obavezno | Upravljanje projektima i računovodstvo |
