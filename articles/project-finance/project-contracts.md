---
title: Ugovori o projektu
description: Ova tema daje primere ugovora o projektu koje možete kreirati za različite vrste projekata i izvore finansiranja, kao i kako možete upravljati ugovorima i fakturisati klijentima projekata.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755196"
---
# <a name="project-contracts"></a>Ugovori o projektu

[!include [banner](../includes/banner.md)]

Ovaj članak daje primere ugovora o projektu koje možete kreirati za različite vrste projekata i izvore finansiranja, kao i kako možete upravljati ugovorima i fakturisati klijentima projekata.

Tip projekta koji kreirate za ugovor o projektu određuje metodu koji se koristi za fakturisanje klijenata projekta. Možete da promenite ugovor o projektu i s njim povezani projekat, ali ne možete da promenite tip projekta. 

Korišćenjem ugovora o projektu možete istovremeno fakturisati jedan ili više projekata. Ugovor o projektu takođe garantuje dosledne procedure fakturisanja za svaki podprojekat u strukturi projekta. 

Svaki projekat koji će biti fakturisan mora biti povezan sa ugovorom o projektu. Postavke za ugovor o projektu odnose se na sve projekte i potprojekte koji su povezani sa tim ugovorom o projektu. 

U ugovoru o projektu može se navesti jedan ili više izvora finansiranja. Prema tome, možete podeliti obračun između više donatora, postaviti ograničenja finansiranja tako da se izvorima finansiranja ne naplaćuje više od određenog iznosa i konfigurisati pravila finansiranja za naplatu troškova.

## <a name="funding-for-project-contracts"></a>Finansiranje ugovora o projektu
Neki ugovori o projektu navode da više strana deli odgovornost za finansiranje troškova projekta. U nastavku su navedeni neki primeri:

-   Veliki klijent koji ima više odeljenja zahteva da se finansiranje projekta podeli po odsecima.
-   Vaša kompanija deli troškove velikog projekta sa spoljnom organizacijom.
-   Projekat puta sufinansiraju dve opštine.
-   Projekt mosta finansira se iz državnih grantova i privatne korporacije.

U usluzi Dynamics 365 Finance, možete da podelite naplatu za jednu transakciju ili ceo projekat između više klijenata, grantova ili organizacija. 

U projektima koji imaju više donatora, sve strane koje doprinose finansiranju naprednog projekta finansiranja nazivaju se izvorima finansiranja. Nakon što se klijent, organizacija ili grant definiše kao izvor finansiranja, može se dodeliti jednom ili više pravila finansiranja. Pravila finansiranja sadrže kriterijume koji određuju način na koji se troškovi dodeljuju različitim izvorima finansiranja za projekat. 

Budući da se zalihe stavki, poput onih koje se pojavljuju u zahtevima za kupovinu i porudžbenicama, ne mogu podeliti, iznos troškova ne može se podeliti između više izvora finansiranja u trenutku distribucije. Stoga, vrednost izvora finansiranja ostaje 0 (nula) dok se problem sa inventarom ne proknjiži. Kada se problem sa inventarom proknjiži, iznos troškova se raspoređuje prema pravilima raspodele računa za projekat.

Evo nekih koraka koje možete preduzeti da biste olakšali podelu naplate između više izvora finansiranja:

-   Navedite da sve transakcije koje se unose za projekat koriste istu valutu prodaje kao i ugovor o projektu.
-   Postavite ograničenja finansiranja, tako da izvor finansiranja ne fakturiše više od određenog iznosa za projekat.
-   Konfigurišite pravila finansiranja i ograničenja finansiranja za svakog radnika, stavku, kategoriju, grupu kategorija i vrstu transakcije (ili za sve vrste transakcija).
-   Izaberite neobavezne datume početka i završetka da biste definisali period kada važi svako pravilo finansiranja.
-   Navedite procenat za koji je odgovoran svaki izvor finansiranja.
-   Navedite koji je izvor finansiranja odgovoran za zaokruživanje razlika uzrokovanih proračunima dodele sredstava.
-   Postavite pravila koja određuju kako će se troškovi projekta fakturisati spoljnim klijentima, a naplaćivati internim organizacijama.
-   Evidentirajte transakcije na računu za finansiranje na čekanju dok ne bude moguće dobiti dodatna sredstva ili dok ne odlučite da snosite troškove interno.

Da bi se utvrdilo koju poresku grupu treba povezati sa transakcijom, u projektu se traži dodeljivanje poreske grupe. Ako na nivou projekta nije izvršeno dodeljivanje poreske grupe, pretražuje se ugovor o projektu.

### <a name="example-multiple-funding-sources-simple"></a>Primer: Više izvora finansiranja (jednostavno)

Sledeća tabela daje scenarije za upravljanje raspodelom sredstava između više izvora finansiranja. Ovi scenariji zasnovani su na sledećim pretpostavkama:

-   Postavke prioriteta uzimaju se u obzir u raspodeli sredstava pre nego što se primene drugi kriterijumi pravila finansiranja.
-   Nije naveden nijedan datumski period koji bi definisao period od kada važi pravilo finansiranja.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Izvor finansiranja</strong></td>
<td><strong>Procenat dodele</strong></td>
<td><strong>Prioritet dodele</strong></td>
</tr>
<tr class="even">
<td>Želite da dodelite troškove jednom izvoru finansiranja dok se njegova sredstva ne iscrpe, dodelite troškove drugom izvoru finansiranja dok se njegova sredstva ne iscrpe i konačno dodelite preostale troškove trećem izvoru finansiranja.</td>
<td><ul>
<li>Izvor　finansiranja　1</li>
<li>Izvor　finansiranja　2</li>
<li>Izvor　finansiranja　3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Želite da dodelite 75 procenata troškova jednom izvoru finansiranja, a 25 procenata drugom izvoru finansiranja. Kada se iscrpi bilo koji od tih izvora finansiranja, preostale troškove želite da platite iz trećeg izvora finansiranja.</td>
<td><ul>
<li>Izvor　finansiranja　1</li>
<li>Izvor　finansiranja　2</li>
<li>Izvor　finansiranja　3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Želite da dodelite 75 procenata troškova jednom izvoru finansiranja, a 25 procenata drugom izvoru finansiranja. Kada se iscrpi bilo koji od tih izvora finansiranja, preostale troškove želite da podelite između trećeg i četvrtog izvora finansiranja.</td>
<td><ul>
<li>Izvor　finansiranja　1</li>
<li>Izvor　finansiranja　2</li>
<li>Izvor　finansiranja　3</li>
<li>Izvor　finansiranja　4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Želite da dodelite prvih 25 procenata troškova jednom izvoru finansiranja, a ostatak drugom izvoru finansiranja.</td>
<td><ul>
<li>Izvor　finansiranja　1</li>
<li>Izvor　finansiranja　2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Primer: Više izvora finansiranja (složeno)

Imate tri izvora finansiranja koja želite da koristite po sledećem redosledu:

1.  Koristite izvor finansiranja 2 i izvor 3 jednako dok se izvor 2 ne iscrpi.
2.  Nastavljate da koristite izvor finansiranja 3 dok se ne iscrpi.
3.  Koristite izvor finansiranja 1 nakon što se izvor 3 iscrpi.

Da biste postigli taj cilj, prvo morate da uradite sledeće:

-   Postavite ograničenja finansiranja za izvor finansiranja 2 i izvor finansiranja 3, za njihove odgovarajuće iznose.
-   Kreirajte sledeća pravila finansiranja:
    -   Pravilo 1 (Prioritet 1): Dodeli 50 procenata transakcija izvoru finansiranja 2 i 50 procenta izvoru finansiranja 3.
    -   Pravilo 2 (Prioritet 2): Dodeli 100% transakcija izvoru finansiranja 3.
    -   Pravilo 3 (Prioritet 3): Dodeli 100% transakcija izvoru finansiranja 1.

Ovo podešavanje funkcioniše jer se proverava da li transakcije poštuju pravila i ograničenja kako bi se utvrdilo da li se neko od njih odnosi na transakciju. Ako se na transakciju ne primenjuju posebna pravila ili ograničenja, primenjuje se pravilo Sve transakcije. Pravilo Sve transakcije podudara se sa svim transakcijama. 

Ako se pronađe pravilo koje se podudara sa transakcijom, prvo se primenjuje procenat koji je dodeljen u tom pravilu, ali tek nakon što se podudaranja provere prema bilo kojim ograničenjima koja su postavljena. Ako je ograničenje ispunjeno, a sredstva izvora finansiranja su iscrpljena, pravilo finansiranja koje je povezano sa ograničenjem finansiranja se zanemaruje, a program proverava sledeće pravilo koje se primenjuje. 

U nekim slučajevima, samo deo transakcije može biti dodeljen po pravilu. To se može dogoditi jer se dostigne ograničenje kada se transakcija dodeli. U ovom slučaju, samo se određeni iznos dodeljuje prema tom pravilu, poput 50 procenata za svaki izvor finansiranja. To je slučaj u pravilu 1, koje je opisano ranije u ovom odeljku. Ostatak se dodeljuje prema sledećem pravilu u nizu. 

Sledeća tabela detaljnije ispituje ovaj scenario.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Fokus</strong></td>
<td><strong>Detalji</strong></td>
</tr>
<tr class="even">
<td>Pravila finansiranja</td>
<td><ul>
<li>Pravilo 1 (Prioritet 1): Sve transakcije. Dodeli izvor finansiranja 2 sa 50% i izvor finansiranja 3 sa 50%.</li>
<li>Pravilo 2 (Prioritet 2): Sve transakcije. Izdvoj izvor finansiranja 3 na 100%.</li>
<li>Pravilo 3 (Prioritet 2): Sve transakcije. Izdvoj izvor finansiranja 1 na 100%.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Ograničenja finansiranja</td>
<td><ul>
<li>Ograničenje izvora finansiranja 1 = 10.000,00</li>
<li>Ograničenje izvora finansiranja 2 = 500,00</li>
<li>Ograničenje izvora finansiranja 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transakcija 1</td>
<td><strong>Iznos transakcije:</strong> 100,00<strong>Finansiranje:</strong> Transakcija se plaća samo prema pravilu 1, jer se transakcija u potpunosti plaća nakon primene pravila 1. Transakcija se finansira na jednak način između izvora finansiranja 2 i izvora finansiranja 3.
<ul>
<li>Izvor finansiranja 2: 50,00</li>
<li>Izvor finansiranja 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transakcija 2</td>
<td><strong>Iznos transakcije:</strong> 5.000,00<strong>Finansiranje:</strong> Transakcija se plaća prema sva tri pravila. <strong>Pravilo 1</strong>
<ul>
<li>Izvor finansiranja 2: 450,00</li>
<li>Izvor finansiranja 3: 450,00</li>
</ul>
<strong>Pravilo 2</strong>
<ul>
<li>Izvor finansiranja 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Pravilo 3</strong>
<ul>
<li>Izvor finansiranja 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Ukupna sredstva koja se raspoređuju za svaki izvor finansiranja</td>
<td><ul>
<li>Izvor finansiranja 1: 3.850,00</li>
<li>Izvor finansiranja 2: 500,00</li>
<li>Izvor finansiranja 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Pravila za naplate
Kada pregovarate o ugovoru o projektu sa klijentom, vi definišete kako i kada možete fakturisati klijentu za rad na projektu. Nakon što postavite ugovor o projektu i projekat, možete postaviti pravila naplate za projekat. Pravila za naplate zasnivaju se na uslovima projekta koji su navedeni u ugovoru o projektu. Pravila za naplatu koja možete kreirati zavise od uslova ugovora o projektu i vrste projekta, kao što su vreme i materijal ili fiksna cena, koje povezujete sa pravilom za naplatu. Za ugovor o projektu možete kreirati više pravila za naplatu. Pravilo naplate možete dodeliti i više za projekata koji su povezani sa istim ugovorom o projektu i imaju slične uslove naplate. 

Možete da podesite sledeće vrste naplate:

-   **Jedinica isporuke** – Fakturišite klijentu kada završite jedinicu isporuke. Jedinice isporuke definišete u ugovoru.
-   **Napredak** – Fakturišite klijentu kada završite određeni procenat projekta. Možete da podesite pravilo naplate tako da automatski izračunava procenat obavljenog posla ili možete ručno da izračunate procenat završenog posla i iznos za fakturisanje klijentu.
-   **Kontrolna tačka** – Fakturišite klijentu puni iznos kontrolne tačke projekta kada ta kontrolna tačka bude dostignuta.
-   **Naknada** – Fakturišite klijentu za vaše usluge plus naknadu za upravljanje, koja je obično procenat troškova usluga.
-   **Vreme i materijal** – Fakturišite klijentu za vrednost vremena i materijala koji se koriste na projektu.

Za sve vrste pravila naplate, možete odrediti procenat zadržavanja koji se oduzima od faktura klijenta dok projekat ne dostigne neku dogovorenu fazu. Procenat zadržavanja plaćanja se navodi u ugovoru o projektu. Iznos se izračunava na osnovu i oduzima od ukupne vrednosti linija u fakturi klijenta. 

Za pravila obračuna **Vreme i materijal** i **Napredak**, možete dodeliti naplative kategorije. Naplative kategorije označavaju transakcije koje treba da budu uključene u fakture klijenata. 

Kada budete spremni da fakturišete klijentu, iznos fakture za projekat se izračunava na osnovu pravila naplate i generiše se predlog fakture za projekat. 

Sledeći odeljci pružaju primere koji pokazuju kako se postavljaju pravila naplate za projekat i njima upravlja.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Primer: Kreirajte pravilo naplate koje se zasniva na broju isporučenih jedinica

Vaša organizacija zaključuje ugovor o pružanju ukupno pet obuka zaposlenima po ceni od 10.000 po sesiji. Klijentu fakturišete nakon svake sesije obuke. 

Kada postavite pravila naplate za ugovor, koristite sledeće vrednosti:

-   Jedinica isporuke je jedna sesija obuke.
-   Jedinična cena je 10.000 po sesiji obuke.
-   Ukupan broj jedinica je pet sesija obuke.

Kada završite jednu sesiju obuke, možete da napravite fakturu za 10.000 za prvu isporučenu jedinicu i pošaljite fakturu klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Primer: Kreirajte pravilo naplate koje se zasniva na određenom procentu završetka projekta (ručni proračun)

Vaša organizacija, firma za softversko savetovanje, sklapa ugovor sa klijentom o razvoju dela proizvoda koji klijent razvija. Vaša organizacija pristaje na isporuku softverskog koda u periodu od šest meseci. Klijent se slaže da će vašoj organizaciji platiti ukupno 100.000 za rad. Pravilo naplate kreirate da biste fakturisali klijentu na osnovu procenta posla koji je završen na projektu, kako je navedeno u ugovoru.

-   Na kraju prvog meseca, sastajete se sa klijentom da biste utvrdili procenat obavljenog posla. Nakon što vi i klijent pregledate projekat, odlučujete da je projekat završen 15 posto.
-   Kreirate fakturu na 15.000 (15 procenta od 100.000) i šaljete je klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Primer: Kreirajte pravilo naplate koje se zasniva na određenom procentu završetka projekta (automatski proračun)

Vaša organizacija, firma za razvoj softvera, pristaje da razvije paket obračuna zarada za klijenta po ceni od 30.000. Klijent se slaže da će vašoj organizaciji platiti na osnovu procenta završenog posla. Procenjujete da troškovi projekta iznose 20.000. Ugovor o projektu navodi kategorije posla koje koristite u postupku naplate. Postavljate pravila naplate koja automatski izračunavaju iznose faktura za procenat završenog posla za svaku kategoriju. Podesili ste budžet za svaku kategoriju:

-   **Razvoj** – Trošak od 15.000 i prihod od 20.000
-   **Instalacija** – Trošak od 5.000 i prihod od 10.000

Kada prvi put kreirate fakturu klijenta, iznos fakture se automatski izračunava na osnovu sledećih informacija:

-   Posle mesec dana, radnik na projektu podnosi vremenski raspored za projekat. Troškovi radnih sati radnika su 5.000 za razvoj i 1.000 za instalaciju. Razvojni radovi su završeni 33 procenta (5.000 stvarnih troškova / 15.000 troškova budžeta), a instalacioni radovi su završeni 20 procenata (1.000 stvarnih troškova / 5.000 troškova budžeta).
-   Iznos fakture od 8.667 se automatski izračunava (33 procenta od 20.000 + 20 procenata od 10.000).
-   Kreirate fakturu na 8.667 i šaljete je klijentu.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Primer: Kreirajte pravilo naplate koje se zasniva na dogovorenim kontrolnim tačkama

Vaša organizacija, konsultantska firma za menadžment, pristaje da sprovede istraživanje tržišta za potrošački proizvod koji klijent planira da proda. Klijent se slaže da će koristiti vaše usluge u periodu od tri meseca, počev od marta, i slaže se da će vašoj organizaciji platiti 50.000. Projekat ima tri kontrolne tačke:

-   Kontrolna tačka 1: Prikupljanje podataka o potrošačima – 31. mart
-   Kontrolna tačka 2: Analiza podataka potrošača – 30. april
-   Kontrolna tačka 3: Predstavljanje predloga održivosti proizvoda – 31. maj

Klijent se slaže da će vašoj organizaciji platiti 10.000 za prvu kontrolnu tačku, 20.000 za drugu kontrolnu tačku i 20.000 za treću kontrolnu tačku. 

Kada postavite ugovor o projektu, slažete se da ćete klijentu naplatiti na osnovu kontrolne tačke koja je završena. Postavljanje pravila naplate uključuje sledeće korake:

-   Definišite kontrolne tačke projekta.
-   Definišite iznos za fakturisanje klijentu kada se završi svaka kontrolna tačka.

Kada se prva kontrolna tačka završi 31. marta, označite je kao ispunjenu, a zatim napravite fakturu na iznos od 10.000 i pošaljite je klijentu. Ne možete da kreirate fakturu za kontrolnu tačku dok je ne označite kao završenu.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Primer: Kreirajte pravilo naplate koje se zasniva na uslugama uz naknadu za upravljanje

Vaša organizacija, konsultantska firma za menadžment, pristaje da sprovede istraživanje tržišta kako bi procenila održivost proizvoda koji klijent, maloprodajna kompanija, upravo razvija. Uslovi ugovora preciziraju da ćete pružati usluge svoja tri najbolja savetnika za menadžment, koji će sprovoditi istraživanje na osnovu vremena i materijala. Klijent se slaže da plaća 100 na sat, plus 10 posto naknade za upravljanje za konsultantske sate koji se naplaćuju za projekat. 

Kada postavite ugovor o projektu, kreirajte pravilo naplate da biste dodali naknadu od 10% za menadžment na savetodavne sate koji se naplaćuju projektu. 

Kada kreirate fakturu za klijenta, njemu se naplaćuje 10% naknade za upravljanje uz troškove konsultantskih sati. Na primer, ako su tri konsultanta radila ukupno 200 sati na projektu, faktura na iznos od 22.000 kreira se na osnovu sledećeg proračuna:

-   200 sati po 100 na sat = 20.000
-   Naknada za menadžment od 10% = 2.000
-   Ukupan iznos fakture = 22.000

Ako su naknade klijentu oporezive, a u ugovoru o projektu odaberete grupu za porez na promet, grupa poreza na promet automatski se unosi u pravilo naplate naknada.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Primer: Kreirajte pravilo naplate vrednosti vremena i materijala

Vaša organizacija, firma za softversko savetovanje, pristaje da obezbedi pet tehničkih konsultanata koji će raditi na projektu razvoja softvera za klijenta u narednih šest meseci. Klijent se slaže da plati 150 za svaki sat konsultovanja, uz troškove kancelarijskog materijala. Vaša organizacija šalje fakturu klijentu na kraju svakog meseca. 

Kada postavljate ugovor o projektu, saglasni ste da klijentu svakog meseca obračunavate vreme i materijale na projektu. Kreirate pravilo naplate koje uključuje sledeće informacije:

-   Period ugovora je šest meseci.
-   Vreme konsultacija izračunava se po ceni od 150 na sat.
-   Kancelarijski materijal se fakturiše po ceni koštanja, a ukupni troškovi projekta ne smeju preći 10.000.
-   Fakturu za klijenta kreirate na kraju svakog kalendarskog meseca tokom trajanja projekta.

Tokom prvog meseca, konsultanti na projektu beleže ukupno 800 sati. Troškovi kancelarijskog materijala koji se naplaćuju za projekat su 2.000. Stoga na kraju meseca kreirate fakturu na iznos od 122.000, što je izračunato kao 800 sati po 150 na sat, plus 2.000 za kancelarijski materijal.



