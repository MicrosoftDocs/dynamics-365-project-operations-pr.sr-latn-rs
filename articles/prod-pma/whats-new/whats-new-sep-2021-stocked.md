---
title: Šta je novo ili promenjeno u usluzi Project Operations u septembru 2021. za scenarije zasnovane na zalihama/proizvodnji
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Project Operations za septembar 2021. za scenarije zasnovane na zalihama/proizvodnji.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029869"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Šta je novo ili promenjeno u usluzi Project Operations u septembru 2021. za scenarije zasnovane na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.21
 
## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
|---|---|---|
| Upravljanje projektima i računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Ako je ulozi menadžera kupovine dat pristup jednom pravnom licu, on takođe dobija pristup svim projektima u svim pravnim licima. |
| Upravljanje projektima i računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Do problema sa zaokruživanjem poreza na dodatu vrednost (PDV) dolazi dok se odobrenje izmiruje prema originalnoj fakturi projekta. |
| Upravljanje projektima i računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Koristite alternativni budžet projekta za proveru budžeta. |
| Upravljanje projektima i računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grupa cena **Prodajna cena sata** se ne izračunava na strukturnoj analizi posla za ponude za projekat. |
| Upravljanje projektima i računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Eliminisanje procene ne uspeva kada se funkcija **Omogući valutu ugovora za projekat za izračunavanje procene** omogući. |
| Upravljanje projektima i računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija poreza na promet po količini se dodaje iznosu prodajne cene kada se porez na korišćenje koristi u grupi poreza na promet u dnevniku troškova projekta. |
| Upravljanje projektima i računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Uslovni porez nije pravilno izračunat za poslednju uplatu kada se odlaganje dobavljača i avansno plaćanje primenjuju na fakture porudžbenice. |
| Upravljanje projektima i računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Praćenje korekcije ne funkcioniše za dnevnike početnog salda. |
| Upravljanje projektima i računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dodela revizije budžeta projekta po periodu** je podeljena na sve budžetske periode. Kada se dodela prosledi, zapis se ne briše. |
| Upravljanje projektima i računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Knjiženja rada u toku (WIP) u glavnoj knjizi imaju netačan iznos. |
| Upravljanje projektima i računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobrenje za dnevnih sati projekta ne funkcioniše. |
| Upravljanje projektima i računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cena korekcije projekta se ne ažurira indirektnim troškovima kada ograničenje finansiranja nije označeno. |
| Upravljanje projektima i računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Nije moguće kreirati zahtev za artikal kada je zaglavlje tabele Prodaja fakturisano, a prateća izlazna porudžbina za postojeće stavke završena. |
| Upravljanje projektima i računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Iznos zadržavanja za pravilo naplate koje ima kontrolnu tačku za drugi projekat nije proknjižen u odgovarajućem ID-u projekta koji je izabran za kontrolnu tačku. Umesto toga, proknjižen je sa prvim projektom. |
| Upravljanje projektima i računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kada izaberete **Skup finansijskih aspekata** na predlogu fakture, pojavljuje se sledeća greška: „Nije moguće konvertovati objekat tipa 'Dynamics.AX.Application.FormIntControl' u tip 'Dynamics.AX.Application.FormStringControl'.“ |
| Upravljanje projektima i računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Izveštaj **Faktura projekta** preskače stavke. |
| Upravljanje projektima i računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Do greške dolazi prilikom izračunavanja kontrole troškova za investicioni projekat. |
| Upravljanje projektima i računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metod **ProjTable::InitFromCustTable - canDeletePostalAddress** dovodi do problema sa performansama. |
| Upravljanje projektima i računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Poruka o grešci bi trebalo da bude jasnija od „Neočekivana greška“. |
| Upravljanje projektima i računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Grupni posao knjiženja fakture projekta obrađuje i knjiži predlog fakture čak i ako stavke faktura nisu generisane. |
| Upravljanje projektima i računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Do problema sa zaokruživanjem dolazi kada je ključ za konfiguraciju licence u javnom sektoru isključen. Netačan trošak ili prodajna cena se generišu u časovima vremenskog rasporeda za ugovore koji imaju više izvora finansiranja. |
| Upravljanje projektima i računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cena projekta u fakturisanoj porudžbenici projekta pogrešno se izračunava kada je model prodajne cene **Odnos doprinosa**. |
| Upravljanje projektima i računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem ne smatra aktivne dane koji su između kada izračunava efektivne stope rada za zaposlenog. |
| Upravljanje projektima i računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Došlo je do greške prilikom knjiženja u međukompanijskom vremenskom rasporedu zbog sledeće greške u proveri valjanosti: „Nijedan trgovinski partner nije konfigurisan za pravno lice.“ |
| Upravljanje projektima i računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz porudžbenice koja ima kategoriju troškova nije preuzet na listi proknjiženih transakcija projekta. |
| Upravljanje projektima i računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Postoji netačna konverzija u dnevnicima artikala koji se knjiže u projekat. |
| Upravljanje projektima i računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Porudžbenicu možete potvrditi čak i ako je prekoračen limit finansiranja. |
| Upravljanje projektima i računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Odeljak **Korekcija/Otkazivanje fakture** na fakturi bez ulazne porudžbine nestaje kada je izabran ID projekta. |
| Upravljanje projektima i računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Postoje problemi sa performansama kada se predlog fakture projekta proknjiži iz prodajnog naloga projekta koji uključuje artikal na zalihama. |
| Upravljanje projektima i računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Fakture nabavke za projekat ne mogu biti proknjižene jer dolazi do sledeće greške: „Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine je pogrešno pozvana.“ |
| Upravljanje projektima i računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Ažurirajte na kreiranje grupnih poslova procene projekta za podršku pri izvršavanju više podzadataka. |
| Upravljanje projektima i računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status vremenskog rasporeda ne može da se ažurira u **Radnu verziju** kada se tok posla zaglavi u statusu **Otkazano**. |
| Upravljanje projektima i računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Iznosi zadržavanja se ne izračunavaju u predlogu fakture za kreditnu notu ako postoji više redova. |
| Upravljanje projektima i računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kada pokušate da promenite iznos na generisanoj fakturi iz porudžbenice, dolazi do sledeće greške: „Transakcije na vaučeru ne saldiraju prema XX/XX/XXXX. (računovodstvena valuta: 0,00 – valuta za izveštavanje: 0,01).“ |
| Upravljanje projektima i računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Postoji problem sa performansama kada je predlog fakture projekta proknjižen u grupnom režimu, zbog spajanja sa **GeneralJournalAccountEntry**. |
| Upravljanje projektima i računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Postoje problemi sa performansama prilikom knjiženja vremenskog rasporeda. |
| Upravljanje projektima i računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Hijerarhija procene troškova strukturne analize posla nije ispravno usklađena nakon što se svi zadaci prošire ili nakon ručnog proširenja jednog zadatka. |
| Upravljanje projektima i računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Nije moguće dodati Excel predložak ponude projekta u meni **Otvori u programu Excel**. |
| Upravljanje projektima i računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Broj oslobađanja od poreza za pravno lice nije uključeno na štampanoj fakturi za projekat. |
| Upravljanje projektima i računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Kada se projekat usklađuje u odnosu na kreditne redove, u jedinici inventara se ne ažuriraju finansijski podaci. |
| Upravljanje projektima i računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Kada primenite KB 461935, ne možete da knjižite procene ako se prebacite na kontinuirane sekvence brojeva. |
| Upravljanje projektima i računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** dovodi do prestanka reagovanja aplikacije Vremenski raspored projekta za mobilne uređaje za operativni sistem Android. |
| Upravljanje projektima i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Stornirana vrednost za WIP iz knjiženja na fakturi razlikuje se od prvobitno knjižene vrednosti za WIP iz stavke vremena. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | U primenjenim slučajevima zadržavanja, transakcije na vaučeru se ne saldiraju kada se proknjiži fakturisani prihod za projekat. |
| Upravljanje projektima i računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kada je omogućena funkcija **Poboljšanje performansi planiranja resursa projekta**, decimalne vrednosti se nepravilno zaokružuju za raspoloživost i kapacitet resursa. |
| Upravljanje projektima i računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kada je omogućena funkcija **Kreiranje procena projekta korišćenjem više grupnih zadataka**, kreiranje procena u grupi koja ima više podzadataka funkcioniše samo za trenutni period. |
| Putovanje i trošak | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Smernice zahteva za putovanja se zanemaruju, a tok posla se odobrava bez grešaka. |
| Putovanje i trošak | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija Troškovi za mobilne uređaje ne čuva sledeće informacije na stavci troška:</p><ul><li>ID projekta</li><li>Da li je trošak naplativ</li><li>Broj aktivnosti</li></ul> |
| Putovanje i trošak | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Polje **Priložene priznanice** podešeno je na **Da**, čak i ako stavci troškova nije priložena nijedna priznanica. |
| Putovanje i trošak | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Dolazi do greške kada promenite kategoriju troškova u **Lični**. |
| Putovanje i trošak | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Ne možete da priložite priznanicu i uredite nadređeni trošak nakon što se transakcija podeli na lični trošak. |
| Putovanje i trošak | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Politika troškova za međukompanijske transakcije koje imaju ID projekta ne radi ispravno. |
| Putovanje i trošak | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Informacije o datumu knjiženja nedostaju za proknjižene izveštaje o troškovima. |
| Putovanje i trošak | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | U aplikaciji za mobilne uređaje za troškove postoje problemi sa načinom plaćanja. |
| Putovanje i trošak | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Zahtev za putovanje koji je kreiran za jednog radnika može se koristiti za izveštaj o troškovima drugog radnika pre datuma delegiranja. |
| Putovanje i trošak | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kada kreirate trošak, promene vrednosti finansijske dimenzije ne ažuriraju se na odgovarajući način na nivou računovodstvene distribucije u radnom prostoru **Upravljanje troškovima**. |
| Putovanje i trošak | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status odobrenja glavne linije troškova se ne sinhronizuje sa statusom odobrenja toka posla po stavkama. |
| Putovanje i trošak | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Do greške dolazi ako proknjižite izveštaj o troškovima i omogućite povraćaj poreza. |
| Putovanje i trošak | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegat ne može da izbriše dokumentaciju o troškovima za zaposlenog koji je dobio otkaz. |
| Putovanje i trošak | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje stavke troška traje duže od očekivanog i utiče na performanse. |
| Putovanje i trošak | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** dovodi do nasleđenog zapisa **TaxUncommitted**, jer se briše samo **SourceDocumentLine**. |
| Putovanje i trošak | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne poštuje **trvExpTrans.ReferenceDataAreaId** za kreiranje novog broja sekvence. |

## <a name="regulatory-updates"></a>Regulatorne ispravke

Za informacije o regulatornim ispravkama za aplikacije za finansije i operacije, pogledajte članak [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe se možete prijaviti u Microsoft Dynamics Lifecycle Services (LCS) i koristiti alatku za pretragu problema da biste pregledali planirane regulatorne ispravke. Pretraga problema vam omogućava pretragu po zemlji ili regionu, tipu funkcije i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
