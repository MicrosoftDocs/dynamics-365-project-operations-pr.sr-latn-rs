---
title: Isključivanje dimenzije za određivanje cena
description: Ova tema pruža informacije o isključivanju dimenzija za određivanje cena.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1a7c91ef70b1dd3697f6a8b5044c6ad4a14c4e74
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083676"
---
# <a name="turning-off-a-pricing-dimension"></a>Isključivanje dimenzije za određivanje cena

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Možda ćete morati da pregledate i ažurirate svoju strategiju određivanja cena svakih nekoliko godina. Sve ispravke koje unesete mogu zahtevati da isključite postojeću dimenziju za određivanje cena i kreirate novu. Na primer, možda ste prethodno određivali cenu po **ulozi** , ali ste sada odlučili da to radite prema **radnom iskustvu**. Ovo može zahtevati da isključite dimenziju za određivanje cena **Uloga** i da kreirate **Radno iskustvo** kao novu dimenziju za određivanje cena. 

Dimenzija za određivanje cena, bez obzira na to da li je unapred definisana ili prilagođena, može se isključiti ako polja **Primenljivo na troškove** i **Primenljivo na prodaju** u okviru dimenzije za određivanje cena podesite na **Ne**.

Međutim, kada to učinite, možda ćete dobiti poruku o grešci, **Dimenzija za određivanje cene se ne može ažurirati ili izbrisati ako postoje povezani zapisi cena.**

Ova poruka o grešci ukazuje na to da postoje zapisi cena koji su prethodno podešeni za dimenziju koja je isključena. Sve zapise **Cena uloge** i **Provizija na cenu uloge** koji se odnose na dimenziju morate izbrisati pre nego što se primenjivost dimenzije podesi na **Ne**. Ovo pravilo primenjuje se na unapred definisane dimenzije za određivanje cena i sve prilagođene dimenzije za određivanje cena koje ste možda kreirali. Razlog ove validacije je što svaki zapis **Cena uloge** mora da ima jedinstvenu kombinaciju dimenzija. Na primer, u cenovniku pod nazivom **Stope troška u SAD za 2018** , imate sledeće redove **Cena uloge**. 

| Standardna pozicija         | Organizaciona jedinica    |Jedinica   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sistema|Contoso US|Hour| 100.|USD|
| Viši inženjer sistema|Contoso US|Hour| 150| USD|


Kada isključite polje **Standardna pozicija** kao dimenziju za određivanje cena, a mehanizam za određivanje cena pretražuje cenu, koristiće samo vrednost **Organizaciona jedinica** iz konteksta unosa. Ako je **Organizaciona jedinica** konteksta unosa „Contoso US“, rezultat će biti neodređen jer će se oba reda podudarati. Da biste izbegli ovaj scenario, kada kreirate zapise **Cena uloge** , sistem proverava da li je kombinacija dimenzija jedinstvena. Ako je dimenzija isključena nakon kreiranja zapisa **Cena uloge** , ovo ograničenje može da se prekrši. Zbog toga je neophodno da pre isključivanja dimenzije izbrišete sve redove **Cena uloge** i **Provizija na cenu uloge** u kojima je ta vrednost dimenzije popunjena.
