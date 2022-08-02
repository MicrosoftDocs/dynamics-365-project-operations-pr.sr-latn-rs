---
title: Šta je novo u junu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama dostupnim u junu 2021.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028280"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u junu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće Dynamics 365 Project Operations komponente i verzije:

- Project Operations u Dynamics 365 Dataverse okruženju verzije 4.11.0.156 ili 4.11.0.164.
- Upravljanje projektima i računovodstvo u oblasti finansija i operacija aplikacije verzija 10.0.19.

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Mogućnost brisanja [stavki predloga fakture za projekat za scenarije prilagođavanja](../invoicing/correct-project-invoice-proposals.md).
- Pojedinačni redovi troškova odražavaju nazive potkategorija u izveštaju o troškovima [Ponovo osmišljeni izveštaji – Nove funkcije](../expense/expense-reports-reimagined.md#new-features).
- Način plaćanja je dostupan u oknu „Novi trošak“ prilikom kreiranja novog troška.
- Opšta dostupnost API-ja planiranja projekata. Ova nova funkcionalnost omogućava klijentima da programski izvršavaju operacije kreiranja, ažuriranja i brisanja projektnih zadataka, dodeljivanja resursa, zavisnosti zadataka i zapisa članova projektnog tima. Više informacija potražite u članku [Korišćenje API-ja za raspored projekata za izvršavanje operacija sa planiranjem entiteta](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. 

Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne Dataverse operacije i verziju rešenja za finansije i operacije. Određene funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti na stranici **Dvostruko upisivanje** u koloni **Verzija**. Aktivirajte novu verziju mape izborom **Verzije mape tabela**, odabirom najnovije verzije, a zatim čuvanjem izabrane verzije. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem pri pokretanju mape, sledite uputstva u odeljku [Problem nedostajućih kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2281417 | Rešen je problem u vezi sa neuspehom radnje automatskog kreiranja fakture kroz raspored faktura. |
| Naplata i određivanje cena | 2287835 | Poboljšane performanse potvrđivanja fakture. |
| Upravljanje mogućnostima za poslovanje | 2222555 | Naplativost procena materijala mora se pravilno kopirati u ponudu detalja stavki kada se koristi **Uvoz iz procene projekta**. |
| Upravljanje mogućnostima za poslovanje | 2223427 | Prilagođavanja su sada dozvoljena za radnju **GenerateRetainersFromRetainerScheduleOptions**. |
| Upravljanje mogućnostima za poslovanje | 2277528 | Izračunavanje fiksne vrednosti naplate za predmete ugovora projekta sa više klijenata. |
| Planiranje i praćenje projekta | 2226110 | Rešen je povremeni problem sa funkcijom **Generisanje zahteva** u mreži **Projektni tim**. |
| Planiranje i praćenje projekta | 2208109 | Korisnici ne mogu da kreiraju projekat u jednoj valuti sa povezanim zadacima u drugoj valuti. |
| Planiranje i praćenje projekta | 2258228 | Ažurirana je lista polja kojima je dozvoljeno menjanje pomoću entiteta **Zakazivanje** koji koriste API za raspored. |
| Planiranje i praćenje projekta | 2293989 | Tačan jezik i regionalna podešavanja moraju se proslediti mreži **Projektni zadaci**. |
| Upravljanje resursima | 2220493 | Ispravljeno je korisničko iskustvo u mreži **Zadatak** kada se zahtev za resursom brzo označi kao završen. |
| Upravljanje resursima | 2330496 | Rešen je problem sa učitavanjem **tabele rasporeda**. (Ispravka kvaliteta je dostupna u verziji 4.11.0.164) |
| Vreme i trošak | 2194431 | Mreža **Stavka vremena** mora da poštuje početak nedelje kako je podešeno u **podešavanjima sistema**. |
| Vreme i trošak | 2277311 | Kada izbrišete vrednost u ćeliji u mreži **Stavka vremena**, kursor ostaje u mreži. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Opcije **Beleške obrazaca** i **Podešavanje obrasca** nisu vidljive u dijalogu **Podešavanje upravljanja projektima** u pravnim licima usluge Finance koja su integrisana u Project Operations. |
| Upravljanje projektima i računovodstvo | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Podrazumevani opis za PDV je prazan kada je **Tip knjiženja** = **Porez na promet** za vaučere za fakturu projekta. |
| Upravljanje projektima i računovodstvo | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dvostruke transakcije se knjiže kada se koristi naplata zasnovana na zadatku na platformi Dataverse sa Project Operations integracijom. |
| Upravljanje projektima i računovodstvo | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Procenat potpunog prepoznavanja prihoda je netačan dok se koristi Project Operations integracija. |
| Upravljanje projektima i računovodstvo | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Pripisivanje prihoda se udvostručuje na fakturi dobavljača na čekanju u Project Operations integrisanom scenariju. |
| Upravljanje projektima i računovodstvo | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nije moguće objaviti dnevnik integracije kada je pravilo profila prihoda postavljeno na podešavanje **Grupe**. |
| Upravljanje projektima i računovodstvo | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Račun za kupovinu se ne može knjižiti za porudžbenice projekta koje imaju stavke sa više mernih jedinica. |
| Upravljanje projektima i računovodstvo | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Podrazumevani finansijski aspekt na projektu se ne može ažurirati pomoću entiteta podataka projekata **V2**. |
| Upravljanje projektima i računovodstvo | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Postupak grupnog kreiranja procena projekata traje predugo. |
| Upravljanje projektima i računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Brisanjem ugovora briše se i adresa povezana sa klijentom. |
| Putovanje i trošak | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Uslov toka posla za odobrenje izveštaja o troškovima se ne izračunava pravilno. |
| Putovanje i trošak | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Smernice izveštaja o troškovima ne procenjuju pravilno ID projekta. |
| Putovanje i trošak | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Radnja **Podelite na lično za transakcije troškova unutar preduzeća** ne radi ispravno. |
| Putovanje i trošak | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Poravnanja stavki izveštaja o troškovima se slučajno izbrišu kada se izbrišu određeni zahtevi za putovanje. To se događa kada su isti recID izveštaja o troškovima i recID zahteva za putovanje. |
| Putovanje i trošak | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Postoji problem u aplikaciji Troškovi za mobilne uređaje kada je polje **ID projekta** obavezno u smernicama izveštaja o troškovima. |
| Putovanje i trošak | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Nije moguće uređivati troškove unutar preduzeća koji su povezani sa projektom. Umesto toga, prikazuje se sledeća poruka o grešci: „Referenca objekta nije podešena na instancu objekta“. |
| Putovanje i trošak | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Kada se proknjiži izveštaj o troškovima, pogrešna valuta i iznos se navode u knjizi analitike banke. |
| Putovanje i trošak | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Obavljena su poboljšanja funkcije *Brisanje transakcija kreditnom karticom*.  |
| Putovanje i trošak | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Porez na promet uključen u izveštaj o rashodima ne izračunava se dosledno kada se u pravnom licu navede druga valuta izveštavanja. |
| Putovanje i trošak | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Dodavanje novog putnog troška u gotovini utiče na performanse. |
| Putovanje i trošak | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravila politike troškova se ne pokreću u izveštaju o troškovima. |
| Putovanje i trošak | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Otpremanjem nove deljene kategorije pomoću radnog okvira za upravljanje podacima uklanjaju se sve potkategorije za sve deljene kategorije. |
| Putovanje i trošak | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Kada kreirate stavku troškova, a zatim izaberete kategoriju, prikazuje se sledeća poruka o grešci: „Kombinacija grupe poreza na promet DOM i grupe poreza na promet stavki STD nije važeća.“ |
| Putovanje i trošak | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Postoje problemi sa sinhronizacijom u aplikaciji Troškovi za mobilne uređaje. |
