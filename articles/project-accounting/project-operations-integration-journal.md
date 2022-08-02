---
title: Dnevnik integracije u usluzi Project Operations
description: Ovaj članak pruža informacije o radu sa nalogom za integraciju u operacijama projekta.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106292"
---
# <a name="integration-journal-in-project-operations"></a>Dnevnik integracije u usluzi Project Operations

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke vremena, troškova, naknade i materijala kreiraju **stvarne** transakcije koje predstavljaju operativni prikaz dovršenog rada u odnosu na projekat. Dynamics 365 Project Operations pruža računovođama alat za pregled transakcija i prilagođavanje računovodstvenih atributa po potrebi. Nakon završetka pregleda i prilagođavanja, transakcije se knjiže u potknjigu projekta i u glavnu knjigu. Knjigovođa može da obavlja ove aktivnosti koristeći nalog **za integraciju** operacija projekta (**Dynamics 365 Finance** > **Nalog za upravljanje i knjigovodstvene** > **naloge** > **projektnih operacija integracije**.

![Tok dnevnika integracije.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Kreiranje zapisa u dnevniku integracije u usluzi Project Operations

Zapisi u Project Operations dnevniku integracije kreiraju se periodičnim postupkom, **Uvoz iz pripremne tabele**. Ovaj proces možete pokrenuti tako što ćete iz **pripremne tabele Dynamics 365 Finance** > **upravljanje i knjigovodstvene** > **·** > **periodične integracije projektnih** > **operacija**. Proces možete pokrenuti interaktivno ili po potrebi konfigurisati postupak da se pokreće u pozadini.

Kada se periodični proces pokrene, pronađu se sve stvarne vrednosti koje još nisu dodate u dnevnik integracije u usluzi Project Operations. Kreira se stavka u glavnoj knjizi za svaku stvarnu transakciju.
Sistem grupira redove naloga u posebne naloge **na osnovu** vrednosti izabrane u jedinici perioda u polju "Integracija projektnih **operacija" (** > **Upravljanje projektima** > **·** > **finansija** i parametri obračunskog podešavanja projekta i računovodstveni parametri **,** Operacije projekta na Dynamics 365 Customer Engagement kartici). Moguće vrednosti za ovo polje uključuju:

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
    - Ako **kategorija transakcije** nije postavljena u stvarnom projektu, sistem koristi vrednost u **polju Podrazumevane vrednosti kategorije projekta** **na kartici "Operacije projekta" na kartici Dynamics 365 Customer Engagement na** **stranici "Upravljanje projektima i računovodstvenim parametrima**".
  - Polje **Resurs** predstavlja resurs projekta koji se odnosi na ovu transakciju. Resurs se koristi kao referenca u predlozima klijentima za projektne fakture.
  - Podrazumevane **vrednosti polja** kursa valute iz **kursa valute** postavljene u Dynamics 365 Finance. Ako podešavanje deviznog kursa nedostaje, periodični proces **Uvoz iz pripremne tabele** neće dodati zapis u dnevnik, a poruka o grešci će biti dodata u dnevnik izvršavanja posla.
  - Polje **Svojstvo stavke** predstavlja tip naplate u trenutnom stanju projekta. Svojstvo reda i mapiranje vrste naplate definisani su **na kartici "Operacije projekta Dynamics 365 Customer Engagement na** **stranici "Upravljanje projektima i računovodstveni parametri**".

Samo se sledeći računovodstveni atributi mogu ažurirati u stavkama u glavnoj knjizi Project Operations integracije:

- **Grupa za naplatu poreza na promet** i **Grupa za porez na promet stavki na računu**
- **Finansijske dimenzije** (pomoću radnje **Raspodeli iznose**)

Redovi naloga integracije se mogu izbrisati. Međutim, svi neproknjiženi redovi će ponovo biti umetnuti u nalog nakon što ponovo pokrenite periodični **proces** uvoza.

### <a name="post-the-project-operations-integration-journal"></a>Knjiženje naloga integracije operacija projekta

Kada objavite dnevnik integracije, kreiraju se transakcije potknjige i glavne knjige projekta. One se koriste u posledičnom fakturisanju klijenata, priznavanju prihoda i finansijskom izveštavanju.

Izabrani nalog integracije operacija projekta može biti proknjižen pomoću funkcije "Proknjiži" **na stranici** "Integracija operacija projekta". Svi nalozi se mogu automatski proknjižiti pokretanjem procesa u periodičnoj integraciji **operacija projekta** > **Proknjiži integraciju** > **projektnih operacija**.

Knjiženje se može izvršiti interaktivno ili u grupi. Imajte na kraju da će svi nalozi koji imaju više od 100 redova automatski biti proknjiženi u grupi. Za bolje performanse kada se nalozi koji imaju mnogo redova knjiže u grupi, omogućite nalog **integracije operacija projekta koristeći više funkcija grupnih zadataka** u **radnom prostoru za upravljanje** funkcijama. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Prenos svih redova koji imaju greške prilikom knjiženja u novi nalog

> [!NOTE]
> Da biste koristili ovu mogućnost, omogućite prenos svih **redova sa greškama u knjiženju u novu funkciju naloga integracije operacija** projekta u radnom **prostoru za** upravljanje funkcijama.

Tokom knjiženja u nalog integracije operacija projekta, sistem proverava valjanost svakog reda u nalogu. Sistem knjiži sve redove koji nemaju greške i kreira novi nalog za sve redove koji imaju greške u knjiženju. Da biste pregledali naloge koji imaju redove greške prilikom knjiženja, idite u **nalog** > **za integraciju projektnih** > **operacija upravljanja** projektima i filtrirajte naloge **korišćenjem polja Nalog original**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
