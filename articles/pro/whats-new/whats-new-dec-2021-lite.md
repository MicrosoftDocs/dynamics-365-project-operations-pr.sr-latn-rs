---
title: Šta je novi decembar 2021.
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u decembru 2021.
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
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Šta je novi decembar 2021.

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

### <a name="subcontract-management"></a>Upravljanje podizvođačima 

- [Članovi projekta podizvođači](../subcontracting/subcontracting-project-team-members.md): Menadžer projekta može da kreira imenovane ili generičke članove tima sa podizvođačima i linijama podizvođače kako bi uticao na osoblje i procenu.
- [Opcije podizvođanja za članove projektnog tima](../subcontracting/subcon-options.md): Prilikom pravljenja izbora osoblja za imenovane ili generičke članove projektnog tima, menadžer projekta može da pregleda postojeće podizvođače ili da kreira nove podizvođače za jednog ili više članova projektnog tima. 
- [Procena troškova dodeljivanja resursa podizvođačima](../subcontracting/costing-subcon-ra.md): Procena troškova projekta će uzeti u obzir dodele resursa podizvođačima i koštaće ih korišćenjem nabavnih cenovnika povezanih sa podizvođačima. 
- [Konfigurišite tablu rasporeda da prikaže radnike po ugovoru i kapacitet podizvođači](../subcontracting/configure-sb-subcon.md): Tabla rasporeda u projektnim operacijama sada može biti konfigurisana da traži i predlaže tip radnika po ugovoru knjigovodstvenih resursa i kapaciteta podizvođaca zajedno sa zaposlenima. Ova konfiguracija se može primeniti prilikom traženja resursa u kontekstu osoblja za određeni zahtev projekta ili prilikom pretraživanja izvan konteksta zahteva projekta.
- [Osoblje projekta sa radnicima po ugovoru i podizvođačima](../subcontracting/staffing-cw.md): Radnici po ugovoru sada mogu da rezervišu projekte koji koriste iskustva odbora.
- [Vreme snimanja, troškovi i korišćenje materijala na projektima za komponente podizvođači](../subcontracting/recording-subcon-actuals.md): Radnici po ugovoru mogu da zabeleže vreme i troškove, a članovi projektnog tima takođe mogu da zabeleže upotrebu materijala kupljenih pomoću podizvođač na projektu. To će rezultirati zapisivanjem tačnih troškova na projekte koji koriste kupljene kapacitete ili materijale.
- [Državni prelazi na podizvođač](../subcontracting/subcon-states.md): Podizvođači mogu biti potvrđeni da bi se završili pregovori sa dobavljačem, zatvoreni da bi se označio završetak isporuke ili otkazano da bi se označio raskid ugovora sa dobavljačem pre završetka isporuke.

### <a name="task-planning"></a>Planiranje zadataka
- Poboljšano rešavanje problema za administratore sistema. Kada korisnik ne može da otvori projekat, administrator može da pregleda greške koje nisu povezane sa licencom, a koje se generišu iz projekta za Veb [u evidencijama planiranje projekta](../../project-management/schedule-api-logs.md).
- [Koristite liste za proveru zadataka u programu Microsoft Project za Veb](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U programu Microsoft Project za Web možete da dodate listu za proveru zadatku da biste pratili određene stavke.

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | Planirajte da API sada dozvoli ažuriranje preostalih **napora, dovršavanja** **napora i** **% Dovršenih** polja. |
| Planiranje i praćenje | 2478497 | Broj API-ja **aktivnosti i** **ID-a zadatka** mogu biti prazni na ulazu jer će ih sistem popuniti korišćenjem automatizovanog numerisanja.|
| Vreme i trošak | 2468135 | Broj ponovnih odobrenja se smanjuje sa pet na tri. |
| Vreme i trošak | 2468188 | Otklonjen je problem sa tekstom evidencije **koji premašuje** maksimalnu dužinu u atributu **beleške entiteta beleške**. |
