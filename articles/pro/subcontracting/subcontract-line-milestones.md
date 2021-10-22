---
title: Kontrolne tačke predmeta podugovora
description: Ova tema objašnjava kako da kreirate i održavate raspored faktura zasnovan na kontrolnim tačkama za podugovor sa prodavcem.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7f99853f5f649f96225b7d72580db97bb92de7c5
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558519"
---
# <a name="subcontract-line-milestones"></a>Kontrolne tačke predmeta podugovora

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U aplikaciji Dynamics 365 Project Operations, predmet podugovora sa metodom naplate po fiksnoj ceni može da navede raspored faktura na osnovu kontrolnih tačaka za prodavca.

Kontrolne tačke za fakturisanje prodavaca mogu se generisati automatski pomoću podešene učestalosti ili ih možete kreirati ručno.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatski kreirajte raspored faktura na osnovu kontrolnih tačaka za predmet podugovora

Dovršite sledeće korake da biste automatski generisali raspored faktura zasnovan na kontrolnim tačkama za fiksni skup ravnomerno raspoređenih kontrolnih tačaka.

1. Idite na **Podešavanja** > **Učestalosti faktura** i podesite učestalost faktura za predmete podugovora.
2. Otvorite stranicu **Podugovori**, otvorite podugovor sa kojim želite da radite, a zatim otvorite predmet podugovora sa fiksnom cenom za koju ćete napraviti raspored kontrolnih tačaka.
3. Na kartici **Kontrolne tačke za predmete podugovora** izaberite **Generišite periodične kontrolne tačke**.
4. U dijalogu unesite ili izaberite opseg datuma, broj kontrolnih tačaka i učestalost faktura. Možete izabrati datum početka, ili možete izabrati broj kontrolnih tačaka i učestalost faktura ili datum početka, ili možete izabrati datum završetka i učestalost faktura. Ne možete da izaberete datum završetka i broj kontrolnih tačaka.
Koristeći ove informacije, sistem generiše kontrolne tačke i zapise koji su prikazani na mreži **Kontrolne tačke**.

   - **Ime kontrolne tačke** – Ime kontrolne tačke je podešeno na datum kontrolne tačke na osnovu učestalosti faktura.
   - **Datum kontrolne tačke** – Datum zasnovan na učestalosti faktura.
   - **Količina kontrolne tačke** – Izračunava se deljenjem iznosa međuzbira na predmetu podugovora sa brojem kontrolnih tačkaka.

Ako predmet podugovora ima vrednost u polju **Procenjeni iznos poreza**, ova vrednost se dodaje svakoj kontrolnoj tački podjednako pri generisanju periodičnih kontrolnih tačaka.

Zbir iznosa kontrolnih tačaka predmeta podugovora treba da bude jednak vrednosti predmeta podugovora. Ako nisu jednake, dolazi do greške. Možete da ispravite grešku i proverite da li je ukupan iznos kontrolnih tačaka jednak vrednosti predmeta podugovora tako što ćete kreirati, urediti ili izbrisati kontrolne tačke i iznose poreza. Nakon što unesete promene, sačuvajte i osvežite stranicu kako biste bili sigurni da nema više grešaka.

## <a name="manually-create-subcontract-line-milestones"></a>Ručno kreiranje kontrolnih tačaka predmeta podugovora

Kontrolne tačke sa fiksnom cenom na predmetu podugovora mogu se generisati ručno ako se periodično ne dele. Da biste ručno kreirali kontrolnu tačku predmeta podugovora, obavite sledeće korake.

1. Na stranici navigacije izaberite **Podugovori** i otvorite podugovor sa kojim želite da radite.
2. Otvorite predmet podugovora sa fiksnom cenom za koji želite da napravite kontrolnu tačku.
3. Na kartici **Kontrolne tačke predmeta podugovora**, na podformi izaberite **+ Nova kontrolna tačka za predmet podugovora**.
4. Na stranici **Nova kontrolna tačka za predmet podugovora** unesite potrebne podatke na osnovu sledeće tabele.

    | Polje | Opis |Funkcionalni uticaj|
    | --- | --- |----------------------|
    | Naziv kontrolne tačke | Naziv kontrolne tačke. |Ovo će biti prikazano kao prva kolona u svim pretragama zasnovanim na kontrolnim tačkama predmeta podugovora. Stavka fakture dobavljača koja je kreirana na osnovu ove kontrolne tačke takođe će koristiti naziv kontrolne tačke stavke podugovora kao podrazumevani naziv stavke fakture dobavljača.|
    | Opis | Opis kontrolne tačke. |Stavka fakture dobavljača koja je kreirana na osnovu ove kontrolne tačke takođe će koristiti opis kontrolne tačke stavke podugovora kao podrazumevani opis stavke fakture dobavljača.|
    | Datum kontrolne tačke | Datum kada bi proces automatskog kreiranja fakture trebalo da traži status ove kontrolne tačke kako bi se uzeo u obzir za fakturisanje.| Ova vrednost će se koristiti kao podrazumevani datum stavke fakture dobavljača prilikom fakturisanja za ovu stavku podugovora. |
    | Iznos | Iznos ili vrednost kontrolne tačke koja će se fakturisati klijentu. |Ova vrednost se koristi kao podrazumevani iznos stavke fakture dobavljača prilikom fakturisanja za ovu stavku podugovora. |
    | Porez | Iznos poreza primenjen na kontrolnu tačku.| Ova vrednost se koristi kao podrazumevani iznos poreza za stavku fakture dobavljača prilikom fakturisanja za ovu stavku podugovora. |
    | Iznos sa porezom | Ovo polje je samo za čitanje izračunava se kao iznos + porez.|Ova vrednost se koristi kao podrazumevana za stavku fakture dobavljača prilikom fakturisanja za ovu stavku podugovora. |
    | Status fakture | Kada se kontrolna tačka kreira, ovaj status je uvek podešen na **Nije spremno za fakturisanje**.|  Kada je status **Spremno za fakturisanje**, kreiranje fakture prodavca uključuje ovu kontrolnu tačku na fakturi prodavca. |

5. Izaberite stavku **Sačuvaj i zatvori**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
