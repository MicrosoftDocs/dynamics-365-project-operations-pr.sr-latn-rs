---
title: Pregled stavki ponude zasnovane na projektu
description: Ova tema pruža informacije o korišćenju stavki ponude zasnovanim na projektu za rad na projektu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 2f2d38c7fb3bc3ec26cf64525ef8275adecafd7fc48e97d6daef595d341c045d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001583"
---
# <a name="project-based-quote-lines-overview"></a>Pregled stavki ponude zasnovane na projektu 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture, Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju. Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:

- Način naplate
- Mapiranje projekata i zadataka
- Uključene klase transakcija
- Ograničenje koje ne sme da se prekorači
- Podešavanje naplativosti
- Procena pomoću detalja stavki ponude
- Klijenti stavki ponude

Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu. Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| +Ime | Naziv ponude koji vam pomaže da prepoznate diskretnu komponentu ponude koja se procenjuje. | Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Način naplate | U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje. Ovo polje uključuje dva glavna modela ugovaranja koje Dynamics 365 Project Operations podržava:</br>- Fiksna cena</br>- Vreme i materijal.| Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Project | Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju. Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude. Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda.|
| Obuhvaćeni zadaci | Označava da li se ova stavka ponude koristi za sve ili neke projektne zadatke za izabrani projekat. Ovo polje podložno uređivanju ima sledeće moguće vrednosti:</br>- Svi projektni zadaci</br>- Samo izabrani projektni zadaci</br>Prazna vrednost u ovom polju je ekvivalentna opciji **Svi projektni zadaci**. | Kada se na stranici projekta izabere **Samo izabrani projektni zadaci**, kartica **Podešavanje naplate za zadatak** vam omogućava da izaberete određene zadatke da biste ih povezali sa ovom stavkom ponude. Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Sadrži vreme | Vrednost **Da**/**Ne** pokazuje da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude. Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude. Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Sadrži trošak | Vrednost **Da**/**Ne** pokazuje da li će cena troškova na izabranom projektu biti uključena u procenu ove stavke ponude. Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude. Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Sadrži materijal | Vrednost **Da**/**Ne** pokazuje da li će cena materijala na izabranom projektu biti uključena u procenu ove stavke ponude. Vrednost **Ne** pokazuje da cena materijala neće biti uključena u procenu ove stavke ponude. Vrednost **Da** pokazuje da cena materijala neće biti uključena u procenu ove stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Sadrži nadoknadu | Vrednost **Da**/**Ne** pokazuje da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude. Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude. Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Ponuđeni iznos | Ovo je iznos koji će biti naveden klijentu za sve radove predviđene na ovoj stavci ponude zasnovane na projektu. U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje. Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Procenjeni porez | To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude. Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Ponuđeni oporezovani iznos | Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje. Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Ograničenje koje ne sme da se prekorači | Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |
| Budžet klijenta | Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje. | Ova vrednost se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se dobije ponuda. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu

**1. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je podešeno na **Svi projektni zadaci**, projekat je uključen u stavku ponude.

**2. pravilo**: Ako je polje **Uključeni zadaci** prazno ili ako je postavljeno na **Svi projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni samo u jednu stavku ponude zasnovane na projektu.

**3. pravilo**: Ako je polje **Uključeni zadaci** postavljeno na **Samo izabrani projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni u više stavki ponude zasnovane na projektu.

**4. pravilo**: Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.

**5. pravilo**: Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Mogućnost za poslovanje</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Ponuda</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Stavka ponude</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Obuhvaćeni zadaci</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Sadrži vreme</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Sadrži trošak</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Sadrži materijal</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Uvrsti</strong>
                </p>
                <p>
                    <strong>Naknada</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Važi / Ne važi</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vreme, materijal i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Važeće </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Vreme, materijal i naknade za projekat P1 uključeni su u QL1 <br>
Troškovi za projekat P1 uključeni su u QL2 <br>
Nema preklapanja u onome što je uključeno u svaku stavku ponude i stoga je važeće.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2 </p>
                <p>
Q1 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1 </p>
                <p>
QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i stoga se preklapa sa onim što je uključeno u Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Važeće </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po pravilu br. 3, </p>
                <p>
Q1 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
QL2 uključuje vreme, materijal, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
Jedina dodatna provera valjanosti oko podskupa zadataka na QL1 koja se razlikuje od podskupa zadataka na QL2 kako bi se osiguralo da tamo nema preklapanja. To sistem radi kada su zadaci povezani.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi projektni zadaci ili prazni </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Važeće </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po pravilu br. 5, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da se mogu obe proceniti za iste komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi projektni zadaci ili prazni </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi projektni zadaci ili prazni </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Po pravilu br. 4, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da se ne mogu proceniti za iste komponente istog projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Svi projektni zadaci ili prazni </p>
            </td>
            <td width="45" valign="top">
                <p>
Da </p>
            </td>
            <td width="46" valign="top">
                <p>
Da </p>
            </td>
            <td width="43" valign="top">
                <p>
Da </p>
            </td>
            <td width="41" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
