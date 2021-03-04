---
title: Načini dodele rezervacija
description: Ova tema pruža informacije o tome kako načini dodele rezervacija funkcionišu u usluzi Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: cc539a376088627aa8d3e9678b2aec4bd5d0edc3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121505"
---
# <a name="booking-allocation-methods"></a>Načini dodele rezervacija

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Bilo da dodajete člana tima direktno u projekat na kartici **Tim** ili rezervišete resurs za projekat ili zahtev na tabeli rasporeda, postoji nekoliko različitih načina dodele rezervacija koje možete da koristite. Ova tema objašnjava kako svaki metod funkcioniše i koji načini mogu dovesti do prebukiranja resursa.

## <a name="booking-allocation-methods"></a>Načini dodele rezervacija

Postoji šest načina dodele rezervacija koje možete koristiti:

- [Puni kapacitet](#full)
- [Preostali kapacitet](#remaining)
- [Kapacitet u procentima](#percentage)
- [Broj časova ravnomernog raspoređivanja](#evenly)
- [Broj časova početnog opterećenja](#front)
- [Nijedno](#none)

### <a name="full-capacity"></a><a name="full"></a>Puni kapacitet 
Metod punog kapaciteta rezerviše puni kapacitet resursa za navedene početne i krajnje datume. Na primer, ako resurs ima kalendar podešen na osam radnih sati dnevno, pet dana u sedmici, podešavanje datuma početka i završetka koji pokriva pet radnih dana rezerviše resurs na 40 časova. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 40 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

### <a name="remaining-capacity"></a><a name="remaining"></a>Preostali kapacitet
Metod preostalog kapaciteta je dostupan samo kada rezervišete direktno za projekat pomoću tabele rasporeda. Ovaj način rezerviše dostupan kapacitet resursa u okviru navedenog opsega datuma. Na primer, ako resurs ima kapacitet od 40 časova sedmično i već je rezervisan za 10 časova, rezervisanje za istu sedmicu dovodi do rezervacije preostalih 30 časova kapaciteta za tu sedmicu.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapacitet u procentima
Metod procenta kapaciteta rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka. Na primer, ako resurs ima kalendar podešen na osam radnih sati dnevno, pet dana u sedmici, podešavanje datuma početka i završetka koji pokriva pet radnih dana sa po 50% kapaciteta rezerviše resurs na 20 časova. Pojedinačne rezervacije po danu se ravnomerno dele tokom perioda, u ovom primeru na četiri radna sata dnevno. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 20 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Broj časova ravnomernog raspoređivanja
Metodom broja časova ravnomernog raspoređivanja rezervišete resurs za određeni broj časova, ravnomerno raspoređujući vreme po danu tokom navedenih datuma početka/završetka. Na primer, ako rezervišete resurs za 20 radnih sati tokom perioda od pet dana, ovaj metod distribuira 20 sati ravnomerno na četiri sata po danu. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 20 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

### <a name="front-load-hours"></a><a name="front"></a>Broj časova početnog opterećenja
Metodom broja časova početnog opterećenja rezervišete resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka. Početno opterećivanje troši dostupan kapacitet resursa po redosledu kako posao stiže. Na primer, ako je raspored rada resursa osam radnih sati dnevno, pet dana sedmično, a trenutno nema rezervacije, rezervisanje resursa na 20 časova tokom perioda od pet radnih dana dovodi do sledećeg obrasca dnevne rezervacije: 

|                           |    Dan 1    |    Dan 2    |    Dan 3    |    Dan 4    |    Dan 5    |    Ukupno    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Postojeće   rezervacije**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nova   rezervacija**          |    8        |    8        |    4        |    0        |    0        |    20.       |

Način početnog opterećenja uzima u obzir postojeće rezervacije i dostupan kapacitet. Na primer, ako isti resurs već ima 20 časova rezervacija tokom radne sedmice, nove rezervacije troše preostali kapacitet na sledeći način:

|                     | Dan 1 | Dan 2 | Dan 3 | Dan 4 | Dan 5 | Ukupno |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Postojeće   rezervacije** | 8     | 8     | 4     | 0     | 0     | 20.    |
| **Nova   rezervacija**       | 0     | 0     | 4     | 8     | 8     | 20.    |

Zato što se uzima u obzir dostupan kapacitet, možete da dobijete poruku o grešci ako resurs nema preostali kapacitet koji rezervacija resursa može da pokrije. Sa ovom načinom ne možete da izvršite prebukiranje.

### <a name="none"></a><a name="none"></a>Nijedno
Metod Nijedan je dostupan samo kada rezervišete na kartici **Tim** u okviru projekta. Ovaj metod dodaje resurs kao člana tima u projektu, ali ne kreira nijednu rezervaciju koja troši kapacitet resursa. Ovaj metod se koristi kada se prilikom kreiranja projekta dodaje član tima podrazumevanog menadžera projekta. Korisnik menadžera projekta koji je kreirao projekat se podrazumevano dodaje u projekat, tako da zapis entiteta projekta ima vlasnika i ne postoji odobravalac na projektu. Zato što ovaj korisnik nema rezervacije, ako želite da rezervišete resurs, možete da ga izbrišite i zatim ga ponovo dodate pomoću drugog načina dodele. Drugi način je da resurs dodate zadacima, a da zatim koristite opciju **Produži rezervacije** na kartici **Usaglašenost** kako biste kreirali rezervacije za dodele.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Načini dodele koji dovode do prebukiranja
Da rezimiramo, sledeći načini dodele dovode do prebukiranja ako je resurs već izvršen u drugim projektima (ili za druge radne naloge ili entitete za koje je moguće zakazivati):

- Puni kapacitet
- Kapacitet u procentima
- Broj časova ravnomernog raspoređivanja

Kada koristite neki od ova tri načina dodele, nećete biti obavešteni da je resurs prebukiran. Da biste ispravili prebukiranje, potrebno je da koristite tabelu rasporeda.


[!INCLUDE[footer-include](../includes/footer-banner.md)]