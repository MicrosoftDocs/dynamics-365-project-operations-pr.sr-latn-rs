---
title: Predmeti podugovora za vreme
description: Ovaj članak objašnjava kako snimiti predmete podugovora za vreme i evidentirati kupovinu vremena od prodavaca.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522250"
---
# <a name="subcontract-lines-for-time"></a>Predmeti podugovora za vreme

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Podugovor u usluzi Dynamics 365 Project Operations može imati predmet podugovora za vreme. Predmeti podugovora za vreme omogućavaju menadžeru projekta da kupuje vreme resursa prodavca za osoblje projektnih zadataka i potrebe za resursima.

Dovršite sledeće korake da biste kreirali predmet podugovora za vreme u usluzi Project Operations.

1. U oknu za navigaciju izaberite **Podugovori**, i otvorite podugovor.
2. Na kartici **Predmeti podugovora** izaberite **Novo** za kreiranje novog predmeta podugovora.
3. Na stranici **Brzo kreiranje**, u polju **Klasa transakcije** izaberite **Vreme**.
4. Unesite preostale informacije za polje, a zatim izaberite **Sačuvaj**.

  Sledeća tabela pruža informacije o poljima na stranici **Predmet podugovora** i stranici **Brzo kreiranje**.

| **Polje** | **Opis** | **Funkcionalni uticaj** |
| --- | --- | --- |
| +Ime | Naziv stavke podugovora za pomoć pri identifikaciji. | Ovo će biti prikazano kao prva kolona u svim pretragama zasnovanim na stavkama predmeta podugovora. |
| Opis | Kratak opis usluga koje se kupuju u okviru predmeta podugovora. |Ništa |
| Tip predmeta |   Ovo polje ima podrazumevanu vrednost **Na osnovu količine**.| Ništa |
| Način naplate | Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja podržana u usluzi Project Operations: **Fiksna cena** i **Vreme i materijal**. | Na osnovu izabranog načina obračuna, raspored faktura zasnovan na kontrolnim tačkama je dostupan za stavke podugovora sa metodom naplate po fiksnoj ceni. |
| Klasa transakcije | Podrazumevana vrednost je **Vreme**. | Ovo ukazuje na to da se stavka podugovora koristi za evidentiranje kupovine vremena za podizvođača. |
| Uloga | Odaberite ulogu resursa podugovora čije se vreme kupuje. | Uloga koju obavljaju resursi podugovora određuje cenu kupovine. |
| Zahtevani početak | Unesite datum kada resursi podizvođača treba da počnu sa radom. | Ovo se koristi za izbor cenovnika projekta iz cenovnika projekta koji je priložen podugovoru. Cena uloge na stavci podugovora potiče iz tog cenovnika. |
| Zahtevani završetak | Unesite datum kada se angažovanje resursa podugovarača završava. | Ovo će se koristiti za prikazivanje upozorenja kada vođa projekta koristi kapacitete za zahteve za resursima koji se javljaju nakon ovog datuma. |
| Poručena količina | Unesite broj sati za ulogu koja se kupuje od dobavljača. | Ovo će se koristiti za prikazivanje upozorenja kada vođa projekta koristi kapacitete veće od onih iz ovog zahteva za resursima. |
| Grupa jedinica | Podrazumevana vrednost je **Grupa vremenskih jedinica** i to se ne može promeniti. | Ništa|
| Jedinica | Podrazumevana vrednost za ovo polje je osnovna jedinica sati iz **Grupe vremenskih jedinica**. Ovu vrednost možete promeniti da biste kupili bilo koju jedinicu iz **grupe vremenskih jedinica**, na primer dan ili nedelju. | Kombinacija **Uloge** i **Jedinice** koristiće se kao podrazumevana vrednost ili će biti izračunata za jediničnu cenu za predmet podugovora. |
| Cena po jedinici | Podrazumevana jedinična cena koristi kombinaciju **Uloga** i **Jedinica** iz cenovnika projekta koji se primenjuje za **Traženi datum početka** za stavku podugovora. | Kada je na važećem cenovniku projekta cena postavljena u različitoj jedinici od jedinice na predmetu podugovora, sistem koristi konverziju jedinice za izračunavanje jedinične cene. |
| Međuiznos |    Ovo je polje samo za čitanje koje se izračunava kao „Količina“ x „Jedinična cena“, ako su unete vrednosti za količinu i jediničnu cenu. Ako je količina, cena po jedinici ili oba polja prazna, vrednost možete uneti u polje. | Ništa|
| Porez na promet |   Unesite iznos poreza na promet. |Ništa |
| Ukupan iznos | Ukupan iznos iz predmeta podugovora uključujući porez. Ovo polje se računa kao međuzbir + porez na promet.|Ništa |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
