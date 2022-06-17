---
title: Performanse API-ja za raspored projekata
description: Ovaj članak pruža informacije o odrednicama performansi API-ja rasporeda projekta i identifikuje najbolje prakse za optimalnu upotrebu.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911199"
---
# <a name="project-schedule-api-performance"></a>Performanse API-ja za raspored projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, jednostavnu implementaciju – pogodbu o predračunima, Project for the Web_

Ovaj članak pruža informacije o odrednicama performansi programskih interfejsa aplikacije Project schedule (API) i identifikuje najbolje prakse za optimizaciju korišćenja.

## <a name="project-scheduling-service"></a>Usluga planiranja projekta
Usluga planiranja projekta je usluga sa više zakupaca koja se pokreće u usluzi Microsoft Azure. Dizajniran je da poboljša interakciju pružanjem brzog i tečnog iskustva kada korisnici rade na projektima. Ovo poboljšanje je postignuto prihvatanjem zahteva za promenu, njihovom obradom, a zatim odmah vraćanjem rezultata. Usluga asinhrono traje na usluzi Dataverse i ne blokira korisnike da obavljaju druge operacije.

API-je za planiranje projekta oslanjaju se na uslugu zakazivanja projekta da bi pokrenuli zahteve koji su detaljnije opisani u kasnijim odeljcima ovog članka.

API-ji rasporeda projekata su dizajnirani za rad sa sledećim entitetima strukturne analize posla (SAP):

  - Project
  - Projektni zadatak
  - Zavisnost projektnog zadatka
  - Član projektnog tima
  - Dodela resursa
  
Podržana su i gotova polja i prilagođena polja. Osim ako nije drugačije naznačeno, podržane su sve uobičajene operacije, kao što su kreiranje, ažuriranje i brisanje. Više informacija potražite u članku [Korišćenje API-ja za raspored projekata za izvršavanje operacija i planiranje entiteta](schedule-api-preview.md).

U sklopu API-ja za raspored projekta, dodat je obrazac radne jedinice. Ovaj obrazac je poznat kao OperationSet, i može se koristiti kada nekoliko zahteva mora biti obrađeno u jednoj transakciji.

Sledeća ilustracija prikazuje tok koji će partner iskusiti kada se ova funkcija koristi.

![Dataverse i tok usluge planiranja projekta.](./media/dataverse-project-scheduling-service-flow.png)

**1 korak**: Klijent upućuje API poziv krajnjoj tački otvorenog protokola za podatke (OData) u usluzi Dataverse kako bi kreirao OperationSet.

**2. korak**: Nakon kreiranja novog OperationSet, vraća se vrednost **OperationSetId**.

**3. korak**: Klijent koristi vrednost **OperationSetId** da bi napravio još jedan API zahtev za raspored projekta. Rezultat je zahtev za kreiranje, ažuriranje ili brisanje entiteta za zakazivanje. Kada se ovaj zahtev uputi, vrši se provera valjanosti metapodataka. Ako provera valjanosti ne uspe, zahtev se prekida i vraća se greška.

**Koraci 4a–4c**: Ovi koraci predstavljaju fazu PRIHVATANJA. Klijent poziva **ExecuteOperationSetV1** API, koji šalje sve promene u uslugu planiranja projekta u jednoj grupi. Usluga planiranja projekta pokreće sopstvene provere valjanosti na zahteve u grupi. Sve greške prilikom provere valjanosti opozivaju grupu i vraćaju izuzetak pozivaocu. Ako je usluga planiranja projekta uspešno prihvatila grupu, OperationSet status se ažurira tako da odražava činjenicu da uslugu OperationSet obrađuje usluga planiranja projekta.

**5. korak**: Ovaj korak predstavlja fazu TRAJANJE. Usluga planiranja projekta asinhrono upisuje grupu u uslugu Dataverse u jednoj transakciji. Ako operacija pisanja bude uspešna, OperationSet se označava kao **Dovršeno**. Sve greške vraćaju transakciju i grupu, a OperationSet se označava kao **Neuspešno**.

## <a name="performance-methodology"></a>Metodologija performansi
Vreme izvršavanja se definiše kao vreme od poziva API-ju **ExecuteOperationSetV1** sve dok usluga planiranja projekta ne završi pisanje u uslugu Dataverse. Sve operacije rade kombinovano 2.200 puta, a prijavljena su i merenja vremena izvršenja P99. Mere se operacije sa jednim zapisom, kao i masovne operacije.

Za operaciju sa jednim zapisom, OperationSet sadrži jedan zahtev. Za masovne operacije, on sadrži 20, 50 ili 100 zahteva. Svaka veličina grupe se posebno izveštava.

Ove operacije se pokreću na UR 15 Project Operations Lite primeni u Severnoj Americi.

## <a name="results"></a>Rezultati
### <a name="create-operations"></a>Kreiranje operacija
#### <a name="single-record-create-operations"></a>Operacije kreiranja jednog zapisa
Sledeća tabela prikazuje vremena izvršavanja za kreiranje jednog zapisa. Vremena su u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Vreme</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodela</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zavisnost</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacije masovnog kreiranja
Sledeća tabela prikazuje vremena izvršavanja za kreiranje mnogo zapisa. Konkretno, Microsoft je izmerio vremena izvršavanja za kreiranje 20, 50 i 100 zapisa u jednom OperationSet. Vremena su u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tip&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Vreme</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisa</th>
    <th class="tg-0lax" colspan="2">50 zapisa</th>
    <th class="tg-0lax" colspan="2">100 zapisa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodela</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zavisnost</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operacije masovnog kreiranja nad entitetima **Projekat** i **Član tima** nisu uvrštene u ovu tabelu, jer vreme izvršavanja za te operacije nalikuje vremenu izvršavanja kada se API za kreiranje jednog zapisa poziva više puta. Ovi API-ji se odmah pokreću u usluzi Dataverse.

Sledeća ilustracija prikazuje scenario vremena izvršavanja za entitete **Zadatak**, **Dodela** i **Zavisnost** kada se kreira 20, 50 i 100 zapisa i kada se koriste sva podržana polja.

![Kreirajte grafikon vremena izvršavanja zapisa.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Ažuriranje operacija
#### <a name="single-record-update-operations"></a>Operacije ažuriranja jednog zapisa
Sledeća tabela prikazuje vremena izvršavanja za ažuriranje jednog zapisa. Vremena su u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="2">Vreme</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obavezna polja </th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije ažuriranja za entitete **Dodele resursa** i **Zavisnost projektnog zadatka** nisu podržane.

#### <a name="bulk-update-operations"></a>Operacije masovnog ažuriranja
Sledeća tabela prikazuje vremena izvršavanja za ažuriranja mnogo zapisa. Konkretno, Microsoft je izmerio vremena izvršavanja za ažuriranja 20, 50 i 100 zapisa u jednom OperationSet. Vremena su u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tip&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="6">Vreme</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 zapisa</th>
    <th class="tg-0lax" colspan="2">50 zapisa</th>
    <th class="tg-0lax" colspan="2">100 zapisa</th>
  </tr>
  <tr>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
    <th class="tg-0lax">Obavezna polja</th>
    <th class="tg-0lax">Sva podržana polja</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije ažuriranja za entitete **Dodele resursa** i **Zavisnost projektnog zadatka** nisu podržane.

Sledeća ilustracija prikazuje scenario vremena izvršavanja za entitete Zadatak, i Član tima kada se ažurira 20, 50 i 100 zapisa i kada se koriste sva podržana polja.

![Ažurirajte grafikon vremena izvršavanja zapisa.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operacije brisanja
#### <a name="single-record-delete-operations"></a>Operacije brisanja jednog zapisa
Sledeća tabela prikazuje vremena izvršavanja za brisanje jednog zapisa. Vremena su u sekundama.

| Vrsta zapisa | Vreme  |
|-------------|-------|
| Zadatak        | 20.12 |
| Dodela  | 10.86 |
| Član tima | 12.52 |
| Zavisnost  | 20.89 |

> [!NOTE]
> Operacije brisanja nad entitetom **Projekat** nisu podržane.

#### <a name="bulk-delete-operations"></a>Operacije masovnog brisanja
Sledeća tabela prikazuje vremena izvršavanja za brisanje mnogo zapisa. Konkretno, Microsoft je izmerio vremena izvršavanja za brisanje 20, 50 i 100 zapisa u jednom OperationSet. Vremena su u sekundama.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tip&nbsp;&nbsp;&nbsp;zapisa</th>
    <th class="tg-0lax" colspan="3">Vreme</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 zapisa</th>
    <th class="tg-0lax">50 zapisa</th>
    <th class="tg-0lax">100 zapisa</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Zadatak</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dodela</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Član tima</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Zavisnost</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operacije brisanja nad entitetom **Projekat** nisu podržane.

Sledeća ilustracija prikazuje scenario vremena izvršavanja za entitete **Zadatak**, **Dodela**, **Član tima** i **Zavisnost** kada se briše 20, 50 i 100 zapisa.

![Brišite grafikon vremena izvršavanja zapisa.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Zapažanja
Za svaku operaciju zapisa, API-ju **ExecuteOperationSet** je potrebno oko 800 milisekundi da pošalje zahtev sluzi planiranja projekta. Usluzi planiranja projekta zatim treba oko pet sekundi za obradu korisnog opterećenja i pozivanje usluge Dataverse. Ostatak vremena izvršavanja se troši na vođenje poslovne logike i pisanje podataka u bazu podataka u programu Dataverse.

Kada se 100 zapisa kreira, ažurira ili izbriše, API-ju **ExecuteOperationSet** je potrebno oko tri sekunde da pošalje zahtev usluzi planiranja projekta. Usluzi planiranja projekta zatim treba oko pet sekundi za obradu zahteva i pozivanje usluge Dataverse. Masovne operacije moraju jednokratno da plate **porez na uslugu planiranja projekta** za sve zapise u OperationSet-u. Zbog toga masovne operacije imaju znatno niže prosečno vreme izvršavanja od operacija sa jednim zapisom.

## <a name="scenarios"></a>Scenariji
Sledeća tabela prikazuje vreme izvršavanja kada se API-ju planiranja projekta koriste za izvršavanje određenih scenarija. Vremena su u sekundama.

| Scenario                                                                   | Vreme  |
|----------------------------------------------------------------------------|-------|
| Kreirajte projekat koji ima 40 zadataka.                                      | 36.01 |
| Kreirajte projekat koji ima 40 zadataka i 20 zavisnosti.                  | 38.11 |
| Kreirajte projekat koji ima 40 zadataka i 30 dodela.                   | 60.17 |
| Kreirajte projekat koji ima 40 zadataka, 20 zavisnosti i 30 dodela. | 60.27 |

## <a name="best-practices"></a>Najbolji primeri iz prakse
Na osnovu rezultata prethodnih scenarija, performanse API-ja su bolje u sledećim uslovima:

  - Grupišite što više operacija zajedno. Prosečno vreme izvršavanja za masovne operacije je bolje od prosečnog vremena izvršavanja za operacije sa jednim zapisom. Što je manji broj OperationSets koji se koriste, to će vreme izvršavanja biti brže.
  - Podesite samo minimalne atribute koji su potrebni za ostvarivanje vašeg scenarija. Budite selektivni u pogledu tipova polja koja nisu potrebna u zahtevu za OperationSet. Polja koja sadrže strane ključeve ili polja zbirne vrednosti negativno će uticati na performanse.
