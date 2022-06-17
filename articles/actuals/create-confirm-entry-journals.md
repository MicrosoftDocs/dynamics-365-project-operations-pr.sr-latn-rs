---
title: Kreiranje i potvrda stavki knjiženja u glavnoj knjizi
description: Ovaj članak pruža informacije o kreiranju i potvrđiju dnevnika unosa u korporaciji Microsoft Dynamics 365 Project Operations.
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

Naloge unosa koristite za zapisivanje stvarnih podataka direktno u korporaciji Microsoft Dynamics 365 Project Operations. Kada koristite naloge stavki, ne morate da unosite evidencije korišćenja vremena, troškova i materijala u operacije projekta.

Jedan nalog unosa vam omogućava da kreirate više redova naloga. Kada je nalog potvrđen, red naloga unosa zapisuje stvarne za sledeće detalje:

- Trošak ili prihod, u zavisnosti od izabrane vrste transakcije.
- Izabrana klasa transakcije. Raspoložive klase su Vreme **, Trošak** **, Materijal** **, Retainer** **, Prekretnica** **i** Porez **.**
- Projekat i/ili zadatak koji je izabran u redu naloga.

Sledite ove korake da biste kreirali nalog unosa u operacijama projekta.

1. Idite na **naloge** \> **transakcija** \> **prodaje.**
2. Na stranici **Lista naloga unosa**, u oknu za radnje izaberite stavku Novo **da** biste kreirali nalog.
3. Na stranici **"** Novi nalog", u **polje** Opis unesite opis naloga.
4. Uverite se da je polje **"Vrsta naloga**" podešeno na "Stavka **", a** zatim izaberite stavku **Sačuvaj**. Nakon što se novi nalog unosa sačuva, na stranici **naloga** bi trebalo da se pojavi kartica "Redovi naloga".
5. Na kartici **Redovi naloga**, na traci sa alatkama iznad koordinatne mreže izaberite stavku Novo **da** biste kreirali red naloga unosa.
6. U dijalogu **Brzo** kreiranje za kreiranje reda naloga unosa postavite polja kao što je opisano u sledećoj tabeli.

    | Polje | Opis | Funkcionalni uticaj |
    | --- | --- | --- |
    | Klasa transakcije | Red naloga se može klasifikovati u jednu od šest klasa transakcija: **"Vreme**", **"Troškovi**", **"Materijal**", **"Zadruga",** "Prekretnica **"** ili "Porez **"**. | Klasa poreskih **transakcija** je zastarela u projektnim operacijama. <br> Ako kreirate klasu **transakcija** sa PDV-om, ona neće biti obrađena fakturisanjem ili obračunom troškova ili prihoda. **Prekretnica** je klasa transakcija samo za prihode. <br>Klasa **transakcije "Retainer** " predstavlja avans koji je primljen od kupca. Uvek ga treba kreirati kao par fakturisanih redova prodaje i neoslobiđenog naloga prodaje. |
    | Tip transakcije | Vrste **transakcija** **troška, interorga** i **resourcing troška po** jedinici treba da se koriste za zapisivanje troška.<br> Vrste **transakcija "Neželjena** prodaja" **i "Fakturisana** prodaja" treba da se koriste za zapisivanje prihoda. | Klasa **transakcije "Retainer** " funkcioniše samo sa vrstama transakcija **"Neželjena prodaja** " i **"Fakturisana** prodaja".<br> Klasa transakcije **Milestone** funkcioniše samo sa vrstom transakcije **"Fakturisana** prodaja". <br>Vrste **transakcija troškova po jedinici "Interorg Prodaja** **" i "Resourcing**" primenjuju se samo na klasu transakcija "Vreme **" i one** su samo avijatične u nalozima stavki u lite scneario, a ne prilikom primene operacija projekta u scenarijima resursa / neobavezujućih. |
    | Izaberite proizvod | Kada je **izabrana** klasa transakcije materijala, ovo polje vam omogućava da navedete da li je transakcija materijala za koju kreirate red naloga postojeći proizvod ili proizvod za upis. | Ako izaberete **opciju "Upisi** proizvod", možete uneti ime proizvoda. |
    | Proizvod | Referenca na proizvod iz kataloga. | |
    | Opis | Opis reda naloga koji olakšava identifikaciju. | Za redove naloga neželjene prodaje, vrednost će biti korišćena kao opis kada se kreiraju detalji reda fakture. |
    | Spoljni opis | Opis reda naloga koji se može koristiti za deljenje sa spoljnim zainteresovanim stranama. | Za redove naloga neželjene prodaje, vrednost će biti korišćena kao eksterni opis kada se kreiraju detalji reda fakture. Takođe se može pojaviti u fakturi koja se šalje kupcu. |
    | Tip naplate | Vrednost koja označava da li će red naloga biti ubrajan kao komponenta koja se naplaćuje, može da se naplati ili ne naplaćuje na projektu. | U tipičnom toku, vrsta naplate je izvedena iz dogovorenih uslova koji su podešeni na ugovor. Međutim, kada zakažete red naloga, u ovo polje možete uneti vrednost. |
    | Datum dokumenta | Koristite datum kada je došlo do transakcije. | |
    | Datum početka | Koristite datum kada je došlo do transakcije. | Ovo polje se koristi za poređenje sa datumom kreiranja fakture za transakcije vrste **"Neželjena prodaja** ". Ovo poređenje će vam pomoći da odlučite da li je transakcija datirana u budućnosti ili u prošlosti. Fakturi će biti dodate samo transakcije koje su datirane iz prošlosti. |
    | Datum završetka | Koristite datum kada je došlo do transakcije. | |
    | Datum knjiženja | Koristite datum kada će biti zapisan računovodstveni uticaj. | |
    | Kupac reda ugovora | Podrazumevano, ako red ugovora ima samo jednog kupca, ovo polje je podešeno na kupca u redu ugovora kada je red naloga sačuvan. Ako red ugovora ima više kupaca, izaberite tačnog kupca u redu ugovora. | Ako sistem ne može da odredi kupca reda ugovora u redu naloga i ako je prazan na stvarnoj **vrsti "Neželjena** prodaja" koja je kreirana iz reda naloga, stvarni neće biti fakturisan. |
    | Project | Izaberite projekat na koji ćete zapisati stvarni. | Na osnovu izabranog projekta, klase transakcija i zadatka, sistem će pokušati da odredi kupca ugovora, ugovora i reda ugovora. |
    | Zadatak | Izaberite zadatak na koji ćete zapisati stvarni zadatak. | Ako ste povezali zadatke sa redovima ugovora tokom podešavanja ugovora, sistem će koristiti izabrani zadatak, zajedno sa projektnom i klasom transakcija, za određivanje ugovora, reda ugovora i kupca reda ugovora. |
    | Kategorija transakcije | Izaberite kategoriju transakcije da biste zapisali stvarnu. | Za troškove, izabrana kategorija transakcije određuje podrazumevanu cenu koja će biti uneta u red naloga kada se sačuva. |
    | Uloga | Ovo polje je relevantno za redove naloga vremena. Izaberite ulogu resursa koji je proveo vreme na projektu i/ili zadatku. | Za redove naloga vremena, ako koristite konfiguraciju pravo iz kutije za unos podrazumevanih troškova resursa i stope računa, izabrana uloga se koristi zajedno sa jedinicom za resourcing da bi se odredila podrazumevana cena koja će biti uneta u red naloga kada se sačuva. Ako koristite prilagođenu konfiguraciju za unos podrazumevanih cena, trebalo bi da pregledate tu konfiguraciju da biste utvrdili da **li se polje "** Uloga" koristi za unos podrazumevanih vrednosti cena. |
    | Podugovor | Ako red naloga predstavlja kapacitet podizvođaca ili troškove podizvođaca ili materijala, izaberite odgovarajući podizvođaи. | Kada se zapuše redovi naloga troška, izabrani podizvođač će odrediti cenovnik koji se koristi za unos podrazumevanog troška po jedinici. |
    | Red podizvođači | Ako red naloga predstavlja kapacitet podizvođaca ili troškove podizvođači ili materijale, izaberite odgovarajući red podizvođaca. | Kada se zapuše redovi naloga troška, izabrani red podizvođač će se postarati da se raspoloživi obračuni kapaciteta u redu podizvođač ispravno izračunaju. |
    | Način izračunavanja iznosa | Ovo polje je podrazumevano podešeno na "Pomnoži **količinu po ceni"**. Kada se ovaj metod koristi, iznos će biti izračunat kao × *cena* *.* Drugi podržani metod je Fiksna **cena**. Kada se ovaj metod koristi, cena će biti podešena na iznos, a količina neće biti korišćena u obračunu. | |
    | Raspored i jedinica jedinice | Zajedno, plan jedinice i jedinica identifikuju jedinicu količine. | Kombinacija jedinice i kategorije transakcije se koristi za unos podrazumevanih cena za troškove. U podrazumevanoj konfiguraciji operacija projekta, kombinacija jedinice, uloge i jedinice za resourcing se koristi za unos podrazumevanih cena za vreme. Ako imate prilagođenu konfiguraciju za unos podrazumevanih cena, ona će se koristiti zajedno sa jedinicom. Kombinacija proizvoda i jedinice se koristi za unos podrazumevanih cena materijala. |
    | Količina | Unesite količinu. | |
    | Cena | Ako cena ostane prazna kada se kreira red naloga, relevantne vrednosti će biti korišćene za unos podrazumevanih cena, u zavisnosti od klase transakcije. Ako je cena uneta prilikom kreiranja reda naloga, ta cena će biti iskorišćena. | |
    | Porez | Unesite bilo koji iznos poreza. | U zavisnosti od iznosa poreza koji je unet, produženi iznos će biti izračunat kao Porez *na* + *iznos*. |

## <a name="confirm-an-entry-journal"></a>Potvrda naloga unosa

Nakon što ste uneli sve redove naloga u nalog unosa, možete potvrditi nalog. Ovaj proces će zapisati svaki red naloga kao stvarne u odgovarajućim projektima.

Nakon potvrde naloga, više ne možete da ga uređujete niti bilo koji od njegovih redova.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Stvarne stavke kreirane potvrdom dnevnika unosa

Postoji nekoliko ključnih razlika između stvarnih stavki koje su kreirane potvrdom naloga unosa i stvarnih vrednosti koje se kreiraju tokom odobravanja evidencija korišćenja vremena, troškova i materijala i potvrde fakture u operacijama projekta:

- Nalozi stavki ne koriste veze sa transakcijama da bi povezali stvarni trošak sa stvarnim neželjenim prodajom. Stvarne stavke koje se kreiraju kada se odobravaju evidencije korišćenja vremena, troškova i materijala uvek koriste veze transakcija za povezivanje stvarnih troškova i neželjene prodaje.
- Nalozi stavki ne koriste poreklo transakcija da bi povezali stvarne troškove i neželjene rezultate prodaje sa bilo kojim zapisom koji potiče. Stvarne stavke koje se kreiraju kada se odobravaju evidencije korišćenja vremena, troškova i materijala uvek koriste poreklo transakcije da bi povezale stvarne troškove i neželjenu prodaju sa stavkom vremena koja potiče.
- Kada se fakturiše neželjena potvrda o prodaji koja je kreirana potvrdom naloga stavki, fakturisane stvarne prodaje koje su kreirane tokom potvrde fakture povezane su sa neželjenim stvarnim prodajama, na sličan način kao i neželjene stvarne prodaje koje se kreiraju kada se odobre evidencije korišćenja vremena, troškova i materijala.
- Redovi naloga stavki koji su kreirani za vreme koje unose međuosovladini **resursi ne prouzrokuje automatsko kreiravanje stvarnih podataka o trošku po jedinici "Resourcing** **" i "Interorg Sales**". Ove stvarne stvari moraju biti ručno kreirane. Ovo ponašanje se razlikuje od ponašanja stavki vremena koje zapisuje međuosovladini resursi. U tom slučaju, kada je vreme odobreno, aplikacija automatski kreira stvarne stavke **vrste "Trošak**" na projektu i stvarne **vrste troškova po jedinici "Resourcing** **" i "Interorg Sales**" u odeljenju u vlasništvu zaposlenog. Zatim koristi veze transakcija za povezivanje tih stvarnih podataka i porekla transakcija da bi ih povezala sa stavkom vremena koja potiče.
- Kada su nalozi stavki potvrđeni, oni kreiraju stvarne vrednosti. Međutim, korektivni nalozi se ne mogu koristiti za ispravljanje tih stvarnih podataka. Ovo ponašanje se razlikuje od ponašanja stvarnih stvari koje se kreiraju kada se odobre evidencije korišćenja vremena, troškova i materijala. U tom slučaju, aplikacija vam omogućava da koristite korektivne naloge da biste ispravili stvarne stvari da biste otklonili greške, pod uslovom da te stvarne stvari još uvek nisu fakturisane. Ako su već fakturisane, i dalje možete ispraviti stvarni ako kupcu obradite pun kredit od tog stvarnog.

> [!NOTE]
> Nalozi unosa ne sprovode stroga pravila podrazumevanih vrednosti. Zbog toga koristite ove dnevnike unosa što je manje moguće i budite oprezni i vodite računa da ne kreirate oštećene finansijske podatke u sistemu. Kad god možete, koristite evidencije korišćenja vremena, troškova i materijala, podešavanje prekretnice i prodavca ugovora o projektu i proces potvrde fakture projekta umesto naloga stavki da biste kreirali stvarne stavke.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
