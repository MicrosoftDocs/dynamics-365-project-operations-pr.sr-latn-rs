---
title: Kreiranje dodela resursa
description: Ovaj članak pruža informacije o kreiranju generičkih i imenovanih dodela resursa.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812011"
---
# <a name="create-resource-assignments"></a>Kreiranje dodela resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_


Dodeljivanje resursa je direktno povezivanje člana projektnog tima sa zadatkom čvora lista. Ovaj članak pruža informacije o različitim načinima za dodeljivanje resursa.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Kreiranje generičkog člana tima preko dodele zadatka


Kada kreirate generičkog člana tima dodeljivanjem zadatka, kreirate rezervisano mesto ili generički resurs. Ovaj generički resurs opisuje karakteristike imenovanog resursa koje na kraju želite da radite na zadacima. Zatim generišete zahtev ili podnosite zahtev koristeći zahtev koji se koristi za traženje i rezervisanje imenovanog resursa.

1. Na mreži Raspored za zadatak, izaberite ikonu resursa u ćeliji **Resurs**.
2. Otkucajte ime koje će poslužiti kao ime resursa čuvara mesta. Na primer, Menadžer programa.
3. Izaberite **Kreiraj**, pa u polju **Brzo kreiranje člana projektnog tima** podesite ulogu za generički resurs.
4. Dodeljujte zadatke po potrebi u ovaj resurs čuvara mesta izborom resursa u **biraču resursa** za zadatak. Resursi su navedeni u okviru opcije **Članovi tima**.
5. Kada završite sa dodeljivanjem generičkog resursa, na kartici **Tim** izaberite generički resurs, a zatim izaberite **stavku Generiši zahtev** da biste kreirali zahtev resursa za generički resurs.
6. Izaberite stavku **Rezerviši** za generički resurs, a zatim koristite tabelu rasporeda da biste pronašli i rezervisali stvarni resurs. Možete i da prosledite zahtev za ispunjenje od strane menadžera resursa.
7. Kada je generički resurs u potpunosti ispunjen imenovanim resursom, generički resurs se uklanja iz tima. (Delimično ispunjenje zahteva resursa neće rezultirati dodeljivanjem resursa.) Dodele zadataka za generički resurs dodeljuju se imenovanom resursu koji je ispunio zahtev za resurs generičkog resursa.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Dodela imenovanog resursa sa liste svih resursa koji mogu da se rezervišu

Možete da koristite polje za pretragu u **biraču resursa** da pretražite sve aktivne resurse koji mogu da se rezervišu i dodelite ih zadatku čvora lista. Resursi dodeljeni na ovaj način dodaju se u tim bez ikakvih rezervacija. To je slično dodavanju člana tima i odluci da izaberete **Nijedno** kao metodu dodele. Resurs se prikazuje na karticama **Tim**, **Dodela resursa** i **Usaglašenost** kao resurs samo sa dodelama i sa nedostatkom rezervacije. Rezervišete ih ako želite da koristite njihovu dostupnost.

1. Iz mreže zadataka, sa table ili vremenske ose idite na ćeliju **Dodeljeno**.
2. U polju za pretragu počnite da kucate ime. Prikazuju se rezultati pretrage za ime u **biraču resursa** u okviru opcije **Drugi resursi**.
3. Izaberite resurs koji želite da dodelite zadatku ili izaberite ime resursa u delu **Ostali resursi tima**.

## <a name="editing-resource-assignment-contours"></a>Uređivanje kontura dodeljivanja resursa

Po podrazumevanoj vrednosti, kada se resursi dodele zadatku u rasporedu, njihov trud se linearno distribuira svakom resursu, na osnovu radnog vremena tog resursa i režima rasporeda projekta. Menadžer projekta može da koristi koordinatnu mrežu za dodeljivanje resursa da bi suzio procenu napora svakog resursa koji je dodeljen jednom ili više zadataka u različitim vremenskim skalama. Ova funkcija pomaže menadžerima projekta da proizvedu preciznije procene troškova i prodaje, koje pokreću konture dodele resursa koje se generišu kada se dodeli resurs zadatku. Pored toga, menadžeri projekata mogu lakše da odražavaju zahtev resursa koji je potreban za izgradnju zahteva u zahtevu resursa.

### <a name="navigation"></a>Navigacija

Da bi pristupio koordinatnoj mreži za uređivanje konture, menadžer projekta prvo bira karticu **"Zadaci** " na glavnoj stranici projekta, a zatim bira karticu **"Dodele** ".

![Kartica "Dodele" na kartici "Zadaci" na glavnoj stranici projekta.](media/AssignmentGrid.png)

Koordinatna mreža podržava dva metoda za grupisanje:grupisanje po **resursu i** grupisanje **po zadatku**. Za razliku od prikaza koordinatne mreže, kolone se ne mogu konfigurisati. Jedine vidljive kolone su dodeljene,,Ime **zadatka,Početak** **dodele,Završetak** **dodele** i Napor **dodele**. **·**

Kada je koordinatna mreža inicijalno prikazana, ona počinje najranijom konturom dodele. Ako raspored ne sadrži zadatke koji imaju napora, koordinatna mreža će biti prazna i neće prikazivati ništa.

![Prazna koordinatna mreža za dodeljivanje.](media/emptyassignmentgrid.png)

Ako želite da prikažete konture i različite vremenske skale, dostupna je i koordinatna mreža za dodeljivanje resursa samo za čitanje i mreža za sravnjenje resursa.

### <a name="resource-calendars"></a>Kalendari resursa

Mogućnost uređivanja konture za određeni dan regulisana je radnim danima resursa, kao što se ogleda u njihovom kalendaru. Ako je ćelija onemogućena za dati resurs, taj resurs nema radne dane u tom periodu.

Konture resursa mogu da se prošire i izvan trenutnih datuma početka i završetka dodeljenog zadatka. Ako se kontura ažurira tako da bude nakon poslednjeg datuma završetka zadatka ili najranijeg datuma početka zadatka, krajnji datum ili datum početka zadatka biće promenjeni na odgovarajući način. Međutim, ako je kontura ažurirana tako da bude veća od datuma početka zadatka koji je povezan sa prethodnikom, ispravka neće uspeti jer će dodela pokrenuti zadatak da se započne pre nego što se dovrši njegov prethodnik, a to ponašanje trenutno nije podržano.

### <a name="co-authoring"></a>Koautori

Promene u koordinatnoj mreži za dodeljivanje resursa automatski se odražavaju na sve povezane prikaze, uključujući grafikon, vremensku osu, tablu i prikaze koordinatne mreže. Ako više korisnika istovremeno pregleda projekat, sve promene koje jedan korisnik napravi odraziće se na koordinatnu mrežu. Nasuprot tome, sve promene izvršene u koordinatnoj mreži za dodeljivanje resursa biće prikazane svim ostalim korisnicima koji pregledaju projekat u istoj sesiji.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
