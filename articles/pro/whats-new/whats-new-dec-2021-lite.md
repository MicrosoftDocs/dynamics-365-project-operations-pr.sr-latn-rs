---
title: Šta je novo u decembru 2021. – Project Operations jednostavna primena
description: Ovaj članak pruža informacije o ažuriranjima kvaliteta koja su dostupna u izdanju Project Operations Lite za decembar 2021. godine.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914097"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Šta je novo u decembru 2021. – Project Operations jednostavna primena

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

### <a name="subcontract-management"></a>Upravljanje podugovorima 

- [Članovi projektnog tima podugovora](../subcontracting/subcontracting-project-team-members.md): Menadžer projekta može da kreira imenovane ili generičke članove tima sa podugovorima i predmetima podugovora kako bi uticao na popunu osoblja i procenu.
- [Opcije podugovaranja za članove projektnog tima](../subcontracting/subcon-options.md): Prilikom pravljenja izbora osoblja za imenovane ili generičke članove projektnog tima, menadžer projekta može da pregleda postojeće podugovore ili da kreira nove podugovore za jednog ili više članova projektnog tima. 
- [Procena troškova dodela resursa iz podugovora](../subcontracting/costing-subcon-ra.md): Procena troškova na projektu će uzeti u obzir dodele resursa iz podugovora i koštaće ih koristeći cenovnike nabavke povezane sa podugovorima. 
- [Konfigurišite Tablu rasporeda da biste prikazali radnike po ugovoru i podugovoreni kapacitet](../subcontracting/configure-sb-subcon.md): Tabla rasporeda u Project Operations sada može biti konfigurisana da traži i predlaže vrstu radnika po ugovoru resursa koji se mogu rezervisati i podugovoreni kapacitet zajedno sa zaposlenima. Ova konfiguracija se može primeniti prilikom pretrage resursa u kontekstu popune osoblja za određeni zahtev projekta ili prilikom pretrage izvan konteksta zahteva projekta.
- [Popuna projekta osobljem sa radnicima po ugovoru i sa podugovorenim kapacitetom](../subcontracting/staffing-cw.md): Radnici po ugovoru sada mogu da se rezervišu na projektima koji koriste iskustva Table rasporeda.
- [Evidentiranje vremena, troškova i korišćenja materijala na projektima za podugovorene komponente](../subcontracting/recording-subcon-actuals.md): Radnici po ugovoru mogu da evidentiraju vreme i troškove, a članovi projektnog tima takođe mogu da evidentiraju korišćenje materijala kupljenih koristeći podugovor na projektu. To će dovesti do evidentiranja tačnih troškova na projektima koji koriste kupljene kapacitete ili materijale.
- [Prelazi između statusa na podugovoru](../subcontracting/subcon-states.md): Podugovori mogu biti potvrđeni da bi se završili pregovori sa dobavljačem, zatvoreni da bi se označio završetak isporuke ili otkazani da bi se označio raskid ugovora sa dobavljačem pre završetka isporuke.

### <a name="task-planning"></a>Planiranje zadataka
- Poboljšano rešavanje problema za administratore sistema. Kada korisnik ne može da otvori projekat, administrator može da pregleda greške koje nisu povezane sa licencom koje se generišu iz rešenja Project for the Web u [Evidencijama zakazivanja projekta](../../project-management/schedule-api-logs.md).
- [Korišćenje kontrolnih listi za zadatak u usluzi Microsoft Project for the web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U programu Microsoft Project for the web, možete dodati kontrolnu listu za zadatak kako biste vodili evidenciju o određenim stavkama.

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | API-iji planiranja sada omogućavaju ažuriranja polja **Preostali napor**, **Dovršeni napor** i **% dovršenja**. |
| Planiranje i praćenje | 2478497 | Polja **Broj aktivnosti** i **ID zadatka** za API-je rasporeda mogu biti prazna pri unosu jer će ih sistem popuniti korišćenjem automatizovanog numerisanja.|
| Vreme i trošak | 2468135 | Broj ponovnih pokušaja odobrenja se smanjuje sa pet na tri. |
| Vreme i trošak | 2468188 | Otklonjen je problem sa tekstom evidencije koji premašuje maksimalnu dužinu u atributu **notetext** entiteta **Anotacija**. |
