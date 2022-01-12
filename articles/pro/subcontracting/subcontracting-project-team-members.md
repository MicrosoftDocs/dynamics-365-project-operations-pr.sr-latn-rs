---
title: Članovi tima projekta podizvođači
description: Ova tema objašnjenja o tome kako se podizvođači članova projektnog tima u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: b98fc356d7de77fa7f05667acaa5569a7053e4d1
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903753"
---
# <a name="subcontracting-project-team-members"></a>Članovi tima projekta podizvođači

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U Dynamics 365 Project Operations korporaciji Microsoft možete odabrati da podizvođačima odvrate članove projektnog tima koji nisu u štimovanim ili osobljem.

- Članovima projektnog tima nije dodeljen generički resurs.
- Članovima tima sa osobljem je dodeljen imenovani resurs.

Kada povežete člana projektnog tima sa redom podizvođače, sve dodele zadacima koje ima član tima biće ponovo zakazane na osnovu cenovnik nabavne cene priloženog podizvođačem.  Na **kartici Procene** na **stranici Detalji projekta izaberite dugme** **Ažuriraj cene** da biste videli ažurirane cene i/ili troškove koji su rezultat odluke o podizvođačima. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podizvođači neodobravanog člana projektnog tima
Stranica **"Detalji člana** tima" ima polja podizvođača i reda podizvođača koja omogućavaju menadžeru projekta da izrazi kako bi želeli da crpi potrebne kapacitete iz podizvođača. Da biste podizvođali člana projektnog tima kao generički resurs, sledite ove korake:

1.  Odaberite podizvođaи na stranici **sa detaljima** иlana tima.

2.  Možete da izaberete samo podizvođači sa **statusom** "Radna **verzija" ili** "Potvrđeno". **Nije** moguće **izabrati** zatvorene ili otkazane podizvođači. 

3.  Polje **reda podizvođači** postaje vidljivo nakon što izaberete podizvođaи.

4.  U polju **Red podizvođači** možete izabrati samo redove podizvođači koji su za vreme. Ne možete izabrati redove podizvođači za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima treba da se podudara sa ulogom u redu podizvođač. Ovim se obezbeđuje da vreme za ulogu koja se procenjuje na projektu bude ista uloga koja se kupuje u redu podizvođači. 

Kada je generički član tima povezan sa redom podizvođač i podizvođač, polje "Vrsta radnika" u redu generičkog člana tima biće ažurirano **u** **"Radnik** po **ugovoru" i "Validnost podizvođače" na** vrednost **"Važeće".**

## <a name="subcontracting-a-staffed-project-team-member"></a>Podizvođači osoblja projektnog tima
Kao i generički ili neodložni članovi tima, kadrovske kapacitete članova tima koji su potrebni za projekat takođe mogu biti povezani sa podizvođačima. Da biste podizvođači imenovali člana projektnog tima, sledite ove korake:

1.  Uverite se da je imenovani resurs podešen kao tip knjigovodstvenog resursa po ugovoru. Takođe, uverite se da **se polje Dobavljač u knjigovodstvenom resursu podudara sa dobavljačem u** podizvođačem koji ste izabrali. 

2.  Podizvođači možete da izaberete samo u **statusu Radne** verzije **ili** Potvrđeno. **Nije** moguće **izabrati** zatvorene ili otkazane podizvođači. 

3.  Polje **reda podizvođači** postaje vidljivo nakon što izaberete podizvođaи.

4.  U polju **Red podizvođači** možete izabrati samo redove podizvođači koji su za vreme. Ne možete izabrati redove podizvođači za trošak ili materijal.

5.  Uloga zapisa člana projektnog tima treba da se podudara sa ulogom u redu podizvođač. Ovim se obezbeđuje da vreme za ulogu koja se procenjuje na projektu bude ista uloga koja se kupuje u redu podizvođači. 

Imenovani članovi projektnog tima koji su podešeni kao tip radnika **po ugovoru resursa "Knjigovodstveni resurs" biće** pokazani sa statusom provere valjanosti podizvođaca "Nije važeće" ako nisu povezani **sa** podizvođačem. Kada je imenovani član projektnog tima povezan sa redom podizvođač i podizvođač, polje "Tip radnika" u redu člana tima će biti podešeno na **vrednost** **"Radnik** po **ugovoru" i "Validnost podizvođače"** na **vrednost** "Važeće".

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
