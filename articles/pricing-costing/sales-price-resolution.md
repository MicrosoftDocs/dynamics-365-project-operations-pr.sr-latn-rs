---
title: Rešite prodajne cene za procene i trenutno stanje
description: Ova tema pruža informacije o rešavanju stopa prodaje za procene i trenutno stanje.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119570"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Rešite prodajne cene za procene i trenutno stanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Kada se prodajne cene za procene i trenutno stanje reše u programu Dynamics 365 Project Operations, sistem prvo koristi datum i valutu odgovarajuće ponude ili ugovora projekta za rešavanje prodajnog cenovnika. Kada se reši cenovnik prodaje, sistem rešava stopu prodaje ili naplate.

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
