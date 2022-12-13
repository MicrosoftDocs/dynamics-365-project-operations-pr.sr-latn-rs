---
title: Pregled redova ugovora o projektu
description: Ovaj članak pruža informacije o radu sa redovima ugovora o projektu u operacijama projekta.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824644"
---
# <a name="project-contract-lines-overview"></a>Pregled redova ugovora o projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Predmeti ugovora zasnovani na projektu u usluzi Dynamics 365 Project Operations dizajnirani su tako da drže ugovore o proceni i obračunu za određene komponente projektnog rada na angažmanu. Struktura stavke ugovora zasnovane na projektu proširena je za procene projekata i scenarije naplate sa sledećim konceptima:

- Način naplate
- Mapiranje projekata i zadataka
- Uključene klase transakcija
- Ograničenje koje ne sme da se prekorači
- Podešavanje naplativosti
- Procene korišćenjem detalja o predmeta ugovora
- Klijenti predmeta ugovora

Sledeća tabela uključuje polja na kartici **Opšti podaci** predmeta ugovora zasnovanih na projektu koji pomažu u postavljanju osnove za detaljnu, osnovnu procenu i aranžmane za obračun za projektni rad.

| Polje | Opis | Posledični uticaj |
| --- | --- | --- |
| **Ime** | Naziv predmeta ugovora. Ovo identifikuje diskretnu komponentu ugovora koja se procenjuje. Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajuće vrednosti stavke ponude zasnovane na projektu. | Ime kopirano u stavku fakture za projekat koja se kreira iz ovog predmeta ugovora kada se kreira faktura. |
| **Način naplate** | Za projektni ugovor kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude. Ovo je skup opcija koji predstavlja dva glavna modela ugovaranja koja podržava usluga Project Operations:</br>- **Fiksna cena**</br>- **Vreme i materijal** | Na osnovu načina naplate navedenog predmeta ugovora, stvarna transakcija će biti obrađena. Ako predmet ugovora na koji se poziva stvarna vrednost ima način naplate vremena i materijala, kreiraju se zapisi stvarnih vrednosti troškova i nenaplaćene prodaje. Ako predmet ugovora na koji se poziva stvarna vrednost ima način obračuna sa fiksnom cenom, kreiraće se samo stvarni trošak. |
| **Project** | Koristite ovo polje za identifikovanje projekta koji će se koristiti za izvođenje radova na ovom angažmanu. | Ova vrednost će se koristiti zajedno sa **Obuhvaćeni zadaci** i **Obuhvaćene klase transakcija** da se reši referenca na predmet ugovora na stvarnom ili procenjenom zapisu stavke. |
| **Obuhvaćeni zadaci** | Označava da li ova linija ugovora uključuje sve projektne zadatke za izabrani projekat ili samo podskup zadataka. Ovo je skup opcija koji ima sledeće moguće vrednosti:</br>- **Svi projektni zadaci**</br>- **Samo izabrani projektni zadaci**. Prazna vrednost u ovom polju jednaka je odabiru **Svi projektni zadaci**. | Ako je izabrana opcija **Samo izabrani zadaci**, možete izabrati određene zadatke i povezati ih sa ovim predmetom ugovora na kartici **Podešavanje zadatka za obračun** na stranici **Projekat**. Vrednost će se koristiti zajedno sa klasama **Projekat** i **Uključene klase transakcija** da se razreši referenca na predmet ugovora na stvarnoj vrednosti ili zapisu predmeta procene. |
| **Sadrži vreme** | Vrednost **Da**/**Ne** pokazuje da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u ovaj predmet ugovora. Vrednost **Ne** označava da vremenske transakcije ili troškovi rada neće biti uključeni u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke. |
| **Sadrži trošak** | Vrednost **Da**/**Ne** pokazuje da li će cena troškova na izabranom projektu biti uključena u ovaj predmet ugovora. Vrednost **Ne** označava da cena troškova na izabranom projektu neće biti uključena u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke. |
| **Sadrži materijale** | Vrednost **Da**/**Ne** pokazuje da li će cena materijala na izabranom projektu biti uključena u ovaj predmet ugovora. Vrednost **Ne** pokazuje da cena materijala neće biti uključena u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke. |
| **Sadrži nadoknadu** | Vrednost **Da**/**Ne** pokazuje da li će naknade na izabranom projektu biti uključene u ovaj predmet ugovora. Vrednost **Ne** označava da naknade neće biti uključene u ovaj predmet ugovora. Vrednost **Da** ukazuje na to da hoće. | Ova vrednost se koristi zajedno sa projektom za rešavanje reference na predmet ugovora na stvarnom ili procenjenom zapisu stavke. |
| **Ugovoreni iznos** | Na predmetu ugovora sa fiksnom cenom, ovaj iznos je ugovorena vrednost koja će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora. Na predmetu ugovora za vreme i materijal, ovaj iznos je procenjena vrednost onoga što će se fakturisati klijentu za sve radne komponente povezane sa ovim predmetom ugovora. Za projektni ugovor koji je kreiran iz ponude, ova vrednost se kopira iz odgovarajućeg polja na stavki ponude. Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa u detaljima linije ugovora. | Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa na detaljima stavki. U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje iznosa pre oporezivanja na periodičnim kontrolnim tačkama obračuna. |
| **Procenjeni porez** | Korisnik može da uređuje ovo polje kako bi uneo procenjeni iznos poreza u predmet ugovora. Kada predmet ugovora zasnovan na projektu sadrži detalje stavki, ovo polje se zaključava za uređivanje i sažima iz iznosa poreza u detaljima predmeta ugovora. | Kada predmet ugovora sadrži detalje stavki, ova vrednost se može izmeniti promenom iznosa poreza na detaljima stavki. U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje poreza na periodičnim kontrolnim tačkama obračuna. |
| **Ugovoreni iznos sa porezom** | Iznos predmeta ugovora sa porezom. Ovo polje je samo za čitanje i izračunava se kao **Ugovoreni iznos + porez**. | U predmetu ugovora sa fiksnom cenom, ova vrednost se koristi za generisanje periodičnih kontrolnih tačaka obračuna. |
| **Ograničenje koje ne sme da se prekorači** | Korisnik može da uređuje ovo polje i ono je dostupno samo na predmetima ugovora zasnovanim na projektu čiji način obračuna je postavljen na vreme i materijal. | Korisnik može da uređuje ovo polje. Kada se stvarna vrednost za vreme i materijal odnosi na ovaj predmet ugovora za vreme i materijal, iznos na stvarnoj vrednosti se procenjuje prema ograničenju koje ne sme da se premaši na predmetu ugovora. Ova procena se završava nakon što se obračunaju već potrošeni i preuzeti iznosi. |
| **Budžet klijenta** | Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja na stavki ponude ako je ugovor kreiran iz ponude. | Ovo polje se koristi samo za informacije i nema nikakav dalji značaj. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Pravila za validaciju za opcije na kartici Opšti podaci za predmete ugovora zasnovane na projektu

Pravilo 1: Ako je polje **Uključeni zadaci** prazno ili podešeno na **Svi projektni zadaci**, svi zadaci projekta su uključeni u predmet ugovora.

Pravilo 2: Kada je polje **Uključeni zadaci** prazno ili je izričito postavljeno na **Svi projektni zadaci**, projekat i određena klasa transakcija mogu biti uključeni samo u jedan predmet ugovora zasnovan na projektu.

Pravilo 3: Kada je polje **Uključeni zadaci** postavljeno na **Samo izabrani projektni zadaci**, projekat i određena klasa transakcija mogu da se uključe u više predmeta ugovora zasnovanih na projektu.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Ugovor</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Predmet ugovora</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Obuhvaćeni zadaci</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sadrži vreme</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sadrži trošak</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sadrži materijale</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Uvrsti</strong>
                </p>
                <p>
                    <strong>Naknada</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Važi / Ne važi</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vreme, troškovi, materijali i naknade na projektu P1 uključeni su u oba predmeta ugovora CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2. Vreme, troškovi, materijali i naknade na projektu P1 uključeni su u oba predmeta ugovora CL1 i CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Važeće </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Vreme, materijali i naknade za projekat P1 uključeni su u CL1.
                </p>
                <ul>
                    <li>
Troškovi za projekat P1 uključeni su u CL2.
                    </li>
                </ul>
                <p>
Nema preklapanja u onome što je uključeno u svaki predmet ugovora i stoga je važeće.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 2 </p>
                <p>
C1 uključuje vreme, materijale, troškove i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
CL2 uključuje vreme, materijale, troškove i naknade za ceo projekat P1 i stoga se preklapa sa onim što je uključeno u C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Prazno </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Važeće </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Po pravilu br. 3 </p>
                <p>
C1 uključuje vreme, troškove, materijale i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
CL2 uključuje vreme, troškove, materijale i naknade za podskup zadataka na projektu P1.
                </p>
                <p>
Jedina dodatna provera valjanosti oko podskupa zadataka na CL1 razlikuje se od podskupa zadataka na CL2 kako bi se osiguralo da tamo nema preklapanja. To sistem radi kada su zadaci povezani.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Samo izabrani zadaci </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="48" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
            <td width="42" valign="top">
                <p>
Da </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
