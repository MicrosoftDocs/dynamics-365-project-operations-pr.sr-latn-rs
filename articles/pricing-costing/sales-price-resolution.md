---
title: Rešite prodajne cene za procene i trenutno stanje
description: Ova tema pruža informacije o rešavanju stopa prodaje za procene i trenutno stanje.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9ce095723e8ac300caf7d11ae37b5c721b57795
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877462"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Rešite prodajne cene za procene i trenutno stanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada se prodajne cene na procenama i u stvarnim podacima reše u usluzi Dynamics 365 Project Operations, sistem prvo koristi datum i valutu odgovarajuće ponude projekta ili ugovora za rešavanje cenovnika prodaje. Kada se reši cenovnik prodaje, sistem rešava stopu prodaje ili naplate.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Rešite stope prodaje na linijama trenutnog stanja i procene za vreme

U usluzi Project Operations, linije procene vremena koriste se za označavanje linije ponude i detalja predmeta ugovora za vreme i dodeljivanje resursa na projektu.

Nakon što se reši cenovnik prodaje, sistem dovršava sledeće korake da bi zadao podrazumevanu stopu naplate.

1. Sistem koristi polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse** na liniji procene za vreme, kako bi se podudarala sa linijama cena uloga u rešenom cenovniku. Ovo podudaranje pretpostavlja da se koriste gotove dimenzije utvrđivanja cena za stope naplate. Ako ste konfigurisali cene na osnovu bilo kog drugog polja umesto ili pored polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, onda je to kombinacija koja će se koristiti za preuzimanje odgovarajuće linije cena uloga.
2. Ako sistem pronađe liniju cena uloga koja ima stopu naplate za kombinaciju polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, tada je ta stopa naplate podrazumevana.
3. Ako sistem ne može da se podudari sa vrednostima polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, preuzima linije cena uloga sa podudarnom ulogom, ali sa nultim vrednostima za opciju **Jedinica za resurse**. Nakon što sistem pronađe podudarni zapis o ceni uloge, postaviće podrazumevanu stopu naplate iz tog zapisa. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet polja **Uloga** u odnosu na polje **Jedinica za resurse** kao dimenziju prodajnih cena.

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, ovo ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise o ceni uloga sa podudarnim vrednostima svake od vrednosti dimenzije cene po redosledu prioriteta sa redovima koji imaju nulte vrednosti za te dimenzije koje dolaze poslednje.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Rešite stope prodaje na linijama trenutnog stanja i procene za trošak

U usluzi Project Operations, linije procene troška koriste se za označavanje linije ponude i detalja predmeta ugovora za troškove i dodeljivanje troškova na projektu.

Nakon što se reši cenovnik prodaje, sistem dovršava sledeće korake da bi zadao podrazumevanu jediničnu prodajnu cenu.

1. Sistem koristi kombinaciju polja **Kategorija** i **Jedinica** na liniji procene za trošak, kako bi ih podudario sa linijama cena kategorija u rešenom cenovniku.
2. Ako sistem pronađe liniju cena kategorija koja ima stopu prodaje za kombinaciju polja **Kategorija** i **Jedinica**, tada je ta stopa prodaje podrazumevana.
3. Ako sistem pronađe podudarnu liniju cena kategorije, metod određivanja cena može se koristiti za zadavanje podrazumevane prodajne cene. Sledeća tabela prikazuje ponašanje podrazumevanog vraćanja cena troškova u usluzi Project Operations.

    | Kontekst | Način određivanja cena | Cena je podrazumevano vraćena |
    | --- | --- | --- |
    | Procena | Cena po jedinici | Na osnovu linije cena kategorija |
    | &nbsp; | Po ceni | 0.00 |
    | &nbsp; | Provizija preko troškova | 0.00 |
    | Stvarna vrednost | Cena po jedinici | Na osnovu linije cena kategorija |
    | &nbsp; | Po ceni | Na osnovu povezanih stvarnih troškova |
    | &nbsp; | Provizija preko troškova | Primenom provizije definisane linijom cene kategorije na jediničnu stopu cene povezanog stvarnog troška |

4. Ako sistem ne može da podudari vrednosti polja **Kategorija** i **Jedinica**, stopa prodaje podrazumevano je nula (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Rešavanje stopa prodaje na stvarnim i procenjenim stavkama za materijal

U usluzi Project Operations, stavke procene za materijal se koriste da označe detalje stavki ponude i predmeta ugovora za materijale i stavke procene materijala na projektu.

Nakon što se reši cenovnik prodaje, sistem dovršava sledeće korake da bi zadao podrazumevanu jediničnu prodajnu cenu.

1. Sistem koristi kombinaciju polja **Proizvod** i **Jedinica** na stavki procene za materijal koji se podudara sa redovima stavki cenovnika u cenovniku koji je rešen.
2. Ako sistem pronađe red stavke cenovnika koja ima stopu prodaje za kombinaciju polja **Proizvod** i **Jedinica** i metoda određivanja cena je **Iznos valute**, koristi se prodajna cena koja je navedena u redu cenovnika.
3. Ako se vrednosti polja **Proizvod** i **Jedinica** ne podudaraju, stopa prodaje je podrazumevano nula.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
