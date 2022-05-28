---
title: Poreklo transakcije - Povezivanje stvarnih podataka sa njihovim izvorom
description: Ova tema objašnjava kako se koncept porekla transakcije koristi za povezivanje stvarnih podataka sa originalnim izvornim zapisima, kao što su stavka vremena, stavka troškova ili evidencije korišćenja materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584843"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Poreklo transakcije - Povezivanje stvarnih podataka sa njihovim izvorom

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Zapisi o poreklu transakcije se kreiraju da bi se povezale stvarne vrednosti sa njihovim izvorom, kao što su stavke vremena, stavke troškova, evidencije korišćenja materijala i fakture projekta.

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u usluzi Project Operations.

> ![Obrada celih vremena u operacijama projekta.](media/basic-guide-17.png)
 
1. Prosleđivanje stavke vremena dovodi do kreiranja dva reda naloga: jedan za trošak i jedan za neosloženu prodaju.
2. Eventualno odobravanje stavke vremena dovodi do kreiranja dve stvarne stavke: jedne za trošak i druge za neželjenu prodaju.
3. Kada korisnik kreira fakturu za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz stvarne vrednosti nenaplaćene prodaje.
4. Kada je faktura potvrđena, kreiraju se dve nove stvarne vrednosti: storniranje nenaplaćene prodaje i stvarna vrednost naplaćene prodaje.

Svaki događaj u ovom toku posla za obradu pokreće kreiranje zapisa u entitetu porekla transakcije da bi se izgradio trag odnosi između ovih zapisa koji se kreiraju putem stavke vremena, reda naloga, stvarnih i detalja reda fakture.

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
| GUID ispravljene fakture      | Faktura                  | GUID nove nenaplaćene stvarne vrednosti prodaje    | Stvarna vrednost                            |                          |


Sledeća ilustracija prikazuje veze koje su kreirane između stvarnih i njihovih izvora na različitim događajima koristeći primer stavki vremena u operacijama projekta.

> ![Kako su stvarni povezani sa izvornim zapisima u operacijama projekta.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
