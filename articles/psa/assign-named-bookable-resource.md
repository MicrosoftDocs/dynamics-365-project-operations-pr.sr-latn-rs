---
title: Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka
description: Ova tema pruža informacije o tome kako da rezervišete imenovane resurse za projektne timove i dodeljujete ih zadacima.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575367"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Rezervisanje imenovanih resursa koje je moguće rezervisati za projektni tim i dodeljivanje zadataka 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Možete da dodate imenovani resurs u projektni tim tako što ćete ga direktno rezervisati za tim. Da biste to uradili, obavite sledeće korake.

1. U aplikaciji Project Service Automation idite na **Projekat** i otvorite projekat za koji rezervišete resurse.
2. Na stranici **Projekat**, na kartici **Tim** kliknite na **Novo**. 

![Dodavanje člana tima na kartici Tim.](media/RM-how-to-1.png)

3. U dijalogu **Brzo kreiranje člana projektnog tima** izaberite resurs koji se može rezervisati. Polje **Uloga** će se popuniti podrazumevanom ulogom resursa ako je ona dodeljena. Možete da promenite ulogu ako je potrebno. 
4. Izaberite datum početka i završetka, odnosno period u kome vam resurs treba i izaberite način dodele kapaciteta resursa. 
5. Ako želite da član tima bude osoba koja odobrava projekat, izaberite opciju **Da** u polju **Osoba koja odobrava projekat**. Ovo će značiti da član tima može da odobri prosleđene stavke za vreme i troškove za ovaj projekat. 
6. Kliknite na **Sačuvaj**.

![Dodavanje člana tima u obrazac za brzo kreiranje.](media/RM-how-to-2.png)


Sada možete dodeliti rezervisani resurs zadacima u projektu. Na stranici **Projekat** kliknite na karticu **Raspored** da biste dodelili zadatke novom resursu. Birač resursa koji je pokrenut iz polja **Resursi** u mreži zadataka će prikazati članove tima koje možete izabrati.

![Dodeljivanje člana tima zadatku na kartici Raspored.](media/RM-how-to-3.png)

U verziji 3 aplikacije Project Service Automation (PSA), rezervisanje resursa i dodeljivanje zadataka nisu tesno povezani. To znači da kada koristite birač resursa u rasporedu, možete da dodelite zadatke članovima tima za više sati nego što pokriva njihovo vreme rezervisanja za projekat.
Možete da vidite razlike između rezervacija članova tima i dodeljenih zadataka na kartici **Tim** ili na kartici **Usaglašavanje resursa**. Takođe možete da usaglasite razlike između rezervacija i dodela resursa na detaljnijem nivou.

![Kartica Usaglašavanje resursa.](media/RM-how-to-4.png)

Takođe možete koristiti birač resursa na kartici **Raspored** da biste potražili i izabrali resurse koji mogu da se rezervišu, a koji još nisu deo projektnog tima. Oni se prikazuju u biraču resursa kao **Ostali resursi**.

![Dodeljivanje resursa koji nije član tima zadatku.](media/RM-how-to-5.png)

Kada to uradite, resurs će biti dodat u tim projekta i dodeljen zadatku, ali se ne generišu rezervacije.

![Član tima sa dodelama i bez rezervacija.](media/RM-how-to-6.png)

Možete koristiti mogućnost produženja rezervacije na kartici **Usaglašenost** ili **tabelu rasporeda** da biste rezervisali kapacitet resursa za projekat.

![Produženje rezervacije člana tima na kartici Usaglašenost resursa.](media/RM-how-to-7.png)

Nakon što je član tima rezervisan za projekat, možete da koristite održavanje rezervacija ili tabelu rasporeda direktno da biste upravljali rezervacijama.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
