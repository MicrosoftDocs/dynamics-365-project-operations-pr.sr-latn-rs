---
title: Utvrđivanje stope troškova za procene projekta i stvarne vrednosti
description: Ovaj članak pruža informacije o tome kako se određuju stope troškova za procene projekta i stvarne vrednosti.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410176"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Utvrđivanje stope troškova za procene projekta i stvarne vrednosti

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Da bi odredio cenovnik troška i cene troškova u proceni i stvarnim kontekstima, sistem koristi informacije u **poljima Datum**, **Valuta** i **Jedinica ugovaranja** povezanog projekta.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Određivanje stope troškova u proceni i stvarnim kontekstima za vreme

Procena konteksta vremena **odnosi** se na:

- Detalji reda ponude za **vreme**.
- Detalji reda ugovora za **vreme**.
- Dodeljivanje resursa na projektu.

Stvarni kontekst vremena **odnosi** se na:

- Redovi naloga unosa i korekcije za **vreme**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja stavke vremena.

Nakon što se utvrdi cenovnik troška, sistem dovršavanje sledećih koraka za unos podrazumevane stope troška.

1. Sistem se podudara sa kombinacijom polja **"Uloga"** i **"Jedinica resourcing" u** proceni ili stvarnom kontekstu **vremena u** odnosu na redove cene uloge u cenovnik. Ovo podudaranje pretpostavlja da koristite standardne dimenzije cena za trošak rada. Ako ste podesili sistem tako da odgovara poljima koja nisu ili **pored jedinice za** **uloge i resourcing**, koristi se druga kombinacija za preuzimanje odgovarajućeg reda cene uloga.
1. Ako sistem pronađe red cene uloge koji ima cenu troška za **kombinaciju "Uloga** **" i "Jedinica resovanja**", ta stopa troška se koristi kao podrazumevana stopa troška.
1. Ako sistem ne može da parira vrednostima **"Uloga** **" i "Jedinica resovanja**", preuzima redove cene uloga **koji imaju odgovarajuće vrednosti za polje "Uloga**", ali vrednosti "null **" za polje "Jedinica resourcing**". Nakon što sistem ima odgovarajući zapis cene uloge, stopa troška iz tog zapisa će se koristiti kao podrazumevana stopa troška.

> [!NOTE]
> Ako konfigurišete drugačiju određivanje prioriteta **polja "Uloga** **" i "Jedinica za resorsing**" ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise cena uloga koji imaju vrednosti koje se podudaraju sa svakom vrednošću dimenzije cena po redosledu prioriteta. Redovi koji imaju vrednosti "null" za te dimenzije su poslednji.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje stope troškova u stvarnim i procenjenim redovima za troškove

Procena konteksta za **troškove** odnosi se na:

- Detalji reda ponude za **trošak**.
- Detalji reda ugovora za **troškove**.
- Procene troškova na projektu.

Stvarni kontekst za troškove **odnosi** se na:

- Redovi naloga unosa i korekcije za **troškove**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja stavke troška.

Nakon što se utvrdi cenovnik troška, sistem dovršavanje sledećih koraka za unos podrazumevane stope troška.

1. Sistem se podudara sa kombinacijom polja "Kategorija **" i** " **Jedinica** " u proceni ili stvarnom kontekstu troškova **u** odnosu na redove cene kategorije u cenovnik.
1. Ako sistem pronađe red cene kategorije koji ima cenu troška za kombinaciju **"Kategorija"** **i "Jedinica** ", ta stopa troška se koristi kao podrazumevana stopa troška.
1. Ako sistem ne može da parira vrednostima "Kategorija" i **"Jedinica", cena je podrazumevano** postavljena na 0 **(** nula).**·**
1. U kontekstu procene, ako sistem može da pronađe odgovarajući red cena kategorije, ali je način određivanja **cena nešto drugo osim "Cena po jedinici**", stopa troška je **podrazumevano podešena na 0** (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Određivanje stope troškova u stvarnim i procenjenim redovima za Materijal

Procena konteksta **materijala** odnosi se na:

- Detalji reda ponude za **materijal**.
- Detalji reda ugovora za **materijal**.
- Materijalne procene na projektu.

Stvarni kontekst materijala **odnosi** se na:

- Redovi naloga unosa i korekcije za **materijal**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja evidencije korišćenja materijala.

Nakon što se utvrdi cenovnik troška, sistem dovršavanje sledećih koraka za unos podrazumevane stope troška.

1. Sistem koristi kombinaciju polja "Proizvod" **i "** **Jedinica"** u proceni ili stvarnom kontekstu **materijala u odnosu** na redove artikla cenovnka u cenovnik.
1. Ako sistem pronađe red stavke cenovnik koji ima stopu troška za kombinaciju **"Proizvod** **" i "Jedinica**", ta stopa troška se koristi kao podrazumevana stopa troška.
1. Ako sistem ne može da parira vrednostima **proizvoda** **i jedinice**, trošak po jedinici je podrazumevano **podešen na 0** (nula).
1. U proceni ili stvarnom kontekstu, ako sistem može da pronađe odgovarajući red stavke cenovnik, ali je način određivanja cena nešto **drugo osim iznosa valute**, trošak po jedinici je **podrazumevano podešen na 0**. Do ovog ponašanja dolazi zato što operacije projekta podržavaju samo **metod određivanja** cena iznosa valute za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
