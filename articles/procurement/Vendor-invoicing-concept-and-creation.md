---
title: Kreiranje faktura prodavca
description: Ovaj članak opisuje koncept faktura dobavljača i objašnjava kako da ih kreirate u usluzi Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475482"
---
# <a name="create-vendor-invoices"></a>Kreiranje faktura prodavca

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da biste koristili funkcionalnost opisanu u ovom članku, morate omogućiti funkciju **Omogući obradu stvarnih vrednosti podugovora pomoću rešenja Project Operations scenarije zasnovane na resursima** u radnom prostoru **Upravljanje funkcijama**.

Fakturisanje dobavljača u usluzi Microsoft Dynamics 365 Project Operations može se koristiti za evidentiranje cena za isporuke usluga i/ili materijala na projektu koji su dovršili dobavljači.

Kada se usluge i/ili materijali podugovaraju sa prodavcem, podugovor predstavlja ugovorni sporazum sa tim prodavcem. Kako dobavljač isporučuje usluge ili kako se materijali primaju i koriste na projektnim zadacima, cene se beleže na projektu. Dobavljač zatim periodično šalje fakture. Te fakture se proveravaju i podudaraju sa cenama koje su zabeležene na projektu. Nakon završetka procesa verifikacije, faktura prodavca se potvrđuje i pušta za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji upotrebe

Fakture dobavljača u rešenju Project Operations mogu se koristiti za podršku dva različita scenarija:

- Klijenti koriste puna iskustva podugovaranja.
- Klijenti ne koriste potpuna iskustva podugovaranja, ali žele da imaju jedinstven prikaz cena na projektima u rešenju Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti koriste puna iskustva podugovaranja

Iskustva sa fakturom dobavljača obezbeđuju način provere unosa vremena, korišćenja materijala i stavki troškova koje su reference za komponente podugovora i podudaraju ih sa redovima na fakturi dobavljača. Ovaj proces se može koristiti za proveru tačnosti redova na fakture dobavljača. Nakon dovršavanja procesa verifikacije i potvrde fakture dobavljača, sistem stornira stvarne vrednosti koje su evidentirane odobrenim evidencijama vremena, troškova i korišćenja materijala, a zatim kreira nove stvarne vrednosti za cenu korišćenjem redova na fakturi dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti ne koriste potpuna iskustva podugovaranja, ali žele da imaju jedinstven prikaz cena na projektima u rešenju Project Operations

Ako pratite proces podugovora u sistemu nezavisnog proizvođača, cene iz sistema tog nezavisnog proizvođača možete evidentirati u rešenju Project Operations kreiranjem faktura dobavljača koje ne upućuju na podugovore. Na taj način menadžeri projekata mogu da imaju jedinstven, objedinjen prikaz svih cena na datom projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u rešenju Project Operations

Fakture dobavljača se kreiraju u sistemu Dynamics 365 Finance korišćenjem modula **Dugovanja**. Fakture dobavljača ne možete kreirati direktno u usluzi Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Podešavanje provere fakture dobavljača

Ako je faktura dobavljača namenjena za podugovor u usluzi Dataverse, morate da omogućite parametar **Ručna verifikacija od strane PM-a**. Postavka opcije određuje da li faktura dobavljača treba automatski da bude potvrđena u usluzi Dataverse ili zahteva ručnu potvrdu. Zaglavlje svake fakture dobavljača na projektu uključuje opciju istog imena. Podrazumevano, opcija u zaglavlju svih faktura dobavljača na projektu postavljena je na vrednost koju ste ovde postavili. Međutim, vrednost možete ažurirati po potrebi u zaglavlju pojedinačnih faktura dobavljača.

Ako je opcija postavljena na **Da**, faktura dobavljača koja je kreirana u Finansijama i sinhronizovana sa uslugom Dataverse ima status **Radna verzija**. Faktura zatim mora biti proverena i verifikovana od strane projektnog menadžera, kao i potvrđena, pre nego što se obradi i proknjiži na određena konta projekta i glavne knjige u Finansijama.

Ako je opcija podešena na **Ne**, faktura dobavljača se automatski potvrđuje. Nije potrebna dodatna radnja.

Da biste podesili verifikaciju fakture dobavljača, pratite ove korake.

1. U Finansijama, idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.
1. Na kartici **Finansije** postavite opciju **Ručno verifikacija od strane PM-a** na **Da** ako smernice preduzeća zahtevaju verifikaciju faktura dobavljača podizvođača. Ako verifikacija od strane projektnog menadžera nije obavezna u usluzi Dataverse, ostavite skup opcija na **Ne**. Postavka će podrazumevano biti korišćena na stranici **Fakture dobavljača na čekanju**.

> [!NOTE]
> Fakture dobavljača koje su kreirane za podizvođače u usluzi Dataverse mogu se ispravno obraditi samo ako je opcija **Ručno verifikacija od strane PM-a** podešena na **Da**. Stvarne vrednosti za cene za vreme, materijal i troškove koje kreiraju podizvođači mogu se ručno podudarati sa redovima na fakturi dobavljača od strane projektnog menadžera samo ako je ova opcija podešena na **Da**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Podesite nalog za integraciju nabavki za fakture dobavljača

Kada se faktura dobavljača proknjiži u rešenju Finance for Project Operations – Integrisano okruženje (koji nisu na zalihama), finansije se knjiže na konto integracije sa nabavkama. Sistem generiše stvarne vrednosti u usluzi Dataverse za proknjiženu fakturu. Ove stvarne vrednosti se knjiže u Finansijama korišćenjem dnevnika za integraciju projekata. Knjiženjem u dnevnika integracije projekta knjiži se stvarna vrednost cene i stronira konto integracije nabavki.

Da biste podesili konto za integraciju nabavki za fakture dobavljača, pratite ove korake.

1. U Finansijama, idite na **Upravljanje projektima i računovodstvo** \> **Podešavanje** \> **Upravljanje projektom i računovodstveni parametri**.
1. Na kartici **Project Operations u usluzi Dynamics 365 Customer Engagement**, izaberite **Materijali** \> **Konto integracije nabavki**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Kreiranje i knjiženje faktura klijenta podugovora

Kada službenik za dugovanja primi fakturu od podizvođača, nova faktura se kreira u oblasti Finansijama.

1. U Finansijama idite na **Dugovanja** \> **Fakture** \> **Fakture dobavljača na čekanju**.
1. U **Oknu Radnje** izaberite **Novo** da biste kreirali fakturu dobavljača.
1. U zaglavlju fakture, u polju **Konto fakture** izaberite stavku **Podizvođač**.
1. Izaberite datum fakture.
1. Na kartici **Zaglavlje** postavite opciju **Ručna verifikacija od strane PM-a je potrebna** na **Da**. Podrazumevana postavka ove opcije potiče sa stranice **Upravljanje projektima i računovodstveni parametri**. Međutim, ona se može promeniti na nivou fakture dobavljača.
1. Na brzoj kartici **Stavka fakture** izaberite **Dodaj red** da biste kreirali red na fakturi dobavljača.
1. Izaberite kategoriju nabavke koja je kreirana za predmete podugovora i unesite jediničnu cenu, jedinicu mere i količinu.
1. U odeljku Predmeti fakture dobavljača, na kartici **Projekat** izaberite projekat za koji podizvođač deli fakturu podizvođača.
1. Izaberite kategoriju projekta. Može biti bilo koji tip: **Stavka**, **Trošak**, **Materijali** ili **Sati**.
1. Izaberite ulogu samo ako je izabrana kategorija projekta tipa **Sat**.
1. Kliknite na **Proknjiži** da biste proknjižili fakturu dobavljača.

Druga mogućnost je da kreirate fakturu dobavljača tako što ćete ići na **Dugovanja** \> **Fakture** \> **Otvorene fakture dobavljača** i izabrati **Novo**.

Kada se faktura dobavljača proknjiži, ona postaje dostupna u usluzi Dataverse za proveru i obradu od strane projektnog menadžera.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obrada fakture dobavljača u usluzi Dataverse

U fakturi dobavljača koja je kreirana u usluzi Dataverse, neke vrednosti polja potiču iz fakture dobavljača koja je evidentirana u Finansijama. Druge vrednosti su podrazumevane vrednosti koje potiču iz podugovora.

Sledeća polja i povezani zapisi biće kopirani iz podugovora u zaglavlje fakture dobavljača:

- Valuta
- Jedinica ugovaranja
- Uslovi plaćanja

U stavkama na fakturi dobavljača, Project Operations koristi sledeće vrednosti polja za unos podrazumevani podugovor i referencu na predmet podugovora:

- Klasa transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak

> [!NOTE]
> Predmeti podugovora sa fiksnom cenom nisu podržani u Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
