---
title: Poslovne transakcije u usluzi Project Operations
description: Ovaj članak pruža pregled koncepta poslovnih transakcija u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923297"
---
# <a name="business-transactions-in-project-operations"></a>Poslovne transakcije u usluzi Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U aplikaciji Microsoft Dynamics 365 Project Operations, *poslovna transakcija* je apstraktni koncept koji ne predstavlja nijedan entitet. Međutim, neka uobičajena polja i procesi u entitetima su dizajnirani da koriste koncept poslovnih transakcija. Sledeći entiteti koriste ovu apstrakciju:

- Detalji stavke ponude
- Detalji predmeta ugovora
- Stavke procene
- Stavke u glavnoj knjizi
- Stvarne vrednosti

Od ovih entiteta, Detalji stavke ponude, Detalji predmeta ugovora i Stavke procene se mapiraju na *fazu procene* u životnom ciklusu projekta. Stavke u glavnoj knjizi i entiteti trenutnog stanja se mapiraju na *fazu izvršavanja* u životnom ciklusu projekta.

Project Operations tretira zapise u svih ovih pet entiteta kao poslovne transakcije. Jedina razlika je u tome što se zapisi u entitetima koji su mapirani na fazu procene (Detalji reda ponude, detalji predmeta ugovora i redovi procene) smatraju *finansijskim predviđanjima*, dok se zapisi u entitetima koji su mapirani na fazu izvršenja (Stavke u glavnoj knjizi i Stvarne vrednosti) smatraju *finansijskim činjenicama* koje su se već dogodile.

Više informacija potražite u članku [Procene](../project-management/estimating-projects-overview.md) i [Stvarne vrednosti](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije

Sledeći koncepti su jedinstveni za koncept poslovnih transakcija:

- Tip transakcije
- Klasa transakcije
- Poreklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Tip transakcije

Vrsta transakcije predstavlja trajanje i kontekst finansijskog uticaja na projekat. To je definisano skupom opcija sa sledećim podržanim vrednostima u usluzi Project Operations:

- Cena
- Ugovor za projekat
- Nenaplaćena prodaja
- Naplaćena prodaja
- Prodaja između organizacija
- Troškovi jedinice za obezbeđivanje resursa

### <a name="transaction-class"></a>Klasa transakcije

Klasa transakcije predstavlja različite vrste troškova koji se ostvaruju na projektima. To je definisano skupom opcija sa sledećim podržanim vrednostima u usluzi Project Operations:

- Vreme
- Trošak
- Materijal
- Naknada
- Kontrolna tačka
- Porez

> [!NOTE]
> Vrednost **Kontrolne tačke** se obično koristi u poslovnoj logici za naplatu fiksne cene u usluzi Project Operations.

### <a name="transaction-origin"></a>Poreklo transakcije

Poreklo transakcije je entitet koji skladišti poreklo svake poslovne transakcije radi lakšeg izveštavanja i sledljivosti. Kada projekat počinje, svaka poslovna transakcija kreira još jednu poslovnu transakciju, koja će zauzvrat kreirati još jednu poslovnu transakciju i tako dalje.

### <a name="transaction-connection"></a>Veza transakcije

Veza transakcije je stavka koji skladišti odnos između dve slične poslovne transakcije, kao što su troškovi i pripadajuće stvarne vrednosti prodaje ili vraćanje transakcija koje aktiviraju aktivnosti naplate kao što su potvrda fakture ili korekcije fakture.

Entiteti Poreklo transakcije i Veza transakcije vam zajedno pomažu da pratite odnose između poslovnih transakcija i radnji koje su dovele do kreiranja određene poslovne transakcije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
