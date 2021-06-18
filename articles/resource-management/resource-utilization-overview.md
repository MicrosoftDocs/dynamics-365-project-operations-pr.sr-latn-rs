---
title: Pregled ukupne iskorišćenosti resursa
description: Ova tema pruža informacije o prikazu ukupne iskorišćenosti resursa u usluzi Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000813"
---
# <a name="resource-utilization-overview"></a>Pregled ukupne iskorišćenosti resursa

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Resursi mogu imati ciljanu naplativu ukupnu iskorišćenost. Ukupna iskorišćenost se definiše kao atribut podrazumevane uloge resursa ili je podešena u zapisu pojedinačnog resursa koji se može rezervisati. Izračunavanje ukupne iskorišćenosti temelji se na stvarnim satima koje su resursi prijavili korišćenjem odobrenih stavki vremena.

Sledeće formule se koriste za izračunavanje ukupne iskorišćenosti:

  - Naplativa ukupna iskorišćenost = naplativi stvarni sati ÷ kapacitet resursa
  - Nenaplativa ukupna iskorišćenost = Stvarno vreme sa ID-om vrste naplate = Nenaplativo, dopunsko ili nedostupno ÷ Kapacitet resursa
  - Interno = Stvarno vreme bez prodajnog ugovora ÷ Kapacitet resursa
  - Kapacitet resursa = Radno vreme resursa – Van kancelarije – Neradni dani

Možete pronaći prikaz **Ukupna iskorišćenost resursa** u oknu **Resursi**.

Svaka ćelija u mreži predstavlja procenat naplative ukupne iskorišćenosti resursa u nekom periodu, kao što je dan, nedelja ili mesec. Sledeće formule se koriste za bojenje ćelija:

  - **Zelena**: Naplativa ukupna iskorišćenost >= Ciljna ukupna iskorišćenost resursa
  - **Žuta**: Ciljna ukupna iskorišćenost – 20 <= Naplativa ukupna iskorišćenost < Ciljna ukupna iskorišćenost
  - **Crvena**: Naplativa ukupna iskorišćenost < Ciljna ukupna iskorišćenost – 20

Zbog toga što je prikaz **Ukupna iskorišćenost resursa** zasnovana na tabeli rasporeda, za filtriranje rezultata možete koristiti mogućnosti filtriranja tabele rasporeda.

Mreža zahteva da podesite ciljnu ukupnu iskorišćenost za ulogu ili pojedinačni resurs. Da biste to podesili, idite na stavku **Resursi** > **Uloge resursa**.

Uz to, svakom resursu koji se može rezervisati mora se dodeliti podrazumevana uloga. Idite na **Resursi** > **Resursi**. Na kartici **Project Service** potvrdite da je definisana uloga resursa i da je polje **Da li je podrazumevano** za tu ulogu podešeno na **Da**. Možete dodati dodatne uloge za koje važi **Da li je podrazumevano** = **Ne**. Uloga gde se **Da li je podrazumevano** = **Da** koristi za procenu ukupne iskorišćenosti resursa u odnosu na ciljnu iskorišćenost za tu ulogu.

Na kartici **Project Service** možete podesiti i pojedinačnu ciljnu ukupnu iskorišćenost za resurs. Kalkulacija ukupne iskorišćenosti zatim koristi tu ciljnu ukupnu iskorišćenost za procenu cilja resursa umesto cilja podrazumevane uloge resursa.

Ukupna iskorišćenost se prikazuje za resurs samo ako je taj resurs odobrio naplativo vreme tokom perioda koji je prikazan na mreži.


[!INCLUDE[footer-include](../includes/footer-banner.md)]