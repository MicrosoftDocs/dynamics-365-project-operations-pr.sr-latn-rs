---
title: Kreiranje strukturne analize posla
description: Ovaj članak objašnjava kako da kreirate strukturnu analizu posla (SAP) koja uključuje osnovne kontrole u novom interfejsu za planiranje.
author: ruhercul
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 19d2dfeff39fd3c5edd5124c27134a9fe360e4d1
ms.sourcegitcommit: 8f4841387deea2998589b7365c3373585a16cb0e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9655206"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Kreiranje strukturne analize posla (SAP)

Raspored projekta navodi koji posao treba da se završi, koji resursi će obavljati posao i vremenski okvir u kom posao mora da se završi. Raspored odražava sav posao povezan sa završavanjem projekta na vreme. U usluzi Dynamics 365 Project Operations kreirate raspored projekata na sledeći način:

  - Raščlanjujete posao u zadatke kojima je lako upravljati.
  - Procenjujete vreme potrebno za obavljanje svakog zadatka.
  - Podešavate zavisne elemente zadataka.
  - Podešavate trajanja zadataka.
  - Procenjujete generičke resurse koji će izvršiti zadatke. 

Raspored projekata kreiran je na kartici **Raspored** na stranici **Projekat**.

## <a name="tasks"></a>Zadaci

Prvi korak u kreiranju projektnog rasporeda je raščlanjivanje posla na upravljive delove. Raspored u usluzi Project Operations podržava sledeće funkcije:

- Rezime ili zadaci spremišta
- Zadaci čvora lista

### <a name="summary-tasks"></a>Rezimirani zadaci

Rezimirani zadaci mogu da uskladište druge rezimirane zadatke ili zadatke čvora lista. Oni nemaju sopstvene radne aktivnosti ni troškove. Umesto toga, njihove radne aktivnosti i troškovi su zbirna vrednost radnih aktivnosti i troškova njihovih zadataka u kontejneru. Datum početka rezimiranog zadataka je datum početka zadataka u kontejneru, a datum završetka je datum završetka zadataka u kontejneru. Naziv rezimiranog zadatka može se uređivati, ali svojstva zakazivanja, uključujući aktivnosti, datume i trajanje, ne mogu se uređivati. Ako obrišete rezimirani zadatak, brišete i sve njegove zadatke u kontejneru.

### <a name="leaf-node-tasks"></a>Zadaci čvora lista

Zadaci čvora lista predstavljaju najdetaljniji posao na projektu. Oni imaju procenjene aktivnosti, resurse, planirane datume početka i završetka i trajanje.

## <a name="create-a-task-hierarchy"></a>Kreiranje hijerarhije zadatka

### <a name="add-a-task"></a>Dodavanje zadatka

Dovršite sledeće korake da biste dodali jedan ili više zadataka.

1. Idite na **Projekti**, izaberite i otvorite zapis projekta za koji želite da kreirate raspored. 
2. Izaberite karticu **Zadaci**. 
3. Izaberite **Dodajte novi zadatak**, unesite ime zadatka, a zatim pritisnite taster Enter.
2. Unesite ime drugog zadatka i ponovo pritisnite Enter dok ne dobijete kompletnu listu zadataka.

### <a name="manage-hierarchy-of-a-task"></a>Upravljanje hijerarhijom zadatka

Kada je zadatak razveden, postaje podređen zadatku koji se nalazi neposredno iznad njega. ID rasporeda zadatka se zatim ponovo izračunava tako da se zasniva na ID-u rasporeda njegovog novog nadređenog elementa i sledi šemu numerisanja. Nadređeni zadatak je sada rezimirani zadatak. Stoga postaje zbirna vrednost podređenih zadataka. Kada se zadatak unapredi, to više nije podređeni zadatak nadređenog zadatka. ID rasporeda se zatim ponovo izračunava tako da odražava ažuriranu dubinu i položaj zadatka u hijerarhiji. Aktivnosti, troškovi i datumi prethodnog nadređenog zadatka se ponovo izračunavaju kako ne bi uključili ovaj zadatak.

Dovršite sledeće korake da biste uvukli ili promovisali zadatak.

1. Na stranici **Projekat**, na kartici **Zadaci**, u delu **Rezimirani zadaci** izaberite tri vertikalne tačke po nazivu zadatka, a zatim izaberite **Napravite podzadatak**. 
2. Izaberite zadatak za uvlačenje ili promociju. Da biste izabrali više zadataka, izaberite zadatak, pritisnite i držite taster Ctrl, a zatim izaberite dodatne zadatke.
2. Izaberite **Uvuci** ili **Promoviši podzadatak** za premeštanje zadataka ispod ili iznad rezimiranih zadataka.

### <a name="move-tasks-up-and-down"></a>Premeštanje zadataka nagore i nadole

Zadaci mogu da se premeste na bilo koji nivo u strukturnoj analizi posla na jedan od dva načina:

- Izaberite još jedan zadatak i prevucite ga na željeno mesto.
- Izaberite jedan ili više zadataka, kliknite desnim tasterom miša i izaberite **Iseci**, izaberite odredišnu ćeliju u rasporedu, a zatim kliknite desnim tasterom miša i izaberite **Nalepi**.

## <a name="task-attributes"></a>Atributi zadatka

Ime zadatka opisuje posao koji mora da se dovrši. U usluzi Project Operations, atributi koji su povezani sa zadatkom opisuju raspored zadatka i njegove potrebe za angažovanjem resursa.

## <a name="schedule-attributes"></a>Zakazivanje atributa

Atributi **Aktivnosti**, **Datum početka**, **Datum završetka** i **Trajanje** definišu raspored za zadatak.

Sledeća tabela prikazuje dodatne atribute rasporeda.

| **Konačno ime za prikaz** | **Konačan opis** |
| --- | --- |
| Angažovanje na završetku (časovi) | Odrađeni posao za zadatak u časovima. |
| Trajanje | Prikazuje trajanje zadatka u danima. |
| Ukupno angažovanje | Ukupan posao na zadatku u časovima. |
| Završetak | Datum i vreme završetka. |
| % dovršenosti | Procenat zadatka koji je završen. |
| Kontejner projekta | Tabla zadataka može biti grupisana prema kontejneru tako da svaki kontejner ima sopstvenu kolonu. |
| Preostalo angažovanje (časovi) | Preostali posao za zadatak u časovima. |
| Pokreni | Datum i vreme početka. |
| +Ime | Ime zadatka. |
| ID | ID zadatka u strukturnoj analizi posla. |

Kao administrator možete da definišete prilagođena polja na entitetu zadatka. Međutim, polja se ne mogu prikazati na mreži rasporeda. Da biste videli prilagođena polja, dodajte ih na stranici sa detaljima **Projektni zadatak**.

## <a name="staffing-attributes"></a>Atributi zaposlenih

Atributima angažovanja se pristupa u polju **Resursi** u rasporedu. Možete potražiti postojeći resurs ili izaberite **Kreiraj** i u oknu **Brzo kreiranje** dodajte člana projektnog tima kao novi resurs.  Kada tražite resurs koristeći birač resursa u matrici koordinatne mreže zadataka, prikazu table ili gantovom dijagramu, pretraga vraća postojeće članove projektnog tima ili aktivne resurse koji se mogu knjižiti.

Polja **Uloga**, **Jedinica za obezbeđivanje resursa** i **Naziv pozicije** se koriste za opisivanje potreba za angažovanjem resursa na zadatku. Ovi atributi angažovanja, zajedno sa rasporedom zadataka, koriste se za pronalaženje dostupnih resursa za obavljanje ovog zadatka.

   - **Uloga**: Navedite vrstu resursa koji je potreban za izvršavanje zadatka.
   - **Jedinica za obezbeđivanje resursa**: Navedite jedinicu iz koje treba dodeliti resurse za zadatak. Ovaj atribut utiče na procenu troškova i prodaje za zadatak ako su stope troškovi i naplate za resurs podešene na osnovu jedinica za obezbeđivanje resursa.
   - **Naziv pozicije**: Unesite ime za generički resurs koje služi kao čuvar mesta za resurs koji će na kraju obaviti posao.

Polje **Resursi** sadrži naziv pozicije generičkog resursa ili imenovanog resursa kada ga neko pronađe.

Polje **Kategorija** sadrži vrednosti koje ukazuju na širi tip posla u koji se zadatak može grupisati. Ovo polje ne utiče na zakazivanje niti obezbeđivanje resursa. Umesto toga, polje se koristi samo za izveštavanje.

## <a name="task-dependencies"></a>Zavisnosti zadatka

Raspored u usluzi Project Operations možete da koristite za kreiranje odnosa prethodnika između zadataka. Polje **Prethodni zadatak** koristi jednu ili više vrednosti kako bi označio zadatke od kojih zadatak zavisi. Kada dodelite prethodne vrednosti zadatku, zadatak možete da pokrenete jedino kada dovršite sve prethodne zadatke. Zbog zavisnih elemenata, planirani datum početka zadatka vraća se na datum kada su prethodni zadaci završeni.

Režim zadatka nema uticaja na ažuriranja koja se obavljaju na datum početka i završetka prethodnih/zavisnih zadataka.

## <a name="understanding-the-impacts-of-duration-resource-calendars-and-project-calendars-on-tasks"></a>Razumevanje uticaja trajanja, kalendara resursa i projektnih kalendara na zadatke
Trajanje zadatka se definiše kao broj radnih sati između vremena početka datuma početka i vremena završetka datuma završetka zadatka.   Project for the Web definiše jedinice mere trajanja na sledeći način:

| **Mera trajanja** | **Količina**|
|----------------------------------------------------|----------------------|
| Sati dnevno | 8 |
| Sati nedeljno |  40 |
| Dana mesečno |  20 |

Nedodeljeni zadaci se zakazuju pomoću kalendara projekta. Međutim, nakon početne dodele resursa, planiranje zadatka se ažurira tako da poštuje kalendar resursa. Naknadne promene zadatka koji ima dodelu biće regulisane [režimom zakazivanja](scheduling-modes.md) projekta. Da biste saznali više o uticaju kalendara na zadatke, pogledajte članke [Kalendari resursa u rešenju Project for the Web](https://techcommunity.microsoft.com/t5/project-blog/resource-calendars-in-project-for-the-web/ba-p/3269686) i [Vremena početka zadatka i vaši projekti!](https://techcommunity.microsoft.com/t5/project-blog/task-start-times-amp-your-projects/ba-p/3269665)


## <a name="accessibility-and-keyboard-shortcuts"></a>Pristupačnost i tasterske prečice

Mreža **Raspored** je potpuno dostupna i može se koristiti sa čitačima ekrana kao što su Narrator, JAWS ili NVDA. Kroz oblast mreže možete se kretati pomoću tastera sa strelicama (kao u programu Microsoft Excel), možete koristiti taster Tab da biste se kretali kroz interaktivne elemente korisničkog interfejsa, a pomoću tastera sa strelicom nadole, tastera Enter ili razmaknice možete da izaberete i otvorite padajuće menije.

## <a name="project-limitations"></a>Ograničenja projekta 
Trebalo bi da znate za sledeća ograničenja ako koristite strukturu analize posla u usluzi Project Operations. Ova ograničenja se odnose na projekte i zadatke. Više informacija potražite u članku [Ograničenja i granice usluge Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

| **Polje**                                          |  **Ograničenje**           |
|----------------------------------------------------|----------------------|
| Maksimalni ukupni broj zadataka za projekat                  | 500                  |
| Maksimalno ukupno trajanje za projekat               | 3650 dana (10 godina) |
| Maksimalni ukupni broj resursa za projekat              | 300                  |
| Maksimalan ukupni broj veza (samo narednih) za projekat | 600                  |
| Maksimalni ukupni broj prilagođenih polja za projekat          | 10                   |
| Maksimalne stavke kontrolne liste po zadatku                   | 20                   |

**Ograničenja zadatka**

| **Polje**                               |   **Ograničenje**           |
|-----------------------------------------|-----------------------|
| Maksimalni nivo hijerarhije                 | 10 nivoa             |
| Maksimalan broj veza (narednih + prethodnih) | 20                    |
| Maksimalno trajanje zadatka lista           | 1250 dana             |
| Maksimalno trajanje zadatka rezimea      | 3650 dana (10 godina)  |
| Maksimalan broj resursa dodeljenih zadatku    | 20 resursa          |
| Podržani opseg datuma za zadatak         | 1.1.2000. – 12.31.2149. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
