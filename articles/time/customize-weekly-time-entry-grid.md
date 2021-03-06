---
title: Proširenje stavki vremena
description: Ova tema pruža informacije o tome kako programeri mogu da prošire kontrolu stavki vremena.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930897"
---
# <a name="extending-time-entries"></a>Proširenje stavki vremena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations uključuje prilagođenu kontrolu stavki vremena. Ova kontrola sadrži sledeće funkcije:

- Unesite vreme horizontalno tokom nedelje
- Ukupno po danu, redu ili nedelji
- Kopirajte redove ili nedelje
- Stavka vremena kroz HH:mm ili HH.hh (automatski se konvertuje u HH.hh)
- Uvoz iz dodela, rezervacija ili zakazanih obaveza

Produženje unosa vremena moguće je u dve oblasti:
- [Dodajte prilagođene stavke vremena za sopstvenu upotrebu](#add)
- [Prilagođavanje kontrole sedmične stavke vremena](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Dodajte prilagođene stavke vremena za sopstvenu upotrebu.

Stavke vremena su osnovni entitet koji je dizajniran da se koristi za više scenarija. U 1. talasu za april 2020. predstavljeno je osnovno rešenje TESA, koje pruža entitet **Podešavanja** i nova bezbednosna uloga **Korisnik stavke vremena**. Nova polja, **msdyn_start** i **msdyn_end**, koja imaju direktnu vezu sa **msdyn_duration**, takođe su bila uključena. Novi entitet, bezbednosna uloga, i polja omogućavaju jedinstveniji pristup vremenu u više proizvoda.


### <a name="time-source-entity"></a>Izvorni entitet vremena
| Polje | Opis | 
|-------|------------|
| +Ime  | Naziv stavke izvora vremena koji se koristi kao vrednost izbora tokom kreiranja stavke vremena. |
| Podrazumevani izvor vremena [Izvor vremena: isdefault] | Podrazumevano, samo jedan izvor vremena može biti označen kao podrazumevani izvor vremena. Ova mogućnost omogućava da se za stavke podrazumeva izvor vremena ako nijedno vreme nije navedeno. |
|Tip izvora vremena [Izvor vremena: sourcetype] | Tip izvora je opcija (Tip stavke izvora vremena) koja omogućava povezivanje izvora vremena sa aplikacijom. Dodatne vrednosti će se dodati ovom skupu opcija kako se dodaju dodatne aplikacije. Imajte na umu da Microsoft zadržava vrednosti veće od 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Stavke vremena i Izvorni entitet vremena
Svaka stavka vremena povezana je sa zapisom izvora vremena. Ovaj zapis određuje kako i koje aplikacije treba da obrade stavku vremena.

Stavke vremena su uvek jedan neprekidni vremenski blok sa povezanim početkom, krajem i trajanjem.

Logika će automatski ažurirati zapis stavke vremena u sledećim situacijama:

- Ako su navedena dva od tri sledeća polja, treće se izračunava automatski 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Polja **msdyn_start** i **msdyn_end** prepoznaju vremensku zonu.
- Stavke vremena kreirane samo sa navedenim poljima **msdyn_date** i **msdyn_duration** počeće u ponoć, a polja **msdyn_start** i **msdyn_end** biće ažurirana u skladu s tim.

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

- Dodajte prilagođeno polje u dijalog za brzo kreiranje.
- Konfigurišite mrežu da prikazuje prilagođeno polje.
- Dodajte prilagođeno polje u tok zadataka uređenja reda ili tok zadataka uređenja ćelije.

Morate takođe biti sigurni da novo polje ima potrebne potvrde u toku zadataka uređenja reda ili ćelije. Kao deo ovog koraka, morate zaključati polje na osnovu statusa stavke vremena.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijalog za brzo kreiranje
Morate dodati prilagođeno polje u dijalog **Brzo kreiranje stavke vremena**. Korisnici tada mogu da unesu vrednost kada dodaju stavke vremena izborom opcije **Nova**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurisanje mreže za prikaz prilagođenog polja
Prilagođeno polje možete da dodate na dva načina u mrežu sedmičnih stavki vremena:

  - Prilagodite prikaz i dodajte prilagođeno polje
  - Kreirajte novu podrazumevanu prilagođenu stavku vremena 


**Prilagodite prikaz i dodajte prilagođeno polje**

Možete da prilagodite prikaz **Moje sedmične stavke vremena** i dodate mu prilagođeno polje. Možete odabrati položaj i veličinu prilagođenog polja u mreži uređivanjem tih svojstava u prikazu.

**Kreirajte novu podrazumevanu prilagođenu stavku vremena** 

Ovaj prikaz treba da sadrži polja **Opis** i **Spoljni komentari**, pored kolona koje želite da imate na mreži. 

1. Odaberite položaj, veličinu i podrazumevani redosled sortiranja u mreži uređivanjem tih svojstava u prikazu. 
2. Konfigurišite prilagođenu kontrolu za ovaj prikaz tako da to bude kontrola **Mreža stavke vremena**. 
3. Dodajte ovu kontrolu u prikaz i odaberite je za veb, telefon i tablet. 
4. Konfigurišite parametre za mrežu sedmičnih stavki vremena. Podesite polje **Datum početka** na **msdyn_date**, podesite polje **Trajanje** na **msdyn_duration**, a **Status** na **msdyn_entrystatus**. 
5. Za podrazumevani prikaz, polje **Lista statusa samo za čitanje** je podešeno na **192350002,192350003,192350004**, polje **Tok zadataka uređenja reda** na **msdyn_timeentryrowedit**, a polje **Tok zadataka uređenja ćelije** na **msdyn_timeentryedit**. 
6. Ova polja možete prilagoditi da biste dodali ili uklonili status samo za čitanje ili koristili drugo iskustvo zasnovano na zadacima za uređivanje redova ili ćelija. Ova polja treba da budu vezana za statičku vrednost.


> [!NOTE] 
> Obe opcije će ukloniti neko unapred definisano filtriranje za entitete **Projekat** i **Projektni zadatak**, tako da će svi prikazi pronalaženja entiteta biti vidljivi. Kao unapred definisani su vidljivi samo relevantni prikazi pronalaženja.
Morate odrediti odgovarajući tok zadataka za prilagođeno polje. Najvjerovatnije, ako ste dodali polje u mrežu, ono bi trebalo da ide u tok zadataka uređenja reda koji se koristi za polja koja se primjenjuju na celi red sa stavkama vremena. Ako prilagođeno polje ima jedinstvenu vrednost svakog dana, kao što je prilagođeno polje za **Vreme završetka**, trebalo bi da ide u tok zadataka uređenja ćelije.

Da biste dodali prilagođeno polje u tok zadataka, prevucite element **Polje** u odgovarajuću poziciju na stranici, a zatim podesite svojstva polja. Podesite svojstvo **Izvor** na **Stavka vremena**, a svojstvo **Polje podataka** na prilagođeno polje. Svojstvo **Polje** određuje ime za prikaz na stranici koja pruža iskustvo zasnovano na zadacima. Izaberite **Primeni** da biste sačuvali promene u polju, a zatim izaberite **Ažuriraj** da biste sačuvali promene na stranici.

Da biste umesto toga koristili novu prilagođenu stranicu koja pruža iskustvo zasnovano na zadacima, kreirajte novi postupak. Podesite kategoriju na **Tok poslovnog procesa**, entitet na **Stavka vremena**, a vrstu poslovnog procesa na **Pokreni proces kao tok zadataka**. U delu **Svojstva**, svojstvo **Naziv stranice** treba da podesite na ime za prikaz na stranici. Na stranicu koja pruža iskustvo zasnovano na zadacima dodajte sva relevantna polja. Sačuvajte i aktivirajte postupak, a zatim ažurirajte svojstvo prilagođene kontrole za odgovarajući tok zadataka na vrednost **Ime** za proces.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrednosti skupa opcija
Da biste dodali vrednosti skupa opcija u unapred definisano polje, otvorite stranicu za uređivanje polja, a zatim u delu **Tip** odaberite **Uredi** pored skupa opcija. Zatim dodajte novu opciju koja ima prilagođenu oznaku i boju. Ako želite da dodate novi status stavke vremena, unapred definisano polje se zove **Status stavke**, a ne **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označavanje statusa nove stavke vremena kao samo za čitanje
Da biste označili status nove stavke vremena kao samo za čitanje, dodajte vrednost nove stavke vremena u svojstvo **Lista statusa samo za čitanje**. Deo mreže stavke vremena koji može da se uređuje biće zaključan za redove koji imaju novi status.
Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama **Uređivanje reda stavke vremena** i **Uređivanje stavke vremena** koje pružaju iskustvo zasnovano na zadacima. Poslovnim pravilima za ove stranice možete pristupiti tako što ćete otvoriti uređivač toka poslovnog procesa za stranicu i izabrati **Poslovna pravila**. Novi status možete dodati u uslov postojećih poslovnih pravila ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila za proveru valjanosti
Postoje dve vrste pravila za validaciju koje možete dodati za sedmično iskustvo mreže s unosom vremena:

- Poslovna pravila na strani klijenta koja rade u dijalozima za brzo kreiranje i na TBX stranicama.
- Provere valjanosti dodatnih komponenti na strani servera koja se primenjuju na sva ažuriranja stavki vremena.

#### <a name="business-rules"></a>Poslovna pravila
Upotrebite poslovna pravila za zaključavanje i otključavanje polja, unesite podrazumevane vrednosti u polja i definišite validacije koje zahtevaju informacije samo iz trenutnog zapisa stavke vremena. Poslovnim pravilima za stranicu koja pruža iskustvo zasnovano na zadacima možete pristupiti tako što ćete otvoriti uređivač toka poslovnog procesa za stranicu i izabrati **Poslovna pravila**. Zatim možete da izmenite postojeća poslovna pravila ili dodate novo poslovno pravilo. Za još prilagođenije provere valjanosti, možete da pokrenete JavaScript pomoću poslovnog pravila.

#### <a name="plug-in-validations"></a>Provere valjanosti dodatnih komponenti
Treba da koristite validacije dodatnih komponenti za sve validacije za koje je potrebno više konteksta nego što je dostupno u jednom zapisu stavke vremena ili za bilo kakve validacije koje želite da pokrenete iznutra za ažuriranja mreže. Da biste dovršili proveru valjanosti, napravite prilagođenu dodatnu komponentu u entitetu **Stavka vremena**.
