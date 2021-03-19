---
title: Rešavanje prodajnih cena za procene i trenutne vrednosti – jednostavno
description: Ova tema pruža informacije o rešavanju prodajnih cena za procene i trenutno stanje.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25620704570fa702e1e5e09c83005be50f98f20a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274520"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Rešavanje prodajnih cena za procene i trenutne vrednosti – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Kada se prodajne cene na procenama i u stvarnim podacima reše u usluzi Dynamics 365 Project Operations, sistem prvo koristi datum i valutu odgovarajuće ponude projekta ili ugovora za rešavanje cenovnika prodaje. Kada se reši cenovnik prodaje, sistem rešava stopu prodaje ili naplate.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Rešite stope prodaje na linijama trenutnog stanja i procene za vreme

U usluzi Project Operations, linije procene vremena koriste se za označavanje linije ponude i detalja predmeta ugovora za vreme i dodeljivanje resursa na projektu.

Nakon što se reši cenovnik prodaje, sistem dovršava sledeće korake da bi zadao podrazumevanu stopu naplate.

1. Sistem koristi polja **Uloga** i **Jedinica za resurse** na liniji procene za vreme, kako bi se podudarala sa linijama cena uloga u rešenom cenovniku. Ovo podudaranje pretpostavlja da se koriste gotove dimenzije utvrđivanja cena za stope naplate. Ako ste konfigurisali cene na osnovu bilo kog drugog polja umesto ili pored polja **Uloga** i **Jedinica za resurse**, onda je to kombinacija koja će se koristiti za preuzimanje odgovarajuće linije cena uloga.
2. Ako sistem pronađe liniju cena uloga koja ima stopu naplate za kombinaciju polja **Uloga** i **Jedinica za resurse**, tada je ta stopa naplate podrazumevana.
3. Ako sistem ne može da se podudari sa vrednostima polja **Uloga** i **Jedinica za resurse**, preuzima linije cena uloga sa podudarnom ulogom, ali sa nula vrednostima za **Jedinica za resurse**. Nakon što sistem pronađe podudarni zapis o ceni uloge, postaviće podrazumevanu stopu naplate iz tog zapisa. Ovo podudaranje pretpostavlja gotovu konfiguraciju za relativni prioritet polja **Uloga** u odnosu na polje **Jedinica za resurse** kao dimenziju prodajnih cena.

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, ovo ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise o ceni uloga sa podudarnim vrednostima svake od vrednosti dimenzije cene po redosledu prioriteta sa redovima koji imaju nulte vrednosti za te dimenzije koje dolaze poslednje.

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
    | &nbsp; | Provizija preko troškova | Primenite proviziju definisanu linijom cene kategorije na jediničnu stopu cene povezanog stvarnog troška |

4. Ako sistem ne može da podudari vrednosti polja **Kategorija** i **Jedinica**, stopa prodaje podrazumevano je nula (0).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]