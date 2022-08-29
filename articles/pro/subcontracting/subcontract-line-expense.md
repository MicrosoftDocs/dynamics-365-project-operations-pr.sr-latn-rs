---
title: Predmeti podugovora za kategorije troškova
description: Ovaj članak sadrži objašnjenja o tome kako da zapušite redove podizvođača za troškove i koristite polja da biste zapisali nabavku vremena od dobavljača.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7166642abc2187a53f7019639df6f0d7124f4765
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261858"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Predmeti podugovora za kategorije troškova

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Podugovor u usluzi Dynamics 365 Project Operations može imati predmet za kategorije troškova. Predmeti podugovora za kategorije troškova dozvoljavaju menadžeru projekta da kupuje kategorije usluga ili proizvoda od prodavaca koje mogu da naplate na ime projekta.

Dovršite sledeće korake da biste kreirali predmet podugovora za kategorije troškova u usluzi Project Operations.

1. Na stranici navigacije izaberite **Podugovori** i otvorite podugovor sa kojim želite da radite.
2. Na kartici **Predmeti podugovora** izaberite **Novo** za kreiranje novog predmeta.
3. Na stranici **Brzo kreiranje**, u polju **Klasa transakcije** izaberite **Trošak** i unesite ili izaberite bilo koje druge potrebne informacije o polju.

Sledeća tabela pruža informacije o poljima na stranici sa detaljima **Predmet podugovora** i stranici **Brzo kreiranje**.

| **Polje** | **Opis** | **Funkcionalni uticaj** |
| --- | --- | --- |
| +Ime | Naziv stavke podugovora za pomoć pri identifikaciji. | Ovo će biti prikazano kao prva kolona u svim pretragama zasnovanim na stavkama predmeta podugovora. |
| Opis | Kratak opis kategorija troškova koje se kupuju u stavci podugovora. | Ništa |
|Tip predmeta | Ovo polje ima podrazumevanu vrednost **Na osnovu količine**. |Ništa |
| Način naplate | Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja podržana u usluzi Project Operations: **Fiksna cena** i **Vreme i materijal**. | Raspored faktura zasnovan na kontrolnim tačkama je dostupan za stavke podugovora kada je izabran metod naplate po fiksnoj ceni. |
| Klasa transakcije | Ovo polje ima podrazumevanu vrednost **Vreme**. Da biste kreirali predmete podugovora za kupovinu proizvoda, podesite polje **Klasa transakcije** na **Trošak**.  | Ovo ukazuje na to da se predmet podugovora koristi za evidentiranje kupovine kategorije troškova koji će se koristiti na projektima. |
| Kategorija transakcije | Prikazuje listu aktivnih kategorija transakcija u sistemu. |Ništa |
| Zahtevani početak | Unesite datum kada kategorije nabavke moraju da budu dostupne kod dobavljača. | Zahtevano vreme početka se koristi za izbor cenovnika projekta iz cenovnika projekta koji je priložen podugovoru. Cena kategorije na stavci podugovora potiče iz tog cenovnika. |
| Zahtevani završetak | Unesite datum kada kategorije nabavke više neće biti potrebne. | Ovo će se koristiti za prikazivanje upozorenja kada vođa projekta poveže ovu stavku podugovora sa određenim procenama troškova na projektu koji su potrebni nakon ovog datuma. |
| Poručena količina | Količina kategorije koja se kupuje od dobavljača. | Ovo će se koristiti za prikazivanje upozorenja kada vođa projekta koristi količinu veću od ove.|
| Grupa jedinica | Podrazumevana vrednost se zasniva na podrazumevanoj grupi jedinica koja je podešena za izabranu kategoriju. |Ništa |
| Jedinica | Podrazumevana vrednost se zasniva na podrazumevanoj jedinici koja je podešena za izabranu kategoriju.  | Kombinacija **Kategorije** i **Jedinice** koristiće se kao podrazumevana vrednost ili će biti izračunata za jediničnu cenu za predmet podugovora.  |
| Cena po jedinici | Podrazumevana vrednost koristi kombinaciju **Kategorije** i **Jedinice** iz cena kategorija koje su povezane sa cenovnikom projekta, što je primenljivo za traženo vreme početka za stavku podugovora. |Ništa |
| Međuiznos | Ovo je polje samo za čitanje koje se izračunava kao „Količina“ X „Jedinična cena“, ako su unete vrednosti za količinu i jediničnu cenu. Ako su jedno ili oba polja prazna, možete uneti vrednost u ovo polje. |Ništa |
| Porez na promet | Unesite iznos poreza na promet. |Ništa |
| Ukupan iznos | Ukupan iznos iz predmeta podugovora uključujući porez. Ovo polje se računa kao međuzbir + porez na promet. |Ništa |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
