---
title: Šta je novo u septembru 2022. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama
description: Ovaj članak pruža informacije o ispravkama kvaliteta koje su dostupne u izdanju usluge Microsoft Dynamics 365 Project Operations za septembar 2022. za scenarije zasnovane na resursima/bez zaliha.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634823"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Šta je novo u septembru 2022. – Project Operations za resurs/scenarije koji nisu zasnovani na zalihama

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Ovaj članak se odnosi na sledeće komponente i verzije usluge Microsoft Dynamics 365 Project Operations:

- Project Operations u Dataverse okruženju verzije 4.46.0.60
- Upravljanje projektima i računovodstvo u Dynamics 365 Finance okruženju verzije 10.0.29

## <a name="features-included-in-this-release"></a>Funkcije uključene u ovom izdanju

| Oblast funkcija | Naziv funkcije | Više informacija |
| --- | --- | --- |
| Upravljanje mogućnostima za poslovanje | **Revizija i aktiviranje ponuda**<br>Project Operations donosi punu podršku procesu prodaje. Ponude projekta se mogu aktivirati tako da predstavljaju status u kojem je ponuda samo za čitanje i kada se revidira. Aktivirane ponude se mogu revidirati da bi se kreirale nove ponude koje imaju inkrementalni broj revizije. Aktivirane ponude za projekat ili revizije ponude mogu da se zatvore kao ostvarene ili neostvarene. | [Aktiviranje i korigovanje ponude za projekat](/dynamics365/project-operations/sales/activation-and-revision) |
| Naplata i određivanje cena | **Podrazumevana cena sa nepoznatom vremenskom zonom**<br>Project Operations su uvele koncept datuma sa nepoznatom vremenskom zonom na svim stvarnim vrednostima u projektu. Novo polje **Datum transakcije** je sada dostupno u stavkama u glavnoj knjizi i stvarnim vrednostima i koristiće se za skladištenje datuma kada je transakcija izvršena, ali bez konvertovanja tog datuma u koordinirano univerzalno vreme. Ovaj datum će se koristiti za posledične procese kao što su postavljanje podrazumevane cene i kreiranje faktura. | <p>[Utvrđivanje stopa za cenu za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Utvrđivanje prodajnih cena za procene i stvarne vrednosti zasnovane na projektu](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Naplata i određivanje cena | **Zamene cene na određeni datum u usluzi Project Operations**<br>Izmene cena na određeni datum obezbeđuju način zamene ili promene određene cene u cenovniku. | [Izmene cena na određeni datum](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Podugovaranje | **Sravnjenje podugovaranja i fakture dobavljača**<br>Ova funkcija omogućava klijentima da kreiraju podugovore za vreme nabavke, kategorije troškova i materijale kupovine koji se koriste za rad na projektu. Takođe omogućava klijentima da beleže, u aplikacijama za finansije i operacije, fakture dobavljača koje će biti dostupne projektnim menadžerima u usluzi Dataverse radi provere. | <p>[Upravljanje podugovorima](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Kreiranje faktura prodavca](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Vreme i trošak | **Globalna osoba koja vrši odobravanje**<br>Ova funkcija omogućava nezavisnog prodavca softvera (ISV) i centralizovano odobravanje, bez obzira na status projekta ili člana tima u projektu. | [Bezbednost i odobrenja](/dynamics365/project-operations/approvals/approvals-security) |
| Upravljanje troškovima | **Mogućnost knjiženja odgovornosti troškova u valuti dobavljača**<br>Ova funkcija omogućava knjiženje izveštaja o troškovima u valuti dobavljača za način plaćanja gotovinom. | [Mogućnost knjiženja odgovornosti troškova u valuti dobavljača](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Nabavka projekata | **Plaćanje prodavcima nakon izvršene naplate**<br>Ova funkcija omogućava da se funkcija Plaćanje nakon uplate (PWP) koristi sa Project Operations okruženjima bez zaliha. Omogućava da se uplate dobavljačima blokiraju/zadržavaju, na osnovu uslova zadržavanja, sve dok se uplata ne primi od klijenta. | [Plaćanje prodavcima nakon izvršene naplate](/dynamics365/project-operations/procurement/pay-when-paid) |
| Nabavka projekata | **Zahtevi za kupovinu za projekat**<br>Ova funkcija omogućava korisnicima da kreiraju porudžbenice vezane za projekat u pravnim licima gde je omogućena integracija usluge Project Operations sa sistemom Dynamics 365 Customer Engagement. Porudžbenice projekta se mogu koristiti za evidentiranje nabavke materijala koji nije na zalihama za projekat od strane osobe u odeljenju za nabavke. Porudžbenice projekta neće biti sinhronizovane sa uslugom Dataverse. Međutim, virtuelni entitet možete koristiti za stavke porudžbenice projekta u usluzi Dataverse za informacije za projektnog menadžera. Cena na fakturi dobavljača povezane sa projektom je integrisana sa entitetom Stvarne vrednosti projekta u programu Dataverse. Cena za projekat evidentira se u knjizi analitike projekta koristeći dnevniku integracije u usluzi Project Operations. | |
|Planiranje i praćenje projekta|**Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja** </br> </br>API za uređivanje konture dodele resursa omogućava programerima da programski navedu napore osobe kojoj je dodeljen zadatak u bilo kom podržanom opsegu datuma za granuliranije planiranje napora u vremenskoj fazi.|[Korišćenje API-ja za raspored projekata za izvođenje operacija sa entitetima raspoređivanja](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Ažuriranja mapa dvostrukog upisivanja za Project Operations

Sledeća tabela prikazuje mape dvostrukog pisanja koje su izmenjene ili dodate u izdanju Project Operations od septembra 2022. godine.

| Mapa entiteta | Ažurirana verzija | komentara |
| -------------- | ------------------- | ------------|
| Project Operations stvarne vrednosti integracije (msdyn_actuals) | 1.0.0.15 | Ova mapa podržava obradu stvarnih vrednosti podugovora sa uslugom Project Operations za scenarije zasnovane na resursima. |
| Project Operations entitet izvoza fakture prodavca (msdyn_projectvendorinvoices) | 1.0.0.2 | Ova mapa podržava obradu stvarnih vrednosti podugovora sa uslugom Project Operations za scenarije zasnovane na resursima. |
| Project Operations entitet izvoza reda fakture prodavca (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ova mapa podržava obradu stvarnih vrednosti podugovora sa uslugom Project Operations za scenarije zasnovane na resursima. |

Uvek pokrenite najnoviju verziju mape u svom okruženju i omogućite sve povezane mape tabela dok ažurirate svoje Project Operations Dataverse rešenje i verzija rešenja usluge Finance. Neke funkcije i mogućnosti možda neće raditi ispravno ako se ne aktivira najnovija verzija mape. Aktivnu verziju mape možete videti u koloni **Verzija** na stranici **Dvostruko upisivanje**. Da biste aktivirali novu verziju mape, izaberite **Verzije tabele mape**, izaberite najnoviju verziju, a zatim sačuvajte izabranu verziju. Ako ste prilagodili mapu tabele koja je gotova, ponovo primenite. Za još informacija pogledajte [Upravljanje životnim ciklusom aplikacije](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ako naiđete na problem kada pokrenete mapu, sledite uputstva u odeljku [Nedostaje izdanje kolona tabele na mapama](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) vodiča za rešavanje problema sa dvostrukim upisivanjem.

## <a name="quality-updates"></a>Ispravke kvaliteta

### <a name="project-operations-on-dataverse"></a>Project Operations u usluzi Dataverse

| Oblast funkcija | Referentni broj | Ispravka kvaliteta |
| --- | --- | --- |
| Naplata i određivanje cena | 2754422 | Procene materijala i troškova ne teku u Finansije kada se projekti kopiraju u uslugu Dataverse. |
| Vreme i trošak | 2787409 | Odobravalac koji nije važeći može da odobri unos vremena koje nije projektno. |
| Upravljanje mogućnostima za poslovanje | 2788907 | Ažurirana poruka o grešci prilikom provere valjanosti jedinstvenosti za stavke porudžbenice koje obuhvataju zastavice. |
| Vreme i trošak | 2842253 | Bez načina obrade izuzetaka za odobravanje vremena. |
| Naplata i određivanje cena | 2844181 | Ako ne dobijete ID korelacije, blokira se kreiranje fakture. |
| Naplata i određivanje cena | 2876628 | QLD, CLD – Procena rešenja cenovnika treba da koristi zastarela polja opsega datuma cenovnika. |
| Podugovaranje | 2893222 | Ako nije navedena nijedna uloga za predmet podugovora, trebalo bi da bude moguće izabrati taj predmet za člana tima za bilo koju ulogu. |

### <a name="project-management-and-accounting-in-finance"></a>Upravljanje projektima i računovodstvo u usluzi Finance

Za informacije o ispravkama grešaka koje su uključene u ovu ispravku, prijavite se na Microsoft Dynamics Lifecycle Services i pogledajte [članak u bazi znanja](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcije su podrazumevano uključene u predstojećem izdanju

Sledeća tabela navodi funkcije koje su podrazumevano uključene u verziji 10.0.30. Većina funkcija koje su automatski uključene može biti isključena u [Upravljanju funkcijama](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ubuduće, neke funkcije koje su automatski uključene mogu biti uklonjene iz Upravljanja funkcijama i postati obavezne. Ova promena obezbeđuje da korisnici koriste trenutnu funkcionalnost, tako da poboljšanja mogu da se nadograde na trenutnu funkcionalnost kako se dodaju. Funkcije nikada neće biti automatski omogućene za manje od godinu dana, osim ako nije utvrđeno da su od suštinskog značaja.

| Naziv funkcije | Datum omogućavanja | Dodata funkcija | Status funkcije | Modul |
| --- | --- | --- |--- |--- |
| Omogućavanje asinhrone operacije kada korisnik treba da se prebacuje između sinhronih i asinhronih operacija | 21. oktobar 2022. | 9. april 2021. | Podrazumevano uključeno | Upravljanje troškovima |
| Procena smernica troškova za obavezne potvrde | 21. oktobar 2022. | 20. decembar 2021. | Podrazumevano uključeno | Upravljanje troškovima |
| Prikaz liste izveštaja o troškovima koje su kreirali radnici koji delegiraju | 21. oktobar 2022. | 19. februar 2020. | Podrazumevano uključeno | Upravljanje troškovima |
| Izračunavanje ukupne kilometraže po fiskalnoj godini | 21. oktobar 2022. | 10. maj 2022. | Podrazumevano uključeno | Upravljanje troškovima |
