---
title: Troškovi dnevnica
description: Ovaj članak pruža informacije o načinu rada sa troškovima za dnevnice.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923205"
---
# <a name="per-diem-expenses"></a>Troškovi dnevnica

> [!IMPORTANT] 
> Funkcionalnost koja je opisana u ovom članku dostupna je ciljanim korisnicima kao deo izdanja verzije za pregled.

Isplata dnevnice je fiksni, unapred određeni dnevni dodatak koji preduzeće plaća svojim zaposlenima za smeštaj (hotele), obroke i druge slučajne troškove koje ti zaposleni snose dok putuju zbog posla. Preduzeće plaća ovu naknadu zaposlenima umesto da plaća stvarne putne troškove. Zaposleni mogu da koriste svoje naknade dnevnica za **Slučajne/druge troškove** za pokrivanje napojnica, posluge u sobi, pranja veša ili usluga hemijskog čišćenja za važne poslovne sastanke. Iznos dnevnica može da varira, u zavisnosti od toga da li poslodavac odluči da nadoknadi kombinovane troškove smeštaja i obroka, ili samo troškove obroka i slučajne troškove.

Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje. Kada kreirate pravilo za dnevnicu, možete da odredite da se procenat iznosa dnevnice zadržava ako zaposleni dobije besplatne obroke ili usluge. Takođe možete da odredite minimalni broj sati i maksimalni broj sati za koje iznos dnevnice može da se primeni na putovanje zaposlenog.

Dnevnice se izračunavaju kao ukupna naknada koje se nudi po danu minus smanjenja za obroke (trošak besplatnih obroka) koji se obezbeđuje zaposlenom.

## <a name="configure-per-diems"></a>Konfigurisanje dnevnica

Da biste konfigurisali troškove dnevnica, pratite ove korake.

1. Idite na **Upravljanje troškovima** \> **Instalacija** \> **Opšti podaci** \> **Parametri upravljanja troškovima**.
2. Na kartici **Dnevnice**, u polju **Izračunaj smanjenje obroka za** izaberite kako treba izračunati dnevnice:

    - **Vrsta obroka po putovanju** – Izračunajte dnevnice na osnovu vrste obroka koji se unosi (doručak, ručak ili večera) i na smanjenju obroka koji je naveden za svaku vrstu obroka za naknadu dnevnica tokom trajanja putovanja.
    - **Vrsta obroka po danu** – Izračunajte dnevnice na osnovu vrste obroka koji se unosi i na smanjenju obroka koji je naveden za svaku vrstu obroka za naknadu dnevnica po danu.
    - **Broj obroka dnevno** – Izračunajte dnevnicu na osnovu broja obroka koji se unose dnevno i na smanjenju obroka za broj obroka koji se obezbeđuju svakog dana.

3. Idite na **Upravljanje troškovima** \> **Konfigurisanje** \> **Izračunavanja i šifre** \> **Lokacije dnevnica**.
4. Dodajte lokacije na kojima se mogu koristiti dnevnice.
5. Za svaku lokaciju koju dodate, na kartici **Dnevnice** izaberite iznos dnevnice i valutu koje važe između određenog datuma početka i završetka za boravak, obroke i ostale troškove. Da biste konfigurisali iznose dnevnica i valute, idite na **Upravljanje troškovima** \> **Konfiguracija** \> **Izračunavanja i šifre** \> **Dnevnice**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice u redizajniranom interfejsu troškova

Funkcija dnevnice je podržana u redizajniranom radnom prostoru **Upravljanje troškovima** u usluzi Microsoft Dynamics 365 Finance u verziji 10.0.25 i novijoj.

Da biste omogućili dnevnice, pratite ove korake.

1. U radnom prostoru **Upravljanje funkcijama** pronađite i na listi izaberite funkciju **Redizajn izveštaja o troškovima**, a zatim izaberite **Omogući odmah**.
2. Pronađite i izaberite funkciju **Redizajn interfejsa izveštaja o dnevnicama za troškove**, a zatim izaberite **Omogući odmah**.

## <a name="how-the-feature-works"></a>Kako funkcioniše funkcija

Ovaj odeljak pruža primere za tri scenarija konfiguracije. U svakom primeru, polje **Izračunaj umanjenje za obroke za** je postavljeno na drugu vrednost. Za sva tri primera, ukupan iznos koji se isplaćuje je isti dok se ne primeni umanjenje za obroke. Nakon toga, ukupan iznos za isplatu se razlikuje za svaki primer.

Da biste kreirali trošak dnevnice koje se koriste za sva tri primera, pratite ove korake.

1. Idite na **Radni prostori** \> **Upravljanje troškovima**.
2. Izaberite **Novi izveštaj o troškovima** ili izaberite postojeći izveštaj o troškovima.
3. Dodajte novi trošak. U polju **Kategorija**, izaberite **Dnevnica**. Izaberite lokaciju, te datume početka i završetka putovanja. Dnevnica za smeštaj, obroke i slučajne troškove (ostale troškove) se izračunava na osnovu dnevne naknade koja je postavljena za izabranu lokaciju.

    Na primer, kao lokaciju birate **Redmond (SAD)**. Dnevna naknada za tu lokaciju je 150 američkih dolara (150 USD) za smeštaj, 75 USD za obroke i 5 USD za slučajne troškove. Datum početka je 10. januar, a datum završetka je 14. januar. Stoga, izabrano trajanje je pet dana kada je izabrana konfiguracija kalendarski dani sa vremenom, a izabrano vreme počinje i završava se u 12:00 časova na datum početka i završetka. Evo izračunavanja:

    - Ukupan naplativi iznos = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Obrok i slučajni deo ukupne količine = 5 × (75 + 5) = 400 USD

Ako su tokom putovanja obezbeđeni doručak, ručak i večera, ti obroci moraju biti uzeti u obzir za umanjenje za obrok.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1. primer: Dnevnice gde se umanjenje za obrok zasniva na vrsti obroka po putovanju

U ovom primeru, umanjenje za obrok je 30 procenata za doručak, 30 procenata za ručak i 40 procenata za večeru. Na stranici **Parametri upravljanja troškovima**, polje **Izračunaj umanjenje za obroke za** postavljeno je na **Vrstu obroka po putovanju**. Evo izračunavanja ako su zaposlenom obezbeđena tri doručka, dva ručka i nula večera:

- Umanjenje za obrok = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Obroci i slučajni troškovi = 400 – 112,50 = 287,50 USD
- Ukupan naplativi iznos = Ukupna naknada – umanjenje za obrok = 1.150 – 112,50 = 1.037,50 USD

![Trošak dnevnice gde se umanjenje za obrok zasniva na vrsti obroka po putovanju.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2. primer: Dnevnice gde se umanjenje za obrok zasniva na vrsti obroka po danu

U ovom primeru, umanjenje za obrok je 30 procenata za doručak, 30 procenata za ručak i 40 procenata za večeru. Na stranici **Parametri upravljanja troškovima**, polje **Izračunaj umanjenje za obroke za** postavljeno je na **Vrstu obroka po danu**. U ovom slučaju, u matrici koordinatne mreže **Obroci** u dijalogu **Uređivanje troškova** opozovite izbor u poljima za potvrdu da biste naznačili koji obroci su vam obezbeđeni tokom putovanja.

Na primer, evo izračunavanja ako je doručak obezbeđen prva tri dana putovanja:

- Dnevno umanjenje za obrok za svaki od prva tri dana = 75 × 30% = 22,50 USD
- Ukupno umanjenje za obrok = 3 × 22,50 = 67,50 USD
- Obroci i slučajni troškovi za dane od 1 do 3 = 75 – 22,50 = 57,50 USD
- Ukupno za obroke i slučajne troškove = Zbir obroka i slučajnih troškova tokom pet dana = 400 – 67,50 = 332,50 USD
- Ukupan naplativi iznos = Ukupan iznos – umanjenje za obrok = 1.150 – 67,50 = 1.082,50 USD

![Trošak dnevnice gde se umanjenje za obrok zasniva na vrsti obroka po danu.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3. primer: Dnevnice gde se umanjenje za obrok zasniva na broju obroka po danu

U ovom primeru, umanjenje za obroke se izračunava na osnovu broja obroka koji su obezbeđeni po danu (to jest, polje **Izračunaj umanjenje za obrok za** na stranici **Parametri upravljanja troškovima** postavljeno je na **Broj obroka dnevno**). U matrici koordinatne mreže **Obroci** u dijalogu **Uređivanje troškova** opozovite izbor u poljima za potvrdu da biste naznačili koji obroci su vam obezbeđeni.
U ovom slučaju, umanjenje za obrok se zasniva samo na broju obezbeđenih obroka, a ne na vrsti obroka (doručak/ručak/večera) koji je obezbeđen.

Evo izračunavanja za dnevnice kada je dnevna naknada 150 USD za smeštaj, 75 USD za obroke i 5 USD za slučajne troškove:

- **Ukupan naplativi iznos** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Jedan obrok:** Umanjenje za obrok = 20% = 15 USD
- **Dva obroka:** Umanjenje za obrok = 50% = 37,50 USD
- **Tri obroka:** Umanjenje za obrok = 100% = 75 USD

Evo izračunavanja za **obroke i dodatke za slučajne troškove**, što uključuje 5 USD za slučajne troškove:

- 1. dan – Dva obezbeđena obroka = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 2. dan – Dva obezbeđena obroka = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 3. dan – Jedan obezbeđeni obrok = (75 – 15) + 5 = 60 + 5 = 65 USD
- 4. dan – Nula obezbeđenih obroka = (75 – 0) + 5 = 75 + 5 = 80 USD
- 5. dan – Tri obezbeđena obroka = (75 – 75) + 5 = 0 + 5 = 5 USD

- Ukupno za obroke i slučajne troškove = Obroci i slučajni troškovi za 1. dan + 2. dan + 3. dan + 4. dan + 5. dan = 235 USD
- Ukupno umanjenje za obrok = Umanjenje za obrok za 1. dan + 2. dan + 3. dan + 4. dan + 5. dan = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Ukupan naplativi iznos = Ukupna naknada – Ukupno umanjenje za obrok = 1.150 USD – 165 USD = 985 USD

![Trošak dnevnice gde se umanjenje za obrok zasniva na broju obroka po danu.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verzije Finansija 10.0.23, ako koristite redizajnirani interfejs za troškove, ne možete da kreirate troškove za dnevnice u kojima se datumi preklapaju. Ako pokušate, dobićete poruku o grešci.
