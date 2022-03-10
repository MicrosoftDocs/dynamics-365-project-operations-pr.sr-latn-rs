---
title: Šta je novo u januaru 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations za januar 2021. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9d54d5fed6e8ec1535ad798073ac8a1eec36e87d1dbba4cc4acd94d8bbdc5157
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008108"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u januaru 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_


Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

  - Project Operations u Dataverse okruženju verzije 4.6.0.154
  - Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.16

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| **Primena i konfiguracija** | 2106818 | Ispravljeno je preimenovanje veb-resursa koje je uzrokovalo probleme u vezi sa prilagođavanjem stranice. |
| **Naplata i određivanje cena** | 2091908 | Popravljena je vidljivost opcija **Zaključaj cene** i **Koristite trenutne cene** na stranici **Faktura** kada su instalirani i Project Operations i Dynamics 365 Field Service. |
| **Naplata i određivanje cena** | 2103058 | Osvežene su **Ukupne vrednosti za projekat** za obradu nultih vrednosti stvarnih troškova zadatka. |
| **Naplata i određivanje cena** | 2116100 | Poboljšane su poruke o greškama koje se koriste sa funkcionalnošću **Ispravni unosi za stvarne vrednosti**. |
| **Naplata i određivanje cena** | 2116129 | Poboljšana je vidljivost procena troškova na kartici **Procene** na stranici **Projekti**. |
| **Naplata i određivanje cena** | 2119112 | Ispravljeno je objedinjavanje stvarne prodaje i stvarnih troškova kada se koriste različiti devizni kursevi. |
| **Naplata i određivanje cena** | 2134705 | Ispravljena je greška „Ne može da se pročita svojstvo **getResourceString** nedefinisane stavke“ kada je stranica **Faktura** otvorena i kada je Field Service instaliran. |
| **Upravljanje mogućnostima za poslovanje** | 2022195 | Mreža za naplatu zasnovana na zadacima na stranici **Projekat** sadrži ikonu koja ukazuje da postoji predmet ugovor ili ponuda povezana sa tim zadatkom. |
| **Upravljanje mogućnostima za poslovanje** | 2029135 | Ispravljena je greška poslovnog procesa koja se javlja kada korisnik pokuša da otvori stavku fakture na potvrđenoj fakturi koja ima fakturisani iznos avansa. |
| **Upravljanje mogućnostima za poslovanje** | 2040713 | Ispravljena je greška skripte koja se javlja prilikom kreiranja fakture iz ugovora i kada je Field Service instaliran. |
| **Planiranje i praćenje projekta** | 2090202 | Označena su poslovna pravila koja se više ne koriste kao **Zastarela**. |
| **Vreme i trošak** | 2091249 | Ograničene su kontrole tako da korisnici ne mogu da promene zadatak u stavci vremena koja je podneta ili odobrena. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstva u usluzi Dynamics 365 Finance

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| **Upravljanje projektima i računovodstvo** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Netačan iznos za ugovor na stranici **Na kredit** za projekat sa fiksnom cenom sa više izvora finansiranja. |
| **Upravljanje projektima i računovodstvo** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Čuvar mesta **Invoiceproposal.PSAnfRefProjId** ne prikazuje ID projekta za tok posla **Pregled predloga projektnih faktura**. |
| **Upravljanje projektima i računovodstvo** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Pogrešan datum popusta na gotovinu koristi se prilikom knjiženja predloga fakture za projekat. |
| **Upravljanje projektima i računovodstvo** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Uklanjanje i čitanje dodela resursa u usluzi Project Operations udvostručuje unose predviđanja projekata u usluzi Finance. |
| **Upravljanje projektima i računovodstvo** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | U usluzi Project Operations ne možete da kreirate procene projekata u usluzi Dataverse ako ne postoji predmet ugovora za projekat. |
| **Upravljanje projektima i računovodstvo** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Finansijski aspekt transakcije troškova projekta nije sinhronizovan sa povezanim vaučerom i računovodstvenom distribucijom izveštaja o troškovima kada se troškovi knjiže na bilans. |
| **Upravljanje projektima i računovodstvo** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filter **Status fakture** za proknjižene transakcije projekata sa fiksnom cenom ne radi. |
| **Upravljanje projektima i računovodstvo** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacija obrnute procene ne radi u odeljku **Periodično**. |
| **Upravljanje projektima i računovodstvo** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Stavke predloga fakture ne mogu se izbrisati u usluzi Project Operations kada se integrišu uz Dataverse. |
| **Upravljanje projektima i računovodstvo** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Sprečite omogućavanje funkcije više predmeta ugovora bez Dataverse integracije. |
| **Upravljanje projektima i računovodstvo** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Kada je fakturisanje na kredit jednako profitu i gubitku, fakturisani prihod je naveden kao nula na stranici Procene. |
| **Upravljanje projektima i računovodstvo** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Ispravke fakture ne funkcionišu u integrisanim okruženjima. |
| **Upravljanje projektima i računovodstvo** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Prilikom knjiženja WIP prodajne vrednosti u fakturisanju projekta u okviru preduzeća, bira se pogrešan poslovni kontakt. |
| **Upravljanje projektima i računovodstvo** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | U usluzi Project Operations ne mogu se ažurirati zavisni elementi u zadacima procene u usluzi Dataverse. |
| **Upravljanje projektima i računovodstvo** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Neprestano brisanje Project Operations dnevnika integracije u usluzi Finance dovodi do gubitka podataka. |
| **Upravljanje projektima i računovodstvo** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Sledeća greška se javlja prilikom knjiženja predloga fakture za projekat: „Transakcija se ne uravnotežuje u valuti izveštavanja kada se doda odbijena fakturisana avansna uplata“. |
| **Upravljanje projektima i računovodstvo** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Pogrešan ID projekta uključuje se u odbitke nakon što se podrazumevani projektni ugovor ažurira u usluzi Project Operations. |
| **Upravljanje projektima i računovodstvo** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Procena i prepoznavanje prihoda ne mogu se dovršiti kada je Project Operations omogućen. |
| **Upravljanje projektima i računovodstvo** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | U usluzi Project Operations, uklanjanje projekta iz ugovora ne resetuje podrazumevani projekat u ugovoru. |
| **Upravljanje projektima i računovodstvo** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | U usluzi Project Operations, na fakturi u okviru preduzeća se prikazuju pogrešni redovi troškova na listi **Dodaj red**. |
| **Putovanje i trošak** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Redovi troškova ne mogu se knjižiti jer u predmetu ugovora nedostaje podešavanje za sate. |
| **Putovanje i trošak** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Kada je validacija projekta/kategorije obavezna, kategorije troškova povezane sa projektom nisu vidljive u izveštaju o troškovima. |
| **Putovanje i trošak** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Stanje gotovinskog avansa se ne ažurira kada se izveštaj o troškovima objavi po redu. |
| **Putovanje i trošak** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Posao **Ažuriranje informacija o plaćanju** ne uspeva nakon storniranja poravnanja gde je faktura izmirena sa dve ili više platnih transakcija. |
| **Putovanje i trošak** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Postoji problem sa izračunavanjem umanjenja za obrok poslednjeg dana za kategoriju troška dnevnica. |
| **Putovanje i trošak** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Izveštaj **Vrsta troškova po zaposlenom** ne prikazuje pojedinačne troškove ako je prva veza korisnik na jeziku es-MX. |
| **Putovanje i trošak** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Isplata dobavljača za fakturu izveštaja o troškovima koristi pogrešan objedinjeni poslovni kontakt za knjiženje poravnanja. |
| **Putovanje i trošak** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Kada je izveštaj o troškovima postavljen sa omogućenim opcijama **Dozvoli grupisanje transakcija na osnovu pomaka plaćanja za poslovni kontakt** i **Korekcija računovodstvenog datuma pri knjiženju**, datumi knjiženja nisu grupisani u tabeli **Računovodstvena distribucija**, što utiče na evidenciju poreza na promet. |
| **Putovanje i trošak** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Mapiranje potkategorije troškova uklanja se kada se izbriše znak u polju za potvrdu „Koristi za troškove“, a zatim ponovo unese. |
| **Putovanje i trošak** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Nije moguće kreirati izveštaj o troškovima u okviru preduzeća ako se ID projekta doda na nivou zaglavlja. |
| **Putovanje i trošak** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Postoji problem u vezi sa plaćanjem troškova kada je iznos troškova veći od iznosa gotovinskog avansa. |
| **Putovanje i trošak** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Polje **ID projekta** u izveštaju o troškovima u okviru preduzeća je prazno ako je korisnička uloga dodeljena određenoj organizaciji. |
| **Putovanje i trošak** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorija troškova je zaključana prilikom dodavanja novog reda za troškove. |
| **Putovanje i trošak** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Navođenje redova izveštaja o troškovima koji su već podeljeni dovodi do nekompletnog proknjiženog vaučera za Dugovanja\Glavna knjiga. Zbog dupliranja stavke **TRVEXPTRANS.SOURCEDOCUMENTLINE** neispravan je i istraživač računovodstvenog izvora. |
| **Putovanje i trošak** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeks dodat u tabelu **TRVREQUISITIONLINE** za koju klijent ima duplikate dovodi do greške tokom nadogradnje. |
| **Putovanje i trošak** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | U usluzi Project Operations, vreme za zadatke u okviru preduzeća ne može se kreirani ni odobriti u usluzi Dataverse. |

## <a name="regulatory-updates"></a>Regulatorne ispravke

Za informacije o regulatornim ispravkama za Finance and Operations aplikacije, pogledajte članak [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe se možete prijaviti na LCS i pregledati planirane regulatorne ispravke pomoću alatke za pretragu problema. Pretraga problema vam omogućava pretragu po zemlji, tipu funkcije i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]