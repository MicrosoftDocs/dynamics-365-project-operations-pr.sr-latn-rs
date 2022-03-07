---
title: Kreiranje rezervacije u projektu iz tabele rasporeda
description: Ova tema pruža informacije o tome kako da kreirate rezervaciju u projektu na tabeli rasporeda.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083597"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Kreiranje rezervacije u projektu iz tabele rasporeda

Možete da rezervišete resurs za projekat direktno na kartici **Tim** za projekat ili da generišete potrebu za resursom iz dodele generičkog člana tima, a da zatim ispunite generisanu potrebu članom projektnog tima.

Možete i da rezervišete resurs za projekat direktno iz tabele rasporeda. To može da se uradi na tri načina:

- **Rezervisanje iz generisane potrebe za resursom:** Potrebu za resurs možete da generišete nakon što kreirate generički resurs i dodelite zadatke unutar projekta.

- **Rezervisanje iz primarne potrebe:** Primarne potrebe se pojavljuju na tabeli rasporeda na kartici **Projekat**. 

- **Rezervisanje iz nove potrebe za resursom:** Možete da kreirate potrebu za resursom ispočetka i povežete je sa projektom. Na tabeli rasporeda, potreba za resursom se prikazuje na kartici **Otvorene potrebe**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervisanje iz generisanog zahteva za resursom

Možete da kreirate generički resurs i da mu dodelite zadatak ili više zadataka u okviru projekta. Zatim možete da generišete potrebu za resursom za generičkog člana tima. 

1.  Na tabeli rasporeda, ovaj resurs će se prikazati na kartici **Otvorene potrebe**. Možda ćete morati da koristite filtere kolona na mreži ukoliko imate mnogo otvorenih zahteva. 

    ![Otvaranje kartice Zahtevi na tabeli rasporeda](media/FAQ-Project-Booking-Schedule-Board-1.png "Snimak ekrana tabele rezervacija i dodela")

2. Izaberite zahtev. Kartica **Pretraga dostupnosti** će se pojaviti pri vrhu izabranog reda.
 
3. Kada izaberete karticu, pokreće se režim Pomoćnik za zakazivanje u tabeli rasporeda, a zatim filtrira dostupne resurse koji ispunjavaju potrebe za resursima. Posle toga možete da rezervišete resurs.

4. Možete i da prevučete i otpustite izabrani red sa dna tabele rasporeda u ćeliju resursa na mreži iznad. Kada ga spustite, on otvara tablu **Kreiranje rezervacije resursa** sa desne strane.

    Izbor opcije **Rezerviši** rezerviše resurs u projektnom timu.

![Tabla Kreiranje rezervacije resursa](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervisanje iz primarnog zahteva

Kreiranje projekta u programu Project Service automatski kreira zahtev za resursom pod imenom Primarni zahtev. To je prazan zahtev koji se koristi za brzo rezervisanje resursa pomoću tabele rasporeda bez generisanja zahteva ili kreiranja zahteva iz početka. Pošto je zahtev prazan, moraćete da navedete datume, kao i način dodele i sate ako je to primenljivo. 

1. Da biste rezervisali resurs sa primarnim zahtevom, u tabeli rasporeda izaberite karticu **Projekat**. Možda ćete morati da koristite filter kolone za kolonu **Projekat** ukoliko imate više projekata.

   ![Filteri kolone na tabli rasporeda](media/FAQ-Project-Booking-Schedule-Board-2.png "Snimak ekrana tabele rezervacija i dodela")

2. Izaberite zahtev koji ima samo ime projekta kao svoje ime i čije trajanje iznosi nula (0).

3. Izaberite karticu **Pretraga dostupnosti** koja se pojavljuje u redu. Na taj način tabela rasporeda ulazi u režim Pomoćnik za zakazivanje i prikazuje dostupne resurse koje je moguće rezervisati za projekat.

4. Pošto je **Primarni zahtev** prazan zahtev čije trajanje iznosi nula (0), moraćete da podesite trajanje na tabli **Kreiranje rezervacije resursa** prilikom izbora i rezervisanja resursa.

5. Možete i da izaberete **Primarni zahtev projekta** u dnu tabele rasporeda i da ga prevučete do resursa da biste ga rezervisali.
 
    Pošto je **Primarni zahtev** prazan zahtev čije trajanje iznosi nula (0), moraćete da podesite trajanje na tabli **Kreiranje rezervacije resursa** prilikom izbora i rezervisanja resursa.
 
    Kada rezervišete resurs putem **primarnog zahteva** u tabeli rasporeda, dodajete ga u projektni tim bez ijedne dodele.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervisanje iz novog zahteva za resursom
Obavite sledeće korake da biste obavili rezervaciju iz nove potrebe za resursom. 

1. Idite na **Potrebe za resursima**, a zatim izaberite **Novi** da biste kreirali novu potrebu za resursom.

2. Na kartici **Projekat** odaberite projekat kako biste povezali zahtev i projekat.
 
    U tabeli rasporeda, ovaj novi zahtev se prikazuje kao **Otvoreni zahtev** koji možete da popunite.

3. Rezervišite resurs da biste ga dodali u projektni tim.

4. Sada kada je resurs rezervisan, morate da mu ručno dodelite zadatke.

