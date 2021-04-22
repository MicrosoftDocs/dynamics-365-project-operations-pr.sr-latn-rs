---
title: Šta je novo u aprilu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha
description: Ova tema pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations za april 2021. godine za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868010"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u aprilu 2021. – Project Operations za scenarije zasnovane na resursima / bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ova tema se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.9.0.221
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.17

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Materijali bez zaliha za projekte. Ključne mogućnosti uključuju:
  - Procena i određivanje cene materijala bez zaliha tokom ciklusa prodaje u projektu. Za više informacija, pogledajte [Podešavanje troškova i stopa prodaje za proizvode iz kataloga – jednostavno](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Praćenje upotrebe materijala bez zaliha tokom isporuke projekata. Za više informacija pogledajte [Evidentiranje upotrebe materijala na projektima i projektnim zadacima](../material/material-usage-log.md).
  - Fakturisanje utrošenih troškova materijala bez zaliha. Za više informacija, pogledajte [Upravljanje zaostalim obračunom](../proforma-invoicing/manage-billing-backlog.md).
- Naplata zasnovana na zadatku: Dodata je mogućnost povezivanja projektnih zadataka sa predmetima ugovora o projektu, izlažući ih istom načinu naplate, učestalosti fakturisanja i klijentima kao i onima na predmetu ugovora. Ova veza osigurava tačno fakturisanje, računovodstvo, procenu prihoda i priznanje za rad u skladu sa ovim podešavanjem na projektnim zadacima.
- Novi API-ji u platformi Dynamics 365 Dataverse dozvoljavaju kreiranje, ažuriranje i brisanje operacija pomoću **entiteta planiranja**. Za više informacija, pogledajte [Korišćenje API-ja za raspored za obavljanje operacija sa entitetima planiranja](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations na platformi Dynamics 365 Dataverse

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Naplata i određivanje cena | 2124532 | Dugme **Ispravi fakturu** se prikazuje na predračunu kada je iznos zadrške ili primenjeni iznos zadrške prisutan na originalnoj fakturi. Dugme se prikazuje samo za okruženja sa uslugom Finance verzije 10.0.19 ili novijom. |
| Naplata i određivanje cena | 2224568 | Dodata je logika za omogućavanje prilagođavanja koja uključuju pozivanje dodatne komponente za potvrdu fakture. |
| Naplata i određivanje cena | 2101098 | Poboljšana logika podrazumevanih polja za predračun: **Adresa fakturisanja**, **Ime fakturisanja** i **Uslovi plaćanja** sada se podrazumevaju iz odgovarajućeg zapisa klijenta ugovora o projektu. |
| Naplata i određivanje cena | 2021413 | Ažurirana su polja **Stvarna cena** i **Prodaja** na entitetu **Zadatak** da uključi vrednosti prodaje iz nenaplaćenih i naplaćenih troškova na zadacima. |
| Naplata i određivanje cena | 2182110 | Prilikom kopiranja ugovora o projektu, ID predmeta ugovora se ponovo generiše u ugovoru o odredišnom projektu kako bi se osiguralo da je jedinstven. |
| Upravljanje mogućnostima za poslovanje | 2186741 | Dodate su validacije kako bi se osiguralo da polje **Poreklo** i **Tip transakcije** ne mogu da se ažuriraju na postojećim detaljima stavke ponude. |
| Upravljanje mogućnostima za poslovanje | 2191353 | Kontrolne tačke se ne smeju kreirati na predmetu ugovora za vreme i materijal. |
| Upravljanje mogućnostima za poslovanje | 2216956 | Rešeni su problemi sa **ažuriranjem cena**. |
| Planiranje i praćenje | 2182979 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo kopiranje stavki procene troškova iz originalnog projekta. |
| Planiranje i praćenje | 2184144 | Poboljšana je funkcija kopiranja projekta kako bi se osiguralo da se naziv položaja resursa kopira iz originalnog projekta. |
| Planiranje i praćenje | 2184799 | Kopiranje projekta: Pooštrena je kontrola kako bi se osiguralo da se procenjeni datum početka ne može promeniti dok je kopiranje u toku. |
| Planiranje i praćenje | 2185134 | Kopiranje projekta: Predviđeni datum početka odredišnog projekta postavljen je na današnji datum. |
| Planiranje i praćenje | 2196373 | Kopiranje projekta: Uverite se da se zapisi menadžera projekta i člana tima ne dupliraju u projektnom timu. |
| Planiranje i praćenje | 2211833 | Kopiranje projekta: Zadaci resursa se kopiraju iz izvornog projektnog zadatka u odredišni projekat. |
| Planiranje i praćenje | 2186541 | Rešeni su problemi u mreži **Procene** pri grupisanju po resursima. |
| Planiranje i praćenje | 2166906 | Kategorija transakcije iz zadatka mora se kopirati u entitet **Dodeljivanje resursa**. |
| Upravljanje resursima | 2125362 | Rešeni su problemi sa kreiranjem generičkog člana tima pomoću metode raspodele zasnovane na satima. |
| Vreme i trošak | 2113603 | Rešen je problem sa uklanjanjem atributa povezan sa prilagođavanjem sa stranice **Stavka vremena**. Sistem sada proverava da li atribut postoji na stranici pre nego što im pristupi pomoću skripte. |
| Vreme i trošak | 2204377 | Kopirani vremenski rasporedi moraju se automatski prikazati kada izaberete **kopiranje sedmice** tokom unosa vremena. |
| Vreme i trošak | 2209059 | Polje **Status** može da se uređuje za Dynamics 365 Field Service stavke vremena. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstva u usluzi Dynamics 365 Finance

| **Oblast funkcija** | **Referentni broj** | **Ispravka kvaliteta** |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminacija obrnute procene ne funkcioniše **Periodično**.  |
| Upravljanje projektima i računovodstvo | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funkcija **Prilagođavanje računovodstva** kreira problem sa računima glavne knjige za koje je izabrana opcija **Ne dozvoljavaj ručni unos**. |
| Upravljanje projektima i računovodstvo | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Dodata je poslovna logika za obradu faktura za korekciju, uključujući iznos zadržavanja ili primenjeni iznos zadržavanja. |
| Upravljanje projektima i računovodstvo | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP – Knjiženje prodajne vrednosti u fakturisanju projekta u okviru preduzeća bira neočekivani poslovni kontakt. |
| Upravljanje projektima i računovodstvo | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Kada radite sa obustavama u usluzi Project Operations, promena podrazumevanog projekta na ugovoru nakon fakturisanja pretplate uzrokuje kasnije probleme sa dolaznim odbicima. |
| Upravljanje projektima i računovodstvo | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | U usluzi Project Operations, uklanjanje projekta iz ugovora trebalo bi da resetuje podrazumevani projekat ugovora, ako je potrebno. |
| Upravljanje projektima i računovodstvo | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | U usluzi Project Operations, pogrešne stavke troškova prikazuju se u listi **Dodaj red** na fakturi u okviru preduzeća. |
| Upravljanje projektima i računovodstvo | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | U usluzi Project Operations, stranica **Ugovor o kupovini** nije vidljiva u pravnim licima iz oblasti finansija koja su integrisana u Project Operations. |
| Upravljanje projektima i računovodstvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Zbog greške Dataverse integracije, ne možete konvertovati ponudu kao ostvarenu u usluzi Project Operations. |
| Upravljanje projektima i računovodstvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** može da podesi adresu fakture izvora finansiranja od drugog klijenta.  |
| Upravljanje projektima i računovodstvo | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | U usluzi Project Operations aspekti se ne biraju kada kreirate fakturisanje knjiženja za transakciju. |
| Putovanje i trošak | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Bilans gotovinskog avansa se ne ažurira za izveštaj o troškovima ako je odobren i knjižen red po red. |
| Putovanje i trošak | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Porezi za detaljne izveštaje o troškovima unutar preduzeća nisu pravilno izračunati. |
| Putovanje i trošak | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Dodatna polja koja se odnose na projekte prikazuju se na ponovo zamišljenoj stranici **Izveštaji o troškovima u okviru preduzeća**. |
| Putovanje i trošak | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Na zaglavljima izveštaja o troškovima prikazuje se netačna poruka o grešci. |
| Putovanje i trošak | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Izveštaj o troškovima se pogrešno knjiži u scenariju unutar preduzeća ako se porez na promet knjiži u pravnom licu na odredištu. |
| Putovanje i trošak | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Datumi podnošenja izveštaja se ne štampaju na odobrenim izveštajima o troškovima. |
| Putovanje i trošak | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Polja **Datum odobrenja** i **Datum odbijanja** se ne popunjavaju nakon odobrenja troškova. |
| Putovanje i trošak | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Zahtev za putovanje kreiran za jednog radnika može se koristiti za izveštaj o trošku drugog radnika. |
| Putovanje i trošak | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategorije troškova zaključavaju se prilikom dodavanja nove stavke troškova. |
| Putovanje i trošak | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Stavljanje u spisak već podeljenih redova izveštaja o troškovima rezultira nepotpunim knjiženjem vaučera za dugovanja \ glavnu knjigu i raščlanjava istraživač izvora računovodstva, jer je dupliran parametar **TRVEXPTRANS.SOURCEDOCUMENTLINE**. |
| Putovanje i trošak | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Politika zahteva za putovanje ne funkcioniše kako se očekivalo. |
| Putovanje i trošak | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Ime poslovnog kontakta dobavljača se ne prikazuje u proknjiženim transakcijama projekata za izveštaje o troškovima. |
| Putovanje i trošak | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | U usluzi Project Operations ne možete odobriti vreme sa zadatkom za projekat u okviru preduzeća. |
| Putovanje i trošak | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategorija povraćaja avansa u gotovini ne ažurira bilanse avansa u gotovini kada se knjiže. |
| Putovanje i trošak | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Prodajna cena se pogrešno izračunava u izveštajima o troškovima koji su kreirani u stranoj valuti korišćenjem uvezenih transakcija kreditnom karticom i povezani su sa projektom. |
| Putovanje i trošak | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Poništavaju se entitet podataka **TrvRequisitionLine** i pridruženi jedinstveni indeks. |
| Putovanje i trošak | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Dodata je instrumentacija u generisanje **SOURCEDOCUMENTLINE**. |
| Putovanje i trošak | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Prikazuje se pogrešan nalog za knjiženje u potknjizi u scenariju unutar preduzeća ako se porez na promet knjiži u pravnom licu na odredištu. |
| Putovanje i trošak | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | U usluzi Project Operations, procene troškova se ne brišu iz usluge Finance kada se brišu iz platforme Dataverse. |
| Putovanje i trošak | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kada je kategorija troškova kategorija koja nije projekat, finansijski aspekti izabrani na stranici **Trošak** se ne kopiraju u izveštaj o troškovima. |
