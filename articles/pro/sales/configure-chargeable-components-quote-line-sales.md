---
title: Konfigurišite naplative komponente stavke ponude – jednostavno
description: Ova tema pruža informacije o podešavanju naplativih i nenaplativih komponenata na liniji ponude zasnovanoj na projektu.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177123"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurišite naplative komponente stavke ponude – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Linija ponude zasnovana na projektu ima koncept *uključenih* komponenti i *naplativih* komponenti.

Uključene komponente podležu:

  - Načinu naplate i podelama klijenata
  - Ograničenja koja ne smeju da se prekorače 
  - Podešavanja učestalosti fakture definisane u liniji ponude zasnovane na projektu

Podskup uključenih komponenti može se označiti kao naplativ pomoću polja **Tip obračuna**. Polje **Tip obračuna** je skup opcija koji omogućava sledeće vrednosti u kontekstu linije ponude:

  - Naplativo
  - Nenaplativo

Komponente koje se naplaćuju mogu se definisati na zadacima, ulogama i kategorijama transakcija.

Naplativost je definisana na zadacima za liniju ponude i odnosi se na sve klase transakcija uključene u tu liniju. Ako je polje **Uključi zadatke** prazno ili postavljeno na **Čitav projekat**, kartica **Zadaci koji se naplaćuju** neće biti dostupna.

Naplativost je definisana u ulogama za liniju ponude i odnosi se samo na klasu transakcija **Vreme**. Ako je polje **Uključi vreme** postavljeno na **Ne** na liniji ponude projekta, kartica **Uloge koje se naplaćuju** neće biti dostupna.

Naplativost je definisana u kategorijama transakcija za liniju ponude i odnosi se samo na klasu transakcija **Trošak**. Ako je polje **Uključi troškove** postavljeno na **Ne** na liniji ponude projekta, kartica **Kategorije koje se naplaćuju** neće biti dostupna.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Ažurirajte projektni zadatak tako da bude naplativ ili nenaplativ

Projektni zadatak može biti naplativ ili nenaplativ u kontekstu određene linije ponude zasnovane na projektu, što omogućava sledeće podešavanje:

Ako linija ponude zasnovana na projektu uključuje **Vreme** i zadatak **T1**, zadatak je povezan sa linijom ponude kao naplativ. Ako postoji druga linija ponude koja uključuje **Troškove**, zadatak **T1** na liniji ponude možete povezati kao nenaplativ. Rezultat je da je sve vreme evidentirano u zadatku naplativo, a svi troškovi evidentirani u zadatku nenaplativi.

Tip naplate zadatka može se konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**. Pored toga, možete da ažurirate tip naplate za projektni zadatak u polju **Tip naplate** na podformi zadatka Postavljanje obračuna projekta koje prikazuje stavke ponude povezane sa zadatkom.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažurirajte ulogu da bude naplativa ili nenaplativa

Uloga može biti naplativa ili nenaplativa u kontekstu određene linije ponude zasnovane na projektu.

Tip naplate uloge se može konfigurisati na kartici **Naplativi zadaci** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Zadaci stavke ponude**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa

Kategorija transakcija može biti naplativa ili nenaplativa na određenoj liniji ponude.

Tip naplate transakcije se može konfigurisati na kartici **Naplative kategorije** stavke ponude zasnovane na projektu ažuriranjem polja **Tip naplate** na podformi **Naplative kategorije**.

### <a name="resolve-chargeability"></a>Rešite naplativost
Procena ili stvarna vrednost kreirana za vreme smatraće se naplativom samo ako je **Vreme** uključeno u predmet ugovora i ako su **Zadatak** i **Uloga** konfigurisani kao naplativi na liniji ponude.

Procena ili stvarna vrednost kreirana za trošak smatraće se naplativom samo ako je **Trošak** uključen u liniju ponude i ako su kategorije **Zadatak** i **Transakcija** konfigurisane kao naplative na liniji ponude.

| Sadrži vreme | Sadrži trošak | Obuhvaćeni zadaci | Uloga | Kategorija | Zadatak | Naplata |
| --- | --- | --- | --- | --- | --- | --- |
| Da | Da | Čitav projekat | Naplativo | Naplativo | Nije moguće podesiti | Obračun u stvarnom vremenu: Naplativo </br>Tip obračuna na stvarnom trošku: Naplativo |
| Da | Da | Samo izabrani zadaci | Naplativo | Naplativo | Naplativo | Obračun u stvarnom vremenu: Naplativo</br>Tip obračuna na stvarnom trošku: Naplativo |
| Da | Da | Samo izabrani zadaci | Nenaplativo | Naplativo | Naplativo | Obračun u stvarnom vremenu: Nenaplativo</br>Tip obračuna na stvarnom trošku: Naplativo |
| Da | Da | Samo izabrani zadaci | Naplativo | Naplativo | Nenaplativo | Obračun u stvarnom vremenu: Nenaplativo</br> Tip obračuna na stvarnom trošku: Nenaplativo |
| Da | Da | Samo izabrani zadaci | Nenaplativo | Naplativo | Nenaplativo | Obračun u stvarnom vremenu: Nenaplativo</br> Tip obračuna na stvarnom trošku: Nenaplativo |
| Da | Da | Samo izabrani zadaci | Nenaplativo | Nenaplativo | Naplativo | Obračun u stvarnom vremenu: Nenaplativo</br> Tip obračuna na stvarnom trošku: Nenaplativo |
| No | Da | Čitav projekat | Nije moguće podesiti | Naplativo | Nije moguće podesiti | Obračun u stvarnom vremenu: Nije dostupno </br>Tip obračuna na stvarnom trošku: Naplativo |
| No | Da | Čitav projekat | Nije moguće podesiti | Nenaplativo | Nije moguće podesiti | Obračun u stvarnom vremenu: Nije dostupno </br>Tip obračuna na stvarnom trošku: Nenaplativo |
| Da | No | Čitav projekat | Naplativo | Nije moguće podesiti | Nije moguće podesiti | Obračun u stvarnom vremenu: Naplativo</br>Tip obračuna na stvarnom trošku: Nije dostupno |
| Da | No | Čitav projekat | Nenaplativo | Nije moguće podesiti | Nije moguće podesiti | Obračun u stvarnom vremenu: Nenaplativo </br>Tip obračuna na stvarnom trošku: Nije dostupno |