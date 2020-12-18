---
title: Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu – jednostavno
description: Ova tema pruža informacije o tome kako dodati naplative komponente u predmete ugovora u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513896"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurisanje naplativih komponenti za predmet ugovora zasnovan na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Predmet ugovora zasnovan na projektu ima *uključene* komponente i *naplative* komponente.

Uključene komponente su komponente koje podležu:

  - Načinu naplate i podelama klijenata
  - Ograničenja koja ne smeju da se prekorače 
  - Postavke učestalosti fakture definisane u predmetu ugovora zasnovanog na projektu

Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**. Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu predmeta ugovora:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.

Naplativost je definisana na zadacima za predmet ugovora o projektu i odnosi se na sve klase transakcija uključene u liniju. Ako je polje **Uključi zadatke** na predmetu ugovora prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.

Naplativost definisana u ulogama za predmet ugovora o projektu odnosi se samo na klasu transakcija **Vreme**. Ako je polje **Uključi vreme** na predmetu ugovora postavljeno na **Ne**, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost definisana u kategorijama transakcija za predmet ugovora o projektu odnosi se samo na klasu transakcija **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne**, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Ažurirajte projektni zadatak kao naplativi ili nenaplativi

Projektni zadatak može biti naplativ ili nenaplativ na određenom predmetu ugovora što omogućava sledeće podešavanje:

Ako predmet ugovora zasnovan na projektu uključuje **Vreme** i određeni zadatak, **T1** je povezan sa njim kao naplativ. Ako postoji drugi predmet ugovora koji uključuje **Trošak**, zadatak T1 na predmetu ugovora liniji možete povezati kao nenaplativ. Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi nenaplativi.

Tip naplate zadatka može se konfigurisati na kartici **Zadaci koji se naplaćuju** predmeta ugovora ažuriranjem polja **Tip naplate** na podformi zadataka predmeta ugovora. Pored toga, možete da ažurirate polje **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje predmete ugovora povezane sa zadatkom.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Ažurirajte ulogu kao naplativu ili nenaplativu

Uloga može biti naplativa ili nenaplativa na određenom predmetu ugovora.

Tip obračuna uloge može se konfigurisati na kartici **Uloge koje se naplaćuju** predmeta ugovora. Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative uloge**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija kao naplativu ili nenaplativu

Kategorija transakcija može biti naplativa ili nenaplativa na određenom predmetu ugovora.

Tip obračuna transakcije može se konfigurisati na kartici **Kategorije koje se naplaćuju** predmeta ugovora zasnovanom na projektu. Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rešite naplativost

Procena ili stvarna vrednost kreirana za vreme smatraće se naplativom samo ako je **Vreme** uključeno u predmet ugovora i ako su **Zadatak** i **Uloga** konfigurisani kao naplativi na predmetu ugovora.

Procena ili stvarna vrednost kreirana za trošak smatraće se naplativom samo ako je **Trošak** uključen u predmet ugovora i ako su kategorije **Zadatak** i **Transakcija** konfigurisani kao naplative na predmetu ugovora.


| Sadrži vreme | Sadrži trošak | Sadrži zadatke | Uloga           | Kategorija       | Zadatak                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Da           | Da              | Čitav projekat | Naplativo     | Naplativo     | Obračun u stvarnom vremenu: **Naplativo** </br> Vrsta obračuna na stvarnom trošku: **Naplativo**           |
| Da           | Da              | Izabrani zadaci | Naplativo     | Naplativo     | Obračun u stvarnom vremenu: **Naplativo** </br> Vrsta obračuna na stvarnom trošku: **Naplativo**           |
| Da           | Da              | Izabrani zadaci | Nenaplativo | Naplativo     | Obračun u stvarnom vremenu: **Nenaplativo** </br> Vrsta obračuna na stvarnom trošku: **Naplativo**       |
| Da           | Da              | Izabrani zadaci | Naplativo     | Naplativo     | Obračun u stvarnom vremenu: **Nenaplativo** </br> Tip obračuna na stvarnom trošku:   **Nenaplativo** |
| Da           | Da              | Izabrani zadaci | Nenaplativo | Naplativo     | Obračun u stvarnom vremenu: **Nenaplativo** </br> Tip obračuna na stvarnom trošku:   **Nenaplativo** |
| Da           | Da              | Izabrani zadaci | Nenaplativo | Nenaplativo | Obračun u stvarnom vremenu: **Nenaplativo** </br> Tip obračuna na stvarnom trošku:   **Nenaplativo** |
| No            | Da              | Čitav projekat | Nije moguće podesiti   | Naplativo     | Obračun u stvarnom vremenu: **Nije dostupno**</br>Vrsta obračuna na stvarnom trošku: **Naplativo**          |
| No            | Da              | Čitav projekat | Nije moguće podesiti   | Nenaplativo | Obračun u stvarnom vremenu: **Nije dostupno**</br> Tip obračuna na stvarnom trošku: **Nenaplativo**     |
| Da           | No               | Čitav projekat | Naplativo     | Nije moguće podesiti   | Obračun u stvarnom vremenu: **Naplativo** </br> Tip obračuna na stvarnom trošku: **Nije dostupno**        |
| Da           | No               | Čitav projekat | Nenaplativo | Nije moguće podesiti   | Obračun u stvarnom vremenu: **Nenaplativo** </br>Tip obračuna na stvarnom trošku: **Nije   dostupno**   |
