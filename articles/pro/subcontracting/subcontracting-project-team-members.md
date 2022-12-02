---
title: Članovi projektnog tima podugovaranja
description: Ovaj članak objašnjava kako da podugovorite člana projektnog tima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522813"
---
# <a name="subcontracting-project-team-members"></a>Članovi projektnog tima podugovaranja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U usluzi Microsoft Dynamics 365 Project Operations, možete odabrati da podugovorite članove projektnog tima sa resursima ili bez njih.

- Članovima projektnog tima bez resursa imaju dodeljen generički resurs.
- Članovima tima sa resursima dodeljen je imenovani resurs.

Kada povežete člana projektnog tima sa predmetom podugovora, za sve dodele zadacima koje član tima ima biće ponovo obračunata cena na osnovu nabavnog cenovnika priloženog podugovoru.  Na kartici **Procene** na stranici **Detalji o projektu**, izaberite dugme **Ažuriraj cene** da biste videli ažurirano određivanje cena i/ili obračun cena koji su nastali na osnovu odluke o podugovaranju. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez resursa
Stranica **Detalji o članu tima** ima polja podugovora i predmeta podugovora koja omogućavaju menadžeru projekta da izrazi kako bi želeo da povlači potrebne kapacitete iz podugovora. Da biste podugovorili člana projektnog tima kao generički resurs, pratite ove korake:

1.  Odaberite podugovor na stranici **Detalji o članu tima**.

2.  Možete da izaberete samo podugovore sa statusom **Radna verzija** ili **Potvrđeno**. **Zatvorene** ili **Otkazane** podugovore ne možete izabrati. 

3.  Polje **Predmet podugovora** postaje vidljivo nakon što izaberete podugovor.

4.  U polju **Predmet podugovora** možete izabrati samo predmete podugovora koji su za vreme. Ne možete izabrati predmete podugovora za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima treba da se podudara sa ulogom u predmetu podugovora. Ovim se obezbeđuje da vreme za ulogu koja se procenjuje na projektu bude ista uloga koja se kupuje u predmetu podugovora. 

Kada je član generičkog tima povezan sa podugovorom i predmetom podugovora, polje **Vrsta radnika** u redu člana generičkog tima biće ažurirano u **Radnik po ugovoru**, a vrednost **Važenje podugovora** na **Važeće**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima u resursima
Kao i generički ili članovi tima bez resursa, kapacitet članova tima u resursima koji je potreban za projekat takođe može biti povezani sa podugovorom. Da biste podugovorili imenovanog člana projektnog tima pratite ove korake:

1.  Uverite se da je imenovani resurs podešen kao tip resursa koji je moguće rezervisati sa vrstom radnika po ugovoru. Takođe, uverite se da se polje **Dobavljač** u resursu koji je moguće rezervisati podudara sa dobavljačem u podugovoru koji ste izabrali. 

2.  Možete da izaberete samo podugovore u statusu **Radna verzija** ili **Potvrđeno**. **Zatvorene** ili **Otkazane** podugovore ne možete izabrati. 

3.  Polje **Predmet podugovora** postaje vidljivo nakon što izaberete podugovor.

4.  U polju **Predmet podugovora** možete izabrati samo predmete podugovora koji su za vreme. Ne možete izabrati predmete podugovora za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima treba da se podudara sa ulogom u predmetu podugovora. Ovim se obezbeđuje da vreme za ulogu koja se procenjuje na projektu bude ista uloga koja se kupuje u predmetu podugovora. 

Imenovani članovi projektnog tima koji su podešeni kao vrsta tipa radnika po ugovoru **Resursa koji je moguće rezervisati** biće prikazani sa statusom važenja podugovarača **Nije važeće** ako nisu povezani sa podugovorom. Kada je imenovani član projektnog tima povezan sa podugovorom i predmetom podugovora, polje **Vrsta radnika** u redu člana tima ažuriraće se u **Radnik po ugovoru**, a vrednost **Važenje podugovora** na **Važeće**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
