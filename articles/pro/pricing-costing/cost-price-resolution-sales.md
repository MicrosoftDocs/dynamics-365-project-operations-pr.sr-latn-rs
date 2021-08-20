---
title: Rešavanje cena koštanja za procene i trenutno stanje projekta – jednostavno
description: Ova tema pruža informacije o načinu rešavanja cena koštanja u procenama projekata i trenutnom stanju.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997578"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Rešavanje cena koštanja za procene i trenutno stanje projekta – jednostavno 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Da bi rešio cene koštanja i cenovnik troškova za procene i stvarne podatke, sistem koristi informacije u poljima **Datum**, **Valuta** i **Ugovaračka jedinica** srodnog projekta. Nakon rešavanja cenovnika troškova, aplikacija rešava stopu troškova.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za vreme

Stavke procene za vreme odnose se na detalje o ponudama i predmetima ugovora za dodeljivanje vremena i resursa na projektu.

Nakon rešavanja problema sa cenovnikom troškova, polja **Uloga** i **Jedinica za određivanje resursa** u redu procene za Vreme se uparuju sa redovima cena uloga u cenovniku. Ovo podudaranje pretpostavlja da za troškove rada koristite standardne aspekte za određivanje cena. Ako ste konfigurisali sistem tako da podudara polja umesto ili pored polja **Uloga** i **Jedinica za resurse**, onda će se koristiti različita kombinacija za preuzimanje podudarne linije cena uloga. Ako aplikacija pronađe liniju cena uloga koja ima stopu troškova za kombinaciju polja **Uloga** i **Jedinica za resurse**, tada je ta stopa troškova podrazumevana. Ako aplikacija ne može da se podudari sa vrednostima polja **Uloga** i **Jedinica za resurse**, preuzima linije cena uloga sa podudarnom ulogom, ali sa nultim vrednostima za **Jedinica za resurse**. Kada dobije podudarni zapis cene uloga, stopa troškova se podrazumevano dobija od te evidencije. 

> [!NOTE]
> Ako ste konfigurisali drugačije određivanje prioriteta za polja **Uloga** i **Jedinica za resurse**, ili ako imate druge dimenzije koje imaju veći prioritet, ovo ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise o ceni uloga sa podudarnim vrednostima svake od vrednosti dimenzije cene po redosledu prioriteta sa redovima koji imaju nulte vrednosti za te dimenzije koje dolaze poslednje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Rešite stope troškova na stavkama trenutnog stanja i procene za trošak

Stavke procene za trošak se odnose na detalje ponude i predmeta ugovora za troškove, kao i linije procene troškova na projektu.

Nakon što se reši problem sa cenovnikom troškova, sistem koristi kombinaciju polja **Kategorija** i **Jedinica** u redu procene troškova da bi ga upario sa redovima **Cena kategorije** u cenovniku u kome su otklonjeni problemi. Ako sistem pronađe liniju cena kategorija koja ima stopu troškova za kombinaciju polja **Kategorija** i **Jedinica**, tada je ta stopa troškova podrazumevana. Ako sistem ne može da upari vrednosti **Kategorija** i **Jedinica** ili ako može da pronađe odgovarajući red cene kategorije, ali metod određivanja cene nije **Cena po jedinici**, stopa troškova je podrazumevano nula (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Rešavanje stopa troškova na stvarnim i procenjenim stavkama za materijal

Stavke procene za materijal odnose se na detalje o stavkama ponuda i predmetima ugovora za materijale i stavke procene materijala na projektu.

Kada se reši cenovnik troškova, sistem koristi kombinaciju polja **Proizvod** i **Jedinica** na liniji procene za procenu materijala koja se podudara sa redovima **Stavke u cenovniku** na rešenom cenovniku. Ako sistem pronađe red cene proizvoda koji ima stopu troškova za kombinaciju polja **Proizvod** i **Jedinica**, podrazumevana je stopa troškova. Ako sistem ne može da se podudara sa vrednostima **Proizvod** i **Jedinica** ili ako je u mogućnosti da pronađe odgovarajuću stavku cenovnika, ali metoda određivanja cena se zasniva na standardnoj ceni ili trenutnoj ceni, a nijedna nije definisana na proizvodu, cena jedinice je podrazumevano nula.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
