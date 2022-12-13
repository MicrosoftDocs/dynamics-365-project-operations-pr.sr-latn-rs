---
title: Šta je novo u oktobru 2022. – primena usluge Project Operations Lite
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u oktobru 2022 Dynamics 365 Project Operations .
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806765"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Šta je novo u oktobru 2022. – primena usluge Project Operations Lite

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.57.0.176

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Naziv funkcije | Još informacija |
| --- | --- | --- |
| Planiranje i praćenje projekta | **Spoljno planiranje operacija projekta**<br>Režim spoljnog zakazivanja omogućava korisnicima da izvorno kreiraju, ažuriraju i brišu entitete koji su povezani sa strukturama radne analize (WBS) Dataverse pomoću izvornih API-ja, bez trenutnih ograničenja koja sprovodi Projekat za Web. | [Spoljno planiranje](/dynamics365/project-operations/project-management/external-scheduling) |
| Primena i konfiguracija | <p>**Dozvoli korisnicima da odaberu tip primene**<br>Ispravke (PDU- ove) projektnih operacija koje se pokreću sa proizvodima koriste se za automatsko instaliranje rešenja za dvostruko pisanje projektnih operacija kada se u okruženju instaliraju dual-write core i orchestrationa rešenja.</p><p>Ova funkcija uvodi novi parametar ponašanja **nadogradnje rešenja** u parametrima projekta. Kada je ovaj parametar podešen samo **na Lite**, PUD-ovi više neće automatski instalirati Project Operations Dual-write rešenje, čak i ako su Dual-write core i orchestrationa rešenja instalirana u okruženju. Ovakvo ponašanje koristiće klijentima koji planiraju da koriste rešenja za dvostruko pisanje za integrisanje ulaznih porudžbina u aplikacije za finansije i operacije, ali žele da koriste projektne operacije u lite režimu (to jest bez integracije u aplikacije za finansije i operacije).</p> | |

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2316317 | Sistem dozvoljava da se kreira faktura koja nema transakcije za naplatu. |
| Naplata i određivanje cena | 2737300 | Proverite valjanost za raspoloživost polja Kupca pre pristupa obrascu. |
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
| Upravljanje resursima | 2751560 | Nedosledne željene organizacione jedinice u zahtevu resursa. |
| Podugovaranje | 2907231 | Faza procesa faktura dobavljača ne može da se avansno. |
| Vreme i trošak | 2867363 | Zapisi ne ispadaju iz prikaza "Odsustva/godišnji odmori za odobravanje" kada su u redu za odobravanje. |
| Vreme i trošak | 2894405 | TESA: Neiskorišćeni POC direktorijum izaziva probleme usaglašenosti. |
