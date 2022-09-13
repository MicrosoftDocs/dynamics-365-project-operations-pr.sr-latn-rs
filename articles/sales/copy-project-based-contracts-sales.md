---
title: Kopiranje ugovora zasnovanih na projektu
description: Ovaj članak pruža informacije o kopiranju ugovora o projektu u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410385"
---
# <a name="copy-project-based-contracts"></a>Kopiranje ugovora zasnovanih na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Nove projektne ugovore možete lako kreirati kopiranjem postojećih ugovora na jedan od dva načina:

- Na stranici **lista Ugovori o** projektu izaberite ugovor o projektu, a zatim kliknite na dugme **Kopiraj**.
- Na stranici detalja **Ugovori za projekat** izaberite **Kopiraj**.

U oba slučaja pojavljuje se dijalog u kome možete da postavite parametre kopiranog ugovora. Dijalog sadrži sledeća polja. U zavisnosti od izabranih vrednosti, proces kopiranja može da se promeni.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| Tema | Unesite temu ciljnog ugovora. Kada se dijalog otvori, sistem postavlja polje na ime izvornog ugovora, ali mu je reč "kopija" pridodato. | Nema posledičnog uticaja za ovo polje. |
| klijentu | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se dijalog otvori, sistem postavlja polje na konto izvornog ugovora. | Ovo polje je primarni klijent u ugovoru. |
| Preduzeće-vlasnik | Preduzeće koje je odgovorno za isporuku projekata koji su povezani sa ovim dogovorom. Kada se dijalog otvori, sistem postavlja polje na preduzeće izvornog ugovora u vlasništvu. | Kompanija u vlasništvu je pravno lice koje će sprovoditi projekat po zaključenju sporazuma. Valuta preduzeća u vlasništvu mora da se podudara sa valutom jedinice za ugovaranje. |
| Jedinica ugovaranja | Organizaciona jedinica koja je odgovorna za isporuku projekata koji su povezani sa ovim dogovorom. Kada se dijalog otvori, sistem postavlja polje na jedinicu ugovora izvornog ugovora. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršavati projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu. Ova valuta se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |
| Valuta | Valuta u kojoj se obavljaju transakcije u pogodbi. Kada se dijalog otvori, sistem postavlja polje na valutu izvornog ugovora. Nije moguće promeniti valutu. Ako jeste, polje Kopiranje **cena je** uvek podešeno na "Ne **·**", jer cenovnici u izvornom ugovoru više nisu relevantni. | Ova valuta se koristi za podrazumevane cenovnike, za generisanje finansijskih procena ugovora i za fakturisanje kupca prilikom dobi ugovora. |
| Zahtevani datum isporuke | Datum dostave koji kupac zahteva. | Ovaj datum se koristi kao krajnji datum kada kreirate datume fakturisanja na određenoj frekvenciji. |
| Kopiranje određivanja cene | Vrednost koja označava da li cene ugovora treba kopirati iz izvornog ugovora. | Ako je polje podešeno na "Da **",** reference na projekat i cenovnik proizvoda se kopiraju iz izvornog ugovora u ciljni ugovor. Ako je podešeno na "Ne **",** koriste se podrazumevani cenovnici na osnovu najnovijih cenovnika u parametrima konta ili projekta. |

Kada u dijalogu **izaberete** opciju "U redu", sistem kreira kopiju ugovora na osnovu vrednosti parametara koje ste postavili. Onda se otvara novi ugovor.

Sledeće informacije se ne **kopiraju** iz izvornog ugovora u ciljni ugovor, jer su specifične za svaki ugovor:

- Rasporedi za fakturisanje
- Ugovor i klijenti predmeta ugovora
- Referenca projekta u predmetima ugovora zasnovanih na projektu
- Informacije o budžetu klijenta

Kopiraju se redovi ugovora za projekte i proizvode, procene u detaljima reda ugovora i vrednosti koje se ne premašuju na nivou ugovora. Unos podrazumevanih cena i cena troškova zavisi od izbora u polju Kopiranje **cena** u dijalogu **Kopiranje** parametara.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
