---
title: Predmeti podugovora za kategorije troškova
description: Ova tema objašnjava kako evidentirati predmete podugovora za trošak i koristiti polja za beleženje vremena kupovine od prodavaca.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323838"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Predmeti podugovora za kategorije troškova

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Podugovor u usluzi Dynamics 365 Project Operations može imati predmet za kategorije troškova. Predmeti podugovora za kategorije troškova dozvoljavaju menadžeru projekta da kupuje kategorije usluga ili proizvoda od prodavaca koje mogu da naplate na ime projekta.

Dovršite sledeće korake da biste kreirali predmet podugovora za kategorije troškova u usluzi Project Operations.

1. Na stranici navigacije izaberite **Podugovori** i otvorite podugovor sa kojim želite da radite.
2. Na kartici **Predmeti podugovora** izaberite **Novo** za kreiranje novog predmeta.
3. Na stranici **Brzo kreiranje**, u polju **Klasa transakcije** izaberite **Trošak** i unesite ili izaberite bilo koje druge potrebne informacije o polju.

Sledeća tabela pruža informacije o poljima na stranici sa detaljima **Predmet podugovora** i stranici **Brzo kreiranje**.

| **Polje** |  **Opis** |
| ----------| ---------------- |
| +Ime | Naziv predmeta podugovora. |
| Opis | Kratak opis kategorija usluga ili proizvoda koji se kupuju u okviru predmeta podugovora. |
| Tip predmeta | Ovo polje ima podrazumevanu vrednost **Na osnovu količine**.  |
| Način naplate | Način naplate predmeta podugovora. Na osnovu načina naplate predmeta, raspored faktura zasnovan na kontrolnim tačkama je dostupan za način naplate po fiksnoj ceni.  |
| Klasa transakcije | Ovo polje ima podrazumevanu vrednost **Vreme**. Da biste kreirali predmete podugovora za kupovinu proizvoda, podesite polje **Klasa transakcije** na **Trošak**. Vrednost ovog polja ukazuje na to da se predmet podugovora koristi za evidentiranje kategorije proizvoda ili usluga koji će se koristiti na projektima. |
| Kategorija transakcije | Izaberite kategoriju transakcije. |
| Zahtevani početak | Datum kada kategorije kupovine moraju biti dostupne od prodavca. Zahtevani početak se takođe koristi za izbor cenovnika projekta iz cenovnika projekta koji su priloženi podugovoru. Cena kategorije na predmetu podugovora podrazumevano ima vrednost iz tog cenovnika. |
| Zahtevani završetak | Datum kada kategorije kupovine više nisu potrebne. Ovaj datum prikazuje upozorenje kada menadžer projekta poveže ovaj predmet podugovora sa konkretnim procenama troškova za projekte koji su datirani posle ovog datuma. |
| Poručena količina | Količina kategorije koja se kupuje od prodavca. Kada menadžer projekta prekorači kupljenu količinu, pojaviće se upozorenje.  |
| Grupa jedinica | Ova vrednost polja ima podrazumevanu vrednost na osnovu podrazumevane grupe jedinica koja je postavljena za odabranu kategoriju. |
| Jedinica | Ova vrednost polja ima podrazumevanu vrednost na osnovu podrazumevane jedinice postavljene za odabranu kategoriju. Kombinacija kategorije i jedinice koristi se za izračunavanje podrazumevane jedinične cene na predmetu podugovora. |
| Cena po jedinici | Podrazumevane vrednosti vrednosti polja jedinične cene određuju se na osnovu kombinacije kategorije i jedinice iz cena kategorija koje se odnose na cenovnik projekta koja se primenjuje za traženi početak predmeta podugovora.  |
| Međuiznos | Ovo polje samo za čitanje automatski se računa kao jedinična cena količine ako se unesu i vrednosti količine i jedinične cene. Ako su bilo koje ili oba polja prazni, vrednost u ovo polje možete uneti ručno.  |
| Porez na promet | Unesite iznos poreza na promet.  |
| Ukupan iznos | Ukupan iznos iz predmeta podugovora uključujući porez. Ovo polje se računa kao međuzbir + porez na prodaju.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
