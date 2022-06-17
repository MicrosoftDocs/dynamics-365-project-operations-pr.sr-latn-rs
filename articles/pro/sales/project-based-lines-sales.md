---
title: Stavke mogućnosti za poslovanje zasnovane na projektu – jednostavno
description: Ovaj članak pruža informacije o redovima mogućnosti za poslovanje zasnovanim na projektu. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b5a8fc32ca903d7da2e090137bed358b364902a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914281"
---
# <a name="project-based-opportunity-lines---lite"></a>Stavke mogućnosti za poslovanje zasnovane na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Predmeti mogućnosti za poslovanje zasnovani na projektu dostupni su samo u okviru mogućnosti za poslovanje zasnovanih na projektu. Zapisi mogućnosti za poslovanje zasnovani na projektu imaju polje **Tip** postavljeno na **Zasnovano na poslu**.

Predmeti mogućnosti za poslovanje zasnovani na projektu su stavke koje će biti isporučene klijentu korišćenjem projekta. Međutim, projekat ne može biti vezan za predmet mogućnosti za poslovanje zasnovan na projektu. Projekti se mogu vezati za stavke iz faze **ponude** i kasnije, jer mogućnost za poslovanje je obično u ranoj fazi životnog ciklusa pogodbe. Određivanje broja projekata koji će se koristiti za isporuku posla klijentu je odluka koja se donosi kasnije u fazi prodaje. Fazu mogućnosti za poslovanje možete koristiti za identifikovanje diskretnih komponenti isporuke za klijenta. Odluke u vezi sa stvarnim brojem projekata koji se koriste za isporuku ovih komponenti mogu se odbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja u predmetu mogućnosti za poslovanje zasnovanom na projektu:

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip proizvoda | Kartica Opšti podaci (skrivena) | Možete da izaberite neku od sledećih opcija:</br>- Usluga zasnovana na projektu (dostupna samo kada je instaliran Dynamics 365 Project Operations)</br>- Proizvod (dostupan samo kada su instalirane usluge Project Operations i Dynamics 365 Sales) | Vrednost ovog polja je postavljena na **Usluga zasnovana na projektu** kada kreirate stavku mogućnosti za poslovanje zasnovanu na projektu iz mreže stavki zasnovanih na projektu u mogućnosti za poslovanje. <br> Ako promenite ili zamenite ovu vrednost, funkcionalnost projekta neće biti omogućena na stavkama zasnovanim na projektu. |
| Mogućnost za poslovanje | Kartica Opšti podaci | Ovo polje je samo za čitanje i odnosi se na nadređeni zapis mogućnosti za poslovanje kojem pripada ova stavka. | Nema posledičnog uticaja iz ovog polja. |
| +Ime | Kartica Opšti podaci | Ovo tekstualno polje podložno uređivanju može se koristiti za davanje kratkog identiteta stavci. | Ova vrednost se prenosi na stavku ponude kada kreirate ponudu iz ove mogućnosti za poslovanje. |
| Budžet klijenta | Kartica Opšti podaci | Ovo polje valute za uređivanje može se koristiti za praćenje iznosa koji je klijent spreman da potroši za ovu stavku. | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje. |
| Način naplate | Kartica Opšti podaci | Ovo polje podložno uređivanju ima sledeće vrednosti:</br>- Vreme i materijal</br>- Fiksna cena | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje. Kada kreirate stavku ponude, polje je zaključano i ne može se promeniti. Dodelite vrednost ovog polja što je tačnije moguće. Ako je potrebno da promenite vrednost ovog polja u stavci ponude, izbrišite i ponovo kreirajte stavku ponude. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]