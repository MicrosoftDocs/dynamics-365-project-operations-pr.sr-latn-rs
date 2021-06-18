---
title: Podešavanja mogućnosti za poslovanje – jednostavno
description: Ova tema pruža informacije o projektnim ponudama i stavkama mogućnosti za poslovanje zasnovanim na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4539a34cface9999c9cd029f8d44f835a8fe27ca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994693"
---
# <a name="header-details-for-project-opportunities"></a>Detalji zaglavlja za mogućnosti za poslovanje za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Zaglavlje mogućnosti za poslovanje obuhvata sveukupne informacije o pogodbi zasnovanoj na projektu koja se odnosi na sve stavke mogućnosti za poslovanje zasnovane na projektu.

Mogućnosti zasnovane na projektima u usluzi Dynamics 365 Project Operations predstavljaju proširenja mogućnosti u usluzi Dynamics 365 Sales. Ova proširenja pružaju dodatnu funkcionalnost koja je specifična i potrebna za mogućnosti za poslovanje zasnovane na projektima. Ova proširenja mogu da uključuju nova polja i radnje na traci dostupne u mogućnostima za poslovanje zasnovanim na projektima. Možda ćete pronaći neka polja, funkcionalnost i podrazumevanu logiku koja je dostupna u odeljku Prodaja, a nije dostupna u usluzi Project Operations.

Sledeća tabela uključuje polja u mogućnosti za poslovanje zasnovanoj na projektu koja su jedinstvena za Project Operations ili imaju neke važne promene u ponašanju iz mogućnosti za poslovanje u prodaji.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip | Kartica Opšti podaci (skrivena) | Ovo polje skupa opcija ima sledeće opcije:</br>- Zasnovano na poslu (dostupno samo u usluzi Project Operations)</br>- Zasnovano na stavci (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- Zasnovano na servisnom održavanju (dostupno kada je instalirana usluga Field Service) | Kada koristite Project Operations, ova vrednost polja se automatski postavlja na opciju **Zasnovano na poslu**, koja klasifikuje mogućnost za poslovanje kao zasnovanu na projektu. Mogućnost za poslovanje treba da se zasniva na projektu kako bi se omogućila sva proširenja i funkcije specifične za projekat u procesu prodaje za ovu pogodbu. |
| Kontakt | Kartica Opšti podaci | Upućivanje na primarni kontakt klijenta za ovu pogodbu. | |
| Nalog | Kartica Opšti podaci | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. | |
| Menadžer za poslovne kontakte | Kartica Opšti podaci | Ime menadžera naloga za ovu mogućnost za poslovanje zasnovanu na projektu. | Menadžer poslovnog kontakta je odgovoran za upravljanje odnosom sa klijentom kroz završetak ovog projekta. Na osnovu zapisa resursa koji može da se rezerviše povezanog sa menadžerom naloga, ugovorna jedinica je podrazumevana. |
| Jedinica ugovaranja | Kartica Opšti podaci | Organizaciona jedinica koja je odgovorna za isporuku projekta ili projekata povezanih sa ovom pogodbom. | Ugovorna jedinica je odeljenje preduzeća koje će završiti projekte nakon zaključenja pogodbe. Svaka ugovorna jedinica ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |

Za sva ostala polja i odeljke na kartici **Rezime** mogućnosti za poslovanje, pogledajte [Kreiranje ili uređivanje mogućnosti za poslovanje (Prodaja i Čvorište za prodaju)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
