---
title: Fakturisanje dobavljača – koncept i kreiranje
description: Ovaj članak opisuje koncept faktura dobavljača, scenarija za korišćenje i kako se kreiraju fakture dobavljača u korporaciji Microsoft Dynamics 365 Project Operations.
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

Fakturisanje dobavljača u korporaciji Microsoft Dynamics 365 Project Operations može se koristiti za zapisivanje troškova isporuka usluga i/ili materijala na projektu od strane dobavljača.

Kada se servisi i/ili materijali podubeđuju dobavljaču, podizvođač predstavlja ugovorni ugovor sa tim dobavljačem. Dok dobavljač isporučuje usluge ili se materijali primaju i koriste na projektnim zadacima, troškovi se beleže na projektu. Dobavljač povremeno šalje fakture koje se proveravaju i podudaraju sa troškovima koji su zapisani u projektu. Nakon završetka procesa verifikacije, faktura dobavljača se potvrđuje i oslobađa za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji za upotrebu

Fakture dobavljača u operacijama projekta mogu se koristiti za podršku dva različita scenarija.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti koriste kompletna iskustva podizvođanja

Iskustva sa fakturom dobavljača obezbeđuju način provere i podudaranja stavki vremena, korišćenja materijala i stavki troškova koje referencuju komponente podizvođačima sa redovima fakture dobavljača. Ovaj proces se može koristiti za proveru tačnosti redova fakture dobavljača. Nakon završetka procesa verifikacije i potvrde fakture dobavljača, zatvaranje će stornirati stvarne stavke koje su zapisane odobrenim evidencijama vremena, troškova i korišćenja materijala i kreirati nove stvarne troškove korišćenjem redova fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti ne koriste kompletna iskustva podizvođanja, ali žele da imaju jedinstven prikaz troškova projekata u projektne operacije

Ako pratite proces podizvođače u sistemu nezavisnog proizvođača, troškove iz tog sistema nezavisnih proizvođača možete zapisati u operacije projekta kreiranjem faktura dobavljača koje ne upućuju na podizvođače. Na taj način menadžeri projekata mogu imati jedinstven, jedinstven prikaz svih troškova na datom projektu.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u projektne operacije

Fakture dobavljača se mogu kreirati na dva načina:

- Sa stranice sa listom faktura dobavljača ili stranice sa detaljima za jednu fakturu dobavljača
- Sa stranice liste podizvođači ili stranice sa detaljima za jedan podizvođaи

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kreiranje sa stranice sa listom faktura dobavljača ili stranicom sa detaljima

1. Idite na **fakture dobavljača** \> **za nabavku**.
2. Na stranici sa listom faktura dobavljača ili stranici sa detaljima za jednu fakturu dobavljača izaberite stavku **Novo da** biste kreirali novu fakturu dobavljača.

Fakture dobavljača koje su kreirane na ovaj način takođe mogu da upućuju na podizvođaи.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kreiranje sa stranice liste podizvođaka ili stranice sa detaljima

1. Idite na **podizvođače** \> **nabavke.**
2. Izaberite jedan ili više podizvođači.
3. Na stranici liste podizvođači ili stranici sa detaljima za jedan podizvođaи izaberite stavku **Kreiraj fakturu dobavljača da** biste kreirali novu fakturu dobavljača.

Nova faktura dobavljača u **statusu** radne verzije kreira se za svaki izabrani podizvođaи.

Fakture dobavljača koje kreirate na ovaj način uvek upućuju na podizvođaи u zaglavlju fakture dobavljača. Svaki red u podizvođačem koji ima način fakturisanja vremena i materijala prouzrokovaće kreiranje reda u fakturi dobavljača. Svaki red u podizvođačem koji ima metod fakturisanja fiksne cene prouzrokovaće kreiranje reda u fakturi dobavljača za svaku prekretnicu reda podizvođače koja ima status "Spremno **za fakturisanje"**.

Sledeća polja i srodni zapisi biće kopirani iz podizvođača u zaglavlje fakture dobavljača:

- Dobavljača.
- Srodni cenovnici će biti kopirani u fakturu dobavljača kao cenovnici.
- Valuta.
- Jedinica za ugovaranje.
- Uslovi plaćanja.

Za redove podizvođača vremena i materijala, sledeća polja i srodni zapisi biće kopirani iz reda podizvođača u red fakture dobavljača:

- Reference reda podizvođaka i podizvođači
- Klasa transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak
- Resurs koji može da se rezerviše

Za redove podizvođača fiksne cene, sledeća polja će biti kopirana iz reda podizvođača i prekretnice reda podizvođača u red fakture dobavljača:

- Reference reda podizvođaka i podizvođači.
- Klasa transakcije. Podrazumevano, vrednost će biti **Prekretnica**.
- Prekretničko ime i iznos biće kopirani sa povezane prekretnice podizvođačka reda.
- Korisnik će moći da izabere projekat i zadatak u redu fakture dobavljača.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
