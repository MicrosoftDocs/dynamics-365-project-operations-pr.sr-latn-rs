---
title: Poreklo transakcija – povezivanje stvarnih vrednosti sa njihovim izvorom
description: Ovaj članak objašnjava kako se koncept porekla transakcija koristi za povezivanje stvarnih vrednosti sa originalnim zapisima izvora kao što su stavka vremena, stavka troškova ili evidencija korišćenja materijala.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921319"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Poreklo transakcija – povezivanje stvarnih vrednosti sa njihovim izvorom

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Zapisi o poreklu transakcije se kreiraju da bi se povezale stvarne vrednosti sa njihovim izvorom, kao što su stavke vremena, stavke troškova, evidencije korišćenja materijala i fakture projekta.

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u usluzi Project Operations.

> ![Obrada stavki vremena u usluzi Project Operations.](media/basic-guide-17.png)
 
1. Prosleđivanje stavke vremena uzrokuje kreiranje dve stavke u glavnoj knjizi: jedne za troškove i jedne za nenaplaćenu prodaju.
2. Krajnje odobravanje stavke vremena uzrokuje kreiranje dve stvarne vrednosti: jedne za troškove i jedne za nenaplaćenu prodaju.
3. Kada korisnik kreira fakturu za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz stvarne vrednosti nenaplaćene prodaje.
4. Kada je faktura potvrđena, kreiraju se dve nove stvarne vrednosti: storniranje nenaplaćene prodaje i stvarna vrednost naplaćene prodaje.

Svaki događaj u ovom toku posla obrade pokreće kreiranje zapisa u entitetima Poreklo transakcije da bi mogli da se prate odnosi između ovih zapisa koji su kreirani u detaljima stavke vremena, stavke u glavnoj knjizi, stvarne vrednosti i stavke fakture.

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


Sledeća ilustracija prikazuje veze koje su kreirane između stvarnih vrednosti i njihovih izvora na različitim događajima koristeći primer stavki vremena u usluzi Project Operations.

> ![Kako su stvarne vrednosti povezane sa izvornim zapisima u usluzi Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
