---
title: Opoziv prethodno odobrenih stavki
description: Ovaj članak sadrži objašnjenja o tome kako član projektnog tima može da zatraži opoziv prethodno prosleđenih i odobrenih zapisa o vremenu, troškovima i korišćenju materijala i kako menadžer projekta može da odobri ili odbije zahteve za opoziv.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930381"
---
# <a name="recall-previously-approved-entries"></a>Opoziv prethodno odobrenih stavki

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Član projektnog tima koji prosleđuje stavku vremena, troška ili korišćenja materijala može je opozvati nakon što je odobrena. Proces opoziva ima dva glavna koraka:

1. Podnosilac zahteva opozivanje.
2. Davalac odobrenja odobrava zahtev za opoziv.

## <a name="request-a-recall"></a>Zatražite opozivanje

Pratite ove korake da biste zatražili opoziv odobrenih stavki vremena, troškova ili korišćenja materijala.

1. Pratite jedan od ovih koraka, u zavisnosti od vrsta stavke koju želite da opozovete:

    - Za stavke vremena idite na **Projekti** \> **Moj posao** \> **Stavka vremena** i izaberite sve stavke za određenu kombinaciju projekta i zadatka. Alternativno, u mreži odaberite pojedinačne ćelije za vreme za određeni datum i projekat.
    - Za stavke troškova idite na **Projekti** \> **Moj posao** \> **Troškovi** i izaberite red za stavku troška za opoziv.
    - Za stavke korišćenja materijala idite na **Projekti** \> **Moj posao** \> **Evidencija korišćenja materija** i izaberite red za stavku korišćenja materijala za opoziv.

2. Izaberite **Opozovi**. Pojavljuje se dijalog za potvrdu. Ako su odabrane stavke vremena, troškova ili korišćenja materijala već odobrene, od vas će se tražiti da unesete razlog opoziva.
3. Unesite razlog opoziva, a zatim izaberite **U redu** da potvrdite operaciju. Sistem šalje osobi koja je odobrila stavke zahtev za odobrenje opoziva.

> [!IMPORTANT]
> Ne možete da kreirate zahtev za opoziv za odobrenu stavku vremena, troškova ili korišćenja materijala koja je već fakturisana klijentu. Ako pokušate, dobićete poruku u kojoj stoji da se stavka vremena, troška ili korišćenja materijala ne može opozvati jer je već fakturisana. U tom slučaju, možete zahtevati opoziv stavke samo ako se korektivna faktura koristi za izdavanje kompletnog kredita ili povraćaja novca klijentu u originalnoj fakturi.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahteva za opoziv

Sledite ove korake da biste odobrili ili odbacili zahtev za opoziv.

1. Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici liste **Odobrenja** promenite prikaz na **Opozovi zahteve za odobrenja**. Prikazuje se lista prosleđenih zahteva za opoziv.
3. Izaberite jednu ili više stavki, a zatim **Odobri** ili **Odbaci**.
4. Ako ste izabrali **Odobri**, dobijate poruku upozorenja koja objašnjava efekat odobrenja. Izaberite **U redu** da biste potvrdili operaciju. Zahtev za opoziv je odobren.

    –ili–

    Ako ste izabrali **Odbaci**, zahtev za opoziv je odbijen.

> [!IMPORTANT]
> Kada se opoziv odobri, kao i u slučaju njegovog zahtevanja, kada se opoziv odobri, sistem proverava da li ima bilo kakvih aktivnosti fakturisanja u stavkama vremena, troškova ili korišćenja materijala. Ako je stavka već fakturisana ili je u radnoj verziji fakture, davalac odobrenja će primiti poruku o grešci u kojoj stoji da se opoziv vremena ili troška ne može odobriti jer je već fakturisan. U tom slučaju, davalac odobrenja možete odobriti opoziv stavke samo ako se korektivna faktura koristi za izdavanje kompletnog kredita ili povraćaja novca klijentu u originalnoj fakturi.

## <a name="impact-of-a-recall-request"></a>Efekat zahteva za opoziv

Kada se odobrenje opozove, postoji i operativni i finansijski uticaj.

### <a name="operational-impact"></a>Operativni uticaj

Ako je zahtev za opoziv odobren, zapis odobrenja označava se kao **Odbačen**. Status stavke se menja u **Vraćena** ili **Odbačena**, u zavisnosti da li je to stavka vremena, troškova ili korišćenja materijala.

Član projektnog tima može pregledati stavke, uređivati i zatim ponovo prosleđivati stavke ili ih u potpunosti brisati.

Ako se zahtev za opoziv odbaci, status stavke ostaje **Odobrena** i stavku ne može da uređuje član projektnog tima niti davalac odobrenja za projekat.

### <a name="financial-impact"></a>Finansijski uticaj

Ako se zahtev za opoziv odobri, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:

- Polje **Status poravnanja** se ažurira na **Poravnato**.
- Polje **Status naplate** se ažurira na **Otkazano**.

Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti. Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti. Jedine vrednosti koje se ne kopiraju su vrednosti količine. Umesto toga, ove vrednosti se storniraju. Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**. Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a polje **Status naplate** na **Otkazano**. Zbog ovih izmena, evidentirana potrošnja za projekat i preostali prihod od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.

Ako se zahtev za opoziv odbaci, nema finansijskog uticaja na projekat.

## <a name="changes-to-time-entry-records"></a>Promene zapisa stavke vremena

Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke vremena i odgovarajuće zapise odobrenja kada su opozvani.

![Promene statusa stavke vremena.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Promene zapisa stavke troškova i korišćenja materijala

Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke troškova i korišćenja materijala i odgovarajuće zapise odobrenja kada su opozvani.

![Promene statusa stavke troškova.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
