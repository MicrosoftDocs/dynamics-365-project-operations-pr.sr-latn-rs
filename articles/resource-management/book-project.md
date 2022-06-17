---
title: Rezervisanje za projekat
description: Ovaj članak pruža informacije o rezervisanju resursa za projekat.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: dca9d722eae595af7a81c2b4684729d7658ed012
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928541"
---
# <a name="book-to-a-project"></a>Rezervisanje za projekat

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Postoje slučajevi u kojima će menadžer projekta ili menadžer resursa morati da dodeli resurs projektu, a da od generičkog člana tima nije definisan poseban zahtev. To se može postići na jedan od tri načina.

- Rezervacija iz mreže člana tima
- Rezervisanje sa tabele rasporeda
- Rezervacija iz obrasca **Projekat**

## <a name="book-from-the-team-member-grid"></a>Rezervacija iz mreže člana tima

Ako vaša organizacija radi u hibridnom režimu dodele resursa, menadžer projekta može rezervisati resurs direktno u projekat tako što će izvršiti sledeće korake.

1. Iz projekta idite na mrežu članova tima i izaberite **Novo**.
2. Definišite naziv pozicije i ulogu resursa.
3. Izaberite resurs koji može da se rezerviše iz dostupnog pronalaženja.
4. Kada odaberete resurs, definišite sledeće informacije o polju da biste rezervisali resurs:

    - Datum početka
    - Datum završetka
    - Način dodele
    - Sati, ako je primenljivo
    - Davalac odobrenja za projekat

6. Izaberite stavku **Sačuvaj i zatvori**

## <a name="book-from-the-schedule-board"></a>Rezervisanje sa tabele rasporeda

Kada menadžer resursa treba da rezerviše resurs direktno za projekat, može da koristi tablu rasporeda i zahteve projekta. Zahtev projekta je zahtev za resursom koji je uvek dostupan za rezervisanje. Da biste rezervisali direktno u obrazac projekta iz tabele rasporeda, obavite sledeće korake.

1. Idite na tabelu rasporeda i na levoj stranici filtrirajte resurse koje uzimate u obzir za zahtev.
2. U donjem oknu izaberite karticu **Projekat** da biste videli listu projektnih zahteva.
3. Prevucite zahtev na resurs i definišite sledeće informacije:

    - Datum početka
    - Datum završetka
    - Status rezervacije
    - Metod rezervacije
    - Trajanje
   
   > [!NOTE]
   > Trenutno ne Dynamics 365 Project Operations podržava tablu rasporeda.   

## <a name="book-from-the-project-form"></a>Rezervacija iz obrasca Projekat

Kao menadžer projekta, možda ćete morati da rezervišete resurs za projekat, ali znate samo kriterijume, a ne i naziv resursa. Dovršite sledeće korake da biste pomoću pomoćnika za planiranje pronašli resurs na osnovu bilo kojih dostupnih atributa resursa. 

1. Dođite do projekta i izaberite **Rezerviši** da biste otvorili pomoćnika za planiranje.
2. Pomoću filtera na levoj strani pomoćnika za planiranje, suzite kriterijume i izaberite **Pretraga.**
3. Na osnovu resursa vraćenih u rezultatima, možete rezervisati resurs.

> [!NOTE]
> Ova metoda ne kreira nikakve rezervacije za resurs. Umesto toga, dodaje resurs timu. Kada se član tima doda u projekat, menadžer projekta može koristiti održavanje rezervacija ili produžiti rezervacije da bi potrebne rezervacije dodao resursu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
