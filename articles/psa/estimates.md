---
title: Procene
description: Ova tema pruža informacije o procenama u aplikaciji Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ebb59d2b38bf99aed15206646e77c74003aba2a92a6d8d262e6e7b2017285ed3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992403"
---
# <a name="estimates"></a>Procene

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U ponudi zasnovanoj na projektu možete koristiti entitet Detalji stavke ponude da biste procenili posao koji je neophodan za isporučivanje projekta. Zatim možete da podelite tu procenu sa klijentom.

Stavke ponude zasnovane na projektu ne moraju da imaju detalje o stavci ponude. Umesto toga, mogu da imaju mnogo detalja stavke ponude. Detalji stavke ponude se koriste za procenu vremena, troškova ili naknada. PSA ne dozvoljava procene materijala u detaljima stavke ponude. To su klase transakcija. Procenjeni iznosi poreza takođe mogu da se unesu u klasu transakcije.

Pored klasa transakcija, detalji stavke ponude imaju vrstu transakcije. PSA podržava dve vrste transakcija za detalje stavke ponude: **Troškovi** i **Ugovor o projektu**.

## <a name="estimate-by-using-a-contract"></a>Procenjivanje korišćenjem ugovora

Ako ste koristili PSA ponudu kada ste kreirali ugovor zasnovan na projektu, procena za svaku stavku ponude u ponudi kopira se u ugovor o projektu. Struktura ugovora o projektu je nalik strukturi ponude projekta koja ima stavke, detalje stavke i rasporede fakturisanja.

Procene se mogu obaviti direktno u ugovoru o projektu, kao i u ponudi projekta. Za ponudu projekta, procena se vrši korišćenjem predmeta ugovora i detalja predmeta ugovora. Detalji predmeta ugovora mogu da se generišu i iz plana projekta koji je kreiran pomoću kompletnog pristupa procene.

Detalji predmeta ugovora mogu da se koriste za procenu vremena, troškova ili naknada. Procenjeni iznosi poreza takođe mogu da se unesu u detalj predmeta ugovora.

PSA ne dozvoljava procene materijala u detaljima predmeta ugovora.

Procesi koji su podržani u ugovoru o projektu su kreiranje i potvrda fakture. Kreiranje fakture kreira radnu verziju fakture zasnovanu na projektu koja uključuje sve nenaplaćene stvarne vrednosti prodaje do sadašnjeg datuma.

Potvrda omogućava da ugovor bude samo za čitanje i menja njegov status iz **Radna verzija** u **Potvrđeno**. Nakon što preduzmete ovu radnju, ne možete da je opozovete. Budući da je ova radnja trajna, najbolje je da se ugovor zadrži u statusu **Radna verzija**.

Jedine razlike između radnih verzija ugovora i potvrđenih ugovora su njihov status i činjenica da se radne verzije ugovora mogu uređivati, a potvrđeni ugovori ne mogu. Kreiranje fakture i praćenje stvarnih vrednosti mogući su za radne verzije ugovora i potvrđene ugovore.

PSA ne podržava promenu porudžbina u ugovorima ili projektima.

## <a name="estimating-projects"></a>Procene projekata

Možete proceniti vreme i troškove za projekte. PSA ne dozvoljava procene materijala ni naknada za projekte.

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
| Kada korisnik opisuje resurs u projektnom zadatku                                                                                                                                                                                                                                                                                            | Zapis stavke procene se kreira da bi se prikazala vrednost prodaje zadatka, prilikom kreiranja zadatka sa svim potrebnim dimenzijama određivanja cena. Uloga i organizaciona jedinica su OOB Project Service dimenzije za određivanje cena | Ugovor za projekat | Time        |                                                                                   |
|     | Zapis stavke procene se kreira da bi se prikazala vrednost troškova zadatka, prilikom kreiranja zadatka sa svim potrebnim dimenzijama određivanja cena. Sistem kopira sva polja koja nemaju novčanu vrednost iz stavke procene prodaje u stavku procene troškova. Uloga i organizaciona jedinica su OOB PSA dimenzije za određivanje cena kako za stope troškova tako i za stope naplate.                                                                                                                                                                                                                | Troškovi             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Prilagođavanje entiteta Detalj stavke ponude i Detalj predmeta ugovora

Ako ste u detalj stavke ponude dodali prilagođeno polje i želite da sistem unese vrednost polja kao podrazumevanu vrednost u povezanu liniju troškova koju kreira, upotrebite alatke za registraciju dodatnih komponenti PreOperationContractLineDetailUpdate i PreOperationQuoteLineDetailUpdate. Ove dodatne komponente moraju biti ponovo registrovane nakon što se promene detalj stavke ponude ili detalj predmeta ugovora. Da biste dovršili postupak, sledite ove korake.

1. Otvorite PluginRegistrationTool i povežite se sa instancom na mreži.
2. Izaberite **Pretraga** i potražite dodatnu komponentu za ažuriranje.

    ![Dijalog stabla za pretragu.](media/basic-guide-19.png)

3. Izaberite dodatnu komponentu, a zatim na glavnoj stranici stavku **Izaberi**.
4. Izaberite korak dodatne komponente za ažuriranje, kliknite desnim tasterom miša, a zatim izaberite **Ažuriraj**.

    ![Izbor koraka u dodatnoj komponenti.](media/basic-guide-20.png)

5. U dijalogu **Ažuriranje postojećeg koraka**, u polju **Atributi filtriranja**, izaberite dugme sa tri tačke (**...**):
 
    ![Dijalog Ažuriranje postojećeg koraka.](media/basic-guide-21.png)

6. U dijalogu **Izbor atributa** potvrdite izbor u poljima za prilagođene atribute.

    ![Dijalog Izbor atributa.](media/basic-guide-22.png)

7. Izaberite **U redu** da zatvorite dijalog, a zatim izaberite **Ažuriraj korak**.
 
    ![Dugme Ažuriraj korak.](media/basic-guide-23.png)

8. Ponovite korake od 1 do 7 za drugu dodatnu komponentu.
9. Zatvorite PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]