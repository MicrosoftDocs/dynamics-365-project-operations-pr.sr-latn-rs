---
title: Resursi za predmete podugovora
description: Ovaj članak sadrži objašnjenja o tome kako da navedete namenske resurse koje dobavljač obezbeđuje za određeni red podizvođač za vreme.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522390"
---
# <a name="subcontract-line-resources"></a>Resursi za predmete podugovora

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U aplikaciji Dynamics 365 Project Operations, prodavac može da navede resurse koji će se koristiti za snabdevanje kapaciteta resursa koji se kupuje na predmetu podugovora za vreme.

## <a name="create-subcontract-line-resources"></a>Kreiranje aktivnih resursa za predmet podugovora

Da biste kreirali resurse predmeta podugovora, obavite sledeće korake.

1. Na stranici navigacije izaberite **Podugovori** i otvorite podugovor sa kojim želite da radite.
2. Otvorite predmet podugovora za vreme za koji želite da navedete resurse dobavljača.
3. Na kartici **Resursi predmeta podugovora**, na podformi izaberite **+ Novi resurs za predmet podugovora**.
4. Na stranici **Novi resurs stavke podugovora** unesite potrebne podatke, a zatim izaberite opciju **Sačuvaj i zatvori**.

Sledeća tabela objašnjava polja na resursu predmeta podugovora.

| Polje | Opis | Funkcionalni uticaj |
| ----- | ----------- | ----------------- |
| Resurs koji može da se rezerviše | Izaberite resurs koji se može rezervisati tipa **Ugovorni radnik** koji želite da koristite kao resurs na stavci podugovora.| Ako niste kreirali resurs koji se može rezervisati za radnika po ugovoru, ostavite ovo polje prazno. Resurs koji se može rezervisati biće kreiran kada sačuvate zapis.  |
| Kontakt | Možete da kreirate resurs stavke podugovora od postojećeg kontakta. Koristite pronalaženje da biste videli listu aktivnih kontakata u sistemu. Izaberite kontakt za proizvođača ovog podugovora. Ako kontakt koji ste izabrali nije važeći kontakt za dobavljača na podugovoru, zapis o resursu stavke podugovora neće biti sačuvan.| Ako nema resursa koji se može rezervisati za izabrani kontakt, sistem kreira resurs koji se može rezervisati za izabrani kontakt pre nego što se kreira resurs predmeta podugovora. |
| Korisnik | Resurs stavke podugovora možete da kreirate tako što ćete odabrati aktivnog korisnika. Koristite pronalaženje da biste videli listu aktivnih korisnika u sistemu.| Ako nema resursa koji se može rezervisati za izabranog korisnika, sistem kreira resurs koji se može rezervisati za izabranog korisnika pre nego što se kreira resurs predmeta podugovora. |
| Datum početka | Datum kada počinje angažman radnika iz podugovora.| Ako je ovaj resurs rezervisan za period koji prethodi ovom opsegu datuma, pojaviće se upozorenje. |
| Datum završetka | Datum kada se završava angažman radnika iz podugovora.| Ako je ovaj resurs rezervisan za period koji sledi ovom opsegu datuma, pojaviće se upozorenje. |
| Angažovanje | Ukupan broj časova angažovanja koji će radnik po ugovoru potrošiti za ovu stavku podugovora.| Ako se ovaj resurs rezerviše izvan angažovanja koje je dodeljeno ovim podugovorom, pojaviće se upozorenje. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
