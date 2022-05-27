---
title: Detalji zaglavlja za fakture dobavljača
description: Ova tema objašnjava funkcionalnost koja je obezbeđena u zaglavlju fakture dobavljača u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575597"
---
# <a name="header-details-for-vendor-invoices"></a>Detalji zaglavlja za fakture dobavljača

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Ova tema objašnjava funkcionalnost koja je obezbeđena u zaglavlju fakture dobavljača u korporaciji Microsoft Dynamics 365 Project Operations.

Dok menadžeri projekata planiraju i izvršavaju projekte, oni mogu da zapošljavaju podizvođača i proizvode za nabavku i usluge od dobavljača. Tokom izvršenja projekta, troškovi nastaju iz kategorija usluga, materijala i troškova koji se nabavljaju na podizvođačima sa dobavljačima. Dobavljači fakturiše ove troškove projektima kreiranjem faktura dobavljača.

Sledeća tabela pruža informacije o poljima u zaglavljima faktura dobavljača u operacijama projekta.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Ime fakture dobavljača. | U svim padajućim listama fakture dobavljača, ime fakture dobavljača je navedeno u prvoj koloni koja će vam pomoći da identifikujete fakturu dobavljača. Podrazumevano, kada se faktura dobavljača kreira iz podizvođaca, **polje Ime** fakture dobavljača je postavljeno na vrednost koja se sastoji od imena podizvođaca plus trenutnog datuma. |
| Opis | Kratak opis usluga i proizvoda koji se fakturišu u fakturi dobavljača. | Nijedno |
| Prodavac | Ime preduzeća koje se poziva na proizvode i usluge. Ovo preduzeće bi trebalo da bude zapis konta koji ima vrstu relacije "Dobavljač" **ili "** Dobavljač **"**. | <p>Na osnovu izabranog dobavljača, podrazumevane vrednosti se automatski unose u sledeća polja:</p><ul><li>Valuta</li><li>Cenovnici</li><li>Uslovi plaćanja</li><li>Adresa plaćanja</li></ul> |
| Podugovor | Referenca na podizvođaи za fakturu dobavljača. | <p>Na osnovu izabranog podizvođača podrazumevane vrednosti se automatski unose u sledeća polja:</p><ul><li>Valuta</li><li>Cenovnici</li><li>Uslovi plaćanja</li><li>Adresa plaćanja</li></ul><p>Podizvođači koji su izabrani u zaglavlju fakture dobavljača podrazumevano se unose u redove fakture dobavljača i tu se ne mogu menjati.</p> |
| Datum fakture | Datum za stvarne troškove koji će biti kreiran kada se potvrdi faktura dobavljača. | Datum fakture se takođe koristi za izbor tačnog cenovnika nabavke iz cenovnika koji su priloženi povezanom dobavljaču ili iz parametara projekta. |
| Razlog statusa | Status fakture dobavljača. | <p>Status određuje gde se faktura dobavljača nalazi u poslovnom procesu i da li može da se uređuje. Evo nekih od dostupnih vrednosti:</p><ul><li>**Radna verzija** – Faktura dobavljača se može uređivati.</li><li>**Potvrđeno** – Faktura dobavljača je verifikovana i potvrđena. Fakture dobavljača u ovom statusu se ne mogu uređivati ili brisati.</li><li>**U toku** – Faktura dobavljača se rediguje. Fakture dobavljača u ovom statusu mogu da se uređuju, ali ih nije moguće izbrisati.</li><li>**Otkazano** – Faktura dobavljača je otkazana. Fakture dobavljača u ovom statusu se ne mogu uređivati ili brisati.</li></ul> |
| Valuta | Valuta u kojoj dobavljač poziva proizvode i usluge u fakturi dobavljača. | U fakturi dobavljača koja upućuje na podizvođač, valuta podizvođač se podrazumevano unosi kao valuta fakture dobavljača. U fakturu dobavljača koja ne upućuje na podizvođač, podrazumevana vrednost se unosi iz zapisa konta dobavljača i može se promeniti. Nakon što se sačuva faktura dobavljača, valuta se više ne može uređivati. |
| Jedinica ugovaranja | Podela preduzeća koje je odgovorno za prijem usluga i/ili proizvoda od dobavljača. | Nijedno |
| Uslovi plaćanja | Uslovi plaćanja na fakturama dobavljača koji su izdati. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Uslovi plaćanja iz podizvođači se kopiraju u sve fakture dobavljača koje su povezane sa podizvođačima. Uslovi plaćanja se mogu ažurirati ako faktura dobavljača ima status radne **verzije**. |
| Adresa plaćanja | Adresa dobavljača kojem treba poslati uplate. Podrazumevana vrednost se automatski unosi iz zapisa poslovnog kontakta dobavljača. | Adresa uplate iz podizvođači se kopira kao adresa uplate svim fakturama dobavljača koje su kreirane za taj podizvođac. Adresa uplate se može ažurirati ako faktura dobavljača ima status radne **verzije**. |
| Međuiznos | Ako faktura dobavljača nema redove, unesite podzbir fakture pre poreza. Ako faktura dobavljača ima redove, ovo polje se čita samo. U ovom slučaju, prikazani iznos je iznos međuvrednosti iz svih redova u fakturi dobavljača. | Nijedno |
| Ukupan porez | Ako faktura dobavljača nema redove, unesite ukupne poreze u podizvođaи. Ako faktura dobavljača ima redove, ovo polje se čita samo. U ovom slučaju, prikazani iznos je zbir iznosa poreza iz svih redova u fakturi dobavljača. | Nijedno |
| Ukupan iznos | Ovo izračunato polje prikazuje ukupan iznos fakture dobavljača nakon uključenja poreza. | Nijedno |

> [!NOTE]
> Sledeća polja u fakturi dobavljača se ne mogu promeniti nakon uštede fakture dobavljača: "Dobavljač", "Podizvođač", "**Valuta** **", "** Jedinica za ugovaranje **" i "** Uslovi plaćanja"**.** **·** Ako su potrebne neke promene u ovim poljima u fakturi dobavljača, morate izbrisati fakturu dobavljača i kreirati novu fakturu dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
