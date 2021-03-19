---
title: Isključivanje dimenzije za određivanje cena
description: Ova tema pokazuje kako se podešavaju dimenzije za određivanje cena u rešenju Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 6e4b80b9c4b1b0f57d04079c9d2f84051b451d29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281855"
---
# <a name="turn-off-a-pricing-dimension"></a>Isključivanje dimenzije za određivanje cena

[!include [banner](../includes/psa-now-project-operations.md)]

Možda ćete morati da pregledate i ažurirate svoju strategiju određivanja cena svakih nekoliko godina. Sve ispravke koje unesete mogu zahtevati da isključite postojeću dimenziju za određivanje cena i kreirate novu. Na primer, možda ste prethodno određivali cenu po **ulozi**, ali ste sada odlučili da to radite prema **radnom iskustvu**. Ovo može zahtevati da isključite dimenziju za određivanje cena **Uloga** i da kreirate **Radno iskustvo** kao novu dimenziju za određivanje cena. 

Dimenzija za određivanje cena, bez obzira na to da li je unapred definisana ili prilagođena, može se isključiti ako polja **Primenljivo na troškove** i **Primenljivo na prodaju** u okviru dimenzije za određivanje cena podesite na **Ne**.

Međutim, kada to uradite, možda ćete dobiti sledeću poruku o grešci.

![Greška poslovnog procesa je moguća kada isključujete dimenziju za određivanje cena](media/Business-Process-Error.png)


Ova poruka o grešci ukazuje na to da postoje zapisi cena koji su prethodno podešeni za dimenziju koja je isključena. Sve zapise **Cena uloge** i **Provizija na cenu uloge** koji se odnose na dimenziju morate izbrisati pre nego što se primenjivost dimenzije podesi na **Ne**. Ovo pravilo primenjuje se na unapred definisane dimenzije za određivanje cena i sve prilagođene dimenzije za određivanje cena koje ste možda kreirali. Razlog ove validacije je što Project Service ima ograničenje da svaki zapis **Cena uloge** mora da ima jedinstvenu kombinaciju dimenzija. Na primer, u cenovniku pod nazivom **Stope troška u SAD za 2018**, imate sledeće redove **Cena uloge**. 

| Standardna pozicija         | Organizaciona jedinica    |Jedinica   |Cena  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Inženjer sistema|Contoso US|Hour| 100.|USD|
| Viši inženjer sistema|Contoso US|Hour| 150| USD|


Kada isključite polje **Standardna pozicija** kao dimenziju za određivanje cena, a Project Service mehanizam za određivanje cena pretražuje cenu, koristiće samo vrednost **Organizaciona jedinica** iz konteksta unosa. Ako je **Organizaciona jedinica** konteksta unosa „Contoso US“, rezultat će biti neodređen jer će se oba reda podudarati. Da biste izbegli ovaj scenario, kada kreirate zapise **Cena uloge**, Project Service proverava da li je kombinacije dimenzija jedinstvena. Ako je dimenzija isključena nakon kreiranja zapisa **Cena uloge**, ovo ograničenje može da se prekrši. Zbog toga je neophodno da pre isključivanja dimenzije izbrišete sve redove **Cena uloge** i **Provizija na cenu uloge** u kojima je ta vrednost dimenzije popunjena.



[!INCLUDE[footer-include](../includes/footer-banner.md)]