---
title: Ugovori za projekat – Ključni koncepti
description: Ova tema pruža informacije o ključnim konceptima ugovora za projekat u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa00bd5b4a1179f38d5dfb63a47b39eec69c6ecf
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642155"
---
# <a name="project-contracts---key-concepts"></a>Ugovori za projekat – Ključni koncepti

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U ovoj temi dati su ključni koncepti kojih morate biti svesni pre nego što počnete da koristite projektne ugovore u Dynamics 365 Project Operations:

## <a name="owning-company"></a>Preduzeće-vlasnik

Preduzeće-vlasnik je pravno lice u modulu **Upravljanje projektima i računovodstvo** za Project Operations u usluzi Dynamics 365 Finance. Preduzeće-vlasnik predstavlja pravno lice koje će obračunati troškove i prihode nastale iz pogodbe.

## <a name="contracting-unit"></a>Jedinica ugovaranja

Jedinica ugovaranja predstavlja odeljenje ili praksu koja je vlasnik isporuke projekta. Možete podesiti troškove resursa za svaku jedinicu ugovaranja. Kada odredite troškove resursa za resurs, moći ćete da podesite različite stope troškova za resurse. Ova ugovorna jedinica pozajmljuje ove resurse od drugih odeljenja ili praksi u preduzeću. Stope troškova za resurse nazivaju se cenama transfera, pozajmljivanjem resursa ili menjačkim cenama. Kada postavite stope troškova za pozajmljivanje resursa iz drugih odeljenja, koristite valutu odeljenja pozajmljivanja.

## <a name="cost-currency"></a>Valuta cene

Valuta cene je valuta u kojoj se iskazuju cene na ekranu. Ova valuta je izvedena iz valute koja je priložena uz polje **Jedinica ugovaranja** o ugovoru i projektu. Troškovi se mogu evidentirati u bilo kojoj valuti u odnosu na projekat. Međutim, postoji konverzija valute iz valute u kojoj su zabeleženi troškovi u valutu troškova projekta kada se prikazuju na ekranu.

Budući da devizni kursevi na platformi Common Data Service (CDS) ne mogu da važe na datum, ukupni troškovi na ekranu mogu se promeniti tokom vremena ako ažurirate devizne kurseve. Međutim, troškovi zabeleženi u bazi podataka ostaju nepromenjeni jer se iznosi čuvaju u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Valuta prodaje u usluzi Project Operations je valuta u kojoj se evidentiraju i prikazuju procenjeni i stvarni iznosi prodaje. Valuta prodaje je takođe valuta u kojoj se klijentu fakturiše za pogodbu. U projektnom ugovoru, valuta prodaje podrazumevano dolazi iz zapisa klijenta ili poslovnog kontakta i može se promeniti kada se kreira ugovor. Kada se ugovor kreira zatvaranjem ponuđene ponude, valuta na ugovoru se podrazumeva od valute na ponudi.

Kada kreirate ugovor o projektu od nule, polje **Valuta prodaje** se ne može uređivati. Cenovnik proizvoda i projekata zadat je na osnovu ove valute u ugovoru.

Za razliku od troškova, vrednosti prodaje mogu se evidentirati samo u valuti prodaje.

## <a name="billing-method"></a>Način naplate

Obično postoje dva tipa modela ugovaranja za projekte, zasnovani na naknadama i potrošnji. Ovi modeli su predstavljeni u usluzi Project Operations kao načini naplate sa dve moguće vrednosti:

- Vreme i materijal: Model ugovora zasnovan na potrošnji gde svaki nastali trošak potkrepljuje odgovarajući prihod. Kako procenite ili napravite više troškova, odgovarajuća procenjena i stvarna prodaja će se takođe povećati. Navedite ograničenja koja se ne smeju premašiti za predmete ugovora koji imaju ovaj način obračuna koji ograničava stvarni prihod. Procenjeni prihod ne utiče na ograničenja koja se ne smeju premašiti.
- Fiksna cena: Model ugovora sa fiksnom naknadom koji ukazuje da će prodajne vrednosti biti nezavisne od nastalih troškova. Vrednost prodaje je fiksna i ne menja se kako procenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cenovnici projekta

Cenovnici projekata se koriste za podrazumevane cene, a ne za stope troškova, za vreme, troškove i druge komponente povezane sa projektom. Cenovnika može biti više. Svaki cenovnik ima svoj datum stupanja na snagu za svaki ugovor o projektu. Preklapanje datuma stupanja na snagu cenovnika za projekat nije podržano u usluzi Project Operations.

Kada se projektni ugovor kreira dobijanjem projektne ponude, cenovnici projekata se kopiraju sa uključenim nazivom i datumom ugovora. Kopiranje ovih podataka predstavlja prilagođenu cenu za komponente projekta na ovom ugovoru o projektu.

## <a name="transaction-classes"></a>Klase transakcije

Projektne operacije podržavaju četiri vrste klasa transakcija:

- Vreme
- Trošak
- Materijal
- Naknada

Vrednosti troškova i prodaje mogu se proceniti i nastati za klase transakcija vremena, rashoda i materijala. Naknada je klasa transakcija koja predstavlja samo prihod.

## <a name="work-entities-and-billing-entities"></a>Radni entiteti i entiteti obračuna

Entiteti koji predstavljaju rad su projekti i zadaci. Entiteti koji predstavljaju aspekte obračuna su predmeti ugovora. Možete povezati različite radne entitete sa opcijama naplate povezivanjem sa predmetima ugovora.

## <a name="multi-customer-deals"></a>Pogodbe sa više klijenata

Pogodbe sa više klijenata imaju više klijenata kojima se fakturiše u pogodbi. Uobičajeni primeri uključuju sledeće:

- OEM preduzeća i njihovi partneri: Partneri i lokalni prodavci prodaju proizvod sa nekim uslugama sa dodatom vrednošću, što obično uključuje određenu pogodbu sa klijentom. OEM nudi finansiranje dela projekta. 

- Projekti javnog sektora: Više odeljenja lokalne samouprave pristaje da finansira projekat i njima se fakturiše prema prethodno dogovorenoj podeli. Na primer, školski okrug i lokalna uprava dogovore se da finansiraju izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi za fakturisanje

Rasporedi faktura specifični su za svaki predmet ugovora i potrebni su da bi automatsko fakturisanje funkcionisalo. Rasporedi za fakturisanje se kreiraju na osnovu određenih datuma početka i završetka i učestalosti fakturisanja. Rasporedi se koriste u fazi ugovora kada se konfiguriše automatski postupak kreiranja fakture. Kada se kreira ugovor projekta iz ponude, raspored fakturisanja se kopira u ugovor projekta iz ponude.

## <a name="changes-from-dynamics-365-sales-orders"></a>Promene iz Dynamics 365 Sales porudžbina

Ugovori u usluzi Project Operations se grade na osnovu porudžbina u usluzi Dynamics 365 Sales. Međutim, postoje važne razlike u funkcionalnosti. Ugovori imaju sopstveni obrazac i elemente korisničkog interfejsa, poslovna pravila, poslovnu logiku u dodatnim komponentama i skripte na strani klijenta koje ih čine jedinstvenim u odnosu na porudžbine. Iz ovih razloga ne treba da koristite Sales porudžbinu i Project Operations ugovor o projektu naizmenično.
