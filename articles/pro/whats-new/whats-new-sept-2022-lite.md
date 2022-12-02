---
title: Šta je novo u septembru 2022. – primena usluge Project Operations Lite
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju za septembar 2022. usluge Microsoft Dynamics 365 Project Operations jednostavna primena.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634870"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Šta je novo u septembru 2022. – primena usluge Project Operations Lite

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Naziv funkcije | Više informacija |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | **Revizija i aktiviranje ponuda**<br>Project Operations donosi punu podršku procesu prodaje. Ponude projekta se mogu aktivirati tako da predstavljaju status u kojem je ponuda samo za čitanje i kada se revidira. Aktivirane ponude se mogu revidirati da bi se kreirale nove ponude koje imaju inkrementalni broj revizije. Aktivirane ponude za projekat ili revizije ponude mogu da se zatvore kao ostvarene ili neostvarene. | [Aktiviranje i korigovanje ponude za projekat](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cena | **Podrazumevana cena sa nepoznatom vremenskom zonom**<br>Project Operations su uvele koncept datuma sa nepoznatom vremenskom zonom na svim stvarnim vrednostima u projektu. Novo polje **Datum transakcije** je sada dostupno u stavkama u glavnoj knjizi i stvarnim vrednostima i koristiće se za skladištenje datuma kada je transakcija izvršena, ali bez konvertovanja tog datuma u koordinirano univerzalno vreme. Ovaj datum će se koristiti za posledične procese kao što su postavljanje podrazumevane cene i kreiranje faktura. | <p>[Utvrđivanje stopa za cenu za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Utvrđivanje prodajnih cena za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Naplata i određivanje cena | **Zamene cene na određeni datum u usluzi Project Operations**<br>Izmene cena na određeni datum obezbeđuju način zamene ili promene određene cene u cenovniku. | [Izmene cena na određeni datum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Vreme i trošak | **Globalna osoba koja vrši odobravanje**<br>Ova funkcija omogućava nezavisnog prodavca softvera (ISV) i centralizovano odobravanje, bez obzira na status projekta ili člana tima u projektu. | [Bezbednost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
|Planiranje i praćenje projekta|**Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja** </br> </br>API za uređivanje konture dodele resursa omogućava programerima da programski navedu napore osobe kojoj je dodeljen zadatak u bilo kom podržanom opsegu datuma za granuliranije planiranje napora u vremenskoj fazi.|[Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2754422 | Procene materijala i troškova ne teku u Dynamics 365 Finance kada se projekti kopiraju u uslugu Dataverse. |
| Vreme i trošak | 2787409 | Odobravalac koji nije važeći može da odobri unos vremena koje nije projektno. |
| Upravljanje mogućnostima za poslovanje | 2788907 | Ažurirana poruka o grešci prilikom provere valjanosti jedinstvenosti za stavke porudžbenice koje obuhvataju zastavice. |
| Vreme i trošak | 2842253 | Bez načina obrade izuzetaka za odobravanje vremena. |
| Naplata i određivanje cena | 2844181 | Ako ne dobijete ID korelacije, blokira se kreiranje fakture. |
| Naplata i određivanje cena | 2876628 | QLD, CLD – Procena rešenja cenovnika treba da koristi zastarela polja opsega datuma cenovnika. |
| Podugovaranje | 2893222 | Ako nije navedena nijedna uloga za predmet podugovora, trebalo bi da bude moguće izabrati taj predmet za člana tima za bilo koju ulogu. |
