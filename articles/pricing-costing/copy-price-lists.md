---
title: Kopiranje cenovnika
description: Ova tema pruža informacije o načinu kopiranja cenovnika u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 67a69d521ac0a5632371138bd4fbb9dd00fe34ee
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181514"
---
# <a name="copy-price-lists"></a>Kopiranje cenovnika

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

Kopije cenovnika možete da kreirate u usluzi Dynamics 365 Project Operations. Na primer, možete da napravite cenovnike za predstojeću godinu koristeći cenovnik iz tekuće godine.  Ili možete kopirati cenovnik stopa naplate i prodajnih cena iz cenovnika troškova. 

Da biste napravili kopiju cenovnika, izvršite sledeće korake.

1. Otvorite cenovnik čiju kopiju želite da napravite i izaberite **Kopiraj**.
2. Unesite sve potrebne podatke za kopiranje cenovnika. Sledeća tabela prikazuje razmatranja koja treba imati na umu prilikom unošenja informacija.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| Imenuj | Naziv izvornog cenovnika sa dodatkom **-kopija**. | Cenovnik obuhvata ovu vrednost na svim stranicama liste i padajućim opcijama. |
| Kontekst | Unesite kontekst koji želite za ciljni cenovnik. | Cenovnik čiji je kontekst podešen na **Trošak** koristi se za traženje cene za procene troškova i stvarne troškove. Cenovnik čiji je kontekst podešen na **Prodaja** koristi se za traženje cene za procene prodaje i stvarne iznose prodaje. Samo cenovnici kojima je kontekst postavljen na **Prodaja** mogu se priložiti projektnim cenovnicima za klijente, ponudama i ugovorima. |
| Datum početka | Datum početka perioda u kome je cenovnik na snazi. | Sa poljem **Datum završetka**, ovo polje se koristi da bi se utvrdilo koji cenovnik je primenljiv za određenu procenu ili stvarnu liniju. |
| Datum završetka | Datum završetka perioda u kome je cenovnik na snazi. | Sa poljem **Datum početka**, ovo polje se koristi da bi se utvrdilo koji cenovnik je primenljiv za određenu procenu ili stvarnu liniju. |
| Valuta | Valuta izvornog cenovnika. To možete promeniti. | Kada se ovo promeni, sve rezultujuće linije cena za rad, troškove i stavke kataloga proizvoda pretvaraju se u valutu ciljnog cenovnika tokom kopiranja. |
| Jedinica vremena | Valuta izvornog cenovnika. To možete promeniti. | Kada se ovo promeni, sve rezultujuće linije cena za stavke rada konvertuju se u jedinicu ciljnog cenovnika tokom kopiranja. Koristi se konverzija iz podešavanja jedinice za vremensku jedinicu izvornog cenovnika i vremensku jedinicu ciljnog cenovnika. |
| Opis | Opis izvornog cenovnika sa dodatkom **-kopija**. Ovo je tekstualno polje koje vam omogućava da imate višelinijski opis cenovnika. | Ovo polje je prikazano u **Vezanim** prikazima na cenovniku u različitim entitetima koji imaju povezane cenovnike. |

3. Sačuvajte cenovnik. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Ažurirajte cenovnik primenom provizije za sve cene

1. Na karticama cenovnika **Uloga**, **Kategorija** i **Stavka cenovnika**, možete izabrati **Ažuriranje cena** da biste primenili proviziju na sve cene u podformi. 
2. Na stranici dijaloga koja se otvori, unesite proviziju. Takođe možete da unesete negativni procenat provizije da biste smanjili cene za određeni procenat. 
3. Izaberite **U redu** na stranici dijaloga, a zatim proverite da li cene u podformi odražavaju promene koje ste uneli.