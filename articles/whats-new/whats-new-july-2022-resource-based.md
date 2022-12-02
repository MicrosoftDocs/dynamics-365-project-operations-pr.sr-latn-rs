---
title: Šta je novo u julu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Microsoft Dynamics 365 Project Operations za jul 2022. za scenarije zasnovane na resursima/bez zaliha.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403969"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u julu 2022. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.44.0.22
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Primena i konfiguracija | 2761472 | Obrađuje se greška Project Operations instalacije. |
| Naplata i određivanje cena | 2746940 | Naziv reda podugovora treba da ima maksimalnu dužinu od 100 znakova. |
| Naplata i određivanje cena | 2739162 | Klijenti moraju biti u mogućnosti da vide dugmad na glavnoj traci u stvarnom prikazu matrice koordinatne mreže. |
| Planiranje i praćenje projekta | 2730318 | Ažurirana provera valjanosti za nepodržane znakove u temi projekta. |
| Naplata i određivanje cena | 2705361 | Stvarne vrednosti naplate prodaje prema kontrolnoj tački moraju biti uključene u polja za praćenje projekta. |
| Naplata i određivanje cena | 2675880 | Sprečite da projekat bude povezan sa predmetom ugovora koji nije zasnovan na poslu. |
| Naplata i određivanje cena | 2664396 | Ako je cenovnik ponude sačuvan bez ponude, mora doći do greške koja navodi da ponuda ne može biti prazna. |
| Naplata i određivanje cena | 2184019 | Kartica **Naplata zasnovana na zadatku** ne bi trebalo da bude prikazana za projekte koji nemaju prateći ugovor ili ponudu. |
| Vreme i trošak | 2754459 | Kada je tok u oblaku periodičnog planiranja neaktivno, prikažite reklamni natpis i zaobiđite asinhronu obradu. |
| Naplata i određivanje cena | 2724391 | Pogrešan izuzetak se dobija kada pravilu podeljene naplate za projektni ugovor projektu nedostaje vrednost klijenta. |
| Naplata i određivanje cena | 2708638 | Zapis nije pronađen prilikom pretrage koristeći matricu koordinatne mreže u Korišćenju materijala i Odobrenjima za korišćenje materijala.|
| Naplata i određivanje cena | 2686977 | Sprečite proveru valjanosti reda na fakturi tokom kreiranja fakture. |
| Naplata i određivanje cena | 2683032 | Kopiranje uloga i kategorija koje se naplaćuju ne skalira se preko 5000 zapisa.|
| Naplata i određivanje cena | 2673363 | % potrošnje troškova u projektu je oštećen kada za projekat postoje procene Napora i troškova, kao i stvarne vrednosti. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services (LCS) i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije su podrazumevano uključene u predstojećem izdanju

Sledeća tabela navodi funkcije koje su podrazumevano uključene u verziji 10.0.29. Većina funkcija koje su automatski uključene može biti isključena u [Upravljanju funkcijama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ubuduće, neke funkcije koje su automatski uključene mogu biti uklonjene iz Upravljanja funkcijama i postati obavezne. Ova promena obezbeđuje da korisnici koriste trenutnu funkcionalnost, tako da poboljšanja mogu da se nadograde na trenutnu funkcionalnost kako se dodaju. Funkcije nikada neće biti automatski omogućene za manje od godinu dana, osim ako nije utvrđeno da su od suštinskog značaja.

| Naziv funkcije | Datum omogućavanja | Dodata funkcija | Status funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogućite korekciju transakcije sati na osnovu promene raspodele pravila finansiranja | 16. septembar 2022. | 7. oktobar 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Funkcija za storniranje fakture za avansnu uplatu porudžbenice za projekat | 16. septembar 2022. | 6. oktobar 2021. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Brisanje redova na predlogu fakture prilikom korišćenja usluge Project Operations za scenarije zasnovane na resursima / bez zaliha | 16. septembar 2022. | 6. oktobar 2021. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Korekcija računovodstva na proknjiženoj projektnoj transakciji | 16. septembar 2022. | 10. maj 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Omogućavanje podrazumevanog podešavanja računovodstva za projekat | 16. septembar 2022. | 19. februar 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Omogućite više predmeta ugovora za projekat | 16. septembar 2022. | 29. jun 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Neka dnevnici za sate na projektu budu samo za čitanje ako trenutni status odobrenja ne dozvoljava uređivanje | 16. septembar 2022. | 6. oktobar 2021. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Omogućavanje sinhronizacije redova prodaje iz redova nabavke kada se ažuriraju redovi nabavke i kada je uključen parametar upravljanja promenom porudžbenice | 16. septembar 2022. | 7. oktobar 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Omogućavanje Project Operations u usluzi Dynamics 365 Customer Engagement | 16. septembar 2022. | 29. jun 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |
| Funkcija korekcije storniranja transakcije projekta | 16. septembar 2022. | 13. jul 2020. | Podrazumevano uključeno | Upravljanje projektima i računovodstvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcije koje postaju obavezne u predstojećem izdanju

Sledeća tabela navodi funkcije koje su obavezne od verzije 10.0.29. pa nadalje.

| Naziv funkcije | Datum omogućavanja | Dodata funkcija | Status funkcije | Modul |
| --- | --- | --- | --- | --- |
| Izračunavanje izvršene vrednosti na izvoru finansiranja bez zaokruživanja deviznog kursa | 16. septembar 2022. | 14. jun 2020. | Obavezno | Upravljanje projektima i računovodstvo |
| Omogućavanje knjiženja korekcije projekta sa istim kontima glavne knjige kao i originalna transakcija | 16. septembar 2022. | 14. jun 2020. | Obavezno | Upravljanje projektima i računovodstvo |
| Detalj iznosa izvršenog projektnog ugovora | 16. septembar 2022. | 31. avgust 2019. | Obavezno | Upravljanje projektima i računovodstvo |
| Omogućavanje sortiranja prema resursu tokom kreiranja predloga projektne fakture | 16. septembar 2022. | 31. avgust 2019. | Obavezno | Upravljanje projektima i računovodstvo |
