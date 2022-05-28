---
title: Verifikacija faktura dobavljača sa odobrenim stvarnim stvarima
description: Ova tema objašnjava kako menadžeri projekta korporacije Microsoft Dynamics 365 Project Operations proveravaju fakture dobavljača sa stvarnim rezultatima koji su odobreni kao izvođači radova i zapisano vreme, kao i troškove i materijale koje su koristili članovi projektnog tima.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585487"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Verifikacija faktura dobavljača sa odobrenim stvarnim stvarima

[!include [banner](../../includes/dataverse-preview.md)]

_ **Applies To:** Lite deployment - deal to proforma invoicing

Microsoft hajde Dynamics 365 Project Operations da menadžeri projekta provere redove fakture dobavljača na sledeće načine:

- Koristite polje **Status verifikacije** u redovima fakture dobavljača.
- Ako redovi fakture dobavljača upućuju na red podizvođača, trošak veze se stvarni iz aktivnosti podizvođača odnosi na redove fakture dobavljača. Veza se kreira podudaranjem stvarnih troškova sa redovima fakture dobavljača.

    > [!NOTE]
    > Iako se status verifikacije može pratiti za redove fakture dobavljača koji ne upućuju na podizvođača, stvarni troškovi se ne mogu povezati sa redovima fakture dobavljača.

## <a name="verification-status"></a>Status verifikacije

Polje **Status verifikacije** u redu fakture dobavljača označava taj status provere. Podržani su sledeći statusi:

1. Nije započeto
2. U toku
3. Dovršite

Redovi fakture dobavljača koji imaju status provere statusa "Nije **započeto"** mogu se uređivati.

Redovi fakture dobavljača koji imaju status verifikacije "U **toku"** više se ne mogu uređivati. Za red fakture dobavljača koji upućuje na podizvođača, status **verifikacije se automatski postavlja na vrednost "U toku** " čim se prvi stvarni trošak podudara sa redom fakture dobavljača.

Redovi fakture dobavljača koji imaju status verifikacije "Dovršeno **·**" više se ne mogu uređivati. Kada svi redovi u fakturi dobavljača imaju ovaj status verifikacije, faktura dobavljača može biti potvrđena.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Podudaranje stvarnih troškova sa redovima fakture dobavljača

Podudaranje stvarnih troškova pomaže u procesu verifikacije u redu fakture dobavljača. Da biste podudarali stvarne troškove sa redom fakture dobavljača, sledite ove korake.

1. Otvorite red fakture dobavljača i izaberite karticu **Nedovršeni troškovi** . Koordinatna mreža prikazuje listu stvarnih troškova koji upućuju na isti red podizvođači kao i red fakture dobavljača.
2. Izaberite jednu ili više stvarnih troškova, a zatim na traci sa alatkama **iznad** koordinatne mreže izaberite stavku Podudaranje. Sistem proverava da li se izabrane stvarne cene mogu podudarati. Nakon što se provera valjanosti prosledi, stvarni troškovi su povezani sa redom fakture dobavljača.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Kriterijumi provere valjanosti koji se koriste za povezivanje stvarnih troškova sa redovima fakture dobavljača

Tokom procesa podudaranja, veza između stvarnog troška i reda fakture dobavljača može se uspostaviti samo ako su ispunjena oba sledeća uslova:

- Polje Status **korekcije** za svaki stvarni izabrani trošak mora biti prazno. Drugim rečima, stvarni troškovi ne smeju biti zamenjeni drugim stvarnim troškovima tokom procesa opoziva, otkazivanja odobravanja ili korektivnog naloga.
- Vrednosti sledećih polja se podudaraju između reda fakture dobavljača i izabranog troška. Ako neko polje nije podešeno u redu fakture dobavljača, ono se ne smatra podudaranjem.

    - Ugovor za projekat
    - Predmet ugovora za projekat
    - Klasa transakcije
    - Project
    - Zadatak
    - Kategorija resursa
    - Kategorija transakcije
    - Proizvod
    - Red podizvođači
    - Resurs koji može da se rezerviše

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Raspuštanje stvarnih troškova iz reda fakture dobavljača

Dematching of cost actuals can also help with the verification process on a vendor invoice by enabling previously established links to be removed. Stvarne troškove možete nenadmašiti samo iz redova fakture dobavljača koji imaju status verifikacije u **toku**. Da biste nenadklizali stvarne troškove iz reda fakture dobavljača, sledite ove korake.

1. Otvorite red fakture dobavljača i izaberite karticu Podumećeni **troškovi** . Koordinatna mreža prikazuje listu stvarnih troškova koji upućuju na red fakture dobavljača.
2. Izaberite jednu ili više stvarnih troškova, a zatim na traci sa alatkama **iznad koordinatne mreže izaberite** stavku "Nenadmaši".

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
