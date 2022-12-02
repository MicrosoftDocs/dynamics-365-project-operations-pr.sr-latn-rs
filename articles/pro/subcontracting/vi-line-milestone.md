---
title: Stavke fakture dobavljača za kontrolne tačke
description: Ovaj članak sadrži objašnjenja o tome kako da kreirate redove na fakturi dobavljača za kontrolne tačke na podugovoru.
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

Faktura dobavljača u usluzi Microsoft Dynamics 365 Project Operations može da ima redove na fakturi dobavljača za kontrolne tačke koje su definisane predmetom podugovora. Menadžeri projekta mogu da koriste redove na fakturi dobavljača za kontrolne tačke da bi evidentirali cene usluga koje se nabavljaju kao cene zasnovane na kontrolnim tačkama koje nastaju na uslugama ili proizvodima koji se nabavljaju za projekat.

Redovi na fakturi dobavljača za kontrolne tačke uvek moraju da upućuju na predmet podugovora koji ima metod fakturisanja Fiksna cena. Kada red na fakturi dobavljača za kontrolne tačke upućuje na predmet podugovora, projektni menadžeri će moći da podudaraju i potvrđuju osnovne cene za vreme, troškove ili materijale koji upućuje na taj predmet podugovora u odnosu na kontrolnu tačku koju dobavljač fakturiše.

Sledeća tabela pruža informacije o poljima na redovima na fakturi dobavljača za kontrolne tačke.

| Polje | Opis | Funkcionalni uticaj |
| --- | --- | --- |
| Imenuj | Naziv reda na fakturi dobavljača, za pomoć pri identifikaciji. | Naziv će biti prikazan kao prva kolona u svim pretragama koje su zasnovane na stavkama na fakturi dobavljača. |
| Opis | Kratak opis usluga koje dobavljač fakturiše na redu na fakturi dobavljača. | Nijedno |
| Podugovor | Podugovor pod kojim su usluge prvobitno naručene. | Kada je za fakturu dobavljača izabran podugovor, svi redovi na fakturi dobavljača će naslediti taj izbor. Faktura dobavljača ne može imati redove na fakturi dobavljača koji upućuju na različite podugovore. |
| Predmet podugovora | Predmet podugovora pod kojim su usluge naručene. Lista predmeta podugovora koji se mogu izabrati ograničena je na predmete izabranog podugovora. | Kada je predmet podugovora izabran u redu na fakturi dobavljača za kontrolne tačke, polja **Uloga** i **Kategorija transakcije** i polja povezana sa proizvodom su nebitna i nisu dostupna. Polja **Količina**, **Jedinica** i **Grupa jedinica** takođe nisu relevantna za redove na fakturi dobavljača zasnovane na kontrolnim tačkama. |
| Datum transakcije | Datum kada će stvarna vrednost troška reda na fakturi biti evidentirana u projekat. | Nijedno |
| Klasa transakcije | Izaberite **Kontrolnu tačku** da biste evidentirali fakturu dobavljača za dovršenu kontrolnu tačku koja je definisana u predmetu podugovora. | Nijedno |
| Kontrolna tačka | Izaberite kontrolnu tačku koja je definisana u povezanom predmetu podugovora koji je označen kao **Spremno za fakturisanje**. | Kontrolne tačke predmeta podugovora koje imaju status **Spremno za fakturisanje** mogu biti izabrane na redu na fakturi dobavljača. |
| Project | Naziv projekta u kom se koriste usluge koje su fakturisane. | Ovo polje je obavezno i ne može da ostane prazno. |
| Zadatak | Naziv projektnog zadatka u kom se koriste usluge koje su fakturisane. Ovo polje je dostupno samo ako je izabran projekat. Izbor projektnog zadatka je opcionalan. | Ako ovo polje ostane prazno, menadžer projekta može da uporedi red na fakturi dobavljača sa klasom transakcija na povezanom predmetu podugovora koja je evidentirana na bilo kom zadatku na projektu. Ako red na fakturi dobavljača ne upućuje na predmet podugovora, a ovo polje ostane prazno, stvarna vrednost troška koju kreira red na fakturi dobavljača neće biti povezana ni sa jednom stvarnom vrednošću nenaplative prodaje. U ovom slučaju, ako je podešena naplata zasnovana na zadatku, troškovi možda neće moći da se fakturišu krajnjem klijentu. |
| Iznos kontrolne tačke | Unesite vrednost za kontrolnu tačku koja je definisana u predmetu podugovora koji je spreman za fakturisanje. | Nijedno |
| Porez na promet | Unesite iznos poreza na promet. | Nijedno |
| Ukupan iznos | Ukupan iznos iz reda na fakturi dobavljača, uključujući porez. Ovo polje se izračunava kao *Iznos kontrolne tačke* + *Porez na promet*. | Nijedno |

> [!NOTE]
> Kada se kreira red na fakturi dobavljača koji upućuje na kontrolnu tačku predmeta podugovora, status kontrolne tačke podugovora se ažurira na **Kreirana je faktura dobavljača**. Zatim, kada je ta faktura dobavljača potvrđena, status kontrolne tačke predmeta podugovora se ažurira na **Faktura dobavljača je potvrđena**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
