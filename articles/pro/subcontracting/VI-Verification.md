---
title: Verifikacija faktura dobavljača sa odobrenim stvarnim vrednostima
description: Ovaj članak sadrži objašnjenja o tome Microsoft Dynamics 365 Project Operations omogućava menadžerima projekta da verifikuju fakture dobavljača sa stvarnim vrednostima koje su odobrene kad su izvođači radova obavili posao i evidentirali vreme, kao i troškove i materijale koje su koristili članovi projektnog tima.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522963"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifikacija faktura dobavljača sa odobrenim stvarnim vrednostima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Microsoft Dynamics 365 Project Operations omogućava menadžerima projekta da provere redove na fakturi dobavljača, i to na sledeće načine:

- Koristite polje **Status verifikacije** u redovima na fakturi dobavljača.
- Ako redovi na fakturi dobavljača upućuju na predmet podugovora, povežite stvarne vrednosti cene iz aktivnosti podugovarača sa redovima na fakturi dobavljača. Veza se kreira podudaranjem stvarnih vrednosti za cenu sa redovima na fakturi dobavljača.

    > [!NOTE]
    > Iako se status verifikacije može pratiti za redove na fakturi dobavljača koji ne upućuju na podugovor, stvarne vrednosti cene se ne mogu povezati sa redovima na fakturi dobavljača.

## <a name="verification-status"></a>Status verifikacije

Polje **Status verifikacije** u redu na fakturi dobavljača označava taj status provere. Podržani su sledeći statusi:

1. Nije započeto
2. U toku
3. Dovršite

Redovi na fakturi dobavljača koji imaju status verifikacije **Nije započeto** mogu biti uređeni.

Redovi na fakturi dobavljača koji imaju status verifikacije **U toku** ne mogu se više uređivati. Za red na fakturi dobavljača koji upućuje na podugovor, status verifikacije se automatski postavlja na **U toku** čim se prva stvarna vrednost za cenu podudara sa redom na fakturi dobavljača.

Redovi na fakturi dobavljača koji imaju status verifikacije **Dovršeno** ne mogu se više uređivati. Kada svi redovi na fakturi dobavljača imaju ovaj status verifikacije, faktura dobavljača ne može biti potvrđena.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Podudaranje stvarnih vrednosti cena sa redovima na fakturi dobavljača

Podudaranje stvarnih vrednosti cene pomaže u procesu verifikacije u redu na fakturi dobavljača. Da biste podudarali stvarne vrednosti cene sa redom na fakturi dobavljača, pratite ove korake.

1. Otvorite red na fakturi dobavljača i izaberite karticu **Nepodudarene stvarne vrednosti cene**. Matrica koordinatne mreže prikazuje listu stvarnih vrednosti cene koje upućuju na isti predmet podugovora kao i red na fakturi dobavljača.
2. Izaberite jednu ili više stvarnih vrednosti cene, a zatim na traci sa alatkama iznad matrice koordinatne mreže izaberite **Podudaranje**. Sistem proverava da li se izabrane stvarne vrednosti cene mogu podudarati. Nakon što provera valjanosti prođe, stvarne vrednosti cene su povezane sa redom na fakturi dobavljača.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriterijumi provere valjanosti koji se koriste za povezivanje stvarnih vrednosti cene sa redovima na fakturi dobavljača

Tokom procesa podudaranja, veza između stvarne vrednosti cene i reda na fakturi dobavljača može se uspostaviti samo ako su ispunjena oba sledeća uslova:

- Polje **Status korekcije** za svaku izabranu stvarnu vrednost cene mora biti prazno. Drugim rečima, stvarne vrednosti cene ne smeju biti zamenjeni drugim stvarnim vrednostima cene tokom procesa opoziva, otkazivanja odobrenja ili korektivnog naloga.
- Vrednosti sledećih polja se podudaraju između reda na fakturi dobavljača i izabrane stvarne vrednosti cene. Ako neko polje nije podešeno u redu na fakturi dobavljača, ono se ne smatra podudaranjem.

    - Ugovor za projekat
    - Predmet ugovora za projekat
    - Klasa transakcije
    - Project
    - Zadatak
    - Kategorija resursa
    - Kategorija transakcije
    - Proizvod
    - Predmet podugovora
    - Resurs koji može da se rezerviše

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Poništavanje podudaranja stvarnih vrednosti cene sa redom na fakturi dobavljača

Poništavanje podudaranja stvarnih vrednosti cene takođe može pomoći u procesu verifikacije na fakturi dobavljača omogućavajući uklanjanje prethodno uspostavljenih veza. Poništavanje podudaranja stvarnih vrednosti cene možete izvršiti samo sa fakture dobavljača koje imaju status verifikacije **U toku**. Da biste poništili podudaranje stvarne vrednosti cene sa reda na fakturi dobavljača, pratite ove korake.

1. Otvorite red na fakturi dobavljača i izaberite karticu **Podudarene stvarne vrednosti cene**. Matrica koordinatne mreže prikazuje listu stvarnih vrednosti cene koje upućuju na red na fakturi dobavljača.
2. Izaberite jednu ili više stvarnih vrednosti cene, a zatim na traci sa alatkama iznad matrice koordinatne mreže izaberite **Poništi podudaranje**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
