---
title: Predmeti mogućnosti za poslovanje zasnovani na projektu
description: Ova tema pruža informacije o radu sa predmetima mogućnosti za poslovanje zasnovanim na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cb44f10e2ce02ce57a44252fd99ce769f20d5cb7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011388"
---
# <a name="project-based-opportunity-lines"></a>Predmeti mogućnosti za poslovanje zasnovani na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Predmeti mogućnosti za poslovanje zasnovani na projektu dostupni su samo u okviru mogućnosti za poslovanje zasnovanih na projektu. Zapisi mogućnosti za poslovanje zasnovani na projektu imaju polje **Tip** postavljeno na **Zasnovano na poslu**.

Predmeti mogućnosti za poslovanje zasnovani na projektu su stavke koje će biti isporučene klijentu korišćenjem projekta. Međutim, projekat ne može biti vezan za predmet mogućnosti za poslovanje zasnovan na projektu. Projekti se mogu vezati za stavke iz faze **ponude** i kasnije, jer mogućnost za poslovanje se obično javlja u ranoj fazi životnog ciklusa pogodbe. Određivanje broja projekata koji će se koristiti za isporuku posla klijentu je odluka koja se donosi kasnije u fazi prodaje. Koristite fazu mogućnosti za poslovanje za identifikovanje diskretnih komponenti isporuke za klijenta. Odluke u vezi sa stvarnim brojem projekata koji se koriste za isporuku ovih komponenti mogu se odbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja u predmetu mogućnosti za poslovanje zasnovanom na projektu:

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip proizvoda | Kartica Opšti podaci (skrivena) | Ovo je polje skupa opcija. Ako imate instaliranu uslugu Dynamics 365 Project Operations. jedna od dostupnih opcija je **Usluga zasnovana na projektu**.  | Vrednost ovog polja je postavljena na **Usluga zasnovana na projektu** kada kreirate stavku mogućnosti za poslovanje zasnovanu na projektu iz mreže stavki zasnovanih na projektu u mogućnosti za poslovanje. <br> Ako promenite ili zamenite ovu vrednost, funkcionalnost projekta neće biti omogućena na stavkama zasnovanim na projektu. |
| Mogućnost za poslovanje | Kartica Opšti podaci | Ovo polje je samo za čitanje i odnosi se na nadređeni zapis mogućnosti za poslovanje kojem pripada ova stavka. | Nema posledičnog uticaja ovog polja. |
| +Ime | Kartica Opšti podaci | Ovo je tekstualno polje podložno uređivanju koje se može koristiti za davanje kratkog identiteta ovoj stavci | Ova vrednost se prenosi na stavku ponude kada kreirate ponudu iz ove mogućnosti za poslovanje |
| Budžet klijenta | Kartica Opšti podaci | Ovo polje valute za uređivanje može se koristiti za praćenje iznosa koji je klijent spreman da potroši za ovu stavku. | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje |
| Način naplate | Kartica Opšti podaci | Ovo polje podložno uređivanju ima sledeće vrednosti:</br>- Vreme i materijal</br>- Fiksna cena | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje. Kada kreirate stavku ponude, polje je zaključano i ne može se promeniti. Dodelite vrednost ovog polja što je tačnije moguće. Ako je potrebno da promenite vrednost ovog polja u stavci ponude, izbrišite i ponovo kreirajte stavku ponude. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]