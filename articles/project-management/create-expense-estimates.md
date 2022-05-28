---
title: Finansijske procene troškova na projektima
description: Ova tema pruža informacije o definisanju ili proceni troškova zasnovanih na projektu.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c14dc31d666d0e0d026cf9cddfa1e78dee40f717
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589490"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Finansijske procene troškova na projektima
_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations omogućava menadžerima projekata da definišu troškove zasnovane na projektu za svaki projekat ili zadatak. Svaka stavka troška može biti povezana sa određenim projektnim zadatkom. Troškovi se klasifikuju u različite kategorije troškova, koje su definisane na nivou organizacije. Cena i obračun troškova za svaku kategoriju troška definišu se cenovnikom. 

Dovršite sledeće korake za prikaz, dodavanje ili brisanje troškova projekta.

1. Idite na **Projekti**, i izaberite projekat na kojem želite da radite.
2. Izaberite karticu **Projektne procene** i pogledajte listu troškova projekta.
3. Izaberite **Novi trošak** da biste dodali trošak. Ili izaberite trošak koji želite da izbrišete, a zatim izaberite **Izbriši trošak**.

Sledeća tabela pruža informacije o poljima **stavke procene troška** na projektu. 

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Zadatak | Lista zadataka u projektu. To uključuje zadatke rezimea i čvora lista. | Izbor zadatka za stavku procene troškova uticaće na procenjenu cenu troškova i procenjeni iznos troškova prodaje za zadatak. Ako to polje ostane prazno, procena troškova se prati i rezimira samo na nivou projekta. |
| Kategorija | Lista kategorija transakcija koje imaju povezane kategorije troškova u aplikaciji. | Izbor kategorije pokreće određivanje cena i troškova na stavci procene troškova. |
| Datum početka | Predviđeni datum kad trošak treba da nastane. | Nema posledičnog uticaja za ovo polje. |
| Grupa jedinica | Podrazumevana vrednost u ovom polju dolazi iz grupe jedinica koja je postavljena kao podrazumevana za izabranu kategoriju. Ovo polje možete ažurirati da biste izabrali drugu grupu jedinica. | Nema posledičnog uticaja za ovo polje. |
| Jedinica | Podrazumevana vrednost u ovom polju je podrazumevana jedinica izabrane kategorije. Ovo polje možete ažurirati da biste izabrali drugu jedinicu. | Promena jedinice rezultira drugačijom podrazumevanom cenom i troškom jedinice. |
| Količina | Količina procenjenog troška koje ćete imati. | Nema posledičnog uticaja za ovo polje. |
| Cena po jedinici | Cena izabrane kategorije i kombinacije jedinica kako su postavljene u važećem cenovniku troškova | Cena jedinice se uvek prikazuje u valuti cene projekta. |
| Cena po jedinici | Cena izabrane kategorije i kombinacije jedinica kako su postavljene u važećem cenovniku prodaje. | Cena jedinice se uvek prikazuje u valuti prodaje za projekat. |
| Ukupna cena | Iznos troškova koji se izračunava kao količina \* jedinični trošak.| Iznos cene se uvek prikazuje u valuti cene projekta. |
| Ukupna prodaja | Iznos prodaje koji se izračunava kao količina \* jedinična cena. | Iznos troška se uvek prikazuje u valuti prodaje za projekat. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
