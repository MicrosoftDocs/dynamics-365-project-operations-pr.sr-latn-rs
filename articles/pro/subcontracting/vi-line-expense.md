---
title: Stavke fakture dobavljača za kategorije troškova
description: Ovaj članak sadrži objašnjenja o tome kako se zapisuju redovi fakture dobavljača za kategorije troškova.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261717"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Stavke fakture dobavljača za kategorije troškova

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Faktura dobavljača u korporaciji Microsoft može Dynamics 365 Project Operations imati redove fakture dobavljača za kategorije troškova. Menadžeri projekta mogu da koriste redove fakture dobavljača za kategorije troškova da bi zapisali troškove usluga koji se nabavljaju kao kategorije troškova.

Redovi fakture dobavljača za kategorije troškova mogu, ali i ne mora da upućuju na red podizvođači za kategorije troškova. Ako red fakture dobavljača za kategorije troškova upućuje na podizvođač, menadžeri projekta će moći da se podudaraju i verifikuju troškove koje fakturiše red fakture dobavljača u odnosu na troškove koji su zapisani u ovim kategorijama troškova i odobreni od strane menadžera projekta na projektu.

Sledeća tabela pruža informacije o poljima u redovima fakture dobavljača za kategorije troškova.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Ime reda fakture dobavljača, da biste pomogli u identifikaciji. | Ovo ime će biti prikazano kao prva kolona u svim pronalaženjem koja se zasniva na redovima fakture dobavljača. |
| Opis | Kratak opis servisa koje dobavljač fakturiše u redu fakture dobavljača. | Nijedno |
| Podugovor | Podizvođači na koji su usluge prvobitno naručene. | Kada je za fakturu dobavljača izabran podizvođaи, svi redovi u fakturi dobavljača жe naslediti taj izbor. Faktura dobavljača ne može imati redove fakture dobavljača koji upućuju na različite podizvođači. |
| Red podizvođači | Red podizvođače na kojem su usluge naručene. Lista redova podizvođaka koji se mogu izabrati ograničena je na redove izabranog podizvođaka. | Kada je red podizvođača izabran u redu fakture dobavljača za kategorije troškova, podrazumevane vrednosti **za polja "Projekat**", **"Zadatak**" i "Transakcija" **se** unose iz odgovarajućih polja u redu podizvođača. Ako izabrani red podizvođača ima vrednosti u poljima **"Projekat",**"**Projektni** zadatak" i **"Transakcija**", vrednosti odgovarajućih polja u redu fakture dobavljača ne mogu da se razlikuju od tih vrednosti. |
| Datum transakcije | Datum kada će trošak stvarnog reda fakture dobavljača biti zapisan u projekat. |Nijedno |
| Klasa transakcije | Izaberite **troškove** da biste zapisali fakturu dobavljača za kategoriju troškova. | Vrednost "Troškovi **"** označava da se red fakture dobavljača koristi za zapisivanje iznosa fakture za servise koji su nabavljeni kao kategorije troškova. |
| Project | Korišćeno je ime projekta na kojem su korišćene usluge koje se fakturiše. | Ovo polje je obavezno i ne može ostati prazno. |
| Zadatak | Korišćeno je ime projektnog zadatka na kojem su korišćene usluge koje se fakturiše. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red fakture dobavljača sa troškovima koji su zapisani na bilo kom zadatku projekta. Ako red fakture dobavljača ne upućuje na red podizvođača, a ovo polje ostane prazno, stvarni trošak koji je kreirao red fakture dobavljača neće biti povezan ni sa jednom neobličavanom stvarnom prodajom. U ovom slučaju, ako je naplata zasnovana na zadatku podešena, troškovi možda neće moći da se fakturišu krajnjem kupcu. |
| Kategorija transakcije | Kategorija transakcije koja se fakturiše. Za izabranu kategoriju transakcije mora biti kreirana odgovarajuća kategorija troškova. | Kombinacija kategorije " **Transakcija** " **i "** Jedinične vrednosti" će biti korišćena kao podrazumevana ili izračunata vrednost za **polje Jedinična** cena u redu fakture dobavljača. |
| Količina | Unesite količinu koju fakturiše dobavljač u redu fakture. |Nijedno|
| Grupa jedinica | Podrazumevana vrednost se unosi na osnovu grupe jedinica izabrane kategorije transakcije. | Nijedno |
| Jedinica | Podrazumevana vrednost je osnovna jedinica izabrane grupe jedinica. Ovu vrednost možete promeniti da biste je kupili u bilo kojoj jedinici grupe jedinica. | Kombinacija kategorije " **Transakcija** " **i "** Jedinične vrednosti" će biti korišćena kao podrazumevana ili izračunata vrednost za **polje Jedinična** cena u redu fakture dobavljača. |
| Jedinična cena | Podrazumevana jedinična cena koristi kombinaciju kategorije **Transakcija** **i Vrednosti** jedinice iz cenovnik projekta koji je primenljiv na datum transakcije reda fakture dobavljača. | Ako je cena za važeći cenovnik projekta podešena u jedinici koja se razlikuje od jedinice u redu fakture dobavljača, sistem koristi konverziju jedinice da bi izračunao cenu po jedinici. |
| Međuiznos | Ovo polje samo za čitanje se izračunava kao jedinična *cena*&times;*količine*, ako su vrednosti unete i **u polje Količina** i u polje **Jedinična** cena. Ako su jedno ili oba polja prazna, u ovo polje možete uneti vrednost.| Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos reda fakture dobavljača, uključujući poreze. Ovo polje se izračunava kao podzbir *poreza* + *na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
