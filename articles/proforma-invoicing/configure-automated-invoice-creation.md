---
title: Konfigurisanje automatskog kreiranja fakture
description: Ova tema pruža informacije o načinima konfigurisanja sistema za automatsko generisanje faktura.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 894e8f6e4ffbb5f003cdd1f69594e2a1e043b514923de5673d7ba9afaa6894e8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992673"
---
# <a name="configure-automatic-invoice-creation"></a>Konfigurisanje automatskog kreiranja fakture

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Dovršite sledeće korake da biste konfigurisali automatsko pokretanje faktura usluzi Dynamics 365 Project Operations.

1. Idite do stavke **Podešavanja** > **Grupni poslovi**.
2. Kreirajte grupni posao i imenujte ga **Kreiranje faktura u usluzi Project Operations**. Naziv grupnog posla mora da sadrži reči „kreiranje faktura“.
3. U polju **Tip posla** izaberite **Nijedan**. Podrazumevano se opcije **Dnevna učestalost** i **Je aktivna** podešavaju na **Da**.
4. Izaberite **Pokreni tok posla**. U dijalogu **Pronalaženje zapisa** ćete videti tri toka posla:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Izaberite **ProcessRunCaller**, a zatim **Dodaj**.
6. U sledećem dijalogu izaberite **U redu**. Tok posla **Hibernacija** prati tok posla **Proces**.

  > [!NOTE]
  > Možete izabrati i **ProcessRunner** u koraku 5. Nakon toga, kada izaberete **U redu**, tok posla **Proces** će biti praćen tokom posla **Hibernacija**.

Tokovi posla **ProcessRunCaller** i **ProcessRunner** kreiraju fakture. **ProcessRunCaller** poziva **ProcessRunner**. **ProcessRunner** je tok posla koji zapravo kreira fakture. On prolazi kroz sve predmete ugovora za koje se moraju kreirati fakture i kreira fakture za te predmete. Da bi odredio predmete ugovora za koje fakture moraju biti kreirane, posao traži datume pokretanja fakture za predmete ugovora. Ako predmeti ugovora koji pripadaju jednom ugovoru imaju isti datum pokretanja fakture, transakcije se kombinuju u jednu fakturu koja ima dve stavke fakture. Ako ne postoje transakcije za koje treba kreirati fakture, posao preskače kreiranje fakture.

Nakon što se **ProcessRunner** pokrene, on poziva **ProcessRunCaller**, obezbeđuje vreme završetka i zatvara se. **ProcessRunCaller** zatim pokreće tajmer koji će biti pokrenut tokom perioda od 24 časa od određenog vremena završetka. Na kraju tajmera **ProcessRunCaller** se zatvara.

Posao grupne obrade za kreiranje faktura je periodični posao. Ako se ova grupna obrada pokreće više puta, kreira se više instanci posla i izazivaju greške. Zbog toga bi trebalo samo jednom da pokrenete grupnu obradu i trebalo bi da je ponovo pokrenete samo ako prestane da radi.

> [!NOTE]
> Grupno fakturisanje se izvodi samo za predmete ugovora o projektu koji su konfigurisani prema rasporedima faktura. Predmet ugovora sa načinom naplate uz fiksnu cenu mora da ima konfigurisane kontrolne tačke. Predmet ugovora za projekat sa načinom naplate vremena i materijala treba da uspostavi raspored faktura na osnovu datuma. Isto se odnosi i na predmet ugovora zasnovan na projektu.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]