---
title: Uvoz procena za projekat u stavku ponude zasnovanu na projektu – jednostavno
description: Ova tema pruža informacije o načinu uvoza procena iz projekta u stavku ponude.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5ac7827f3499aafb63f6bc0b8580ca52e883f272464532bd353170a12b3ae55
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986148"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Uvoz procena za projekat u stavku ponude zasnovanu na projektu 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ako se projekat kreira tokom faze pretprodaje, možete izabrati uvoz finansijske procene iz projekta u stavku ponude zasnovanu na projektu.

1. Uverite se da stavka ponude zasnovana na projektu sadrži informacije o projektu u polju **Projekat**.
2. Na kartici **Detalji stavke ponude**, izaberite **Uvoz iz procene projekta**.
3. Na stranici dijaloga koja se otvori, izaberite jednu od sledećih opcija rezimiranja.

  - **Klasa transakcije**
  - **Kategorija**
  - **Uloga** 
  - **Projektni zadatak**

Na osnovu vašeg izbora, kopira se procena iz projekta za sve klase transakcija koje su uključene u ovu stavku ponude. Da biste proverili koje su klase transakcija uključene, izaberite karticu **Opšti podaci** na stavki ponude zasnovane na projektu i proverite vrednosti za **Sadrži vreme**, **Sadrži troškove**, **Sadrži materijale** i **Sadrži naknade**.  Da biste proverili koji su zadaci obuhvaćeni, odaberite karticu **Zadaci koji se naplaćuju** u stavci ponude.

Na osnovu povezanih zadataka i uključenih klasa transakcija, procene za te kombinacije zadataka i klasa transakcija uvoze se u stavku ponude.

Kada uvezete procene, sistem će podrazumevano odrediti cene na osnovu projektnih cenovnika koji su priloženi uz ponudu i vrste fakturisanja postavljene u stavci ponude zasnovane na projektu. Ako su zadatak, uloga ili kategorija podešeni u stavci ponude zasnovanoj na projektu kao nenaplativi, uvezena stavka procene postaviće se kao nenaplativa i neće se dodati u navedenu vrednost stavke ponude.

Kada stavka ponude sadrži detalje o stavci, polja **Vrednost ponude** i **Procenjeni porez** u stavci ponude su rezimirana i ne mogu se uređivati.

Kada je izabrano više opcija rezimiranja, sistem pokušava da rezimira po svim odabranim opcijama. To znači da će izlaz uvezenih stavki ponude biti veći nego ako ste izabrali samo jednu opciju rezimiranja.

Na primer, ako je projekat imao sledeće stavke procene za troškove.

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |

Kada korisnik izabere da rezimira po klasi transakcije, biće uvezene sledeće informacije.

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
|||1.10.2020. | 3.34 | 840 | 2800 |

Kada korisnik izabere da rezimira po klasi transakcije i kategoriji, biće uvezene sledeće informacije.

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| | Hotel | 1.10.2020. | 6 | 200 | 1200 |

Kada korisnik izabere da rezimira po klasi transakcije, kategoriji i zadatku čvora lista, biće uvezene sledeće informacije. Uočite da je ovaj rezultat isti kao i onaj na projektu.

| Zadatak | Kategorija | Datum | Količina | Cena po jedinici | Iznos |
| --- | --- | --- | --- | --- | --- |
| Zadatak A | Avionska karta | 1.10.2020. | 4 | 400 | 1600 |
| Zadatak B | Hotel | 1.10.2020. | 4 | 200 | 800 |
| Zadatak C | Hotel | 1.11.2020. | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
