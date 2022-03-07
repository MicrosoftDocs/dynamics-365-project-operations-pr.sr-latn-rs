---
title: Šta je novi decembar 2021.
description: Ovaj tema pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju project Operations lite deployment u decembru 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942994"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Šta je novi decembar 2021.

_Odnosi se na: Jednostavna primena – od pogodbe do profakture_

Ova tema se odnosi na sledeće komponente i verzije korporacije Dynamics 365 Project Operations Microsoft:

- Operacije projekta u Dataverse verziji okruženja 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

### <a name="subcontract-management"></a>Upravljanje podizvođačima 

- [Članovi tima projekta podizvođači : Menadžer projekta može da kreira](../subcontracting/subcontracting-project-team-members.md) imenovane ili generičke članove tima sa podizvođačima i linijama podizvođače kako bi uticao na osoblje i procenu.
- [Opcije podizvođanja za članove projektnog tima : Prilikom izrade izbora osoblja za imenovane](../subcontracting/subcon-options.md) ili generičke članove projektnog tima, menadžer projekta može da pregleda postojeće podizvođače ili da kreira nove podizvođače za jednog ili više članova projektnog tima. 
- [Procena troškova dodeljivanja resursa podizvođačima : Procena troškova projekta će uzeti u obzir](../subcontracting/costing-subcon-ra.md) dodele resursa podizvođačima i koštaće ih korišćenjem nabavnih cenovnika povezanih sa podizvođačima. 
- [Konfigurišite tablu rasporeda da prikaže radnike po ugovoru i kapacitet podizvođačima : Tabla rasporeda u projektnim operacijama sada može da se konfiguriše da traži i predlaže tip radnika po ugovoru](../subcontracting/configure-sb-subcon.md) knjigovodstvene resurse i kapacitet podizvođačima zajedno sa zaposlenima. Ova konfiguracija se može primeniti prilikom traženja resursa u kontekstu osoblja za određeni zahtev projekta ili prilikom pretraživanja izvan konteksta zahteva projekta.
- [Osoblje projekta sa radnicima po ugovoru i podizvođačima : Radnici po ugovoru sada mogu da rezervišu projekte](../subcontracting/staffing-cw.md) koji koriste iskustva odbora.
- [Vreme snimanja, troškovi i korišćenje materijala na projektima za komponente podizvođačima : Radnici po ugovoru mogu da zabeleže vreme i troškove, a članovi projektnog tima takođe](../subcontracting/recording-subcon-actuals.md) mogu da zabeleže upotrebu materijala kupljenih pomoću podizvođač na projektu. To će rezultirati zapisivanjem tačnih troškova na projekte koji koriste kupljene kapacitete ili materijale.
- [Državni prelazi na podizvođač : Podizvođači mogu biti potvrđeni da bi se završili pregovori sa dobavljačem, zatvorili da bi se označio završetak isporuke ili otkazani da bi se označio raskid](../subcontracting/subcon-states.md) ugovora sa dobavljačem pre završetka isporuke.

### <a name="task-planning"></a>Planiranje zadataka
- Poboljšano rešavanje problema za administratore sistema. Kada korisnik ne može da otvori projekat, administrator može da pregleda greške koje nisu vezane za licencu generisane iz projekta za Veb [u evidencijama planiranje projekta](../../project-management/schedule-api-logs.md).
- [Koristite liste za proveru zadataka u programu Microsoft Project za Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). U programu Microsoft Project za Web možete da dodate listu za proveru zadatku da biste pratili određene stavke.

## <a name="quality-updates"></a>Ispravke kvaliteta

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Planiranje i praćenje | 2392596 | Planirajte da API sada dozvoli ažuriranje **preostalih napora**, **dovršenog napora** i **%Complete** polja. |
| Planiranje i praćenje | 2478497 | Broj API-ja **aktivnosti i** **ID-a** zadatka mogu biti prazni na ulazu jer će ih sistem popuniti korišćenjem automatizovanog numerisanja.|
| Vreme i trošak | 2468135 | Broj ponovnih odobrenja se smanjuje sa pet na tri. |
| Vreme i trošak | 2468188 | Otklonjen je problem sa tekstom evidencije koji **premašuje maksimalnu** dužinu u **atributu beleške entiteta** beleške. |
