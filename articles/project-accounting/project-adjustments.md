---
title: Korekcije projekta
description: Ovaj članak pruža informacije o korekcijama projekta.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788373"
---
# <a name="project-adjustments"></a>Korekcije projekta

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

## <a name="adjustments-overview"></a>Pregled korekcija

Korporaciju Microsoft možete da Dynamics 365 Project Operations konfigurišete tako da korisnici mogu da menjaju proknjižene transakcije. Transakcije projekta možete korigovati pojedinačno ili možete izabrati više transakcija istovremeno na listi svih projektnih transakcija. Korekcije projekta se koriste, na primer, za masovno ažuriranje statusa naplate, ponovno izračunavanje troškova nakon promene konfiguracije ili ažuriranje izvora finansiranja.

Korisnici mogu da pristupe funkcionalnosti prilagođavanja projekta na nekoliko načina:

- Korišćenjem stranice " **Prilagođavanje transakcija** " kojoj se može pristupiti iz prozora "Upravljanje **projektima" i "Podešavanje računovodstva** \> **"**.
- Korišćenjem dugmeta " **Korekcija** " na stranici **"Proknjižene transakcije projekta** " kojoj se može pristupiti iz upravljanja **projektima i računovodstvenih** \> **transakcija**.
- Korišćenjem dugmeta **"** Korekcija" **na stranici "Proknjižene** transakcije projekta" u kontekstu projekta. Ovoj stranici se može pristupiti iz projektnog **menadžmenta i knjigovodstva** \> **Svi projekti**.

Da biste dozvolili korekcije, morate omogućiti jedan ili više statusa transakcija iz upravljanja projektima i knjigovodstvenih projekata i računovodstvenih paramatera na kartici **Opšte** \> **postavke u odeljku Dozvoli korekciju**  **statusa transakcije** . **·** Primeri statusa transakcija uključuju proknjižene transakcije, fakturisane transakcije ili eliminisane transakcije. Svaki status transakcije koji je postavljen na "Ne **"** imaće transakcije u tom statusu koje se neće pojaviti u okviru procesa korekcije kao što je moguće izabrati za korekciju.

Opcija konfiguracije koja je nazvana "Uvek **kreiraj transakciju korekcije"** trenutno je dostupna u parametrima upravljanja projektima i računovodstva. Ovu opciju možete onemogućiti da biste ažurirali originalnu transakciju umesto da kreirate nove transakcije tokom korekcije u podskupu scenarija. Najavljeno je da će ovaj parametar biti depreciran do 1. marta 2023. godine. Posle 1. marta 2023. godine, sistem će se uvek ponašati kao da je opcija omogućena.

## <a name="adjustments-process-flow"></a>Posagađivanja procesa protoka

Sledeći koraci prikazuju tipičan tok za korekcije obrade.

1. Otvorite stranicu **"Prilagođavanja** projekta".
2. Izaberite **opciju** Izaberite da biste potražili transakcije koje zadovoljavaju očekivane kriterijume za korekciju.
3. Sa liste transakcija izaberite sve transakcije ili podskup transakcija za korekciju.
4. Izaberite **stavku** Prilagodi i izmenite atribute u redu. Druga mogućnost je da, ako su vrednosti ručno navedene tokom stavke transakcije, možete izabrati da unesete podrazumevane sistemske vrednosti.
5. Lista transakcija se vraća, a potvrdni znak se pojavljuje u koloni korekcije na **čekanju da bi** se označilo gde su izvršene promene. Sve korekcije koje imaju neobrađene promene prikazane su u donjoj polovini stranice. Tamo možete izvršiti dodatne detaljne promene izvan onoga što je prikazano na prethodnoj stranici.
6. Izaberite **stavku Proknjiži** da biste proknjižili transakcije korekcije.

U zavisnosti od konfiguracije, za korekciju se obično kreiraju nove transakcije.

- Polje **Status fakture** originalne transakcije je podešeno na "Korigovano **"**.
- Transakcija storniranja se kreira da bi se storniranje originalne transakcije, a polje **Status** je podešeno na "Korigovano **"**.
- Kreirana je nova transakcija koja ima promene koje su izvršene tokom procesa korekcije.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Biranje više proknjiženih projektnih transakcija istovremeno za korekcije i kreditne napomene

Nova funkcija koja je uvedena u izdanju 10.0.30 omogućava izbor više transakcija za korekciju u isto vreme sa **stranice Proknjižene transakcije** projekta.

Da biste mogli da koristite ovu funkciju, ona mora biti omogućena u sistemu. Administratori mogu da koriste **radni prostor** za upravljanje funkcijama da bi proverili status funkcije i omogućili je ako je to potrebno. U radnom **prostoru za upravljanje** funkcijama potražite i izaberite **proknjižene transakcije proknjiženog projekta za korekcije i kreditne napomene, a** zatim izaberite omogući **odmah**.

Ova funkcija omogućava funkcionalnost sledećeg ključa:

- Njemu se može pristupiti sa stranice proknjižene transakcije u okviru projekta pomoću postojećeg dugmeta " **Korekcija** ".
- Omogućava kontrolu izbora u više redova na stranici "Proknjižene **transakcije projekta** ". Filtere možete primeniti na stranicu liste i izabrati zapise pre nego što počnete sa podešavanjima.
- Onemogućava dugme "Korekcija **" ako** nijedna transakcija ne može da se koriguje ili ako izaberete kombinaciju kreditnih napomena i naloga zajedno umesto pojedinačno.
- Zbog dodavanja kontrole izbora u više redova, **veza "Posvećeni trošak** " na glavnoj traci više neće biti onemogućena ako je izabrano više redova.
- Dodaje sledeću poruku upozorenja: "Izabrali ste više od (izabranih brojeva) zapisa za korekciju. Nastavak ove akcije može potrajati neko vreme. Želite li zaista da nastavite sa ovom akcijom?"

Ova funkcija takođe uklanja korak 2 iz toka procesa koji je opisan ranije u ovom članku. Zbog toga će sve transakcije koje su izabrane pre nego što je stranica **"Prilagođavanje** transakcija" otvorena biti uključene u listu transakcija za korekciju. Ne morate da koristite dugme "Izaberi" **da** biste ih potražili.

> [!NOTE] 
> Čak i ako je ova funkcija onemogućena, i dalje možete da izaberete više zapisa za podešavanje. Međutim, ostaće izabran samo jedan zapis *, a* dijalog **"Izbor transakcija** " će se pojaviti odmah nakon što izaberete da otvorite korekcije.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Korekcija statusa transakcije koji se mogu omogućiti ili onemogućiti za korekcije

Sledeći statusi se mogu omogućiti ili onemogućiti na kartici Opšte **postavke stranice** Upravljanje **projektima i računovodstveni parametri** :

- Objavljeno
- Predlog fakture
- Fakturisano
- Procenjeno
- Eliminisan
- Početni saldo (čas)

## <a name="adjustment-parameters"></a>Parametri podešavanja

Ovi parametri su navedeni na stranici **"Upravljanje projektnim i računovodstvenim parametrima** " na **kartici "Opšte**  **postavke" u okviru grupe "Podešavanje** " i izmeniće ponašanje načina obrade korekcija. 

| Naziv parametra | Opis |
|----------------|-------------
| Uvek kreiraj transakciju korekcije | Ako je ovaj parametar omogućen, proces korekcije će uvek kreirati novu transakciju storekta i novu korigovanu transakciju kada postoji finansijski ili izveštajni uticaj. Ako je parametar onemogućen, proces korekcije će ažurirati originalnu transakciju umesto kreiranja storniranja i nove transakcije za scenario kao što je ažuriranje teksta transakcije. |
| Polje automatskog označavanja | Ako je ovaj parametar omogućen, sistem će ponovo obračunati cenu troška i prodajnu cenu. |
| Koristi datum korekcije kao novi projekat | Ovaj parametar se koristi za premeštanje transakcija u buduću fiskalni period što je sistem podržao ovu funkciju. Ne preporučujemo da ga koristite jer menja datum poslovanja transakcije i biće zaprećen u budućem izdanju. |
| Dozvoli zatvorene aktivnosti | Obično nije moguće kreirati transakcije za zatvorene aktivnosti. Ako je ovaj parametar omogućen, to ponašanje je zamenjeno. Zbog toga se mogu kreirati korekcije za zatvorene aktivnosti. |
