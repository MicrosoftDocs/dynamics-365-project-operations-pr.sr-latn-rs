---
title: Veze sa transakcijama – povezivanje stvarnih vrednosti različitih tipova transakcija
description: Ovaj članak sadrži objašnjenja o tome kako se veza transakcije koristi za povezivanje stvarnih vrednosti različitih vrsta radi praćenja profitabilnosti, zaostalih naplata i izračunavanja nenaplaćenih prihoda.
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

Zapisi veze transakcije se kreiraju da bi se povezale stvarne vrednosti različitih tipova dok se vreme, troškovi ili korišćenje materijala premeštaju u svom životnom ciklusu iz faze ponude ili pretprodaje u fazu ugovora, odobrenja i/ili opoziva, fakturisanja i potencijalnog kreditnog ili korektivnog fakturisanja.

Sledeći primer prikazuje tipičnu obradu stavki vremena u životnom ciklusu projekta u usluzi Project Operations.

> ![Obrada stavki vremena u usluzi Project Operations.](media/basic-guide-17.png)

Obrada stavki vremena u životnom ciklusu projekta u usluzi Project Operations prati ove korake: 

1. Prosleđivanje stavke vremena uzrokuje kreiranje dve stavke u glavnoj knjizi: jedne za troškove i jedne za nenaplaćenu prodaju. 
2. Krajnje odobravanje stavke vremena uzrokuje kreiranje dve stvarne vrednosti: jedne za troškove i jedne za nenaplaćenu prodaju. Ove 2 stvarne vrednosti su povezane pomoću transakcionih veza.
3. Kada korisnik kreira fakturu za projekat, transakcija stavke fakture se kreira korišćenjem podataka iz stvarne vrednosti nenaplaćene prodaje.
4. Kada je faktura potvrđena, to kreira dve nove stvarne vrednosti: storniranje nenaplaćene prodaje i stvarna vrednost naplaćene prodaje. Stornirana nenaplaćena prodaja i originalna nenaplaćena prodaja su povezane korišćenjem veza transakcija storniranja. Stvarne vrednosti naplaćene prodaje i originalne nenaplaćene prodaje takođe su povezane da bi se veze između onoga što je nekada bilo zaostali ili prihod rada u toku (WIP) prikazivali sa onim što je sada fakturisani prihod.   

Svaki događaj u toku posla obrade pokreće kreiranje zapisa u tabeli **Veza transakcije**. Time pomažete pravljenje praćenja relacija između zapisa koji se kreiraju kroz stavku vremena, stavku u glavnoj knjizi, stvarnu vrednosti i detalje stavki faktura.

Sledeća tabela prikazuje zapise u entitetu **Veza transakcije** za prethodni tok posla.

|Događaj                   |1. transakcija                 |Uloga 1. transakcije |Tip 1. transakcije       |2. transakcija          |Uloga 2. transakcije |Tip 2. transakcije |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Prosleđivanje stavke vremena   |GUID stavke u glavnoj knjizi (prodaja)     |Nenaplaćena prodaja |msdyn_journalline            |GUID stavke u glavnoj knjizi (troškovi)     |Troškovi            |msdyn_journalline  |
|Odobrenje vremena           |GUID nenaplaćene stvarne vrednosti (prodaja)  |Nenaplaćena prodaja |msdyn_actual                 |GUID stvarne vrednosti troškova (troškova)       |Troškovi            |msdyn_actual       |
|Kreiranje fakture        |GUID detalja stavke fakture      |Naplaćena prodaja   |msdyn_invoicelinetransaction |GUID nenaplaćene stvarne vrednosti prodaje   |Nenaplaćena prodaja  |msdyn_actual       |
|Potvrđivanje fakture    |GUID storniranih stvarnih vrednosti         |Storniranje      |msdyn_actual                 |GUID originalne nenaplaćene prodaje |Originalno        |msdyn_actual       |
|                        |GUID naplaćene prodaje             |Naplaćena prodaja   |msdyn_actual                 |GUID nenaplaćene stvarne vrednosti prodaje   |Nenaplaćena prodaja  |msdyn_actual       |
|Korekcija radne verzije fakture |GUID transakcije stavke fakture|Zamena      |msdyn_invoicelinetransaction |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |
|Potvrđivanje korekcije fakture|GUID storniranja naplaćene prodaje  |Storniranje      |msdyn_actual                 |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |
|                        |GUID nove nenaplaćene prodaje |Zamena            |msdyn_actual                 |GUID naplaćene prodaje            |Originalno        |msdyn_actual       |


Sledeća ilustracija prikazuje veze koje su kreirane između različitih vrsta stvarnih vrednosti i njihovih izvora na različitim događajima koristeći primer stavki vremena u usluzi Project Operations.

> ![Kako su stvarne vrednosti različitih vrsta međusobno povezane u Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
