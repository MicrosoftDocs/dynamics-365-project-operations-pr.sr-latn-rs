---
title: Podešavanja mogućnosti za poslovanje – jednostavno
description: Ova tema pruža informacije o projektnim ponudama i stavkama mogućnosti za poslovanje zasnovanim na projektu.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c34817181b75b1b0079974f536e4d7b032ae87dd
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181063"
---
# <a name="opportunity-header---lite"></a>Zaglavlje mogućnosti za poslovanje – jednostavno

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Zaglavlje mogućnosti za poslovanje obuhvata sveukupne informacije o pogodbi zasnovanoj na projektu koja se odnosi na sve stavke mogućnosti za poslovanje zasnovane na projektu.

Mogućnosti za poslovanje zasnovane na projektu u usluzi Dynamics 365 Project Operations su proširenja mogućnosti za poslovanje u usluzi Dynamics 365 Sales. Ova proširenja pružaju dodatnu funkcionalnost koja je specifična i potrebna za mogućnosti za poslovanje zasnovane na projektima. Ova proširenja mogu da uključuju nova polja i radnje na traci dostupne u mogućnostima za poslovanje zasnovanim na projektima. Možda ćete pronaći neka polja, funkcionalnost i podrazumevanu logiku koja je dostupna u odeljku Prodaja, a nije dostupna u usluzi Project Operations.

Sledeća tabela uključuje polja u mogućnosti za poslovanje zasnovanoj na projektu koja su jedinstvena za Project Operations ili imaju neke važne promene u ponašanju iz mogućnosti za poslovanje u prodaji.

| **Polje** | **Lokacija** | **Opis** | **Posledični uticaj** |
| --- | --- | --- | --- |
| Tip | Kartica Opšti podaci (skrivena) | Ovo polje skupa opcija ima sledeće opcije:</br>- Zasnovano na poslu (dostupno samo u usluzi Project Operations)</br>- Zasnovano na stavci (dostupno samo kada su instalirane usluge Project Operations i Sales)</br>- Zasnovano na servisnom održavanju (dostupno kada je instalirana usluga Field Service) | Kada koristite Project Operations, ova vrednost polja se automatski postavlja na opciju **Zasnovano na poslu**, koja klasifikuje mogućnost za poslovanje kao zasnovanu na projektu. Mogućnost za poslovanje treba da se zasniva na projektu kako bi se omogućila sva proširenja i funkcije specifične za projekat u procesu prodaje za ovu pogodbu. |
| Kontakt | Kartica Opšti podaci | Upućivanje na primarni kontakt klijenta za ovu pogodbu. | |
| Nalog | Kartica Opšti podaci | Upućivanje na zapis o kompaniji klijenta ili poslovnom kontaktu. | |
| Menadžer za poslovne kontakte | Kartica Opšti podaci | Ime menadžera naloga za ovu mogućnost za poslovanje zasnovanu na projektu. | Menadžer poslovnog kontakta je odgovoran za upravljanje odnosom sa klijentom kroz završetak ovog projekta. Na osnovu zapisa resursa koji može da se rezerviše povezanog sa menadžerom naloga, ugovorna jedinica je podrazumevana. |
| Jedinica ugovaranja | Kartica Opšti podaci | Organizaciona jedinica koja je odgovorna za isporuku projekta ili projekata povezanih sa ovom pogodbom. | Ugovorna jedinica je odeljenje preduzeća koje će završiti projekte nakon zaključenja pogodbe. Svaka ugovorna jedinica ima valutu i ona se koristi za izveštavanje o procenjenim i stvarnim troškovima nastalim tokom projekta. |

Za sva ostala polja i odeljke na kartici **Rezime** mogućnosti za poslovanje, pogledajte [Kreiranje ili uređivanje mogućnosti za poslovanje (Prodaja i Čvorište za prodaju)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
