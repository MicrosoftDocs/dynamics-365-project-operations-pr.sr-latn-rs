---
title: Šta je novo novembra 2020. – Project Operations za scenarije zasnovane na resursima/bez zaliha
description: Ovaj članak pruža informacije o ispravkama kvaliteta dostupnim u izdanju usluge Project Operations za novembar 2020. za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 75a7b63c12b0ad3c6808785b6cbe6f22bd65f126
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029547"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo novembra 2020. – Project Operations za scenarije zasnovane na resursima/bez zaliha

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Dynamics 365 Project Operations:

- Project Operations u CDS okruženju verzije 4.4.0.70
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Ispravke usluge Project Operations za scenarije zasnovane na resursima-bez zaliha

### <a name="project-operations-on-cds"></a>Project Operations u usluzi CDS

| Oblast funkcija                 | Referentni broj | Ispravka kvaliteta                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje mogućnostima za poslovanje       | 2036993          | Predmeti ugovora za stavke procene i dodelu resursa ažuriraju se na dobitnim ponudama kada stavka ponude ima tip **Svi zadaci**.                                                 |
| Naplata i određivanje cena          | 2070392          | Predmeti ugovora za projekat na fakturi se povećavaju svaki put kada izaberete **Osveži transakcije fakture**.                                                                         |
| Planiranje projekta             | 2043336          | Nije moguće izbrisati zapis člana projektnog tima.                                                                                                                                  |
| Planiranje projekta             | 2046013          | Nedosledno ponašanje za označavanje kolona Procene tokom učitavanja u odnosu na promenu tipa vremenske faze.                                                                                   |
| Planiranje projekta             | 2046647          | Vreme početka i završetka su pomereni za sat vremena kada zahteve za resursima generišu članovi projektnog tima.                                                                      |
| Planiranje projekta             | 2053879          | (Po predstojećem uvođenju CDS-a) PublishUnassignedAssignments prekida pokušaj čuvanja zadatka kada je greška „Vrednost prosleđena za ConditionOperator.In prazna“.                       |
| Planiranje projekta             | 2055501          | Ako **Datum početka projekta** ostane prazan, dolazi do neuspeha u rasporedu.                                                                                                      |
| Planiranje projekta             | 2066817          | Ne mogu da napravim generički resurs pomoću birača ljudi na kartici **Zadaci**.                                                                                                   |
| Planiranje projekta             | 2067034          | Dugme **Prikaz detalja** nije dostupno na stranici **Detalji zadatka**.                                                                                                       |
| Upravljanje resursima          | 2046667          | Članovi generičkog tima se ne brišu čak ni kada se svi resursi ispune.                                                                                                    |
| Stavka vremena i brzog troška | 2047499          | Dugme **Novo** na stranici Stavka vremena otvara stranicu **Nov potpis e-pošte**.                                                                                               |
| Stavka vremena i brzog troška | 2059859          | Otvara se neočekivani iskačući prozor prilikom kreiranja stavke troška.                                                                                                                         |
| Drugi                        | 2044181          | (Deinstaliranje porudžbenice)   Kada pokušate da deinstalirate osnovna rešenja msdyn_ProjectServiceCore_Patch i msdyn Project Service, dolazi do greške „Zapis nije dostupan“.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Upravljanje projektima i računovodstvo u rešenju Dynamics 365 Finance

| Oblast funkcija        | Referentni broj | Ispravka kvaliteta                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prepoznavanje prihoda | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Procenat procene dovršenosti projekta je pogrešan kada se u ugovoru koristi strana valuta i metod procenta napredovanja posla do dovršenosti.                     |
| Prepoznavanje prihoda | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Nije moguće objaviti procene pomoću metoda **stvarne cene** po završetku.                                                                                                    |
| Prepoznavanje prihoda | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminacija ne uspeva zbog greške u neuravnoteženom vaučeru kada se valuta kompanije i valuta transakcije razlikuju.                                              |
| Upravljanje troškovima  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Za korisnike koji nisu administratori, vrednosti pronalaženja za kolone stavki troškova kao što su **ID projekta** i **Kategorija rashoda** ne prikazuju se pravilno u okviru konektora za podatke. |
| Upravljanje troškovima  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Podrazumevano svojstvo stavke se ne prikazuje za kategorije troškova.                                                                                                         |
| Upravljanje troškovima  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integracija troškova mora da sadrži svojstvo stavke iz izveštaja o troškovima.                                                                                             |
| Fakturisanje           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Ne mogu da objavim predloge faktura za projekat zbog poruke o grešci koja kaže da kombinacija FD nije potvrđena.                                                    |
| Fakturisanje           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Ne mogu da vidim transakcije sa stranice sa detaljima **fakture**.                                                                                                              |
| Fakturisanje           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Stavke predloga fakture se mogu izbrisati.                                                                                                                                  |
| Projektno računovodstvo  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Stavke menija **Predviđanje** nisu vidljive na stranici sa listom **Projekti**.                                                                                                   |
| Projektno računovodstvo  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Ne mogu da otvorim **Izjava o projektu**   > **Transakcije i predviđanje**.                                                                                                       |
| Projektno računovodstvo  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Prilagođavanje računovodstva** nije omogućeno za fakturisane projektne transakcije.                                                                                                  |
| Projektno računovodstvo  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Podaci o računovodstvu nisu uključeni u tabelu **ProjCDSActualsImport** kada se proknjiži dnevnik **integracije**.                                                  |
| Projektno računovodstvo  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Stavka predviđanja projekta se udvostručuje kada uklonite, a zatim ponovo dodate dodeljivanje resursa.                                                                            |
| Projektno računovodstvo  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Izborom veze za ID projekta ne otvara se URL adresa duboke veze za CDS.                                                                                                         |
| Projektno računovodstvo  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nije moguće ažurirati datum početka zadatka u CDS-u.                                                                                                                           |
| Projektno računovodstvo  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Omogućavanje funkcije Više linija ugovora nije moguće bez CDS integracije.                                                                                   |

### <a name="regulatory-updates"></a>Regulatorne ispravke
Za informacije o regulatornim ispravkama za aplikacije za finansije i operacije, pogledajte članak [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe se možete prijaviti na LCS i pregledati planirane regulatorne ispravke pomoću alatke za pretragu problema. Pretraga problema vam omogućava pretragu po zemlji, tipu funkcije i izdanju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]