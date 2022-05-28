---
title: Isključivanje dimenzije za određivanje cena
description: Ova tema pruža informacije o isključivanju dimenzija za određivanje cena.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cba1f9915087f7910a9aa93378cb861983ca36ab
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600345"
---
# <a name="turning-off-a-pricing-dimension"></a>Isključivanje dimenzije za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možda ćete morati da pregledate i ažurirate svoju strategiju određivanja cena svakih nekoliko godina. Sve ispravke koje unesete mogu zahtevati da isključite postojeću dimenziju za određivanje cena i kreirate novu. Na primer, možda ste prethodno određivali cenu po **ulozi**, ali ste sada odlučili da to radite prema **radnom iskustvu**. Ovo može zahtevati da isključite dimenziju za određivanje cena **Uloga** i da kreirate **Radno iskustvo** kao novu dimenziju za određivanje cena. 

Dimenzija za određivanje cena, bez obzira na to da li je unapred definisana ili prilagođena, može se isključiti ako polja **Primenljivo na troškove** i **Primenljivo na prodaju** u okviru dimenzije za određivanje cena podesite na **Ne**.

Međutim, kada to učinite, možda ćete dobiti poruku o grešci, **Dimenzija za određivanje cene se ne može ažurirati ili izbrisati ako postoje povezani zapisi cena.**

![Greška poslovnog procesa je moguća kada isključujete dimenziju za određivanje cena.](media/Business-Process-Error.png)

Ova poruka o grešci ukazuje na to da postoje zapisi cena koji su prethodno podešeni za dimenziju koja je isključena. Sve zapise **Cena uloge** i **Provizija na cenu uloge** koji se odnose na dimenziju morate izbrisati pre nego što se primenjivost dimenzije podesi na **Ne**. Ovo pravilo primenjuje se na unapred definisane dimenzije za određivanje cena i sve prilagođene dimenzije za određivanje cena koje ste možda kreirali. Razlog ove validacije je što svaki zapis **Cena uloge** mora da ima jedinstvenu kombinaciju dimenzija. Na primer, u cenovniku pod nazivom **Stope troška u SAD za 2018**, imate sledeće redove **Cena uloge**. 

| Standardna pozicija         | Organizaciona jedinica    |Jedinica   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sistema|Contoso US|Hour| 100.|USD|
| Viši inženjer sistema|Contoso US|Hour| 150| USD|


Kada isključite polje **Standardna pozicija** kao dimenziju za određivanje cena, a mehanizam za određivanje cena pretražuje cenu, koristiće samo vrednost **Organizaciona jedinica** iz konteksta unosa. Ako je **Organizaciona jedinica** konteksta unosa „Contoso US“, rezultat će biti neodređen jer će se oba reda podudarati. Da biste izbegli ovaj scenario, kada kreirate zapise **Cena uloge**, sistem proverava da li je kombinacija dimenzija jedinstvena. Ako je dimenzija isključena nakon kreiranja zapisa **Cena uloge**, ovo ograničenje može da se prekrši. Zbog toga je neophodno da pre isključivanja dimenzije izbrišete sve redove **Cena uloge** i **Provizija na cenu uloge** u kojima je ta vrednost dimenzije popunjena.


[!INCLUDE[footer-include](../includes/footer-banner.md)]