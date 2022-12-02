---
title: Utvrđivanje stopa cena za procene i trenutno stanje projekta
description: Ovaj članak pruža informacije o načinu utvrđivanja stopa cena za procene projekata i stvarne vrednosti.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475253"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Utvrđivanje stopa cena za procene i trenutno stanje projekta

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Da bi odredile stope cena za procene i stvarne vrednosti u programu Microsoft Dynamics 365 Project Operations, sistem prvo koristi datum i valutu u dolaznoj proceni ili stvarnom kontekstu za određivanje cenovnika koštanja. U stvarnom kontekstu posebno, sistem koristi polje **Datum transakcije** da bi odredio koji cenovnik je primenljiv. Vrednost **Datum transakcije** dolazne procene ili stvarne vrednosti se poredi sa vrednostima za **Efektivni početak (nezavisno od vremenske zone)** i **Efektivni kraj (nezavisno od vremenske zone)** na cenovniku. Nakon utvrđivanja cenovnika troškova, sistem utvrđuje stopu cena. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Utvrđivanje stopa cena u kontekstima procene i stvarnih vrednosti za vreme

Kontekst procene za **Vreme** odnosi se na:

- Detalji stavke ponude za **Vreme**.
- Detalji predmeta ugovora za **Vreme**.
- Dodeljivanja resursa na projektu.

Kontekst stvarne vrednosti za **Vreme** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Vreme**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja stavke vremena.

Nakon što se utvrdi cenovnik koštanja, sistem dovršava sledeće korake da bi uneo podrazumevanu stopu cene.

1. Sistem podudara kombinaciju polja **Uloga** i **Jedinica za resurse** u kontekstu procene ili stvarne vrednosti za **Vreme**, kako bi se podudarala sa linijama cena uloga u cenovniku. Ovo podudaranje pretpostavlja da za troškove rada koristite standardne aspekata za određivanje cena. Ako ste konfigurisali sistem tako da podudara polja koja nisu ili pored polja **Uloga** i **Jedinica za resurse**, koristiće se različita kombinacija za preuzimanje podudarne linije cena uloga.
1. Ako sistem pronađe liniju cena uloga koja ima stopu troškova za kombinaciju polja **Uloga** i **Jedinica za resurse**, tada se ta stopa cene koristi kao podrazumevana stopa cene.
1. Ako sistem ne može da se podudari sa vrednostima polja **Uloga**, **Jedinica za resurse** , on preuzima redove cena uloga koje imaju podudarne vrednosti za polje **Uloga** ali sa nultim vrednostima za polje **Jedinica za resurse**. Nakon što je sistem pronašao podudarni zapis o stopi cene, stopa naplate iz tog zapisa će se koristiti kao podrazumevana stopa cene.

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise cena uloga koji imaju vrednosti koje se podudaraju sa svakom vrednošću dimenzije cena po redosledu prioriteta. Redovi koji nemaju vrednosti za te dimenzije su poslednji.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Utvrđivanje stopa troškova na stavkama trenutnog stanja i procene za trošak

Kontekst procene za **Trošak** odnosi se na:

- Detalji stavke ponude za **Trošak**.
- Detalji predmeta ugovora za **Trošak**.
- Procene troškova na projektu.

Kontekst stvarne vrednosti za **Trošak** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Trošak**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja stavke troška.

Nakon što se utvrdi cenovnik koštanja, sistem dovršava sledeće korake da bi uneo podrazumevanu stopu cene.

1. Sistem podudara kombinaciju polja **Kategorija** i **Jedinica** u kontekstu procene ili stvarne vrednosti za **Trošak**, kako bi se podudarala sa linijama cena kategorije u cenovniku.
1. Ako sistem pronađe liniju cena kategorija koja ima stopu troškova za kombinaciju polja **Kategorija** i **Jedinica**, ta stopa cene se koristi kao podrazumevana stopa cene.
1. Ako sistem ne može da podudari vrednosti polja **Kategorija** i **Jedinica**, cena se podrazumevano postavlja na **0** (nulu).
1. U kontekstu procene, ako sistem ne može da upari red cene za kategoriju, ali metod određivanja cene nije **Cena po jedinici**, stopa troškova se podrazumevano postavlja na **0** (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Utvrđivanje stopa troškova na stvarnim i procenjenim stavkama za materijal

Kontekst procene za **Materijal** odnosi se na:

- Detalji stavke ponude za **Materijal**.
- Detalji predmeta ugovora za **Materijal**.
- Procene materijala na projektu.

Kontekst stvarne vrednosti za **Materijal** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Materijal**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja evidencije korišćenja materijala.

Nakon što se utvrdi cenovnik koštanja, sistem dovršava sledeće korake da bi uneo podrazumevanu stopu cene.

1. Sistem koristi kombinaciju polja **Proizvod** i **Jedinica** u kontekstu procene ili stvarne vrednosti za **Materijal**, kako bi se podudarala sa linijama stavke cenovnika u cenovniku.
1. Ako sistem pronađe liniju stavke cenovnika koja ima stopu troškova za kombinaciju polja **Proizvod** i **Jedinica**, ta stopa cene se koristi kao podrazumevana stopa cene.
1. Ako sistem ne može da podudari vrednosti polja **Proizvod** i **Jedinica**, stopa po jedinici se podrazumevano postavlja na **0** (nula).
1. U kontekstu procene ili stvarne vrednosti, ako sistem ne može da upari liniju stavke cenovnika, ali metod određivanja cene nije **Iznos valute**, cena jedinice se podrazumevano postavlja na **0** (nula). Do ovog ponašanja dolazi zato što Project Operations podržava samo metod određivanja cena **Iznos valute** za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
