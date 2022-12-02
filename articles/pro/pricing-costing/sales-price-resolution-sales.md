---
title: Utvrđivanje prodajnih cena za procene i trenutno stanje projekta
description: Ovaj članak pruža informacije o načinu utvrđivanja prodajnih cena za procene projekata i stvarne vrednosti.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475202"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Utvrđivanje prodajnih cena za procene i trenutno stanje projekta

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Da bi odredile prodajne cene za procene i stvarne vrednosti u programu Microsoft Dynamics 365 Project Operations, sistem prvo koristi datum i valutu u dolaznoj proceni ili stvarnom kontekstu za određivanje prodajnog cenovnika. U stvarnom kontekstu posebno, sistem koristi polje **Datum transakcije** da bi odredio koji cenovnik je primenljiv. Vrednost **Datum transakcije** dolazne procene ili stvarne vrednosti se poredi sa vrednostima za **Efektivni početak (nezavisno od vremenske zone)** i **Efektivni kraj (nezavisno od vremenske zone)** na cenovniku. Kada se utvrdi prodajni cenovnik, sistem utvrđuje stopu prodaje ili naplate.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Utvrđivanje stopa prodaje na redovima trenutnog stanja i procene za vreme

Kontekst procene za **Vreme** odnosi se na:

- Detalji stavke ponude za **Vreme**.
- Detalji predmeta ugovora za **Vreme**.
- Dodeljivanja resursa na projektu.

Kontekst stvarne vrednosti za **Vreme** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Vreme**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja stavke vremena.
- Detalji predmeta fakture za **Vreme**. 

Nakon što se utvrdi prodajni cenovnik, sistem dovršava sledeće korake da bi uneo podrazumevanu stopu naplate.

1. Sistem podudara kombinaciju polja **Uloga** i **Jedinica za resurse** u kontekstu procene ili stvarne vrednosti za **Vreme**, kako bi se podudarala sa linijama cena uloga u cenovniku. Ovo podudaranje pretpostavlja da koristite gotove dimenzije utvrđivanja cena za stope naplate. Ako ste konfigurisali određivanje cene tako da se zasniva na polja koja nisu pored polja **Uloga** i **Jedinica za resurse**, onda se ta kombinacija polja koristiti za preuzimanje odgovarajuće uloge stavke cene.
1. Ako sistem pronađe liniju cena uloga koja ima stopu naplate za kombinaciju **Uloge** i **Jedinice za resurse**, tada se ta stopa naplate koristi kao podrazumevana stopa naplate.
1. Ako sistem ne može da se podudari sa vrednostima polja **Uloga**, **Jedinica za resurse** , on preuzima redove cena uloga koje imaju podudarne vrednosti za polje **Uloga** ali sa nultim vrednostima za polje **Jedinica za resurse**. Nakon što sistem pronađe podudarni zapis o ceni uloge, stopa naplate iz tog zapisa će se koristiti kao podrazumevana stopa naplate. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet polja **Uloga** u odnosu na polje **Jedinica za resurse** kao dimenziju prodajnih cena.

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise cena uloga koji imaju vrednosti koje se podudaraju sa svakom vrednošću dimenzije cena po redosledu prioriteta. Redovi koji nemaju vrednosti za te dimenzije su poslednji.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Utvrđivanje stopa prodaje na redovima stvarnih vrednosti i procena za trošak

Kontekst procene za **Trošak** odnosi se na:

- Detalji stavke ponude za **Trošak**.
- Detalji predmeta ugovora za **Trošak**.
- Redovi sa procenom troškova na projektu.

Kontekst stvarne vrednosti za **Trošak** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Trošak**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja stavke troška.
- Detalji reda na fakturi za **Trošak**. 

Nakon što se utvrdi cenovnik prodaje, sistem dovršava sledeće korake da bi uneo podrazumevanu jediničnu prodajnu cenu.

1. Sistem podudara kombinaciju polja **Kategorija** i **Jedinica** na liniji procene za **Trošak**, kako bi ih podudario sa linijama cena kategorija u cenovniku.
1. Ako sistem pronađe liniju cena kategorija koja ima stopu prodaje za kombinaciju polja **Kategorija** i **Jedinica**, tada se ta stopa prodaje koristi kao podrazumevana.
1. Ako sistem pronađe podudarnu liniju cena kategorije, metod određivanja cena može se koristiti za unos podrazumevane prodajne cene. Sledeća tabela prikazuje podrazumevano ponašanje za cene troškova u usluzi Project Operations.

    | Kontekst | Način određivanja cena | Podrazumevana cena |
    | --- | --- | --- |
    | Procena | Cena po jedinici | Na osnovu linije cena kategorija. |
    |        | Po ceni | 0.00 |
    |        | Provizija preko troškova | 0.00 |
    | Stvarna vrednost | Cena po jedinici | Na osnovu linije cena kategorija. |
    |        | Po ceni | Na osnovu povezanih stvarnih troškova. |
    |        | Provizija preko troškova | Primenjuje se provizija, definisana linijom cene kategorije na jediničnu stopu cene povezanog stvarnog troška. |

1. Ako sistem ne može da podudari vrednosti polja **Kategorija** i **Jedinica**, stopa prodaje se podrazumevano postavlja na **0** (nulu).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Utvrđivanje stopa prodaje na stvarnim i procenjenim stavkama za materijal

Kontekst procene za **Materijal** odnosi se na:

- Detalji stavke ponude za **Materijal**.
- Detalji predmeta ugovora za **Materijal**.
- Redovi procene materijala na projektu.

Kontekst stvarne vrednosti za **Materijal** odnosi se na:

- Stavke knjiženja u glavnoj knjizi unosa i korekcije za **Materijal**.
- Stavke knjiženja u glavnoj knjizi se kreiraju prilikom prosleđivanja evidencije korišćenja materijala.
- Detalji reda na fakturi za **Materijal**. 

Nakon što se utvrdi cenovnik prodaje, sistem dovršava sledeće korake da bi uneo podrazumevanu jediničnu prodajnu cenu.

1. Sistem podudara kombinaciju polja **Proizvod** i **Jedinica** na stavki procene za **Materijal** koji se podudara sa redovima stavki cenovnika u cenovniku.
1. Ako sistem pronađe red stavke cenovnika koja ima stopu prodaje za kombinaciju polja **Proizvod** i **Jedinica** i ako metoda određivanja cena je **Iznos valute**, koristi se prodajna cena koja je navedena u redu cenovnika. 
1. Ako se vrednosti polja **Proizvod** i **Jedinica** ne podudaraju ili ako način određivanja cena nije **Iznos u valuti**, stopa prodaje se podrazumevano podešava na **0** (nula). Do ovog ponašanja dolazi zato što Project Operations podržava samo metod određivanja cena **Iznos valute** za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
