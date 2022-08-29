---
title: Stavke fakture dobavljača za kontrolne tačke
description: Ovaj članak sadrži objašnjenja o tome kako da kreirate redove fakture dobavljača za prekretnice u podizvođači.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261046"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Stavke fakture dobavljača za kontrolne tačke

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Faktura dobavljača u korporaciji Microsoft Dynamics 365 Project Operations može imati redove fakture dobavljača za prekretnice koje su definisane u redu podizvođači. Menadžeri projekta mogu da koriste redove fakture dobavljača za prekretnice da bi zapisali troškove usluga koji se nabavljaju kao troškove zasnovane na prekretnici koji nastavljaju na uslugama ili proizvodima koji se nabavljaju za projekat.

Redovi fakture dobavljača za prekretnice uvek moraju da upućuju na red podizvođače koji ima metod fakturisanja fiksne cene. Kada red fakture dobavljača za prekretnice upućuje na red podizvođače, menadžeri projekta će moći da se podudaraju i verifikuju osnovne troškove vremena, troškova ili materijala koji referencuju na red podizvođače u odnosu na prekretnicu koju fakturiše dobavljač.

Sledeća tabela pruža informacije o poljima u redovima fakture dobavljača za prekretnice.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Ime reda fakture dobavljača, da biste pomogli u identifikaciji. | Ovo ime će biti prikazano kao prva kolona u svim pronalaženjem koja se zasniva na redovima fakture dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturiše u redu fakture dobavljača. | Nijedno |
| Podugovor | Podizvođači na koji su usluge prvobitno naručene. | Kada je za fakturu dobavljača izabran podizvođaи, svi redovi u fakturi dobavljača жe naslediti taj izbor. Faktura dobavljača ne može imati redove fakture dobavljača koji upućuju na različite podizvođači. |
| Red podizvođači | Red podizvođače na kojem su usluge naručene. Lista redova podizvođaka koji se mogu izabrati ograničena je na redove izabranog podizvođaka. | Kada je red podizvođača izabran u redu fakture dobavljača za prekretnice, **polja kategorija "Uloga** **" i "Transakcija**" i polja povezana sa proizvodom su nebitna i nisu dostupna. Polja **"Količina", "** Jedinica **"** i "Grupa **jedinica" takođe** nisu relevantna za redove fakture dobavljača zasnovane na prekretnici. |
| Datum transakcije | Datum kada će trošak stvarnog reda fakture dobavljača biti zapisan u projekat. | Nijedno |
| Klasa transakcije | Izaberite **stavku** Prekretnica da biste zapisali fakturu dobavljača za dovršenu prekretnicu koja je definisana u redu podizvođač. | Nijedno |
| Kontrolna tačka | Izaberite prekretnicu koja je definisana u povezanom redu podizvođači koji je označen kao "Spremno **za fakturisanje"**. | Prekretnice u redu podizvođanja koje imaju status "Spremno **za fakturisanje** " mogu biti izabrane u redu fakture dobavljača. |
| Project | Korišćeno je ime projekta na kojem su korišćene usluge koje se fakturiše. | Ovo polje je obavezno i ne može ostati prazno. |
| Zadatak | Korišćeno je ime projektnog zadatka na kojem su korišćene usluge koje se fakturiše. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red fakture dobavljača sa klasom transakcija u povezanom redu podizvođač koji je zapisan na bilo kom zadatku projekta. Ako red fakture dobavljača ne upućuje na red podizvođača, a ovo polje ostane prazno, stvarni trošak koji je kreirao red fakture dobavljača neće biti povezan ni sa jednom neobličavanom stvarnom prodajom. U ovom slučaju, ako je naplata zasnovana na zadatku podešena, troškovi možda neće moći da se fakturišu krajnjem kupcu. |
| Iznos kontrolne tačke | Unesite vrednost prekretnice koja je definisana u redu podizvođači koji je spreman za fakturisanje. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos reda fakture dobavljača, uključujući poreze. Ovo polje se izračunava kao porez na *promet u iznosu* + *prekretnice*. | Nijedno |

> [!NOTE]
> Kada se kreira red fakture dobavljača koji upućuje na prekretnicu reda podizvođanja, status prekretnice podizvođanja se ažurira u kreiranu **fakturu dobavljača**. Zatim, kada je ta faktura dobavljača potvrđena, status prekretnice reda podizvođači se ažurira u fakturu **dobavljača potvrđen.**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
