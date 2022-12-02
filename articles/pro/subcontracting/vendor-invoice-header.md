---
title: Detalji za zaglavlje faktura dobavljača
description: Ovaj članak objašnjava funkcionalnost koja je obezbeđena u zaglavlju fakture dobavljača u programu Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261700"
---
# <a name="header-details-for-vendor-invoices"></a>Detalji za zaglavlje faktura dobavljača

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ovaj članak objašnjava funkcionalnost koja je obezbeđena u zaglavlju fakture dobavljača u programu Microsoft Dynamics 365 Project Operations.

Kako menadžeri projekata planiraju i izvršavaju projekte, mogu zaposliti podizvođače i kupovati proizvode i usluge od prodavaca. Tokom izvršenja projekta, troškovi nastaju iz kategorija usluga, materijala i troškova koji se nabavljaju od podizvođača sa prodavcima. Dobavljači fakturišu ove troškove projektima kreiranjem faktura prodavca.

Sledeća tabela pruža informacije o poljima na zaglavljima fakture dobavljača u programu Project Operations.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Naziv fakture dobavljača. | Na svim padajućim listama faktura prodavca, naziv fakture dobavljača naveden je u prvoj koloni kako bi vam pomogao da identifikujete fakturu dobavljača. Podrazumevano, kada se faktura prodavca kreira iz podugovora, polje **Naziv** fakturi dobavljača je postavljeno na vrednost koja se sastoji od naziva podugovarača plus trenutnog datuma. |
| Opis | Kratak opis usluga i proizvoda koji se fakturišu na fakturi dobavljača. | Nijedno |
| Prodavac | Naziv preduzeća koja fakturiše proizvode i usluge. Preduzeće treba da bude zapis poslovnog kontakta koji ima vrstu odnosa **Prodavac** ili **Dobavljač**. | <p>Na osnovu izabranog dobavljača, podrazumevane vrednosti se automatski unose u sledeća polja:</p><ul><li>Valuta</li><li>Cenovnici</li><li>Uslovi plaćanja</li><li>Adresa plaćanja</li></ul> |
| Podugovor | Referenca na podugovor za fakturu dobavljača. | <p>Na osnovu izabranog podugovora, podrazumevane vrednosti se automatski unose u sledeća polja:</p><ul><li>Valuta</li><li>Cenovnici</li><li>Uslovi plaćanja</li><li>Adresa plaćanja</li></ul><p>Podugovor koji je izabran u zaglavlju fakture dobavljača podrazumevano se unosi u redove fakture dobavljača i tu se ne mogu menjati.</p> |
| Datum fakture | Datum za stvarne vrednosti cena koji će biti kreiran kada se potvrdi faktura prodavca. | Datum fakture se takođe koristi za izbor ispravnog cenovnika za nabavku, bilo iz cenovnika koji su priloženi povezanom dobavljaču ili iz parametara projekta. |
| Razlog statusa | Status fakture dobavljača. | <p>Status određuje gde se faktura prodavca nalazi u poslovnom procesu i da li se može urediti. Evo nekih od dostupnih vrednosti:</p><ul><li>**Radna verzija** – Faktura prodavca može da se uređuje.</li><li>**Potvrđeno** – Faktura dobavljača je verifikovana i potvrđena. Fakture prodavca sa ovim statusom ne mogu se uređivati ili izbrisati.</li><li>**U toku** – Faktura dobavljača se rediguje. Fakture prodavca sa ovim statusom mogu se uređivati, ili se ne mogu izbrisati.</li><li>**Otkazano** – Faktura prodavca je otkazana. Fakture prodavca sa ovim statusom ne mogu se uređivati ili izbrisati.</li></ul> |
| Valuta | Valuta u kojoj prodavac fakturiše proizvode i usluge na fakturi dobavljača. | Na fakturi dobavljača koja upućuje na podugovor, valuta podugovora se podrazumevano unosi kao valuta fakture dobavljača. Na fakturi dobavljača koja ne upućuje na podugovor, podrazumevana vrednost se unosi iz zapisa poslovnog kontakta prodavca i može se promeniti. Nakon što se sačuva faktura prodavca, valuta se više ne može uređivati. |
| Jedinica ugovaranja | Podela preduzeća koje je odgovorno za prijem usluga i/ili proizvoda od prodavca. | Nijedno |
| Uslovi plaćanja | Uslovi plaćanja na fakturama prodavca koje su izdate. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Uslovi plaćanja iz podugovora kopiraju se na sve fakture dobavljača koje su povezane sa ovim podugovorom. Uslovi plaćanja se mogu ažurirati ako faktura prodavca ima status **Radna verzija**. |
| Adresa plaćanja | Adresa dobavljača kojem treba poslati uplate. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Adresa za plaćanje iz podugovora kopira se kao adresa za plaćanje na sve fakture dobavljača koje su kreirane za ovaj podugovor. Adresa za plaćanje se može ažurirati ako faktura prodavca ima status **Radna verzija**. |
| Međuiznos | Ako faktura prodavca nema redove, unesite međuzbir fakture pre oporezivanja. Ako faktura prodavca ima redove, ovo polje je samo za čitanje. U tom slučaju, iznos koji je prikazan je međuzbir iz svih stavki na fakturi dobavljača. | Nijedno |
| Ukupan porez | Ako faktura prodavca nema redove, unesite ukupan iznos poreza na podugovoru. Ako faktura prodavca ima redove, ovo polje je samo za čitanje. U tom slučaju, iznos koji je prikazan je zbir iznosa poreza svih redova na fakturi dobavljača. | Nijedno |
| Ukupan iznos | Ovo izračunato polje prikazuje ukupan iznos iz fakture dobavljača nakon uključivanja poreza. | Nijedno |

> [!NOTE]
> Sledeća polja na fakturi dobavljača se ne mogu promeniti nakon čuvanja fakture dobavljača: **Prodavac**, **Podugovor**, **Valuta**, **Jedinica za ugovaranje** i **Uslovi plaćanja**. Ako su potrebne neke promene u ovim poljima na fakturi dobavljača, morate izbrisati fakturu dobavljača i kreirati novu fakturu dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
