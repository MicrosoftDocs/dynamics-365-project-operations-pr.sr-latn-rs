---
title: Pregled strukturne analize posla
description: Strukturna analiza posla (SAP) je opis posla koji će biti završen za projekat. To je hijerarhija zadataka koja predstavlja razumevanje projektnog tima o sastavu posla i veličini, ceni i trajanju svake komponente ili zadatka.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23861
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 954965ee947cbce9d1ae686d281a5fed25a78245
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755177"
---
# <a name="work-breakdown-structures-overview"></a>Pregled strukturne analize posla

[!include [banner](../includes/banner.md)]

Strukturna analiza posla (SAP) je opis posla koji će biti završen za projekat. To je hijerarhija zadataka koja predstavlja razumevanje projektnog tima o sastavu posla i veličini, ceni i trajanju svake komponente ili zadatka. SAP ima tri glavne svrhe:

-   Opisivanje analize ili sastava posla u zadacima.
-   Raspoređivanje posla u projektu.
-   Procena troškova svakog zadatka.

Stepen detalja u SAP-u zavisi od nivoa tačnosti koji je potreban u procenama i nivoa praćenja koji je potreban u odnosu na te procene. Projekti koji imaju vrlo malu toleranciju na klizanje u rasporedu ili troškovima obično zahtevaju detaljniji SAP, kao i marljivo praćenje napretka u radu i troškova u odnosu na SAP. Ova vrsta projekata je česta u građevinarstvu i inženjeringu. 

Suprotno tome, projekti u delatnostima kao što su mediji i oglašavanje, softver i IT infrastruktura imaju tendenciju da budu jedinstveni, a produktivnost je relativna spram iskustva i kompetencije pojedinca koji izvršava zadatak. Stoga ove delatnosti koriste SAP kako bi dobile približnu veličinu projekta, a ne da detaljno prate napredak tog projekta. 

Izgradnja SAP je intenzivan proces koji se obično radi tokom dužeg perioda i koji zahteva saradnju i informacije širokog spektra ljudi. Ova tema opisuje kako možete da koristite SAP poboljšanja da biste zadovoljili svoje zahteve za procene i praćenje.

## <a name="prerequisites-for-creating-a-wbs"></a>Preduslovi za kreiranje SAP
Da biste kreirali SAP, morate biti u stanju da kreirate raspored rada i procenite troškove rada.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Preduslovi za kreiranje rasporeda rada

Da biste koristili sve mogućnosti raspoređivanja funkcija SAP, dovršite sledeće podešavanje:

1.  Postavite podrazumevani kalendar i kalendar projekta:
    1.  Kliknite na **Upravljanje projektima i računovodstvo** &gt; **Podešavanje** &gt; **Parametri upravljanja projektom i računovodstvom** &gt; **Raspoređivanje**. U polju **Podrazumevani radni kalendar** navedite podrazumevani kalendar. Ovo će biti podrazumevani radni kalendar za svaki novi projekat koji je kreiran.
    2.  Možete da promenite podrazumevani kalendar za određeni projekat. Kliknite na stranicu sa detaljima projekta, a zatim na brzoj kartici **Projektni tim i zakazivanje** ažurirajte polje **Kalendar zakazivanja** izborom drugog kalendara.

2.  Podesite standardne radne dane i radno vreme. Kalendar koji ste postavili kao radni kalendar za svoj projekat koristiće se u SAP-u za utvrđivanje sledećih informacija:

-   Radni dani i praznici
-   Broj radnih sati u danu

Da biste podesili radne dane i radno vreme za kalendar ili kreirali novi kalendar, kliknite na **Administracija organizacije** &gt; **Zajednički** &gt; **Kalendari**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Preduslovi za procenu troškova rada

Da biste koristili pune mogućnosti procene troškova SAP, trebalo bi da odredite troškove i prodajne cene za radnike, kategorije rada, troškove i naknade, kao i stavke.

-   Da biste postavili troškove i prodajnu cenu rada, troškove i kategorije naknada, kliknite na **Upravljanje projektima i računovodstvo** &gt; **Podešavanje** &gt; **Cene**.
-   Da biste postavili troškove i prodajnu cenu stavki, koristite stranicu **Trgovinski ugovori** za svaku stavku na stranici liste **Objavljeni proizvodi** u upravljanju informacijama o proizvodu.

## <a name="creating-a-wbs"></a>Kreiranje WBS-a
Kreiranje SAP uključuje tri aktivnosti:

1.  **Dekompozicija posla** – Kreirajte raščlanjavanje posla na upravljačke delove ili zadatke.
2.  **Raspored rada** – Procenite vreme potrebno za izvršavanje zadatka, postavite međuzavisnost zadatka i izaberite datume početka i završetka zadataka.
3.  **Procena troškova** – Procenite troškove za svaki zadatak.

U sledećim odeljcima se razmatra kako mogućnosti SAP mogu pomoći u svakoj od ovih aktivnosti.

### <a name="work-decomposition"></a>Dekompozicija posla

Raščlanjavanje ili dekompozicija posla obično je prvi korak u procesu kreiranja SAP. SAP funkcionalnost podržava sledeće osnovne konstrukcije za raščlanjivanje ili dekompoziciju posla. 

**Osnovni zadatak projekta** Osnovni zadatak projekta je sažeti zadatak najvišeg nivoa za projekat. Svi drugi projektni zadaci se kreiraju ispod njega. Naziv osnovnog zadatka je uvek podešen na naziv projekta. Napor, datumi i trajanje osnovnog čvora sumiraju vrednosti zadataka ispod osnovnog zadatka. Nije moguće izmeniti svojstva osnovnog čvora niti ga izbrisati.

**Zadaci sažetka ili zadaci kontejnera** Zadatak sažetka je zadatak koji ispod sebe ima podzadatke ili sastavne zadatke. Zadatak sažetka nema samostalni trud ili trošak. Umesto toga, radni napor i cena zadatka sažetka su zbir radnog napora i troškova njegovih sastavnih zadataka. Najraniji datum početka sastavnih zadataka se koristi kao datum početka zadatka sažetka, a najkasniji datum završetka sastavnih zadataka se koristi kao datum završetka. Možete izmeniti naziv zadatka sažetka, ali ne možete izmeniti svojstva zakazivanja za trud, datume i trajanje. Ako izbrišete zadatak sažetka, brišete i sve njegove sastavne zadatke. 

**Zadaci čvora lista** Zadatak čvora lista predstavlja najdetaljniji radni paket na projektu. Čvor lista sadrži procenjeni trud, planirani broj resursa, planirane datume početka i završetka i trajanje. 

Možete izvršiti sledeće operacije hijerarhije da biste omogućili kreiranje hijerarhije posla ili dekompoziciju za projekat. 

**Novi zadatak** Svaki novi zadatak koji kreirate automatski se dodaje pod osnovni čvor, a zadatku se automatski dodeljuje SAP broj. SAP broj predstavlja nivo zadatka u hijerarhiji. Za zadatke na prvom nivou pod osnovnim zadatkom projekta, koristi se šema numerisanja od 1, 2, 3 i tako dalje. Za zadatke koji su ispod prvog nivoa, koristi se šema numerisanja 1.1, 1.2, 1.3 itd. Za svaki nivo koji se dodaje ispod prethodnog nivoa, dodaje se nova tačkasta serija brojeva. 

Trenutno ne možete prilagoditi SAP numerisanje. 

**Zadatak uvlačenja** Kada uvučete zadatak, on postaje podređen zadatku koji mu prethodi. SAP broj novog podređenog zadatka automatski se preračunava na osnovu SAP broja njegovog novog nadređenog zadatka. Nadređeni zadatak je sada zadatak sažetka ili zadatak kontejnera i stoga postaje zbir svojih sastavnih zadataka. 

> [!NOTE] 
> Kada uvlačite zadatke pod zadatkom koji je bio čvor lista pre operacije uvlačenja, novokreirani zadatak sažetka gubi vlastite datume, napor i broj resursa. Sada koristi sažetak vrednosti svojih novih sastavnih zadataka. 

**Izvlačenje zadatka** Kada izvučete zadatak, to više nije sastavni zadatak njegovog nadređenog zadatka. SAP broj ovog zadatka automatski se preračunava da bi odražavao novi nivo zadatka u hijerarhiji. Trud, troškovi i datumi prethodnog nadređenog zadatka ovog zadatka ponovo se izračunavaju kako ne bi uključili ovaj zadatak. 

**Pomeranje nagore i nadole** Kad kliknete na **Pomeri nagore** i **Pomeri nadole**, menjate položaj zadatka u hijerarhiji njegovog nadređenog zadatka. Pozicija zadatka ne utiče na aktivnosti, troškove, datume niti trajanje zadatka. Međutim, SAP broj zadatka se automatski preračunava da bi odražavao novu poziciju zadatka.

### <a name="schedule-estimation"></a>Procena rasporeda

Procena rasporeda je obično drugi korak u kreiranju SAP. Kao najbolja praksa, trebalo bi da završite procenu rasporeda nakon što kreirate zadatke. Stranica **Strukturna analiza posla** u usluzi Finance ima dva odeljka. Gornje okno je namenjeno proceni rasporeda, a donje uključuje karticu **Procenjeni troškovi i prihodi** koju možete koristiti za procenu troškova. 
**Zavisnosti zadatka** U SAP možete kreirati relaciju prethodnika između zadataka. Kada dodelite zadatke prethodnika nekom zadatku,taj zadatak možete da pokrenete jedino kada dovršite sve zadatke prethodnika. Planirani datum početka zadatka automatski se postavlja na najnoviji datum svih njegovih prethodnika. 

**Raspored zadataka** Sledeći faktori određuju raspoređivanje zadataka čvorova lista:

-   Prethodni zadaci
-   Napor
-   Broj resursa
-   Datume početka i završetka

Datum početka zadatka čvora lista koji nema prethodnih zadataka automatski se podešava na datum početka projekta. Trajanje zadatka čvora lista se uvek izračunava kao broj radnih dana između njegovog početka i završetka. 

*<strong><em>Pravila zakazivanja</em></strong>* Kada se uključi pomoć za automatsko raspoređivanje, sledeća pravila se primenjuju na zakazivanje zadataka za zadatke čvorova lista:

-   Datumi početka i završetka zadatka moraju biti radni dani, u skladu sa kalendarom za zakazivanje u okviru projekta.
-   Datum početka zadatka koji ima prethodne zadatke automatski se podešava na poslednji datum završetka prethodnih zadataka.
-   Napor za zadatak automatski se izračunava na sledeći način:

Broj osoba × Trajanje × Broj časova u standardnom radnom danu u kalendaru projekta. 

U nekim slučajevima, možda ćete želeti da odstupite od ovih pravila. Možete isključiti automatsko zakazivanje da biste sprečili da Finance automatski podešava ili ispravlja bilo koja svojstva zadataka čvorova lista. Kada unesete informacije o zadatku koji uzrokuje kršenje pravila zakazivanja, za zadatak se prikazuje ikona greške zakazivanja. Ako ne želite da se prikazuju greške rasporeda, kliknite na **Prikazane su greške rasporeda** da biste isključili funkciju. 

> [!NOTE] 
> Vrednosti zadatka sažetka ili zadatka kontejnera i dalje se izračunavaju kao zbir vrednosti sastavnih zadataka, bez obzira na to da li je pomoć za automatsko zakazivanje uključena ili isključena. 

**Ispravljanje grešaka u rasporedu** Kada je uključena pomoć za automatsko zakazivanje, verovatno neće doći do grešaka u zakazivanju. Međutim, ako isključite pomoć za automatsko zakazivanje, a zatim je ponovo uključite kasnije, ikone grešaka u zakazivanju mogu se pojaviti u SAP-u. 

**Ispravljanje grešaka u rasporedu prema zadatku** Kada dvaput kliknete na ikonu greške rasporeda za određeni zadatak, dijalog prikazuje sve greške rasporeda za taj zadatak. Možete odlučiti koje ćete greške rasporeda otkloniti za zadatak. 

**Ispravljanje svih grešaka u rasporedu** Ako želite da Finance popravi sve greške rasporeda u SAP-u, u oknu za radnje kliknite na **Ispravi sva odstupanja u planiranju**. 

> [!NOTE] 
> Ova funkcija može prouzrokovati značajne izmene SAP. Greške se ispravljaju sledećim redosledom:

1.  Procenjeni napor na svim zadacima se menja tako da je jednak kapacitetu definisanom u kalendaru projekta.
2.  Datum početka svakog zadatka se menja tako da zadatak započinje kada se završe svi prethodni zadaci.
3.  Datum početka svakog zadatka se menja kako bi se uklonili nedostaci u datumima početka prethodnih zadataka.

### <a name="cost-estimation"></a>Procena troškova

Kao što je ranije pomenuto u ovom dokumentu, unos procene troškova za svaki zadatak čvora lista koristeći karticu **Procenjeni troškovi i prihodi** u donjem oknu stranice **Strukturna analiza posla**. 

> [!NOTE] 
> Ne možete izmeniti procenu troškova za zadatak sažetka ili zadatak kontejnera. Procena troškova za zadatak sažetka jednaka je zbiru procene troškova njegovih zadataka u čvoru lista. Procenjeni ukupni trošak za svaki zadatak izračunava se kao zbir procenjenih iznosa troškova za sledeće vrste transakcija:

-   Rad
-   Stavka ili materijal
-   Troškovi

Tip transakcije **Naknada** koristi se za procenu prihoda zasnovanog na naknadama. Ova vrsta transakcije nema komponentu troškova i stoga se ne uzima u obzir prilikom procene troškova. 

Vrsta transakcije **Po računu** koristi se za beleženje ugovorene vrednosti prodaje u projektu sa fiksnom vrednošću. Ova vrsta transakcije se takođe ne uzima u obzir prilikom procene troškova. 

Kada procenjujete cenu rada, materijala i troškova za svaki zadatak, procenjenim troškovima morate dodeliti kategoriju projekta. 

**Procenjeni troškovi rada** Za svaki zadatak čvora lista, dodeljujete radni napor u satima i podrazumevanu kategoriju. Stoga, kada postavite raspored za zadatak, procena troškova rada za taj zadatak automatski se dodaje u podrazumevanu kategoriju za rad. Ova procena troškova je prikazana na kartici **Procenjeni troškovi i prihodi** u mreži **Detalji linije** za taj zadatak. Ako vam je potrebno više procena troškova rada, možete ih dodati na ovoj kartici. Ako povećate ili smanjite sate na proceni troškova rada, raspored zadatka se automatski preračunava. 

**Procena troškova i materijalnih troškova** Kartica **Procenjeni troškovi i prihodi** vam takođe omogućava da procenite troškove i materijalne troškove za zadatak, ako su vam potrebne procene. 

Troškovi i prodajna cena za svaku liniju procene rada ili troškova zasnivaju se na postavci koja je definisana za svaku kategoriju u tabelama cena na **Upravljanje projektima i računovodstvom** &gt; **Podešavanje** &gt; **Cene**. Za stavke, troškovi i prodajna cena se podrazumevano dodaju iz stavke ili trgovinskih ugovora na stranici liste **Objavljeni proizvodi** u upravljanju informacijama o proizvodu.

## <a name="tracking-progress-on-the-wbs"></a>Praćenje napretka na SAP-u
Neke delatnosti prate napredak projekta u odnosu na SAP na vrlo detaljnom nivou, dok druge prate napredak na višem nivou SAP. Ovaj odeljak opisuje kako možete da koristite SAP praćenje za svoje potrebe projekta. 

Finance ima tri prikaza za SAP projekta: prikaz planiranja, prikaz praćenja napora i prikaz praćenja troškova.

### <a name="planning-view"></a>Prikaz planiranja

Prikaz planiranja prikazuje planiranu ili osnovnu procenu rasporeda i informacije o troškovima. Iako ne postoje funkcije za praćenje verzije i osnovne linije za SAP projekta, vrednosti u ovom prikazu namenjene su predstavljanju osnovne verzije. Odeljci Procena rasporeda i Procena troškova ove teme opisuju ovaj prikaz i kako se koristi za kreiranje SAP.

### <a name="effort-tracking-view"></a>Prikaz za praćenje angažovanja

Prikaz Praćenje aktivnosti prikazuje praćenje napredovanja za zadatke u SAP-u. Upoređuje akumulirani stvarni broj sati napora za zadatak sa planiranim satima napora. Sledeće formule pružaju vrednosti u prikazu praćenja napora:

-   Procenat napretka = Stvarno angažovanje do danas ÷ Planirano angažovanje za zadatak
-   Preostali napor (poznat i kao Procena do završetka \[ETC\]) = Planirani napor - Stvarni napor do danas
-   Procena po završetku (EAC) = Preostalo angažovanje + Stvarno vreme angažovanja do danas
-   Odstupanje od projektovanog angažovanja = Planirano angažovanje - EAC

Pogled praćenja napora prikazuje projekciju varijanse napora za zadatak na osnovu toga da li je EAC veći ili manji od planiranog napora:

-   Ako je EAC veći od planiranog angažovanja, predviđa se da će zadatak oduzeti više vremena nego što je prvobitno planirano i kasniće.
-   Ako je EAC manji od planiranog angažovanja, predviđa se da će zadatak oduzeti manje vremena nego što je prvobitno planirano i biće ispred planiranog vremena.

**Ponovna projekcija napora rukovodioca projekta** Povremeno će menadžer projekta ili druga osoba koja prati napredak projekta morati da revidira prvobitne procene zadatka. Zadatak se može kretati brže ili sporije nego što je prvobitno predviđeno iz različitih razloga. Na primer, opseg je smanjen ili radnici imaju manje iskustva nego što je prvobitno planirano. Projekcije predstavljaju menadžerovu percepciju procene projekta, zasnovano na trenutnom statusu projekta. U opštem slučaju, ne bi trebalo da menjate vrednosti osnovne linije zato što osnovna linija projekta predstavlja objavljeni dokument za raspored projekta i procene troškova koje su svi zainteresovani za projekat prihvatili. 

Postoje dva načina na koje menadžeri projekta mogu da izmene angažovanje na zadacima:

-   Izmenite preostali napor koji je automatski podešen da ažurira stvarni preostali napor na zadatku.
-   Izmenite procenat napredovanja koji je automatski podešen da ažurira stvarno napredovanje na zadatku.

Oba ova pristupa dovode do toga da se ponovo izračunaju ETC, EAC i procenat napretka zadatka, kao i odstupanje od projektovane varijanse na zadatku. EAC, ETC i procenat napretka u zadacima sažetka takođe se ponovo izračunavaju, a njihova projektovana varijansa angažovanja se ažurira. 

**Modifikovani napor na zadacima sažetka** Možete da izmenite napore na zadacima sažetka ili zadacima kontejnera. Bez obzira na to da li menjate ove vrednosti pomoću preostalog angažovanja ili procenta napretka zadataka sažetka, do izračunavanja dolazi automatski u sledećem redosledu:

1.  EAC, ETC i procenat napretka zadatka se izračunavaju.
2.  Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni iznos EAC.
3.  Novi EAC se izračunava za svaki zadatak čvora lista.
4.  Preostali napor i procenat napretka preračunavaju se za sve podređene zadatke na koje utiču, na osnovu nove vrednosti EAC. Takođe se preračunava varijansa napora zadataka.
5.  EAC zadataka sažetka se takođe preračunava iz čvorova lista.

Kliknite na **Proširi do nivoa** u prikazu praćenja napora da biste postavili nivo na kojem ćete pratiti i održavati svoj SAP. SAP se automatski proširuje na taj nivo u prikazu praćenja napora kad god ga otvorite.

### <a name="cost-tracking-view"></a>Prikaz praćenja troškova

Prikaz praćenja troškova prikazuje praćenje troškova korišćenja za zadatak. U ovom prikazu, stvarni troškovi potrošeni u odnosu na zadatak do danas se upoređuju sa planiranim troškovima zadatka. Sledeće formule pružaju vrednosti u prikazu praćenja troškova:

-   Procenat ostvarenih troškova = Stvarni troškovi do danas ÷ Planirani troškovi zadatka
-   Troškovi do završetka (CTC) = Planirani troškovi – Stvarni troškovi do danas
-   Procena pri završetku (EAC) = CTC + stvarni trošak do danas
-   Odstupanje od projektovanih troškova = Planirani troškovi - EAC

Pogled praćenja troškova prikazuje projekciju varijanse troškova za zadatak na osnovu toga da li je EAC veći ili manji od planiranog troška:

-   Ako je EAC veći od planiranog troška, predviđa se da će zadatak potrošiti više novca nego što je prvobitno planirano i premašiće budžet.
-   Ako je EAC manji od planiranog troška, predviđa se da će zadatak potrošiti manje novca nego što je prvobitno planirano i biće ispod budžeta.

**Ponovna projekcija troškova menadžera projekta** Menadžeri projekata moraju da koriste CTC za reviziju prvobitne procene troškova zadatka. Menadžer projekta može da prilagodi CTC vrednost trošku koji je potreban za dovršavanje zadatka. Ako izmenite CTC vrednost, izračunavaju se CTC zadatka, EAC i procenat potrošenih troškova, kao i projektovana varijansa troškova na zadatku. EAC, ETC i procenat troškova utrošenih u zadacima sažetka takođe se ponovo izračunavaju, a njihova projektovana varijansa troška se ažurira. 

> [!NOTE] 
> Kada revidirate napor SAP zadatka u prikazu praćenja napora, CTC zadatka, EAC, procenat utrošenog troška i projektovana varijansa troškova preračunavaju se u prikazu praćenja troškova. Međutim, revizije troškova ne utiču na vrednosti u prikazu praćenja napora jer se troškovi prema vrsti transakcije (rad, materijal ili trošak) ili kategoriji projekta ne revidiraju. 

**Revizija projekcije troškova zadatka sažetka** Možete izvršiti reviziju troškova za zadatke sažetka, a proračuni se odvijaju automatski sledećim redosledom:

1.  Ponovno se izračunavaju EAC, CTC i procenat troškova utrošenih na zadatak.
2.  Novi EAC se distribuira do nadređenih zadataka u istoj proporciji kao i izvorni EAC za zadatke.
3.  Izračunava se novi EAC za svaki zadatak.
4.  CTS i procenat utrošenih troškova se preračunavaju za zadatke deteta na koje se to odnosi, na osnovu vrednosti EAC. Takođe se preračunava varijansa troškova zadataka.
5.  EAC za sve zadatke sažetka se preračunava na osnovu ove promene.

Kliknite na **Proširi do nivoa** u prikazu praćenja troškova da biste postavili nivo na kojem ćete pratiti i održavati svoj SAP. SAP se automatski proširuje na taj nivo u prikazu praćenja troškova kad god ga otvorite.

### <a name="earned-value-management"></a>Upravljanje zarađenom vrednošću

Možete koristiti metodu zarađene vrednosti (EVM) da biste pratili napredak projekta. Pokazatelje zarađene vrednosti možete pregledati u Centru za uloge menadžera projekta. Komponenta grafikona zarađenih vrednosti prikazuje vrednosti sa vremenskom fazom planirane vrednosti i stvarnih troškova. Zarađena vrednost na tekućem datumu prikazana je kao poen. Podaci sa vremenskom fazom za zarađenu vrednost trenutno nisu dostupni. 

Vremenska faza na grafikonu zarađenih vrednosti prikazuje se po nedeljama ili mesecima. Ovaj odeljak opisuje tri stuba EVM: planiranu vrednost, ostvarenu vrednost i stvarni trošak. 

**Planirana vrednost** Teorija EVM kaže da postavljanje planirane vrednosti predstavlja stopu kojom je projektni tim planirao da zaradi vrednost na projektu. 

Finance koristi pravilo zarade 0:100 kada postavlja planiranu vrednost. Prema ovom pravilu, vrednost zadatka se knjiži u zadatak od datuma završetka. Nijedna vrednost se ne objavljuje dok se zadatak ne izvrši 100 posto. 

U Upravljanju projektima i računovodstvu unosite datum završetka čvorova lista i planirani trošak za to. Kada se grafikon planirane vrednosti prikaže po nedeljama, planirana vrednost se sažima po nedeljama za sve zadatke čvorova lista tokom trajanja projekta. 

**Zarađena vrednost** Teorija EVM kaže da postavljanje zarađene vrednosti predstavlja stopu kojom je projektni tim zapravo zarađivao vrednost na projektu. 

Finance koristi pravilo zarade 0:100 kada postavlja zarađenu vrednost. Prema ovom pravilu, vrednost zadatka se knjiži u zadatak od datuma završetka. Nijedna vrednost se ne objavljuje dok se zadatak ne izvrši 100 posto. 

Kada se izračunava zarađena vrednost, uzima se u obzir procenat napretka svakog zadatka. Prema pravilu zarade 0:100, za izračunavanje zarađene vrednosti na kraju tog perioda uzimaju se u obzir samo zadaci koji su završeni u datom periodu. Zarađena vrednost na projektu izračunava se za sve zadatke koji su završeni prilikom kreiranja grafikona. 

> [!NOTE] 
> Trenutno sistem za praćenje SAP nema strukture podataka za čuvanje istorijskih procenata napretka za svaki zadatak. Stoga se zarađena vrednost može prijaviti samo u trenutku obrade kocke. Redovno obrađujte kocku da biste ažurirali podatke o zarađenoj vrednosti koja se prikazuje u centru uloga. 

**Stvarna cena** Teorija EVM kaže da postavljanje stvarnih troškova predstavlja stopu po kojoj se novac troši na projekat. 

Transakcije koje se knjiže u projekat koriste se za postavljanje stvarne linije troškova. Troškovi su sažeti po datumima. Ovi podaci se zatim koriste za grafičko predstavljanje stvarnih troškova po nedelji ili mesecu na grafikonu zarađenih vrednosti.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Kako se koriste koncepti planirane vrednosti, ostvarene vrednosti i stvarnih troškova

**Varijansa rasporeda** Tokom planiranja kreirate predviđanje za rad na vremenskoj liniji. Stoga je planirana vrednost stopa kojom će planeri projekta misliti da će biti završen na projektu. Nakon što je projekat bude toku, posao je završen i projekat donosi vrednost. Upoređivanjem planirane vrednosti sa ostvarenom vrednošću, možete videti kako napreduje rad na projektu. Rezultat ovog poređenja naziva se varijansa rasporeda. 

Ako je planirana vrednost za period veća od ostvarene vrednosti, količina posla koji se obavlja na projektu je manja od planirane. Stoga projekat kasni sa rokom. Budući da su planirana vrednost i zarađena vrednost izraženi u novčanim vrednostima, vreme kašnjenja na projektu takođe dobija novčanu vrednost. 

Ako je planirana vrednost za period manja od ostvarene vrednosti, količina posla koji se obavlja na projektu je veća od planirane. Stoga je projekat ispred roka. Ovo vreme isporuke takođe dobija novčanu vrednost.

**Varijansa troškova** Budući da zarađena vrednost koristi cenu koštanja kao množilac, zarađena vrednost ukazuje na cenu posla koji se obavlja na projektu. Kako projekat napreduje, dnevnik transakcija daje evidenciju novca koji se stvarno troši na taj projekat. Upoređivanjem zarađene vrednosti sa stvarnim troškovima, možete da vidite količinu novca koji se troši u odnosu na zarađenu vrednost. Rezultat ovog poređenja naziva se varijansa troška. 

Ako je stvarni trošak koji se troši tokom određenog perioda veći od zarađene vrednosti, potrošeno je više novca nego što je zarađeno. Stoga je projekat preko budžeta. 

Ako je stvarni trošak koji se troši tokom određenog perioda manji od zarađene vrednosti, zarađeno je više novca nego što je potrošeno. Stoga je projekat ispod budžeta.

## <a name="wbs-templates"></a>SAP predlošci
Funkcionalnost SAP predložaka možete koristiti za kreiranje standardnih predložaka za projekte. Ako projekti koje nudi vaša kompanija uključuju puno ponovljivih poslova, trebalo bi da razmislite o kreiranju SAP predložaka. 

SAP predložak možete kreirati od SAP-a postojećeg projekta, tako da znanje i najbolje prakse koje ste prikupili tokom planiranja tog projekta možete ponovo koristiti na sličnim projektima u budućnosti. Međutim, ponekad možda neće imati smisla da sačuvate ceo SAP kao predložak. Zbog toga možete i da kreirate predloške iz delova SAP-a za projekat.

### <a name="saving-a-projects-wbs-as-a-template"></a>Čuvanje SAP projekta kao predloška

Kada kreirate predložak, možete ga uvesti u SAP novog projekta pod korenskim čvorom ili pod bilo koji zadatak u SAP-u projekta.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Uvoz SAP predloška u SAP projekta

Kada uvezete zadatke, zadaci u predlošku se organizuju na osnovu datuma početka zadatka pod kojim se uvoze. Tokom uvoza, relacije prethodnika sa zadacima predloška se koriste za izračunavanje datuma početka uvezenih zadataka. Standardni radni kalendar odredišnog projekta primenjuje se za izračunavanje datuma završetka uvezenih zadataka, tako da se zadržavaju radni dani i standardno radno vreme definisani u radnom kalendaru trenutnog projekta. 

Iznosi troškova i prodajne cene na linijama procene primenjuju se kako bi se zagarantovalo da cene koje su specifične za projekat ili ugovor o projektu imaju važeće datume.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Razlike između SAP-a projekta i SAP predloška

-   Zadaci u SAP predlošcima nemaju datume početka i datume završetka.

Radni i neradni dani nisu postavljeni za SAP predloške.

-   SAP predlošci uvek koriste kalendar zakazivanja koji je postavljen kao podrazumevani kalendar za sve projekte.

Podrazumevani kalendar zakazivanja koristi se samo za utvrđivanje radnog vremena u standardnom radnom danu.

-   Relacije sa prethodnikom se ne kopiraju u SAP predložak.

Budući da SAP predlošci nemaju datume, logika datuma početka koja se zasniva na datumu završetka prethodnika nije potrebna.

-   Linija procene troškova rada automatski se kreira kada se zadatak kreira u SAP predlošku. Prodajna cena i iznos troškova kopiraju se od izabranog radnika.

Troškovi i cene stavki mogu se kreirati ručno, baš kao i na SAP-u projekta.

-   Greške u planiranju prikazuju se kada postoje odstupanja od sledeće formule:

Napor = Broj resursa × Trajanje × Broj sati u standardnom radnom danu 

Sve greške rasporeda možete istovremeno ispraviti klikom na **Ispravi sve greške rasporeda**. 

Alternativno, možete i pojedinačno da ispravite greške u rasporedu klikom na ikonu upozorenja za svaki zadatak.



