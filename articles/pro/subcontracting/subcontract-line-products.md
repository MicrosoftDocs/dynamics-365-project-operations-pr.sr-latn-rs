---
title: Predmet podugovora za proizvode
description: Ova tema objašnjava kako evidentirati predmete podugovora za proizvode i koristiti različita polja za beleženje kupovine proizvoda od prodavaca.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558564"
---
# <a name="subcontract-lines-for-products"></a>Predmet podugovora za proizvode

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Podugovor u usluzi Dynamics 365 Project Operations može imati predmet podugovora za proizvode. Ovi predmeti omogućavaju menadžeru projekta da kupuje proizvode od prodavaca koje zatim može koristiti u projektnim zadacima.

Dovršite sledeće korake da biste kreirali predmet podugovora za proizvode u usluzi Project Operations.

1. Na stranici navigacije izaberite **Podugovori**, a zatim otvorite podugovor sa kojim želite da radite. 
2. Na kartici **Predmeti podugovora** izaberite **+ Novo** za kreiranje novog predmeta podugovora.
3. Na stranici **Brzo kreiranje**, u polju **Klasa transakcije** izaberite **Materijal** i unesite ili izaberite potrebne informacije o polju. 
4. Izaberite stavku **Sačuvaj**.

Sledeća tabela pruža informacije o poljima na stranici **Detalji o predmetu podugovora** i stranici **Brzo kreiranje** jer su relevantni za kupovinu proizvoda.

| Polje | Opis | Funkcionalni uticaj|
| ----- | ----------- | ----------- |
| +Ime | Naziv stavke podugovora za pomoć pri identifikaciji. |Ovo će biti prikazano kao prva kolona u svim pretragama zasnovanim na stavkama predmeta podugovora.
| Opis | Kratak opis proizvoda koji se naručuju u okviru predmeta podugovora. | Ništa |
| Tip predmeta | Ovo polje ima podrazumevanu vrednost **Na osnovu količine**. |Ništa |
| Način naplate | Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja podržana u usluzi Project Operations: **Fiksna cena** i **Vreme i materijal**. | Na osnovu izabranog načina obračuna, raspored faktura zasnovan na kontrolnim tačkama je dostupan za stavke podugovora sa metodom naplate po fiksnoj ceni. |
| Klasa transakcije |Ovo polje ima podrazumevanu vrednost **Vreme**. Da biste kreirali predmete podugovora za kupovinu proizvoda, podesite polje **Klasa transakcije** na **Materijal**.  | Ovo ukazuje na to da se predmet podugovora koristi za evidentiranje kupovine proizvoda koji će se koristiti na projektima. |
| Izaberite proizvod | Odaberite da li se proizvod koji se kupuje nalazi u katalogu proizvoda ili je to ručno dodat proizvod. |Ništa |
| Proizvod | Izaberite aktivan proizvod iz kataloga. Ovo polje je dostupno samo kada je **Izaberite proizvod** podešen na **Postojeći**. |Kombinacija **Proizvoda** i **Jedinice** koristiće se kao podrazumevana vrednost ili će biti izračunata za jediničnu cenu za predmet podugovora.
| Ručno dodat proizvod | Unesite naziv ručno dodatog proizvoda. Ovo polje je dostupno samo kada je **Izaberite proizvod** podešen na **Ručno dodat**.  |Kupovna cena se neće automatski popuniti za ručno dodate proizvode.|
| Zahtevani datum isporuke | Unesite željeni datum isporuke proizvoda.| Ovaj datum se takođe koristi za izbor cenovnika projekta iz cenovnika projekta koji su priloženi podugovoru. Cena proizvoda na predmetu podugovora podrazumevano ima vrednost iz tog cenovnika. |
| Ugovoreni datum isporuke | Unesite datum kada je ugovorom ugovorena isporuka proizvoda.  |Ništa|
| Poručena količina | Unesite količinu proizvoda koji se kupuje od prodavca.| Ovo će se koristiti za prikazivanje upozorenja kada vođa projekta koristi količinu veću od ove.|
| Grupa jedinica | Ova vrednost je podrazumevana samo za kataloške proizvode. |Kada su izabrani **Proizvod** i **Traženi datum dostave**, sistem bira važeći cenovnik na osnovu datuma isporuke. Srodne stavke cenovnika se traže za odgovarajući proizvod. Vrednosti jedinice i grupe jedinica podrazumevano su podešene u zapisu stavke cenovnika. |
| Jedinica | Ova vrednost je podrazumevano podešena na jedinicu koja je podešena u zapisu stavke cenovnika. Po potrebi ovo možete promeniti u drugu jedinicu.| Kombinacija proizvoda i jedinice koristi se za određivanje podrazumevane jedinične cene na predmetu podugovora za postojeće kataloške proizvode. |
| Cena po jedinici | Podrazumevane vrednosti jedinične cene se određuju na osnovu kombinacije proizvoda i jedinice iz stavki cenovnika koji se odnose na cenovnik projekta koja se primenjuje za traženi datum isporuke predmeta podugovora.  |Ništa |
| Međuiznos | Ovo polje samo za čitanje izračunava se kao Količina x Jedinična cena ako oba polja imaju unete vrednosti. Ako je polje **Količina**, polje **Cena po jedinici** ili oba polja prazna, vrednost možete uneti ručno.  |Ništa |
| Porez na promet | Unesite vrednost poreza na promet. |Ništa |
| Ukupan iznos | Ovo izračunato polje prikazuje ukupan iznos predmeta podugovora nakon uključivanja poreza. Vrednost u ovom polju se računa kao međuzbir + porez. |Ništa |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
