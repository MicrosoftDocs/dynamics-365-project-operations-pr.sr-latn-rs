---
title: Spoljno zakazivanje
description: Ovaj članak pruža informacije o spoljnom zakazivanju.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736993"
---
# <a name="external-scheduling"></a>Spoljno zakazivanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Režim spoljnog zakazivanja vam omogućava da izvorno kreirate, ažurirate i brišete entitete koji su povezani sa strukturnim analizama posla (WBS-ovima), ali bez trenutnih ograničenja koja nameće Microsoft Project for the Web. Takođe obezbeđuje ograničenu proveru valjanosti. Ovaj režim bi trebalo da koriste samo sledeći klijenti:

- Klijenti koji imaju potrebne alatke za definisanje WBS-a izvan logike planiranja koju obezbeđuje Project Operations
- Klijenti koji moraju da upravljaju hijerarhijom planiranja, zavisnostima ili trajanjem zadatka

> [!IMPORTANT]
> Podaci koji nisu ispravno uneti u entitete povezane sa WBS-om možda neće biti prikazani u matrici koordinatne mreže za sravnjenje resursa, matrici koordinatne mreže za procene, matrici koordinatne mreže za praćenje ili matrici koordinatne mreže za dodelu resursa.

## <a name="configuration"></a>Konfigurisanje

Ova funkcija je podrazumevano omogućena. Međutim, na gotovoj glavnoj stranici za projekte, povezano polje nije podrazumevano vidljivo. Da biste omogućili polje, na portalu Maker portal otvorite glavnu stranicu za entitet projekta, izaberite **Mehanizam za planiranje**, a zatim promenite polje u **Podrazumevano vidljivo**. Ako ne koristite gotovu stranicu projekta, uredite postojeću stranicu i i dodajte u nju polje **Mehanizam za planiranje**.

## <a name="settings"></a>Podešavanja

Da biste koristili spoljni režim planiranja prvo morate da kreirate novi projekat i izaberete **Spoljno planirani** mehanizam za planiranje u padajućoj listi na glavnoj stranici projekta. Kada se ovaj režim podesi za projekat, ne možete ga promeniti.

## <a name="viewing-the-wbs"></a>Prikazivanje u WBS-u

Ako je projekat spoljno planiran, pristup usluzi Project for the Web ograničen je za taj projekat. Da biste prikazali WBS, morate otići u matricu koordinatne mrežu za praćenje, gde je prikazan kompletan WBS.

## <a name="creating-and-editing-the-wbs"></a>Kreiranje i uređivanje WBS-a

Ako je za projekat omogućeno spoljno planiranje, morate definisati podatke za sve entitete povezane sa WBS-om, uključujući zadatke, članove tima, dodele resursa i zavisnosti.

Sledeća ilustracija prikazuje model podataka za planiranje projekta.

![Model podataka za planiranje projekta.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funkcionalna ograničenja

Sledeće operacije nisu dozvoljene nad spoljno planiranim projektima.

### <a name="project-planning"></a>Planiranje projekta

- **Kopiranje projekta** – Ova operacija nije podržana na projektima planiranim spolja.
- **Premeštanje projekta** – Promene datuma početka projekta neće premestiti početak dodela zadataka ili resursa u WBS-u.
- **Ažuriranje menadžera projekta** – Promene menadžera projekta na glavnoj stranici projekta neće automatski kreirati novog člana projektnog tima sve dok projekat ne bude konvertovan.
- **Ažuriranje predloška radnog sata projekta** – Promene predloška radnog sata projekta neće ponovo izračunati raspored projekta.
- **Konture dodele resursa** – Kreiranje dodela resursa neće automatski ažurirati polje **mdyn\_PlannedWork**. Ovo polje se koristi za skladištenje kontura za napore u dodeli resursa. Ako prikažete vremenski smereni napor u matrici koordinatne mreže za dodelu resursa ili matrici koordinatne mreže za sravnjenje resursa, morate definisati važeće konture dodele resursa. Ove konture moraju biti ispravno oblikovane tako da pokreću izračunavanje i kontura troškova i kontura prodajnih cena. Preporučujemo vam da kreirate probni projekat koji je planiran za Project for the Web, a da zatim pregledate povezane podatke da biste potvrdili zahteve i oblikovanje.

### <a name="resource-management"></a>Upravljanje resursima

- **Generičko ispunjenje resursa** – Generičko ispunjenje resursa nije podržano za spoljno planirane projekte. Pokušaji da se ispune aktivni otvoreni zahtevi kreiraće nove članove projektnog tima, ali neće izbrisati generičkog člana tima niti zameniti generičkog člana tima na postojećim dodelama resursa.
- **Brisanje člana tima** – Brisanje člana tima neće automatski izbrisati dodele resursa.

### <a name="quoting-and-contracting"></a>Slanje ponuda i ugovaranje

- **Uvoz detalja o predmetu ponude i predmetu ugovora** – Kada se detalji o ponudi ili predmetu ugovora uvezu iz projekta, aplikacija je testirana tako da podržava samo 500 zadataka u WBS-u, na osnovu ograničenja od 20 dodela po zadatku.

### <a name="actuals-and-invoicing"></a>Stvarne vrednosti i fakturisanje

- Iako nema promena u postojećim proverama valjanosti između WBS-a i finansijskih transakcija, važno je da se uskladite sa gotovim modelom podataka kako biste se uverili da se sve posledične transakcije pokreću na očekivani način.
