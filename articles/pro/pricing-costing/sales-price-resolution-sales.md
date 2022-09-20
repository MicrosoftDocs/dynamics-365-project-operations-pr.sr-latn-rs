---
title: Utvrđivanje prodajnih cena za procene i trenutno stanje projekta
description: Ovaj članak pruža informacije o načinu na koji se određuju prodajne cene za procene projekta i stvarne vrednosti.
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

Da bi odredio prodajne cene za procene i stvarne vrednosti u korporaciji Microsoft Dynamics 365 Project Operations, sistem prvo koristi datum i valutu u dolaznoj proceni ili stvarnom kontekstu za određivanje cenovnik prodaje. U stvarnom kontekstu posebno, sistem koristi polje "Datum transakcije **"** da bi odredio koji cenovnik je primenljiv. Vrednost **datuma transakcije** dolazne ili stvarne vrednosti se poredi sa **vrednostima "Efektivni početak" (samo za vremensku zonu)** **i Efektivni kraj (nezavisno od vremenske zone)** na cenovnik. Nakon utvrđivanja prodajnog cenovnka, sistem određuje prodajni ili redni kurs.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Određivanje stope prodaje u stvarnim i redovima procene vremena

Procena konteksta vremena **odnosi** se na:

- Detalji reda ponude za **vreme**.
- Detalji reda ugovora za **vreme**.
- Dodeljivanje resursa na projektu.

Stvarni kontekst vremena **odnosi** se na:

- Redovi naloga unosa i korekcije za **vreme**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja stavke vremena.
- Detalji reda fakture za **vreme**. 

Nakon što se utvrdi cenovnik prodaje, sistem dovršavanje sledećih koraka za unos podrazumevane stope računa.

1. Sistem se podudara sa kombinacijom polja **"Uloga"** i **"Jedinica resourcing" u** proceni ili stvarnom kontekstu **vremena u** odnosu na redove cene uloge u cenovnik. Ovo podudaranje pretpostavlja da koristite dimenzije određivanja cena za cene računa. Ako ste cene konfigurisali tako da budu zasnovane na poljima **koja nisu ili pored jedinice "Uloga** **" i "Resourcing",** ta kombinacija polja se koristi za preuzimanje odgovarajućeg reda cene uloge.
1. Ako sistem pronađe red cene uloge koji ima cenu računa za **kombinaciju "Uloga** **" i "Jedinica za resorsing**", ta stopa računa se koristi kao podrazumevana stopa fakturisanja.
1. Ako sistem ne može da parira vrednostima **"Uloga** **" i "Jedinica za resorsing**", on preuzima redove cene uloga koji imaju odgovarajuće **vrednosti za polje "Uloga",** ali vrednosti "null" **za polje "Jedinica resursa**". Kada sistem pronađe odgovarajući zapis cene uloge, stopa računa iz tog zapisa će biti korišćena kao podrazumevana stopa računa. Ovo podudaranje preuzima konfiguraciju "Out-box" za relativni prioritet **"Uloga** **" u odnosu na "Jedinicu za resourcing**" kao dimenziju cene prodaje.

> [!NOTE]
> Ako konfigurišete drugačiju određivanje prioriteta **polja "Uloga** **" i "Jedinica za resorsing**" ili ako imate druge dimenzije koje imaju veći prioritet, prethodno ponašanje će se promeniti u skladu sa tim. Sistem preuzima zapise cena uloga koji imaju vrednosti koje se podudaraju sa svakom vrednošću dimenzije cena po redosledu prioriteta. Redovi koji imaju vrednosti "null" za te dimenzije su poslednji.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Određivanje stope prodaje u stvarnim i procenjenim redovima za troškove

Procena konteksta za **troškove** odnosi se na:

- Detalji reda ponude za **trošak**.
- Detalji reda ugovora za **troškove**.
- Redovi procene troškova na projektu.

Stvarni kontekst za troškove **odnosi** se na:

- Redovi naloga unosa i korekcije za **troškove**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja stavke troška.
- Detalji reda fakture za **trošak**. 

Nakon što se utvrdi cenovnik prodaje, sistem dovršavanje sledećih koraka za unos podrazumevane jedinične prodajne cene.

1. Sistem se podudara sa kombinacijom polja Kategorija i Jedinica u redu procene troškova **u odnosu** na redove cene kategorije u cenovnik.**·** **·**
1. Ako sistem pronađe red cene kategorije koji ima prodajni kurs za kombinaciju **"Kategorija** **" i "Jedinica**", taj prodajni kurs se koristi kao podrazumevani prodajni kurs.
1. Ako sistem pronađe odgovarajući red cene kategorije, metod određivanja cena može da se koristi za unos podrazumevane prodajne cene. Sledeća tabela prikazuje podrazumevano ponašanje za cene troškova u operacijama projekta.

    | Kontekst | Način određivanja cena | Podrazumevana cena |
    | --- | --- | --- |
    | Procena | Cena po jedinici | Na osnovu reda cene kategorije. |
    |        | Po ceni | 0.00 |
    |        | Provizija preko troškova | 0.00 |
    | Stvarna vrednost | Cena po jedinici | Na osnovu reda cene kategorije. |
    |        | Po ceni | Na osnovu povezanih troškova. |
    |        | Provizija preko troškova | Naznake se primenjuju, kao što je definisano redom cene kategorije, na stopu troška po jedinici povezanog troška. |

1. Ako sistem ne može da parira vrednostima **kategorije** **i** jedinice, stopa prodaje je podrazumevano **podešena na 0** (nula).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Određivanje prodajnih stopa u stvarnim i procenjenim redovima za Materijal

Procena konteksta **materijala** odnosi se na:

- Detalji reda ponude za **materijal**.
- Detalji reda ugovora za **materijal**.
- Redovi za procenu materijala na projektu.

Stvarni kontekst materijala **odnosi** se na:

- Redovi naloga unosa i korekcije za **materijal**.
- Redovi naloga koji se kreiraju prilikom prosleđivanja evidencije korišćenja materijala.
- Detalji reda fakture za **materijal**. 

Nakon što se utvrdi cenovnik prodaje, sistem dovršavanje sledećih koraka za unos podrazumevane jedinične prodajne cene.

1. Sistem se podudara sa kombinacijom polja "**Proizvod" i**"Jedinica **" u redu procene za Materijal** u **odnosu na redove artikla cenovnka** u cenovnik.
1. Ako sistem pronađe red artikla cenovnik koji ima prodajni kurs **za kombinaciju "Proizvod** **i jedinica**" i ako je način određivanja cena iznos **valute**, koristiće se prodajna cena navedena u redu cenovnka. 
1. Ako se **vrednosti** polja **"Proizvod"** i "Jedinica" ne podudaraju ili ako je način određivanja cena nešto **drugo od iznosa valute**, stopa prodaje je podrazumevano **podešena na 0** (nula). Do ovog ponašanja dolazi zato što operacije projekta podržavaju samo **metod određivanja** cena iznosa valute za materijale koji se koriste na projektu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
