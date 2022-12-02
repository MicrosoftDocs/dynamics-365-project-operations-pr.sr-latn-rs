---
title: Uvezite procenu u predmet ugovora zasnovan na projektu
description: Ovaj članak pruža informacije o načinu uvoza procena iz projekta u predmetu ugovora.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4a298cbcb8d13447c0f6e264d2aa85ad7ed43bf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915109"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Uvezite procenu u predmet ugovora zasnovan na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

U usluzi Dynamics 365 Project Operations možete da uvozite procene iz projekta u predmet ugovora zasnovan na projektu.

1. Proverite da li je popunjeno polje **Projekat** na predmetu ugovora zasnovanom na projektu.
2. Na kartici **Detalji predmeta ugovora**, na podformi izaberite **Uvoz iz procene projekta**. Otvoriće se stranica dijaloga sa opcijama rezimiranja. Dostupne opcije rezimiranja su **Klasa transakcije**, **Kategorija**, **Uloga** i **Projektni zadatak**. Na osnovu vašeg izbora rezimiranja, kopira se procena iz projekta za sve klase transakcija uključene u ovaj predmet ugovora. 
3. Da biste proverili koje su klase transakcija uključene, na kartici **Opšti podaci** u premetu ugovora proverite vrednosti za **Uključi vreme**, **Uključi troškove** i **Uključi naknade**.

Kada uvezete procene, aplikacija će podrazumevano odrediti cene na osnovu projektnih cenovnika koji su priloženi uz ugovor i vrste fakturisanja postavljene u predmetu ugovora zasnovanog na projektu. Ako su uloga ili kategorija podešeni u predmetu ugovora zasnovanog na projektu kao nenaplativi, uvezena stavka procene za tu ulogu ili kategoriju biće nenaplativa i neće se dodati u ugovornu vrednost predmeta ugovora.

Kada predmet ugovora sadrži detalje o stavci, polja **Vrednost ugovora** i **Procenjeni porez** u predmetu ugovora su rezimirana i ne mogu se uređivati.

Kada je izabrano više opcija rezimiranja, sistem pokušava da rezimira po svim odabranim opcijama. Rezultat rezimiranja ima više uvezenih predmeta ugovora nego ako izaberete samo jednu opciju rezimiranja.

Na primer, ako je projekat imao sledeće stavke procene za troškove:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |

Kada korisnik izabere da rezimira po **klasi transakcije**, biće uvezene sledeće informacije:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1.10.2020. | 3.34 | 840 | 2800 |

Kada korisnik izabere da rezimira po **klasi transakcije** i **kategoriji**, biće uvezene sledeće informacije:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1.10.2020. | 6 | 200 | 1200 |

Kada korisnik izabere da rezimira po **klasi transakcije**, **kategoriji** i **zadatku čvora lista**, biće uvezene sledeće informacije: Uočite da je ovaj rezultat isti kao i onaj na projektu:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]