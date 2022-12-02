---
title: Nadogradnja sa aplikacije Project Service Automation na uslugu Project Operations
description: Ovaj članak pruža pregled procesa nadogradnje sa Microsoft Dynamics 365 Project Service Automation na rešenje Dynamics 365 Project Operations.
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736684"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Nadogradnja sa aplikacije Project Service Automation na uslugu Project Operations

Sa uzbuđenjem najavljujemo drugu od tri faze nadogradnje sa rešenja Microsoft Dynamics 365 Project Service Automation na Microsoft Dynamics 365 Project Operations. Ovaj članak pruža pregled za klijente koji kreću na ovo uzbudljivo putovanje. 

Program isporuke nadogradnje biće podeljen u tri faze.

| Isporuka nadogradnje | 1. faza (januar 2022.) | 2. faza (novembar 2022.) | 3. faza (aprilski talas 2023.)  |
|------------------|------------------------|---------------------------|---------------------------|
| Nema zavisnosti na strukturnoj analizi posla (SAP) za projekte | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| SAP unutar trenutno podržanih ograničenja za Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| SAP izvan trenutno podržanih ograničenja za Project Operations, uključujući podršku za Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funkcije procesa nadogradnje 

U sklopu procesa nadogradnje dodali smo evidencije nadogradnje na mapu lokacije kako bismo omogućili administratorima da lakše dijagnostikuju neuspehe. Pored novog interfejsa, biće dodata i nova pravila za proveru ispravnosti kako bi se osigurao integritet podataka nakon nadogradnje. Sledeće provere ispravnosti biće dodate procesu nadogradnje.

| Validacije | 1. faza (januar 2022.) | 2. faza (novembar 2022.) | Faza 3  |
|-------------|------------------------|---------------------------|---------------------------|
| SAP će biti validiran prema uobičajenim kršenjima integriteta podataka (na primer, dodele resursa koje su povezane sa istim nadređenim zadatkom, ali imaju različite nadređene projekte). | | :heavy_check_mark: | :heavy_check_mark: |
| SAP će biti validiran prema [poznatim ograničenjima za Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| SAP će biti validiran prema poznatim ograničenjima za Project Desktop Client. | |  | :heavy_check_mark: |
| Knjigovodstveni resursi i kalendari projekta biće procenjeni u odnosu na uobičajene nekompatibilne izuzetke pravila kalendara. | | :heavy_check_mark: | :heavy_check_mark: |

U fazi 2, klijenti koji nadograde na Project Operations imaće svoje postojeće projekte nadograđene na iskustvo samo za čitanje za planiranje projekta. U ovom iskustvu koje je samo za čitanje, ceo SAP biće vidljiv u matrici koordinatne mreže za praćenje. Da bi uredili SAP, projektni menadžeri mogu da izaberu [**Konvertuj**](/PSA-Upgrade-Project-Conversion.md) na glavnoj stranici projekta. Proces u pozadini zatim ažurira projekat tako da podržava novo iskustvo zakazivanja projekta iz rešenja Project for the Web. Ova faza je prikladna za klijente koji imaju projekte koji se uklapaju u [poznata ograničenja rešenja Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

U 3. fazi, biće dodata podrška za Project desktop client, u korist klijenata koji žele da nastave da uređuju svoje projekte iz te aplikacije. Međutim, ako postojeći projekti budu konvertovani u novo iskustvo rešenja Project for the Web, pristup programskom dodatku biće onemogućen za svaki konvertovani projekat.

## <a name="prerequisites"></a>Preduslovi

Da biste ispunili uslove za nadogradnju 1. faze, morate da ispunite sledeće kriterijume:

- Ciljno okruženje ne sme da sadrži zapise u **msdyn_projecttask** entitetu.
- Važeće licence za Project Operations moraju biti dodeljene svim aktivnim korisnicima. 
- Morate da proverite valjanost procesa nadogradnje u najmanje jednom neproizvodnom okruženju koje sadrži reprezentativni skup podataka koji je usklađen sa proizvodnim okruženjem.
- Ciljno okruženje mora biti ažurirano na 37 verziju ažuriranja rešenja Project Service Automation (V3.10.58.120) ili noviju verziju.

Da biste ispunili uslove za nadogradnju 2. faze, morate da ispunite sledeće kriterijume:

- Važeće licence za Project Operations moraju biti dodeljene svim aktivnim korisnicima. 
- Morate da proverite valjanost procesa nadogradnje u najmanje jednom neproizvodnom okruženju koje sadrži reprezentativni skup podataka koji je usklađen sa proizvodnim okruženjem.
- Ciljno okruženje mora biti ažurirano na 37 verziju ažuriranja rešenja Project Service Automation (V3.10.58.120) ili noviju verziju.
- Okruženja koja sadrže zadatke (msdyn_projecttask) podržana su samo ako je ukupan broj zadataka po projektu 500 ili manji.

Preduslovi za 3. fazu biće ažurirani kako se približava datum opšte dostupnosti.

## <a name="licensing"></a>Licenciranje

Ako imate aktivne licence za Project Service Automation, možete instalirati i koristiti rešenje Project Operations, što uključuje sve mogućnosti rešenja Project Service Automation i još mnogo toga. Na taj način možete da testirate mogućnosti rešenja Project Operations dok nastavljate da koristite Project Service Automation u proizvodnji. Kada licence za Project Service Automation isteknu, moraćete da pređete na Project Operations. Kada planirate ovaj prelaz, morate da računate na činjenicu da licenca za Project Operations ne uključuje licencu za Project Service Automation. Klijenti koji imaju scenarije u kojima su primenili Project Service Automation i moraju da nastave da koriste ili povećavaju svoje licence za PSA dok nameravaju da pređu na Project Operations mogu da zatraže privremene PSA licence na osnovu kupljenih licenci za Project Operations. Jedna Project Service Automation licenca biće izdata za jednu Project Operations licencu. Privremene PSA licence mogu biti zatražene putem ovog linka: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Prilagođavanja testiranja i refaktoringa

Kao polaznu tačku, uvezite sva prilagođavanja u čisto Project Operations (jednostavna primena) okruženje kako biste potvrdili da je uvoz uspešan i da se poslovne operacije ponašaju kao što je očekivano.

Evo nekih stvari na koje treba da obratite pažnju:

- Uvoz možda neće uspeti zbog zavisnosti koje nedostaju. Drugim rečima, referentna polja prilagođavanja ili druge komponente koje su uklonjene u usluzi Project Operations. U ovom slučaju, uklonite ove zavisnosti iz razvojnog okruženja.
- Ako nenadgledano i kompletno rešenje uključuju komponente koje nisu prilagođene, uklonite te komponente iz rešenja. Na primer, kada prilagodite entitet **Projekat**, dodajte samo zaglavlje entiteta u rešenje. Nemojte dodavati sva polja. Ako ste prethodno dodali sve potkomponente, možda ćete morati ručno da kreirate novo rešenje i dodate mu relevantne komponente.
- Obrasci i prikazi se možda neće prikazivati na očekivani način. U nekim okolnostima, ako ste prilagodili neki od gotovih obrazaca ili prikaza, prilagođavanja mogu da spreče stupanje na snagu novih ispravki u usluzi Project Operations. Da biste identifikovali ove probleme, preporučujemo da uradite komparativni pregled čiste instalacije rešenja Project Operations i instalacije rešenja Project Operations koja uključuje prilagođavanja. Uporedite najčešće korišćene obrasce u poslovanju da biste potvrdili da vaša verzija obrasca i dalje ima smisla i da vam ne nedostaje nešto iz čiste verzije obrasca. Uradite isti tip komparativnog pregleda za sve prikaze koje ste prilagodili.
- Poslovna logika može otkazati pri vremenu izvršavanja. Pošto reference na polja u dodatnim komponentama nisu potvrđene u trenutku uvoza, poslovna logika može da ne uspe zbog referenci na polja koja više ne postoje i možda ćete dobiti poruku o grešci koja je slična sledećem primeru: „Entitet 'Project' ne sadrži atribut sa Name = 'msdyn_plannedhours' i NameMapping = 'Logical'“. U tom slučaju, izmenite prilagođavanja tako da koriste nova polja. Ako koristite automatski generisane proksi klase i reference jakog tipa u logici dodatne komponente, razmislite o ponovnom generisanju tih proksija iz čiste instalacije. Na ovaj način možete lako da identifikujete sva mesta na kojima dodatne komponente zavise od zastarelih polja.

Kada ažurirate prilagođavanja da biste čisto uvezli rešenje Project Operations, pređite na sledeće korake.

## <a name="end-to-end-testing-in-development-environments"></a>Kompletno testiranje u razvojnim okruženjima

### <a name="initiate-upgrade"></a>Započni nadogradnju 

1. U Power Platform centru administracije, pronađite i izaberite vaše okruženje. Zatim, u aplikacijama, pronađite i izaberite **Dynamics 365 Project Operations**.
2. Izaberite **Instaliraj** za početak nadogradnje. Power Platform centar administracije će predstaviti ovu instalaciju kao novu instalaciju. Međutim, biće detektovano prisustvo prethodne verzije rešenja Project Service Automation i postojeća instalacija će biti nadograđena.

    Kada se nadogradnja dovrši, okruženje bi trebalo da pokaže da je Project Operations instalirano, a da Project Service Automation nije instaliran.

    U zavisnosti od količine podataka u okruženju, za nadogradnju može biti potrebno nekoliko časova. Osnovni tim koji upravlja nadogradnjom treba da planira u skladu sa tim i da pokrene nadogradnju van radnog vremena. U nekim slučajevima, ako je količina podataka velika, nadogradnja bi trebalo da se pokrene tokom vikenda. Odluka o planiraju treba da bude zasnovana na rezultatima testiranja u nižim okruženjima.

3. Nadogradite prilagođena rešenja na odgovarajući način. U ovom trenutku, primenite sve promene koje ste napravili u prilagođavanjima u odeljku [Prilagođavanja testiranja i refaktoringa](#testing-and-refactoring-customizations) ovog članka.
4. Idite na **make.powerapps.com**, sa padajućeg menija u gornjem desnom uglu portala izaberite vaše okruženje, izaberite **Rešenja** iz levog menija, izaberite rešenje **Zastarele komponente rešenja Project Operations** i **Deinstalirajte**.

    Ovo rešenje je privremeno rešenje koje sadrži postojeći model podataka i komponente koje su prisutne tokom nadogradnje. Uklanjanjem ovog rešenja uklanjate sva polja i komponente koje se više ne koriste. Na taj način ćete pojednostaviti interfejs i olakšati integraciju i proširenje.
    
### <a name="upgrade-to-project-operations-lite"></a>Nadogradnja na Project Operations jednostavnu primenu

Sledeći koraci opisuju proces nadogradnje i povezano evidentiranje grešaka:

1. **Provera PSA verzije:** Da biste instalirali Project Operations, morate da imate V3.10.58.120 ili noviju verziju.
1. **Prethodna provera valjanosti:** Kada administrator inicira nadogradnju, sistem pokreće operaciju prethodne provere valjanosti za svaki entitet koji predstavlja jezgro rešenja Project Operations. Ovaj korak potvrđuje da su reference svih entiteta važeće i obezbeđuje da podaci koji su povezani sa SAP-om budu u okviru objavljenih granica rešenja Project for the Web.
1. **Nadogradnja metapodataka:** Nakon uspešne prethodne provere valjanosti, sistem pokreće promene šeme i kreira rešenje za zastarele komponente. Ovo zastarelo rešenje možete ukloniti nakon što dovršite sav potreban refaktoring i prilagođavanja. Ovaj korak je najduži deo procesa nadogradnje i može da potraje do četiri sata.
1. **Nadogradnja podataka:** Kada se sve potrebne promene šeme dovrše u koraku nadogradnje metapodataka, podaci se migriraju u novu šemu i rade se sva potrebna podešavanja podrazumevanih vrednosti i ponovno izračunavanje.
1. **Ažuriranje mehanizma za raspored projekta:** Nakon uspešne nadogradnje podataka, kartica **Raspored** na glavnoj stranici je ponovo označena kao **Zadaci**. Kada korisnik izabere ovu karticu nakon nadogradnje, usmerava se da ode do matrice koordinatne mreže za praćenje da bi prikazao verziju SAP-a koja je samo za čitanje. Da bi uredio SAP, mora da započne [proces konverzije](/PSA-Upgrade-Project-Conversion.md) rasporeda. Svi projekti bez postojećeg SAP-a mogu direktno da koriste novo iskustvo planiranja, bez konverzije.
 
### <a name="validate-common-scenarios"></a>Provera uobičajenih scenarija

Kada proveravate valjanost određenih prilagođavanja, preporučujemo da pregledate i poslovne procese koji su podržani u svim aplikacijama. Ovi poslovni procesi uključuju, ali se ne ograničavaju na, kreiranje entiteta prodaje kao što su ponude i ugovori, kao i kreiranje projekata koji uključuju SAP-ove i odobrenje stvarnih vrednosti.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Glavne promene između rešenja Project Service Automation i Project Operations

Ovaj odeljak sadrži rezime velikih promena koje možete očekivati između rešenja Project Service Automation i Project Operations.

### <a name="project-planning"></a>Planiranje projekta

Mogućnosti planiranja projekta u Project Operations se više ne oslanjaju na kombinaciju logike na strani klijenta i logike na strani servera. Umesto toga, Project Operations koristi Project for the Web kao mehanizam za planiranje. Ova promena mogućnosti planiranja omogućava nekoliko novih funkcija, kao što su prikazi table i Gantovog dijagrama, planiranje zasnovano na resursima, [stavke kontrolne liste zadataka](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i režimi planiranja projekta. Nove mogućnosti planiranja takođe podržavaju bogat skup novih [interfejsa za programiranje aplikacija (API)](../project-management/schedule-api-preview.md). Ovi API-ji su namenjeni da obezbede da nijedna programska operacija za kreiranje, ažuriranje ili brisanje entiteta u SAPU-u ne ošteti izračunata polja u rasporedu.

### <a name="billing-and-pricing"></a>Naplata i određivanje cena

U okviru kontinuiranih ulaganja u Project Operations, u Naplati i određivanju cena dostupno je nekoliko novih mogućnosti. U nastavku su navedeni neki primeri:

- [Evidentiranje korišćenja materijala na projektima i projektnim zadacima](../material/material-usage-log.md)
- [Upravljanje podugovorima](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avansi i ugovori zasnovani na avansnim uplatama](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Statusom i provere ugovora koje ne smete premašiti](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Naplata zasnovana na zadatku

### <a name="resource-management"></a>Upravljanje resursima

Project Operations pruža opcionu podršku za Universal Resource Scheduling (URS) tablu i pomoćnika za zakazivanje. Ovo novo iskustvo postaće obavezno u talasu izdanja za april 2023.

## <a name="frequently-asked-questions"></a>Najčešća pitanja

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Koji tipovi primene su trenutno podržani za nadogradnju?

| Izvor                                                 | Cilj                                                    | Status                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations jednostavna primena                        | Podržano               |
| Dynamics 365 Finance upravljanje projektima i računovodstvo | Project Operations jednostavna primena                        | Trenutno nije podržano |
| Upravljanje projektima i računovodstvo za Finance              | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Project Service Automation 3.x                         | Project Operations za scenarije sa resursima/materijalima koji nisu na zalihama     | Trenutno nije podržano |
| Project for the Web (namensko okruženje)            | Project Operations jednostavna primena                        | Trenutno nije podržano |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Kako mogu da instaliram Project Operations pre nego što alatke za nadogradnju budu dostupne?

Postoje dve opcije za instaliranje rešenja Project Operations pre nego što alatka za nadogradnju bude dostupna:

- Obezbedite novo okruženje.
- Primenite Project Operations zasebno na bilo koju prodajnu organizaciju na kojoj Project Service Automation nije prisutan.

Ako je Project Service Automation instaliran u organizaciji, ali se ne koristi, možete ga deinstalirati. Kada u potpunosti uklonite Project Service Automation, Project Operations možete instalirati u istoj organizaciji.
