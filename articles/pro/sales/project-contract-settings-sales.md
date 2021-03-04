---
title: Podešavanja ugovora za projekat – jednostavno
description: Ova tema pruža informacije o poljima koja utiču na predmet ugovora i informacije o ugovoru koje su sažete u svim stavkama.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 28dfb256eb75ca9484161f053969c205fcd60965
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180938"
---
# <a name="project-contract-settings---lite"></a>Podešavanja ugovora za projekat – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema pruža informacije o poljima koja se primenjuju na celokupan ugovor o projektu, uključujući podešavanja koja utiču na sve predmete ugovora. Takođe su uključene informacije o ugovoru koje su sažete u svim stavkama za pokretanje KPI-jeva projektnog ugovora.

Sledeća tabela navodi polja u projektnom ugovoru koja su jedinstvena za Dynamics 365 Project Operations ili imaju neke važne promene u ponašanju iz ulaznih porudžbina u usluzi Dynamics 365 Sales.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Tip | Kartica **Rezime** (skrivena) | Ovo je polje skupa opcija sa sledećim opcijama:</br>- **Zasnovano na poslu** (Dostupno samo kada je instalirana usluga Project Operations)</br>- **Zasnovano na stavci** (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- **Zasnovano na servisnom održavanju** (Dostupno kada je instalirana usluga Dynamics 365 Field Service) | U usluzi Project Operations vrednost ovog polja podrazumevano je **Zasnovano na poslu**, a ugovor klasifikuje kao ugovor zasnovan na projektu. Ugovor treba da se zasniva na projektu kako bi se omogućila sva proširenja i funkcije specifične za projekat. |
| Potencijalni klijent | Kartica **Rezime** | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. Kada se kreira ugovor iz ponude, ovo polje se kopira iz odgovarajućeg polja u zapisu ponude. | Valuta u ponudi za projektni ugovor se podrazumevano zasniva na valuti klijenta. To može da se promeni pre nego što se ugovor sačuva. |
| Menadžer za poslovne kontakte | Kartica **Rezime** | Ime menadžera poslovnog kontakta za ovu pogodbu. Kada se kreira ugovor iz ponude, ovo polje se kopira iz odgovarajućeg polja u zapisu ponude. | Menadžer poslovnog kontakta je odgovoran za upravljanje odnosom sa klijentom kroz završetak ovog projekta. Na osnovu zapisa resursa koji može da se rezerviše povezanog sa menadžerom poslovnog kontakta, ugovorna jedinica se podrazumeva iz projektnog ugovora. |
| Jedinica ugovaranja | Kartica **Rezime** | Organizaciona jedinica koja je odgovorna za isporuku projekata povezanih sa ovim ugovorom. Kada se kreira ugovor iz ponude, ovo polje se kopira iz odgovarajućeg polja u zapisu ponude. | Jedinica ugovaranja je odeljenje preduzeća koje izvršava projekte nakon zaključenja pogodbe. Svaka ugovorna jedinica ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |
| Cenovnik proizvoda | Kartica **Rezime** | Ovaj cenovnik se koristi za određivanje podrazumevanih cena u predmetima ugovora zasnovanim na proizvodima. Lista padajućih opcija za ovo polje prikazuje listu cenovnika gde se valuta cenovnika podudara sa valutom u ugovoru. Kada se kreira ugovor iz ponude, ovo polje se kopira iz odgovarajućeg polja u zapisu ponude. U projektnom ugovoru, ovo polje se podrazumeva iz zapisa poslovnog kontakta, ali se može promeniti. | Za ovo polje ne postoji posledična relevantnost. |
| Valuta | Kartica **Rezime** | Valuta koja se koristi za izveštavanje o vrednosti ovog posla i valuta u kojoj će se fakturisati kupac. Kada se kreira ugovor iz ponude, ovo polje se kopira iz odgovarajućeg polja u zapisu ponude. U projektnom ugovoru, ovo polje se podrazumeva iz zapisa poslovnog kontakta, ali se može promeniti. | Kada se ugovor sačuva, ovo polje više nije moguće uređivati. Ovo polje se koristi da se odrede podrazumevani cenovnici proizvoda i projekta u ugovoru. Valuta u ugovoru se koristi za podudaranje valute sa cenovnikom. |
| Ograničenje koje ne sme da se prekorači | Kartica **Rezime** | Ovo polje ukazuje na dogovoreno gornje ograničenje konačne vrednosti sa kojim se klijent slaže za ovaj posao. | Gornje ograničenje se procenjuje tokom izvršenja i primenljivo je na sve stavke i projekte povezane sa ovom pogodbom. |
| Zahtevani datum isporuke | Kartica **Rezime** | Kada se kreira ugovor iz ponude projekta, ovo polje se kopira iz odgovarajućeg polja u ponudi projekta. | Ovaj datum se koristi kao datum završetka za generisanje rasporeda za fakturisanje. |

Sledeći KPI-jevi su dostupni na kartici **Izvršenje ugovora** projektnog ugovora.

| Polje | Lokacija | Opis |
| --- | --- | --- |
| Vrednost ugovora | Ukupan ugovor | Ukupna vrednost projektnog ugovora. |
| Naplaćeni iznos | Ukupan ugovor | Zbir iznosa na svim fakturama po ovom ugovoru. |
| Nastali troškovi | Ukupan ugovor | Zbir svih stvarnih troškova evidentiranih na svim projektima koji su mapirani sa ugovorom. |
| Bruto marža | Ukupan ugovor | Naplaćeni iznos – Troškovi nastali do datuma/Naplaćeni iznos |
| Očekivana marža | Ukupan ugovor | (Vrednost ugovora – Procenjeni troškovi) / Vrednost ugovora Procenjeni troškovi = Zbir svih procenjenih troškova na svim projektima mapiranim sa ugovorom.|
| Vrednost ugovora | Stavke zasnovane na projektu | Vrednost predmeta ugovora. |
| Naplaćeni iznos | Stavke zasnovane na projektu | Za predmet ugovora sa fiksnom cenom: Zbir iznosa svih fakturisanih stvarnih tačaka prodaje u odnosu na ovaj predmet ugovora na različitim fakturama kreiranim za ovaj ugovor. Za predmet ugovora sa vremenom i materijalom: Zbir iznosa svih stvarnih naplativih iznosa naplaćene prodaje u odnosu na ovaj predmet ugovora na različitim fakturama kreiranim za ovaj ugovor. |
| Nastali troškovi | Stavke zasnovane na projektu | Zbir svih stvarnih troškova evidentiranih na svim projektima koji su mapirani sa predmetom ugovora. |
| Bruto marža | Stavke zasnovane na projektu | (Naplaćeni iznos – Troškovi nastali do datuma) / Naplaćeni iznos |
| Očekivana marža | Stavke zasnovane na projektu | (Iznos predmeta ugovora u osnovnoj valuti – Procenjeni troškovi predmeta ugovora u osnovnoj valuti) / Iznos predmeta ugovora u osnovnoj valuti |
| Nastali troškovi | Detalji predmeta zasnovanog na projektu | Vreme: Zbir iznosa stvarnih troškova evidentiranih za ovu ulogu na projektu mapiranom sa predmetom ugovora. Troškovi: Zbir iznosa svih stvarnih troškova evidentiranih za ovu kategoriju na projektu mapiranom sa predmetom ugovora. |
| Evidentirana količina | Detalji predmeta zasnovanog na projektu | Vreme: Količina stvarnih cena utrošenog vremena za ulogu na projektu koji je mapiran sa ovim predmetom ugovora. Troškovi: Sve količine za ovu kategoriju troškova na trenutnom stanju iznosa troškova na projektu mapirane su sa ovim predmetom ugovora. |
| Naplaćeni iznos | Detalji predmeta zasnovanog na projektu | Za predmet ugovora sa fiksnom cenom, ovo polje ostaje prazno na nivou detalja i prikazuje se samo na nivou predmeta ugovora. Za predmet ugovora sa vremenom i materijalom, proračuni se dovršavaju na nivou detalja. Detalji prikazuju sumu iznosa na svim naplaćenim linijama prihoda u odnosu na ovaj predmet ugovora koje se naplaćuju. |
| Naplaćena količina | Detalji predmeta zasnovanog na projektu | Za predmet ugovora sa fiksnom cenom, ovo polje ostaje prazno na nivou detalja i prikazuje se samo na nivou predmeta ugovora. Za predmet ugovora sa vremenom i materijalom, proračuni se dovršavaju na nivou detalja za vreme i troškove. Vreme: Zbir sati na svim naplaćenim linijama prihoda za ovu ulogu u odnosu na ovaj predmet ugovora koje se naplaćuju. Troškovi: Sve količine za ovu kategoriju troškova na trenutnom stanju iznosa troškova na projektu mapirane su sa ovim predmetom ugovora. |
| Vrednost ugovora | Stavke zasnovane na proizvodu | Vrednost predmeta ugovora za ovaj predmet ugovora zasnovana na proizvodu. |
| Naplaćeni iznos | Stavke zasnovane na proizvodu | Zbir iznosa na svim linijama faktura u odnosu na ovaj predmet ugovora zasnovan na proizvodu na različitim fakturama kreiranim za ovaj ugovor. |
| Nastali troškovi | Stavke zasnovane na proizvodu | Zbir svih stvarnih troškova evidentiranih za predmet ugovora zasnovan na projektu. |
| Bruto marža | Stavke zasnovane na projektu | Naplaćeni iznos – Troškovi nastali do datuma/Naplaćeni iznos |
| Očekivana marža | Stavke zasnovane na proizvodu | (Vrednost predmeta ugovora - Procenjeni troškovi za predmet ugovora) / Vrednost predmeta ugovora |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]