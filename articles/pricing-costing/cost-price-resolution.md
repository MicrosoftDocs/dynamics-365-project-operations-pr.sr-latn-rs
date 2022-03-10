---
title: Rešavanje cena koštanja za procene i trenutno stanje
description: Ova tema pruža informacije o rešavanju cena koštanja za procene i trenutno stanje.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003698"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Rešavanje cena koštanja za procene i trenutno stanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da bi rešio cene koštanja i cenovnik troškova za procene i stvarne podatke, sistem koristi informacije u poljima **Datum**, **Valuta** i **Ugovaračka jedinica** srodnog projekta. Nakon rešavanja cenovnika troškova, aplikacija rešava stopu troškova.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za vreme

Stavke procene za vreme odnose se na detalje o ponudama i predmetima ugovora za dodeljivanje vremena i resursa na projektu.

Kada se cenovnik troškova reši, sistem koristi polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse** na liniji procene za vreme radi podudaranja sa linijama cena uloga u rešenom cenovniku. Ovo podudaranje pretpostavlja da koristite gotove dimenzije utvrđivanja cena za cenu rada. Ako ste konfigurisali sistem tako da podudara polja umesto ili pored polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, onda će se koristiti različita kombinacija za preuzimanje podudarne linije cena uloga. Ako aplikacija pronađe liniju cena uloga koja ima stopu troškova za kombinaciju polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, tada je ta stopa troškova podrazumevana. Ako aplikacija ne može tačno da se podudara sa kombinacijom vrednosti **Uloga**, **Preduzeće koje određuje resurse** i **Jedinica za određivanje resursa**, preuzeće stavke cena uloga sa odgovarajućom vrednošću uloge, ali će biti bez vrednosti za polja **Jedinica za određivanje resursa** i **Preduzeće koje određuje resurse**. Kada se pronađe odgovarajući zapis cene uloge sa odgovarajućom vrednošću cene uloge, stopa troškova podrazumeva se iz tog zapisa. 

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga**, **Kompanija za resurse** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, ovo ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise cena uloga sa vrednostima koje se podudaraju sa svakom od vrednosti dimenzije cene po redosledu prioriteta sa redovima koji su bez vrednosti za one dimenzije koje su poslednje u redosledu prioriteta.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za trošak

Stavke procene za trošak se odnose na detalje ponude i predmeta ugovora za troškove, kao i linije procene troškova na projektu.

Kada se cenovnik troškova reši, sistem koristi kombinaciju polja **Uloga** i **Jedinica za resurse** na liniji procene za trošak radi podudaranja sa linijama **Cena kategorija** u rešenom cenovniku. Ako sistem pronađe liniju cena kategorija koja ima stopu troškova za kombinaciju polja **Kategorija** i **Jedinica**, tada je ta stopa troškova podrazumevana. Ako sistem ne može da nađe podudaranje sa vrednostima **Kategorija** i **Jedinica**, ili ako je u stanju da pronađe podudarnu liniju cena kategorija, ali metoda određivanja cene nije **Cena po jedinici**, stopa troškova je podrazumevano nula (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rešavanje stopa troškova na stvarnim i procenjenim stavkama za materijal

Stavke procene za materijal odnose se na detalje o stavkama ponuda i predmetima ugovora za materijale i stavke procene materijala na projektu.

Kada se reši cenovnik troškova, sistem koristi kombinaciju polja **Proizvod** i **Jedinica** na liniji procene za procenu materijala koja se podudara sa redovima **Stavke u cenovniku** na rešenom cenovniku. Ako sistem pronađe red cene proizvoda koji ima stopu troškova za kombinaciju polja **Proizvod** i **Jedinica**, podrazumevana je stopa troškova. Ako sistem ne može da podudari vrednosti polja **Proizvod** i **Jedinica**, stopa po jedinici je podrazumevano nula. Ovo podrazumevanje će se dogoditi i ako postoji odgovarajući red stavke cenovnika, ali metoda određivanja cena se zasniva na standardnoj ceni ili trenutnoj ceni koja nije definisana u proizvodu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
