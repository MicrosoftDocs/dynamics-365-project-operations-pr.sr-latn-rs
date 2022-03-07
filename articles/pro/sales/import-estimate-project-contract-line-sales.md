---
title: Uvoz procene u predmet ugovora zasnovan na projektu – jednostavno
description: Ova tema pruža informacije o uvozu finansijskih procena iz projekta u predmet ugovora.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fb85d835789da82f22ae007addb6757ab3c166180992e4ce3a5c85606be6671d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997263"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Uvoz procene u predmet ugovora zasnovan na projektu – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations možete da uvozite procene iz projekta u predmet ugovora zasnovan na projektu.

1. Proverite da li je popunjeno polje **Projekat** na predmetu ugovora zasnovanom na projektu.
2. Na kartici **Detalji predmeta ugovora**, na podformi izaberite **Uvoz iz procene projekta**. Otvoriće se stranica dijaloga sa opcijama rezimiranja. Dostupne opcije rezimiranja su **Klasa transakcije**, **Kategorija**, **Uloga** i **Projektni zadatak**.
3. Na osnovu vašeg izbora rezimiranja, kopiraju se procena iz projekta za sve klase transakcija i zadaci uključeni u ovaj predmet ugovora. Da biste proverili koje su klase transakcija uključene, na kartici **Opšti podaci** u premetu ugovora zasnovanog na projektu proverite vrednosti za **Uključi vreme**, **Uključi troškove** i **Uključi naknade**. 
4. Da biste videli koji su zadaci obuhvaćeni, odaberite karticu **Zadaci koji se naplaćuju** u predmetu ugovora. Na osnovu povezanih zadataka koji imaju polje **Uključene klase transakcija** podešeno na **Da**, sve procene za te kombinacije zadataka i klasa transakcija uvoze se u predmet ugovora.

Kada uvezete procene, sistem će podrazumevano odrediti cene na osnovu projektnih cenovnika koji su priloženi uz ugovor i vrste fakturisanja postavljene u predmetu ugovora zasnovanog na projektu. Ako su zadatak, uloga ili kategorija podešeni u predmetu ugovora zasnovanog na projektu kao nenaplativi, uvezena stavka procene biće nenaplativa i neće se dodati u ugovornu vrednost predmeta ugovora.

Kada predmet ugovora sadrži detalje o stavci, polja **Vrednost ugovora** i **Procenjeni porez** u predmetu ugovora su rezimirana i ne mogu se uređivati.

Kada je izabrano više opcija rezimiranja, sistem pokušava da rezimira po svim odabranim opcijama. Rezultat rezimiranja ima više uvezenih predmeta ugovora nego ako izaberete samo jednu opciju rezimiranja.

Na primer, ako projekat ima sledeće stavke procene za troškove:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |

Kada korisnik izabere da rezimira po **klasi transakcije**, biće uvezene sledeće informacije:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1.10.2020. | 3.34 | 840 | 2800 |

Kada korisnik izabere da rezimira po **klasi transakcije** i **kategoriji**, biće uvezene sledeće informacije:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| &nbsp;| Hotel | 1.10.2020. | 6 | 200 | 1200 |

Kada korisnik izabere da rezimira po **klasi transakcije**, **kategoriji** i **zadatku čvora lista**, biće uvezene sledeće informacije: Uočite da je ovaj rezultat isti kao i onaj na projektu:

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]