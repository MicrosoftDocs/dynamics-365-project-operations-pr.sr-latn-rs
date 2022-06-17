---
title: Opcije podugovaranja za članove projektnog tima
description: Ovaj članak sadrži objašnjenja o opcijama podizvođanja za članove projektnog tima u korporaciji Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88a76ccf73a4b6cfa13a67b50130b007f244d831
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919801"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcije podugovaranja za članove projektnog tima

[!include [banner](../../includes/dataverse-preview.md)]

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

U korporaciji Microsoft Dynamics 365 Project Operations možete da procenite opcije podizvođanja koje su dostupne za jednog ili više članova projektnog tima. Dostupne opcije podizvođanja vam omogućavaju da:

- Kreirajte novi podizvođači i/ili kreirajte nove redove na postojećem podizvođači za izabrane članove projektnog tima. 
- Rezervišite u odnosu na već postojeći red podizvođaиa i podizvoрaиa. 

Možete odabrati jednu od dostupnih opcija podizvođanja za članove generičkog projektnog tima ili odabrati neki od članova projektnog tima koji imaju imenovani resurs koji je radnik po ugovoru. 

Nema dostupnih opcija podizvođanja za sledeće:

- Članovi projektnog tima koji su bili zaposleni. 
- Članovi projektnog tima koji su već povezani sa redom podizvođačima i podizvođačima. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podizvođači neodobravanog člana projektnog tima

Da biste pregledali i odabrali jednu od dostupnih opcija podizvođača za generičkog ili neodobravanog člana projektnog tima, sledite ove korake:

1. Izaberite jedan ili više zapisa članova projektnog tima u kojima je resurs generički resurs.
2. Uverite se da nijedan od izabranih zapisa članova projektnog tima nije već podizvođačen. 
3. Izaberite **opcije podizvođanja u** podmrežnoj mreži članova projektnog tima. Otvoriće **se dijalog opcija podizvođanja**. 
4. Ako ste izabrali samo jedan zapis člana projektnog tima u koraku 1, biće dostupne sledeće opcije:
    - Kreirajte nove redove podizvođači. 
    - Rezervišite u odnosu na postojeći podizvođaи Ako ste izabrali viљe zapisa иlaka projektnog tima u koraku 1, onda je jedina dostupna opcija kreiranje novih redova podizvoрaиa.
5. Opcija rezervisanja u odnosu na postojeći red podizvođači vam omogućava da izaberete red podizvođači i podizvođači protiv kojih želite da rezervišete. Kada birate red podizvođače da biste rezervisali kapacitet, trebalo bi da se uverite da je izabrani red podizvođače za vreme i da se uloga potrebna članu projektnog tima podudara sa ulogom koja je kupljena u redu podizvođače.
6. Kada izaberete da kreirate nove redove podizvođači za članove projektnog tima, sistem će vam dozvoliti da izaberete podizvođaи koji želite da kreirate u ovim redovima. Podizvođači u kojima ste izabrali da kreirate nove redove trebalo bi da se nađu u statusu radne **verzije**. Pomoću ove opcije za kreiranje novih redova podizvođačima za izabrane članove projektnog tima, sistem će kreirati jedan red podizvođanja za vreme za svakog člana projektnog tima. Uloga, časovi i datumi biće kopirani iz člana projektnog tima u svaki red podizvođača koji je kreiran. 
7. Kada je generički član tima povezan sa redom podizvođač i podizvođač, **polje "Vrsta radnika" u** redu generičkog člana tima biće ažurirano u "**Radnik po ugovoru",** **a vrednost "Validnost** podizvođaca" na vrednost "Važeće **"**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podizvođači osoblja projektnog tima

Kao i generički ili neodgovarajući članovi tima, takođe možete da prikažete opcije podizvođača za člana tima projekta sa osobljem sve dok je član tima sa osobljem radnik po ugovoru. Da biste pregledali i odabrali jednu od dostupnih opcija podizvođanja za osoblje ili imenovanog člana projektnog tima, sledite ove korake:

1. Izaberite jedan ili više zapisa članova projektnog tima u kojima je resurs imenovani radnik po ugovoru.
2. Uverite se da nijedan od izabranih zapisa članova projektnog tima nije već podizvođačen. 
3. Izaberite **opcije podizvođanja u** podmrežnoj mreži članova projektnog tima. Otvoriće **se dijalog opcija podizvođanja**. 
4. Ako ste izabrali samo jedan zapis člana projektnog tima u koraku 1, biće dostupne sledeće opcije:
      - Kreirajte nove redove podizvođači.
      - Rezervišite u odnosu na postojeći podizvođaи.
  Ako ste izabrali više zapisa članova projektnog tima u koraku 1, jedina dostupna opcija je kreiranje novih redova podizvođači.
5. Opcija rezervisanja u odnosu na postojeći red podizvođači vam omogućava da izaberete red podizvođači i podizvođači protiv kojih želite da rezervišete. Kada birate red podizvođače da biste rezervisali kapacitet, trebalo bi da obezbedite sledeće:
      - Izabrani red podizvođači je za vreme. 
      - Uloga potrebna članu projektnog tima podudara se sa ulogom koja je kupljena u redu podizvođači. 
      - Dobavljač sa kog je povezan radnik po ugovoru je isti kao dobavljač u podizvođači.
6. Kada izaberete da kreirate nove redove podizvođači za članove projektnog tima, sistem će vam dozvoliti da izaberete podizvođaи koji želite da kreirate u ovim redovima. Ovom opcijom treba da se uverite da je dobavljač kome pripada radnik po ugovoru isti kao dobavljač u podizvođači. 
7. Podizvođači u kojima ste izabrali da kreirate nove redove trebalo bi da se nađu u statusu radne **verzije**. Pomoću ove opcije za kreiranje novih redova podizvođačima za izabrane članove projektnog tima, sistem će kreirati jedan red podizvođanja za vreme za svakog člana projektnog tima. Uloga, časovi i datumi biće kopirani iz člana projektnog tima u svaki red podizvođača koji je kreiran.  
8. Kada je imenovani član tima povezan sa redom podizvođač i podizvođač, **polje "Vrsta radnika" u** imenovanom redu člana tima biće ažurirano u "**Radnik po ugovoru",** **a vrednost "Validnost** podizvođaca" na vrednost "Važeće **"**.

## <a name="re-costing-subcontractor-assignments"></a>Ponovni troškovi dodeljivanja podizvođača

Kada je član projektnog tima (generički ili imenovan) povezan sa redovima podizvođačem **pomoću dijaloga "Opcije podizvođanja** ", sve dodele zadacima koje član tima ima biće ponovo skupljene na osnovu nabavnog cenovnog spiska priloženog podizvođačem. Na kartici **Procene** na stranici **Detalji projekta** izaberite **dugme Ažuriraj cene** da biste videli ažurirane cene i/ili troškove koji su rezultat odluke o podizvođačima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
