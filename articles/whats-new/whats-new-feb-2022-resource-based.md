---
title: Šta je novo u februaru 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u februaru 2022.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933003"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u februaru 2022. – Project Operations za scenarije zasnovane na resursima/bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.28.0.120
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.24

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

- Od ovog izdanja, možete da dodate do 300 članova tima u jedan projekat. Prethodno je ograničenje broja članova tima bilo 150. Više informacija potražite u članku [Ograničenja projekta](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Ispravke mape dvostrukog pisanja projektnih operacija

Sledeća lista prikazuje mape sa dva pisanja koje su izmenjene ili dodate u izdanje "Operacije projekta" iz februara 2022.

| Mapa entiteta | Ažurirana verzija | komentara |
| --- | --- | --- |
| Projektne operacije integracije projektni troškovi izvoz entiteta (msdyn\_ troškovi) | 1.0.0.3 | Prošireno za sinhronizaciju projektne aktivnosti na Dataverse. |

Za trenutnu listu i verzije mapa dvostrukog pisanja operacija projekta pogledajte verzije [mape dvostrukog pisanja operacija projekta](../environment/resource-dual-write-maps.md).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mapa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) u vodiču za rešavanje problema sa dvojnim pisanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2415109 | Podrazumevana vrednost u polju Uslovi plaćanja **operacija mora** biti zapis kupca ugovora o projektu i zapis proforma fakture. |
| Naplata i određivanje cena | 2497369 | Korekcija materijala mora pratiti vrednost datuma u parametrima **Ispravka**. |
| Naplata i određivanje cena | 2498697 | Poboljšana je bezbednosna konfiguracija za opoziv **stavke vremena**. |
| Naplata i određivanje cena | 2513824 | Za scenarije zasnovane na resursima, ID kategorije transakcije ne sme da premaši 28 znakova u operacijama projekta. |
| Naplata i određivanje cena | 2517455 | Radnja **transakcija reda osvežavanja** fakture ne sme biti dozvoljena da bude aktivirana više puta istovremeno za istu fakturu. |
| Naplata i određivanje cena | 2517465 | Radnja **detalja o deaktiviranju** reda fakture je blokirana jer nije podržana. |
| Naplata i određivanje cena | 2556660 | Fiksirana je provera efektivnosti datuma koja se obavlja na cenovnik koji je priložen zapisu parametara projekta. |
| Upravljanje mogućnostima za poslovanje | 2369202 | Ispravljena poslovna logika koja potvrđuje da cenovnici koji imaju preklapajuće datume efektivosti mogu biti priloženi istom projektnim ugovorom. |
| Upravljanje mogućnostima za poslovanje | 2385965 | Ispravili ste ponašanje na kartici "Kupci **"** na stranici "Ugovor o **projektu** " kada izaberete opciju "Sačuvaj **i zatvori"**. |
| Vreme i trošak | 2538503 | Projektni zadatak mora biti dostupan u **entitetu stvarnih** projekata nakon što se proknjiži izveštaj o troškovima. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo na Dynamics 365 Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Tokom uvoza kreditnih beleški dobavljača dolazi do greške. U poruci o grešci piše: "Iznos zadržavanja ne može biti veći od preostalog neto iznosa". |
| Upravljanje projektima i računovodstvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ako predlog fakture uključuje transakcije naknade za nula iznosa koje su neželjene stvarne prodaje, fakturisanje ne može da se dogodi. |
| Upravljanje projektima i računovodstvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Proknjiženi trošak nije tačan nakon što se ažurira nabavna cena i omogući **aktiviranje** upravljanja promenama.|
| Upravljanje projektima i računovodstvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Procena knjiženja za projekat fiksne cene koristi netačnu valutu i iznos u vaučeru za procenu, čak i **kada je omogućena valuta ugovora** o projektu za funkciju obračuna procene. |
| Upravljanje projektima i računovodstvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extension ne** bi trebalo da pozove da omogući praćenje promena bez hvatanja izuzetaka za entitete koji imaju ključeve za konfiguraciju koji nisu omogućeni. |
| Upravljanje projektima i računovodstvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Grupna obrada se popravlja kada se proknjiži više naprednih naloga i dođe do greške. |
| Putovanje i trošak | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Zbog problema sa poravnanjem koji se odnosi na gotovinske avanse na izveštaje o troškovima, iznos poreza nije pokriven kao deo gotovinskog avansa. |
| Putovanje i trošak | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informacije o porezu na promet nisu uključene u izveštaj **Troškovi - proknjižene transakcije**. |
| Putovanje i trošak | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kršenje **smernica troškova "Prijemnice** koje su potrebne" netačno prikazuje upozorenje u izveštajima o troškovima. |
| Putovanje i trošak | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakcija projekta ne uključuje porez na promet koji se ne može oporaviti u ukupnom iznosu prodaje kada je transakcija rezultat troškova kilometraže. |
| Putovanje i trošak | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kada red po stavkama ima porez, ne možete da promenite datum reda stavke i dolazi do greške u stanju izvornog dokumenta. |

## <a name="removed-and-deprecated-features"></a>Uklonjene i neodobrene funkcije

Uklonjene [ili zastarele funkcije u članku "Operacije](removed-depreciated-features-project.md) projekta" opisuju funkcije koje su uklonjene ili zastarele za Dynamics 365 Project Operations.

- Uklonjena funkcija više nije dostupna u proizvodu.
- Zastarela funkcija nije u aktivnom razvoju i može biti uklonjena u budućoj ispravci.

Najava amortizacije će se pojaviti u funkcijama " [Uklonjeno" ili "Zastarelo" u članku "Operacije](removed-depreciated-features-project.md) projekta" 12 meseci pre nego što bilo koja funkcija bude uklonjena iz proizvoda.

Za prekid promena koje utiču samo na vreme kompilacije, ali su binarno kompatibilne sa sandbox i proizvodnim okruženjem, vreme amortizacije će biti manje od 12 meseci. Ove promene obično su funkcionalne ispravke koje se moraju izvršiti na kompajleru.
