---
title: Konfigurisanje naplativih komponenti predmeta ugovora za projekat
description: Ova tema pruža informacije o uključenim, naplativim i nenaplativim komponentama na predmetima ugovora.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 60a2792f7783053a288303e1dcc01a986e948300
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858355"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurisanje naplativih komponenti predmeta ugovora za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Predmet ugovora zasnovan na projektu ima koncept uključenih, naplativih i nenaplativih komponenti.

Uključene komponente podležu načinu naplate, podeli klijenata, ograničenjima koja se ne smeju premašiti i podešavanjima učestalosti fakturisanja definisanim u okviru predmeta ugovora zasnovanog na projektu.

Podskup uključenih komponenti može se označiti kao naplativ ažuriranjem polja **Tip obračuna**.

Komponente koje se naplaćuju mogu se definisati na ulogama i kategorijama transakcija.

Za predmet ugovora o projektu, naplativost definisana na ulozi odnosi se samo na klasu transakcija **Vreme**. Ako je **Uključi vreme** postavljeno na **Ne** na predmetu ugovora za projekat, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost definisana u kategorijama transakcija za predmet ugovora o projektu odnosi se samo na klasu transakcija **Trošak**. Ako je **Uključi troškove** postavljeno na **Ne** na predmetu ugovora za projekat, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažurirajte ulogu da bude naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa na određenom predmetu ugovora zasnovanom na projektu.

Na kartici **Naplative uloge** predmeta ugovora zasnovanog na projektu, u podformi **Naplative kategorije**, u polju **Tip naplate** ažurirajte vrstu obračuna za ulogu.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa

Kategorija transakcija može biti naplativa ili nenaplativa na određenom predmetu ugovora zasnovanom na projektu.

Na kartici **Naplative kategorije** predmeta ugovora zasnovanog na projektu, u podformi **Naplative kategorije**, u polju **Tip naplate** ažurirajte vrstu obračuna za transakciju.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
