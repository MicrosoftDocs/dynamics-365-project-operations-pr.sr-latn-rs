---
title: Kreiranje i potvrda stavki knjiženja u glavnoj knjizi
description: Ovaj članak pruža informacije o tome kako da kreirate i potvrdite dnevnike unosa u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912349"
---
# <a name="create-and-confirm-entry-journals"></a>Kreiranje i potvrda stavki knjiženja u glavnoj knjizi

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dnevnike unose koristite za evidentiranje stvarnih vrednosti direktno u usluzi Microsoft Dynamics 365 Project Operations. Kada koristite dnevnike unosa, ne morate da unosite evidencije vremena, troškova i korišćenja materijala u usluzi Project Operations.

Jedan dnevnik unosa omogućava vam da kreirate više stavki knjiženja u glavnoj knjizi. Kada je glavna knjiga potvrđena, stavke u dnevniku unosa evidentiraju stvarne vrednosti za sledeće detalje:

- Cena ili prihod, u zavisnosti od izabrane vrste transakcije.
- Izabrana klasa transakcije. Dostupne klase su **Vreme**, **Trošak**, **Materijal**, **Avans**, **Kontrolna tačka** i **Porez**.
- Projekat i/ili zadatak koji je izabran u stavci u glavnoj knjizi.

Pratite ove korake da biste kreirali dnevnik unosa u usluzi Project Operations.

1. Idite na **Prodaja** \> **Transakcije** \> **Glavne knjige**.
2. Na stranici liste **Dnevnici unosa**, u oknu Radnja, izaberite **Novo** da biste kreirali glavnu knjigu.
3. Na stranici **Nova glavna knjiga**, u polju **Opis**, unesite opis za glavnu knjigu.
4. Uverite se da je polje **Tip glavne knjige** podešeno na **Ulazni**, a zatim izaberite **Sačuvaj**. Nakon što se novi dnevnik unosa sačuva, na stranici glavne knjige, trebalo bi da se pojavi kartica **Stavke u glavnoj knjizi**.
5. Na kartici **Stavke u glavnoj knjizi**, na traci sa alatkama iznad matrice koordinatne mreže izaberite stavku **Novo** da biste kreirali stavku u glavnoj knjizi unosa.
6. U dijalogu **Brzo kreiranje** za kreiranje reda stavke u glavnoj knjizi unosa, postavite polja kao što je opisano u sledećoj tabeli.

    | Polje | Opis | Funkcionalni uticaj |
    | --- | --- | --- |
    | Klasa transakcije | Stavka u glavnoj knjizi se može klasifikovati u jednu od šest klasa transakcija: **Vreme**, **Trošak**, **Materijal**, **Avans**, **Kontrolna tačka** ili **Porez**. | Klasa transakcija **Porez** je zastarela u usluzi Project Operations. <br> Ako kreirate klasu transakcije **Porez**, ona neće biti obrađena fakturisanjem ili u izračunavanjima cene ili prihoda. **Kontrolna tačka** je klasa transakcija koja predstavlja samo prihod. <br>Klasa transakcije **Avans** predstavlja avans koji je primljen od klijenta. Uvek ga treba kreirati kao par fakturisanih prodajnih i nefakturisanih prodajnih stavki u glavnoj knjizi. |
    | Tip transakcije | Vrste transakcija **Cena**, **Prodaja između organizacija** i **Troškovi jedinice za obezbeđivanje resursa** bi trebalo da se koriste za evidentiranje cene.<br> Vrste transakcija **Nenaplaćena prodaja** i **Naplaćena prodaja** bi trebalo da se koriste za evidentiranje prihoda. | Klasa transakcija **Avans** funkcioniše samo sa vrstama transakcija **Nenaplaćena prodaja** i **Naplaćena prodaja**.<br> Klasa transakcije **Kontrolna tačka** funkcioniše samo sa vrstom transakcije **Naplaćena prodaja**. <br>Vrste transakcija **Prodaja između organizacija** i **Troškovi jedinice za obezbeđivanje resursa** primenjive su samo na klasu transakcija **Vreme** i dostupne su samo u dnevnicima unosa u scenariju jednostavne primene, ali ne i prilikom primene usluge Project Operations u scenarijima Resursa/Bez zaliha. |
    | Izaberite proizvod | Kada je izabrana klasa transakcija **Materijal**, ovo polje vam omogućava da navedete da li je transakcija materijala za koju kreirate stavku u glavnoj knjizi za postojeći proizvod ili za ručno dodat proizvod. | Ako izaberete **Ručno dodat proizvod**, možete da unesete naziv proizvoda. |
    | Proizvod | Referenca na proizvod iz kataloga. | |
    | Opis | Opis stavke u glavnoj knjizi koji olakšava identifikaciju. | Za stavke nenaplaćene prodaje u prodajnoj knjizi, vrednost će biti korišćena kao opis kada se kreiraju detalji stavke fakture. |
    | Spoljni opis | Opis stavke u glavnoj knjizi koji se može koristiti za deljenje sa spoljnim zainteresovanim stranama. | Za stavke nenaplaćene prodaje u prodajnoj knjizi, vrednost će biti korišćena kao spoljni opis kada se kreiraju detalji stavke fakture. Takođe se može pojaviti na fakturi koja se šalje klijentu. |
    | Tip naplate | Vrednost koja označava da li će stavka u glavnoj knjizi biti ubrajana kao komponenta koja se naplaćuje, koja može da se naplati ili koja se ne naplaćuje na projektu. | U tipičnom toku, vrsta naplate se izvodi iz dogovorenih uslova koji su podešeni u ugovoru. Međutim, kada evidentirate stavku u glavnoj knjizi, u ovo polje možete uneti vrednost. |
    | Datum dokumenta | Koristite datum kada je došlo do transakcije. | |
    | Datum početka | Koristite datum kada je došlo do transakcije. | Ovo polje se koristi za poređenje sa datumom kreiranja fakture za transakcije vrste **Nenaplaćena prodaja**. Ovo poređenje će vam pomoći da odlučite da li je transakcija datirana u budućnosti ili u prošlosti. Fakturi će biti dodate samo transakcije koje su datirane u prošlosti. |
    | Datum završetka | Koristite datum kada je došlo do transakcije. | |
    | Datum knjiženja | Koristite datum kada će biti evidentiran računovodstveni uticaj. | |
    | Klijent predmeta ugovora | Podrazumevano, ako predmet ugovora ima samo jednog klijenta, ovo polje je podešeno na klijenta u predmetu ugovora kada se stavka u glavnoj knjizi čuva. Ako predmet ugovora ima više klijenata, izaberite ispravnog klijenta u predmetu ugovora. | Ako sistem ne može da odredi klijenta u predmetu ugovora u stavci u glavnoj knjizi i ako je prazan na stvarnoj vrednosti tipa **Nenaplaćena prodaja** koja je kreirana iz stavke u glavnoj knjizi, stvarna vrednost neće biti fakturisana. |
    | Project | Izaberite projekat u koji ćete evidentirati stvarnu vrednost. | Na osnovu izabranog projekta, klase transakcija i zadatka, sistem će pokušati da odredi ugovor, predmet ugovora i klijenta predmeta ugovora. |
    | Zadatak | Izaberite zadatak u koji ćete evidentirati stvarnu vrednost. | Ako ste povezali zadatke sa predmetima ugovora tokom konfigurisanja ugovora, sistem će koristiti izabrani zadatak, zajedno sa projektom i klasom transakcija, da bi utvrdio ugovor, predmet ugovora i klijenta predmeta ugovora. |
    | Kategorija transakcije | Izaberite kategoriju transakcije u koju ćete evidentirati stvarnu vrednost. | Za troškove, izabrana kategorija transakcije određuje podrazumevanu cenu koja će biti uneta u stavku u glavnoj knjizi kada se sačuva. |
    | Uloga | Ovo polje je relevantno za stavke u glavnoj knjizi vremena. Izaberite ulogu resursa koji je proveo vreme na projektu i/ili zadatku. | Za stavke u glavnoj knjizi vremena, ako koristite gotovu konfiguraciju za unos podrazumevane cene resursa i stope naplate, izabrana uloga se koristi zajedno sa jedinicom za resurse da bi se odredila podrazumevana cena koja će biti uneta u stavku u glavnoj knjizi kada se sačuva. Ako koristite prilagođenu konfiguraciju za unos podrazumevanih cena, trebalo bi da pregledate tu konfiguraciju da biste utvrdili da se polje **Uloga** koristi za unos podrazumevanih vrednosti cena. |
    | Podugovor | Ako stavka u glavnoj knjizi predstavlja kapacitet iz podugovora ili troškove ili materijale iz podugovora, izaberite odgovarajući podugovor. | Kada se evidentiraju stavke u glavnoj knjizi troškova, izabrani podugovor će odrediti cenovnik koji se koristi za unos podrazumevane jedinične cene. |
    | Predmet podugovora | Ako stavka u glavnoj knjizi predstavlja kapacitet podizvođača ili troškove ili materijale podizvođača, izaberite odgovarajući predmet podugovora. | Kada se evidentiraju stavke u glavnoj knjizi troškova, izabrani predmet podugovora će se pobrinuti da se dostupna izračunavanja kapaciteta na predmetu podugovora ispravno ispravno izračunaju. |
    | Način izračunavanja iznosa | Podrazumevano, ovo polje je podešeno na **Množenje količine cenom**. Kada se ovaj metod koristi, količina će biti izračunata kao *Količina* × *Cena*. Drugi podržani metod je **Fiksna cena**. Kada se ovaj metod koristi, cena će biti podešena na iznos, a količina neće biti korišćena u izračunavanju. | |
    | Raspored jedinice i jedinica | Zajedno, raspored jedinice i jedinica identifikuju jedinicu količine. | Kombinacija jedinice i kategorije transakcije koristi se za unos podrazumevanih cena za troškove. U podrazumevanoj konfiguraciji usluge Project Operations, kombinacija jedinice, uloge i jedinice za resurse koristi se za unos podrazumevanih cena za vreme. Ako imate prilagođenu konfiguraciju za unos podrazumevanih cena, ona će se koristiti zajedno sa jedinicom. Kombinacija proizvoda i jedinice koristi se za unos podrazumevanih cena za materijale. |
    | Količina | Unesite količinu. | |
    | Cena | Ako cena ostane prazna kada se kreira stavka u glavnoj knjizi, relevantne vrednosti će biti korišćene za unos podrazumevanih cena, u zavisnosti od klase transakcije. Ako je cena uneta prilikom kreiranja stavke u glavnoj knjizi, ta cena će biti iskorišćena. | |
    | Porez | Unesite bilo koji iznos poreza. | U zavisnosti od iznosa poreza koji je unet, prošireni iznos će biti izračunat kao *Iznos* + *Porez*. |

## <a name="confirm-an-entry-journal"></a>Potvrda dnevnika unosa

Nakon što ste uneli sve stavke u glavnoj knjizi u dnevnik unosa, možete potvrditi glavnu knjigu. Ovaj proces će evidentirati svaku stavku u glavnoj knjizi kao stvarne vrednosti u odgovarajućim projektima.

Nakon potvrde glavne knjige, više ne možete da uređujete nju niti bilo koji od njenih redova.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Stvarne vrednosti kreirane potvrdom dnevnika unosa

Postoji nekoliko ključnih razlika između stvarnih vrednosti koje su kreirane potvrdom dnevnika unosa i stvarnih vrednosti koje se kreiraju tokom odobravanja evidencija vremena, troškova i korišćenja materijala i potvrde fakture u usluzi Project Operations:

- Dnevnici unosa ne koriste veze sa transakcijama za povezivanje stvarne vrednosti cene sa stvarnom vrednošću nenaplaćene prodaje. Stvarne vrednosti koje se kreiraju kada se odobravaju evidencije vremena, troškova i korišćenja materijala uvek koriste veze sa transakcijama za povezivanje stvarnih vrednosti cene i nenaplaćene prodaje.
- Dnevnici unosa ne koriste porekla transakcija za povezivanje stvarne vrednosti cene i stvarne vrednosti nenaplaćene prodaje sa bilo kojim izvornim zapisom. Stvarne vrednosti koje se kreiraju kada se odobravaju evidencije vremena, troškova i korišćenja materijala uvek koriste porekla transakcija za povezivanje stvarnih vrednosti cene i nenaplaćene prodaje sa izvornom stavkom vremena.
- Kada se fakturišu stvarne vrednosti nenaplaćene prodaje koje su kreirane potvrdom ulazne glavne knjige, stvarne vrednosti naplaćene prodaje koje se kreiraju tokom potvrde fakture povezuju se sa stvarnim vrednostima nenaplaćene prodaje, slično onome kako se stvarne vrednosti nenaplaćene prodaje kreiraju kada se odobravaju evidencije vremena, troška i korišćenja materijala.
- Stavke u glavnoj knjizi unosa koje se kreiraju za vreme koje unesu resursi između organizacija ne dovode do toga da se stvarne vrednosti tipova **Troškovi jedinice za obezbeđivanje resursa** i **Prodaja između organizacija** automatski kreiraju. Ove stvarne vrednosti moraju ručno da se kreiraju. Ovo ponašanje se razlikuje od ponašanja unosa vremena koji se evidentiraju resursima između organizacija. U tom slučaju, kada se vreme odobri, aplikacija automatski kreira stvarne vrednosti tipa **Cena** na projektu i stvarne vrednosti tipova **Troškovi jedinice za obezbeđivanje troškova** i **Prodaja između organizacija** u odeljenju u vlasništvu zaposlenog. Zatim koristi veze sa transakcijama za povezivanje tih stvarnih vrednosti i porekla transakcija kako bi bili povezani sa izvornom stavkom vremena.
- Kada su dnevnici unosa potvrđeni, oni kreiraju stvarne vrednosti. Međutim, dnevnici sa ispravkama se ne mogu koristiti za ispravljanje tih stvarnih vrednosti. Ovo ponašanje se razlikuje od ponašanja stvarnih vrednosti koje se kreiraju kada se odobre evidencije vremena, troškova i korišćenja materijala. U tom slučaju, aplikacija vam omogućava da koristite dnevnike sa ispravkama da biste ispravili stvarne vrednosti i otklonili eventualne greške, pod uslovom da te stvarne vrednosti još uvek nisu fakturisane. Ako su već fakturisane, i dalje možete ispraviti stvarnu vrednost ako obradite pun kredit te stvarne vrednosti za klijenta.

> [!NOTE]
> Dnevnici unosa ne nameću stroga pravila podrazumevanih vrednosti. Zbog toga koristite ove dnevnike unosa što je manje moguće i budite oprezni i vodite računa da ne kreirate pogrešne finansijske podatke u sistemu. Kad god možete, koristite evidencije vremena, troškova i korišćenja materijala, podešavanje kontrolne tačke i avansa u ugovorima za projekat, a proces potvrde fakture projekta umesto dnevnika unosa da biste kreirali stvarne vrednosti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
