---
title: Stavke fakture dobavljača za proizvode
description: Ovaj članak sadrži objašnjenja o tome kako da zakažete redove fakture dobavljača za proizvode i koristite različita polja za zapisivanje nabavki proizvoda od dobavljača.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261576"
---
# <a name="vendor-invoice-lines-for-products"></a>Stavke fakture dobavljača za proizvode

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Faktura dobavljača u korporaciji Microsoft Dynamics 365 Project Operations može imati redove fakture dobavljača za proizvode (nazivaju se i materijali). Menadžeri projekta mogu da koriste redove fakture dobavljača za proizvode da bi zapisali troškove proizvoda koji su kupljeni na projektima.

Redovi fakture dobavljača za proizvode mogu, ali i ne mora da upućuju na red podizvođaca za materijale. Ako red fakture dobavljača za proizvode upućuje na podizvođač, menadžeri projekta će moći da se podudaraju i verifikuju proizvode koje fakturiše red fakture dobavljača u odnosu na korišćenje nabavljenih proizvoda koje zapisuju i odobravaju menadžeri projekta.

Sledeća tabela pruža informacije o poljima u redovima fakture dobavljača za proizvode.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Ime reda fakture dobavljača, da biste pomogli u identifikaciji. | Ovo ime će biti prikazano kao prva kolona u svim pronalaženjem koja se zasniva na redovima fakture dobavljača. |
| Opis | Kratak opis proizvoda koje dobavljač fakturiše u redu fakture dobavljača. | Nijedno |
| Podugovor | Podizvođači na koji su proizvodi prvobitno poručeni. | Kada je za fakturu dobavljača izabran podizvođaи, svi redovi u fakturi dobavljača жe naslediti taj izbor. Faktura dobavljača ne može imati redove fakture dobavljača koji upućuju na različite podizvođači. |
| Red podizvođači | Linija podizvođače na koju su poručeni proizvodi. Lista redova podizvođaka koji se mogu izabrati ograničena je na redove izabranog podizvođaka. | Kada je u redu podizvođača izabran red podizvođača za proizvode, podrazumevane vrednosti **za polja "Projekat**", **"Zadatak**" i "Proizvod **"** se unose iz odgovarajućih polja u redu podizvođača. Ako izabrani red podizvođača ima vrednosti u **poljima "Projekat**", **"Zadatak**" **i "Proizvod** ", vrednosti odgovarajućih polja u redu fakture dobavljača ne mogu da se razlikuju od tih vrednosti. |
| Datum transakcije | Datum kada će trošak stvarnog reda fakture dobavljača biti zapisan u projekat. | Nijedno|
| Klasa transakcije | Kada su proizvodi fakturisani, ovo polje bi trebalo da bude podešeno na "Materijal **"**. | Vrednost " **Materijal"** označava da se red fakture dobavljača koristi za zapisivanje iznosa fakture za nabavljene materijale. |
| Project | Ime projekta na kojem su korišćeni proizvodi koji se fakturiše. | Ovo polje je obavezno i ne može ostati prazno. |
| Zadatak | Korišćeno je ime projektnog zadatka na koji su korišćeni proizvodi koji se fakturiše. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red fakture dobavljača sa kupljenim proizvodom koji se koristi za bilo koji zadatak projekta. Ako red fakture dobavljača ne upućuje na red podizvođača, a ovo polje ostane prazno, stvarni trošak koji je kreirao red fakture dobavljača neće biti povezan ni sa jednom neobličavanom stvarnom prodajom. U ovom slučaju, ako je naplata zasnovana na zadatku podešena, troškovi neće moći da se fakturišu krajnjem kupcu. |
| Izaberite proizvod | Izaberite da li je proizvod koji se fakturiše postojeći proizvod iz kataloga ili proizvod za upis. | Podrazumevana vrednost se unosi iz reda podizvođaka kada je izabran red podizvođači. |
| Proizvod | Izaberite proizvod iz kataloga. Ako je proizvod proizvod koji se upisi, unesite ime proizvoda. | Ovo polje se koristi za unos podrazumevanih nabavnih cena za postojeće proizvode. |
| Količina | Unesite količinu materijala koju dobavljač fakturiše u ovom redu fakture. | Nijedno |
| Grupa jedinica | Izaberite grupu jedinica u kojoj je izražena količina koja se fakturiše. | Nijedno |
| Jedinica | Podrazumevana vrednost je osnovna jedinica izabrane grupe jedinica. Ovu vrednost možete promeniti da biste platili u bilo kojoj jedinici izabrane grupe jedinica. | Kombinacija vrednosti proizvoda **i** **jedinice** će biti korišćena kao podrazumevana ili izračunata vrednost za polje **Jedinična cena** u redu fakture dobavljača. |
| Jedinična cena | Podrazumevana jedinična cena koristi kombinaciju vrednosti **proizvoda** **i jedinice** iz cenovnik projekta koji je primenljiv na datum transakcije reda fakture dobavljača. | Nijedno |
| Međuiznos | Ovo polje samo za čitanje se izračunava kao jedinična *cena*&times;*količine*, ako su vrednosti unete i **u polje Količina** i u polje **Jedinična** cena. Ako su jedno ili oba polja prazna, u ovo polje možete uneti vrednost. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos reda fakture dobavljača, uključujući poreze. Ovo polje se izračunava kao podzbir *poreza* + *na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
