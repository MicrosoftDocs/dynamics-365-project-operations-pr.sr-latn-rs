---
title: Konfigurisanje naplativim komponentama stavke ponude zasnovane na projektu
description: Ova tema pruža informacije o uključenim, naplativim i nenaplativim komponentama na stavkama ponuda zasnovanih na projektu.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642560"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurisanje naplativim komponentama stavke ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavka ponude zasnovane na projektu može sadržati uključene komponente i naplative komponente.

Uključene komponente podležu načinu naplate, podeli između klijenata, ograničenjima koja nije dozvoljeno prekoračiti i podešavanjima učestalosti fakturisanja definisanim na stavci ponude zasnovanoj na projektu.
Podskup obuhvaćenih komponenti može biti označen kao naplativ korišćenjem **Tipa obračuna**. Možete da izaberete jednu od sledećih opcija u polju **Tip obračuna** u kontekstu stavke na ponudi:

   - Naplativo
   - Nenaplativo

Komponente koje se naplaćuju mogu se definisati na ulogama i kategorijama transakcija.

Naplativost koja je definisana na ulogama za stavku ponude za projekat primenjuje se samo na klasu transakcije **Vreme**. Ako stavka ponude za projekat ima **Uključi vreme** = **Ne**, kartica **Naplative uloge** nije dostupna.

Naplativost koja je definisana na kategorijama transakcija za stavku ponude za projekat primenjuje se samo na klasu transakcije **Trošak**. Ako stavka ponude za projekat ima **Uključi trošak** = **Ne**, kartica **Naplative kategorije** nije dostupna.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Ažurirajte ulogu da bude naplativa ili nenaplativa
Uloga može biti naplativa ili nenaplativa na stavci ponude zasnovanoj na projektu. Tip naplate za ulogu možete konfigurisati na kartici **Naplative uloge** stavke ponude zasnovane na projektu. Da biste to uradili, ažurirajte polje **Tip obračuna** na podformi **Naplative uloge**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Ažurirajte kategoriju transakcija da bude naplativa ili nenaplativa
Kategorija transakcija može biti naplativa ili nenaplativa na stavci ponude zasnovanoj na projektu. Tip naplate za transakciju možete konfigurisati na kartici **Naplative kategorije** stavke ponude zasnovane na projektu. Da biste to uradili, ažurirajte polje **Tip naplate** na podformi **Naplative kategorije**. 

## <a name="resolve-chargeability"></a>Rešite naplativost

Procena ili stvarna vrednost kreirana za vreme smatraće se naplativim samo ako je vreme uključeno u stavci ponude i ako je uloga konfigurisana kao naplativa.
Procena ili stvarna vrednost kreirana za trošak smatraće se naplativim samo ako je trošak uključen u stavci ponude i ako je kategorija transakcija konfigurisana kao naplativa na stavci ponude. Sledeća tabela prikazuje kako je naplativost podrazumevana za svaku stvarnu vrednost. Podrazumevane vrednosti se zasnivaju na uključenim komponentama i tipu obračuna koji je konfigurisan na stavci ponude.

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