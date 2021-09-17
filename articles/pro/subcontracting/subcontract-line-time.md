---
title: Predmeti podugovora za vreme
description: Ova tema objašnjava kako snimiti predmete podugovora za vreme i evidentirati kupovinu vremena od prodavaca.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323883"
---
# <a name="subcontract-lines-for-time"></a>Predmeti podugovora za vreme

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Podugovor u usluzi Dynamics 365 Project Operations može imati predmet podugovora za vreme. Predmeti podugovora za vreme omogućavaju menadžeru projekta da kupuje vreme resursa prodavca za osoblje projektnih zadataka i potrebe za resursima.

Dovršite sledeće korake da biste kreirali predmet podugovora za vreme u usluzi Project Operations.

1. U oknu za navigaciju izaberite **Podugovori**, i otvorite podugovor.
2. Na kartici **Predmeti podugovora** izaberite **Novo** za kreiranje novog predmeta podugovora.
3. Na stranici **Brzo kreiranje**, u polju **Klasa transakcije** izaberite **Vreme**.
4. Unesite preostale informacije za polje, a zatim izaberite **Sačuvaj**.

  Sledeća tabela pruža informacije o poljima na stranici **Predmet podugovora** i stranici **Brzo kreiranje**.

| **Polje** | **Opis** |
| --- | --- |
| +Ime | Naziv predmeta podugovora. |
| Opis | Kratak opis usluga koje se kupuju u okviru predmeta podugovora. | 
| Tip predmeta | Ovo polje je podrazumevana vrednost.  |
| Način naplate | Izaberite način naplate. Na osnovu načina naplate referentnog predmeta podugovora, raspored faktura zasnovan na kontrolnim tačkama je dostupan za način naplate po fiksnoj ceni. |
| Klasa transakcije | Ovo polje je podrazumevana vrednost koja označava da li se predmet podugovora koristi za evidentiranje kupovine vremena podizvođača. |
| Uloga | Uloga resursa podugovarača čije se vreme kupuje. Uloga dodeljena resursima podugovarača određuje cenu kupovine. |
| Zahtevani početak | Datum kada su potrebni resursi podizvođača za početak rada. Zahtevani početak se takođe koristi za izbor cenovnika projekta iz cenovnika projekta koji su priloženi podugovoru. Cena ugovora na predmetu podugovora podrazumevano ima vrednost iz tog cenovnika. |
| Zahtevani završetak | Datum kada se dodeljivanje resursa podizvođača završava. Ovaj datum se koristi za prikazivanje upozorenja kada menadžer projekta koristi ovaj kapacitet za potrebe resursa koji se javljaju nakon tog datuma. |
| Poručena količina | Broj sati uloge koji se kupuju od prodavca. Ova vrednost se koristi za prikazivanje upozorenja kada menadžer projekta previše koristi ovaj kapacitet za potrebe resursa. |
| Grupa jedinica | Ova vrednost polja je podrazumevano grupa vremenskih jedinica i ne može se promeniti.  |
| Jedinica | Ovo polje podrazumevano ima vrednost sati osnovnih jedinica grupe vremenskih jedinica. Ovu vrednost možete promeniti da biste kupili bilo koju jedinicu iz grupe vremenskih jedinica, na primer dan ili nedelju. Kombinacija uloge i jedinice koristi se za izračunavanje podrazumevane jedinične cene na predmetu podugovora. |
| Cena po jedinici | Podrazumevane vrednosti jedinične cene se određuju na osnovu kombinacije uloge i jedinice iz cenovnika koji se odnose na traženi datum početka predmeta podugovora. Kada je na važećem cenovniku projekta cena postavljena u različitoj jedinici od jedinice na predmetu podugovora, sistem koristi konverziju jedinice za izračunavanje jedinične cene. |
| Međuiznos | Ovo je polje samo za čitanje koje se automatski računa kao **Količina x jedinična cena** ako se unesu i vrednosti količine i jedinične cene. Ako je količina, cena po jedinici ili oba polja prazna, vrednost možete uneti u polje. |
| Porez na promet |  Unesite iznos poreza na promet. |
| Ukupan iznos | Ukupan iznos iz predmeta podugovora nakon uključivanja poreza. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
