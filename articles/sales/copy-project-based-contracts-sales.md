---
title: Kopiranje ugovora zasnovanih na projektu
description: Ovaj članak pruža informacije o kopiranju ugovora za projekat u usluzi Microsoft Dynamics 365 Project Operations.
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

Možete lako kreirati nove projektne ugovore kopiranjem postojećih ugovora na jedan od dva načina:

- Na stranici liste **Ugovori o projektima** izaberite ugovor za projekat, a zatim izaberite **Kopiraj**.
- Na stranici detalja **Ugovori za projekat** izaberite **Kopiraj**.

U oba slučaja, otvoriće se dijalog u kom možete postaviti parametre kopiranog ugovora. Sledeća polja su uključena u dijalog. U zavisnosti od vrednosti koje izaberete postupak kopiranja se može promeniti.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| Tema | Unesite temu ciljnog ugovora. Kada se dijalog otvori, sistem podešava polje na naziv izvornog ugovora, ali se reč „kopija“ dodaje njemu. | Nema posledičnog uticaja za ovo polje. |
| klijentu | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se dijalog otvori, sistem postavlja ovo polje na poslovni kontakt u izvornom ugovoru. | Ovo polje je primarni klijent u ugovoru. |
| Preduzeće-vlasnik | Preduzeće koje je odgovorno za isporuku projekata koji su povezani sa ovom pogodbom. Kada se dijalog otvori, sistem postavlja ovo polje na vlasničko preduzeće u izvornom ugovoru. | Vlasničko preduzeće je pravni subjekt koje će izvršavati projekte nakon zaključenja pogodbe. Valuta vlasničkog preduzeća mora da se podudara sa valutom ugovorne jedinice. |
| Jedinica ugovaranja | Organizaciona jedinica koja je odgovorna za isporuku projekata koji su povezani sa ovom pogodbom. Kada se dijalog otvori, sistem postavlja ovo polje na jedinicu ugovaranja u izvornom ugovoru. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršavati projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu. Ova valuta se koristi za izveštavanje o procenjenim i stvarnim troškovima koji su nastali tokom projekta. |
| Valuta | Valuta u kojoj se obavljaju transakcije u pogodbi. Kada se dijalog otvori, sistem postavlja polje na valutu izvornog ugovora. Nije moguće promeniti valutu. Ako jeste, polje **Kopiraj cene** je uvek postavljeno na **Ne** jer cenovnici u izvornom ugovoru više nisu relevantni. | Ova valuta se koristi za podrazumevani cenovnik, za generisanje finansijskih procena na ugovoru i za fakturisanje klijentu kada se pogodba ostvari. |
| Zahtevani datum isporuke | Datum isporuke koji je klijent zahtevao. | Ovaj datum se koristi kao datum završetka prilikom kreiranja datuma fakturisanja prema određenoj učestalosti. |
| Kopiranje određivanja cene | Vrednost koja ukazuje na to da li određivanje cene na ugovoru treba kopirati iz izvornog ugovora. | Ako je polje podešeno na **Da**, reference na cenovnik projekta i cenovnik proizvoda se kopiraju iz izvornog u ciljni ugovor. Ako je podešeno na **Ne**, koriste se podrazumevani cenovnici na osnovu najnovijih cenovnika u parametrima poslovnog kontakta ili projekta. |

Kada na stranici dijaloga izaberete **U redu**, sistem kreira kopiju ugovora na osnovu vrednosti parametara koje ste postavili. Zatim se otvara novi ugovor.

Sledeće informacije se **ne** kopiraju iz izvornog u ciljni ugovor, jer su specifične za svaki ugovor:

- Rasporedi za fakturisanje
- Ugovor i klijenti predmeta ugovora
- Referenca projekta u predmetima ugovora zasnovanih na projektu
- Informacije o budžetu klijenta

Kopiraju se predmeti ugovora za projekte i proizvode, procene u detaljima predmeta ugovora i vrednosti koje ne smeju da premaše vrednost na nivou ugovora. Unos podrazumevanih cena i stopa troškova zavisi od izbora u polju **Kopiranje određivanja cena** u dijalogu **Kopiranje parametara**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
