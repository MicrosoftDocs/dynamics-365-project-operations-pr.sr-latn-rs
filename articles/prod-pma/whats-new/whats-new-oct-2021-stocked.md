---
title: Šta je novo ili promenjeno u projektno poslovanje, oktobar 2021. za snabdevene/proizvodne scenarije
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u oktobru 2021.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029960"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Šta je novo ili promenjeno u projektno poslovanje, oktobar 2021. za snabdevene/proizvodne scenarije

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.22
 
## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
|--------------|------------------|----------------|
| Upravljanje projektima i računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Projektni rad u toku (PUT) i akumulirani iznosi prihoda nisu ispravno stornirani kada se proknjiži faktura međukompanijskog kupca. |
| Upravljanje projektima i računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Sprečavanje **zatvaranja projekta ako postoje otvorene** transakcije ne funkcioniše. |
| Upravljanje projektima i računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija naplate na besplatnoj tekstualnoj fakturi ne popunjava automatski dimenzije iz projekata kada je ta funkcionalnost omogućena. |
| Upravljanje projektima i računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | U nekompanijskim scenarijima, IZNOSI PUT i akumulirani prihodi se ne storniranju kada se proknjiži faktura projekta. |
| Upravljanje projektima i računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrednosti dugovanja i potraživanja se menjaju kada se Microsoft Excel programski dodatak koristi sa nalogom troškova projekta, a polje **Vrsta konta "Pomak"** je podešeno na "Projekat **"**. |
| Upravljanje projektima i računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Iznos koji se knjiži u projektnim transakcijama je prenaglašen u izlaznoj porudžbini projekta koja uključuje snabdevene **artikle i koji ima iznose poreza koji se ne odbijaju kada je oznaka "KorišćenjeTax** ". |
| Upravljanje projektima i računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem deli iznos između izveštaja o dobitku i gubitku projekta i izveštaja o PUT projekta. |
| Upravljanje projektima i računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Zalihe pri ruci su netačne nakon korigovanja delimično vraćenog zahteva artikla. |
| Upravljanje projektima i računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Imena resursa se dupliraju u operacijama projekta kada se uređuju u programu Microsoft Project. |
| Upravljanje projektima i računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Izveštaji o međukompanijskim troškovima koji imaju međukompanijske troškove fakture dobavljača koji se plaćaju prvo se knjiže **u vrstu knjiženja troškova** PUT projekta. Međutim, tokom obrade, troškovi vezani za procenu se knjiže na **vrstu knjiženja troškova** projekta umesto na očekivanu **vrstu knjiženja međukompanijskih** troškova. |
| Upravljanje projektima i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadržavanja dobavljača u transakcijama troškova projekta nisu prikazani. |
| Upravljanje projektima i računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | List sa vremenom mora zaokružiti iznos transakcije u valuti transakcije na određeni broj decimalnih mesta za sve računovodstvene raspodele i stavke dodele naloga knjiženja. |
| Upravljanje projektima i računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahteva za artikal projekta se automatski ažuriraju kada se planirane porudžbine učvrste. |
| Upravljanje projektima i računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Broj vaučera, saldo dobavljača vrste transakcije i broj konta ne mogu se stornirati u fakturi za akontaciju/avansnu uplatu izlazne porudžbine. |
| Upravljanje projektima i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktura međukompanijskog dobavljača se pokvari kada je uključena integracija fakture od dobavljača. |
| Upravljanje projektima i računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Kada kreirate nalog troškova projekta, iznos troška se prikazuje u polju **Potraživanje**. |
| Upravljanje projektima i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uslovi plaćanja na projektnim fakturama ne funkcionišu na očekivani način. |
| Upravljanje projektima i računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Vaučeri za vremenski list mogu biti ponovo upotrebljeni kada je sekvenca brojeva podešena kao neprekidna. |
| Upravljanje projektima i računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | Logika ručnog **zadržavanja ne** podudara se sa logikom iznosa automatskog **zadržavanja u** predlogu fakture za ugovor o projektu. |
| Upravljanje projektima i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada je zadržavanje dobavljača izdato, knjiženje vaučera ima netačne dodatne redove. |
| Upravljanje projektima i računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kada se promeni **polje datuma** fakture na stranici **"Kreiranje predloga fakture** ", može doći do sledeće greške: "Referenca objekta nije postavljena na instancu objekta". |
| Upravljanje projektima i računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Do greške dolazi kada pokušate da odobrite list sa vremenom **iz toka posla TSLine**, a za subotu i nedelju postoje smernice lista sa vremenskim listom. |
| Upravljanje projektima i računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta stavke projekta početnog salda je isključena iz **zbira transakcija predloga fakture** kada se izračuna zbir fakture iz predloga fakture. |
| Upravljanje projektima i računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ako je trošak potrošnje u nalogu za proizvodnju projekta 0 (nula), dolazi do sledeće greške kada pokušate da procenite: "Pokušano deljenje nulom". |
| Upravljanje projektima i računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikacija "Project Timesheet Mobile" prestaje da se odaziva Android. Problem je povezan sa **argumentom TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektima i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Nalog integracije operacija projekta ne uspeva kada ga proknjižite jer kontou nedostaju dimenzije. Međutim, konto koji nedostaje dimenzijama nije konto na koji objavljujete. |
| Upravljanje projektima i računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | ToDate **filter** u pretragama se ne može opozvati kada se **ukloni iz dijaloga "Izbor"** na stranici "**Troškovi objave**". |
| Upravljanje projektima i računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Uspostavljanje početnih** vrednosti svih distribucija nije uspelo i prikazuje grešku za listove sa vremenom koji su kreirani za projekat samo **za tip** vremena. |
| Upravljanje projektima i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **"Projekat** " se ne može uređivati u fakturi dobavljača na čekanju kada je artikalu dodeljena kategorija nabavke. |
| Upravljanje projektima i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Okno za navigaciju nedostaje ako niste prijavljeni u operacije projekta Dataverse. |
| Upravljanje projektima i računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Za transakcije korekcije međukompanijskog projekta postoje problemi u odredišnom preduzeću. |
| Upravljanje projektima i računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Troškovi za projekat izračunavaju pogrešnu količinu i cenu troška ako je izlazna porudžbina obrađena **procesom na kraju godine izlazne porudžbine u** glavnoj knjizi. |
| Upravljanje projektima i računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kada se nalog za proizvodnju projekta koji ima naloge za kvalitet prijavi kao završen, dolazi do sledeće greške: "Nema virtuelne transakcije označene transakcijom zaliha." |
| Upravljanje projektima i računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kada se proknjiži faktura za plaćanje u vezi sa projektom, dolazi do sledeće greške: "Nabrojani tekstualni projekat - trošak - artikal ne postoji". |
| Upravljanje projektima i računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirektni troškovi se udvostručuje kada ručno akumulirate prihod. |
| Upravljanje projektima i računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Akumuliranje prihoda i knjiženje PUT ne proizvodi transakcije. |
| Upravljanje projektima i računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija neobrađene cene ne uspe za artikal standardnog troška kada postoji primljena izlazna porudžbina projekta. |
| Upravljanje projektima i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Vrednost koja je stornirana PUT od knjiženja fakture razlikuje se od originalne proknjižene vrednosti PUT od stavke vremena. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Postoji problem knjiženja za fakturisani prihod projekta u primenjenim slučajevima za zadržavanje u kojima transakcije na vaučeru ne balansiraju. |
| Upravljanje projektima i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procene nakon knjiženja predloga fakture blokira uvoz korektivnih redova u projektne operacije. |
| Upravljanje projektima i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmena potpuno fakturisanog zapisa prekretnice ne bi trebalo da bude moguća. |
| Upravljanje projektima i računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kada se koriste automatski troškovi, nije potrebno proknjižiti fakturu međukompanijskog kupca za list sa vremenom i prikazuje se poruka o grešci. |
| Upravljanje projektima i računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa na podprojektu nije ispravno ažurirana. |
| Upravljanje projektima i računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Cena troška po zahtevima artikla se ažurira nabavnom cenom za konsolidovane izlazne porudžbine. |
| Upravljanje projektima i računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Proknjiženi trošak nije tačan nakon što se ažurira nabavna cena i kada je omogućeno upravljanje **promenom** parametara Aktiviraj. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi troškovi korisnika mogu se videti kada tražite kategoriju u mobilnoj aplikaciji "Troškovi". |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netačni iznosi za transakcije dobavljača i transakcije poreza na promet se knjiže iz troška koji je kreiran iz transakcije kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kada osvežite stranice izveštaja o troškovima, prikazuje se nevažna poruka upozorenja. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešna privremena osoba koja vrši odobravanje se koristi kada izbrišete prelaznu osobu koja vrši odobravanje, a zatim ponovo vršite program putem toka posla. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do greške u knjiženju koja je povezana sa podešavanjem kilometraže. |
| Putovanje i trošak | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne ažurira pravno lice kada se neoštećena transakcija ponovo doda izveštaju o troškovima o međukompanijskom trošku. |

### <a name="regulatory-updates"></a>Regulatorne ispravke

Više informacija o regulatornim ispravkama za aplikacije za finansije i operacije potražite u članku [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe možete da se prijavite u Microsoft Dynamics usluge životnog ciklusa (LCS) i koristite alatku za pretraživanje problema da biste prikazali planirane regulatorne ispravke. Pretraga problema vam omogućava da pretražujete po zemlji ili regionu, tipu funkcije i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
