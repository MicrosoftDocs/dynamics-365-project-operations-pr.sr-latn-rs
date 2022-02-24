---
title: Dnevnik integracije u usluzi Project Operations
description: Ova tema pruža informacije o radu sa dnevnikom integracije u usluzi Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a5f4d524530594bd3118f9b320acf4033c5d503
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948347"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracije u usluzi Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke vremena i troškova kreiraju transakcije **stvarnih vrednosti** koje predstavljaju operativni prikaz na posao završen u odnosu na projekat. Dynamics 365 Project Operations pruža računovođama alat za pregled transakcija i prilagođavanje računovodstvenih atributa po potrebi. Nakon završetka pregleda i prilagođavanja, transakcije se knjiže u potknjigu projekta i u glavnu knjigu. Računovođa može da obavlja ove aktivnosti koristeći dnevnik **Project Operations integracija** (**Dynamics 365 Finance** > **Upravljanje projektima i računovodstvo** > **Dnevnici** > **Project Operations integracija**.

![Tok dnevnika integracije](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kreiranje zapisa u dnevniku integracije u usluzi Project Operations

Zapisi u Project Operations dnevniku integracije kreiraju se periodičnim postupkom, **Uvoz iz pripremne tabele**. Možete pokrenuti ovaj postupak tako što ćete otići na **Dynamics 365 Finance** > **Upravljanje projektima i računovodstvo** > **Periodično** > **Project Operations integracija** > **Uvoz iz pripremne tabele**. Proces možete pokrenuti interaktivno ili po potrebi konfigurisati postupak da se pokreće u pozadini.

Kada se periodični proces pokrene, pronađu se sve stvarne vrednosti koje još nisu dodate u dnevnik integracije u usluzi Project Operations. Kreira se stavka u glavnoj knjizi za svaku stvarnu transakciju.
Sistem grupiše stavke u glavnoj knjizi u zasebne dnevnike na osnovu vrednosti izabrane u polju **Jedinica perioda u dnevniku integracije u usluzi Project Operations** (**Finansije** > **Upravljanje projektima i računovodstvo** > **Podešavanje** > **Parametri upravljanja projektom i računovodstva**, kartica **Project Operations u usluzi Dynamics 365 Customer Engagement**). Moguće vrednosti za ovo polje uključuju:

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

Stavka u glavnoj knjizi integracije se mogu izbrisati, ali sve neobjavljene stavke će se ponovo umetnuti u dnevnik nakon ponovnog pokretanja periodičnog procesa **Uvoz iz pripremne tabele**.

Kada objavite dnevnik integracije, kreiraju se transakcije potknjige i glavne knjige projekta. One se koriste u posledičnom fakturisanju klijenata, priznavanju prihoda i finansijskom izveštavanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]