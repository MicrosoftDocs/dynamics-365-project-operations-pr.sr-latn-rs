---
title: Koncepti finansijske procene
description: Ova tema pruža informacije o finansijskim procenama projekata u usluzi Project Operations.
author: rumant
manager: AnnBe
ms.date: 03/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a251be995abddba04cee689714d0a8f4e9d9e7d7
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701753"
---
# <a name="financial-estimation-concepts"></a>Koncepti finansijske procene

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

U usluzi Dynamics 365 Project Operations, svoje projekte možete finansijski proceniti u dve faze: 
1. Tokom faze pretprodaje pre dobijanja pogodbe. 
2. Tokom faze izvršenja nakon izrade ugovora o projektu. 

Možete da napravite finansijsku procenu za rad na projektu koristeći bilo koju od sledeće 3 stranice:
- Stranicu **Stavka ponude**, koristeći detalje stavke ponude.  
- Stranicu **Predmet ugovora za projekat**, koristeći detalje predmeta ugovora. 
- Stranicu **Projekat**, koristeći stranice kartica **Zadaci** ili **Procene troškova**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Korišćenje ponude za projekat radi kreiranja procene
U ponudi zasnovanoj na projektu možete koristiti entitet **Detalji stavke ponude** da biste procenili posao koji je neophodan za isporučivanje projekta. Zatim možete da podelite tu procenu sa klijentom.

Stavke ponude zasnovane na projektu mogu da imaju između nula i mnogo detalja o stavci ponude. Detalji stavke ponude se koriste za procenu vremena, troškova ili naknada. Microsoft Dynamics 365 Project Operations ne dozvoljava procene materijala u detaljima stavke ponude. To su klase transakcija. Procenjeni iznosi poreza takođe mogu da se unesu u klasu transakcije.

Pored klasa transakcija, detalji stavke ponude imaju vrstu transakcije. Dve vrste transakcija za detalje stavke ponude su podržane: **Troškovi** i **Ugovor o projektu**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Korišćenje ugovora za projekat radi kreiranja procene

Ako ste koristili ponudu kada ste kreirali ugovor zasnovan na projektu, procena za svaku stavku ponude u ponudi kopira se u ugovor o projektu. Struktura ugovora o projektu je nalik strukturi ponude projekta koja ima stavke, detalje stavke i rasporede fakturisanja.

Procene se mogu obaviti direktno u ugovoru o projektu, kao i u ponudi projekta. Za ponudu projekta, procena se vrši korišćenjem predmeta ugovora i detalja predmeta ugovora. Detalji predmeta ugovora mogu da se generišu i iz plana projekta koji je kreiran pomoću kompletnog pristupa procene.

Detalji predmeta ugovora mogu da se koriste za procenu vremena, troškova ili naknada. Procenjeni iznosi poreza takođe mogu da se unesu u detalj predmeta ugovora.

Procene materijala nisu dozvoljene u detaljima predmeta ugovora.

## <a name="use-a-project-to-create-an-estimate"></a>Korišćenje projekta radi kreiranja procene 

Možete proceniti vreme i troškove za projekte. Project Operations ne podržava procene materijala ili naknada za projekte.

Procene vremena se generišu kada kreirate zadatak i identifikujete atribute generičkog resursa koji je potreban za izvršavanje zadatka. Procene vremena se generišu iz zakazanih zadataka. Procene vremena ne kreiraju se ako kreirate generičke članove tima izvan konteksta rasporeda.

Procene troškova se unose u mrežu na stranici **Procene troškova**.

Kreiranje procene za projekat smatra se najboljom praksom jer možete izraditi detaljne procene odozdo prema gore za rad ili vreme i troškove za svaki zadatak u planu projekta. Zatim možete koristiti ovu detaljnu procenu da biste kreirali procene za svaku stavku ponude i kreirali verodostojniju ponudu za klijenta. Kada uvozite ili kreirate detaljnu procenu na stavci ponude pomoću plana projekta, Project Operations uvozi vrednosti prodaje i vrednosti troškova ovih procena. Nakon uvoza, možete da pogledate metrike profitabilnosti, marže i izvodljivosti na ponudi za projekat.

## <a name="understanding-estimates"></a>Objašnjenje procena

Koristite sledeću tabelu kao vodič za razumevanje poslovne logike u fazi procene.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Zapis entiteta                                                                                                                                                                                                       | Tip transakcije | Klasa transakcije | Dodatne informacije                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Kada je potrebno da procenite prodajnu vrednost vremena za ponudu                                                                                                                                                                                                                                                                                    | Kreiran je zapis detalja stavke ponude                                                                                                                                                                               | Ugovor za projekat | Time        | Polje sa poreklom transakcije u redu detalja stavke ponude na strani prodaje upućuje na detalj stavke ponude na strani troškova |
|                                                                                                                                                                                                                                                                                     | Sistem kreira drugi zapis detalja stavke ponude za skladištenje odgovarajućih vrednosti troškova. Sistem kopira sva polja koja nemaju novčanu vrednost iz detalja stavke ponude u detalj stavke troškova.                                                                                                                                                                               | Troškovi | Time        | Polje sa poreklom transakcije u redu detalja stavke ponude na strani prodaje upućuje na detalj stavke ponude na strani troškova |
| Kada je potrebno da procenite prodajnu vrednost vremena za ugovor                                                                                                                                                                                                                                                                                 | Kreiran je zapis detalja predmeta ugovora o projektu                                                                                                                                                                    | Ugovor za projekat | Time        | Polje sa poreklom transakcije u redu detalja stavke ponude na strani prodaje upućuje na detalj stavke ponude za troškove      |
|                                                                                                                                                                                                                                                                                  | Sistem kreira drugi zapis detalja predmeta ugovora za skladištenje odgovarajućih vrednosti troškova. Sistem kopira sva polja koja nemaju novčanu vrednost iz detalja predmeta ugovora prodaje u detalj predmeta ugovora o troškovima.                                                                                                                                                                    | Troškovi | Time        | Polje sa poreklom transakcije u redu detalja stavke ponude na strani prodaje upućuje na detalj stavke ponude za troškove      |
| Kada korisnik opisuje resurs u projektnom zadatku                                                                                                                                                                                                                                                                                            | Zapis stavke procene se kreira da bi se prikazala vrednost prodaje zadatka, prilikom kreiranja zadatka sa svim potrebnim dimenzijama određivanja cena. Uloga i organizaciona jedinica su dimenzije za određivanje cena | Ugovor za projekat | Vreme        |                                                                                   |
|     | Zapis stavke procene se kreira da bi se prikazala vrednost troškova zadatka, prilikom kreiranja zadatka sa svim potrebnim dimenzijama određivanja cena. Sistem kopira sva polja koja nemaju novčanu vrednost iz stavke procene prodaje u stavku procene troškova. Uloga i organizaciona jedinica su dimenzije za određivanje cena kako za stope troškova tako i za stope naplate.                                                                                                                                                                                                                | Cena             | Vreme           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Prilagođavanje entiteta Detalj stavke ponude i Detalj predmeta ugovora

Ako ste u detalj stavke ponude dodali prilagođeno polje i želite da sistem unese vrednost polja kao podrazumevanu vrednost u povezanu liniju troškova koju kreira, upotrebite alatke za registraciju dodatnih komponenti **PreOperationContractLineDetailUpdate** i **PreOperationQuoteLineDetailUpdate**. Ove dodatne komponente moraju biti ponovo registrovane nakon što se promene detalj stavke ponude ili detalj predmeta ugovora. Da biste dovršili postupak, sledite ove korake.

1. Otvorite PluginRegistrationTool i povežite se sa instancom na mreži.
2. Izaberite **Pretraga** i potražite dodatnu komponentu za ažuriranje.
3. Izaberite dodatnu komponentu, a zatim na glavnoj stranici kliknite na **Izaberi**.
4. Izaberite korak dodatne komponente za ažuriranje, kliknite desnim tasterom miša, a zatim izaberite **Ažuriraj**.
5. U dijalogu **Ažuriranje postojećeg koraka**, u polju **Atributi filtriranja**, izaberite dugme sa tri tačke (**...**):
6. U dijalogu **Izbor atributa** potvrdite izbor u poljima za prilagođene atribute.
7. Izaberite **U redu** da zatvorite dijalog, a zatim izaberite **Ažuriraj korak**.
8. Ponovite korake od 1 do 7 za drugu dodatnu komponentu.
9. Zatvorite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
