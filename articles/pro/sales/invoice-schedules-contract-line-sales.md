---
title: Kreiranje rasporeda fakturisanja za predmet ugovora zasnovan na projektu – jednostavno
description: Ova tema pruža informacije o kreiranju rasporeda faktura i kontrolnih tačaka.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dc0cf92ed7af0353baa0f93fc7fb69e02905f805eb04a7b4c7bc99cfe59da62a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006083"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Kreiranje rasporeda fakturisanja za predmet ugovora zasnovan na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Možete priložiti raspored fakturisanja za predmet ugovora zasnovan na projektu. Fakturisanje je dozvoljeno samo nakon dobijanja ugovora za izradu projektnog ugovora. Rasporedi faktura omogućavaju automatsko kreiranje radnih verzija faktura za predmet ugovora zasnovan na projektu. Ako planirate da fakture uvek kreirate ručno, možete preskočiti kreiranje rasporeda fakturisanja na predmetu ugovora zasnovanom na projektu ili predmetu ugovora.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Kreirajte raspored fakturisanja vremena i materijala za predmet ugovora zasnovan na projektu

Kada predmet ugovora zasnovan na projektu ima način naplate za vreme i materijal, možete da kreirate raspored fakturisanja zasnovan na datumu. Da biste automatski generisali raspored za fakturisanje na osnovu datuma, izvršite sledeće korake.

1. Idite na **Podešavanja** > **Učestalosti faktura** da biste podesili učestalost fakturisanja.
2. Otvorite ugovor za projekat i na kartici **Rezime**, postavite traženi datum isporuke.
3. Otvorite predmet ugovora za vreme i materijal za koji želite da napravite raspored fakturisanja na osnovu datuma. 
4. Na kartici **Raspored fakturisanja** izaberite datum početka obračuna i učestalost fakturisanja. 
5. Na podformi izaberite **Generišite raspored za fakturisanje**.

    Sistem generiše raspored fakturisanja sa sledećim informacijama o polju:

    - **Datum pokretanja fakturisanja** se podešava na datum na osnovu učestalosti fakturisanja.
    - **Datum isključivanja transakcije** se postavlja na dan pre **datum pokretanja fakturisanja**.
    - **Status pokretanja** se automatski podešava na **Nije pokrenuto**. Kada se posao automatskog kreiranja fakture pokrene za određeni **datum pokretanja fakturisanja**, ažuriraće ovo polje na **Pokretanje uspešno** ili **Pokretanje nije uspelo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Kreiranje rasporeda fakturisanja po fiksnoj ceni za predmet ugovora zasnovan na projektu

Kada predmet ugovora zasnovan na projektu ima metodu obračuna sa fiksnom cenom, možete da kreirate raspored fakturisanja zasnovan na kontrolnoj tački. Dovršite sledeće korake da biste automatski generisali raspored fakturisanja na osnovu kontrolnih tačaka za fiksni skup kontrolnih tačaka koje se podjednako raspoređuju za kalendarski period.

1. Idite na **Podešavanja** > **Učestalosti faktura** da biste podesili učestalost fakturisanja.
2. Otvorite ugovor za projekat i na kartici **Rezime**, postavite traženi datum isporuke.
3. Otvorite predmet ugovora sa fiksnom cenom na kojoj treba da napravite raspored kontrolnih tačaka. 
4. Na kartici **Raspored fakturisanja (Kontrolne tačke fakturisanja)** izaberite datum početka obračuna i učestalost fakturisanja. 
5. Na podformi izaberite **Generišite periodične kontrolne tačke**.

    Sistem generiše raspored fakturisanja sa sledećim informacijama o kontrolnim tačkama.

    - **Naziv kontrolne tačke** se podešava na datum koji se diktira na osnovu učestalosti fakturisanja.
    - **Datum kontrolne tačke** se podešava na datum koji se diktira na osnovu učestalosti fakturisanja.
    - **Iznos kontrolne tačke** se izračunava tako što se iznos ugovora na predmetu ugovora zasnovanom na projektu podeli sa brojem kontrolnih tačaka, kako što je to diktirano učestalošću, početkom naplate i traženim datumima isporuke.
    - Ako predmet ugovora ima vrednost u polju **Procenjeni iznos poreza**, ovo polje se takođe ravnomerno raspoređuje na svaku kontrolnu tačku prilikom generisanja periodičnih kontrolnih tačaka.

Kontrolne tačke za obračun bi trebalo da budu jednake ugovorenoj vrednosti predmeta ugovora zasnovanog na projektu. Ako nisu jednake, dolazi do greške. Tu grešku možete da ispravite tako što ćete proveriti da li je zbir kontrolnih tačaka za fakturisanje jednak ugovorenoj vrednosti stavke tako što ćete kreirati, izmeniti ili izbrisati kontrolne tačke. Nakon izvršenih promena, osvežite stranicu.

### <a name="manually-create-milestones"></a>Ručno kreiranje kontrolnih tačaka

Kontrolne tačke sa fiksnom cenom mogu se generisati ručno kada se ne dele periodično. Da biste ručno kreirali kontrolnu tačku, izvršite sledeće korake.

1. Otvorite predmet ugovora sa fiksnom cenom na kojoj želite da napravite kontrolnu tačku. 
2. Na kartici **Raspored fakturisanja**, na podformi izaberite **+ Kreiraj novu kontrolnu tačku za predmet ugovora**.
3. Na obrascu **Kreiranje kontrolne tačke**, unesite potrebne informacije na osnovu sledeće tabele. 

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Naziv kontrolne tačke | Brzo kreiranje | Tekstualno polje za ime kontrolne tačke. | Ovo polje je uključeno u kontrolnu tačku predmeta ugovora za projekat i u fakturu. |
| Projektni zadatak | Brzo kreiranje | Ako je kontrolna tačka vezana za projektni zadatak, koristite ovu referencu da biste dodali prilagođenu logiku i podesili status kontrolne tačke na osnovu statusa zadatka. | Ne postoji posledični uticaj ove reference na zadatak. |
| Datum kontrolne tačke | Brzo kreiranje | Datum kada automatski postupak izrade fakture treba da traži status ove kontrolne tačke da bi se uzeo u obzir za fakturisanje. | Ovo je uključeno u kontrolnu tačku predmeta ugovora za projekat i u fakturu. |
| Status fakture | Brzo kreiranje | Kada se kreira kontrolna tačka, ovaj status se uvek postavlja na **Nije spremno za fakturisanje** ili **Nije započeto**. | Ovo je uključeno u kontrolnu tačku predmeta ugovora za projekat i u fakturu. |
| Iznos stavke | Brzo kreiranje | Iznos ili vrednost kontrolne tačke koja će se fakturisati klijentu. | Ovo polje je uključeno u kontrolnu tačku predmeta ugovora za projekat i u fakturu, |
| Porez | Brzo kreiranje | Iznos poreza primenjen na kontrolnu tačku. | Ovo je uključeno u kontrolnu tačku predmeta ugovora za projekat i u fakturu. |

4. Izaberite stavku **Sačuvaj i zatvori**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]