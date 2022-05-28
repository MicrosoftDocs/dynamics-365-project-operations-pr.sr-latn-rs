---
title: Međukompanijsko fakturisanje
description: Ovaj članak pruža informacije i primere o međukompanijskom fakturisanju za projekte.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f66af9b7e2cb0e18a5464b23216ff03b63a0a3
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685441"
---
# <a name="intercompany-invoicing"></a>Međukompanijsko fakturisanje

[!include [banner](../includes/banner.md)]

Ovaj članak pruža informacije i primere o međukompanijskom fakturisanju za projekte.

Vaša organizacija može imati više odeljenja, podružnica i drugih pravnih lica koja međusobno prenose proizvode i usluge za projekte. Pravno lice koje pruža uslugu ili proizvod naziva se *pravno lice – zajmodavac*, a pravno lice koje prima uslugu ili proizvod naziva se *pravno lice – zajmoprimac*. 

Sledeća ilustracija prikazuje tipičan scenario kada dva pravna lica, SI FR (zajmoprimac) i SI USA (zajmodavac) dele resurse za isporuku projekta za klijenta A. Za ovaj scenario, SI FR je ugovoren da isporuči rad za klijenta A. 

[![Primer međukompanijskog fakturisanja.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Cilj je učiniti kontrolu troškova, priznavanje prihoda, poreza i cene transfera za međukompanijske projektne transakcije fleksibilnijim i moćnijim. Pored toga, pružaju se sledeće mogućnosti:

-   Kreirajte fakture za klijenta za projekat u pravnom licu zajmoprimcu korišćenjem međukompanijskih vremenskih rasporeda, troškova i faktura dobavljača u pravnom licu zajmodavcu.
-   Podržite obračune poreza i indirektne troškove.
-   Odložite priznavanje prihoda u pravnom licu zajmodavcu i kada pravno lice zajmoprimac treba da prizna trošak.
-   Steknite prihod od rada u toku u pravnom licu zajmodavcu.
-   Odredite cene transfera koje se mogu zasnivati na različitim modelima određivanja cena. U nastavku su navedeni neki primeri:
    -   **Količina** – Iznos koji unesete u polje **Cene** je stvarni trošak po količini ili jedinici.
    -   **Iznos naknada** – Cena/trošak po transakciji plus iznos naknade koji ste uneli u polje **Cene**.
    -   **Procenat naknada** – Cena transfera je cena/trošak po transakciji pomnožen sa procentom naplate koji unesete u polje **Cene**.
    -   **Procenat prodajne cene** – procenat prodajne cene koja se prenosi na pravno lice zajmodavca.
    -   **Iznos ispod prodajne cene** – Iznos koji pravno lice zajmoprimac zadržava iz prodajnih cena pre prenosa pravnom licu zajmodavcu.
    -   **Odnos doprinosa** – Broj koji ste uneli u polje **Cene** je odnos doprinosa, koji se izražava u procentima od prodajne cene.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>1. primer: Podešavanje parametara za međukompanijsko fakturisanje
U ovom primeru, USSI je pravno lice zajmodavac i njegovi resursi prijavljuju vreme pravnom licu zajmoprimcu, FRSI, koje je vlasnik ugovora sa krajnjim klijentom. Sati i troškovi o kojima izveštavaju zaposleni u USSI mogu biti uključeni u fakturu projekta koju generiše FRSI. Pored toga, postoji i treći izvor transakcija koji može poteći od pravnog lica zajmodavca (USSI u ovom primeru) kada pruža usluge deljenih dobavljača podružnicama (kao što je FRSI), a zatim te troškove prenosi na projekte u okviru tih podružnica. Sve odgovarajuće dokumente fakture i obračune poreza dovršava usluga Finance. 

U ovom primeru, FRSI mora biti klijent u pravnom licu USSI, a USSI mora biti prodavac u pravnom licu FRSI. Zatim možete da uspostavite međukompanijski odnos između dva pravna lica. Sledeći postupak pokazuje kako da podesite parametre tako da oba pravna lica mogu učestvovati u međukompanijskom fakturisanju.

1. Podesite FRSI kao klijenta u pravnom licu USSI i postavite USSI kao dobavljača u pravnom licu FRSI. Postoje tri ulazne tačke za korake potrebne za ovaj zadatak.

   | Korak |                                                       Tačka unosa                                                        |                                                                                                                                                                                               Opis                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | U USSI kliknite na <strong>Potraživanja</strong> &gt; <strong>Klijenti</strong> &gt; <strong>Svi klijenti</strong>. |                                                                                                                                                                  Kreirajte novi zapis klijenta za FRSI i izaberite grupu klijenata.                                                                                                                                                                  |
   |  B   |    U FRSI kliknite na <strong>Dugovanja</strong> &gt; <strong>Prodavci</strong> &gt; <strong>Svi prodavci</strong>.     |                                                                                                                                                                    Kreirajte novi zapis prodavca za USSI i izaberite grupu prodavaca.                                                                                                                                                                    |
   |  C   |                                  U FRSI otvorite zapis prodavca koji ste upravo kreirali.                                  | U oknu radnje, na kartici <strong>Opšti podaci</strong>, u grupi <strong>Podešavanje</strong> kliknite na <strong>Međukompanijsko</strong>. Na stranici <strong>Međukompanijsko</strong>, na kartici <strong>Trgovinski odnos</strong>, podesite klizač <strong>Aktivno</strong> na <strong>Da</strong>. U polju <strong>Kompanija klijenta</strong> izaberite zapis klijenta koji ste kreirali u koraku A. |


2. Kliknite na **Upravljanje projektima i računovodstvo** &gt; **Podešavanje** &gt; **Parametri računovodstva za upravljanje projektima**, a zatim kliknite na karticu **Međukompanijsko**. Način na koji podešavate parametre zavisi od toga da li ste pravno lice zajmoprimac ili pravno lice zajmodavac.
   -   Ako ste pravno lice zajmoprimac, izaberite kategoriju nabavke koja bi se koristila za podudaranje faktura dobavljača koje se automatski generišu.
   -   Ako ste pravno lice zajmodavac, za svako pravno lice zajmoprimca izaberite podrazumevanu kategoriju projekta za svaku vrstu transakcije. Kategorije projekata se koriste za konfiguraciju poreza kada fakturisana kategorija u međukompanijskim transakcijama postoji samo u pravnom licu zajmoprimcu. Možete odabrati da akumulirate prihod za međukompanijske transakcije. Ovo obračunavanje vrši se kada se transakcije knjiže, a zatim se stornira kada se proknjiži međukompanijska faktura.

3. Kliknite na **Upravljanje projektima i računovodstvo** &gt; **Podešavanje** &gt; **Cene** &gt; **Cena transfera**.
4. Izaberite valutu, vrstu transakcije i model cene prenosa. Valuta koja se koristi na fakturi je valuta koja se konfiguriše u zapisu klijenta za pravno lice zajmoprimca u pravnom licu zajmodavca. Valuta se koristi za podudaranje stavki u tabeli cena transfera.
5. Kliknite na **Glavna knjiga** &gt; **Podešavanje knjiženja** &gt; **Međukompanijsko računovodstvo**, i podesite odnos za USSI i FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>2. primer: Kreiranje i objavljivanje međukompanijskog vremenskog rasporeda
USSI, pravno lice zajmodavac, mora da kreira i objavi vremenski raspored za projekat kompanije FRSI, pravnog lica zajmoprimca. Postoje dve ulazne tačke za korake potrebne za ovaj zadatak.

| Korak | Tačka unosa                                                                       | Opis                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Upravljanje projektima i računovodstvo** &gt; **Vremenski rasporedi** &gt; **Svi vremenski rasporedi** | Kreirajte novi vremenski raspored. U redu vremenskog rasporeda, u polju **Pravno lice** izaberite **FRSI**. U polju **ID projekta**, izaberite projekat u FRSI. Unesite sate za svaki dan u nedelji. |
| B    | Stranica **Vremenski raspored**                                                                | Kada se tok posla pokrene, objavite vremenski raspored i zabeležite broj vaučera.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>3. primer: Kreiranje i objavljivanje međukompanijske fakture prodavca
USSI, pravno lice zajmodavac, mora da kreira i objavi međukompanijsku fakturu prodavca za projekat kompanije FRSI, pravnog lica zajmoprimca. Ova faktura prodavca predstavlja spoljni rad i troškove koje su izvršili dobavljači koje plaća USSI. Postoje dve ulazne tačke za korake potrebne za ovaj zadatak.

| Korak | Tačka unosa                                                                                      | Opis                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Dugovanja** &gt; **Fakture** &gt; **Otvorene fakture dobavljača** &gt; **Nova faktura dobavljača** | Kreirajte novu fakturu dobavljača i unesite usluge koje su nabavljene u ime projekta kompanije FRSI.                                                                                                                                                                                  |
| B    | Stranica **Faktura prodavca**                                                                      | Unesite redove koji predstavljaju spoljne izvršioce usluga u ime FRSI. Na brzoj kartici **Detalji linije**, na kartici **Projekat** za red fakture, u polju **Kompanija projekta**, unesite **FRSI**. Unesite projekat i odgovarajuće informacije. Zatim proknjižite fakturu prodavca. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>4. primer: Kreiranje i knjiženje međukompanijske fakture
USSI, pravno lice zajmodavac, mora kreirati i proknjižiti međukompanijsku fakturu. Postoje dve ulazne tačke za korake potrebne za ovaj zadatak.

| Korak | Tačka unosa                                                                                             | Opis                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Međukompanijska faktura klijenta**  | Kliknite na **Novo** da biste otvorili stranicu **Kreiranje međukompanijske fakture**.                                                                                  |
| B    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Međukompanijske fakture klijenata** | Na stranici **Kreiranje međukompanijske fakture**, unesite pravno lice, navedite transakciju koju treba uključiti, a zatim kliknite na **Pretraga**. |
| C    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Međukompanijske fakture klijenata** | Izaberite transakcije za fakturisanje ili kliknite na **Izaberi sve** da fakturišete sve transakcije sa liste, a zatim kliknite na **U redu**.                  |
| D    | Stranica **Međukompanijska faktura**                                                                       | Prikazuje se predlog međukompanijske fakture za klijenta.                                                                                             |
| E    | Stranica **Međukompanijska faktura**                                                                       | Kliknite na **Proknjiži**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>5. primer: Knjiženje fakture prodavca i fakturisanje klijentu
Kada pravno lice zajmodavac, USSI, knjiži međukompanijsku fakturu za klijenta, u pravnom licu zajmoprimcu, FRSI, kreira se odgovarajuća faktura prodavca na čekanju. Nakon knjiženja ove fakture prodavca, FRSI takođe fakturiše klijentu projekta za sate koje je USSI uneo. Postoje tri ulazne tačke za korake potrebne za ovaj zadatak.

| Korak | Tačka unosa                                                                                        | Opis                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Dugovanja** &gt; **Fakture** &gt; **Fakture prodavca na čekanju**                            | Pregledajte fakturu da biste proverili da li su uključene vrednosti vremenskog rasporeda, a zatim proknjižite fakturu prodavca.                  |
| B    | **Upravljanje projektima i računovodstvo** &gt; **Fakture projekta** &gt; **Predlozi za fakture projekta** | Kreirajte novu fakturu projekta za projekat i proverite da li se prikazuju transakcije sati koje su proknjižene.            |
| C    | Stranica **Faktura projekta**                                                                       | Izaberite fakturu projekta, a zatim kliknite **Prikaz detalja** za pregled troškova i iznosa prodaje. Zatim proknjižite fakturu. |


Za više informacija, pogledajte [Konfigurisanje fakturisanja međukompanijskih projekata](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]