---
title: Šta je novo u septembru 2022. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama
description: Ovaj članak pruža informacije o kvalitetnim ispravkama koje su dostupne u izdanju korporacije Microsoft u septembru Dynamics 365 Project Operations 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621374"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u septembru 2022. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije korporacije Microsoft Dynamics 365 Project Operations:

- Operacije projekta u verziji Dataverse okruženja 4.46.0.60
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzija 10.0.29

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Ime funkcije | Više informacija |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | **Revizija i aktiviranje ponuda**<br>Projektne operacije donose punu podršku procesa prodaje. Ponude projekta se mogu aktivirati tako da predstavljaju stanje u kojem je ponuda samo za čitanje i kada se rediguje. Aktivirane ponude se mogu korigovati da bi se kreirale nove ponude koje imaju postepeni broj revizije. Aktivirane ponude projekta ili revizije ponuda mogu biti zatvorene kao osvojene ili izgubljene. | [Aktiviranje i korigovanje ponude za projekat](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cena | **Podrazumevana agnostički cena vremenske zone**<br>Projektne operacije su uvele koncept agnostičnog datuma vremenske zone na svim stvarnim projektima. Novo polje Datum transakcije **je sada dostupno** u redovima naloga i stvarnim vrednostima i koristiće se za skladištenje datuma kada je transakcija izvršena, ali bez konvertovanja tog datuma u koordinirano univerzalno vreme. Ovaj datum će se koristiti za nizvodne procese kao što su podrazumevana cena i kreiranje faktura. | <p>[Utvrđivanje stope troškova za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Utvrđivanje prodajnih cena za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Naplata i određivanje cena | **Datum-efektivna cena zamenjuje u projektnom poslovanju**<br>Zamene cena koje su efektivne za datum obezbeđuju način da se zamene ili promene određene cene u cenovnik. | [Premošćava cena koja je efektivna](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podizvođača | **Sravnjenje podizvođači i sravnjenje fakture dobavljača**<br>Ova funkcija omogućava kupcima da kreiraju podizvođači za vreme nabavke, kategorije troškova i materijale koji se koriste za rad na projektu. Takođe omogućava kupcima da zabeleže, u aplikacijama za finansije i operacije, fakture dobavljača koje će biti dostupne menadžerima projekta Dataverse radi provere. | <p>[Upravljanje podizvođačima](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreiranje faktura prodavca](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Vreme i trošak | **Globalna osoba koja vrši odobravanje**<br>Ova funkcija omogućava nezavisnom prodavcu softvera (ISV) i centralizovano odobravanje, bez obzira na status člana projekta ili tima u projektu. | [Bezbednost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje troškovima | **Mogućnost knjiženja odgovornosti troškova u valuti dobavljača**<br>Ova funkcija omogućava knjiženje izveštaja o troškovima u valuti dobavljača za način plaćanja gotovinom. | [Mogućnost knjiženja odgovornosti troškova u valuti dobavljača](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabavka projekata | **Plaćanje prilikom plaćanja uplatama dobavljača**<br>Ova funkcija omogućava da se funkcija "Plati kada se plati(PWP)" koristi sa ne-berzanskim okruženjima projektnih operacija. Omogućava da se uplate dobavljača blokiraju/zadržavaju, na osnovu uslova zadržavanja, sve dok se uplata ne primi od kupca. | [Plaćanje prilikom plaćanja uplatama dobavljača](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabavka projekata | **Trebovanja nabavke projekta**<br>Ova funkcija omogućava korisnicima da kreiraju izlazne porudžbine vezane za projekat u pravnim licima u kojima je omogućena Dynamics 365 Customer Engagement projekta. Izlazne porudžbine projekta se mogu koristiti za zapisivanje nenapuštene nabavke materijala u odnosu na projekat od strane odeljenja za nabavke persona. Izlazne porudžbine projekta neće biti sinhronizovane sa Dataverse. Međutim, virtuelni entitet možete koristiti za površinu redova izlazne porudžbine projekta za informacije Dataverse o menadžeru projekta. Trošak fakture dobavljača povezan sa projektom je integrisan sa entitetom Project Actuals u programu Dataverse. Trošak projekta se zapisuje u podstanar projekta pomoću naloga za integraciju operacija projekta. | |

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape sa dva pisanja koje su izmenjene ili dodate u izdanju projektnih operacija u septembru 2022.

| Mapa entiteta | Ažurirana verzija | komentara |
| -------------- | ------------------- | ------------|
| Project Operations stvarne vrednosti integracije (msdyn_actuals) | 1.0.0.15 | Ova mapa podržava obradu stvarnih podizvođačima sa operacijama projekta za scenarije zasnovane na resursima. |
| Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices) | 1.0.0.2 | Ova mapa podržava obradu stvarnih podizvođačima sa operacijama projekta za scenarije zasnovane na resursima. |
| Project Operations entitet izvoza reda fakture prodavca (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ova mapa podržava obradu stvarnih podizvođačima sa operacijama projekta za scenarije zasnovane na resursima. |

Uvek pokrenite najnoviju verziju mape u okruženju i omogućite sve povezane mape tabela dok ažurirate rešenje za projektne operacije Dataverse i verziju finansijskog rešenja. Neke funkcije i mogućnosti možda neće ispravno funkcionisati ako najnovija verzija mape nije aktivirana. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele bez okvira, ponovo primenite promene. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem prilikom početka mape, sledite uputstva [u problemu sa kolonama tabele koje nedostaju u odeljku mape](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanja.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2754422 | Procene materijala i troškova se ne slivaju u finansije kada se projekti kopiraju u Dataverse programu. |
| Vreme i trošak | 2787409 | Osoba koja ne važi može da odobri unos vremena koje nije projektno. |
| Upravljanje mogućnostima za poslovanje | 2788907 | Ažurirana poruka o grešci prilikom provere valjanosti jedinstvenosti za redove porudžbine koji uključuju zastavice. |
| Vreme i trošak | 2842253 | Bez načina rukovanja izuzetkom za odobravanje vremena. |
| Naplata i određivanje cena | 2844181 | Ako ne dobijete ID korelacije, blokira se kreiranje fakture. |
| Naplata i određivanje cena | 2876628 | QLD, CLD - Procena rešenja cenovnog lista treba da koristi zastarela polja opsega datuma cenovnik. |
| Podizvođača | 2893222 | Ako nije navedena uloga za red podizvođači, trebalo bi da bude moguće izabrati taj red u članu tima za bilo koju ulogu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u finansijama

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku prijavite se Microsoft Dynamics u usluge životnog ciklusa i pogledajte članak u [bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije su podrazumevano uključene u predstojećem izdanju

Sledeća tabela navodi funkcije koje su podrazumevano uključene u verziji 10.0.30. Većina funkcija koje su automatski uključene može biti isključena u upravljanju [funkcijama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ubuduće, neke funkcije koje su automatski uključene mogu biti uklonjene iz upravljanja funkcijama i postati obavezne. Ova promena obezbeđuje da klijenti koriste trenutnu funkcionalnost, tako da poboljšanja mogu da se nadograde na trenutnoj funkcionalnosti dok se dodaju. Funkcije nikada neće biti automatski omogućene za manje od godinu dana, osim ako nisu utvrđene da su od suštinskog značaja.

| Ime funkcije | Omogući datum | Dodata funkcija | Status funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogući asinc operaciju kada korisnik treba da se prebacuje između operacija sinhronizacije i asinca | 21. oktobar 2022. | 9. april 2021. | Uključeno po podrazumevanoj vrednosti | Upravljanje troškovima |
| Procena smernica troškova za potrebne potvrde | 21. oktobar 2022. | 20. decembar 2021. | Uključeno po podrazumevanoj vrednosti | Upravljanje troškovima |
| Prikaz liste izveštaja o troškovima koje su kreirali delegiranje radnika | 21. oktobar 2022. | 19. februar 2020. | Uključeno po podrazumevanoj vrednosti | Upravljanje troškovima |
| Ukupan obračun kilometraže po fiskalna godina | 21. oktobar 2022. | 10. maj 2022. | Uključeno po podrazumevanoj vrednosti | Upravljanje troškovima |
