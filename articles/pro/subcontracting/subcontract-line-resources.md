---
title: Resursi za predmete podugovora
description: Ova tema objašnjava kako navesti namenske resurse koje prodavac obezbeđuje za određeni predmet podugovora za vreme.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323388"
---
# <a name="subcontract-line-resources"></a>Resursi za predmete podugovora

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U aplikaciji Dynamics 365 Project Operations, prodavac može da navede resurse koji će se koristiti za snabdevanje kapaciteta resursa koji se kupuje na predmetu podugovora za vreme.

## <a name="create-subcontract-line-resources"></a>Kreiranje aktivnih resursa za predmet podugovora

Da biste kreirali resurse predmeta podugovora, obavite sledeće korake.

1. Na stranici navigacije izaberite **Podugovori** i otvorite podugovor sa kojim želite da radite.
2. Otvorite predmet podugovora za vreme za koji želite da navedete resurse dobavljača.
3. Na kartici **Resursi predmeta podugovora**, na podformi izaberite **+ Novi resurs za predmet podugovora**.
4. Na stranici **Nova kontrolna tačka za predmet podugovora** unesite potrebne podatke i izaberite **Sačuvaj i zatvori**.

Sledeća tabela objašnjava polja na resursu predmeta podugovora.

| Polje |  Opis |
| ----- | ------------ |
| Resurs koji može da se rezerviše | Izaberite resurs koji se može rezervisati tipa „Ugovorni radnik“ koji želite da koristite kao resurs na predmetu podugovora. Ako još niste kreirali resurs koji se može rezervisati za ugovornog radnika, ostavite ovo polje prazno. Resurs koji je moguće rezervisati se kreira kada sačuvate zapis.  |
| Kontakt | Ako je polje **Resurs koji je moguće rezervisati** prazno, možete da kreirate resurs predmeta podugovora na osnovu postojećeg kontakta. Koristite pronalaženje da biste videli listu aktivnih kontakata u sistemu. Izaberite kontakt za proizvođača ovog podugovora. Kontakt koji odaberete potvrđuje se kada sačuvate zapis. Ako kontakt koji ste izabrali nije važeći kontakt, vaš zapis se neće sačuvati. Ako nema resursa koji se može rezervisati za izabrani kontakt, sistem kreira resurs koji se može rezervisati za izabrani kontakt pre nego što se kreira resurs predmeta podugovora. |
| Korisnik | Ako je polje **Resurs koji je moguće rezervisati** prazno, možete da kreirate resurs predmeta podugovora ako izaberete aktivnog korisnika. Koristite pronalaženje da biste videli listu aktivnih korisnika u sistemu. Ako nema resursa koji se može rezervisati za izabranog korisnika, sistem kreira resurs koji se može rezervisati za izabranog korisnika pre nego što se kreira resurs predmeta podugovora. |
| Datum početka | Datum kada počinje angažman radnika iz podugovora. Ako je ovaj resurs rezervisan za period koji prethodi ovom opsegu datuma, pojaviće se upozorenje. |
| Datum završetka | Datum kada se završava angažman radnika iz podugovora. Ako je ovaj resurs rezervisan za period koji sledi ovom opsegu datuma, pojaviće se upozorenje. |
| Angažovanje | Ukupan broj sati angažovanja koje će radnik podugovarača potrošiti na ovaj predmet podugovora. Ako se ovaj resurs rezerviše izvan angažovanja koje im je dodeljeno po ovom podugovoru, pojaviće se upozorenje. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
