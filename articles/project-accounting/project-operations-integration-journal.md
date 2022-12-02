---
title: Dnevnik integracije u usluzi Project Operations
description: Ovaj članak pruža informacije o radu sa dnevnikom integracije u usluzi Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541095"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracije u usluzi Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke vremena, troškova, naknade i materijala kreiraju transakcije **Stvarnih vrednosti** koje predstavljaju operativni prikaz na posao završen u odnosu na projekat. Dynamics 365 Project Operations pruža računovođama alat za pregled transakcija i prilagođavanje računovodstvenih atributa po potrebi. Nakon završetka pregleda i prilagođavanja, transakcije se knjiže u potknjigu projekta i u glavnu knjigu. Računovođa može da obavlja ove aktivnosti koristeći dnevnik **Project Operations integracija** (dnevnik **Dynamics 365 Finance** > **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Project Operations integracija**).

![Tok dnevnika integracije.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kreiranje zapisa u dnevniku integracije u usluzi Project Operations

Zapisi u Project Operations dnevniku integracije kreiraju se periodičnim postupkom, **Uvoz iz pripremne tabele**. Možete pokrenuti ovaj proces tako što ćete otići na **Dynamics 365 Finance** > **Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations integracija** > **Uvoz iz pripremne tabele**. Proces možete pokrenuti interaktivno ili po potrebi konfigurisati postupak da se pokreće u pozadini.

Kada se periodični proces pokrene, pronađu se sve stvarne vrednosti koje još nisu dodate u dnevnik integracije u usluzi Project Operations. Kreira se stavka u glavnoj knjizi za svaku stvarnu transakciju.
Sistem grupiše stavke u glavnoj knjizi u zasebne dnevnike na osnovu vrednosti izabrane u polju **Jedinica perioda u dnevniku integracije u usluzi Project Operations** (**Finance** > **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstva**, kartica **Project Operations u usluzi Dynamics 365 Customer Engagement**). Moguće vrednosti za ovo polje uključuju:

  - **Dani**: Stvarne vrednosti su grupisane prema datumu transakcije. Zaseban dnevnik se kreira za svaki dan.
  - **Meseci**: Trenutno stanje je grupisano prema kalendarskom mesecu. Zaseban dnevnik se kreira za svaki mesec.
  - **Godine**: Trenutno stanje je grupisano prema kalendarskoj godini. Zaseban dnevnik se kreira za svaku godinu.
  - **Sve**: Sve transakcije trenutnog stanja su uključene u isti dnevnik integracije. Ako dnevnik nije dostupan kada se periodični proces izvodi, na primer ako je dnevnik u procesu knjiženja transakcija, kreira se novi dnevnik.

Stavke u glavnoj knjizi se kreiraju na osnovu stvarnih podataka o projektu. Sledeća lista uključuje neka značajnija pravila podrazumevanja i transformacije:

  - Svaka stvarna transakcija projekta ima red u dnevniku integracije u usluzi Project Operations. Transakcije troškova i nenaplaćene prodaje za vreme i vrstu naplate materijala prikazane su u zasebnim redovima.
  - Polje **Datum** predstavlja datum transakcije. Polje **Datum računovodstva** predstavlja datum evidentiranja transakcije u glavnu knjigu. Ako je datum računovodstva u [zatvorenom finansijskom periodu](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), a parametar **Automatski podesi datum obračuna na otvoreni period glavne knjige** je postavljen na kartici **Finansije** na stranici **Parametri upravljanja projektom i računovodstvom**, sistem će prilagoditi datum računovodstva transakcije prvom datumu u narednom otvorenom periodu glavne knjige.
  - Polje **Vaučer** prikazuje broj vaučera za svaku stvarnu transakciju. Sekvenca brojeva vaučera se definiše na kartici **Sekvence brojeva** na stranici **Parametri upravljanja projektom i računovodstvom**. Svakom redu se dodeljuje novi broj. Kada se objavi vaučer, možete videti kako su povezani troškovi i transakcije nenaplaćene prodaje ako izaberete **Povezani vaučeri** na stranici **Transakcija vaučera**.
  - Polje **Kategorija** predstavlja projektnu transakciju i podrazumevane vrednosti na osnovu kategorije transakcije za povezanu stvarnu vrednost projekta.
    - Ako se **Kategorija transakcije** postavi u stvarnu vrednost projekta a povezana **Kategorija projekta** postoji u datom pravnom licu, podrazumevana vrednost kategorije je kategorija ovog projekta.
    - Ako **Kategorija transakcije** nije postavljena u stvarnoj vrednosti projekta, sistem koristi vrednost u polju **Podrazumevane kategorije projekata** na kartici **Project Operations u usluzi Dynamics 365 Customer Engagement** na stranici **Parametri upravljanja projektom i računovodstvo**.
  - Polje **Resurs** predstavlja resurs projekta koji se odnosi na ovu transakciju. Resurs se koristi kao referenca u predlozima klijentima za projektne fakture.
  - Polje **Kurs valute** uzima podrazumevane vrednosti iz skupa **Kursna lista za valute** u usluzi Dynamics 365 Finance. Ako podešavanje deviznog kursa nedostaje, periodični proces **Uvoz iz pripremne tabele** neće dodati zapis u dnevnik, a poruka o grešci će biti dodata u dnevnik izvršavanja posla.
  - Polje **Svojstvo stavke** predstavlja tip naplate u trenutnom stanju projekta. Mapiranje svojstava linije i vrste obračuna definisano je na kartici **Project Operations u usluzi Dynamics 365 Customer Engagement** na stranici **Parametri upravljanja projektom i računovodstvom**.

Samo se sledeći računovodstveni atributi mogu ažurirati u stavkama u glavnoj knjizi Project Operations integracije:

- **Grupa za naplatu poreza na promet** i **Grupa za porez na promet stavki na računu**
- **Finansijske dimenzije** (pomoću radnje **Raspodeli iznose**)

Integracije stavki u glavnoj knjizi se mogu izbrisati. Međutim, sve neobjavljene stavke će se ponovo umetnuti u dnevnik nakon ponovnog pokretanja periodičnog procesa **Uvoz iz pripremne tabele**.

### <a name="post-the-project-operations-integration-journal"></a>Knjiženje dnevnika integracije za Project Operations

Kada objavite dnevnik integracije, kreiraju se transakcije potknjige i glavne knjige projekta. One se koriste u posledičnom fakturisanju klijenata, priznavanju prihoda i finansijskom izveštavanju.

Izabrani dnevnik integracije za Project Operations može biti proknjižen koristeći **Knjiži** na stranici dnevnika integracije za Project Operations. Svi dnevnici se mogu automatski proknjižiti pokretanjem procesa **Periodično** > **Project Operations integracija** > **Proknjiži integraciju dnevnika za Project Operations**.

Knjiženje se može izvršiti interaktivno ili u grupi. Imajte u vidu da će svi dnevnici koji imaju više od 100 redova automatski biti proknjiženi u grupi. Za bolje performanse kada se dnevnici koji imaju mnogo redova knjiže u grupi, omogućite funkciju **Proknjiži dnevnik integracija za Project Operations koristeći više grupnih zadataka** u radnom prostoru **Upravljanje funkcijama**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Prenos svih redova koji imaju greške prilikom knjiženja u novi dnevnik

> [!NOTE]
> Da biste koristili ovu mogućnost, omogućite **Prenos svih redova sa greškama u knjiženju u novi dnevnik integracije za Project Operations** u radnom prostoru **Upravljanje funkcijama**.

Ova funkcija pomaže u poboljšanju iskustva u dnevniku integracije za Project Operations. Kada je omogućeno, problemi sa dvostrukim upisivanjem i problemi sa podešavanjem više ne sprečavaju knjiženje važećih dnevnika. Tokom knjiženja u dnevnik integracije za Project Operations, sistem proverava ispravnost svakog reda u dnevniku. Knjiži sve redove koji nemaju greške i kreira novi dnevnik za sve redove koji imaju greške u knjiženju.

Da biste pregledali dnevnike koji imaju redove sa greškom prilikom knjiženja, idite u **Upravljanje projektima i računovodstvo** \> **Dnevnici** \> **Dnevnik integracije za Project Operations** i filtrirajte listu dnevnika koristeći polje **Originalni dnevnik**. Sledeća ilustracija prikazuje primer gde su na ovaj način filtrirani dnevnici na stranici **Dnevnik integracije za Project Operations**.

![Originalni dnevnik prikazan na stranici Dnevnik integracije za Project Operations.](./media/transferLines-originalJournal.png)

Ako je periodična grupna obrada konfigurisana za knjiženje dnevnika integracije, knjiženje će biti ponovo pokušano, a dnevnici će biti proknjiženi ako je problem tokom vremena rešen. Sve preostale dnevnike treba ručno istražiti pregledom evidencija i preduzimanjem bilo koje potrebne radnje.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
