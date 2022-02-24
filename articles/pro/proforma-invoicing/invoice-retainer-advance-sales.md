---
title: Fakturišite avansnu uplatu ili avans
description: Ova tema pruža informacije o tome kako da fakturišete odbitak ili avans u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 12bf3822227badcf8c83d84d6aef6c0fdc7a972a
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596209"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Fakturisanje avansne uplate ili avansa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Dynamics 365 Project Operations podržava ugovore zasnovane na avansnim uplatama i jednokratnim avansima. Na ugovor o projektu možete snimiti raspored odbitaka ili jednokratni avans. Međutim, snimanje na nivou projektnog ugovora ne stavlja odmah odbitak ili avans na raspolaganje za upotrebu. Da biste koristili odbitak ili avans na fakturi koja stvarno zadužuje klijenta, mora se prvo fakturisati odbitak ili avans.

Dovršite sledeće korake da biste fakturisali odbitak ili avans.

1. Izaberite **Prodaja** > **Naplata** > **Odbici i avansi**. 
2. Na stranici **Avansi i odbici** koristite filter da biste izabrali određeni odbitak ili avans za fakturu i označili ga kao **Spremno za fakturisanje**.
3. Napravite fakturu bilo ručno iz liste **Ugovor o projektu** ili sa stranice sa detaljima. Odbitak ili avans je prikazan na nacrtu fakture u odeljku **Avansi i odbici** na stranici **Faktura**.
4. Potvrdite fakturu. Ovo će odbitak ili avans učiniti dostupnim za upotrebu. Fakturu možete verifikovati na stranici liste **Odbici i avansi**. Za fakturisani avans ili odbitak, dostupni iznos je prikazan u mreži.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Napravite odbitak ili avans iz mreže faktura

Možete kreirati odbitak ili avans direktno na fakturi.

1. Na nacrtu fakture, na podmreži **Avansi i odbici**, izaberite **Novo** da biste kreirali novi odbitak ili avans. 
2. Na stranici **Brzo kreiranje**, dodajte potrebne informacije, a zatim izaberite **Sačuvaj**. Odbitak ili avans kreira se na ugovoru o projektu koji se odnosi na fakturu. Odbitak ili avans se automatski označava kao **Spremno za fakturisanje**, a zatim se dodaje na podmrežu **Avansi i odbici** na stranici **Faktura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Sravnjenje fakturisanog odbitka ili avansa

Nakon fakturisanja odbitka ili avansa, oni se mogu koristiti ili sravniti na fakturi sa vremenom, troškovima, kontrolnim tačkama ili drugim projektnim troškovima. Klijent će videti iznos svoje fakture umanjen za odbitak ili avans koji se koristi na ovoj fakturi.

Na svakoj fakturi koja se generiše za projektni ugovor koji fakturiše odbitke ili avanse, Project Operation automatski primenjuje odbitak ili avans na fakturu.

To se može videti u mreži **Primenjeni odbici i avansi** na stranici **Faktura**. Sledeća tabela pruža informacije o poljima na mreži **Primenjeni odbici i avansi** na stranici **Faktura projekta**.

| Polje | Lokacija | Opis | Posledični uticaj |
| --- | --- | --- | --- |
| Opis | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta** |Ovo polje samo za čitanje daje opis odbitaka ili avansa koji se koriste na ovoj fakturi. Ova vrednost ne može da se promeni na fakturi. Ova vrednost se može ažurirati na podmreži na stranici **Ugovor o projektu**. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačilo koji odbitak ili avans se primenjuje na fakturi. |
| Vreme isporuke | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta**  | Ovo polje samo za čitanje daje datum fakture odbitaka ili avansa koji se koriste na ovoj fakturi. Ova vrednost ne može da se promeni na fakturi. Ova vrednost se može ažurirati na podmreži na stranici **Ugovor o projektu**. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačio datum kada su odbitak ili avans prvi put fakturisani klijentu. |
| Iznos | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta**  | Ovo polje samo za čitanje daje iznos odbitka ili avansa koji se koristi na ovoj fakturi. Ova vrednost ne može da se promeni na fakturi. Ova vrednost se može ažurirati na podmreži na stranici **Ugovor o projektu**. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačio originalan iznos odbitka ili avansa koji je klijent platio. |
| Iskorišćen iznos | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta**  | Ovo polje samo za čitanje daje izračunatu vrednost koja sumira koliki je iznos odbitka ili avansa iskorišćen. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačio iznos iz ovog odbitka ili avansa koji je već iskorišćen. |
| Prošireni iznos | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta**  | Ovo polje koje se može urediti daje iznos odbitka ili avansa koji se koristi na ovoj fakturi projekta. Ovaj iznos ne može biti veći od onoga što je dostupno na avansu. Sistem to automatski izračunava kao razliku između polja **Iznos** i **Iskorišćeni iznos** na mreži. Možete smanjiti ovu količinu da biste koristili manje od onoga što je dostupno, ali ne možete povećati količinu da biste koristili više od onoga što je dostupno. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačio iznos iz ovog odbitka ili avansa koji se koristi na fakturi. |
| Iznos bilansa avansa. | Mreža **Primenjeni odbici i avansi** na stranici **Faktura projekta**  | Ovo polje samo za čitanje daje vrednost ostatka odbitka ili avansa nakon potvrde fakture. | Ovo polje se može prikazati klijentu na odštampanoj fakturi kako bi se naznačio iznos koji će ostati iz ovog odbitka ili avansa kada se faktura potvrdi i plati. |
