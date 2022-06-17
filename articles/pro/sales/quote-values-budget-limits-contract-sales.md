---
title: Rezime informacija o ponudi za projekat – jednostavno
description: Ovaj članak pruža informacije o informacijama i postavkama koje se odnose na ponude projekata i utiču na njih. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3441348cb46804f8f76cb23b3f916fe69c3fbe99
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917041"
---
# <a name="header-details-for-project-quotes"></a>Detalji zaglavlja za ponude za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak objašnjava informacije koje se odnose na ponudu za projekat. To uključuje podešavanja koja utiču na sve stavke ponude i informacije o ponudi koje su sažete u svim stavkama za pokretanje KPI-ova ponude za projekat.

Sledeća tabela navodi polja sa rezimiranim informacijama u ponudi projekta koja su jedinstvena za Dynamics 365 Project Operations ili imaju neke važne promene u ponašanju u odnosu na ponude u usluzi Dynamics 365 Sales.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip | Kartica sa rezimeom (skrivena) | Ovo polje skupa opcija ima sledeće opcije:</br>- Zasnovano na poslu (dostupno samo kada je instalirana usluga Project Operations)</br>- Zasnovano na stavci (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- Zasnovano na servisnom održavanju (dostupno kada je instalirana usluga Dynamics 365 Field Service) | Kada koristite aplikaciju Project Operations, vrednost ovog polja se automatski postavlja na opciju **Zasnovano na poslu**. To klasifikuje ponudu kao ponudu zasnovanu na projektu. Ponuda treba da se zasniva na projektu kako bi se omogućila sva proširenja i funkcije specifične za projekat. |
| Potencijalni klijent | Kartica rezimea | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Valuta u ponudi za projekat se podrazumevano zasniva na valuti klijenta. Međutim, to može da se promeni pre nego što se ponuda sačuva. |
| Menadžer za poslovne kontakte | Kartica rezimea | Ime menadžera poslovnog kontakta za ovu pogodbu. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Menadžer poslovnog kontakta je odgovoran za upravljanje odnosom sa klijentom kroz završetak ovog projekta. Na osnovu zapisa resursa koji može da se rezerviše povezanog sa menadžerom poslovnog kontakta, ugovorna jedinica se podrazumeva iz ponude za projekat. |
| Jedinica ugovaranja | Kartica rezimea | Organizaciona jedinica koja je odgovorna za isporuku projekta ili projekata povezanih sa ovom ponudom. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršavati projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom izvršavanja projekta. |
| Cenovnik proizvoda | Kartica rezimea | Ovo je cenovnik koji se koristi za određivanje podrazumevanih cena u stavkama ponuda zasnovanim na proizvodima. Lista opcija za ovo polje prikazuje listu cenovnika gde se valuta cenovnika podudara sa valutom u ponudi. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. Ovo polje u mogućnosti za poslovanje se podrazumeva iz zapisa poslovnog kontakta, ali se može promeniti. | Kada se ponuda ostvari, vrednost polje se kopira u ugovor o projektu koji se kreira. |
| Valuta | Kartica rezimea | To ukazuje na valutu koja će se koristiti za izveštavanje o vrednosti ove pogodbe. To je takođe valuta u kojoj će se klijentu fakturisati ako se ostvari pogodba. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. Ovo polje u mogućnosti za poslovanje se podrazumeva iz zapisa poslovnog kontakta, ali korisnik je može promeniti. | Kada se ponuda sačuva, ovo polje više nije moguće uređivati. Ovo se koristi da se odrede podrazumevani cenovnici proizvoda i projekta u ponudi. Valuta u ponudi se koristi za podudaranje valute sa cenovnikom. |
| Ograničenje koje ne sme da se prekorači | Kartica rezimea | Ovo ukazuje na dogovoreno gornje ograničenje konačne vrednosti sa kojim se klijent slaže za ovaj posao. | Ovo gornje ograničenje se procenjuje tokom izvršenja i primenljivo je na sve stavke i projekte povezane sa ovom pogodbom. |
| Zahtevani datum isporuke | Kartica rezimea | Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Ovaj datum se koristi kao datum završetka za generisanje rasporeda za fakturisanje. |

U nastavku su kartice i KPI-ovi dostupni na ponudi za projekt koji su jedinstveni za Project Operations ili imaju neke važne promene u ponašanju iz ponuda za prodaju:

| **Polje** | **Lokacija** | **Opis** |
| --- | --- | --- |
| Analiza isplativosti | Kartica u ponudi | Kartica prikazuje sledeće metrike:</br>- Ukupni naplativi troškovi</br></br>- Ukupni nenaplativi troškovi</br>- Ukupan prihod</br>- Ukupni prihod (osnovni)</br>- Bruto marža</br>- Prilagođena bruto marža|
| Poređenje sa očekivanjima klijenta | Kartica u ponudi | Ova kartica prikazuje sledeće metrike:</br>- Procenjeni završetak</br>- Zahtevani završetak</br>- Budžet klijenta</br>- Vrednost ponude |
| Analiza ponude | Kartica u ponudi | Ova kartica rezimira sledeće najvažnije KPI-ove za ponudu za projekat</br>- Poređenje sa očekivanjima klijenata za budžet i raspored</br>- Bruto marža</br>- Prilagođena bruto marža |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
