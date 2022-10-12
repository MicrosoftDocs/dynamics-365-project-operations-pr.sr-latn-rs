---
title: Šta je novo u septembru 2022. – primena usluge Project Operations Lite
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju Microsoft Dynamics 365 Project Operations lite primene u septembru 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621375"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Šta je novo u septembru 2022. – primena usluge Project Operations Lite

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Ime funkcije | Više informacija |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | **Revizija i aktiviranje ponuda**<br>Projektne operacije donose punu podršku procesa prodaje. Ponude projekta se mogu aktivirati tako da predstavljaju stanje u kojem je ponuda samo za čitanje i kada se rediguje. Aktivirane ponude se mogu korigovati da bi se kreirale nove ponude koje imaju postepeni broj revizije. Aktivirane ponude projekta ili revizije ponuda mogu biti zatvorene kao osvojene ili izgubljene. | [Aktiviranje i korigovanje ponude za projekat](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cena | **Podrazumevana agnostički cena vremenske zone**<br>Projektne operacije su uvele koncept agnostičnog datuma vremenske zone na svim stvarnim projektima. Novo polje Datum transakcije **je sada dostupno** u redovima naloga i stvarnim vrednostima i koristiće se za skladištenje datuma kada je transakcija izvršena, ali bez konvertovanja tog datuma u koordinirano univerzalno vreme. Ovaj datum će se koristiti za nizvodne procese kao što su podrazumevana cena i kreiranje faktura. | <p>[Utvrđivanje stope troškova za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Utvrđivanje prodajnih cena za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Naplata i određivanje cena | **Datum-efektivna cena zamenjuje u projektnom poslovanju**<br>Zamene cena koje su efektivne za datum obezbeđuju način da se zamene ili promene određene cene u cenovnik. | [Premošćava cena koja je efektivna](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Vreme i trošak | **Globalna osoba koja vrši odobravanje**<br>Ova funkcija omogućava nezavisnom prodavcu softvera (ISV) i centralizovano odobravanje, bez obzira na status projekta ili člana tima u projektu. | [Bezbednost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2754422 | Procene materijala i troškova se ne slivaju na Dynamics 365 Finance kada se projekti kopiraju u Dataverse programu. |
| Vreme i trošak | 2787409 | Osoba koja ne važi može da odobri unos vremena koje nije projektno. |
| Upravljanje mogućnostima za poslovanje | 2788907 | Ažurirana poruka o grešci prilikom provere valjanosti jedinstvenosti za redove porudžbine koji uključuju zastavice. |
| Vreme i trošak | 2842253 | Bez načina rukovanja izuzetkom za odobravanje vremena. |
| Naplata i određivanje cena | 2844181 | Ako ne dobijete ID korelacije, blokira se kreiranje fakture. |
| Naplata i određivanje cena | 2876628 | QLD, CLD - Procena rešenja cenovnog lista treba da koristi zastarela polja opsega datuma cenovnik. |
| Podizvođača | 2893222 | Ako nije navedena uloga za red podizvođači, trebalo bi da bude moguće izabrati taj red u članu tima za bilo koju ulogu. |
