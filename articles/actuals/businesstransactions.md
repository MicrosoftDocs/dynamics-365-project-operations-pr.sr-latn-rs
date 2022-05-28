---
title: Poslovne transakcije u projektno poslovanje
description: Ova tema pruža pregled koncepta poslovnih transakcija u korporaciji Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582221"
---
# <a name="business-transactions-in-project-operations"></a>Poslovne transakcije u projektno poslovanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U korporaciji Dynamics 365 Project Operations Microsoft *,* poslovna transakcija je apstraktni koncept koji ne predstavlja nijedan entitet. Međutim, neka uobičajena polja i procesi u entitetima su dizajnirani da koriste koncept poslovnih transakcija. Sledeći entiteti koriste ovu apstrakciju:

- Detalji stavke ponude
- Detalji predmeta ugovora
- Stavke procene
- Stavke u glavnoj knjizi
- Stvarne vrednosti

Od ovih entiteta, detalji reda ponude, detalji reda ugovora i redovi procene mapirani su u *fazu* procene u životnom ciklusu projekta. Redovi naloga i entiteti stvarnih podataka mapirani su u fazu *izvršavanja* u životnom ciklusu projekta.

Operacije projekta tretiraju zapise u svih pet ovih entiteta kao poslovne transakcije. Jedina razlika je u tome što se zapisi u entitetima koji su mapirani u fazu procene (detalji reda ponude, detalji reda ugovora i redovi procene) *smatraju* finansijskim predviđanjima, dok se zapisi u entitetima koji su mapirani u fazu izvršavanja (redovi naloga i stvarni podaci) *smatraju* finansijskim činjenicama do kojih je već došlo.

Više informacija potražite u članku [Procene](../project-management/estimating-projects-overview.md) i [Stvarne vrednosti](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepti koji su jedinstveni za poslovne transakcije

Sledeći koncepti su jedinstveni za koncept poslovnih transakcija:

- Tip transakcije
- Klasa transakcije
- Poreklo transakcije
- Veza transakcije

### <a name="transaction-type"></a>Tip transakcije

Vrsta transakcije predstavlja trajanje i kontekst finansijskog uticaja na projekat. Definiše ga program koji skup opcija podržane vrednosti u operacijama projekta:

- Cena
- Ugovor za projekat
- Nenaplaćena prodaja
- Naplaćena prodaja
- Prodaja između organizacija
- Troškovi jedinice za obezbeđivanje resursa

### <a name="transaction-class"></a>Klasa transakcije

Klasa transakcije predstavlja različite vrste troškova koji se ostvaruju na projektima. Definiše ga program koji skup opcija podržane vrednosti u operacijama projekta:

- Vreme
- Trošak
- Materijal
- Naknada
- Kontrolna tačka
- Porez

> [!NOTE]
> Vrednost **Milestone** obično koristi poslovna logika za naplatu fiksne cene u operacijama projekta.

### <a name="transaction-origin"></a>Poreklo transakcije

Poreklo transakcije je entitet koji skladišti poreklo svake poslovne transakcije da bi pomogao u izveštavanju i praćenju. Sa početkom izvršenja projekta, svaka poslovna transakcija kreira drugu poslovnu transakciju koja će zauzvrat kreirati drugu poslovnu transakciju i tako dalje.

### <a name="transaction-connection"></a>Veza transakcije

Veza transakcija je entitet koji skladišti odnos između dve slične poslovne transakcije, kao što su troškovi i srodne stvarne prodaje ili storniranje transakcija koje su izazvane aktivnostima fakturisanja kao što su potvrda fakture ili korekcija fakture.

Zajedno, entiteti veza "Poreklo transakcije" i "Transakcija" vam pomažu odnosi praćenje između poslovnih transakcija i radnji koje su prouzrokovale kreiranja određene poslovne transakcije.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
