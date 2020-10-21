---
title: Predmeti mogućnosti za poslovanje zasnovani na projektu (Pro)
description: Ova tema pruža informacije o predmetima mogućnosti za poslovanje zasnovanim na projektu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896388"
---
# <a name="project-based-opportunity-lines-pro"></a>Predmeti mogućnosti za poslovanje zasnovani na projektu (Pro)

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Predmeti mogućnosti za poslovanje zasnovani na projektu dostupni su samo u okviru mogućnosti za poslovanje zasnovanih na projektu. Zapisi mogućnosti za poslovanje zasnovani na projektu imaju polje **Tip** postavljeno na **Zasnovano na poslu**.

Predmeti mogućnosti za poslovanje zasnovani na projektu su stavke koje će biti isporučene klijentu korišćenjem projekta. Međutim, projekat ne može biti vezan za predmet mogućnosti za poslovanje zasnovan na projektu. Projekti se mogu vezati za stavke iz faze **ponude** i kasnije, jer mogućnost za poslovanje je obično u ranoj fazi životnog ciklusa pogodbe. Određivanje broja projekata koji će se koristiti za isporuku posla klijentu je odluka koja se donosi kasnije u fazi prodaje. Fazu mogućnosti za poslovanje možete koristiti za identifikovanje diskretnih komponenti isporuke za klijenta. Odluke u vezi sa stvarnim brojem projekata koji se koriste za isporuku ovih komponenti mogu se odbaciti dok se ne sazna više informacija o samom radu.

Ispod su polja u predmetu mogućnosti za poslovanje zasnovanom na projektu:

| **Polje** | **Lokacija** | **Relevantnost, svrha i smernice** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip proizvoda | Kartica Opšti podaci (skrivena) | Možete da izaberite neku od sledećih opcija:</br>- Usluga zasnovana na projektu (dostupna samo kada je instalirana usluga Dynamics 365 Project Operations)</br>- Proizvod (dostupan samo kada su instalirane usluge Project Operations i Dynamics 365 Sales) | Vrednost ovog polja je postavljena na **Usluga zasnovana na projektu** kada kreirate stavku mogućnosti za poslovanje zasnovanu na projektu iz mreže stavki zasnovanih na projektu u mogućnosti za poslovanje. <br> Ako promenite ili zamenite ovu vrednost, funkcionalnost projekta neće biti omogućena na stavkama zasnovanim na projektu. |
| Mogućnost za poslovanje | Kartica Opšti podaci | Ovo polje je samo za čitanje i odnosi se na nadređeni zapis mogućnosti za poslovanje kojem pripada ova stavka. | Nema posledičnog uticaja iz ovog polja. |
| +Ime | Kartica Opšti podaci | Ovo tekstualno polje podložno uređivanju može se koristiti za davanje kratkog identiteta stavci. | Ova vrednost se prenosi na stavku ponude kada kreirate ponudu iz ove mogućnosti za poslovanje. |
| Budžet klijenta | Kartica Opšti podaci | Ovo polje valute za uređivanje može se koristiti za praćenje iznosa koji je klijent spreman da potroši za ovu stavku. | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje. |
| Način naplate | Kartica Opšti podaci | Ovo polje podložno uređivanju ima sledeće vrednosti:</br>- Vreme i materijal</br>- Fiksna cena | Ova vrednost se prenosi na odgovarajuće polje stavke ponude kada ponudu kreirate iz ove mogućnosti za poslovanje. Kada kreirate stavku ponude, polje je zaključano i ne može se promeniti. Dodelite vrednost ovog polja što je tačnije moguće. Ako je potrebno da promenite vrednost ovog polja u stavci ponude, izbrišite i ponovo kreirajte stavku ponude. |
