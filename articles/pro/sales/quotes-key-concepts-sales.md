---
title: Ponude – Ključni koncepti – jednostavno
description: Ova tema pruža informacije o korišćenju ponuda za projekat u usluzi Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6cc1b38644557370d2447b65d2bba2925dc134a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574861"
---
# <a name="concepts-unique-to-project-quotes"></a>Koncepti jedinstveni za ponude za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


Slede ključni koncepti kojih morate biti svesni pre nego što počnete da koristite ponude projekata u usluzi Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Jedinica ugovaranja

Jedinica ugovaranja predstavlja odeljenje ili praksu koja je vlasnik isporuke projekta. Možete podesiti troškove resursa za svaku jedinicu ugovaranja. Kada odredite cenu resursa za resurs u ugovornoj jedinici, moći ćete i da postavite različite stope troškova za resurse od kojih se ova ugovorna jedinica zadužuje ili druga odeljenja ili prakse u preduzeću. To se naziva cenama transfera, zaduživanjem resursa ili menjačkim cenama. Kada postavite cenu pozajmljivanja resursa iz drugih odeljenja, takođe možete da odaberete da postavite te stope troškova u valuti odeljenja pozajmljivanja.

## <a name="cost-currency"></a>Valuta cene

Valuta cene u usluzi Project Operations je valuta u kojoj se iskazuju cene. Ova valuta je izvedena iz valute koja je priložena uz polje **Jedinica ugovaranja** o ponudi, ugovoru i projektu. Troškovi se mogu evidentirati u bilo kojoj valuti u odnosu na projekat. Međutim, postoji konverzija valute iz valute u kojoj su zabeleženi troškovi u valutu troškova projekta.

Budući da devizni kursevi na CDS platformi ne mogu da važe na datum, ukupni troškovi na ekranu mogu se promeniti tokom vremena ako ažurirate devizne kurseve. Međutim, troškovi zabeleženi u bazi podataka ostaju nepromenjeni jer se iznosi čuvaju u valuti u kojoj su nastali.

## <a name="sales-currency"></a>Valuta prodaje

Valuta prodaje u usluzi Project Operations je valuta u kojoj se evidentiraju i prikazuju procenjeni i stvarni iznosi prodaje. To je takođe valuta u kojoj se klijentu fakturiše za pogodbu. U ponudi za projekat, valuta prodaje podrazumevano dolazi iz zapisa klijenta ili poslovnog kontakta i može se promeniti kada se kreira ponuda. Kada se ponuda sačuva, valuta prodaje se ne može promeniti. Cenovnici proizvoda i projekata podrazumevano su zasnovani na prodajnoj valuti ponude.

Za razliku od troškova, vrednosti prodaje mogu se evidentirati samo u valuti prodaje.

## <a name="billing-method"></a>Način naplate

Projekti obično imaju fiksne modele ugovaranja zasnovane na naknadama i potrošnji. Ovo se u usluzi Project Operations predstavlja kao **Način naplate** i ima dve vrednosti, vreme i materijal i fiksnu cenu.

- **Vreme i materijal:** Ovo je model ugovora zasnovan na potrošnji gde svaki nastali trošak potkrepljuje odgovarajući prihod. Kako procenite ili napravite više troškova, odgovarajuća procenjena i stvarna prodaja će se takođe povećati. Možete odrediti ograničenja koja se ne smeju premašiti za stavke ponude koje imaju ovaj način obračuna. Ovo će ograničiti stvarni prihod. Procenjeni prihod ne utiče na ograničenja koja se ne smeju premašiti.
- **Fiksna cena:** Ovo je model ugovora sa fiksnom naknadom koji ukazuje da će prodajne vrednosti biti nezavisne od nastalih troškova. Vrednost prodaje je fiksna i ne menja se kako procenite ili napravite više troškova.

## <a name="project-price-lists"></a>Cenovnici projekta

Cenovnici projekata su cenovnici koji se koriste za podrazumevane cene, a ne za stope troškova, za vreme, troškove i druge komponente povezane sa projektom. Može biti više cenovnika, a svaka lista može imati svoju efektivnost datuma za svaku ponudu za projekat. Preklapanje datuma stupanja na snagu cenovnika za projekat nije podržano u usluzi Project Operations.

## <a name="product-price-lists"></a>Cenovnici proizvoda

Cenovnici proizvoda su cenovnici koji se koriste za podrazumevane cene, a ne za stope troškova, za stavke zasnovane na proizvodima u ponudi. Postoji samo jedan cenovnik proizvoda po ponudi.

## <a name="transaction-classes"></a>Klase transakcije

Projektne operacije podržavaju četiri vrste klasa transakcija:

- Vreme
- Trošak
- Materijal
- Naknada

Vrednosti troškova i prodaje mogu se proceniti i nastati za klase transakcija vremena, rashoda i materijala. Naknada je klasa transakcija koja predstavlja samo prihod.

## <a name="work-entities-and-billing-entities"></a>Radni entiteti i entiteti obračuna

Entiteti koji predstavljaju rad su projekti i zadaci. Entiteti koji predstavljaju obračun su stavke ponude i predmeti ugovora. Možete povezati različite radne entitete sa opcijama naplate povezivanjem sa stavkama ponude ili predmetima ugovora.

## <a name="multi-customer-deals"></a>Pogodbe sa više klijenata

Pogodbe sa više klijenata nastaju kada postoji više klijenata kojima se fakturiše. Uobičajeni primeri uključuju sledeće:

- **OEM preduzeća i njihovi partneri:** Partneri i preprodavci prodaju proizvod sa uslugama sa dodatom vrednošću. To je obično scenario kada OEM tokom određenog dogovora sa klijentom nudi finansiranje dela projekta. 

- **Projekti javnog sektora:** Više odeljenja lokalne samouprave pristaje da finansira projekat i njima se fakturiše prema prethodno dogovorenoj podeli. Na primer, školski okrug i gradska uprava ili odeljenje lokalne uprave dogovore se da finansiraju izgradnju bazena.

## <a name="invoice-schedules"></a>Rasporedi za fakturisanje

Rasporedi za fakturisanje su specifični za svaku stavku ponude i takođe su opcionalni. Rasporedi za fakturisanje se kreiraju na osnovu određenih datuma početka i završetka i učestalosti fakturisanja. Rasporedi za fakturisanje se koriste u fazi ugovora kada se konfiguriše automatski postupak kreiranja fakture. U fazi ponude, rasporedi su opcionalni. Kada se rasporedi za fakturisanje kreiraju u fazi **Ponuda**, oni se kopiraju u ugovor o projektu koji se kreira kada se ponuda za projekat ostvari.

## <a name="changes-from-dynamics-365-sales-quote"></a>Promene iz Dynamics 365 Sales ponude:

Project Operations ponude se grade na Dynamics 365 Sales ponudama. Međutim, postoje neke važne razlike u funkcionalnosti kojih bi trebalo da budete svesni:

- Radnje **Koriguj** i **Aktiviraj** nisu podržane.
- Project Operations ponude imaju dve različite vrste stavki. Jedna je za projekte, a druga za proizvode.
- Project Operations ponude imaju sopstveni obrazac i elemente korisničkog interfejsa, poslovna pravila, poslovnu logiku u dodatnim komponentama i skripte na strani klijenta koje ih čine jedinstvenim u odnosu na ponuda usluge Sales.

Iz ovih razloga nije preporučljivo naizmenično koristiti Sales ponudu i Project Operations ponudu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
