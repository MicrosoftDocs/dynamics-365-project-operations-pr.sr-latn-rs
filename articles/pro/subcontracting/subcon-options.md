---
title: Opcije podugovaranja za članove projektnog tima
description: Ovaj članak sadrži objašnjenja o opcijama podugovaranja za članove projektnog tima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522296"
---
# <a name="subcontracting-options-for-project-team-members"></a>Opcije podugovaranja za članove projektnog tima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U usluzi Microsoft Dynamics 365 Project Operations možete da procenite opcije podugovaranja koje su dostupne za jednog ili više članova projektnog tima. Dostupne opcije podugovaranja će vam omogućiti da:

- Kreirate novi podugovor i/ili kreirate nove predmete na postojećem podugovoru za izabrane članove projektnog tima. 
- Rezervišete iz već postojećeg podugovora i predmeta podugovora. 

Možete odabrati jednu od dostupnih opcija podugovaranja za članove generičkog projektnog tima ili odabrati nekog od članova projektnog tima koji su među osobljem kao imenovani resurs koji je radnik po ugovoru. 

Ne postoje dostupne opcije podugovaranja za sledeće:

- Članovi projektnog tima koji su u osoblje koje je zaposleno. 
- Članovi projektnog tima koji su već pridruženi podugovoru i predmetu podugovora. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Podugovaranje člana projektnog tima bez resursa

Da biste pregledali i odabrali neku od dostupnih opcija podugovaranja za generičkog ili člana projektnog tima bez resursa, pratite ove korake:

1. Izaberite jedan ili više zapisa članova projektnog tima u kojima je resurs generički resurs.
2. Uverite se da nijedan od izabranih zapisa članova projektnog tima nije već podugovoren. 
3. Izaberite **Opcije podugovaranja** u podmreži članova projektnog tima. Otvara se dijalog **Opcije podugovaranja**. 
4. Ako ste izabrali samo jedan zapis člana projektnog tima u 1. koraku, biće dostupne sledeće opcije:
    - Kreiranje novih predmeta podugovora. 
    - Rezervišite iz postojećeg podugovora Ako ste izabrali više zapisa članova projektnog tima u 1. koraku, onda je jedina dostupna opcija kreiranje novih predmeta podugovora.
5. Opcija rezervisanja iz postojećeg predmeta podugovora vam omogućava da izaberete podugovor i predmet podugovora iz kojih želite da rezervišete. Kada birate predmet podugovora da biste rezervisali kapacitet, trebalo bi da se uverite da je izabrani predmet podugovora za vreme i da se uloga potrebna članu projektnog tima podudara sa ulogom koja je kupljena u predmetu podugovora.
6. Kada izaberete da kreirate nove predmete podugovora za članove projektnog tima, sistem će vam dozvoliti da izaberete podugovor za koji želite da kreirate ove predmete. Podugovor koji izaberete za kreiranje novih predmeta trebalo bi da bude u statusu **Radna verzija**. Pomoću ove opcije za kreiranje novih predmeta podugovora za izabrane članove projektnog tima, sistem će kreirati jedan predmet podugovora za vreme za svakog člana projektnog tima. Uloga, radni sati i datumi biće kopirani iz člana projektnog tima u svaki predmet podugovora koji je kreiran. 
7. Kada je član generičkog tima povezan sa podugovorom i predmetom podugovora, polje **Vrsta radnika** u redu člana generičkog tima biće ažurirano u **Radnik po ugovoru**, a vrednost **Važenje podugovora** na vrednost **Važeće**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Podugovaranje člana projektnog tima u resursima

Kao i generički ili članovi tima bez resursa, takođe možete da prikažete opcije podugovaranja za člana tima projekta sa osobljem u resursima sve dok je član tima u resursima radnik po ugovoru. Da biste pregledali i odabrali neku od dostupnih opcija podugovaranja za popunjenog ili imenovanog člana projektnog tima bez osoblja, pratite ove korake:

1. Izaberite jedan ili više zapisa članova projektnog tima u kojima je imenovani radnih po ugovoru.
2. Uverite se da nijedan od zapisa članova projektnog tima koji je izabran nije već podugovoren. 
3. Izaberite **Opcije podugovaranja** u podmreži članova projektnog tima. Otvara se dijalog **Opcije podugovaranja**. 
4. Ako ste izabrali samo jedan zapis člana projektnog tima u 1. koraku, biće dostupne sledeće opcije:
      - Kreiranje novih predmeta podugovora.
      - Rezervisanje iz postojećeg podugovora.
  Ako ste izabrali više zapisa članova projektnog tima u 1. koraku, onda je jedina dostupna opcija kreiranje novih predmeta podugovora.
5. Opcija rezervisanja iz postojećeg predmeta podugovora vam omogućava da izaberete podugovor i predmet podugovora iz kojih želite da rezervišete. Kada birate predmet podugovora da biste rezervisali kapacitet, trebalo bi da obezbedite sledeće:
      - Izabrani predmet podugovora je za vreme. 
      - Potrebna uloga člana projektnog tima podudara se sa ulogom koja je kupljena u predmetu podugovora. 
      - Dobavljač sa kojim je radnik po ugovoru povezan je isti kao dobavljač u podugovoru.
6. Kada izaberete da kreirate nove predmete podugovora za članove projektnog tima, sistem će vam dozvoliti da izaberete podugovor za koji želite da kreirate ove predmete. Sa ovom opcijom, trebalo bi da osigurate da je dobavljač kome radnik po ugovoru pripada je isti kao dobavljač u podugovoru. 
7. Podugovor koji izaberete za kreiranje novih predmeta trebalo bi da bude u statusu **Radna verzija**. Pomoću ove opcije za kreiranje novih predmeta podugovora za izabrane članove projektnog tima, sistem će kreirati jedan predmet podugovora za vreme za svakog člana projektnog tima. Uloga, radni sati i datumi biće kopirani iz člana projektnog tima u svaki predmet podugovora koji je kreiran.  
8. Kada je imenovani član tima povezan sa podugovorom i predmetom podugovora, polje **Vrsta radnika** u redu imenovanog člana tima biće ažurirano u **Radnik po ugovoru**, a vrednost **Važenje podugovora** na vrednost **Važeće**.

## <a name="re-costing-subcontractor-assignments"></a>Ponovno određivanje troškova dodele podugovora

Kada je član projektnog tima (generički ili imenovan) povezan sa predmetima podugovora koristeći dijalog **Opcije podugovaranja**, za sve dodele zadacima koje član tima ima biće ponovo obračunate cene na osnovu nabavnog cenovnika priloženog podugovoru. Na kartici **Procene** na stranici **Detalji o projektu**, izaberite dugme **Ažuriraj cene** da biste videli ažurirano određivanje cena i/ili obračun cena koji su nastali na osnovu odluke o podugovaranju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
