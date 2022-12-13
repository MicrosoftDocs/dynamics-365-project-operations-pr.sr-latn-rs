---
title: Šta je novo u oktobru 2022. – Project Operations za scenarije zasnovane na resursima/materijalima koji nisu na zalihama
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft Dynamics 365 Project Operations u oktobru 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806754"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u oktobru 2022. – Project Operations za scenarije zasnovane na resursima/materijalima koji nisu na zalihama

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.57.0.176
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.30

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Naziv funkcije | Još informacija |
| --- | --- | --- |
| Planiranje i praćenje projekta | **Spoljno planiranje operacija projekta**<br>Režim spoljnog zakazivanja omogućava korisnicima da izvorno kreiraju, ažuriraju i brišu entitete koji su povezani sa strukturama radne analize (WBS) Dataverse pomoću izvornih API-ja, bez trenutnih ograničenja koja sprovodi Projekat za Web. | [Spoljno planiranje](/dynamics365/project-operations/project-management/external-scheduling) |
| Primena i konfiguracija | <p>**Dozvoli korisnicima da odaberu tip primene**<br>Ispravke (PDU- ove) projektnih operacija koje se pokreću sa proizvodima koriste se za automatsko instaliranje rešenja za dvostruko pisanje projektnih operacija kada se u okruženju instaliraju dual-write core i orchestrationa rešenja.</p><p>Ova funkcija uvodi novi parametar ponašanja **nadogradnje rešenja** u parametrima projekta. Kada je ovaj parametar podešen samo **na Lite**, PUD-ovi više neće automatski instalirati Project Operations Dual-write rešenje, čak i ako su Dual-write core i orchestrationa rešenja instalirana u okruženju. Ovakvo ponašanje koristiće klijentima koji planiraju da koriste rešenja za dvostruko pisanje za integrisanje ulaznih porudžbina u aplikacije za finansije i operacije, ali žele da koriste projektne operacije u lite režimu (to jest bez integracije u aplikacije za finansije i operacije).</p> | |
| Naplata i određivanje cena | <p>**Konverzija valute za troškove neželjene prodajne transakcije u Integrisanim okruženjima**<br>Za klijente koji koriste projektne operacije integrisane sa aplikacijama za finansije i operacije (to jest u tipu raspoređivanja resursa/nenapuštenih zaliha), kursevi valuta se obično ovladaju aplikacijama za finansije i operacije. Međutim, ako kategorija troškova treba da bude cenjena korišćenjem metoda obračuna cena "po trošku" ili "naznake preko troška" prilikom fakturisanja kupca, kurs valute koji se koristi za izračunavanje iznosa prodaje koristi kurseve valuta Dataverse u, a ne kurseve valuta iz aplikacija za finansije i operacije.</p><p>Ova funkcija uvodi novi parametar ponašanja **konverzije valute** u parametre projekta. Kada je ovaj parametar podešen na "Prošireno **sa zaobilaznim vrednostima**", neželjeni iznosi prodaje na transakcijama troškova se izračunavaju korišćenjem kurseva valuta iz aplikacija za finansije i operacije.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2316317 | Sistem dozvoljava da se kreira faktura koja nema transakcije za naplatu. |
| Naplata i određivanje cena | 2737300 | Proverite valjanost za **raspoloživost** polja Kupca pre pristupa obrascu. |
| Naplata i određivanje cena | 2744948 | Dodajte bez potvrde za metod naplate. |
| Naplata i određivanje cena | 2763515 | Regulator greške "Null reference" kada nedostaje ugovor o prodaji fakture. |
| Naplata i određivanje cena | 2844301 | Kreiranje grupne fakture nije uspelo zbog greške. |
| Naplata i određivanje cena | 2845869 | Neispravno skladištenje usluge organizacije. |
| Naplata i određivanje cena | 2853729 | Detalji uloge i cene se ažuriraju prilikom izmene tipa fakturisanja. |
| Naplata i određivanje cena | 2940350 | Kada su stvarne cene, treba automatski uneti samo aktivne cenovnike. |
| Primena i konfiguracija | 3001206 | Msdyn\_ replaylogheader entitet sprečava nadogradnju korisničkih orga. |
| Upravljanje mogućnostima za poslovanje | 2755582 | Regulator bez referenci za izuzetke u pomoćniku pravila za razdeljenu naplatu. |
| Upravljanje mogućnostima za poslovanje | 2761477 | Kada se koristi podeljena naplata, brisanje prekretnice (zaglavlje) ostavlja prekretnice siročićima. |
| Upravljanje mogućnostima za poslovanje | 2767595 | Kada se otvori zapis o korišćenju materijala u glavnom obrascu, resurs koji se može rezervisati za zapis se menja u trenutno prijavljenog korisnika. |
| Planiranje i praćenje projekta | 2790384 | Vremensko vreme za operaciju "Neobrađeni" je prekratko. |
| Planiranje i praćenje projekta | 2957840 | Nije bilo mogu se sačuvati zadaci i kolone se ne mogu dodati na stranicu "Zadaci **" u** integrisanim operacijama projekta. |
| Upravljanje resursima | 2751560 | Nedosledne željene organizacione jedinice u zahtevu resursa. |
| Podugovaranje | 2853245 | Podudaranje sa stvarnim redom fakture dobavljača ne ažurira status verifikacije ako je red ugovora već povezan sa redom fakture dobavljača. |
| Podugovaranje | 2907231 | Faza procesa faktura dobavljača ne može da se avansno. |
| Vreme i trošak | 2867363 | Zapisi ne ispadaju iz prikaza "Odsustva/godišnji odmori za odobravanje" kada su u redu za odobravanje. |
| Vreme i trošak | 2894405 | TESA: Neiskorišćeni POC direktorijum izaziva probleme usaglašenosti. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
