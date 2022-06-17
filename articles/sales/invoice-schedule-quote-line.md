---
title: Rasporedi fakturisanja na stavkama ponude zasnovane na projektu
description: Ovaj članak pruža informacije o kreiranju rasporeda faktura i prekretnica za redove ponude.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b1e431bc3586f9fef7a01348555e4ee4e06cc66c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918329"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Rasporedi fakturisanja na stavkama ponude zasnovane na projektu

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Stavka ponude zasnovane na projektu daje mogućnost izražavanja rasporeda fakturisanja. Ovo je opcionalno tokom faze ponude, jer aplikacija ne podržava fakturisanje projekta kada je vezano za stavku ponude. Fakturisanje je dozvoljeno samo nakon ostvarenja ponude. Jedini posledični uticaj kreiranja rasporeda fakturisanja tokom faze ponude je taj što se ovaj raspored fakturisanja kopira u predmet ugovora zasnovanog na projektu. Ako tokom faze ponude ne napravite raspored za fakturisanje, to ćete moći da uradite u predmetu ugovora zasnovanom na projektu.

Sve u svemu, svrha rasporeda za fakturisanje je da omogući automatsko kreiranje radnih verzija faktura za predmet ugovora zasnovanog na projektu. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Napravite raspored za fakturisanje za vreme i materijal za stavku ponude zasnovane na projektu

Kada je za stavku ponude zasnovane na projektu izabran način naplate „Vreme i materijal“, sistem generiše raspored za fakturisanje zasnovan na datumu. Da biste automatski generisali raspored za fakturisanje na osnovu datuma, izvršite sledeće korake.

1. Idite na **Podešavanja** > **Učestalost fakturisanja** i podesite učestalost fakturisanja.
2. Na stranici **Ponude** otvorite ponudu za projekat i na kartici **Rezime** podesite traženi datum isporuke.
3. Otvorite stavku ponude za vreme i materijal za koju vam je potrebno da kreirate raspored za fakturisanje zasnovan na datumu. 
4. Na kartici **Raspored za fakturisanje** izaberite vrednosti u poljima **Početak obračuna** i **Učestalost fakturisanja**. 
5. Na podformi izaberite **Generišite raspored za fakturisanje**.
6. Aplikacija generiše raspored za fakturisanje pomoću polja **Datum pokretanja fakturisanja**, **Datum isključivanja transakcije** i **Status pokretanja** postavljenih na sledeći način:

    - **Datum pokretanja fakturisanja** se podešava na datum koji je zadat na osnovu učestalosti fakturisanja.
    - **Datum isključivanja transakcije** se postavlja na dan pre **datuma pokretanja fakturisanja**.
    - **Status pokretanja** se automatski podešava na **Nije pokrenuto**. Kada se posao automatskog kreiranja fakture pokrene za određeni datum pokretanja fakture, ažuriraće ovo polje na **Pokretanje uspešno** ili **Pokretanje nije uspelo**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Napravite raspored za fakturisanje za fiksnu cenu za stavku ponude zasnovane na projektu

Kada stavka ponude zasnovane na projektu ima način naplate **Fiksno**, sistem kreira raspored za fakturisanje zasnovan na kontrolnim tačkama. Dovršite sledeće korake da biste automatski generisali ovaj raspored za fiksni skup kontrolnih tačaka koje su podjednako raspoređene za kalendarski period.

1. Idite na **Podešavanja** > **Učestalost fakturisanja** i podesite učestalost fakturisanja.
2. Na stranici **Ponude** otvorite ponudu za projekat i na kartici **Rezime** podesite traženi datum isporuke.
3. Otvorite stavku ponude sa fiksnom cenom za koju treba da napravite raspored kontrolnih tačaka. 
4. Na kartici **Raspored za fakturisanje** izaberite vrednosti u poljima **Početak obračuna** i **Učestalost fakturisanja**. 
5. Na podformi izaberite **Generišite periodične kontrolne tačke**.
6. Aplikacija generiše raspored za fakturisanje sa nazivom, datumom i iznosom kontrolne tačke.

    - Naziv kontrolne tačke se podešava na datum koji je zadat na osnovu učestalosti fakturisanja.
    - Datum kontrolne tačke se podešava na datum koji je zadat na osnovu učestalosti fakturisanja.
    - Iznos kontrolne tačke se izračunava deljenjem iznosa ponude u stavci ponude zasnovane na projektu sa brojem kontrolnih tačaka, kao što je zadato učestalošću, datumom početka obračuna i datumom zahtevane isporuke.
    - Ako stavka ponude takođe ima procenjeni iznos poreza, ova vrednost se deli jednako između svake kontrolne tačke podjednako prilikom generisanja periodičnih kontrolnih tačaka.

### <a name="manually-create-milestones"></a>Ručno kreiranje kontrolnih tačaka

Kontrolne tačke sa fiksnom cenom mogu se generisati i ručno kada se ne dele periodično. Da biste ručno kreirali kontrolnu tačku:

Otvorite stavku ponude sa fiksnom cenom gde treba da napravite kontrolnu tačku. Na kartici **Raspored fakturisanja**, na podformi, izaberite **+ Napravi novu kontrolnu tačku stavke ponude** i unesite potrebne informacije na osnovu sledeće tabele.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Naziv kontrolne tačke | Brzo kreiranje | Naziv kontrolne tačke. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu |
| Projektni zadatak | Brzo kreiranje | Ako je kontrolna tačka vezana za projektni zadatak, pomoću ove reference možete dodati prilagođenu logiku koja je postavila status kontrolne tačke na osnovu statusa zadatka. | Aplikacija nema nikakvog posledičnog uticaja ove reference na zadatak. |
| Datum kontrolne tačke | Brzo kreiranje | Podesite datum na koji bi postupak automatskog kreiranja fakture trebalo da traži status ove kontrolne tačke da bi se uzeo u obzir za fakturisanje. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Status fakture | Brzo kreiranje | Kada se kreira kontrolna tačka, ovaj status se uvek postavlja na **Nije spremno za fakturisanje**. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Iznos stavke | Brzo kreiranje | Iznos ili vrednost kontrolne tačke koja će se fakturisati klijentu. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |
| Porez | Brzo kreiranje | Iznos poreza koji će se primeniti na kontrolnu tačku. | Ovo se prenosi na kontrolnu tačku predmeta ugovora o projektu i na fakturu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]