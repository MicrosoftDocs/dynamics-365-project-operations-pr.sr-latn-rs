---
title: Upravljanje potencijalnim klijentima – jednostavno
description: Ova tema pruža informacije o upravljanju potencijalnim klijentima zasnovanim na projektu (Pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1d3a54a9fcb0b0cef9461219e22305afbf5266e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272855"
---
# <a name="manage-leads---lite"></a>Upravljanje potencijalnim klijentima – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Potencijalnim klijentima zasnovanim na projektu moguće je upravljati i kvalifikovati u usluzi Project Operations. Proces upravljanja potencijalnim klijentima uključuje stvaranje potencijalnih klijenata zasnovanih na radu i njihovo kvalifikovanje. 

## <a name="list-of-project-sales-leads"></a>Spisak potencijalnih klijenata u projektu

U odeljku **Prodaja**, u levom oknu za navigaciju, otvorite stranicu liste **Potencijalni klijenti** da biste videli listu svih zapisa o potencijalnim klijentima u sistemu. Potencijalni klijenti na listi su zasnovani na poslu i drugim tipovima potencijalnih klijenata koje možete kreirati ako imate i Dynamics 365 Sales ili Dynamics 365 Field Service aplikacije.

Možete da kreirate filtrirani prikaz da biste videli samo potencijalne klijente zasnovane na projektu kreiranjem filtera u vrednosti **Tip**. Na primer, možete izabrati da se prikazuju samo potencijalni klijenti zasnovani na poslu.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Kreiranje novog potencijalnog klijenta za pogodbu zasnovanu na projektu

Kada se potencijalni klijent zasnovan na projektu kvalifikuje, kreiraju se mogućnost za poslovanje i poslovni kontakt. Mogućnost za poslovanje zasnovana na projektu je polazna tačka za aktivnosti potrage za prodajom u fazi mogućnosti za poslovanje. Mogućnosti za poslovanje zasnovane na projektu imaju jedinstvene mogućnosti potrebne za prodaju projektnog rada. Te mogućnosti uključuju:

- Vreme i materijal i metode obračuna sa fiksnom cenom
- Više cenovnika za ljudske resurse, troškove i materijale, koji stupaju na snagu određenog datuma i nastali su u projektima.

Da bi kvalifikovani potencijalni klijent automatski kreirao mogućnost za poslovanje, podesite atribut **Tip** na **Zasnovan na poslu** kada kreirate potencijalnog klijenta. Ako odaberete drugi tip, potencijalni klijent neće stvoriti mogućnost za poslovanje zasnovanu na projektu kada je kvalifikovan. Ako se ne stvori mogućnost za poslovanje zasnovana na projektu, mogućnosti specifične za projekat neće biti dostupne u daljim procesima prodaje.

Sledeća tabela uključuje važne informacije o polju za potencijalnog klijenta i kasnije posledice tih polja.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tema | Kartica Opšti podaci | Ovo polje za tekst treba da sadrži kratak opis ponude. | Tema potencijalnog klijenta podrazumevano će biti tema mogućnosti za poslovanje, kao i naziv ponude i projektnog ugovora. |
| Tip | Kartica Opšti podaci | Ovo polje skupa opcija ima sledeće opcije:</br>- Zasnovano na poslu (dostupno samo kada je instalirana usluga Project Operations)</br>- Zasnovano na stavci (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- Zasnovano na servisnom održavanju (dostupno kada je instalirana usluga Field Service) | Kada se vrednost ovog polja postavi na **Zasnovano na poslu** za potencijalnog klijenta, potencijalni klijent je kvalifikovan da kreira mogućnost za poslovanje zasnovanu na projektu. Od mogućnosti za poslovanje zasnovane na projektu se zahteva da omogući sva proširenja i funkcije specifične za projekat u kasnijem procesu prodaje za ovu pogodbu. |
| Ime | Kartica Opšti podaci | Lično ime kontakta potencijalnog klijenta | Kada se potencijalni klijent kvalifikuje, kreiraju se poslovni kontakt, kontakt i mogućnost za poslovanje. Ovde se postavlja vrednost ličnog imena kontakta. |
| Prezime | Kartica Opšti podaci | Prezime kontakta potencijalnog klijenta | Kada se potencijalni klijent kvalifikuje, kreiraju se poslovni kontakt, kontakt i mogućnost za poslovanje. Ovde se postavlja vrednost prezimena kontakta. |
| Preduzeće | Kartica Opšti podaci | Naziv kompanije potencijalnog klijenta | Kada se potencijalni klijent kvalifikuje, kreiraju se poslovni kontakt, kontakt i mogućnost za poslovanje. Ime kreiranog poslovnog kontakta je vrednost koja je ovde postavljena. |
| Valuta | Kartica Detalji | Valuta potencijalnog klijenta | Kada se potencijalni klijent kvalifikuje, kreiraju se poslovni kontakt, kontakt i mogućnost za poslovanje. Valuta kreiranog poslovnog kontakta je vrednost koja je ovde postavljena. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalifikovanje novog potencijalnog klijenta zasnovanog na projektu

Potencijalni klijenti koji imaju vrednost **Tip** postavljenu na **Zasnovan na poslu** nazivaju se potencijalni klijenti zasnovani na projektima. Kada se potencijalni klijent na zasnovan na projektu kvalifikuje, kreira se sledeće:

- Potencijalni klijent koji koristi polje **Preduzeće** od potencijalnog klijenta.
- Zapis kontakta povezan sa poslovnim kontaktom na osnovu vrednosti u poljima **Ime** i **Prezime** potencijalnog klijenta.
- Mogućnost za poslovanje zasnovana na projektu koja ima polje **Tip** postavljeno na **Zasnovano na poslu**.

Za detaljnije informacije o kvalifikovanim potencijalnim klijentima, pogledajte članak [Kvalifikovanje ili konvertovanje potencijalnih klijenata](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Tok poslovnog procesa za pogodbe zasnovane na projektu

Sledeći tokovi poslovnih procesa podržani su za pogodbe zasnovane na projektu u usluzi Project Operations:

- Poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje
- Proces prodaje mogućnosti za poslovanje

Poslovni proces od potencijalnog klijenta do mogućnosti za poslovanje podržava sledeće faze:

| Naziv faze | Mapirani entitet | Funkcionalnost |
| --- | --- | --- |
| Kvalifikuj | Potencijalni klijent | Kvalifikujte potencijalnog klijenta da kreira poslovni kontakt, kontakt i mogućnost za poslovanje. |
| Razvij | Mogućnost za poslovanje | Razvijte mogućnost za poslovanje da biste dodali više informacija o obuhvaćenom poslu, ključnim zainteresovanim stranama i konkurenciji. |
| Predloži | Mogućnost za poslovanje | Razvijte predlog i dobijte odobrenje od internog tima za pregled. |
| Zatvaranje | Mogućnost za poslovanje | Ostvarite priliku da zaključite posao. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]