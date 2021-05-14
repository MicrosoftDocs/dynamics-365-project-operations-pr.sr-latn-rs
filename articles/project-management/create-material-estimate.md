---
title: Finansijske procene materijala na projektima
description: Ova tema pruža informacije o definisanju ili proceni materijala zasnovanih na projektima.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788891"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finansijske procene materijala na projektima

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Dynamics 365 Project Operations omogućava menadžerima projekata da definišu cenu materijala zasnovanu na projektu za svaki projekat ili zadatak. Svaka procena materijala može da se poveže sa određenim projektnim zadatkom. Troškovi se klasifikuju u različite kategorije troškova, koje su definisane na nivou organizacije. Cena i obračun troškova za svaku kategoriju troška definišu se cenovnikom. 

Dovršite sledeće korake za prikaz, dodavanje ili brisanje procene materijala za projekat.

1. Idite na **Projekti** i izaberite projekat koji želite da ažurirate.
2. Na kartici **Procene materijala**, pogledajte listu procena materijala za projekat.
3. Izaberite **Nova procena materijala** da biste kreirali novu procenu materijala. Ili izaberite procenu materijala za brisanje, pa izaberite **Izbriši procenu materijala**.

Sledeća tabela pruža informacije o poljima **Stavka procene materijala** na projektu. 

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Zadatak | Lista zadataka u projektu. To uključuje zadatke rezimea i čvora lista. | Kada odaberete zadatak za stavku procene materijala, to utiče na procenjeni trošak materijala i procenjenu prodaju materijala za zadatak. Ako to polje ostane prazno, procena materijala se prati i rezimira samo na nivou projekta. |
| Izaberite proizvod |  Možete da navedete da li je ova stavka procene za postojeći (kataloški) proizvod ili za ručno dodat proizvod. | Ovo polje određuje da li birate proizvod iz kataloga ili želite da ga ručno dodate. |
| Proizvod | ID proizvoda iz kataloga proizvoda. Kada izaberete ID proizvoda, vrednost u polju **Izaberite proizvod** se automatski ažurira na **Postojeći proizvod**. ID se koristi za preuzimanje cene i prodajnih cena iz cenovnika. | Nema posledičnog uticaja za ovo polje. |
| Opis ručno dodatog proizvoda | Tekstualno polje za upisivanje naziva proizvoda. Ovo polje je treba da se koristi kada izaberete **Ručno dodaj** u polju **Izaberite proizvod**.| Nema posledičnog uticaja za ovo polje. |
| Datum početka | Predviđeni datum kada će se materijal koristiti. | Nema posledičnog uticaja za ovo polje. |
| Grupa jedinica | Podrazumevana vrednost u ovom polju dolazi iz podrazumevane grupe jedinica na kataloškom proizvodu. Ovo polje možete ažurirati da biste izabrali drugu grupu jedinica. | Nema posledičnog uticaja za ovo polje. |
| Jedinica | Vrednost u ovom polju dolazi iz podrazumevane jedinice izabranog proizvoda. Ovo polje možete ažurirati da biste izabrali drugu jedinicu. | Promena jedinice rezultira drugačijom podrazumevanom cenom i troškom jedinice. |
| Količina | Procenjena količina proizvoda koji će se koristiti na projektu. | Nema posledičnog uticaja za ovo polje. |
| Cena po jedinici | Jedinična cena izabranog proizvoda i kombinacija jedinica kako su postavljene u važećem cenovniku troškova. | Cena jedinice se uvek prikazuje u valuti cene projekta. Ako u cenovniku nije podešena jedinična cena za kombinaciju proizvoda i podešavanje jedinice, jedinična cena će podrazumevano iznositi 0,00. |
| Cena po jedinici | Cena izabrane kombinacije proizvoda i jedinice kao što je postavljena u važećem cenovniku prodaje. | Cena jedinice se uvek prikazuje u valuti prodaje za projekat. Ako u cenovniku nije podešena jedinična cena za kombinaciju proizvoda i podešavanje jedinice, tada će jedinična cena podrazumevano iznositi 0,00.|
| Ukupna cena | Iznos troškova koji se izračunava kao količina \* jedinični trošak.| Iznos cene se uvek prikazuje u valuti cene projekta. |
| Ukupna prodaja | Iznos prodaje koji se izračunava kao količina \* jedinična cena. | Iznos troška se uvek prikazuje u valuti prodaje za projekat. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]