---
title: Šta je novo novembra 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ova tema pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju projektnih operacija za scenarije zasnovane na resursima/nenababđenim resursima.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827343"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo novembra 2021. – Project Operations za scenarije zasnovane na resursima/bez zaliha

*Odnosi se na: Project Operations za scenarije zasnovane na resursima / bez zaliha*

Ova tema se primenjuje na sledeće komponente i verzije programa Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.26.0.145, 4.26.0.148, ili 4.26.0.150
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.22

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

Sledeće funkcije su uključene u ovom izdanju:

- Programski interfejsi aplikacija za planiranje projekta (API) sada podržavaju mogućnost kreiranja i brisanja kofa projekta.

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

U ovom izdanju nema ispravki za Project Operations mape dvostrukog upisivanja. Za trenutnu listu i verzije Project Operations mapa dvostrukog upisivanja, pogledajte [Verzije Project Operations mapa dvostrukog upisivanja](/dynamics365/project-operations/environment/resource-dual-write-maps).

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve srodne mape tabela dok ažurirate verziju rešenja za Dataverse operacija projekta i finansije. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva u problemu sa kolonama tabele koje nedostaju [u](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) odeljku mape vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-in-dataverse"></a>Projektne operacije u Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2240080 | Polje **Uslovi** plaćanja ne smeju biti duplirani u fakturi pro forma. |
| Naplata i određivanje cena | 2358236 | Korekcija fakture mora dozvoliti korekcije koje imaju redove nulte cene. |
| Upravljanje resursima | 2410072 | Dozvoli podešavanje resursa koji je dodeljen zadatku kao menadžer projekta. |
| Naplata i određivanje cena | 2430234 | Rešite problem sa izračunavanjem performansi troška. |
| Vreme i trošak | 2436978 | Dozvolite da se vreme unese u hh:mm formatu. |
| Naplata i određivanje cena | 2448623 | Dozvoli ažuriranje cenovnika nakon što su povezani sa organizacionom jedinicom. |
| Vreme i trošak | 2460396 | Dozvolite brisanje vremenskog unosa brisanjem ćelije. |
| Naplata i određivanje cena | 2467386 | Dozvolite brisanje projekta koji ima zadatak, čak i kada je zadatak povezan sa izabranom ponudom. |
| Vreme i trošak | 2461744 | Prikaz **"Moje neuspešno** odobravanje" sadrži samo odobrenja projekta u fazi **"Prosleđeno".** |
| Vreme i trošak | 2464082 | Uklonite vezu iz odobravanja projekta sa skupom odobravanja kada se status cilja podudara. |
| Vreme i trošak | 2468108 | Zadatak "Raspored" ne bi trebalo da postavi **status** obrade za skup odobravanja. |
| Vreme i trošak | 2471503 | Izbrišite skupove odobravanja stare sedam dana. |
| Naplata i određivanje cena | 2480687 | Referenca reda ponude ne sme biti uklonjena kada se kreira prekretnica reda ponude. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u finansijama

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Upravljanje projektima i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Zadržani iznosi dobavljača u transakcijama troškova projekta nisu prikazani na listi transakcija. |
| Upravljanje projektima i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktura međukompanijskog dobavljača se pokvari kada je uključena integracija fakture od dobavljača. |
| Upravljanje projektima i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uslovi plaćanja na projektnim fakturama ne funkcionišu na očekivani način. |
| Upravljanje projektima i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada se izda zadržavanje dobavljača, knjiženje vaučera ima dodatne redove koji su netačni. |
| Upravljanje projektima i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kada se nalog integracije operacija projekta proknjiži, on ne uspeva zbog nedostajućih dimenzija za konto na koji se ne knjiži. |
| Upravljanje projektima i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **·** "Projekat" se ne može uređivati u fakturi dobavljača na čekanju kada je artikalu dodeljena kategorija nabavke. |
| Upravljanje projektima i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Okno za navigaciju nedostaje ako niste prijavljeni na opciju "Operacije projekta" Dataverse. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kada knjižite prihode od fakture projekta u zatvorenom predmetu za zadržavanje, dolazi do problema jer transakcije na vaučeru ne balansiraju. |
| Upravljanje projektima i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procene nakon knjiženja predloga fakture blokira korektivne redove od uvoza. |
| Upravljanje projektima i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmena potpuno fakturisanog zapisa prekretnice ne bi trebalo da bude moguća. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi izveštaji o troškovima su vidljivi kada tražite kategoriju u mobilnoj aplikaciji "Troškovi". |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netačni iznosi za transakcije dobavljača i transakcije poreza na promet se knjiže iz troška koji se kreira iz transakcije kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Do nevažnog upozorenja dolazi kada osvežite **stranicu izveštaja** o troškovima. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešna prelazna osoba koja vrši odobravanje se koristi kada izbrišete prelaznu osobu koja vrši odobravanje, a zatim ponovo prijavite izveštaj o troškovima putem toka posla. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do greške u knjiženju koja je povezana sa podešavanjem kilometraže. |
