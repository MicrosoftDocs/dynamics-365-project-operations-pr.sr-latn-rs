---
title: Opoziv prethodno odobrenih stavki
description: Ova tema objašnjava kako član projektnog tima može da zatraži opoziv prethodno prosleđenog i odobrenog vremena, troškova i zapisa o korišćenju materijala i kako menadžer projekta može da odobri ili odbije zahteve za opoziv.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586591"
---
# <a name="recall-previously-approved-entries"></a>Opoziv prethodno odobrenih stavki

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Član projektnog tima koji prosledi stavku vremena, troškova ili korišćenja materijala može da opozove tu stavku nakon što je odobrena. Proces opoziva ima dva glavna koraka:

1. Podnosilac zahteva opozivanje.
2. Osoba koja vrši odobravanje odobrava zahtev za opoziv.

## <a name="request-a-recall"></a>Zatražite opozivanje

Sledite ove korake da biste zatražili opoziv odobrenog vremena, troškova ili stavki korišćenja materijala.

1. Sledite jedan od ovih koraka, u zavisnosti od tipa stavke koju želite da opozovete:

    - Za stavke vremena idite na **"Projekti** \> **moja stavka** \> **radnog** vremena" i izaberite sve stavke vremena za određenu kombinaciju projekta i zadatka. Alternativno, u mreži odaberite pojedinačne ćelije za vreme za određeni datum i projekat.
    - Za stavke troškova idite na "**Projekti** \> **moji troškovi** \> **rada"** i izaberite red za opozvanu stavku troškova.
    - Za stavke korišćenja materijala idite u "**Projects** \> **My Work** \> **Material Using Log**" i izaberite red za opozvanu stavku korišćenja materijala.

2. Izaberite **Opozovi**. Pojavljuje se dijalog za potvrdu. Ako su izabrane stavke vremena, troškova ili korišćenja materijala već odobrene, od vas će biti zatraženo da unesete razlog opoziva.
3. Unesite razlog opoziva, a zatim izaberite **U redu** da potvrdite operaciju. Sistem šalje osobi koja je odobrila stavke zahtev za odobrenje opoziva.

> [!IMPORTANT]
> Ne možete kreirati zahtev za opoziv za odobreno vreme, trošak ili stavku korišćenja materijala koja je već fakturisana kupcu. Ako pokušate, dobićete poruku u kojoj se navodi da stavka vremena, troškova ili korišćenja materijala ne može biti opozvana jer je već fakturisana. U tom slučaju možete zatražiti opoziv stavke samo ako se korektivna faktura koristi za izdavanje kompletnog kredita ili povraćaja novca kupcu u originalnoj fakturi.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahteva za opoziv

Sledite ove korake da biste odobrili ili odbacili zahtev za opoziv.

1. Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici liste **Odobrenja** promenite prikaz na **Opozovi zahteve za odobrenja**. Prikazuje se lista prosleđenih zahteva za opoziv.
3. Izaberite jednu ili više stavki, a zatim **Odobri** ili **Odbaci**.
4. Ako ste izabrali **Odobri**, dobijate poruku upozorenja koja objašnjava efekat odobrenja. Izaberite **U redu** da biste potvrdili operaciju. Zahtev za opoziv je odobren.

    –ili–

    Ako ste izabrali **Odbaci**, zahtev za opoziv je odbijen.

> [!IMPORTANT]
> Kada opoziv bude odobren, baš kao i kada je to zahtevano, sistem proverava da li postoji bilo kakva aktivnost fakturisanja u vremenu, troškovima ili stavkama korišćenja materijala. Ako je stavka već fakturisana ili se ona na radnoj fakturi odnosi na radnu verziju fakture, osoba koja vrši odobravanje dobija poruku o grešci u kojoj se navodi da vreme ili trošak ne mogu biti odobreni za opoziv jer je već fakturisan. U ovom slučaju, osoba koja vrši odobravanje može da odobri opoziv samo ako se korektivna faktura koristi za izdavanje kompletnog kredita ili povraćaja novca kupcu u originalnoj fakturi.

## <a name="impact-of-a-recall-request"></a>Efekat zahteva za opoziv

Kada se odobrenje opozove, postoji i operativni i finansijski uticaj.

### <a name="operational-impact"></a>Operativni uticaj

Ako je zahtev za opoziv odobren, zapis odobrenja označava se kao **Odbačen**. Status stavke se menja u "Vraćeno" ili **·** "Odbijeno **·**", u zavisnosti od toga da li se radi o stavci vremena ili o trošku ili korišćenju materijala.

Član projektnog tima može da pregleda stavke, uredi, a zatim ponovo zatvori stavke ili da u potpunosti izbriše stavke.

Ako se zahtev za opoziv odbaci, status stavke ostaje **Odobrena** i stavku ne može da uređuje član projektnog tima niti davalac odobrenja za projekat.

### <a name="financial-impact"></a>Finansijski uticaj

Ako se zahtev za opoziv odobri, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:

- Polje **Status poravnanja** se ažurira na **Poravnato**.
- Polje **Status naplate** se ažurira na **Otkazano**.

Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti. Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti. Jedine vrednosti koje se ne kopiraju su vrednosti količine. Umesto toga, ove vrednosti se storniraju. Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**. Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a polje **Status naplate** na **Otkazano**. Zbog ovih izmena, evidentirana potrošnja za projekat i preostali prihod od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.

Ako se zahtev za opoziv odbaci, nema finansijskog uticaja na projekat.

## <a name="changes-to-time-entry-records"></a>Promene zapisa stavke vremena

Sledeća ilustracija prikazuje promene do kojih dolazi za odobrene stavke vremena i odgovarajuće zapise odobravanja kada budu opozvane.

![Prelazi stanja vremenskog ulaska.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Promene zapisa stavki troškova i korišćenja materijala

Sledeća ilustracija prikazuje promene do kojih dolazi za odobrene stavke troškova i korišćenja materijala i odgovarajuće zapise o odobravanju kada budu opozvane.

![Prelazi stanja unosa troškova.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
