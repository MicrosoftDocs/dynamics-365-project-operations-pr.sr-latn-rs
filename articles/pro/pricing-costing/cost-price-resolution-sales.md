---
title: Rešavanje cena koštanja za procene i trenutne vrednosti – jednostavno
description: Ova tema pruža informacije o rešavanju cena koštanja za procene i trenutno stanje.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176808"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Rešavanje cena koštanja za procene i trenutne vrednosti – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Da bi rešio cene koštanja i cenovnik troškova za procene i stvarne podatke, sistem koristi informacije u poljima **Datum**, **Valuta** i **Ugovaračka jedinica** srodnog projekta. Nakon rešavanja cenovnika troškova, aplikacija rešava stopu troškova.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za vreme

Stavke procene za vreme odnose se na detalje o ponudama i predmetima ugovora za dodeljivanje vremena i resursa na projektu.

Kada se cenovnik troškova reši, sistem koristi polja **Uloga** i **Jedinica za resurse** na liniji procene za vreme radi podudaranja sa linijama cena uloga u rešenom cenovniku. Ovo podudaranje pretpostavlja da koristite gotove dimenzije utvrđivanja cena za cenu rada. Ako ste konfigurisali sistem tako da podudara polja umesto ili pored polja **Uloga** i **Jedinica za resurse**, onda će se koristiti različita kombinacija za preuzimanje podudarne linije cena uloga. Ako aplikacija pronađe liniju cena uloga koja ima stopu troškova za kombinaciju polja **Uloga** i **Jedinica za resurse**, tada je ta stopa troškova podrazumevana. Ako aplikacija ne može da se podudari sa vrednostima polja **Uloga** i **Jedinica za resurse**, preuzima linije cena uloga sa podudarnom ulogom, ali sa nultim vrednostima za **Jedinica za resurse**. Kada dobije podudarni zapis cene uloga, stopa troškova se podrazumevano dobija od te evidencije. 

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, ovo ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise o ceni uloga sa podudarnim vrednostima svake od vrednosti dimenzije cene po redosledu prioriteta sa redovima koji imaju nulte vrednosti za te dimenzije koje dolaze poslednje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za trošak

Stavke procene za trošak se odnose na detalje ponude i predmeta ugovora za troškove, kao i linije procene troškova na projektu.

Kada se cenovnik troškova reši, sistem koristi kombinaciju polja **Uloga** i **Jedinica za resurse** na liniji procene za trošak radi podudaranja sa linijama **Cena kategorija** u rešenom cenovniku. Ako sistem pronađe liniju cena kategorija koja ima stopu troškova za kombinaciju polja **Kategorija** i **Jedinica**, tada je ta stopa troškova podrazumevana. Ako sistem ne može da nađe podudaranje sa vrednostima **Kategorija** i **Jedinica**, ili ako je u stanju da pronađe podudarnu liniju cena kategorija, ali metoda određivanja cene nije **Cena po jedinici**, stopa troškova je podrazumevano nula (0).
