---
title: Poslovne transakcije
description: Ova tema pruža informacije o poslovnim transakcijama.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 68506142c5cd046806bc085f297ac928b0c94440
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291231"
---
# <a name="business-transactions"></a>Poslovne transakcije

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U aplikaciji Dynamics 365 Project Service Automation *poslovna transakcija* je apstraktni koncept koji ne predstavlja nijedan entitet. Međutim, neka uobičajena polja i procesi u entitetima su dizajnirani da koriste koncept poslovnih transakcija. Sledeći entiteti koriste ovu apstrakciju:

- Detalji stavke ponude
- Detalji predmeta ugovora
- Stavke procene
- Stavke u glavnoj knjizi
- Stvarne vrednosti

Od ovih entiteta, Detalji stavke ponude, Detalji predmeta ugovora i Stavke procene se mapiraju na fazu procene u životnom ciklusu projekta. Stavke u glavnoj knjizi i entiteti stvarnih vrednosti se mapiraju na fazu izvršavanja u životnom ciklusu projekta.

PSA tretira zapise u ovih pet eititeta kao poslovne transakcije. Jedina razlika je u tome što se zapisi u entitetima koji su mapirani na fazu procene smatraju finansijskim procenama, dok se zapisi u entitetima koji su mapirani na fazu izvršenja smatraju finansijskim činjenicama koje su se već dogodile.

Više informacija potražite u članku [Procene](estimates.md) i [Stvarne vrednosti](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije
Sledeći koncepti su jedinstveni za koncept poslovnih transakcija:

- Tip transakcije
- Klasa transakcije
- Poreklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Tip transakcije

Vrsta transakcije predstavlja trajanje i kontekst finansijskog uticaja na projekat. Predstavlja je skup opcija sa sledećim podržanim vrednosti u aplikaciji PSA:
- Troškovi
- Ugovor za projekat
- Nenaplaćena prodaja
- Naplaćena prodaja
- Prodaja između organizacija
- Troškovi jedinice za obezbeđivanje resursa

### <a name="transaction-class"></a>Klasa transakcije

Klasa transakcije predstavlja različite vrste troškova koji se ostvaruju na projektima. Predstavlja je skup opcija sa sledećim podržanim vrednosti u aplikaciji PSA:

- Time
- Trošak
- Materijal
- Naknada
- Kontrolna tačka
- Porez

Vrednost **Kontrolna tačka** obično koristi poslovna logika za naplatu fiksne cene u aplikaciji PSA.

### <a name="transaction-origin"></a>Poreklo transakcije

Poreklo transakcije je entitet koji skladišti poreklo svake poslovne transakcije. Kako se izvršava projekat, svaka poslovna transakcija će stvoriti još jednu poslovnu transakciju, koja će zauzvrat stvoriti drugu, i tako dalje. Entitet porekla transakcije dizajniran je za skladištenje podataka o poreklu svake transakcije, kako bi se olakšalo izveštavanje i praćenje entiteta. 

### <a name="transaction-connection"></a>Veza transakcije

Veza transakcije je entitet koji skladišti odnos između dve slične poslovne transakcije, kao što su troškovi i pripadajuće stvarne vrednosti prodaje ili storniranje transakcija koje aktiviraju aktivnosti naplate kao što su potvrda fakture ili korekcije faktura.

Poreklo transakcije i Veza transakcije vam zajedno pomažu da pratite odnose između poslovnih transakcija i radnji koje su dovele do kreiranja određene poslovne transakcije.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Primer: Kako poreklo transakcije funkcioniše sa vezom transakcije

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u aplikaciji PSA.

> ![Obrada stavki vremena u životnom ciklusu usluge Project Service](media/basic-guide-17.png)
 
1. Prosleđivanje stavke vremena uzrokuje kreiranje dve stavke u glavnoj knjizi: jedne za troškove i jedne za nenaplaćenu prodaju.
2. Krajnje odobravanje stavke vremena uzrokuje kreiranje dve stvarne vrednosti: jedne za troškove i jedne za nenaplaćenu prodaju.
3. Kada korisnik kreira fakturu za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz stvarne vrednosti nenaplaćene prodaje. 
4. Kada je faktura potvrđena, kreiraju se dve nove stvarne vrednosti: storniranje nenaplaćene prodaje i stvarna vrednost naplaćene prodaje.

Svaki od ovih događaja pokreće kreiranje zapisa u entitetima Poreklo transakcije i Veza transakcije da bi mogli da se prate odnosi između ovih zapisa koji su kreirani u detaljima stavke vremena, stavke u glavnoj knjizi, stvarnih vrednosti i stavke fakture.

Sledeća tabela prikazuje zapise u entitetu Poreklo transakcije za prethodni tok posla.

| Događaj                        | Poreklo                   | Tip porekla                       | Transakcija                       | Tip transakcije         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Prosleđivanje stavke vremena        | GUID zapisa stavke vremena   | Stavka vremena                        | GUID zapisa stavke u glavnoj knjizi (troškovi)   | Stavka u glavnoj knjizi             |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa stavke u glavnoj knjizi (prodaja)  | Stavka u glavnoj knjizi                      |                          |
| Odobrenje vremena                | GUID zapisa stavke u glavnoj knjizi | Stavka u glavnoj knjizi                      | GUID zapisa nenaplaćene prodaje        | Stvarno                   |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa nenaplaćene prodaje        | Stvarno                            |                          |
| GUID zapisa stavke u glavnoj knjizi     | Stavka u glavnoj knjizi             | GUID zapisa stvarnih vrednosti           | Stvarno                            |                          |
| GUID zapisa stavke vremena       | Stavka vremena               | GUID zapisa stvarnih vrednosti           | Stvarno                            |                          |
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

Sledeća tabela prikazuje zapise u entitetu Veza transakcije za prethodni tok posla.

| Događaj                          | 1. transakcija                 | Uloga 1. transakcije | Tip 1. transakcije           | 2. transakcija                | Uloga 2. transakcije | Tip 2. transakcije |
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