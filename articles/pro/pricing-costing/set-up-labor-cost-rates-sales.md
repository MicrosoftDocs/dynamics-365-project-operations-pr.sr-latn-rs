---
title: Podešavanje troškova rada
description: Ova tema pruža informacije o tome kako postaviti stope za troškove rada u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66a254ce4e7c7f25ac3ea303b73a01625988b0d9
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083491"
---
# <a name="setting-up-labor-cost-rates"></a>Podešavanje troškova rada 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Svaki cenovnik ima skup stopa rada (cene uloga) koje se poklapaju sa sadržajem i efektivnošću datuma cenovnika.

1. Napravite cenovnik i na kartici **Uloga cena** , u podmreži odaberite **Nova uloga**.
2. Na stranici **Brzo kreiranje** , izaberite ulogu i organizacionu jedinicu.
3. Unesite informacije u obavezna polja.

Sledeća tabela uključuje neka od polja koja su važna za stvaranje stopa radne snage na cenovniku troškova.

| Polje | Lokacija | Relevantnost, svrha i smernice | Posledični uticaj |
| --- | --- | --- | --- |
| Uloga | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Odaberite ulogu na koju se odnosi stopa cene. | Uloga na dolaznoj proceni ili trenutnom stanju će se podudarati sa ovom linijom kako bi se zadali troškovi uloge. |
| Jedinica za određivanje resursa | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Izaberite organizacionu jedinicu ili odeljenje kompanije odakle će se koristiti ova uloga. Na primer, programer iz odeljenja za robotiku kompanije Fabrikam Indija ili programer iz odeljenja softvera kompanije Fabrikam SAD. | Jedinica koja određuje resurse na dolaznoj proceni ili trenutnom stanju će se podudarati sa ovom linijom kako bi se zadala stopa cene uloge. |
| Cena | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Postavite stopu troškova za ulogu, preduzeće koje određuje resurse i kombinaciju jedinica za obezbeđivanje resursa. Na primer, programer iz kompanije Fabrikam Indija košta 1000 INR ili programer iz kompanije Fabrikam SAD košta 150 USD. | Cena je stopa troškova koja podrazumeva jedinični trošak dolazne procene ili stvarne linije za klasu transakcije **Vreme**. |
| Valuta | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Vrednost valute podrazumevano potiče iz valute iz zaglavlja cenovnika, ali se može zameniti. Na primer, programer iz kompanije Fabrikam Indija košta 1000 INR. Programer iz kompanije Fabrikam SAD košta 150 USD. | Ova valuta podrazumeva jedinični trošak dolazne stvarne linije troškova za klasu transakcije **vreme**. Na proceni projekta, vrednost valute se pretvara u valutu projekta i prikazuje na vremenskom prikazu procene. |
| Raspored jedinica | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Raspored jedinica podrazumevano ima vrednost Vreme i ne može se promeniti u entitetu cene uloga jer se koristi ekspresna stopa po jedinicama vremena. | Nema posledičnog uticaja. |
| Jedinica | Kartica **Opšti podaci** i stranice **Brzo kreiranje** | Vrednost valute podrazumevano potiče iz polja **Jedinica vremena** u zaglavlju cenovnika. Vrednost se može zameniti. Na primer, programer iz kompanije Fabrikam Indija košta 1000 INR po **danu u Indiji**. Programer iz kompanije Fabrikam SAD košta 150 USD po **danu u SAD**. | Sistem koristi sistem jedinica i konverziju u osnovne jedinice za izračunavanje troškova po jedinici radi izračunavanja zadate cene po jedinici na dolaznoj proceni ili stvarnoj liniji. Na primer, procena je za posao od 10 **dana u Indiji** za programera iz Indije, a jedinica, **dan u Indiji** se definiše kao 10 sati. Kada obračunava tu liniju procene, aplikacija izračunava jedinični trošak na proceni kao: 1000 INR/10 sati = 100 INR po satu koji se pretvara u USD i prikazuje kao jedinični trošak na stranici **Projektne procene**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Prenesite cene i troškove za resurse izvan vašeg odeljenja ili pravnog lica

U kompanijama zasnovanim na projektima uobičajeno je da se na projektima koriste zaposleni iz različitih pravnih lica ili odeljenja. Projekat može izvršiti jedno pravno lice, ali zaposleni ili konsultanti koji rade na projektu mogu poticati iz istog pravnog lica ili iz drugog, ili može biti kombinacija oba. U programu Dynamics 365 Project Operations pravno lice koje je vlasnik projekta je **Preduzeće-vlasnik** , a odeljenje koje je vlasnik isporuke je **Jedinica ugovaranja**. Ostala pravna lica koja pružaju resurse su **Preduzeća koja određuju resurse** , a odeljenja koja pružaju resurse su **Jedinice za određivanje resursa**. U većini zemalja kompanije su dužne da osiguraju da pravno lice ili odeljenje za resurse zadužuju kompaniju koja je vlasnik i ugovornu jedinicu za korišćenje resursa.

Na primer, korporacija Fabrikam mora da obezbedi da Fabrikam India-Robotics ima ugovorenu cenovnu kartu sa Fabrikam US-Robotics ili Fabrikam UK-Robotics.

Programer iz Fabrikam India-Robotic naplaćuje 100 USD kada je pozajmljen kompaniji Fabrikam US-Robotics i 150 USD kada je pozajmljen kompaniji Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Podesite troškove za spoljne resurse

1. Napravite cenovnik troškova pod nazivom *Fabrikam US-Robotics stope troškova* i postavite opseg datuma važenja.
2. U cenovniku troškova podesite stope koristeći informacije iz sledeće tabele. 

| Uloga | Preduzeće koje određuje resurse | Jedinica za određivanje resursa | Stopa troškova |
| --- | --- | --- | --- |
| Projektant | Fabrikam India | Fabrikam India-Robotics | $100 |
| Projektant | Fabrikam Philippines | Fabrikam Philippines-Robotics | 90 USD |
| Projektant | Fabrikam US | Fabrikam US-Robotics | 150 USD |

3. Ovaj cenovnik priložite organizacionoj jedinici Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Podesite cene prenosa za resurs u odgovarajućoj valuti 

U usluzi Project Operations, određivanje cene resursa može se izvršiti u bilo kojoj valuti. Podrazumevana vrednost valute je ona koja se nalazi u zaglavlju cenovnika, ali se može promeniti.

Koristeći primer za podešenu cenu prenosa, informacije se mogu promeniti u:

Korporacija Fabrikam mora da obezbedi da Fabrikam India-Robotics ima ugovorenu cenu sa Fabrikam US-Robotics ili Fabrikam UK-Robotics.

Programer iz Fabrikam India-Robotics košta 5000 INR kada je pozajmljen kompaniji Fabrikam US-Robotics i 5500 INR kada je pozajmljen kompaniji Fabrikam UK-Robotics.

U cenovniku troškova za Fabrikam US-Robotics stope troškova mogu se izraziti kao:

| Uloga | Preduzeće koje određuje resurse | Cena |
| --- | --- | --- |
| Projektant | Fabrikam India | 5000 INR |
| Projektant | Fabrikam US | 115 USD |

U cenovniku troškova za Fabrikam UK-Robotics stope troškova mogu se izraziti ovako:

| Uloga | Preduzeće koje obezbeđuje resurse | Cena |
| --- | --- | --- |
| Projektant | Fabrikam India | 5500 INR |
| Projektant | Fabrikam UK | 115 GBP |

Cenovnik troškova može da obezbedi stope rada u više valuta. Prilikom generisanja procene troškova na projektu, usluga Project Operations će pretvoriti ove stope troškova u valutu projekta i prikazati ih korisniku. Kada se odobri unos vremena i stvori stvarni trošak, stvarni trošak se određuje u valuti odgovarajuće linije cena uloge na cenovniku troškova. Stvarni troškovi vremena na jednom projektu mogu se evidentirati u više valuta. Međutim, prilikom pravljenja zbirne vrednosti ili sumiranja stvarnih troškova rada na nivou projekta, Project Operations će pretvoriti sve iznose troškova rada u valutu projekta, koju korisnik može prikazati.
