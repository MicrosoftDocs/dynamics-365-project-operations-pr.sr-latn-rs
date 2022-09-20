---
title: Kreiranje faktura dobavljača
description: Ovaj članak opisuje koncept faktura dobavljača i objašnjava kako da ih kreirate u korporaciji Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Kreiranje faktura dobavljača

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da biste koristili funkcionalnost opisanu u ovom članku, **morate omogućiti da se omogući obrada stvarnih podataka podizvođača pomoću operacija projekta za scenarije zasnovane na resursima** u **radnom prostoru za** upravljanje funkcijama.

Fakturisanje dobavljača u korporaciji Microsoft Dynamics 365 Project Operations može se koristiti za zapisivanje troškova isporuka usluga i/ili materijala na projektu koji su dovršili dobavljači.

Kada se servisi i/ili materijali podubeđuju dobavljaču, podizvođač predstavlja ugovorni ugovor sa tim dobavljačem. Kako dobavljač isporučuje usluge ili kako se materijali primaju i koriste na projektnim zadacima, troškovi se beleže na projektu. Dobavljač zatim periodično šalje fakture. Te fakture se proveravaju i podudaraju sa troškovima koji su zabeleženi na projektu. Nakon završetka procesa verifikacije, faktura dobavljača se potvrđuje i oslobađa za plaćanje.

## <a name="scenarios-for-use"></a>Scenariji za upotrebu

Fakture dobavljača u operacijama projekta mogu se koristiti za podršku dva različita scenarija:

- Klijenti koriste puna iskustva podizvođanja.
- Klijenti ne koriste kompletna iskustva podizvođanja, ali žele da imaju jedinstven prikaz troškova za projekte u operacijama projekta.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klijenti koriste kompletna iskustva podizvođanja

Iskustva sa fakturom dobavljača obezbeđuju način provere vremenskih stavki, korišćenja materijala i stavki troškova koje referencuju komponente podizvođačima i uporećuju ih sa redovima fakture dobavljača. Ovaj proces se može koristiti za proveru tačnosti redova fakture dobavljača. Nakon dovršavanja procesa verifikacije i potvrde fakture dobavljača, sistem stornira stvarne stavke koje su zapisane odobrenim evidencijama vremena, troškova i korišćenja materijala, a zatim kreira nove stvarne troškove korišćenjem redova fakture dobavljača.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klijenti ne koriste kompletna iskustva podizvođanja, ali žele da imaju jedinstven prikaz troškova projekata u projektne operacije

Ako pratite proces podizvođače u sistemu nezavisnog proizvođača, troškove iz tog sistema nezavisnih proizvođača možete zapisati u operacije projekta kreiranjem faktura dobavljača koje ne upućuju na podizvođače. Na taj način menadžeri projekata mogu da imaju jedinstven, objedinjen prikaz svih troškova na datom projektu.

## <a name="create-vendor-invoices-in-project-operations"></a>Kreiranje faktura dobavljača u projektne operacije

Fakture dobavljača se kreiraju u Dynamics 365 Finance, pomoću modula **"Konta za plaćanje**". Fakture dobavljača ne možete kreirati direktno u Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Podešavanje provere fakture dobavljača

Ako je faktura dobavljača namenjena podizvođačima Dataverse u programu, **potreban je parametar Ručna verifikacija od strane premijera**. Postavka opcije određuje da li faktura dobavljača treba automatski da bude potvrđena ili Dataverse zahteva ručnu potvrdu. Zaglavlje svake fakture dobavljača projekta uključuje opciju istog imena. Podrazumevano, opcija u zaglavlju svih faktura dobavljača projekta postavljena je na vrednost koju ste ovde postavili. Međutim, vrednost možete ažurirati po potrebi u zaglavlju pojedinačnih faktura dobavljača.

Ako je opcija postavljena na "Da", **faktura** dobavljača koja je kreirana u "Finansije" i sinhronizovana sa statusom Dataverse "Radna verzija" ima **status "Radna** verzija". Faktura zatim mora biti proverena i verifikovana od strane menadžera projekta i potvrđena, pre nego što se obradi i proknjiži na određena konta projekta i knjige u finansijama.

Ako je opcija podešena na "Ne **·**", faktura dobavljača se automatski potvrđuje. Nije potrebna dalja akcija.

Da biste podesili proveru fakture dobavljača, sledite ove korake.

1. U oblasti Finansije idite na Upravljanje projektima **i računovodstveno podešavanje** \> **projekta** \> **upravljanja i računovodstvenih parametara.**
1. Na kartici **"** Finansije" postavite **opciju "Ručno verifikacija od strane premijera** **·**" ako smernice preduzeća zahtevaju verifikaciju faktura dobavljača podizvođača. Ako verifikacija od strane menadžera projekta nije obavezna, ostavite Dataverse poruku skup opcija na "Ne **"**. Postavka će podrazumevano biti korišćena na stranici fakture dobavljača **na čekanju**.

> [!NOTE]
> Fakture dobavljača koje su kreirane za podizvođača Dataverse mogu se ispravno obraditi samo ako **je opcija "Ručno verifikacija od strane premijera** " podešena na "Da **"**. Stvarne vremenske, materijalne i troškovne troškove koje kreiraju podizvođači mogu se ručno podudarati sa redovima fakture dobavljača od strane menadžera projekta samo ako je ova opcija podešena na "Da **"**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Podešavanje konta integracije nabavke za fakture dobavljača

Kada se faktura dobavljača proknjiži u "Finansije za projektne operacije " – Integrisano okruženje (nenapušteno), finansije se knjiže na konto integracije sa nabavkama. Sistem generiše stvarne stvari za proknjiženu Dataverse fakturu. Ove stvarne stvari se knjiže u "Finansije" korišćenjem naloga za integraciju projekata. Knjiženje naloga integracije projekta knjiži stvarni trošak i storni konto integracije sa nabavkama.

Da biste podesili konto integracije nabavke za fakture dobavljača, sledite ove korake.

1. U oblasti Finansije idite na Upravljanje projektima **i računovodstveno podešavanje** \> **projekta** \> **upravljanja i računovodstvenih parametara.**
1. Na kartici **Projektne operacije na Dynamics 365 kartici angažovanje kupaca** izaberite konto **integracije** \> **nabavki materijala.**

### <a name="create-and-post-subcontract-vendor-invoices"></a>Kreiranje i knjiženje faktura dobavljača podizvođači

Kada službenik koji plaća račune primi fakturu od podizvođača, nova faktura se kreira u oblasti "Finansije".

1. U oblasti "Finansije" idite na fakture **za isplate** \> **na čekanju.** \> **·**
1. U oknu **za radnje** izaberite stavku Novo **da** biste kreirali fakturu dobavljača.
1. U zaglavlju fakture, u polju Konto **fakture** izaberite stavku **Podizvođač**.
1. Izaberite datum fakture.
1. Na kartici **"** Zaglavlje" postavite opciju **"Ručno verifikacija od strane** premijera" na opciju "Da **"**. Podrazumevana postavka ove opcije potiče sa stranice "Upravljanje **projektima i računovodstvenim parametrima** ". Međutim, ona se može promeniti na nivou fakture dobavljača.
1. Na brzoj **kartici Red** fakture izaberite stavku Dodaj **red da biste** kreirali red fakture dobavljača.
1. Izaberite kategoriju nabavke koja je kreirana za redove podizvođači i unesite jediničnu cenu, jedinicu mere i količinu.
1. U odeljku Redovi fakture dobavljača, na **kartici** Projekat izaberite projekat u koji podizvođač deli fakturu podizvođača.
1. Izaberite kategoriju projekta. Može biti bilo koje vrste stavke "Artikal **", "** Troškovi **", "** Materijali **"** ili "Časovi **"**.
1. Izaberite ulogu samo ako je izabrana kategorija projekta tipa "Sat **·**".
1. Kliknite na **dugme Proknjiži** da biste proknjižili fakturu dobavljača.

Druga mogućnost je da kreirate fakturu dobavljača tako što ćete ići na fakture **za plaćanje** \> **·** \> **Otvoriti fakture dobavljača** i izabrati stavku **Novo.**

Kada se faktura dobavljača proknjiži, ona postaje dostupna za Dataverse proveru i obradu menadžera projekta.

## <a name="vendor-invoice-processing-in-dataverse"></a>Obrada fakture dobavljača u Dataverse

U fakturi dobavljača koja je kreirana u Dataverse programu, neke vrednosti polja potiиu iz fakture dobavljača koja je zapisana u "Finansije". Druge vrednosti su podrazumevane vrednosti koje potiиu iz podizvoрaиa.

Sledeća polja i srodni zapisi biće kopirani iz podizvođača u zaglavlje fakture dobavljača:

- Valuta
- Jedinica ugovaranja
- Uslovi plaćanja

U redovima fakture dobavljača, operacije projekta koriste sledeće vrednosti polja da bi uneli podrazumevanu referencu reda podizvođači i podizvođači:

- Klasa transakcije
- Uloga
- Kategorija transakcije
- Polja proizvoda
- Project
- Zadatak

> [!NOTE]
> Redovi podizvođanja fiksne cene nisu podržani u operacijama projekta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
