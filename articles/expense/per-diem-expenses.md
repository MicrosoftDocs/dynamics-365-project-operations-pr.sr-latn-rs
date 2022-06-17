---
title: Troškovi dnevnica
description: Ovaj članak pruža informacije o načinu rada sa troškovima dnevnice.
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
> Funkcionalnost opisana u ovom članku dostupna je ciljanim korisnicima kao deo izdanja za pregled.

Isplata dnevnice je fiksni, unapred određeni dnevni dodatak koji kompanija plaća svojim zaposlenima za smeštaj (hotele), obroke i incidentne troškove koje ti zaposleni snose dok putuju zbog posla. Preduzeće plaća ovaj džeparac zaposlenima umesto da plaća stvarne putne troškove. Zaposleni mogu da koriste svoj **Incidentls/Other** per diem džeparac za pokrivanje saveta, posluge u sobi, pranja veša ili usluga hemijskog čišćenja za važne poslovne sastanke. Stopa dnevnica može da varira, u zavisnosti od toga da li poslodavac odluči da nadoknadi kombinovane troškove smeštaja i obroka, ili samo za troškove obroka i incidenata.

Iznosi dnevnica mogu se zasnivati na dobu godine, lokaciji putovanja ili oboje. Kada kreirate pravilo dnevnice, možete navesti da će procenat po stopi dnevnice biti uskraćen ako zaposleni dobija besplatne obroke ili usluge. Takođe možete podesiti minimalan broj časova i maksimalan broj časova tokom kojih se stopa dnevnica može primeniti na putovanje zaposlenog.

Dnevnice se izračunavaju kao ukupan džeparac koji se nudi po danu minus smanjenja obroka (trošak besplatnih obroka) koji se obezbeđuje zaposlenom.

## <a name="configure-per-diems"></a>Konfiguriši dnevnice

Da biste konfigurisali troškove dnevnice, sledite ove korake.

1. Idite na parametre **upravljanja** \> **troškovima** \> **Opšteg** \> **upravljanja troškovima.**
2. Na kartici **Dnevnice**, u polju **Izračunaj smanjenje obroka** po polju izaberite kako dnevnice treba izračunati:

    - **Vrsta obroka po putovanju** – Izračunajte dnevnice na osnovu vrste obroka koji se unosi (doručak, ručak ili večera) i na smanjenju obroka koji je naveden za svaku vrstu obroka za dnevnica tokom trajanja putovanja.
    - **Vrsta obroka dnevno** – Izračunajte dnevnice na osnovu vrste obroka koji se unosi i na smanjenju obroka koji je naveden za svaku vrstu obroka za dnevnice dnevno.
    - **Broj obroka dnevno** – Izračunajte dnevnici na osnovu broja obroka koji se unose dnevno i na smanjenju obroka za broj obroka koji se obezbeđuju svakog dana.

3. Idite na **obračune podešavanja** \> **·** \> **upravljanja troškovima i** \> **šifre po lokacijama dnevnice.**
4. Dodajte lokacije na kojima se mogu koristiti dnevnice.
5. Za svaku lokaciju koju dodate, na kartici **Dnevnice izaberite** stopu dnevnica i valutu koje važe između određenih datuma početka i završetka za smeštaj, obroke i druge troškove. Da biste konfigurisali stope dnevnice i valute, idite na obračune **podešavanja** \> **·** \> **upravljanja troškovima i** \> **šifre po dnevnim dnevnicima.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dnevnice u interfejsu redizajniranih troškova

Funkcija dnevnice je podržana u redizajniranom radnom prostoru **za upravljanje** troškovima u Microsoft Dynamics 365 Finance verziji 10.0.25 i novijoj verziji.

Da biste omogućili dnevnice, sledite ove korake.

1. U radnom **prostoru za** upravljanje funkcijama pronađite i izaberite funkciju **Ponovno numerisanje izveštaja o troškovima** na listi, a zatim kliknite na dugme Omogući **odmah**.
2. Pronađite i izaberite funkciju **interfejsa "Per-diem" za** izveštaj o troškovima koji je ponovo zamišljen na listi, a zatim kliknite na dugme Omogući **odmah**.

## <a name="how-the-feature-works"></a>Kako funkcija funkcioniše

Ovaj odeljak pruža primere za tri scenarija konfiguracije. U svakom primeru, "Izračunaj **smanjenje obroka po** " postavljeno je na drugu vrednost. Za sva tri primera, ukupan iznos koji se isplati je isti dok se ne primeni smanjenje obroka. Nakon toga, ukupna isplata iznosa se razlikuje za svaki primer.

Da biste kreirali dnevnice koje se koriste za sva tri primera, sledite ove korake.

1. Idite na upravljanje **troškovima radnog** \> **prostora.**
2. Izaberite **novi izveštaj o** troškovima ili izaberite postojeći izveštaj o troškovima.
3. Dodajte novi trošak. U polju **Kategorija** izaberite dnevni **izbor**. Izaberite lokaciju i datume početka i završetka putovanja. Dnevnica za smeštaj, obroke i incidente (ostali troškovi) se izračunava na osnovu dnevnog dodatka koji je postavljen za izabranu lokaciju.

    Na primer, kao lokaciju **birate Redmond (** SAD). Dnevni džeparac za tu lokaciju je 150 američkih dolara (150 USD) za smeštaj, USD 75 za obroke i USD 5 za incidente. Datum početka je 10. januar, a krajnji datum je 14. januar. Zbog toga je izabrano trajanje pet dana kada je izabrana konfiguracija kalendarski dani sa vremenom, a izabrano vreme počinje i završava se u 12:00 časova na datum početka i završetka. Evo proračuna:

    - Ukupan iznos koji se plaća = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Obrok i slučajni deo ukupne količine = 5 × (75 + 5) = USD 400

Ako su tokom putovanja obezbeđeni doručak, ručak i večera, ti obroci moraju biti na broju kao smanjenje obroka.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Primer 1: Dnevnice gde se smanjenje obroka zasniva na vrsti obroka po putovanju

U ovom primeru, smanjenje obroka je 30 procenata za doručak, 30 procenata za ručak i 40 procenata za večeru. Na stranici **Parametri upravljanja troškovima**, polje "Izračunaj **smanjenje obroka po"** postavljeno je na vrstu **"Obrok" po putovanju**. Evo proračuna ako su zaposlenom obezbeđena tri doručka, dva ručka i nula večera:

- Smanjenje obroka = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Obroci i incidenti = 400 – 112,50 = USD 287.50
- Ukupan iznos koji se isplati = Ukupan džeparac – Smanjenje obroka = 1.150 – 112,50 = USD 1,037.50

![Dnevnica gde se smanjenje obroka zasniva na vrsti obroka po putovanju.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Primer 2: Dnevnice gde se smanjenje obroka zasniva na vrsti obroka dnevno

U ovom primeru, smanjenje obroka je 30 procenata za doručak, 30 procenata za ručak i 40 procenata za večeru. Na stranici **Parametri upravljanja troškovima**, polje **"Izračunaj smanjenje obroka po** " postavljeno je na **vrstu obroka po danu**. U ovom slučaju, u koordinatnoj mreži **"Obroci"** u dijalogu **"Uređivanje troškova** " opozovite izbor u poljima za potvrdu da biste naznačili koji obroci su vam obezbeđeni tokom putovanja.

Na primer, evo proračuna ako je doručak obezbeđen prva tri dana putovanja:

- Dnevno smanjenje obroka za svaki od prva tri dana = 75 × 30% = USD 22.50
- Ukupno smanjenje obroka = 3 × 22,50 = USD 67.50
- Obroci i incidenti za dane od 1 do 3 = 75 – 22,50 = USD 57.50
- Ukupni obroci i incidenti = Zbir obroka i incidenata tokom pet dana = 400 – 67,50 = USD 332.50
- Ukupan iznos koji se plaća = Ukupan iznos – Smanjenje obroka = 1.150 – 67,50 = USD 1,082.50

![Dnevnica gde se smanjenje obroka zasniva na vrsti obroka dnevno.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Primer 3: Dnevnice gde se smanjenje obroka zasniva na broju obroka dnevno

U ovom primeru, smanjenje obroka se izračunava na osnovu broja obroka koji su obezbeđeni dnevno (to je pitanje, **"Izračunaj smanjenje obroka** **po polju" na stranici "Parametri upravljanja** troškovima" postavljeno je **na "Broj obroka dnevno"**). U koordinatnoj mreži **"** Obroci" u dijalogu **"Uređivanje** troškova" opozovite izbor u poljima za potvrdu da biste naznačili koji obroci su obezbeđeni.
U ovom slučaju, smanjenje obroka se zasniva samo na # obezbeđenim obrocima, a ne na vrsti obroka ( Doručak/ručak/večera) koji je obezbeđen.

Evo proračuna za dnevnice kada se dnevni dodatak USD 150 smeštaj, USD 75 obroke i USD 5 za incidente:

- **Ukupan iznos koji se** plaća = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Jedan obrok:** Smanjenje obroka = 20% = USD 15
- **Dva obroka:** Smanjenje obroka = 50% = USD 37.50
- **Tri obroka:** Smanjenje obroka = 100% = USD 75

Evo proračuna za obroke i **dodatke za incidente**, koji obuhvataju USD 5 za incidente:

- Dan 1 - Dva obezbeđena obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 2. dan - Dva obezbeđena obroka = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- 3. dan - Jedan obezbeđeni obrok = (75 – 15) + 5 = 60 + 5 = USD 65
- 4. dan - Obezbeđeno nula obroka = (75-0) + 5 = 75 + 5 = USD 80
- 5. dan - Tri obezbeđena obroka = (75 – 75) + 5 = 0 + 5 = USD 5

- Ukupni obroci i incidenti = Obroci i incidenti za dan 1+ Dan 2 +Dan 3+Dan 4+ Dan 5 = USD 235
- Ukupno smanjenje obroka = Smanjenje obroka za dan 1+ Dan 2 +Dan 3+Dan 4+ Dan 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Ukupan iznos koji se isplati = Ukupan džeparac – Ukupno smanjenje obroka = USD 1,150 - USD 165 = USD 985

![Dnevni troškovi gde se smanjenje obroka zasniva na broju obroka dnevno.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verzije "Finansije" 10.0.23, ako koristite interfejs redizajniranih troškova, ne možete da kreirate troškove dnevnica koji imaju preklapajuće datume. Ako pokušate, dobićete poruku o grešci.
