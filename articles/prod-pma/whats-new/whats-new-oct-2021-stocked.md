---
title: Šta je novo ili promenjeno u usluzi Project Operations u oktobru 2021. za scenarije zasnovane na zalihama/proizvodnji
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Project Operations za oktobar 2021. za scenarije zasnovane na zalihama/proizvodnji.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Šta je novo ili promenjeno u usluzi Project Operations u oktobru 2021. za scenarije zasnovane na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.22
 
## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
|--------------|------------------|----------------|
| Upravljanje projektima i računovodstvo | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Rad u toku za projekat (WIP) i akumulirani iznosi prihoda nisu ispravno stornirani kada se proknjiži faktura međukompanijskog klijenta. |
| Upravljanje projektima i računovodstvo | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funkcionalnost **Sprečavanje zatvaranja projekta ako postoje otvorene transakcije** ne funkcioniše. |
| Upravljanje projektima i računovodstvo | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Klasifikacija naplate na fakturi bez ulazne porudžbine ne popunjava automatski dimenzije iz projekata kada je ta funkcionalnost omogućena. |
| Upravljanje projektima i računovodstvo | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | U scenarijima rada izvan preduzeća (WIP) i akumulirani iznosi prihoda nisu ispravno stornirani kada se proknjiži faktura za projekat. |
| Upravljanje projektima i računovodstvo | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Vrednosti dugovanja i potraživanja se menjaju kada se Microsoft Excel programski dodatak koristi sa dnevnikom troškova projekta, a polje **Vrsta računa za prebijanje dugova** je podešeno na **Projekat**. |
| Upravljanje projektima i računovodstvo | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Iznos koji se knjiži u projektnim transakcijama je precenjen u porudžbenici projekta koja uključuje snabdevene artikle i koji ima iznose poreza koji se ne može odbiti kada je označeno **UseTax**. |
| Upravljanje projektima i računovodstvo | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Sistem deli iznos između izveštaja o dobitku i gubitku projekta i WIP izveštaja za projekat. |
| Upravljanje projektima i računovodstvo | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Inventar na zalihama je netačan nakon korigovanja zahteva za delimično vraćeni artikal. |
| Upravljanje projektima i računovodstvo | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Nazivi resursa se dupliraju u Project Operations kada se uređuju u programu Microsoft Project. |
| Upravljanje projektima i računovodstvo | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Izveštaji o troškovima između preduzeća imaju cene fakture dobavljača na čekanju dugovanja između preduzeća prvo se knjiže u tipu knjiženja **Cena WIP projekta**. Međutim, tokom obrade, cene vezane za procenu se knjiže u vrstu knjiženja **Cena projekta** umesto u očekivanu vrstu knjiženja **Cena između kompanija**. |
| Upravljanje projektima i računovodstvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Rezultati zadržavanja dobavljača u transakcijama troškova projekta nisu prikazani. |
| Upravljanje projektima i računovodstvo | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Vremenski raspored mora zaokružiti iznos transakcije u valuti transakcije na određeni broj decimalnih mesta za sve računovodstvene distribucije i stavke dodele opšteg dnevnika. |
| Upravljanje projektima i računovodstvo | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Količine zahteva za artikal za projekat se automatski ažuriraju kada se planirane porudžbine potvrde. |
| Upravljanje projektima i računovodstvo | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Broj vaučera, saldo dobavljača za vrstu transakcije i broj konta ne mogu se stornirati u avansnoj fakturi porudžbenice. |
| Upravljanje projektima i računovodstvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Međukompanijska faktura dobavljača ima grešku kada je uključena integracija fakture dobavljača. |
| Upravljanje projektima i računovodstvo | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Kada kreirate dnevnik troškova projekta, iznos cene se prikazuje u polju **Kredit**. |
| Upravljanje projektima i računovodstvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Uslovi plaćanja na projektnim fakturama ne funkcionišu na očekivani način. |
| Upravljanje projektima i računovodstvo | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Vaučeri za vremenski raspored mogu biti ponovo upotrebljeni kada je sekvenca brojeva podešena kao neprekidna. |
| Upravljanje projektima i računovodstvo | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCUSKA: Logika **Iznosa ručnog zadržavanja** ne podudara se sa logikom **Iznosa automatskog zadržavanja** u predlogu fakture za projektni ugovor. |
| Upravljanje projektima i računovodstvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kada je zadržavanje dobavljača izdato, knjiženje vaučera ima netačne dodatne redove. |
| Upravljanje projektima i računovodstvo | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Kada se promeni polje **Datum fakture** na stranici **Kreiranje predloga fakture**, može doći do sledeće greške: „Referenca objekta nije postavljena na instancu objekta“. |
| Upravljanje projektima i računovodstvo | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Do greške dolazi kada pokušate da odobrite vremenski raspored iz toka posla **TSLine**, a za subotu i nedelju postoje smernice za vremenski raspored. |
| Upravljanje projektima i računovodstvo | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Vrsta stavke projekta za početni saldo je isključena iz **Rezimei transakcija predloga fakture** kada se izračunava zbir fakture iz predloga fakture. |
| Upravljanje projektima i računovodstvo | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Ako je cena potrošnje u nalogu za proizvodnju projekta 0 (nula), dolazi do sledeće greške kada pokušate da procenite: „Pokušano je deljenje nulom“. |
| Upravljanje projektima i računovodstvo | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Aplikacija Vremenski raspored za projekat za mobilne telefone za operativni sistem Android prestaje da reaguje. Problem je povezan sa argumentom **TimeEntryDataManager ArgumentNullException**. |
| Upravljanje projektima i računovodstvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Dnevnik integracije programa Project Operations ima grešku kada ga proknjižite jer kontu nedostaju dimenzije. Međutim, konto kojem nedostaju dimenzije nije konto u kom knjižite. |
| Upravljanje projektima i računovodstvo | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Filter **ToDate** u pretragama se ne briše kada ga uklonite iz dijaloga **Izbor** na stranici **Knjiženje cene**. |
| Upravljanje projektima i računovodstvo | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Uspostavljanje početnih vrednosti svih distribucija** nije uspelo i prikazuje grešku za vremenske rasporede koji su kreirani za projekat tipa **Samo vreme**. |
| Upravljanje projektima i računovodstvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Kartica **Projekat** ne može da se uređuje na fakturi dobavljača na čekanju kada je kategorija nabavke dodeljena stavci. |
| Upravljanje projektima i računovodstvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Okno za navigaciju nedostaje ako niste prijavljeni u Project Operations Dataverse. |
| Upravljanje projektima i računovodstvo | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Za transakcije korekcije međukompanijskog projekta postoje problemi u odredišnoj kompaniji. |
| Upravljanje projektima i računovodstvo | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Dodeljeni troškovi za projekat izračunavaju pogrešnu količinu i cenu koštanja ako je porudžbenicu obradila **Obrada porudžbenica na kraju godine** u glavnoj knjizi. |
| Upravljanje projektima i računovodstvo | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Kada se nalog za proizvodnju projekta koji ima naloge za kvalitet prijavi kao završen, dolazi do sledeće greške: „Nema virtuelne transakcije označene transakcijom inventara.“ |
| Upravljanje projektima i računovodstvo | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Kada se proknjiži faktura dugovanja u vezi sa projektom, dolazi do sledeće greške: "„Nabrojani tekst projekta – cena – stavka ne postoji“. |
| Upravljanje projektima i računovodstvo | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirektne cene se udvostručuju kada ručno akumulirate prihod. |
| Upravljanje projektima i računovodstvo | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Akumuliranje prihoda i WIP knjiženje ne proizvode transakcije. |
| Upravljanje projektima i računovodstvo | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivacija cene na čekanju ne uspeva za artikal standardne cene kada postoji primljena porudžbenica za projekat. |
| Upravljanje projektima i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Stornirana vrednost za WIP iz knjiženja na fakturi razlikuje se od prvobitno knjižene vrednosti za WIP iz stavke vremena. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Postoji problem sa knjiženjem za prihod fakturisan po projektu u primenjenim slučajevima zadržavanja gde se transakcije na vaučeru ne saldiraju. |
| Upravljanje projektima i računovodstvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Kreiranje procene nakon knjiženja predloga fakture blokira uvoz korektivnih redova u Project Operations. |
| Upravljanje projektima i računovodstvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Izmena zapisa potpuno fakturisane kontrolne tačke ne bi trebalo da bude moguća. |
| Upravljanje projektima i računovodstvo | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Kada se koriste automatski troškovi, nije moguće proknjižiti fakturu međukompanijskog klijenta za vremenski raspored i prikazuje se poruka o grešci. |
| Upravljanje projektima i računovodstvo | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adresa na potprojektu nije ispravno ažurirana. |
| Upravljanje projektima i računovodstvo | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Cena koštanja po zahtevima artikla se ažurira nabavnom cenom za konsolidovane porudžbenice. |
| Upravljanje projektima i računovodstvo | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Proknjižena cena nije tačna nakon što se ažurira nabavna cena i kada je omogućen parametar **Aktiviranje upravljanja promenom**. |
| Putovanje i trošak | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Svi troškovi korisnika mogu se videti kada tražite kategoriju u mobilnoj aplikaciji Troškovi. |
| Putovanje i trošak | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Netačni iznosi za transakcije dobavljača i poreza na promet koji su knjiženi iz troška koji je nastao transakcijom kreditnom karticom. |
| Putovanje i trošak | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Kada osvežite stranice izveštaja o troškovima, prikazuje se nevažna poruka upozorenja. |
| Putovanje i trošak | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pogrešna privremena osoba koja vrši odobravanje se koristi kada izbrišete privremenu osobu koja vrši odobravanje, a zatim ponovo pošaljete putem toka posla. |
| Putovanje i trošak | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Dolazi do greške u knjiženju u vezi sa podešavanjem kilometraže. |
| Putovanje i trošak | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribucija ne ažurira pravno lice kada se nepriložena transakcija ponovo doda izveštaju o troškovima o međukompanijskom trošku. |

### <a name="regulatory-updates"></a>Regulatorne ispravke

Za informacije o regulatornim ispravkama za aplikacije za finansije i operacije, pogledajte članak [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe se možete prijaviti u Microsoft Dynamics Lifecycle Services (LCS) i koristiti alatku za pretragu problema da biste pregledali planirane regulatorne ispravke. Pretraga problema vam omogućava pretragu po zemlji ili regionu, tipu funkcije i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
