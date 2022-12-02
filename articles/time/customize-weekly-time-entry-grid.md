---
title: Proširenje stavki vremena
description: Ovaj članak pruža informacije o tome kako programeri mogu da prošire kontrolu stavki vremena.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914787"
---
# <a name="extending-time-entries"></a>Proširenje stavki vremena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations obuhvata proširivu prilagođenu kontrolu unosa vremena. Ova kontrola sadrži sledeće funkcije:

- Unesite vreme horizontalno tokom nedelje
- Ukupno po danu, redu ili nedelji
- Kopirajte redove ili nedelje
- Stavka vremena kroz HH:mm ili HH.hh (automatski se konvertuje u HH.hh)
- Uvoz iz dodela, rezervacija ili zakazanih obaveza

Produženje unosa vremena moguće je u dve oblasti:
- [Dodajte prilagođene stavke vremena za sopstvenu upotrebu](#add)
- [Prilagođavanje kontrole sedmične stavke vremena](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodajte prilagođene stavke vremena za sopstvenu upotrebu

Vremenski unosi su osnovni entitet koji se koristi u više scenarija. U 1. talasu iz aprila 2020. predstavljeno je osnovno rešenje TESA. TESA pruža entitet **Podešavanja** i novu bezbednosnu ulogu **Korisnik stavke vremena**. Nova polja, **msdyn_start** i **msdyn_end**, koja imaju direktnu vezu sa **msdyn_duration**, takođe su bila uključena. Novi entitet, bezbednosna uloga, i polja omogućavaju jedinstveniji pristup vremenu u više proizvoda.


### <a name="time-source-entity"></a>Izvorni entitet vremena
| Polje | Opis | 
|-------|------------|
| Imenuj  | Naziv stavke izvora vremena koji se koristi kao vrednost izbora tokom kreiranja stavki vremena. |
| Podrazumevani izvor vremena [Izvor vremena: isdefault] | Podrazumevano, samo jedan izvor vremena može biti označen kao podrazumevani. Ova opcija omogućava da se za stavke podrazumeva izvor vremena ako nijedno vreme nije navedeno. |
|Tip izvora vremena [Izvor vremena: sourcetype] | Tip izvora je opcija (Tip stavke izvora vremena) koja omogućava povezivanje izvora vremena sa aplikacijom. Microsoft zadržava vrednosti veće od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Stavke vremena i Izvorni entitet vremena
Svaka stavka vremena povezana je sa zapisom izvora vremena. Ovaj zapis određuje koje aplikacije treba da obrade stavku vremena i kako.

Stavke vremena su uvek jedan neprekidni vremenski blok sa povezanim početkom, krajem i trajanjem.

Logika će automatski ažurirati zapis stavke vremena u sledećim situacijama:

- Ako su navedena dva od tri sledeća polja, treće se izračunava automatski: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** prepoznaju vremensku zonu.
- Vremenski unosi napravljeni sa samo pomoću navedenih opcija **msdyn_date** i **msdyn_duration** počeće u ponoć. Polja **msdyn_start** i **msdyn_end** ažuriraju se u skladu sa time.

#### <a name="time-entry-types"></a>Tipovi stavki vremena

Zapisi stavki vremena imaju pridruženi tip koji definiše ponašanje u toku podnošenja pridružene aplikacije.

|Oznaka | Vrednost|
|-----|-----|
|Na pauzi   |192,355,000|
|Putovanje | 192,355,001|
|Prekovremeni rad   | 192,354,320|
|Rad   | 192,350,000|
|Odsustvo    | 192,350,001|
|Odmor   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Prilagođavanje kontrole sedmične stavke vremena
Programeri mogu dodati dodatna polja i pretraživanja drugim entitetima i primeniti prilagođena poslovna pravila kao podršku njihovim poslovnim scenarijima.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Dodavanje prilagođenih polja sa pronalaženjima u druge entitete
Tri su glavna koraka za dodavanje prilagođenog polja u mrežu sedmičnih stavki vremena.

1. Dodajte prilagođeno polje u dijalog **Brzo kreiranje**.
2. Konfigurišite mrežu da prikazuje prilagođeno polje.
3. Dodajte prilagođeno polje na stranicu **Uređivanje reda** ili **Uređivanje stavke vremena**, a prema potrebi.

Uverite se da novo polje ima potrebne potvrde na stranici **Uređivanje reda** ili **Uređivanje stavke vremena**. Kao deo ovog zadatka, zaključajte polje, na osnovu statusa stavke vremena.

Kada dodate prilagođeno polje u matricu koordinatne mreže **Stavka vremena**, a zatim kreirate stavke vremena direktno u matrici koordinatne mreže, prilagođeno polje za te stavke se automatski postavlja tako da se podudara sa redom. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijalog za brzo kreiranje
Dodajte prilagođeno polje u dijalog **Brzo kreiranje: Kreiranje stavke vremena**. Korisnici tada mogu da unesu vrednost kada dodaju stavke vremena izborom opcije **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurisanje mreže za prikaz prilagođenog polja
Prilagođeno polje možete da dodate na dva načina u matricu koordinatne mreže **Sedmične stavke vremena**.

- Prilagodite prikaz **Moje sedmične stavke vremena** i dodajte mu prilagođeno polje. Možete navesti položaj i veličinu prilagođenog polja u mreži uređivanjem svojstava u prikazu.
- Kreirajte nov prilagođeni prikaz stavke vremena i njegovo podešavanje kao podrazumevani prikaz. Ovaj prikaz treba da sadrži polja **Opis** i **Spoljni komentari**, pored kolona koje želite da matrica koordinatne mreže uvrsti. Možete navesti položaj, veličinu i podrazumevani redosled sortiranja u mreži uređivanjem tih svojstava u prikazu. Zatim konfigurišite prilagođenu kontrolu za ovaj prikaz tako da to bude kontrola **Mreža stavke vremena**. Dodajte kontrolu u prikaz i izaberite je za **Veb**, **Telefon** i **Tablet**. Zatim konfigurišite parametre za matricu koordinatne mreže **Sedmične stavke vremena**. Podesite polje **Datum početka** na **msdyn\_date**, podesite polje **Trajanje** na **msdyn\_duration**, a polje **Status** na **msdyn\_entrystatus**. Polje **Lista statusa samo za čitanje** postavljeno je na **192350002 (odobreno)**, **192350003 (prosleđeno)** ili **192350004 (zatražen je opoziv)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodavanje prilagođenog polja na odgovarajuću stranicu za uređivanje
Stranice koje se koriste za uređivanje stavke vremena ili reda stavki vremena mogu se pronaći u okviru stavke **Obrasci** . Dugme **Uredi stavku** u matrici koordinatne mreže otvara stranicu **Uređivanje stavke**, a dugme **Uredi red** otvara stranicu **Uređivanje reda**. Ove stranice možete da uređujete tako da sadrže prilagođena polja.

Obe opcije uklanjaju neko unapred definisano filtriranje za entitete **Projekat** i **Projektni zadatak**, tako da će svi prikazi pronalaženja entiteta biti vidljivi. Kao unapred definisani su vidljivi samo relevantni prikazi pronalaženja.

Morate odrediti odgovarajuću stranicu za prilagođeno polje. Najverovatnije, ako ste dodali polje u mrežu, ono bi trebalo da ide na stranicu **Uređenje reda** koja se koristi za polja koja se primenjuju na celi red sa stavkama vremena. Ako prilagođeno polje ima jedinstvenu vrednost u redu svakog dana (na primer, to je prilagođeno polje za vreme završetka), trebalo bi da ide na stranicu **Uređenje stavke vremena**.

Da biste dodali prilagođeno polje na stranicu, prevucite element **Polje** u odgovarajuću poziciju na stranici, a zatim podesite njegova svojstva.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrednosti skupa opcija
Da biste dodali vrednosti skupa opcija u gotovo polje, pratite ove korake.

1. Otvorite stranicu za uređivanje polja, a zatim u delu **Tip** odaberite **Uredi** pored skupa opcija.
2. Dodajte novu opciju koja ima prilagođenu oznaku i boju. Ako želite da dodate novi status stavke vremena, unapred definisano polje se zove **Status stavke**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označavanje statusa nove stavke vremena kao samo za čitanje
Da biste označili status nove stavke vremena kao samo za čitanje, dodajte vrednost nove stavke vremena u svojstvo **Lista statusa samo za čitanje**. Budite sigurni da dodate broj, a ne oznaku. Deo mreže stavke vremena koji sada može da se uređuje biće zaključan za redove koji imaju novi status. Da biste svojstvo **Lista statusa samo za čitanje** postavili drugačije za različite prikaze **Stavki vremena**, dodajte matricu koordinatne mreže **Stavka vremena** u odeljak **Prilagođene kontrole** prikaza i konfigurišite parametre na odgovarajući način.

Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama **Uređivanje reda** i **Uređivanje stavke vremena** koje pružaju iskustvo zasnovano na zadacima. Da biste pristupili poslovnim pravilima za ove stranice, otvorite uređivač obrazaca za svaku stranicu, a zatim izaberite **Poslovna pravila**. Novi status možete dodati u uslov postojećih poslovnih pravila ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila za proveru valjanosti
Možete da dodate dve vrste pravila za validaciju sedmično iskustvo matrice koordinatne mreže **Sedmične stavke vremena**:

- Poslovna pravila na strani klijenta koja funkcionišu na stranicama
- Provere valjanosti dodatnih komponenti na strani servera koja se primenjuju na sva ažuriranja stavki vremena

#### <a name="client-side-business-rules"></a>Poslovna pravila na strani klijenta
Upotrebite poslovna pravila za zaključavanje i otključavanje polja, unesite podrazumevane vrednosti u polja i definišite validacije koje zahtevaju informacije samo iz trenutnog zapisa stavke vremena. Da biste pristupili poslovnim pravilima za stranicu, otvorite uređivač obrazaca, a zatim izaberite **Poslovna pravila**. Zatim možete da izmenite postojeća poslovna pravila ili dodate novo poslovno pravilo.

#### <a name="server-side-plug-in-validations"></a>Provere valjanosti dodatnih komponenti na strani servera
Trebalo bi da koristite validacije dodatnih komponenti za sve validacije za koje je potrebno više konteksta nego što je dostupno u jednom zapisu stavke vremena. Takođe bi trebalo da ih koristite za sve validacije koje želite da pokrenete na umetnutim ispravkama u matrici koordinatne mreže. Da biste dovršili provere valjanosti, napravite prilagođenu dodatnu komponentu u entitetu **Stavka vremena**.

### <a name="limits"></a>Ograničenja
Trenutno matrica koordinatne mreže **Stavka vremena** ima ograničenje veličine od 500 redova. Ako ima više od 500 redova, višak redova neće biti pokazan. Ne postoji način da povećate ograničenje veličine.

### <a name="copying-time-entries"></a>Kopiranje stavki vremena
Koristite prikaz **Kolone za kopiranje stavki vremena** da biste definisali listu polja za kopiranje tokom unosa vremena. **Datum** i **Trajanje** su obavezna polja i ne bi ih trebalo ukloniti iz prikaza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
