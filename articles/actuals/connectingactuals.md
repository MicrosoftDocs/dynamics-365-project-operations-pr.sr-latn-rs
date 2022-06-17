---
title: Veze sa transakcijama – povezivanje stvarnih vrednosti različitih tipova transakcija
description: Ovaj članak sadrži objašnjenja o tome kako se veza transakcije koristi za povezivanje stvarnih vrsta različitih tipova radi praćenja profitabilnosti, zaostalih naplata i obračuna neodovršenih prihoda.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926103"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Veze sa transakcijama – povezivanje stvarnih vrednosti različitih tipova transakcija

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Zapisi veze transakcije se kreiraju da bi se povezale stvarne vrste različitih tipova dok se vreme, troškovi ili korišćenje materijala premeštaju u svom životnom ciklusu iz faze ponude ili pre prodaje u fazu ugovora, odobrenja i/ili opoziva, fakturisanja i potencijalnog kreditnog ili korektivnog fakturisanja.

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u usluzi Project Operations.

> ![Obrada vremenskih stavki u operacijama projekta.](media/basic-guide-17.png)

Obrada vremenskih stavki u životnom ciklusu projekta "Operacije projekta" sledi ove korake: 

1. Prosleđivanje stavke vremena dovodi do kreiranja dva reda naloga: jedan za trošak i jedan za neosloženu prodaju. 
2. Eventualno odobravanje stavke vremena dovodi do kreiranja dve stvarne stavke: jedne za trošak i druge za neželjenu prodaju. Ove 2 stvarne stvari su povezane pomoću transakcionih veza.
3. Kada korisnik kreira fakturu za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz stvarne vrednosti nenaplaćene prodaje.
4. Kada je faktura potvrđena, ovo kreira dve nove stvarne stavke: storniranu vrednost prodaje i stvarnu fakturisanu prodaju. Neželjena zamena prodaje i originalna neželjena prodaja su povezani sa storniranjem veza transakcija. Fakturisana prodaja i originalne neželjene prodajne stvarne stavke takođe su povezane da bi se veze između onoga što je nekada bilo zaostalo ili rada u toku (PUT) prihoda prikazuju sa onim što je sada fakturisani prihod.   

Svaki događaj u toku posla za obradu pokreće kreiranje zapisa u tabeli "Transakcija **veze** ". Ovo pomaže u izradi praćenja odnosi zapisa koji se kreiraju putem stavke vremena, reda naloga, stvarnih i detalja reda fakture.

Sledeća tabela prikazuje zapise u entitetu **veze transakcije** za prethodni tok posla.

|Događaj                   |1. transakcija                 |Uloga 1. transakcije |Tip 1. transakcije       |2. transakcija          |Uloga 2. transakcije |Tip 2. transakcije |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Prosleđivanje stavke vremena   |GUID stavke u glavnoj knjizi (prodaja)     |Nenaplaćena prodaja |msdyn_journalline            |GUID stavke u glavnoj knjizi (troškovi)     |Troškovi            |msdyn_journalline  |
|Odobrenje vremena           |GUID nenaplaćene stvarne vrednosti (prodaja)  |Nenaplaćena prodaja |msdyn_actual                 |GUID stvarne vrednosti troškova (troškova)       |Troškovi            |msdyn_actual       |
|Kreiranje fakture        |GUID detalja stavke fakture      |Naplaćena prodaja   |msdyn_invoicelinetransaction |GUID nenaplaćene stvarne vrednosti prodaje   |Nenaplaćena prodaja  |msdyn_actual       |
|Potvrđivanje fakture    |GUID storniranih stvarnih vrednosti         |Storniranje      |msdyn_actual                 |GUID originalne nenaplaćene prodaje |Originalno        |msdyn_actual       |
|                        |GUID naplaćene prodaje             |Naplaćena prodaja   |msdyn_actual                 |GUID nenaplaćene stvarne vrednosti prodaje   |Nenaplaćena prodaja  |msdyn_actual       |
|Korekcija radne verzije fakture |GUID transakcije stavke fakture|Zamena      |msdyn_invoicelinetransaction |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |
|Potvrđivanje korekcije fakture|GUID storniranja naplaćene prodaje  |Storniranje      |msdyn_actual                 |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |
|                        |Novi GUID neželjene prodaje |Zamena            |msdyn_actual                 |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |


Sledeća ilustracija prikazuje veze koje su kreirane između različitih tipova stvarnih stvari na različitim događajima koristeći primer stavki vremena u operacijama projekta.

> ![Kako su stvarne vrste različitih tipova međusobno povezane u operacijama projekta.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
