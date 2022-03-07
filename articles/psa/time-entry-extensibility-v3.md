---
title: Prilagođavanje sedmične stavke vremena
description: Ova tema pruža informacije o tome kako implementirati prilagođena poslovna pravila koja podržavaju prakse organizacije.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: fa2ef927e0234919ee4777f24c60569fb33a8570f6d48be6aef356df4f08a6e7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002303"
---
# <a name="customize-weekly-time-entry"></a>Prilagođavanje sedmične stavke vremena 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U aplikaciji Microsoft Dynamics 365 Project Service Automation verzije 3.3, Microsoft je uveo modernu mrežu koja omogućava resursima za projekte da brzo i odjednom unose vreme za najviše nedelju dana. Nova mreža sedmičnih stavki vremena može prikazati ukupan broj stavki po datumu, redovima ili nedeljama. Resursi mogu da naprave kopije stavki vremena u okviru nedelje, a takođe i da grupno kopiraju stavke iz prethodnih nedelja. Osobe koje prilagođavaju sistem mogu prilagoditi prikaz dodavanjem polja, dodavanjem pronalaženja drugim entitetima i primenom prilagođenih poslovnih pravila koja podržavaju prakse njihove organizacije.

Stavci vremena i novoj mreži za vremenski period od nedelju dana pristupa se putem mape lokacije. Iskustvo neproširive prilagođene stavke vremena koje je bilo deo ranijih verzija aplikacije PSA zamenjeno je proširivom mrežom za sedmičnu stavku vremena, a takođe i alternativnim iskustvom u mreži i kalendaru samo za čitanje. Zbog ove promene korisnici mogu unositi vreme u nedeljama.

## <a name="page-layout"></a>Raspored stranice
Nova mreža sedmičnih stavki vremena je prilagođena kontrola koja sadrži traku sa alatkama i dva glavna odeljka, **Dimenzije** i **Trajanje**. Traka sa alatkama sadrži dugme koje se odnosi samo na ovu prilagođenu kontrolu za mrežu stavke vremena. Za razliku od toga, dugmad u oknu sa radnjama na vrhu stranice primenjuju se na tri vrste kontrola koje su podržane za stavku vremena: kontrolu sedmične stavke vremena, kontrolu samo za čitanje i kontrolu kalendara.

### <a name="dimensions"></a>Dimenzije
Odeljak **Dimenzije** prikazuje, kao nazive kolona, sve dimenzije za koje se vreme može uneti. Sledeće dimenzije su podržane kao unapred definisane:

- Projekat
- Projektni zadatak
- Uloga
- Tip
- Status stavke

Odeljak **Dimenzije** ne dozvoljava unutrašnje uređivanje. Ovaj odeljak je podržan prikazom koji omogućava da se prilagođena polja dodaju u mrežu sedmičnih stavki vremena. Informacije o dodavanju prilagođenih polja potražite u odeljku „Proširivost“ kasnije u ovoj temi.

### <a name="duration"></a>Trajanje
Odeljak Trajanje prikazuje dane u nedelji kao zaglavlja kolona. Ovaj odeljak omogućava unutrašnje uređivanje. Nakon što se kreira red za stavku vremena koji ima odgovarajuće dimenzije, korisnici mogu unutra brzo uneti količinu vremena koju su utrošili za te dimenzije.

## <a name="create-a-new-time-entry"></a>Kreiranje nove stavke vremena
Da biste kreirali novu stavku vremena u mreži stavke vremena, izaberite **Nova**. Pojaviće se dijalog **Brzo kreiranje stavke vremena**. U ovom dijalogu, korisnici mogu odabrati datum stavke vremena, a zatim uneti podatke za dimenzije **Projekat**, **Projektni zadatak**, **Uloga** i **Trajanje** u minutima, satima ili danima unosom **s**, **m** ili **d**, zajedno sa brojem. Korisnici takođe mogu uneti opis i komentare koji se mogu deliti eksterno za stavku vremena. Kada korisnici sačuvaju svoje promene, vrednosti koje su uneli za dimenzije se pojavljuju u odeljku **Dimenzije**. Informacije o trajanju koje su uneli u polje **Trajanje** se pojavljuju za datum za koji je kreirana stavka vremena.

Polja za pronalaženje podržavaju sistemski prikazi. Na primer, nakon što korisnik unese projekat, polje **Projektni zadatak** se podrazumevano podešava na prikaz **Kopiranje**. Da biste kreirali stavke vremena za zadatke koji nisu dodeljeni korisniku, izaberite **Promeni prikaz** u dijalogu za pretraživanje, a zatim izaberite **Svi zadaci aktivnog projekta**.

## <a name="edit-a-time-entry"></a>Uređivanje stavke vremena
Detalji iz nekih polja na stranici za stavku vremena, kao što su **Opis** i **Spoljni komentari**, nisu prikazani u mreži sedmičnih stavki vremena. Umesto toga, u ćelijama trajanja pojavljuje se mali trouglasti indikator koji ima ove dodatne detalje. Izaberite ćeliju, a zatim izaberite **Uređivanje detalja** da biste pregledali podatke u oknu **Brzo uređivanje**. Da bi izmenili ili ažurirali detalje za određenu stavku vremena koja nije deo mreže sedmičnih stavki vremena, korisnici moraju da otvore okno **Brzo uređivanje**.

## <a name="copy-a-time-entry-row"></a>Kopiranje reda stavke vremena
Nakon što je kreiran prvi red stavke vremena, korisnici mogu da izaberu **Kopiraj red** da bi iskopirali ceo red u novi red. Kada se red kopira na ovaj način, dimenzije i trajanje se takođe kopiraju. Korisnici takođe mogu da izaberu **Izmeni red** da bi ažurirali vrednosti dimenzija i trajanja u odeljku **Trajanje**.

## <a name="open-a-time-entry"></a>Otvaranje stavke vremena
Da bi podržao optimalan i brz unos u najistaknutija polja, mreža sedmičnih stavki vremena pokazuje podskup odabranih dimenzija i trajanja vremena. Da biste videli sve detalje jedne stavke vremena, u delu **Izmena stavke** odaberite **Otvori**.

## <a name="submit-a-time-entry"></a>Prosleđivanje stavke vremena
Korisnici mogu proslediti jednu stavku vremena ili grupu stavki vremena izborom bloka ćelija ili celog reda stavke vremena, a zatim izborom opcije **Prosledi**. Prosleđene stavke vremena pojavljuju se kao stavke koje čekaju odobrenje na stranici davaoca odobrenja **Odobrenje**. Nakon uspešnog prosleđivanja stavki vremena, one se ne mogu uređivati.

## <a name="recall-a-time-entry"></a>Opozivanje stavke vremena
Možete opozvati stavke vremena koje ste prosledili. Možete da opozovete jednu stavku vremena, blok stavki vremena ili čitav red stavki vremena. Opozvane stavke vremena dostupne su resursima za uređivanje.

## <a name="time-entry-status"></a>Status stavke vremena
Novim stavkama vremena automatski se dodeljuje status **Radna verzija**. Kada se prosledi stavka vremena, status se ažurira na **Prosleđena**. Kada se prosleđena stavka vremena odobri, status se ažurira na **Odobrena**. Ako je stavka vremena odbijena, status se ažurira na **Vraćena** i stavka postaje dostupna za ispravku i ponovno prosleđivanje. Samo stavke vremena koje imaju status **Radna verzija** možete da izbrišete.

## <a name="view-rejection-comments"></a>Pregled komentara o odbacivanju
Kada davalac odobrenja odbaci stavku vremena, može da doda komentare o odbacivanju kako bi pomogao resursu da shvati razlog odbacivanja. Da biste videli komentare o odbacivanju stavke vremena, izaberite **Otvori stavku**. Komentari o odbacivanju biće prikazani na vremenskoj osi. U vremenskoj osi, resurs može da odgovori na komentare o odbacivanju pre nego što ponovo prosledi stavku.

## <a name="copy-week"></a>Kopiranje sedmice
Nakon kreiranja nekoliko stavki vremena, korisnici mogu da izaberu **Kopiranje sedmice** da bi grupno kreirali dodatne stavke vremena. Pojavljuje se dijalog **Kopiranje**. U odeljku **Iz perioda** koristite polja **Datum početka** i **Datum završetka** za definisanje opsega datuma iz kojeg treba kopirati stavke vremena. U odeljku **U period**, u polju **Datum početka**, odredite datum za koji ćete kreirati stavke vremena. Zatim izaberite **Kopiraj**. Za određeni datum u „U“ periodu kreira se kopija stavki vremena za odgovarajući dan u nedelji u „Iz“ periodu. Na primer, stavka vremena za ponedeljak iz prošle nedelje se kopira u ponedeljak one sedmice koja je navedena kao „U“ period.

## <a name="import"></a>Uvoz
Isti osnovni postupak koristi se za uvoz iz rezervacija, dodela i razmena. Korisnici mogu odrediti opseg datuma iz kojeg se uvoze rezervacije. Zatim moraju izričito izabrati rezervacije koje treba kopirati u radne verzije stavki vremena. U prethodnom izdanju, predložene stavke vremena su se prikazivale u mreži i kalendaru i bile izgubljene prilikom osvežavanja sesije.

## <a name="extensibility"></a>Proširivost
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Dodavanje prilagođenih polja koja sadrže pretraživanja u druge entitete
Tri su glavna koraka za dodavanje prilagođenog polja u mrežu sedmičnih stavki vremena.

1.  Dodajte prilagođeno polje u dijalog za brzo kreiranje.
2.  Konfigurišite mrežu da prikazuje prilagođeno polje.
3.  Po potrebi dodajte prilagođeno polje u tok zadataka uređenja reda ili tok zadataka uređenja ćelije.

Morate takođe biti sigurni da novo polje ima potrebne potvrde u toku zadataka uređenja reda ili ćelije. Kao deo ovog koraka morate zaključati polje na osnovu statusa stavke vremena.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Dodavanje prilagođenog polja u dijalog za brzo kreiranje
Morate dodati prilagođeno polje u dijalog za brzo kreiranje stavke vremena. Tako će korisnici moći da unesu vrednost polja kada dodaju stavke vremena klikom na dugme **Nova**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Konfigurisanje mreže za prikaz prilagođenog polja
Prilagođeno polje možete da dodate na dva načina u mrežu sedmičnih stavki vremena. Prva opcija je da prilagodite prikaz **Moje sedmične stavke vremena** i dodate mu prilagođeno polje. Možete odabrati položaj i veličinu prilagođenog polja u mreži uređivanjem tih svojstava u prikazu.

Druga opcija je kreiranje novog prilagođenog prikaza stavke vremena i njegovo podešavanje kao podrazumevanog prikaza. Ovaj prikaz treba da sadrži polja **Opis** i **Spoljni komentari**, pored kolona koje želite da imate na mreži. Možete odabrati položaj, veličinu i podrazumevani redosled sortiranja u mreži uređivanjem tih svojstava u prikazu. Zatim konfigurišite prilagođenu kontrolu za ovaj prikaz tako da to bude kontrola **Mreža stavke vremena**. Dodajte ovu kontrolu u prikaz i odaberite je za veb, telefon i tablet. Zatim konfigurišite parametre za mrežu sedmičnih stavki vremena. Podesite polje **Datum početka** na **msdyn_date**, podesite polje **Trajanje** na **msdyn_duration**, a **Status** na **msdyn_entrystatus**. Za podrazumevani prikaz, polje **Lista statusa samo za čitanje** je podešeno na **192350002,192350003,192350004**, polje **Tok zadataka uređenja reda** na **msdyn_timeentryrowedit**, a polje **Tok zadataka uređenja ćelije** na **msdyn_timeentryedit**. Ova polja možete prilagoditi da biste dodali ili uklonili status samo za čitanje ili koristili drugo iskustvo zasnovano na zadacima za uređivanje redova ili ćelija. Ova polja treba da budu vezana za statičku vrednost.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Dodavanje prilagođenog polja u odgovarajući tok zadatka za uređivanje
Stranice koje pružaju iskustvo zasnovano na zadacima, koje se koriste za uređivanje, možete pronaći u delu **Procesi**. Podrazumevane stranice su **Project Service – Uređivanje reda stavke vremena** i **Project Service – Uređivanje stavki vremena**. Možete da izmenite ove podrazumevan stranice ili da kreirate nove stranice koje pružaju iskustvo zasnovano na zadacima.

> [!NOTE] 
> Obe opcije će ukloniti neko unapred definisano filtriranje za entitete **Projekat** i **Projektni zadatak**, tako da će svi prikazi pronalaženja entiteta biti vidljivi. Kao unapred definisani su vidljivi samo relevantni prikazi pronalaženja.

Morate odrediti odgovarajući tok zadataka za prilagođeno polje. Najvjerovatnije, ako ste dodali polje u mrežu, ono bi trebalo da ide u tok zadataka uređenja reda koji se koristi za polja koja se primjenjuju na celi red sa stavkama vremena. Ako prilagođeno polje ima jedinstvenu vrednost svakog dana, kao što je prilagođeno polje za **Vreme završetka**, trebalo bi da ide u tok zadataka uređenja ćelije.

Da biste dodali prilagođeno polje u tok zadataka, prevucite element **Polje** u odgovarajuću poziciju na stranici, a zatim podesite njegova svojstva. Podesite svojstvo **Izvor** na **Stavka vremena**, a svojstvo **Polje podataka** na prilagođeno polje. Svojstvo **Polje** određuje ime za prikaz na stranici koja pruža iskustvo zasnovano na zadacima. Izaberite **Primeni** da biste sačuvali promene polja. Zatim izaberite **Ažuriraj** da biste sačuvali promene stranice.

Da biste umesto toga koristili novu prilagođenu stranicu koja pruža iskustvo zasnovano na zadacima, kreirajte novi postupak. Podesite kategoriju na **Tok poslovnog procesa**, entitet na **Stavka vremena**, a vrstu poslovnog procesa na **Pokreni proces kao tok zadataka**. U delu **Svojstva**, svojstvo **Naziv stranice** treba da podesite na ime za prikaz na stranici. Na stranicu koja pruža iskustvo zasnovano na zadacima dodajte sva relevantna polja. Sačuvajte i aktivirajte postupak, a zatim ažurirajte svojstvo prilagođene kontrole za odgovarajući tok zadataka na vrednost **Ime** za proces.

### <a name="add-new-option-set-values"></a>Dodavanje novih vrednosti skupa opcija
Da biste dodali vrednosti skupa opcija u unapred definisano polje, otvorite stranicu za uređivanje polja, a zatim u delu **Tip** odaberite **Uredi** pored skupa opcija. Zatim dodajte novu opciju koja ima prilagođenu oznaku i boju. Ako želite da dodate novi status stavke vremena, unapred definisano polje se zove **Status stavke**, a ne **Status**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Označavanje statusa nove stavke vremena kao samo za čitanje
Da biste označili status nove stavke vremena kao samo za čitanje, dodajte vrednost nove stavke vremena (broj, a ne oznaku) u svojstvo **Lista statusa samo za čitanje**. Deo mreže stavke vremena koji može da se uređuje biće zaključan za redove koji imaju novi status.
Zatim dodajte poslovna pravila da biste zaključali sva polja na stranicama **Uređivanje reda stavke vremena** i **Uređivanje stavke vremena** koje pružaju iskustvo zasnovano na zadacima. Poslovnim pravilima za ove stranice možete pristupiti tako što ćete otvoriti uređivač toka poslovnog procesa za stranicu i izabrati **Poslovna pravila**. Novi status možete dodati u uslov postojećih poslovnih pravila ili možete dodati novo poslovno pravilo za novi status.

### <a name="add-custom-validation-rules"></a>Dodavanje prilagođenih pravila za proveru valjanosti
Postoje dve vrste pravila za proveru valjanosti koja možete dodati iskustvu korišćenja mreže sedmičnih stavki vremena: •   Poslovna pravila na strani klijenta koja funkcionišu u dijalozima za brzo kreiranje i na stranicama koje pružaju iskustvo zasnovano na zadacima •   Provera valjanosti dodatnih komponenti na strani servera koja se primenjuje na ispravke svih stavki vremena

#### <a name="business-rules"></a>Poslovna pravila
Upotrebite poslovna pravila za zaključavanje i otključavanje polja, unesite podrazumevane vrednosti u polja i definišite validacije koje zahtevaju informacije samo iz trenutnog zapisa stavke vremena. Poslovnim pravilima za stranicu koja pruža iskustvo zasnovano na zadacima možete pristupiti tako što ćete otvoriti uređivač toka poslovnog procesa za stranicu i izabrati **Poslovna pravila**. Zatim možete da izmenite postojeća poslovna pravila ili dodate novo poslovno pravilo. Za još prilagođenije provere valjanosti, možete da pokrenete JavaScript pomoću poslovnog pravila.

#### <a name="plug-in-validations"></a>Provere valjanosti dodatnih komponenti
Treba da koristite validacije dodatnih komponenti za sve validacije za koje je potrebno više konteksta nego što je dostupno u jednom zapisu stavke vremena ili za bilo kakve validacije koje želite da pokrenete iznutra za ažuriranja mreže. Da biste dovršili proveru valjanosti, napravite prilagođenu dodatnu komponentu u entitetu **Stavka vremena**.

> [!IMPORTANT] 
> Trenutno poznati problem na stranicama koje pružaju iskustvo zasnovano na zadacima sprečavaju korisnike da ispravljaju informacije i ponovo izaberu Gotovo kada ne uspe provera valjanosti dodatne komponente prilikom ažuriranja. Kao zaobilazno rešenje, podesite validacije poslovnih pravila kako biste sprečili ovu situaciju koliko je to moguće.


[!INCLUDE[footer-include](../includes/footer-banner.md)]