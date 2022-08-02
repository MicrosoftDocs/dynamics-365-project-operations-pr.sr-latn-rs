---
title: Šta je novo ili promenjeno u usluzi Project Operations u julu 2021. za scenarije zasnovane na zalihama/proizvodnji
description: Ovaj članak pruža informacije o kvalitetnim ispravkama dostupnim u izdanju projektnih operacija u julu 2021.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028857"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Šta je novo ili promenjeno u usluzi Project Operations u julu 2021. za scenarije zasnovane na zalihama/proizvodnji

_**Odnosi se na:** Project Operations za scenarije zasnovane na zalihama/proizvodnji_

Ovaj članak se odnosi na sledeće Dynamics 365 Project Operations komponente i verzije:

- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.20
 
### <a name="quality-updates"></a>Ispravke kvaliteta
                                                                                                                                                                                  
| Oblast funkcija                      | Referentni broj| Ispravka kvaliteta                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Upravljanje projektima i računovodstvo | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Zapisi obaveza troškova iz zahteva za kupovinu brišu se čim se nalog za kupovinu oslobodi problema zahteva za kupovinu.                                                                           |
| Upravljanje projektima i računovodstvo | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Dolazi do dve validacije budžeta pri zahtevu za kupovinu. Ovo dupliranje znači da se zahtev ne može zatvoriti i da se ne kreira odgovarajući nalog za kupovinu.                                                                                                                        |
| Upravljanje projektima i računovodstvo | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Pravilo za obračun **Procenat za obračun** nije moglo da se dovrši zbog problema sa zaokruživanjem.                                                                              |
| Upravljanje projektima i računovodstvo | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Kada prilagodite transakciju i procenat sadrži decimale, trošak i prodajna cena se ne prilagođavaju ispravno.                                      |
| Upravljanje projektima i računovodstvo | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Istraživač izvora računovodstva prikazuje sate za jednu stavku rasporeda vremena za više stavki rasporeda vremena sa različitim aktivnostima.                                      |
| Upravljanje projektima i računovodstvo | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Sačuvani prikazi i personalizacija detalja stavke rasporeda vremena uzrokuju da sistem uvek otvara detalje za prvi rasporeda vremena na listi kada pokušava da otvori rasporeda vremena.  |
| Upravljanje projektima i računovodstvo | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Osnovni čvor projekta nestaje, a zapisi strukturne analize posla se brišu nakon uvoza.                                                                                             |
| Upravljanje projektima i računovodstvo | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Kada se stavke prime i izdaju delimično iz zahteva za stavkom, sistem ažurira pogrešan bilans budžetske potrošnje. |
| Upravljanje projektima i računovodstvo | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Nalozi za avansnu kupovinu projekta ne prikazuju ispravno ukupne vrednosti u oknu **Ukupni iznosi** ili u mreži **Faktura na čekanju**.                                                                  |
| Upravljanje projektima i računovodstvo | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Prilikom zatvaranja zaliha, prilagođavanja troškova stavki projekta knjiže se na bilansni račun umesto na račun dobiti i gubitka.                                                            |
| Upravljanje projektima i računovodstvo | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Vaučer za transakcije proknjižen u projektu i vaučer za procenu koriste USD kao računovodstvenu valutu, ali iznos pokazuje koliki bi bio ekvivalent u CAD.              |
| Upravljanje projektima i računovodstvo | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Dodeljeni troškovi sa zahtevom za stavkom i porudžbenicom su pogrešni u procesu fakturisanja naloga za kupovinu sa delom računa za proizvod i fakturisanjem dela.       |
| Upravljanje projektima i računovodstvo | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Prilagođavanje projekta ne ažurira ispravno iznos prodaje indirektnim troškovima.                                                                                    |
| Upravljanje projektima i računovodstvo | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabeli **Raspored vremena** nedostaje definisana relacija sa prikazom **Radnik/Resurs**.                                                                                   |
| Upravljanje projektima i računovodstvo | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nije moguće popuniti polje **Broj aktivnosti** kada ga izaberete iz padajućeg menija za raspored vremena u okviru preduzeća.                                                                 |
| Upravljanje projektima i računovodstvo | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nije moguće dodati personalizovano polje **Svrha** ili **Opis aktivnosti** za sledeće stranice: **Transakcija proknjižena u projektu**, **Kreiranje predloga fakture** ili **Predlog fakture**.  |
| Upravljanje projektima i računovodstvo | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Navedena je pogrešna kontrola datuma isporuke kada kreirate zahteve za stavkom pomoću upravljanja podacima (**ProjSalesItemRequirementEntity**).                                              |
| Upravljanje projektima i računovodstvo | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Kada izaberete ID ugovora za projekat u usluzi Finance, Project Operations integrisano okruženje otvara stranicu da kreira novi zapis umesto da otvori postojeći ugovor za projekat.                                                                                                                 |
| Upravljanje projektima i računovodstvo | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Oznaka „@SYS4083080“ („Nije moguće pronaći jedinstveni zapis radnika koji odgovara unetim vrednostima“) nije prevedena na danski.                                |
| Upravljanje projektima i računovodstvo | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Polje **Grupa poreza na promet stavki** se ne može uređivati na predlogu fakture.                                                                               |
| Upravljanje projektima i računovodstvo | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Dodeljeni troškovi su precenjeni sa iznosima poreza koji se ne mogu odbiti.                                                                                                    |
| Upravljanje projektima i računovodstvo | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Knjiženje rasporeda vremena sa više projekata unutar preduzeća i različitih finansijskih aspekata generiše neočekivane vrednosti u glavnoj knjizi.                             |
| Upravljanje projektima i računovodstvo | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Stavke predloga fakture se dupliraju zbog više instanci periodičnih procesa, pri čemu se **uvoz iz pripreme** pokreće istovremeno.                                      |
| Upravljanje projektima i računovodstvo | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Dolazi do greške u knjiženju predloga fakture sa kreditnim zapisom, tako da transakcije na vaučeru nisu poravnate.    |
| Upravljanje projektima i računovodstvo | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Troškovi angažovani na projektu postaju netačni nakon objavljivanja faktura na čekanju.                                                                             |
| Upravljanje projektima i računovodstvo | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Ne možete da kreirate kreditni zapis za ulaznu porudžbinu za projekat kada je porez u valuti koja se razlikuje od valute preduzeća.                                      |
| Upravljanje projektima i računovodstvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Brisanjem ugovora briše se i adresa povezana sa klijentom.                                                                                     |
| Upravljanje projektima i računovodstvo | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Nije moguće proknjižiti predlog fakture koji je rezultat negativne korekcije transakcije vremena.                                                                    |
| Putovanje i trošak                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Porez se različito obračunava u izveštajima o troškovima.                                                                                                                  |
| Putovanje i trošak                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Ispravka izdanja **DB72_Expense.updateTrvExpTransProjTransId()** ne omogućava da **trvExpTrans.ReferenceDataAreaId** kreira novu sekvencu brojeva.                    |
| Putovanje i trošak                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Prijavljeni iznos se ne prikazuje uz obavezno polje.                                                                                                             |
| Putovanje i trošak                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Poboljšanja u performansama povezivanja troška sa izveštajem o troškovima pomoću ponovo osmišljenog korisničkog interfejsa za troškove.                                                            |
| Putovanje i trošak                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Možete da izbrišete proknjižene izveštaje o troškovima.                                                                                           |
| Putovanje i trošak                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Poruka smernica o troškovima se prikazuje više puta.                                                                                                       |
| Putovanje i trošak                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Polje **Način plaćanja** je uključeno u okno **Novi trošak**.                                                                                                      |
| Putovanje i trošak                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Alatka **Resetovanje statusa dokumenta troškova** bi trebalo da resetuje status izveštaja o troškovima na **radnu verziju** ako tok posla ne bude pronađen. 

### <a name="regulatory-updates"></a>Regulatorne ispravke
Više informacija o regulatornim ispravkama za aplikacije za finansije i operacije potražite u članku [Regulatorne ispravke](/dynamics365/finance/localizations/regulatory-updates). Takođe se možete prijaviti u Lifecycle Services (LCS) i pregledati planirane regulatorne ispravke pomoću alatke za pretragu problema. Pretraga problema vam omogućava pretragu po zemlji, tipu funkcije i izdanju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
