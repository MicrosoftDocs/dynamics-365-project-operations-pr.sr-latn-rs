---
title: Stavke fakture dobavljača za vreme
description: Ovaj članak sadrži objašnjenja o tome kako se zapisuju redovi fakture dobavljača za vremenske troškove koje su podizvođači stavili.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927575"
---
# <a name="vendor-invoice-lines-for-time"></a>Stavke fakture dobavljača za vreme

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Faktura dobavljača u korporaciji Microsoft Dynamics 365 Project Operations može imati redove fakture dobavljača za vreme. Menadžeri projekta mogu da koriste redove fakture dobavljača za vreme za zapisivanje troškova vremena podizvođača na projektima.

Redovi fakture dobavljača za vreme mogu, ali i ne mora da upućuju na red podizvođaиa za vreme. Ako red fakture dobavljača za vreme upućuje na podizvođač, menadžeri projekta će moći da se podudaraju i provere vreme koje fakturiše red fakture dobavljača u odnosu na vreme koje su zapisali podizvođači i koje su menadžeri projekta odobrili na projektu.

Sledeća tabela obezbeđuje informacije o poljima u redovima fakture dobavljača za vreme.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Ime reda fakture dobavljača, da biste pomogli u identifikaciji. | Ovo ime će biti prikazano kao prva kolona u svim pronalaženjem koja se zasniva na redovima fakture dobavljača. |
| Opis | Kratak opis servisa koje dobavljač fakturiše u redu fakture dobavljača. | Nijedno |
| Podugovor | Podizvođači na koji su usluge prvobitno naručene. | Kada je za fakturu dobavljača izabran podizvođaи, svi redovi u fakturi dobavljača жe naslediti taj izbor. Faktura dobavljača ne može imati redove fakture dobavljača koji upućuju na različite podizvođači. |
| Red podizvođači | Red podizvođače na kojem su usluge naručene. Lista redova podizvođaka koji se mogu izabrati ograničena je na redove izabranog podizvođaka. | Kada je red podizvođača izabran u redu fakture dobavljača za vreme, podrazumevane vrednosti **za polja "Projekat**", **"Uloga**" i "Resurs za **rezervisanje** " se unose iz odgovarajućih polja u redu podizvođača. Ako izabrani red podizvođača ima vrednosti u **poljima "Projekat**", **"Uloga**" i " **Rezervisano** ", vrednosti odgovarajućih polja u redu fakture dobavljača ne mogu da se razlikuju od tih vrednosti. |
| Datum transakcije | Datum kada će trošak stvarnog reda fakture dobavljača biti zapisan u projekat. | Nijedno |
| Klasa transakcije | Podrazumevana vrednost je **Vreme**. | Vrednost "Vreme **"** označava da se red fakture dobavljača koristi za zapisivanje iznosa fakture vremena podizvođača. |
| Project | Korišćeno je ime projekta na kojem su korišćene usluge koje se fakturiše. | Ovo polje je obavezno i ne može ostati prazno. |
| Zadatak | Korišćeno je ime projektnog zadatka na kojem su korišćene usluge koje se fakturiše. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da se podudara sa redom fakture dobavljača sa vremenom koje su zapisali resursi podizvođača na bilo kom zadatku projekta. Ako red fakture dobavljača ne upućuje na red podizvođača, a ovo polje ostane prazno, stvarni trošak koji je kreirao red fakture dobavljača neće biti povezan ni sa jednom neobličavanom stvarnom prodajom. U ovom slučaju, ako je naplata zasnovana na zadatku podešena, troškovi možda neće moći da se fakturišu krajnjem kupcu. |
| Uloga | Uloga resursa podizvođača čije se vreme fakturiše. | Ovo polje navodi ulogu koju izvršavaju resursi podizvođač čije je vreme fakturisano u fakturi dobavljača. |
| Resurs koji može da se rezerviše | Ime podizvođača čije se vreme fakturiše. Izbor resursa koji se može rezervisati je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da se podudara sa redom fakture dobavljača sa vremenom koje zapisuje bilo koji resurs koji pripada dobavljaču u redu fakture dobavljača. |
| Količina | Unesite broj časova vremena koje dobavljač fakturiše u redu fakture. |Nijedno |
| Grupa jedinica | Podrazumevana vrednost je grupa **jedinica vremena i** ne može se menjati. | Nijedno |
| Jedinica | Podrazumevana vrednost je osnovna jedinica časova iz grupe vremenskih jedinica. Ovu vrednost možete promeniti da biste je kupili u bilo kojoj jedinici grupe vremenskih jedinica, kao što su dan ili sedmica. | Kombinacija vrednosti "Uloga **·**" i **"** Jedinica" će se koristiti kao podrazumevana ili izračunata vrednost za polje **Jedinična cena** u redu fakture dobavljača. |
| Jedinična cena | Podrazumevana jedinična cena koristi kombinaciju vrednosti **"Uloga** " **i** "Jedinica" iz cenovnog lista projekta koji je primenljiv na datum transakcije reda fakture dobavljača. | Ako je cena za važeći cenovnik projekta podešena u jedinici koja se razlikuje od jedinice u redu fakture dobavljača, sistem koristi konverziju jedinice da bi izračunao cenu po jedinici. |
| Međuiznos | Ovo polje samo za čitanje se izračunava kao jedinična *cena*&times;*količine*, ako su vrednosti unete i **u polje Količina** i u polje **Jedinična** cena. Ako su jedno ili oba polja prazna, u ovo polje možete uneti vrednost. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos reda fakture dobavljača, uključujući poreze. Ovo polje se izračunava kao podzbir *poreza* + *na promet*. | Nijedno |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
