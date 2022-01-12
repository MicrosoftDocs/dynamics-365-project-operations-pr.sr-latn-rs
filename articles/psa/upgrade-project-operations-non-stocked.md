---
title: Nadogradnja sa automatizacije projektnih usluga na projektne operacije
description: Ova tema obezbeđuje pregled procesa za nadogradnju sa Microsoft Dynamics 365 Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954300"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja sa automatizacije projektnih usluga na projektne operacije

Uzbuđeni smo što ćemo objaviti prvu od tri faze za nadogradnju Microsoft Dynamics 365 Project Service Automation sa na Dynamics 365 Project Operations. Ovaj tema pruža pregled za kupce koji kreću na ovo uzbudljivo putovanje. Buduće teme će uključivati razmatranja projektanta i detalje o poboljšanjima funkcija. Oni ne samo da će vam pružiti smernice koje će vam pomoći da se pripremite za nadogradnju na operacije projekta, već će vam objasniti i šta možete očekivati nakon nadogradnje.

Program za isporuku nadogradnje biće podeljen u tri faze.

| Nadogradnja isporuke | Faza 1 (januar 2022) | Faza 2 (aprilski talas 2022) | Faza 3 (aprilski talas 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Nema zavisnosti od strukture kvara na radu (WBS) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS u okviru trenutno podržanih granica projektnih operacija | | :heavy_check_mark: | :heavy_check_mark: |
| WBS izvan trenutno podržanih ograničenja projektnih operacija, uključujući podršku za klijenta radne površine projekta | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije procesa nadogradnje 

U sklopu procesa nadogradnje dodali smo evidencije nadogradnje na mapu lokacije, tako da administratori lakše dijagnostikuju neuspehe. Pored novog interfejsa, biće dodata i nova pravila za proveru valjanosti kako bi se osigurao integritet podataka nakon nadogradnje. Sledeće provere valjanosti biće dodate procesu nadogradnje.

| Provere valjanosti | Faza 1 (januar 2022) | Faza 2 (aprilski talas 2022) | Faza 3 (aprilski talas 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| WBS će biti proveren u odnosu na uobičajena kršenja integriteta podataka (na primer, dodele resursa koje su povezane sa istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti proveren u odnosu na [poznata ograničenja projekta za Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| WBS će biti proveren u odnosu na poznata ograničenja klijenta radne površine projekta. | | :heavy_check_mark: | :heavy_check_mark: |
| Knjigovodstveni resursi i kalendari projekta biće procenjeni u odnosu na uobičajene izuzetke pravila kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2, klijenti koji nadograde na projektne operacije imaće svoje postojeće projekte nadograđene na iskustvo samo za čitanje za planiranje projekta. U ovom iskustvu koje je samo za čitanje, ceo WBS će biti vidljiv u mreži za praćenje. Da bi uredili WBS, menadžeri projekta mogu da izaberu opciju **Konvertuj** na glavnoj **stranici** "Projekti". Proces u pozadini će zatim ažurirati projekat tako da podržava novo iskustvo zakazivanja projekta iz projekta za Web. Ova faza je prikladna za klijente koji imaju projekte koji se uklapaju [u poznate granice projekta za Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U fazi 3, biće dodata podrška za Project desktop klijenta, u korist klijenata koji žele da nastave da uređuju svoje projekte iz te aplikacije. Međutim, ako postojeći projekti budu konvertovani u novi Projekat za Web iskustvo, pristup programskog dodatku biće onemogućen za svaki konvertovani projekat.

## <a name="prerequisites"></a>Preduslovi

Da bi stekao pravo na nadogradnju faze 1, kupac mora da ispuni sledeće kriterijume:

- Ciljno okruženje ne sme da sadrži zapise **u msdyn_projecttask** entitetu.
- Važeće licence za projektne operacije moraju biti dodeljene svim aktivnim korisnicima klijenta. 
- Kupac mora da proveri valjanost procesa nadogradnje u najmanje jednom okruženju koje nije proizvodno okruženje koje ima reprezentativni skup podataka koji je usklađen sa podacima o proizvodnji.
- Ciljno okruženje mora biti ažurirano na verziju za automatizaciju usluge projekta Release 38 ili noviju verziju.

Preduslovi za fazu 2 i fazu 3 biće ažurirani kako se budu približavali datumi opšte dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za automatizaciju projektnih usluga, možete instalirati i koristiti projektne operacije, što uključuje sve mogućnosti automatizacije projektnih usluga i još mnogo toga. Na taj način možete da testirate mogućnosti projektnih operacija dok nastavljate da koristite automatizaciju projektnih usluga u proizvodnji. Kada licence za automatizaciju usluge projekta isteknu, moraćete da pređete na operacije projekta. Kada planirate ovaj prelaz, morate da računate na činjenicu da licenca za operacije projekta ne uključuje licencu za automatizaciju usluge projekta.

## <a name="testing-and-refactoring-customizations"></a>Prilagođavanja testiranja i reaktorata

Kao polaznu tačku, uvezite sva prilagođavanja u čisto okruženje projektnih operacija (lite) da biste potvrdili da je uvoz uspešan i da se poslovno poslovanje ponaša na očekivani način.

Evo nekih stvari na koje treba da se pazite:

- Uvoz možda neće uspeti zbog zavisnosti koje nedostaju. Drugim rečima, referentna polja prilagođavanja ili druge komponente koje su uklonjene u operacijama projekta. U ovom slučaju, uklonite ove zavisnosti iz razvojnog okruženja.
- Ako nekontrolisana i upravljana rešenja uključuju komponente koje nisu prilagođene, uklonite te komponente iz rešenja. Na primer, kada prilagodite **entitet** projekta, dodajte samo zaglavlje entiteta u rešenje. Nemojte dodavati sva polja. Ako ste prethodno dodali sve podkomponente, možda ćete morati ručno da kreirate novo rešenje i dodate mu relevantne komponente.
- Obrasci i prikazi možda neće izgledati tako neočekivano. U nekim okolnostima, ako ste prilagodili neki od obrazaca ili prikaza koji nisu u okviru, prilagođavanja mogu da spreče stupanje na snagu novih ispravki u operacijama projekta. Da biste identifikovali ove probleme, preporučujemo da uradite pregled čiste instalacije projektnih operacija i instalacije operacija projekta koja uključuje prilagođavanja. Uporedite najčešće korišćene obrasce u poslovanju da biste potvrdili da vaša verzija obrasca i dalje ima smisla i da vam ne nedostaje nešto iz čiste verzije obrasca. Uradite isti tip bočne redigorije za sve prikaze koje ste prilagodili.
- Poslovna logika može da propadne u vreme trčanja. Pošto reference na polja u dodatnim komponentama nisu proverene u trenutku uvoza, poslovna logika može da ne uspe zbog referenci na polja koja više ne postoje i možda ćete dobiti poruku o grešci koja je slična sledećem primeru: "'Projekat' entitet ne sadrži atribut sa imenom = "msdyn_plannedhours" i "Mapiranje imena " = "Logički". U tom slučaju, izmenite prilagođavanja tako da koriste nova polja. Ako koristite automatski generisane proxy klase i jake reference tipa u logici dodatne komponente, razmislite o ponovnom generisanju tih punomoćnika iz čiste instalacije. Na ovaj način možete lako da identifikujete sva mesta na kojima dodatne komponente zavise od neodobrenih polja.

Kada ažurirate prilagođavanja da biste čisto uvezli operacije projekta, pređite na sledeće korake.

## <a name="end-to-end-testing-in-lower-environments"></a>End-to-end testiranje u nižim okruženjima

### <a name="run-the-upgrade-in-production"></a>Pokretanje nadogradnje u proizvodnji

1. U Power Platform administrativnom centru pronađite i izaberite okruženje. Zatim, u aplikacijama pronađite i izaberite **Dynamics 365 Project Operations**.
2. Kliknite **na dugme** "Instaliraj" da biste započeli nadogradnju. Administrativni Power Platform centar će predstaviti ovu instalaciju kao novu instalaciju. Međutim, biće otkriveno prisustvo prethodne verzije automatizacije projektne usluge i postojeća instalacija će biti nadograđena.

    Kada se nadogradnja dovrši, okruženje bi trebalo da pokaže da su operacije projekta instalirane i da automatizacija usluge projekta nije instalirana.

    > [!NOTE]
    > U zavisnosti od količine podataka u okruženju, nadogradnja može da potraje nekoliko sati. Osnovni tim koji upravlja nadogradnjom treba da planira u skladu sa tim i da pokrene nadogradnju tokom neradnog radnog vremena. U nekim slučajevima, ako je volumen podataka veliki, nadogradnja bi trebalo da se pokrene tokom vikenda. Odluka o zakazivanju treba da bude zasnovana na rezultatima testiranja u nižim sredinama.

3. Nadogradite prilagođena rešenja na odgovarajući način. U ovom trenutku, primenite sve promene koje ste načinili na [prilagođavanjima u odeljku Prilagođavanja testiranja i reaktora](#testing-and-refactoring-customizations) ovog tema.
4. Idite **na** \> **rešenja** za postavke i izaberite da biste deinstalirali rešenje **"Neodobrene komponente operacija** projekta".

    Ovo rešenje je privremeno rešenje koje sadrži postojeći model podataka i komponente koje su prisutne tokom nadogradnje. Uklanjanjem ovog rešenja uklanjate sva polja i komponente koje se više ne koriste. Na taj način ćete pojednostaviti interfejs i olakšati integraciju i proširenje.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Velike promene između automatizacije projektnih usluga i projektnih operacija

Ovaj odeljak sadrži rezime velikih promena koje možete očekivati između automatizacije projektnih usluga i operacija projekta.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u operacijama projekta se više ne oslanjaju na kombinaciju logike na strani klijenta i logike na strani servera. Umesto toga, operacija projekta koristi projekat za Web kao mašinu za planiranje. Ova promena mogućnosti planiranja omogućava nekoliko novih funkcija, kao što su prikazi boarda i gant, planiranje vođeno resursima, [stavke kontrolne liste](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) zadataka i režimi planiranja projekta. Nove mogućnosti zakazivanja takođe podržava bogat skup novih programskih [interfejsa aplikacija (API)](../project-management/schedule-api-preview.md). Ovi API-i su namenjeni da obezbede da nijedna programska operacija za kreiranje, ažuriranje ili brisanje entiteta u WBS-u ne ošteti izračunata polja u rasporedu.

## <a name="billing-and-pricing"></a>Naplata i određivanje cena

U okviru kontinuiranih investicija u projektne operacije, u naplati i cenama dostupno je nekoliko novih mogućnosti. U nastavku su navedeni neki primeri:

- [Snimanje korišćenja materijala na projektima i projektne zadatke](../material/material-usage-log.md)
- [Upravljanje podizvođačima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi i ugovori zasnovani na avansnim uplatama](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Status i provere valjanosti ugovora koji se ne premašuju](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata zasnovana na zadatku

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koji tipovi primene su trenutno podržani za nadogradnju?

| Izvor                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Primena lite operacija projekta                        | Podržano               |
| Dynamics 365 Finance Upravljanje projektima i računovodstvo | Primena lite operacija projekta                        | Trenutno nije podržano |
| Upravljanje i računovodstvo finansijskih projekata              | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Upravljanje i računovodstvo finansijskih projekata              | Project Operations za scenarije sa materijalima na zalihama/porudžbinama za proizvodnju | Trenutno nije podržano |
| Automatizacija usluge projekta 3.x                         | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Projekat za Web (namensko okruženje)            | Primena lite operacija projekta                        | Trenutno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako mogu da instaliram operacije projekta pre nego što alatka za nadogradnju bude dostupna?

Postoje dve opcije za instaliranje operacija projekta pre nego što alatka za nadogradnju bude dostupna:

- Obezbedite novu sredinu.
- Posebno rasporedite operacije projekta na bilo kojoj prodajnoj organizaciji u kojoj automatizacija usluge projekta nije prisutna.

> [!NOTE]
> Ako je automatizacija usluge projekta instalirana u organizaciji, ali nije korišćena, može se deinstalirati. Kada u potpunosti uklonite automatizaciju projektne usluge, operacije projekta se mogu instalirati u istoj organizaciji.
