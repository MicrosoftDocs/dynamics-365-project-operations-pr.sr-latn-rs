---
title: Nadogradnja sa aplikacije Project Service Automation na uslugu Project Operations
description: Ovaj članak pruža pregled procesa sa kojeg se može nadograditi Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 2d7b372cac391fab7a81ac6ac5d2ea6d12977b5c
ms.sourcegitcommit: 9de444ae0460c8d15c77d225d0c0ad7f8445d5fc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9686993"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja sa aplikacije Project Service Automation na uslugu Project Operations

Uzbuđeni smo što ćemo objaviti drugu od tri faze za nadogradnju sa korporacije Microsoft Dynamics 365 Project Service Automation Microsoft Dynamics 365 Project Operations. Ovaj članak pruža pregled za kupce koji kreću na ovo uzbudljivo putovanje. 

Program za isporuku nadogradnje biće podeljen u tri faze.

| Nadogradnja isporuke | Faza 1 (januar 2022) | Faza 2 (novembar 2022) | Faza 3 (aprilski talas 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema zavisnosti od strukture kvara na radu (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS u okviru trenutno podržanih granica projektnih operacija | | :heavy_check_mark: | :heavy_check_mark: |
| WBS izvan trenutno podržanih ograničenja projektnih operacija, uključujući podršku za klijenta radne površine projekta | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije procesa nadogradnje 

U sklopu procesa nadogradnje dodali smo evidencije nadogradnje na mapu lokacije kako bismo omogućili administratorima da lakše dijagnostikuju neuspehe. Pored novog interfejsa, biće dodata i nova pravila za proveru valjanosti kako bi se osigurao integritet podataka nakon nadogradnje. Sledeće provere valjanosti biće dodate procesu nadogradnje.

| Provere valjanosti | Faza 1 (januar 2022) | Faza 2 (novembar 2022) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| WBS će biti proveren u odnosu na uobičajena kršenja integriteta podataka (na primer, dodele resursa koje su povezane sa istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti proveren u odnosu na [poznata ograničenja projekta za Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti proveren u odnosu na poznata ograničenja klijenta radne površine projekta. | |  | :heavy_check_mark: |
| Knjigovodstveni resursi i kalendari projekta biće procenjeni u odnosu na uobičajene izuzetke pravila kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2, klijenti koji nadograde na projektne operacije imaće svoje postojeće projekte nadograđene na iskustvo samo za čitanje za planiranje projekta. U ovom iskustvu koje je samo za čitanje, ceo WBS će biti vidljiv u mreži za praćenje. Da bi uredili WBS, menadžeri projekta mogu da izaberu [**opciju**](/PSA-Upgrade-Project-Conversion.md) Konvertuj na glavnoj stranici projekta. Proces u pozadini zatim ažurira projekat tako da podržava novo iskustvo zakazivanja projekta iz projekta za Web. Ova faza je prikladna za klijente koji imaju projekte koji se uklapaju u [poznate granice projekta za Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U fazi 3, biće dodata podrška za Project desktop klijenta, u korist klijenata koji žele da nastave da uređuju svoje projekte iz te aplikacije. Međutim, ako postojeći projekti budu konvertovani u novi Projekat za Web iskustvo, pristup programskog dodatku biće onemogućen za svaki konvertovani projekat.

## <a name="prerequisites"></a>Preduslovi

Da biste ispunili uslove za nadogradnju faze 1, morate da ispunite sledeće kriterijume:

- Ciljno okruženje ne sme da sadrži zapise u **msdyn_projecttask** entitetu.
- Važeće licence za projektne operacije moraju biti dodeljene svim aktivnim korisnicima. 
- Proces nadogradnje morate da proverite u najmanje jednom okruženju koje nije proizvodno, a koje sadrži reprezentativni skup podataka koji je usklađen sa proizvodnim okruženjem.
- Ciljno okruženje mora biti ažurirano na verziju za automatizaciju usluge projekta Release 37 (V3.10.58.120) ili noviju verziju.

Da biste stekli pravo na nadogradnju u fazi 2, morate da ispunite sledeće kriterijume:

- Važeće licence za projektne operacije moraju biti dodeljene svim aktivnim korisnicima. 
- Proces nadogradnje morate da proverite u najmanje jednom okruženju koje nije proizvodno, a koje sadrži reprezentativni skup podataka koji je usklađen sa proizvodnim okruženjem.
- Ciljno okruženje mora biti ažurirano na verziju za automatizaciju usluge projekta Release 37 (V3.10.58.120) ili noviju verziju.
- Okruženja koja sadrže zadatke (msdyn_projecttask) podržana su samo ako je ukupan broj zadataka po projektu 500 ili manji.

Preduslovi za fazu 3 će biti ažurirani sa približavanjem datuma opšte dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za automatizaciju projektnih usluga, možete instalirati i koristiti projektne operacije, što uključuje sve mogućnosti automatizacije projektnih usluga i još mnogo toga. Zatim možete da testirate mogućnosti projektnih operacija u posebnom okruženju dok nastavljate da koristite automatizaciju projektnih usluga u proizvodnji. Kada licence za automatizaciju usluge projekta isteknu, moraćete da pređete na operacije projekta. Kada planirate ovaj prelaz, morate da računate na činjenicu da licenca za operacije projekta ne uključuje licencu za automatizaciju usluge projekta.

## <a name="testing-and-refactoring-customizations"></a>Prilagođavanja testiranja i reaktorata

Kao polaznu tačku, uvezite sva prilagođavanja u čisto okruženje projektnih operacija (Lite) da biste potvrdili da je uvoz uspešan i da se poslovno poslovanje ponaša kao što se očekivalo.

Evo nekih stvari na koje treba da se pazite:

- Uvoz možda neće uspeti zbog zavisnosti koje nedostaju. Drugim rečima, referentna polja prilagođavanja ili druge komponente koje su uklonjene u operacijama projekta. U ovom slučaju, uklonite ove zavisnosti iz razvojnog okruženja.
- Ako nekontrolisana i upravljana rešenja uključuju komponente koje nisu prilagođene, uklonite te komponente iz rešenja. Na primer, kada prilagodite entitet **projekta**, dodajte samo zaglavlje entiteta u rešenje. Nemojte dodavati sva polja. Ako ste prethodno dodali sve podkomponente, možda ćete morati ručno da kreirate novo rešenje i dodate mu relevantne komponente.
- Obrasci i prikazi se možda neće pojaviti na očekivani način. U nekim okolnostima, ako ste prilagodili neki od obrazaca ili prikaza koji nisu u okviru, prilagođavanja mogu da spreče stupanje na snagu novih ispravki u operacijama projekta. Da biste identifikovali ove probleme, preporučujemo da uradite pregled čiste instalacije projektnih operacija i instalacije operacija projekta koja uključuje prilagođavanja. Uporedite najčešće korišćene obrasce u poslovanju da biste potvrdili da vaša verzija obrasca i dalje ima smisla i da vam ne nedostaje nešto iz čiste verzije obrasca. Uradite isti tip bočne redigorije za sve prikaze koje ste prilagodili.
- Poslovna logika može da propadne u vreme trčanja. Pošto reference na polja u dodatnim komponentama nisu proverene u trenutku uvoza, poslovna logika može da propadne zbog referenci na polja koja više ne postoje i možda ćete dobiti poruku o grešci koja je slična sledećem primeru: "'Projekat' entitet ne sadrži atribut sa imenom = "msdyn_plannedhours" i "Mapiranje imena " = "Logički". U tom slučaju, izmenite prilagođavanja tako da koriste nova polja. Ako koristite automatski generisane proxy klase i jake reference tipa u logici dodatne komponente, razmislite o ponovnom generisanju tih punomoćnika iz čiste instalacije. Na ovaj način možete lako da identifikujete sva mesta na kojima dodatne komponente zavise od neodobrenih polja.

Kada ažurirate prilagođavanja da biste čisto uvezli operacije projekta, pređite na sledeće korake.

## <a name="end-to-end-testing-in-development-environments"></a>End-to-end testiranje u razvojnim okruženjima

### <a name="initiate-upgrade"></a>Započni nadogradnju 

1. U administrativnom Power Platform centru pronađite i izaberite okruženje. Zatim, u aplikacijama pronađite i izaberite **Dynamics 365 Project Operations**.
2. Kliknite na **dugme "** Instaliraj" da biste započeli nadogradnju. Administrativni Power Platform centar će predstaviti ovu instalaciju kao novu instalaciju. Međutim, biće otkriveno prisustvo prethodne verzije automatizacije projektne usluge i postojeća instalacija će biti nadograđena.

    Kada se nadogradnja dovrši, okruženje bi trebalo da pokaže da su operacije projekta instalirane i da automatizacija usluge projekta nije instalirana.

    U zavisnosti od količine podataka u okruženju, nadogradnja može da potraje nekoliko sati. Osnovni tim koji upravlja nadogradnjom treba da planira u skladu sa tim i da pokrene nadogradnju tokom neradnog radnog vremena. U nekim slučajevima, ako je volumen podataka veliki, nadogradnja bi trebalo da se pokrene tokom vikenda. Odluka o zakazivanju treba da bude zasnovana na rezultatima testiranja u nižim sredinama.

3. Nadogradite prilagođena rešenja na odgovarajući način. U ovom trenutku, primenite sve promene koje ste načinili na prilagođavanjima [u odeljku Prilagođavanja testiranja i reaktora](#testing-and-refactoring-customizations) ovog članka.
4. Idite na **rešenja** \> **za** postavke i izaberite da biste deinstalirali rešenje "**Neodobrene komponente operacija projekta**".

    Ovo rešenje je privremeno rešenje koje sadrži postojeći model podataka i komponente koje su prisutne tokom nadogradnje. Uklanjanjem ovog rešenja uklanjate sva polja i komponente koje se više ne koriste. Na taj način ćete pojednostaviti interfejs i olakšati integraciju i proširenje.
    
### <a name="upgrade-to-project-operations-lite"></a>Nadogradnja na projektne operacije Lite

Sledeći koraci opisuju proces nadogradnje i povezano evidentiranje grešaka:

1. **PROVERA PSA verzije:** Da biste instalirali operacije projekta, morate imati V3.10.58.120 ili noviji.
1. **Pre provere valjanosti:** Kada administrator započne nadogradnju, sistem pokreće operaciju provere valjanosti za svaki entitet koji je jezgro rešenja za operacije projekta. Ovaj korak potvrđuje da su reference svih entiteta važeće i obezbeđuje da podaci koji su povezani sa WBS-om budu u okviru objavljenih granica projekta za Web.
1. **Nadogradnja metapodataka:** Nakon uspešne provere valjanosti, sistem pokreće promene šeme i kreira rešenje za neodobrene komponente. Ovo neodobreno rešenje možete ukloniti nakon što dovršite sva potrebna reaktoring prilagođavanja. Ovaj korak je najduži deo procesa nadogradnje i može da potraje do četiri sata.
1. **Nadogradnja podataka:** Kada se sve potrebne promene šeme dovrše u koraku nadogradnje metapodataka, podaci se migriraju u novu šemu i rade se sve potrebne podrazumevane vrednosti i ponovno izračunavanje.
1. **Ažuriranje mašine za plan projekta:** Nakon uspešne nadogradnje podataka, kartica **"** Raspored" na glavnoj stranici je ponovo zaoštećena za **zadatke**. Kada korisnik izabere ovu karticu nakon nadogradnje, oni su usmereni na kretanje do koordinatne mreže za praćenje da bi prikazali verziju WBS-a koja je samo za čitanje. Da bi uredili WBS, moraju da započnu proces konverzije [rasporeda](/PSA-Upgrade-Project-Conversion.md). Svi projekti bez postojećeg WBS-a mogu direktno da koriste novo iskustvo zakazivanja, bez konverzije.
 
### <a name="validate-common-scenarios"></a>Provera valjanosti uobičajenih scenarija

Kada proveravate valjanost određenih prilagođavanja, preporučujemo da pregledate i poslovne procese koji su podržani u svim aplikacijama. Ovi poslovni procesi uključuju, ali se ne ograničavaju na kreiranje entiteta prodaje kao što su citati i ugovori, kao i kreiranje projekata koji uključuju WBS i odobravanje stvarnih podataka.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Velike promene između automatizacije projektnih usluga i projektnih operacija

Ovaj odeljak sadrži rezime velikih promena koje možete očekivati između automatizacije projektnih usluga i operacija projekta.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u operacijama projekta se više ne oslanjaju na kombinaciju logike na strani klijenta i logike na strani servera. Umesto toga, operacija projekta koristi projekat za Web kao mašinu za planiranje. Ova promena mogućnosti planiranja omogućava nekoliko novih funkcija, kao što su prikazi boarda i gant, planiranje vođeno resursima, [stavke kontrolne liste](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) zadataka i režimi planiranja projekta. Nove mogućnosti zakazivanja takođe podržava bogat skup novih interfejsa programiranja [aplikacija (API)](../project-management/schedule-api-preview.md). Ovi API-i su namenjeni da obezbede da nijedna programska operacija za kreiranje, ažuriranje ili brisanje entiteta u WBS-u ne ošteti izračunata polja u rasporedu.

### <a name="billing-and-pricing"></a>Naplata i određivanje cena

U okviru kontinuiranih investicija u projektne operacije, u naplati i cenama dostupno je nekoliko novih mogućnosti. U nastavku su navedeni neki primeri:

- [Snimanje korišćenja materijala na projektima i projektne zadatke](../material/material-usage-log.md)
- [Upravljanje podizvođačima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi i ugovori zasnovani na avansnim uplatama](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status i provere valjanosti ugovora koji se ne premašuju](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata zasnovana na zadatku

### <a name="resource-management"></a>Upravljanje resursima

Operacije projekta pružaju opcionalnu podršku Universal Resource Scheduling odboru (URS) i pomoćniku za planiranje. Ovo novo iskustvo postaće obavezno u talasu aprila 2023.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koji tipovi primene su trenutno podržani za nadogradnju?

| Izvor                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Primena lite operacija projekta                        | Podržano               |
| Dynamics 365 Finance upravljanje projektima i računovodstvo | Primena lite operacija projekta                        | Trenutno nije podržano |
| Upravljanje i računovodstvo finansijskih projekata              | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Automatizacija usluge projekta 3.x                         | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Projekat za Web (namensko okruženje)            | Primena lite operacija projekta                        | Trenutno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako mogu da instaliram operacije projekta pre nego što alatka za nadogradnju bude dostupna?

Postoje dve opcije za instaliranje operacija projekta pre nego što alatka za nadogradnju bude dostupna:

- Obezbedite novu sredinu.
- Posebno rasporedite operacije projekta na bilo kojoj prodajnoj organizaciji u kojoj automatizacija usluge projekta nije prisutna.

Ako je automatizacija usluge projekta instalirana u organizaciji, ali nije korišćena, može se deinstalirati. Kada u potpunosti uklonite automatizaciju projektne usluge, operacije projekta se mogu instalirati u istoj organizaciji.
