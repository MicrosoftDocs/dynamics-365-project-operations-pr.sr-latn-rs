---
title: Predmet podugovora za proizvode
description: Ova tema objašnjava kako evidentirati predmete podugovora za proizvode i koristiti različita polja za beleženje kupovine proizvoda od prodavaca.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323703"
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

| Polje | Opis |
| ----- | ----------- |
| +Ime | Naziv predmeta podugovora. |
| Opis | Kratak opis proizvoda koji se naručuju u okviru predmeta podugovora. |
| Tip predmeta | Ovo polje ima podrazumevanu vrednost **Na osnovu količine**. |
| Način naplate |  Način naplate predmeta podugovora. Raspored faktura na osnovu kontrolne tačke dostupan je za načine naplate po fiksnoj ceni. |
| Klasa transakcije | Ovo polje ima podrazumevanu vrednost **Vreme**. Da biste kreirali predmete podugovora za kupovinu proizvoda, u polju **Klasa transakcije** izaberite **Materijal**. Ovaj izbor ukazuje na to da se predmet podugovora koristi za evidentiranje kupovine proizvoda koji će se koristiti na projektima. |
| Izaberite proizvod | Odaberite da li se proizvod koji se kupuje nalazi u katalogu proizvoda ili je to ručno dodat proizvod. |
| Proizvod | Izaberite aktivan proizvod iz kataloga. Ovo polje je dostupno samo kada je **Izaberite proizvod** podešen na **Postojeći**. |
| Ručno dodat proizvod | Unesite naziv ručno dodatog proizvoda. Ovo polje je dostupno samo kada je **Izaberite proizvod** podešen na **Ručno dodat**.  |
| Zahtevani datum isporuke | Odaberite željeni datum isporuke proizvoda. Ovaj datum se takođe koristi za izbor cenovnika projekta iz cenovnika projekta koji su priloženi podugovoru. Cena proizvoda na predmetu podugovora podrazumevano ima vrednost iz tog cenovnika. |
| Ugovoreni datum isporuke | Odaberite datum kada je ugovorom dogovorena isporuka proizvoda.  |
| Poručena količina | Unesite količinu proizvoda koji se kupuje od prodavca. Ako menadžer projekta prekorači ovu količinu, pojaviće se upozorenje. |
| Grupa jedinica | Ova vrednost je podrazumevana samo za kataloške proizvode. Kada su izabrani **Proizvod** i **Traženi datum dostave**, sistem bira važeći cenovnik na osnovu datuma isporuke. Srodne stavke cenovnika se traže za odgovarajući proizvod. Vrednosti jedinice i grupe jedinica podrazumevano su podešene u zapisu stavke cenovnika. |
| Jedinica | Ova vrednost je podrazumevana za podešavanje jedinice u zapisu stavke cenovnika. Po potrebi ovo možete promeniti u drugu jedinicu. Kombinacija proizvoda i jedinice koristi se za određivanje podrazumevane jedinične cene na predmetu podugovora za postojeće kataloške proizvode. |
| Cena po jedinici | Podrazumevane vrednosti jedinične cene se određuju na osnovu kombinacije proizvoda i jedinice iz stavki cenovnika koji se odnose na cenovnik projekta koja se primenjuje za traženi datum isporuke predmeta podugovora.  |
| Međuiznos | Ovo polje samo za čitanje izračunava se kao Količina x Jedinična cena ako oba polja imaju unete vrednosti. Ako je polje **Količina**, polje **Cena po jedinici** ili oba polja prazna, vrednost možete uneti ručno.  |
| Porez na promet | Unesite vrednost poreza na promet. |
| Ukupan iznos | Ovo izračunato polje prikazuje ukupan iznos predmeta podugovora nakon uključivanja poreza. Vrednost u ovom polju se računa kao međuzbir + porez. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
