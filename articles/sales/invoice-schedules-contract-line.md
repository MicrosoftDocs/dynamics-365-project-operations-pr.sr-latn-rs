---
title: Kreirajte raspored fakturisanja za predmet ugovora zasnovan na projektu
description: Ova tema pruža informacije o kreiranju rasporeda i kontrolnih tačaka fakturisanja na predmetima ugovora.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0da3b3f8f14ecf9a4c4f057cd26c0ca9eb5ec2f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278255"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Kreirajte raspored fakturisanja za predmet ugovora zasnovan na projektu 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Možete da kreirate raspored fakturisanja za predmet ugovora zasnovan na projektu. Fakturisanje je dozvoljeno samo nakon dobijanja ugovora i kada kreirate projektni ugovor. Raspored faktura omogućava automatsko kreiranje nacrta faktura za predmet ugovora zasnovan na projektu. Ako, međutim, samo ručno kreirate fakture, možete preskočiti kreiranje rasporeda faktura na predmetima ugovora.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Napravite raspored za fakturisanje za vreme i materijal za predmet ugovora

Kada predmet ugovora zasnovan na projektu ima način naplate za vreme i materijal, možete da kreirate raspored fakturisanja zasnovan na datumu. Da biste automatski generisali raspored za fakturisanje na osnovu datuma, izvršite sledeće korake.

1. Idite na **Podešavanja** > **Učestalost fakturisanja** i podesite učestalost fakturisanja.
2. Idite na evidenciju ugovora o projektu i na kartici **Rezime** u polju **Traženo vreme dostave** izaberite datum.
3. Otvorite predmet ugovora **Vreme i materijal** za koji kreirate raspored za fakturisanje zasnovan na datumu. 
4. Na kartici **Raspored za fakturisanje** izaberite datum početka obračuna i učestalost fakturisanja.
5. Na podformi izaberite **Generišite raspored za fakturisanje**. Generiše se raspored za fakturisanje pomoću polja **Datum pokretanja fakturisanja**, **Datum isključivanja transakcije** i **Status pokretanja** postavljenih na sledeći način:

    - **Datum pokretanja fakturisanja**: Ovaj datum se podešava na osnovu učestalosti fakturisanja.
    - **Datum isključivanja transakcije**: Dan pre datuma pokretanja fakturisanja.
    - **Status pokretanja**: Automatski se podešava na **Nije pokrenuto**. Kada se posao automatskog kreiranja fakture pokrene za određeni datum pokretanja fakture, ažuriraće ovo polje na **Pokretanje uspešno** ili **Pokretanje nije uspelo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Napravite raspored za fakturisanje za fiksnu cenu za predmet ugovora

Kada predmet ugovora ima način naplate Fiksno, možete da kreirate raspored za fakturisanje zasnovan na kontrolnim tačkama. 

> [!NOTE]
> Kontrolne tačke se ne mogu kreirati na predmetu ugovora ako nema projekta koji je mapiran sa predmetom ugovora.

Dovršite sledeće korake da biste generisali raspored fakturisanja zasnovan na kontrolnim tačakma za fiksni skup podjednako raspoređenih kontrolnih tačaka za kalendarski period.

1. Idite na **Podešavanja** > **Učestalost fakturisanja** i podesite učestalost fakturisanja.
2. Idite na evidenciju ugovora o projektu i na kartici **Rezime** u polju **Traženo vreme dostave** izaberite datum.
3. Otvorite predmet ugovora **Fiksna cena** za koji pravite raspored kontrolnih tačaka. Na kartici **Kontrolne tačke fakturisanja** izaberite datum početka obračuna i učestalost fakturisanja. 
4. Na podformi izaberite **Generišite periodične kontrolne tačke**. Raspored fakturisanja se generiše pomoću polja **Naziv kontrolne tačke**, **Datum kontrolne tačke** i **Iznos kontrolne tačke** postavljenih na sledeći način:

    - **Naziv prekretnice**: Učestalost fakture diktira ovaj naziv.
    - **Datum kontrolne tačke**: Ovaj datum se podešava na osnovu učestalosti fakturisanja.
    - **Iznos kontrolne tačke**: Ovaj iznos se izračunava deljenjem iznosa ugovora u predmetu ugovora sa brojem kontrolnih tačaka, kao što je zadato učestalošću, datumom početka obračuna i datumom zahtevane isporuke.

    Ako predmet ugovora ima vrednost u polju **Procenjeni iznos poreza**, onda se i ovo polje jednako raspoređuje na svaku kontrolnu tačku prilikom generisanja periodičnih kontrolnih tačaka.

Kontrolne tačke za obračun treba da budu jednake ugovornoj vrednosti predmeta ugovora. Ako nisu, dobićete grešku na strani **Predmet ugovora**. Grešku možete ispraviti tako što ćete proveriti da li kontrolne tačke za obračun imaju istu ukupnu vrednost kao ugovorna vrednost linije kreiranjem, uređivanjem ili brisanjem kontrolnih tačaka. Nakon izvršenih promena, osvežite stranicu da biste uklonili grešku.

### <a name="manually-create-milestones"></a>Ručno kreiranje kontrolnih tačaka

Možete da generišete kontrolne tačke sa fiksnom cenom ručno kada se ne dele periodično. Obavite sledeće korake da biste ručno kreirali kontrolnu tačku.

1. Otvorite predmet ugovora sa fiksnom cenom za koji stvarate kontrolnu tačku i na kartici **Raspored fakturisanja**, na podmreži odaberite **+ Kreiraj novu kontrolnu tačku za predmet ugovora**. 
2. Na stranici **Kreiranje kontrolne tačke**, unesite potrebne informacije na osnovu sledeće tabele.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Naziv kontrolne tačke | Brzo kreiranje | Tekstualno polje za ime kontrolne tačke. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Projektni zadatak | Brzo kreiranje | Ako je kontrolna tačka vezana za projektni zadatak, pomoću ove reference možete dodati prilagođenu logiku koja je postavila status kontrolne tačke na osnovu statusa zadatka. | Aplikacija nema nikakvog posledičnog uticaja ove reference na zadatak. |
| Datum kontrolne tačke | Brzo kreiranje | Podesite datum na koji bi postupak automatskog kreiranja fakture trebalo da traži status ove kontrolne tačke da bi se uzeo u obzir za fakturisanje. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Status fakture | Brzo kreiranje | Kada se kreira kontrolna tačka, ovaj status se uvek postavlja na **Nije spremno za fakturisanje** ili **Nije započeto**. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Iznos stavke | Brzo kreiranje | Iznos ili vrednost kontrolne tačke koja će se fakturisati klijentu. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Porez | Brzo kreiranje | Iznos poreza primenjen na kontrolnu tačku. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |

3. Izaberite stavku **Sačuvaj i zatvori**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]