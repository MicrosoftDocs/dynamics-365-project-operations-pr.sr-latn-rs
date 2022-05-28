---
title: Proširenje stavki vremena
description: Ova tema pruža informacije o tome kako programeri mogu da prošire kontrolu stavki vremena.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6b91aecd76950d2bd37192d634c80ea98d08034e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583003"
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
Svaka stavka vremena povezana je sa zapisom izvora vremena. Ovaj zapis određuje koja aplikacija treba da obradi stavku vremena i kako.

Stavke vremena su uvek jedan neprekidni vremenski blok sa povezanim početkom, krajem i trajanjem.

Logika će automatski ažurirati zapis stavke vremena u sledećim situacijama:

- Ako su navedena dva od tri sledeća polja, treće se izračunava automatski: 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** su svesna vremenske zone.
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

1. Dodajte prilagođeno polje dijalogu **"Brzo** kreiranje".
2. Konfigurišite mrežu da prikazuje prilagođeno polje.
3. Dodajte prilagođeno polje stranici za uređivanje **reda** ili **unosa vremena**, na odgovarajući način.

Uverite se da novo polje ima potrebne provere valjanosti na stranici za uređivanje **stavki reda** **ili vremena**. Kao deo ovog zadatka zaključajte polje na osnovu statusa stavke vremena.

Kada dodate prilagođeno polje u koordinatnu mrežu **stavke** vremena, a zatim kreirate stavke vremena direktno u koordinatnoj mreži, prilagođeno polje za te stavke se automatski postavlja tako da se podudara sa redom. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja dijalogu "Brzo kreiranje"
Dodajte prilagođeno polje u dijalog " **Brzo kreiranje: Kreiranje vremenskog** unosa". Korisnici tada mogu da unesu vrednost kada dodaju stavke vremena izborom opcije **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurisanje mreže za prikaz prilagođenog polja
Postoje dva načina za dodavanje prilagođenog polja u koordinatnu mrežu za sedmično **vreme** unosa.

- Prilagodite **prikaz "Moje sedmične** stavke vremena" i dodajte mu prilagođeno polje. Položaj i veličinu prilagođenog polja u koordinatnoj mreži možete da navedete uređivanjem svojstava u prikazu.
- Kreirajte novi prilagođeni prikaz vremenske stavke i postavite ga kao podrazumevani prikaz. Ovaj prikaz bi trebalo da sadrži **polja "Opis**" i "**Spoljni komentari" pored kolona koje želite da koordinatna** mreža uključi. Položaj, veličinu i podrazumevani redosled sortiranja koordinatne mreže možete da navedete uređivanjem svojstava u prikazu. Zatim konfigurišite prilagođenu kontrolu za ovaj prikaz tako da to bude kontrola **Mreža stavke vremena**. Dodajte kontrolu u prikaz i izaberite je za **Web**, **Telefon** i **Tablet**. Zatim konfigurišite parametre za mrežu za unos **sedmičnog** vremena. Postavite **polje Datum početka** na **msdyn\_ datum**, podesite **polje Trajanje** **na msdyn\_ trajanje** i postavite **polje Status** **na msdyn\_ entrystatus**. Polje **"Lista statusa samo za čitanje** " postavljeno **je na 192350002 (odobreno)**, **192350003 (prosleđeno)** ili **na 192350004 (opoziv zahteva)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Dodavanje prilagođenog polja na odgovarajuću stranicu za uređivanje
Stranice koje se koriste za uređivanje vremenske stavke ili reda vremenskih stavki mogu se pronaći u okviru stavke **Obrasci**. Dugme **"Uredi stavku** " u koordinatnoj mreži otvara stranicu " **Uređivanje stavke** ", a dugme " **Uredi red** " otvara stranicu **za uređivanje** reda. Ove stranice možete da uređujete tako da sadrže prilagođena polja.

Obe opcije uklanjaju neke filtriranje iz kutije na entitetima **projekta i** **projektnog** zadatka, tako da svi prikazi pronalaženja entiteta budu vidljivi. Kao unapred definisani su vidljivi samo relevantni prikazi pronalaženja.

Morate odrediti odgovarajuću stranicu za prilagođeno polje. Najverovatnije, ako ste dodali polje u koordinatnu mrežu, ono bi trebalo da se nalazi na **stranici za uređivanje** reda koja se koristi za polja koja se primenjuju na ceo red stavki vremena. Ako prilagođeno polje ima jedinstvenu vrednost u redu svakog dana (na primer, ako je to prilagođeno polje za vreme završetka), trebalo bi da ode na stranicu **za uređivanje stavke** vremena.

Da biste dodali prilagođeno polje stranici, prevucite **element polja** na odgovarajući položaj na stranici, a zatim postavite njegova svojstva.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrednosti skupa opcija
Da biste skup opcija vrednosti u polje za izlaz iz okvira, sledite ove korake.

1. Otvorite stranicu za uređivanje polja, a zatim u okviru **Vrsta** izaberite **stavku** Uredi pored skup opcija.
2. Dodajte novu opciju koja ima prilagođenu oznaku i boju. Ako želite da dodate novi status stavke vremena, polje "Pravo iz kutije" se zove "Status **stavke"**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označavanje statusa nove stavke vremena kao samo za čitanje
Da biste označili status nove stavke vremena kao samo za čitanje, dodajte vrednost nove stavke vremena u svojstvo **Lista statusa samo za čitanje**. Obavezno dodajte broj, a ne oznaku. Deo koordinatne mreže vremenskih stavki koji se može uređivati sada će biti zaključan za redove koji imaju novi status. Da biste svojstvo **statusa samo za čitanje postavili drugačije** za različite **prikaze stavki** vremena, dodajte **koordinatnu mrežu** za unos vremena u odeljak prilagođenih **kontrola** prikaza i konfigurišite parametre na odgovarajući način.

Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama za **uređivanje** i **uređivanje stavki vremena u** redu. Da biste pristupili poslovnim pravilima za ove stranice, otvorite uređivač obrazaca stranicu, a zatim izaberite pravila **"Posao"**. Novi status možete dodati u uslov postojećih poslovnih pravila ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila za proveru valjanosti
Možete dodati dva tipa pravila za proveru valjanosti za iskustvo u koordinatnoj **mreži sedmičnog** vremena:

- Poslovna pravila na strani klijenta koja funkcionišu na stranicama
- Provere valjanosti dodatnih komponenti na strani servera koje se primenjuju na sve ispravke stavki vremena

#### <a name="client-side-business-rules"></a>Poslovna pravila na strani klijenta
Upotrebite poslovna pravila za zaključavanje i otključavanje polja, unesite podrazumevane vrednosti u polja i definišite validacije koje zahtevaju informacije samo iz trenutnog zapisa stavke vremena. Da biste pristupili poslovnim pravilima za stranicu, otvorite uređivač obrazaca, a zatim izaberite pravila **"Posao"**. Zatim možete da izmenite postojeća poslovna pravila ili dodate novo poslovno pravilo.

#### <a name="server-side-plug-in-validations"></a>Provere valjanosti dodatnih komponenti na strani servera
Trebalo bi da koristite provere valjanosti dodatnih komponenti za sve provere valjanosti koje zahtevaju više konteksta nego što je dostupno u jednom zapisu stavke vremena. Takođe bi trebalo da ih koristite za sve provere valjanosti koje želite da pokrenete na umetnutim ispravkama u koordinatnoj mreži. Da biste dovršili provere valjanosti, kreirajte prilagođenu dodatnu komponentu u entitetu **stavke** vremena.

### <a name="limits"></a>Ograničenja
Trenutno koordinatna mreža **za unos** vremena ima ograničenje veličine od 500 redova. Ako ima više od 500 redova, višak redova neće biti pokazan. Ne postoji način da povećate ograničenje veličine.

### <a name="copying-time-entries"></a>Kopiranje stavki vremena
Koristite prikaz **Kolone za kopiranje stavki vremena** da biste definisali listu polja za kopiranje tokom unosa vremena. **Datum** i **Trajanje** su obavezna polja i ne bi ih trebalo ukloniti iz prikaza.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
