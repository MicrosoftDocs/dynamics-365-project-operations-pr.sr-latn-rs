---
title: Konfigurišite naplative komponente za predmet ugovora zasnovan na projektu
description: Ova tema pruža informacije o uključenim, naplativim i nenaplativim komponentama na predmetima ugovora.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083517"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurišite naplative komponente za predmet ugovora zasnovan na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Predmet ugovora zasnovan na projektu ima koncept uključenih, naplativih i nenaplativih komponenti.

Uključene komponente podležu načinu naplate, podeli klijenata, ograničenjima koja se ne smeju premašiti i podešavanjima učestalosti fakturisanja definisanim u okviru predmeta ugovora zasnovanog na projektu.

Podskup uključenih komponenti može se označiti kao naplativ ažuriranjem polja **Tip obračuna**.

Komponente koje se naplaćuju mogu se definisati na ulogama i kategorijama transakcija.

Za predmet ugovora o projektu, naplativost definisana na ulozi odnosi se samo na klasu transakcija **Vreme**. Ako je **Uključi vreme** postavljeno na **Ne** na predmetu ugovora za projekat, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost definisana u kategorijama transakcija za predmet ugovora o projektu odnosi se samo na klasu transakcija **Trošak**. Ako je **Uključi troškove** postavljeno na **Ne** na predmetu ugovora za projekat, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažurirajte ulogu da bude naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa na određenom predmetu ugovora zasnovanom na projektu.

Na kartici **Uloge koje se naplaćuju** na predmetu ugovora zasnovanom na projektu, na podformi **Kategorije koje se naplaćuju** , u polju **Tip obračuna** ažurirajte tip obračuna za ulogu.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa

Kategorija transakcija može biti naplativa ili nenaplativa na određenom predmetu ugovora zasnovanom na projektu.

Na kartici **Kategorije koje se naplaćuju** na predmetu ugovora zasnovanom na projektu, na podformi **Kategorije koje se naplaćuju** , u polju **Tip obračuna** ažurirajte tip obračuna za transakciju.

### <a name="resolve-chargeability"></a>Rešite naplativost

Procena ili stvarna vrednost kreirana za vreme smatraće se naplativom samo ako je vreme uključeno u predmet ugovora i ako je uloga konfigurisana kao naplativa na predmetu ugovora.

Procena ili stvarna vrednost kreirana za trošak smatraće se naplativom samo ako je trošak uključen u predmet ugovora i ako je kategorija transakcije konfigurisana kao naplativa na predmetu ugovora.

| Sadrži vreme | Sadrži trošak | Uloga | Kategorija | Zadatak |
| --- | --- | --- | --- | --- |
| Da | Da | Naplativo | Naplativo | Obračun u stvarnom vremenu: Naplativo </br>Tip obračuna na stvarnom trošku: Naplativo |
| Da | Da | Nenaplativo | Naplativo | Obračun u stvarnom vremenu: Nenaplativo </br>Tip obračuna na stvarnom trošku: Naplativo |
| Da | Da | Nenaplativo | Nenaplativo | Obračun u stvarnom vremenu: Nenaplativo </br>Tip obračuna na stvarnom trošku: Nenaplativo |
| No | Da | Nije moguće podesiti | Naplativo | Obračun u stvarnom vremenu: Nije dostupno </br>Tip obračuna na stvarnom trošku: Naplativo |
| No | Da | Nije moguće podesiti | Nenaplativo | Obračun u stvarnom vremenu: Nije dostupno </br>Tip obračuna na stvarnom trošku: Nenaplativo |
| Da | No | Naplativo | Nije moguće podesiti | Obračun u stvarnom vremenu: Naplativo </br>Tip obračuna na stvarnom trošku: Nije dostupno |
| Da | No | Nenaplativo | Nije moguće podesiti | Obračun u stvarnom vremenu: Nenaplativo </br> Tip obračuna na stvarnom trošku: Nije dostupno |
