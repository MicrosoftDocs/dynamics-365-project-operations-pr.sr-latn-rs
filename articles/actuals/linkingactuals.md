---
title: Povezivanje trenutnog stanja sa originalnim zapisima
description: Ova tema objašnjava kako se povezuje trenutno stanje sa originalnim zapisima kao što su stavka vremena, stavka troškova ili evidencija upotrebe materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fc49211f3c2c79e18f6dd18e9a687091793cad0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996763"
---
# <a name="link-actuals-to-original-records"></a>Povezivanje trenutnog stanja sa originalnim zapisima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_


U usluzi Dynamics 365 Project Operations, *poslovna transakcija* je apstraktni koncept koji ne predstavlja nijedan entitet. Međutim, neka uobičajena polja i procesi u entitetima su dizajnirani da koriste koncept poslovnih transakcija. Sledeći entiteti koriste ovaj koncept:

- Detalji stavke ponude
- Detalji predmeta ugovora
- Stavke procene
- Stavke u glavnoj knjizi
- Stvarne vrednosti

Od ovih entiteta, **Detalji stavke ponude**, **Detalji predmeta ugovora** i **Stavke procene** se mapiraju na fazu procene u životnom ciklusu projekta. **Stavke u glavnoj knjizi** i **entiteti trenutnog stanja** se mapiraju na fazu izvršavanja u životnom ciklusu projekta.

Project Operations prepoznaje zapise u ovih pet entiteta kao poslovne transakcije. Jedina razlika je u tome što se zapisi u entitetima koji su mapirani na fazu procene smatraju finansijskim predviđanjima, dok se zapisi u entitetima koji su mapirani na fazu izvršenja smatraju finansijskim činjenicama koje su se već dogodile.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije
Sledeći koncepti su jedinstveni za koncept poslovnih transakcija:

- Tip transakcije
- Klasa transakcije
- Poreklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Tip transakcije

Vrsta transakcije predstavlja trajanje i kontekst finansijskog uticaja na projekat. To se predstavlja skupom opcija sa sledećim podržanim vrednostima u usluzi Project Operations:

  - Cena
  - Ugovor za projekat
  - Nenaplaćena prodaja
  - Naplaćena prodaja
  - Prodaja između organizacija
  - Troškovi jedinice za obezbeđivanje resursa

### <a name="transaction-class"></a>Klasa transakcije

Klasa transakcije predstavlja različite vrste troškova koji se ostvaruju na projektima. To se predstavlja skupom opcija sa sledećim podržanim vrednostima u usluzi Project Operations:

  - Vreme
  - Trošak
  - Materijal
  - Naknada
  - Kontrolna tačka
  - Porez

**Kontrolna tačka** se obično koristi u poslovnoj logici za naplatu fiksne cene u usluzi Project Operations.

### <a name="transaction-origin"></a>Poreklo transakcije

**Poreklo transakcije** je entitet koji skladišti poreklo svake poslovne transakcije. Kako projekat bude u toku, svaka poslovna transakcija će dovesti do druge poslovne transakcije koja će zauzvrat kreirati drugu i tako dalje. Entitet porekla transakcije dizajniran je za skladištenje podataka o poreklu svake transakcije radi lakšeg izveštavanja i sledljivosti. 

### <a name="transaction-connection"></a>Veza transakcije

**Veza transakcije** je entitet koji skladišti relaciju između dve slične poslovne transakcije, kao što su troškovi i povezano trenutno stanje prodaje ili storniranja transakcija koja aktiviraju aktivnosti naplate kao što su potvrda fakture ili korekcije faktura.

**Poreklo transakcije** i **Veza transakcije** vam zajedno pomažu da pratite relacije između poslovnih transakcija i radnji koje su dovele do kreiranja određene poslovne transakcije.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Primer: Kako poreklo transakcije funkcioniše sa vezom transakcije

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u usluzi Project Operations.

> ![Obrada stavki vremena u životnom ciklusu usluge Project Service](media/basic-guide-17.png)
 
1. Prosleđivanje stavke vremena uzrokuje kreiranje dve stavke u glavnoj knjizi: jedne za troškove i jedne za nenaplaćenu prodaju.
2. Krajnje odobravanje stavke vremena kreira dva trenutna stanja: jedno za troškove i jedno za nenaplaćenu prodaju.
3. Kada se kreira faktura za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz trenutnog stanja nenaplaćene prodaje. 
4. Kada se potvrdi faktura, kreiraju se dva nova trenutna stanja: trenutno stanje storniranja nenaplaćene prodaje i trenutno stanje naplaćene prodaje.

Svaki od ovih događaja kreira zapis u entitetima **Poreklo transakcije** i **Veza transakcije**. Ovi novi zapisi pomažu u stvaranju istorije relacija između zapisa koji se kreiraju kroz stavku vremena, stavku u glavnoj knjizi, trenutno stanje i detalje stavki faktura.

Sledeća tabela prikazuje zapise u entitetu **Poreklo transakcije** za tok posla.

| Događaj                        | Poreklo                   | Tip porekla                       | Transakcija                       | Tip transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Prosleđivanje stavke vremena        | GUID zapisa stavke vremena   | Stavka vremena                        | GUID zapisa stavke u glavnoj knjizi (troškovi)   | Stavka u glavnoj knjizi             |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa stavke u glavnoj knjizi (prodaja)  | Stavka u glavnoj knjizi                      |                          |
| Odobrenje vremena                | GUID zapisa stavke u glavnoj knjizi | Stavka u glavnoj knjizi                      | GUID zapisa nenaplaćene prodaje        | Stvarno                   |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa nenaplaćene prodaje        | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID zapisa stvarnih vrednosti           | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa stvarnih vrednosti           | Stvarna vrednost                            |                          |
| Kreiranje fakture             | GUID zapisa stavke vremena   | Stavka vremena                        | GUID transakcije stavke fakture     | Transakcija stavke fakture |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID transakcije stavke fakture     | Transakcija stavke fakture          |                          |
| Potvrđivanje fakture         | GUID stavke fakture        | Stavka fakture                      | GUID zapisa naplaćene prodaje          | Stvarno                   |
| GUID fakture                 | Faktura                  | GUID zapisa naplaćene prodaje          | Stvarno                            |                          |
| GUID detalja stavke fakture     | Detalj stavke fakture      | GUID zapisa naplaćene prodaje          | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa naplaćene prodaje          | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID zapisa naplaćene prodaje          | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID storniranja nenaplaćene prodaje      | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID storniranja nenaplaćene prodaje      | Stvarno                            |                          |
| Korekcija radne verzije fakture     | GUID starog detalja stavke fakture             | Transakcija stavke fakture          | GUID ispravke detalja stavke fakture               | Transakcija stavke fakture |
| GUID stare stavke fakture                  | Stavka fakture             | GUID ispravke detalja stavke fakture               | Transakcija stavke fakture          |                          |
| GUID stare fakture             | Faktura                  | GUID ispravke detalja stavke fakture               | Transakcija stavke fakture          |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID ispravke detalja stavke fakture               | Transakcija stavke fakture          |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID ispravke detalja stavke fakture               | Transakcija stavke fakture          |                          |
| Potvrđena korekcija fakture | GUID starog detalja stavke fakture             | Transakcija stavke fakture          | GUID stornirane stvarne vrednosti naplaćene prodaje | Stvarno                   |
| GUID stare stavke fakture                  | Stavka fakture             | GUID stornirane stvarne vrednosti naplaćene prodaje | Stvarno                            |                          |
| GUID stare fakture             | Faktura                  | GUID stornirane stvarne vrednosti naplaćene prodaje | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID stornirane stvarne vrednosti naplaćene prodaje | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID stornirane stvarne vrednosti naplaćene prodaje | Stvarno                            |                          |
| GUID starog detalja stavke fakture                 | Transakcija stavke fakture | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID stare stavke fakture                  | Stavka fakture             | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID stare fakture             | Faktura                  | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID ispravke detalja stavke fakture          | Transakcija stavke fakture | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID ispravke stavke fakture           | Stavka fakture             | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |
| GUID ispravljene fakture      | Faktura                  | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarno                            |                          |

Sledeća tabela prikazuje zapise u entitetu **Veza transakcije** za tok posla.

| Događaj                          | Transakcija 1                 | Uloga 1. transakcije | Tip 1. transakcije           | 2. transakcija                | Uloga 2. transakcije | Tip 2. transakcije |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Prosleđivanje stavke vremena          | GUID stavke u glavnoj knjizi (prodaja)     | Nenaplaćena prodaja     | msdyn_journalline            | GUID stavke u glavnoj knjizi (troškovi)     | Troškovi               | msdyn_journalline  |
| Odobrenje vremena                  | GUID nenaplaćene stvarne vrednosti (prodaja)  | Nenaplaćena prodaja     | msdyn_actual                 | GUID stvarne vrednosti troškova (troškova)       | Troškovi               | msdyn_actual       |
| Kreiranje fakture               | GUID detalja stavke fakture      | Naplaćena prodaja       | msdyn_invoicelinetransaction | GUID nenaplaćene stvarne vrednosti prodaje   | Nenaplaćena prodaja     | msdyn_actual       |
| Potvrđivanje fakture           | GUID storniranih stvarnih vrednosti         | Storniranje          | msdyn_actual                 | GUID originalne nenaplaćene prodaje | Originalno           | msdyn_actual       |
| GUID naplaćene prodaje              | Naplaćena prodaja                  | msdyn_actual       | GUID nenaplaćene stvarne vrednosti prodaje   | Nenaplaćena prodaja               | msdyn_actual       |                    |
| Korekcija radne verzije fakture       | GUID transakcije stavke fakture | Zamena          | msdyn_invoicelinetransaction | GUID naplaćene prodaje            | Originalno           | msdyn_actual       |
| Potvrđivanje korekcije fakture     | GUID storniranja naplaćene prodaje    | Storniranje          | msdyn_actual                 | GUID naplaćene prodaje            | Originalno           | msdyn_actual       |
| GUID nove nenaplaćene stvarne vrednosti prodaje | Zamena                     | msdyn_actual       | GUID naplaćene prodaje            | Originalno                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
