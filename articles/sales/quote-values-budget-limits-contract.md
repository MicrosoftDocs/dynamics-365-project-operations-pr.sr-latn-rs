---
title: Rezime informacija o ponudi za projekat
description: Ova tema pruža informacije o informacijama i podešavanjima koji se odnose na ponude za projekte i utiču na njih.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde5305f179e9a4454bf97c44f1ebdf9986dd43
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908531"
---
# <a name="summary-information-on-a-project-quote"></a>Rezime informacija o ponudi za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Ovaj članak objašnjava informacije koje se odnose na ponudu za projekat. To uključuje podešavanja koja utiču na sve stavke ponude i informacije o ponudi koje su sažete u svim stavkama za pokretanje KPI-ova ponude za projekat.

Sledeća tabela navodi polja informacija rezimea o ponudi za projekt koja su jedinstvena za Dynamics 365 Project Operations ili imaju neke važne promene u ponašanju iz Dynamics 365 Sales ponuda.

| **Polje** | **Lokacija** | **Relevantnost, svrha i smernice** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip | Kartica sa rezimeom (skrivena) | Ovo polje skupa opcija ima sledeće opcije:</br>- Zasnovano na poslu (dostupno samo kada je instalirana usluga Project Operations)</br>- Zasnovano na stavci (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- Zasnovano na servisnom održavanju (dostupno kada je instalirana usluga Dynamics 365 Field Service) | Kada koristite aplikaciju Project Operations, vrednost ovog polja se automatski postavlja na opciju **Zasnovano na poslu**. To klasifikuje ponudu kao ponudu zasnovanu na projektu. Ponuda treba da se zasniva na projektu kako bi se omogućila sva proširenja i funkcije specifične za projekat. |
| Preduzeće-vlasnik | Rezime | Pravno lice koje će obračunati troškove i prihode ostvarene u ovom projektu ili u projektima povezanim sa ovom ponudom. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Preduzeće-vlasnik se izjednačava sa konceptom pravnog lica u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. Svi troškovi i prihodi ostvareni od ovog projekta biće evidentirani u glavnoj knjizi preduzeća-vlasnika. |
| Potencijalni klijent | Kartica rezimea | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Važeći klijent koji se poziva na ponudu za projekat mora biti podešen kao klijent u preduzeću koje je vlasnik ponude. Preduzeće-vlasnik prikazuje listu pravnih lica i ona se podešavaju u modulu **Upravljanje projektima i računovodstvo** usluge Project Operations. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Valuta u ponudi za projekat se podrazumevano zasniva na valuti klijenta. Međutim, to može da se promeni pre nego što se ponuda sačuva. |
| Menadžer za poslovne kontakte | Kartica rezimea | Ime menadžera poslovnog kontakta za ovu pogodbu. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Menadžer poslovnog kontakta je odgovoran za upravljanje odnosom sa klijentom kroz završetak ovog projekta. Na osnovu zapisa resursa koji može da se rezerviše povezanog sa menadžerom poslovnog kontakta, ugovorna jedinica se podrazumeva iz ponude za projekat.|
| Jedinica ugovaranja | Kartica rezimea | Organizaciona jedinica koja je odgovorna za isporuku projekta ili projekata povezanih sa ovom ponudom. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Jedinica ugovaranja je odeljenje preduzeća koje će izvršavati projekte nakon zaključenja pogodbe. Svaka jedinica ugovaranja ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom izvršavanja projekta. |
| Cenovnik proizvoda | Kartica rezimea | Ovo je cenovnik koji se koristi za određivanje podrazumevanih cena u stavkama ponuda zasnovanim na proizvodima. Lista opcija za ovo polje prikazuje listu cenovnika gde se valuta cenovnika podudara sa valutom u ponudi. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. Ovo polje u mogućnosti za poslovanje se podrazumeva iz zapisa poslovnog kontakta, ali se može promeniti. | Kada se ponuda ostvari, vrednost polje se kopira u ugovor o projektu koji se kreira. |
| Valuta | Kartica rezimea | To ukazuje na valutu koja će se koristiti za izveštavanje o vrednosti ove pogodbe. To je takođe valuta u kojoj će se klijentu fakturisati ako se ostvari pogodba. Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. Ovo polje u mogućnosti za poslovanje se podrazumeva iz zapisa poslovnog kontakta, ali korisnik je može promeniti.  | Kada se ponuda sačuva, ovo polje više nije moguće uređivati. Ovo se koristi da se odrede podrazumevani cenovnici proizvoda i projekta u ponudi. Valuta u ponudi se koristi za podudaranje valute sa cenovnikom. |
| Ograničenje koje ne sme da se prekorači | Kartica rezimea | Ovo ukazuje na dogovoreno gornje ograničenje konačne vrednosti sa kojim se klijent slaže za ovaj posao. | Ovo gornje ograničenje se procenjuje tokom izvršenja i primenljivo je na sve stavke i projekte povezane sa ovom pogodbom. |
| Zahtevani datum isporuke | Kartica rezimea | Kada se kreira ponuda iz mogućnosti za poslovanje, ovo polje se kopira iz odgovarajućeg polja u mogućnosti za poslovanje. | Ovaj datum se koristi kao datum završetka za generisanje rasporeda za fakturisanje. |

U nastavku su kartice i KPI-ovi dostupni na ponudi za projekt koji su jedinstveni za Project Operations ili imaju neke važne promene u ponašanju iz ponuda za prodaju:

| **Polje** | **Lokacija** | **Relevantnost, svrha i smernice** |
| --- | --- | --- |
| Analiza isplativosti | Kartica u ponudi | Kartica prikazuje sledeće metrike:</br>- Ukupni naplativi troškovi</br></br>- Ukupni nenaplativi troškovi</br>- Ukupan prihod</br>- Ukupni prihod (osnovni)</br>- Bruto marža</br>- Prilagođena bruto marža|
| Poređenje sa očekivanjima klijenta | Kartica u ponudi | Ova kartica prikazuje sledeće metrike:</br>- Procenjeni završetak</br>- Zahtevani završetak</br>- Budžet klijenta</br>- Vrednost ponude |
| Analiza ponude | Kartica u ponudi | Ova kartica rezimira sledeće najvažnije KPI-ove za ponudu za projekat</br>- Poređenje sa očekivanjima klijenata za budžet i raspored</br>- Bruto marža</br>- Prilagođena bruto marža |
