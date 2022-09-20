---
title: Utvrđivanje stope troškova za procene i stvarne vrednosti zasnovane na projektu
description: Ovaj članak pruža informacije o tome kako se određuju stope troškova za procene i stvarne vrednosti zasnovane na projektu.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475296"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Utvrđivanje stope troškova za procene i stvarne vrednosti zasnovane na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da bi odredio cene troškova za procene i stvarne vrednosti u korporaciji Microsoft Dynamics 365 Project Operations, sistem prvo koristi datum i valutu u dolaznoj proceni ili stvarnom kontekstu za određivanje cenovnik prodaje. U stvarnom kontekstu posebno, sistem koristi polje "Datum transakcije **"** da bi odredio koji cenovnik je primenljiv. Vrednost **datuma transakcije** dolazne ili stvarne vrednosti se poredi sa **vrednostima "Efektivni početak" (samo za vremensku zonu)** **i Efektivni kraj (nezavisno od vremenske zone)** na cenovnik. Nakon utvrđivanja cenovnik troška, sistem određuje cenu troška.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Određivanje stope troškova u proceni i stvarnim kontekstima za vreme

Procena konteksta vremena **odnosi** se na:

- Detalji reda ponude za **vreme**.
- Detalji reda ugovora za **vreme**.
- Dodeljivanje resursa na projektu.

Stvarni kontekst vremena **odnosi** se na:

- Redovi naloga unosa i korekcije za **vreme**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja stavke vremena.

Nakon što se utvrdi cenovnik troška, sistem dovršavanje sledećih koraka za unos podrazumevane stope troška.

1. Sistem se podudara sa kombinacijom **polja "Uloga**", **"Resourcing Company**" **i "Jedinica za resourcing"** u proceni ili stvarnom kontekstu **vremena u** odnosu na redove cene uloge u cenovniku. Ovo podudaranje pretpostavlja da koristite standardne dimenzije cena za trošak rada. Ako ste konfigurisali **sistem tako da se podudara sa poljima koja nisu ili pored "Uloga**", **"Resourcing Company** " **i "Resourcing Unit**", koristi se druga kombinacija za preuzimanje reda cene uloge koja se podudara.
1. Ako sistem pronađe red cene uloge koji ima **cenu troška za kombinaciju "Uloga**", **"Preduzeće za resourcing**" **i "Jedinica za resourcing** ", ta stopa troška se koristi kao podrazumevana stopa troška.
1. Ako sistem ne može da parira **vrednostima "Uloga**", **"Resourcing Company**" **i "Jedinica resourcing** ", on spušta dimenziju koja ima najniži prioritet, traži redove cena uloga koji se podudaraju sa vrednostima druge dve dimenzije i nastavlja da progresivno spušta dimenzije dok se ne utvrdi odgovarajući red cena uloge. Stopa troška iz tog zapisa će biti korišćena kao podrazumevana stopa troška. Ako sistem ne pronađe odgovarajući red cene uloge, cena će podrazumevano biti postavljena **na 0** (nula).

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
