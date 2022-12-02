---
title: Fakturisanje dobavljača – koncept i kreiranje
description: Ovaj članak opisuje koncept faktura prodavca, scenarije korišćenja i kako da kreirate fakture dobavljača u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261961"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Fakturisanje dobavljača – koncept i kreiranje

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Fakturisanje prodavaca u usluzi Microsoft Dynamics 365 Project Operations može se koristiti za evidentiranje cena za isporuke usluga i/ili materijala na projektu od strane dobavljača.

Kada se usluge i/ili materijali podugovaraju sa prodavcem, podugovor predstavlja ugovorni sporazum sa tim prodavcem. Kako prodavac isporučuje usluge ili kako se materijali primaju i koriste na projektnim zadacima, cene se beleže na projektu. Periodično, prodavac šalje fakture koje se proveravaju i podudaraju sa cenama koje su zabeležene na projektu. Nakon završetka procesa verifikacije, faktura prodavca se potvrđuje i pušta za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji upotrebe

Fakture prodavaca u rešenju Project Operations mogu se koristiti za podršku dva različita scenarija.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti koriste puna iskustva podugovaranja

Iskustva sa fakturom dobavljača obezbeđuju način provere i podudaranja stavki vremena, korišćenja materijala i stavki troškova koje su reference za komponente podugovora sa redovima na fakturi dobavljača. Ovaj proces se može koristiti za proveru tačnosti redova na fakture dobavljača. Nakon dovršavanja procesa verifikacije i potvrde fakture dobavljača, aplikacija će stornirati stvarne vrednosti koje su evidentirane odobrenim evidencijama vremena, troškova i korišćenja materijala, a zatim kreirati nove stvarne vrednosti za cenu korišćenjem redova na fakturi dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti ne koriste potpuna iskustva podugovaranja, ali žele da imaju jedinstven prikaz cena na projektima u rešenju Project Operations

Ako pratite proces podugovora u sistemu nezavisnog proizvođača, cene iz sistema tog nezavisnog proizvođača možete evidentirati u rešenju Project Operations kreiranjem faktura dobavljača koje ne upućuju na podugovore. Na taj način menadžeri projekata mogu da imaju jedinstven, objedinjen prikaz svih cena na datom projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u rešenju Project Operations

Fakture dobavljača mogu da se kreiraju na dva načina:

- Sa stranice sa listom faktura dobavljača ili stranice sa detaljima za jednu fakturu dobavljača
- Sa stranice liste podugovora ili stranice sa detaljima za jedan podugovor

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kreiranje sa stranice sa listom faktura dobavljača ili stranice sa detaljima

1. Idite na **Nabavka** \> **Fakture dobavljača**.
2. Na stranici sa listom faktura dobavljača ili stranici sa detaljima za jednu fakturu dobavljača izaberite stavku **Novo** da biste kreirali novu fakturu dobavljača.

Fakture dobavljača koje su kreirane na ovaj način takođe mogu da upućuju na podugovor.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kreiranje sa stranice sa listom podugovora ili stranice sa detaljima

1. Idite na **Nabavka** \> **Podugovori**.
2. Izaberite najmanje jedan podugovor.
3. Na stranici sa listom podugovora ili stranici sa detaljima za jedan podugovor, izaberite stavku **Kreiraj fakturu dobavljača** da biste kreirali novu fakturu dobavljača.

Nova faktura dobavljača u statusu **Radna verzija** kreira se za svaki izabrani podugovor.

Fakture dobavljača koje kreirate na ovaj način uvek upućuju na podugovor u zaglavlju fakture dobavljača. Svaki predmet podugovora koji ima način obračuna Vreme i materijal prouzrokovaće kreiranje reda a fakturi dobavljača. Svaki predmet podugovora koji ima način obračuna Fiksna cena prouzrokovaće kreiranje reda na fakturi dobavljača za svaku kontrolnu tačku predmeta podugovora koja ima status **Spremno za fakturisanje**.

Sledeća polja i povezani zapisi biće kopirani iz podugovora u zaglavlje fakture dobavljača:

- Dobavljač.
- Srodni cenovnici će biti kopirani u fakturu dobavljača kao cenovnici.
- Valuta.
- Jedinica ugovaranja.
- Uslovi plaćanja.

Za predmete podugovora Vreme i materijal, sledeća polja i srodni zapisi biće kopirani iz predmeta podugovora u red fakture dobavljača:

- Podugovor i reference predmeta podugovora
- Klasa transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak
- Resurs koji može da se rezerviše

Za predmete podugovora Fiksna cena, sledeća polja biće kopirana iz predmeta podugovora i kontrolne tačke predmeta podugovora u red fakture dobavljača:

- Podugovor i reference predmeta podugovora.
- Klasa transakcije. Podrazumevano, vrednost će biti **Kontrolna tačka**.
- Naziv i iznos kontrolne tačke biće kopirani sa povezanom kontrolnom tačkom predmeta podugovora.
- Korisnik će moći da izabere projekat i zadatak u redu na fakturi dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
