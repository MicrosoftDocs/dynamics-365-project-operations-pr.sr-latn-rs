---
title: Šta je novo ili promenjeno u projektno poslovanje, septembar 2021. za snabdevene/proizvodne scenarije
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju projektnih operacija za scenarije zasnovane na zalihama/proizvodnji u septembru 2021.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916535"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Šta je novo ili promenjeno u projektno poslovanje, septembar 2021. za snabdevene/proizvodne scenarije

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.21
 
## <a name="quality-updates"></a>Ispravke kvaliteta

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
|---|---|---|
| Upravljanje projektima i računovodstvo | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Ako se ulozi Menadžera nabavke da pristup jednom pravnom licu, ona takođe dobija pristup svim projektima u svim pravnim licima. |
| Upravljanje projektima i računovodstvo | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Do problema sa zaokruživanje poreza na dodatu vrednost (PDV) dolazi dok se kreditna napomena rešava u odnosu na originalnu fakturu projekta. |
| Upravljanje projektima i računovodstvo | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Koristite alternativni budžet projekta za proveru budžeta. |
| Upravljanje projektima i računovodstvo | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Grupa **cena po prodajnim** cenama se ne izračunava na strukturi analize rada za citate projekta. |
| Upravljanje projektima i računovodstvo | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | Procena eliminacije ne uspe kada je **omogućena valuta za omogućavanje projektnog ugovora** za funkciju izračunavanja procene. |
| Upravljanje projektima i računovodstvo | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | Faktorizacija poreza na promet po količini se dodaje iznosu prodajne cene kada se porez na korišćenje koristi u grupi poreza na promet u nalogu troškova projekta. |
| Upravljanje projektima i računovodstvo | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | Uslovni porez se ne obračunava ispravno za poslednju uplatu kada se zadržavanje dobavljača i akontacija/avansna uplata primenjuju na fakture izlazne porudžbine. |
| Upravljanje projektima i računovodstvo | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | Praćenje korekcije ne funkcioniše za početne naloge salda. |
| Upravljanje projektima i računovodstvo | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **Dodeljivanje revizije budžeta projekta po periodu** je podeljeno na sve budžetske periode. Kada se dodela prosledi, zapis se ne raščišćaš. |
| Upravljanje projektima i računovodstvo | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Radna knjiženja u glavnoj knjizi (PUT) imaju netačan iznos. |
| Upravljanje projektima i računovodstvo | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | Odobravanje dnevnika "Sat projekta" ne funkcioniše. |
| Upravljanje projektima i računovodstvo | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Prodajna cena korekcije projekta se ne ažurira indirektnim troškovima kada je ograničenje finansiranja neoznačeno. |
| Upravljanje projektima i računovodstvo | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Nije bilo moglo biti kreiran zahtev za artikal kada je zaglavlje tabele "Prodaja" fakturisano, a prateća izlazna porudžbina za postojeće redove završena. |
| Upravljanje projektima i računovodstvo | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Iznos zadržavanja za pravilo o naplati koje ima prekretnicu za drugi projekat nije proknjižen u odgovarajućem ID-u projekta koji je izabran za prekretnicu. Umesto toga, postavljen je sa prvim projektom. |
| Upravljanje projektima i računovodstvo | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Kada izaberete skup **finansijske dimenzije** u predlogu fakture, dolazi do sledeće greške: "Nije moguće baciti objekat tipa 'Dynamics.AX. Application.FormIntControl' da biste otkucali 'Dynamics.AX. Application.FormStringControl'." |
| Upravljanje projektima i računovodstvo | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Izveštaj **o fakturi** projekta preskače redove. |
| Upravljanje projektima i računovodstvo | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Do greške dolazi prilikom izračunavanja kontrole troškova za investicioni projekat. |
| Upravljanje projektima i računovodstvo | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | Metod **ProjTable:: InitFromCustTable - canDeletePostalAddress izaziva** problem sa performansama. |
| Upravljanje projektima i računovodstvo | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Poruka o grešci bi trebalo da bude jasnija od "Neočekivana greška". |
| Upravljanje projektima i računovodstvo | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | Grupna obrada knjiženja fakture projekta i knjiži predlog fakture čak i ako redovi fakture nisu generisani. |
| Upravljanje projektima i računovodstvo | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Do problema sa zaokruživanjem dolazi kada je ključ za konfiguraciju licence u javnom sektoru isključen. Netačan trošak ili prodajna cena se generišu u časovima lista sa vremenom za ugovore koji imaju više izvora osnivača. |
| Upravljanje projektima i računovodstvo | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Prodajna cena projekta u izlaznoj porudžbini fakturisanog projekta se pogrešno izračunava kada je model prodajne cene odnos **"Doprinos"**. |
| Upravljanje projektima i računovodstvo | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Sistem ne smatra aktivne dane između izračunavanja efektivne stope rada zaposlenog. |
| Upravljanje projektima i računovodstvo | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Došlo je do greške prilikom knjiženja u međukompanijskom vremenskom opisu zbog sledeće greške u proveri valjanosti: "Nijedan trgovinski partner nije konfigurisan za pravno lice." |
| Upravljanje projektima i računovodstvo | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | Opis iz izlazne porudžbine koja ima kategoriju troškova nije preuzet na listi proknjiženih transakcija projekta. |
| Upravljanje projektima i računovodstvo | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Postoji netačna konverzija u nalozima artikala koji se knjiže u projekat. |
| Upravljanje projektima i računovodstvo | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Izlaznu porudžbinu možete potvrditi čak i ako je prekoračjen limit finansiranja. |
| Upravljanje projektima i računovodstvo | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | Odeljak **Ispravka/Otkazivanje** fakture na besplatnoj tekstualnoj fakturi nestaje kada je izabran ID projekta. |
| Upravljanje projektima i računovodstvo | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Postoje problemi sa performansama kada se predlog fakture projekta proknjiži iz ulazne porudžbine projekta koja uključuje snabdeven artikal. |
| Upravljanje projektima i računovodstvo | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Nije moguće proknjižiti ulazne fakture projekta jer dolazi do sledeće greške: "Funkcija AccDistProcessorProjectExtension.createForProjectRevenueLine je netačno pozvana." |
| Upravljanje projektima i računovodstvo | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Ažuriranje kreiranja grupnih obrada za procenu projekta da bi se podržalo izvršavanje više podtaskova. |
| Upravljanje projektima i računovodstvo | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Status lista sa vremenom ne može da se ažurira u radnu verziju **kada** se tok posla zaglavi u otkazanom **stanju**. |
| Upravljanje projektima i računovodstvo | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Iznosi zadržavanja se ne izračunavaju u predlogu fakture za kreditnu notu ako postoji više redova. |
| Upravljanje projektima i računovodstvo | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Kada pokušate da promenite iznos na generisanu fakturu iz izlazne porudžbine, dolazi do sledeće greške: "Transakcije na vaučeru ne balansiraju po XX/XX/XXXX. (računovodstvena valuta: 0,00 – valuta za izveštavanje: 0,01).“ |
| Upravljanje projektima i računovodstvo | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Postoji problem sa performansama kada je predlog fakture projekta objavljen u grupnom režimu, zbog spoja sa **generalomJournalAccountEntry**. |
| Upravljanje projektima i računovodstvo | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Postoje problemi sa performansama prilikom objavljenog lista sa vremenom. |
| Upravljanje projektima i računovodstvo | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | Procena troškova hijerarhije strukture radne analize nije ispravno poravnata nakon što se svi zadaci prošire ili nakon ručnog proširenja jednog zadatka. |
| Upravljanje projektima i računovodstvo | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Nije moguće dodati Excel predložak navod projekta u meni "Otvaranje" u **programu Excel**. |
| Upravljanje projektima i računovodstvo | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Broj koji je oslobođen poreza za pravno lice nije uključen u odštampanu fakturu projekta. |
| Upravljanje projektima i računovodstvo | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Finansijski podaci se ne ažuriraju u grešci jedinice zaliha kada se projekat koriguje u odnosu na kreditne redove. |
| Upravljanje projektima i računovodstvo | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Kada primenite KB 461935, ne možete da knjižite procene ako se prebacite na neprekidne sekvence brojeva. |
| Upravljanje projektima i računovodstvo | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager dovodi do** toga da mobilna aplikacija lista vremenskog lista projekta prestane da Android se odaziva. |
| Upravljanje projektima i računovodstvo | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Vrednost koja je stornirana PUT od knjiženja fakture razlikuje se od prvobitno proknjižene vrednosti PUT od stavke vremena. |
| Upravljanje projektima i računovodstvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | U primenjenim slučajevima za zadržavanje, transakcije na vaučeru se ne saočavaju kada se proknjiži fakturisani prihod za projekat. |
| Upravljanje projektima i računovodstvo | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Kada je omogućena **funkcija poboljšanja performansi planiranjem** resursa projekta, decimalne vrednosti se nepravilno zaokružuju za raspoloživost resursa i kapacitet. |
| Upravljanje projektima i računovodstvo | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Kada je **omogućeno kreiranje procena projekta korišćenjem više funkcija** grupnih zadataka, kreiranje procena u grupi koja ima više podtaskova funkcioniše samo za trenutni period. |
| Putovanje i trošak | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Smernice za trebovanje putovanja se zanemaruju, a tok posla se odobrava bez grešaka. |
| Putovanje i trošak | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>Aplikacija "Mobilni troškovi" ne čuva sledeće informacije u redu troškova:</p><ul><li>ID projekta</li><li>Da li je trošak naplativ</li><li>Broj aktivnosti</li></ul> |
| Putovanje i trošak | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Polje Priložene **prijemnice je** podešeno na "Da **"** čak i ako nijedan prijemnica nije priložen redu troška. |
| Putovanje i trošak | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Do greške dolazi kada kategoriju troškova promenite u **ličnu**. |
| Putovanje i trošak | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Ne možete priložiti prijemnicu i urediti nadređeni trošak nakon što se transakcija kreditnom karticom podeli na lični trošak. |
| Putovanje i trošak | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | Smernice troškova za međukompanijske transakcije koje imaju ID projekta ne funkcionišu ispravno. |
| Putovanje i trošak | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Za proknjižene izveštaje o troškovima nedostaju informacije o proknjiženom datumu. |
| Putovanje i trošak | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Postoje problemi sa načinom plaćanja u mobilnoj aplikaciji "Troškovi". |
| Putovanje i trošak | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Putni trebovanje koje je kreirano za jednog radnika može se koristiti za izveštaj o troškovima drugog radnika pre datuma delegata. |
| Putovanje i trošak | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Kada kreirate trošak, promene vrednosti finansijske dimenzije se ne ažuriraju ispravno na nivou obračunske raspodele u radnom prostoru **za upravljanje** troškovima. |
| Putovanje i trošak | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Status odobravanja reda glavnih troškova se ne sinhronizuje sa statusom odobravanja reda stavke. |
| Putovanje i trošak | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Do greške dolazi ako proknjižite izveštaj o troškovima i omogući se oporavak poreza. |
| Putovanje i trošak | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Delegat ne može da izbriše dokumentaciju o troškovima za zaposlenog koji je dobio otkaz. |
| Putovanje i trošak | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | Brisanje reda troškova traje duže od očekivanog i utiče na performanse. |
| Putovanje i trošak | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans izaziva** zapis bez dece **TaxUncommitted**, jer se briše **samo SourceDocumentLine**. |
| Putovanje i trošak | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne **poštuje trvExpTrans.ReferenceDataAreaId da** bi kreirao novi niz brojeva. |

## <a name="regulatory-updates"></a>Regulatorne ispravke

Više informacija o regulatornim ispravkama za aplikacije za finansije i operacije potražite u članku [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe možete da se prijavite u Microsoft Dynamics usluge životnog ciklusa (LCS) i koristite alatku za pretraživanje problema da biste prikazali planirane regulatorne ispravke. Pretraga problema vam omogućava da pretražujete po zemlji ili regionu, tipu funkcije i izdanju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
