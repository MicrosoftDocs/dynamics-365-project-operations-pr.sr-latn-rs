---
title: Metode dodele rezervacija u usluzi Project Service Automation
description: Ova tema pruža informacije o različitim načinima na koje možete rezervisati dodele.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 295da428ce15e7775450dfa94e96047f200bdede
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083574"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Metode dodele rezervacija u usluzi Project Service Automation

Bilo da dodajete člana tima direktno u projekat na kartici **Tim** ili rezervišete resurs za projekat ili zahtev na tabeli rasporeda, postoji nekoliko različitih načina dodele rezervacija koje možete da koristite. Ova tema objašnjava kako svaki metod funkcioniše i koji načini mogu dovesti do prebukiranja resursa.

## <a name="full-capacity"></a>Puni kapacitet 
Metod punog kapaciteta rezerviše puni kapacitet resursa za navedene početne i krajnje datume. Na primer, ako resurs ima kalendar podešen na osam radnih sati dnevno, pet dana u sedmici, podešavanje datuma početka i završetka koji pokriva pet radnih dana rezerviše resurs na 40 časova. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 40 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

## <a name="remaining-capacity"></a>Preostali kapacitet
Metod preostalog kapaciteta je dostupan samo kada rezervišete direktno za projekat pomoću tabele rasporeda. Ovaj način rezerviše dostupan kapacitet resursa u okviru navedenog opsega datuma. Na primer, ako resurs ima kapacitet od 40 časova sedmično i već je rezervisan za 10 časova, rezervisanje za istu sedmicu dovodi do rezervacije preostalih 30 časova kapaciteta za tu sedmicu.

## <a name="percentage-capacity"></a>Kapacitet u procentima
Metod procenta kapaciteta rezerviše određeni procenat kapaciteta resursa za navedene datume početka i završetka. Na primer, ako resurs ima kalendar podešen na osam radnih sati dnevno, pet dana u sedmici, podešavanje datuma početka i završetka koji pokriva pet radnih dana sa po 50% kapaciteta rezerviše resurs na 20 časova. Pojedinačne rezervacije po danu se ravnomerno dele tokom perioda, u ovom primeru na četiri radna sata dnevno. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 20 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

## <a name="evenly-distribute-hours"></a>Broj časova ravnomernog raspoređivanja
Metodom broja časova ravnomernog raspoređivanja rezervišete resurs za određeni broj časova, ravnomerno raspoređujući vreme po danu tokom navedenih datuma početka/završetka. Na primer, ako rezervišete resurs za 20 radnih sati tokom perioda od pet dana, ovaj metod distribuira 20 sati ravnomerno na četiri sata po danu. Rezervacija se obavlja bez obzira na preostali kapacitet resursa. Ako je resurs već rezervisan tokom tog perioda na drugim projektima, 20 časova rezervišete kao dodatne radne sate, što potencijalno dovodi do prebukiranja.

## <a name="front-load-hours"></a>Broj časova početnog opterećenja
Metodom broja časova početnog opterećenja rezervišete resurs za određeni broj časova, raspoređujući časove rada po danu na prve dane tokom navedenih datuma početka i završetka. Početno opterećivanje troši dostupan kapacitet resursa po redosledu kako posao stiže. Na primer, ako je raspored rada resursa osam radnih sati dnevno, pet dana sedmično, a trenutno nema rezervacije, rezervisanje resursa na 20 časova tokom perioda od pet radnih dana dovodi do sledećeg obrasca dnevne rezervacije: 

|         Rezervacije          |    Dan 1    |    Dan 2    |    Dan 3    |    Dan 4    |    Dan 5    |    Ukupno    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Postojeće   rezervacije    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nova   rezervacija          |    8        |    8        |    4        |    0        |    0        |    20.       |

Način početnog opterećenja uzima u obzir postojeće rezervacije i dostupan kapacitet. Na primer, ako isti resurs već ima 20 časova rezervacija tokom radne sedmice, nove rezervacije troše preostali kapacitet na sledeći način:

|   Rezervacije          | Dan 1 | Dan 2 | Dan 3 | Dan 4 | Dan 5 | Ukupno |
|---------------------|-------|-------|-------|-------|-------|-------|
| Postojeće   rezervacije | 8     | 8     | 4     | 0     | 0     | 20    |
| Nova   rezervacija       | 0     | 0     | 4     | 8     | 8     | 20.    |

Zato što se uzima u obzir dostupan kapacitet, možete da dobijete poruku o grešci ako resurs nema preostali kapacitet koji rezervacija resursa može da pokrije. Sa ovom načinom ne možete da izvršite prebukiranje.

## <a name="none"></a>Nijedno
Metod Nijedan je dostupan samo kada rezervišete na kartici **Tim** u okviru projekta. Ovaj metod dodaje resurs kao člana tima u projektu, ali ne kreira nijednu rezervaciju koja troši kapacitet resursa. Ovaj metod se koristi kada se prilikom kreiranja projekta dodaje član tima podrazumevanog menadžera projekta. Korisnik menadžera projekta koji je kreirao projekat se podrazumevano dodaje u projekat, tako da zapis entiteta projekta ima vlasnika i ne postoji odobravalac na projektu. Zato što ovaj korisnik nema rezervacije, ako želite da rezervišete resurs, možete da ga izbrišite i zatim ga ponovo dodate pomoću drugog načina dodele. Drugi način je da resurs dodate zadacima, a da zatim koristite opciju **Produži rezervacije** na kartici **Usaglašenost** kako biste kreirali rezervacije za dodele.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Načini dodele koji dovode do prebukiranja
Da rezimiramo, sledeći načini dodele dovode do prebukiranja ako je resurs već izvršen u drugim projektima (ili za druge radne naloge ili entitete za koje je moguće zakazivati):

- Puni kapacitet
- Kapacitet u procentima
- Broj časova ravnomernog raspoređivanja

Kada koristite neki od ova tri načina dodele, nećete biti obavešteni da je resurs prebukiran. Da biste ispravili prebukiranje, potrebno je da koristite tabelu rasporeda.
