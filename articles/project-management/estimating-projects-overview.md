---
title: Pregled procene projekata
description: Ova tema pruža informacije o procenama u usluzi Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d35be82563515adbba2c22402a751ed3daca8f83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131585"
---
# <a name="estimate-projects-overview"></a>Pregled procene projekata

_**Odnosi se na:** Project Operations za resurs/scenarije koji nisu zasnovani na zalihama, laganu primenu – od pogodbe do profakture_

U ponudi zasnovanoj na projektu možete koristiti entitet **Detalji stavke ponude** da biste procenili posao koji je neophodan za isporučivanje projekta. Zatim možete da podelite tu procenu sa klijentom.

Stavke ponude zasnovane na projektu mogu da imaju između nula i mnogo detalja o stavci ponude. Detalji stavke ponude se koriste za procenu vremena, troškova ili naknada. Microsoft Dynamics 365 Project Operations ne dozvoljava procene materijala u detaljima stavke ponude. To su klase transakcija. Procenjeni iznosi poreza takođe mogu da se unesu u klasu transakcije.

Pored klasa transakcija, detalji stavke ponude imaju vrstu transakcije. Dve vrste transakcija za detalje stavke ponude su podržane: **Troškovi** i **Ugovor o projektu**.

## <a name="estimate-by-using-a-contract"></a>Procenjivanje korišćenjem ugovora

Ako ste koristili ponudu kada ste kreirali ugovor zasnovan na projektu, procena za svaku stavku ponude u ponudi kopira se u ugovor o projektu. Struktura ugovora o projektu je nalik strukturi ponude projekta koja ima stavke, detalje stavke i rasporede fakturisanja.

Procene se mogu obaviti direktno u ugovoru o projektu, kao i u ponudi projekta. Za ponudu projekta, procena se vrši korišćenjem predmeta ugovora i detalja predmeta ugovora. Detalji predmeta ugovora mogu da se generišu i iz plana projekta koji je kreiran pomoću kompletnog pristupa procene.

Detalji predmeta ugovora mogu da se koriste za procenu vremena, troškova ili naknada. Procenjeni iznosi poreza takođe mogu da se unesu u detalj predmeta ugovora.

Procene materijala nisu dozvoljene u detaljima predmeta ugovora.

Procesi koji su podržani u ugovoru o projektu su kreiranje i potvrda fakture. Kreiranje fakture kreira radnu verziju fakture zasnovanu na projektu koja uključuje sve nenaplaćene stvarne vrednosti prodaje do sadašnjeg datuma.

Potvrda omogućava da ugovor bude samo za čitanje i menja njegov status iz **Radna verzija** u **Potvrđeno**. Nakon što preduzmete ovu radnju, ne možete da je opozovete. Budući da je ova radnja trajna, najbolje je da se ugovor zadrži u statusu **Radna verzija**.

Jedine razlike između radnih verzija ugovora i potvrđenih ugovora su njihov status i činjenica da se radne verzije ugovora mogu uređivati, a potvrđeni ugovori ne mogu. Kreiranje fakture i praćenje stvarnih vrednosti mogući su za radne verzije ugovora i potvrđene ugovore.

Project Operations ne podržava promenu porudžbina u ugovorima ili projektima.

## <a name="estimating-projects"></a>Procene projekata

Možete proceniti vreme i troškove za projekte. Project Operations ne dozvoljava procene materijala ni naknada za projekte.

Procene vremena se generišu kada kreirate zadatak i identifikujete atribute generičkog resursa koji je potreban za izvršavanje zadatka. Procene vremena se generišu iz zakazanih zadataka. Procene vremena ne kreiraju se ako kreirate generičke članove tima izvan konteksta rasporeda.

Procene troškova se unose u mrežu na stranici **Procene**.

## <a name="understanding-estimation"></a>Objašnjenje procene

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