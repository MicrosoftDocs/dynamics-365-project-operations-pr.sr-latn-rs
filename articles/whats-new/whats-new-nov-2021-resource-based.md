---
title: Šta je novo novembra 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Project Operations za novembar 2021. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932911"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo novembra 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.22

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Programski interfejsi aplikacije za planiranje projekta (API-ji) sada podržavaju mogućnost kreiranja i brisanja kontejnera projekta.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](/dynamics365/project-operations/environment/resource-dual-write-maps).

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2240080 | Polje **Uslovi plaćanja** ne sme biti duplirano na profakturi. |
| Naplata i određivanje cena | 2358236 | Korekcija fakture mora dozvoliti korekcije koje imaju redove sa nultom cenom. |
| Upravljanje resursima | 2410072 | Dozvolite podešavanje resursa koji je dodeljen zadatku kao menadžer projekta. |
| Naplata i određivanje cena | 2430234 | Rešite problem sa izračunavanjem performansi troška. |
| Vreme i trošak | 2436978 | Dozvolite da se vreme unese u čč:mm formatu. |
| Naplata i određivanje cena | 2448623 | Dozvolite ažuriranje cenovnika nakon što su povezani sa organizacionom jedinicom. |
| Vreme i trošak | 2460396 | Dozvolite brisanje unosa vremena brisanjem ćelije. |
| Naplata i određivanje cena | 2467386 | Dozvolite brisanje projekta koji ima zadatak, čak i kada je zadatak povezan sa dobijenom ponudom. |
| Vreme i trošak | 2461744 | Prikaz **Moje neuspelo odobrenje** sadrži samo odobrenja projekata u fazi **Poslato**. |
| Vreme i trošak | 2464082 | Uklonite vezu iz odobrenja projekta sa skupom odobrenja kada se status cilja podudara. |
| Vreme i trošak | 2468108 | Posao planiranja ne bi trebalo da postavi status **U obradi** za skup odobrenja. |
| Vreme i trošak | 2471503 | Izbrišite skupove odobrenja stare sedam dana. |
| Naplata i određivanje cena | 2480687 | Referenca reda na ponudi ne sme biti uklonjena kada se kreira kontrolna tačka reda ponude. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani iznosi dobavljača u transakcijama troškova projekta nisu prikazani na listi transakcija. |
| Upravljanje projektima i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača ima grešku kada je uključena integracija fakture dobavljača. |
| Upravljanje projektima i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uslovi plaćanja na projektnim fakturama ne funkcionišu na očekivani način. |
| Upravljanje projektima i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada je zadržavanje dobavljača izdato, knjiženje vaučera ima dodatne redove koji nisu tačni. |
| Upravljanje projektima i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kada se dnevnik integracije programa Project Operations knjiži, on ima grešku jer nedostaju dimenzije za poslovni kontakt u koji se ne knjiži. |
| Upravljanje projektima i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Projekat** ne može da se uređuje na fakturi dobavljača na čekanju kada je kategorija nabavke dodeljena stavci. |
| Upravljanje projektima i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Okno za navigaciju nedostaje ako niste prijavljeni u Project Operations Dataverse. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kada knjižite prihod sa fakture za projekat u primenjenoj slučaju zadržavanja, dolazi do greške jer se transakcije na vaučeru ne saldiraju. |
| Upravljanje projektima i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procene nakon knjiženja predloga fakture blokira uvoz korektivnih redova. |
| Upravljanje projektima i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmena zapisa potpuno fakturisane kontrolne tačke ne bi trebalo da bude moguća. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi izveštaji o troškovima su vidljivi kada tražite kategoriju u mobilnoj aplikaciji Troškovi. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netačni iznosi za transakcije dobavljača i poreza na promet koji su knjiženi iz troška koji je nastao transakcijom kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kada osvežite stranicu **Izveštaj o troškovima**, dolazi do nevažnog upozorenja. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešna privremena osoba koja vrši odobravanje se koristi kada izbrišete privremenu osobu koja vrši odobravanje, a zatim ponovo pošaljete izveštaj o troškovima putem toka posla. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do greške u knjiženju u vezi sa podešavanjem kilometraže. |
