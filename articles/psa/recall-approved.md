---
title: Opozivanje odobrenih stavki vremena ili troškova
description: Ova tema pruža informacije o tome kako se opozivaju prethodno odobreno vreme ili transakcija troškova.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
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
ms.openlocfilehash: 457aebb00851a1db3e4aa1068f6a825759b8f2e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578817"
---
# <a name="recall-approved-time-or-expense-entries"></a>Opozivanje odobrenih stavki vremena ili troškova

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Član projektnog tima ili druga osoba koja prosleđuje stavku vremena ili troškova može je opozvati nakon što je odobrena. Proces opozivanja odobrene stavke vremena ili troškova ima dva koraka:

1. Podnosilac zahteva opozivanje.
2. Davalac odobrenja odobrava opoziv.

## <a name="request-a-recall"></a>Zatražite opozivanje

Sledite ove korake da biste zatražili opozivanje odobrene stavke vremena ili troškova.

1. Za stavke vremena, idite na **Projekti** \> **Moj posao** \> **Stavka vremena**.

    –ili–

    Za stavke troškova, idite na **Projekti** \> **Moj posao** \> **Troškovi**.

2. Za stavke vremena odaberite sve stavke za određenu kombinaciju projekta i zadatka. Alternativno, u mreži odaberite pojedinačne ćelije za vreme za određeni datum i projekat.

    –ili–

    Za stavke troškova odaberite red za stavku troška da biste je opozvali.

3. Izaberite **Opozovi**. Pojavljuje se dijalog za potvrdu. Ako su odabrane stavke vremena i troškova već odobrene, od vas će se tražiti da unesete razlog opoziva.
4. Unesite razlog opoziva, a zatim izaberite **U redu** da potvrdite operaciju. Sistem šalje osobi koja je odobrila stavke zahtev za odobrenje opoziva.

> [!NOTE]
> Iako se odobrene stavke vremena i troškova mogu opozvati, ako je odobreno vreme ili trošak već fakturisan klijentu, zahtev za opoziv ne može da se kreira. Korisnik koji pokuša da kreira zahtev za opoziv dobiće poruku u kojoj stoji da se vreme ili trošak ne mogu opozvati jer su već fakturisani.

## <a name="approve-or-reject-a-recall-request"></a>Odobravanje ili odbacivanje zahteva za opoziv

Sledite ove korake da biste odobrili ili odbacili zahtev za opoziv.

1. Idite na **Projekti** \> **Moj posao** \> **Odobrenja**.
2. Na stranici liste **Odobrenja** promenite prikaz na **Opozovi zahteve za odobrenja**. Prikazuje se lista prosleđenih zahteva za opoziv.
3. Izaberite jednu ili više stavki, a zatim **Odobri** ili **Odbaci**.
4. Ako ste izabrali **Odobri**, dobijate poruku upozorenja koja objašnjava efekat odobrenja. Izaberite **U redu** da biste potvrdili operaciju. Zahtev za opoziv je odobren.

    –ili–

    Ako ste izabrali **Odbaci**, zahtev za opoziv je odbijen.

> [!NOTE]
> Kao i u slučaju zahtevanja opoziva, kada se opoziv odobri, sistem proverava da li ima bilo kakvih aktivnosti fakturisanja u stavkama vremena ili troškova. Ako je stavka već fakturisana ili je u radnoj verziji fakture, davalac odobrenja će dobiti poruku o grešci u kojoj stoji da se opoziv vremena ili troška ne može odobriti jer je već fakturisan.

## <a name="impact-of-a-recall-request"></a>Efekat zahteva za opoziv

Kada se odobrenje opozove, postoji i operativni i finansijski uticaj.

### <a name="operational-impact"></a>Operativni uticaj

Ako je zahtev za opoziv odobren, zapis odobrenja označava se kao **Odbačen**. Status stavke se menja u **Vraćena** ili **Odbačena**, u zavisnosti da li je to stavka vremena ili troškova.

Član projektnog tima može pregledati stavke, uređivati i zatim ponovo prosleđivati stavke ili ih u potpunosti brisati.

Ako se zahtev za opoziv odbaci, status stavke ostaje **Odobrena** i stavku ne može da uređuje član projektnog tima niti davalac odobrenja za projekat.

### <a name="financial-impact"></a>Finansijski uticaj

Ako se zahtev za opoziv odobri, odgovarajuće stvarne vrednosti troškova i prodaje se ažuriraju na sledeći način:

- Polje **Status poravnanja** se ažurira na **Poravnato**.
- Polje **Status naplate** se ažurira na **Otkazano**.

Zatim, stavke storniranja se kreiraju u tabeli Stvarne vrednosti. Da bi sistem kreirao stavke storniranja, kopira vrednosti polja iz originalnih stvarnih vrednosti. Jedine vrednosti koje se ne kopiraju su vrednosti količine. Umesto toga, ove vrednosti se storniraju. Stornirane stvarne vrednosti se kreiraju za stvarne vrednosti **Troškovi** i **Nenaplaćena prodaja**. Polje **Status poravnanja** u storniranim stvarnim vrednostima je podešeno na **Ne može da se poravna**, a polje **Status naplate** na **Otkazano**. Zbog ovih izmena, evidentirana potrošnja za projekat i preostali prihod od projekta više neće uzimati u obzir iznose koje ove stvarne vrednosti predstavljaju.

Ako se zahtev za opoziv odbaci, nema finansijskog uticaja na projekat.

## <a name="changes-to-time-entry-records"></a>Promene zapisa stavke vremena

Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke vremena kada su opozvane.

![Promene statusa stavke vremena.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Promene zapisa stavke troškova

Sledeća ilustracija prikazuje promene koje se dešavaju za odobrene stavke troškova kada su opozvane.

![Promene statusa stavke troškova.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
