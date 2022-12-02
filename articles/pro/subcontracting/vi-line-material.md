---
title: Stavke fakture dobavljača za proizvode
description: Ovaj članak objašnjava kako evidentirati redove na fakturi dobavljača za proizvode i koristiti različita polja za beleženje kupovine proizvoda od prodavaca.
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

Faktura dobavljača u usluzi Microsoft Dynamics 365 Project Operations može imati redove na fakturi dobavljača za proizvode (nazivaju se i materijali). Menadžeri projekta mogu da koriste redove na fakturi dobavljača za proizvode da bi evidentirali cene proizvoda koji su kupljeni na projektima.

Redovi na fakturi dobavljača za proizvode mogu, ali i ne moraju da upućuju na predmet podugovora za kategorije materijala. Ako red na fakturi dobavljača za kategorije proizvoda upućuje na podugovor, projektni menadžeri će moći da podudaraju i potvrđuju proizvode koji se fakturišu redom na fakturi dobavljača u odnosu na upotrebu korišćenih proizvoda koji su evidentirani u ovim kategorijama troškova i odobreni od strane projektnog menadžera.

Sledeća tabela pruža informacije o poljima na redovima na fakturi dobavljača za kategorije proizvoda.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Naziv reda na fakturi dobavljača, za pomoć pri identifikaciji. | Naziv će biti prikazan kao prva kolona u svim pretragama koje su zasnovane na stavkama na fakturi dobavljača. |
| Opis | Kratak opis proizvoda koje dobavljač fakturiše na redu na fakturi dobavljača. | Nijedno |
| Podugovor | Podugovor pod kojim su proizvodi prvobitno naručeni. | Kada je za fakturu dobavljača izabran podugovor, svi redovi na fakturi dobavljača će naslediti taj izbor. Faktura dobavljača ne može imati redove na fakturi dobavljača koji upućuju na različite podugovore. |
| Predmet podugovora | Predmet podugovora pod kojim su proizvodi naručeni. Lista predmeta podugovora koji se mogu izabrati ograničena je na predmete izabranog podugovora. | Kada je predmet podugovora izabran na redu na fakturi dobavljača za kategorije proizvoda, podrazumevane vrednosti za polja **Projekat**, **Zadatak** i **Proizvod** se unose iz odgovarajućih polja u predmetu podugovora. Ako izabrani predmet podugovora ima vrednosti u poljima **Projekat**, **Zadatak** i **Proizvod**, vrednosti odgovarajućih polja u redu na fakturi dobavljača ne mogu da se razlikuju od tih vrednosti. |
| Datum transakcije | Datum kada će stvarna vrednost troška reda na fakturi biti evidentirana u projekat. | Nijedno|
| Klasa transakcije | Kada su proizvodi fakturisani, ovo polje bi trebalo da bude podešeno na **Materijal**. | Vrednost **Materijal** označava da se red na fakturi dobavljača koristi za evidentiranje iznosa na fakturi za materijale koji su kupljeni. |
| Project | Naziv projekta u kom se koriste proizvodi koji su fakturisani. | Ovo polje je obavezno i ne može da ostane prazno. |
| Zadatak | Naziv projektnog projekta u kom se koriste proizvodi koji su fakturisani. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red na fakturi dobavljača sa kupljenim proizvodom koji se koristi na bilo kom zadatku projekta. Ako red na fakturi dobavljača ne upućuje na predmet podugovora, a ovo polje ostane prazno, stvarna vrednost troška koju kreira red na fakturi dobavljača neće biti povezana ni sa jednom stvarnom vrednošću nenaplative prodaje. U ovom slučaju, ako je podešena naplata zasnovana na zadatku, troškovi neće moći da se fakturišu krajnjem klijentu. |
| Izaberite proizvod | Izaberite da li je proizvod koji se fakturiše postojeći proizvod iz kataloga proizvoda ili je ručno dodat proizvod. | Podrazumevana vrednost se unosi iz predmeta podugovora kada je izabran predmet podugovora. |
| Proizvod | Izaberite proizvod iz kataloga. Ako je proizvod ručno dodat proizvod, unesite naziv proizvoda. | Ovo polje se koristi za unos podrazumevanih nabavnih cena za postojeće proizvode. |
| Količina | Unesite količinu materijala koju dobavljač fakturiše u ovom redu na fakturi. | Nijedno |
| Grupa jedinica | Izaberite grupu jedinica jedinice u kojoj je izražena količina koja se fakturiše. | Nijedno |
| Jedinica | Podrazumevana vrednost je osnovna jedinica izabrane grupe jedinica. Ovu vrednost možete promeniti da biste platili bilo koju jedinicu iz izabrane grupe jedinica. | Kombinacija vrednosti **Proizvod** i **Jedinica** koristiće se kao podrazumevana ili izračunata vrednost za polje **Jedinična cena** za red na fakturi dobavljača. |
| Jedinična cena | Podrazumevana jedinična cena koristi kombinaciju vrednosti **Proizvod** i **Jedinica** iz cenovnika za projekat koji se odnosi na datum transakcije reda na fakturi dobavljača. | Nijedno |
| Međuiznos | Ovo polje samo za čitanje se računa kao *Količina* &times; *Jedinična cena*, ako se vrednosti unesu i u polje **Količina** i u polje **Jedinična cena**. Ako je jedno od ta dva polja prazno, možete uneti vrednost u ovo polje. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos iz reda na fakturi dobavljača, uključujući porez. Ovo polje se računa kao *Međuzbir* + *Porez na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
