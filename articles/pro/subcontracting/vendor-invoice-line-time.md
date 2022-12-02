---
title: Stavke fakture dobavljača za vreme
description: Ovaj članak objašnjava kako se evidentiraju redovi na fakturi dobavljača za troškove vremena koje uneli podugovarači.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262030"
---
# <a name="vendor-invoice-lines-for-time"></a>Stavke fakture dobavljača za vreme

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Faktura dobavljača u usluzi Microsoft Dynamics 365 Project Operations može imati redove na fakturi dobavljača za vreme. Menadžeri projekta mogu da koriste redove na fakturi dobavljača za vreme da bi evidentirali cene za vreme podugovarača na projektima.

Redovi na fakturi dobavljača za vreme mogu, ali i ne moraju da upućuju na predmet podugovora za kategorije vremena. Ako red na fakturi dobavljača za vreme upućuje na podugovor, projektni menadžeri će moći da podudaraju i potvrđuju vreme koje se fakturiše redom na fakturi dobavljača u odnosu na upotrebu vremena koje su evidentirani podugovarači u ovim kategorijama troškova i odobreni od strane projektnog menadžera na projektu.

Sledeća tabela pruža informacije o poljima na redovima na fakturi dobavljača za kategorije vremena.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Naziv reda na fakturi dobavljača, za pomoć pri identifikaciji. | Naziv će biti prikazan kao prva kolona u svim pretragama koje su zasnovane na stavkama na fakturi dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturiše na redu na fakturi dobavljača. | Nijedno |
| Podugovor | Podugovor pod kojim su usluge prvobitno naručene. | Kada je za fakturu dobavljača izabran podugovor, svi redovi na fakturi dobavljača će naslediti taj izbor. Faktura dobavljača ne može imati redove na fakturi dobavljača koji upućuju na različite podugovore. |
| Predmet podugovora | Predmet podugovora pod kojim su usluge naručene. Lista predmeta podugovora koji se mogu izabrati ograničena je na predmete izabranog podugovora. | Kada je predmet podugovora izabran na redu na fakturi dobavljača za vreme, podrazumevane vrednosti za polja **Projekat**, **Uloga** i **Resurs koji može da se rezerviše** se unose iz odgovarajućih polja u predmetu podugovora. Ako izabrani predmet podugovora ima vrednosti u poljima **Projekat**, **Uloga** i **Može da se rezerviše**, vrednosti odgovarajućih polja u redu na fakturi dobavljača ne mogu da se razlikuju od tih vrednosti. |
| Datum transakcije | Datum kada će stvarna vrednost troška reda na fakturi biti evidentirana u projekat. | Nijedno |
| Klasa transakcije | Podrazumevana vrednost je **Vreme**. | Vrednost **Vreme** označava da se red na fakturi dobavljača koristi za evidentiranje iznosa na fakturi vremena podugovarača. |
| Project | Naziv projekta u kom se koriste usluge koje su fakturisane. | Ovo polje je obavezno i ne može da ostane prazno. |
| Zadatak | Naziv projektnog zadatka u kom se koriste usluge koje su fakturisane. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red na fakturi dobavljača sa vremenom koje su evidentirali resursi podugovarača na bilo kom zadatku na projektu. Ako red na fakturi dobavljača ne upućuje na predmet podugovora, a ovo polje ostane prazno, stvarna vrednost troška koju kreira red na fakturi dobavljača neće biti povezana ni sa jednom stvarnom vrednošću nenaplative prodaje. U ovom slučaju, ako je podešena naplata zasnovana na zadatku, troškovi možda neće moći da se fakturišu krajnjem klijentu. |
| Uloga | Uloga resursa podugovarača čije se vreme fakturiše. | Ovo polje navodi ulogu koju izvršavaju resursi podugovora čije je vreme fakturisano na fakturi dobavljača. |
| Resurs koji može da se rezerviše | Ime podugovarača čije se vreme fakturiše. Izbor resursa koji može da se rezerviše je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red na fakturi dobavljača sa vremenom koje je evidentirao bilo koji resurs koji pripada dobavljaču na redu fakture dobavljača. |
| Količina | Unesite broj sati vremena koje dobavljač fakturiše na redu na fakturi. |Nijedno |
| Grupa jedinica | Podrazumevana vrednost je **Grupa vremenskih jedinica** i to se ne može promeniti. | Nijedno |
| Jedinica | Podrazumevana vrednost je osnovna jedinica sati iz vremenske grupe jedinica. Ovu vrednost možete promeniti da biste kupili bilo koju jedinicu iz vremenske grupe jedinica, na primer dan ili nedelju. | Kombinacija vrednosti **Uloga** i **Jedinica** koristiće se kao podrazumevana ili izračunata vrednost za polje **Jedinična cena** za red na fakturi dobavljača. |
| Jedinična cena | Podrazumevana jedinična cena koristi kombinaciju vrednosti **Uloga** i **Jedinica** iz cenovnika za projekat koji se odnosi na datum transakcije reda na fakturi dobavljača. | Ako je cena za važeći cenovnik projekta postavljena u jedinici koja se razlikuje od jedinice na redu na fakturi dobavljača, sistem koristi konverziju jedinice za izračunavanje jedinične cene. |
| Međuiznos | Ovo polje samo za čitanje se računa kao *Količina* &times; *Jedinična cena*, ako se vrednosti unesu i u polje **Količina** i u polje **Jedinična cena**. Ako je jedno od ta dva polja prazno, možete uneti vrednost u ovo polje. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos iz reda na fakturi dobavljača, uključujući porez. Ovo polje se računa kao *Međuzbir* + *Porez na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
