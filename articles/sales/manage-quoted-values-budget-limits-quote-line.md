---
title: Pregled stavki ponude za projekat
description: Ova tema pruža informacije o korišćenju stavki ponude za projekat za rad na projektu.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996313"
---
# <a name="project-quote-lines-overview"></a>Pregled stavki ponude za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Stavke ponude zasnovane na projektu osmišljene su da pomognu u proceni rada na projektu pri angažovanju. Struktura stavke ponude na osnovu projekta proširena je za procene projekata sledećim konceptima:

- Način naplate
- Mapiranje projekata
- Uključene klase transakcija
- Ograničenje koje ne sme da se prekorači
- Podešavanje naplativosti
- Procena pomoću detalja stavki ponude
- Klijenti stavki ponude

Sledeća tabela pruža informacije o poljima na kartici **Opšti podaci** stavke ponude zasnovane na projektu. Ova polja pomažu u postavljanju osnove za detaljnu, osnovnu procenu rada na projektu.

| **Polje** | **Opis** | **Posledični uticaj** |
| --- | --- | --- |
| Imenuj | Naziv stavke ponude koja bi trebalo da vam pomogne da identifikujete diskretnu komponentu ponude koja se procenjuje. | Kopira se u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Način naplate | U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz odgovarajućeg polja u stavci mogućnosti za poslovanje. Ovo polje uključuje dva glavna modela ugovaranja koje Dynamics 365 Project Operations podržava:</br>- Fiksna cena</br>- Vreme i materijal.| Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Project | Koristite ovo opcionalno polje za identifikovanje projekta koji će se koristiti za izvođenje radova pri ovom angažovanju. Kada se projekat mapira u stavku ponude, to pomaže u postavljanju naplativih zadataka, kao i u donošenju procene zasnovane na projektu u stavci ponude kao detalje stavke ponude. Kada projekat nije mapiran u stavku ponude zasnovanu na projektu, procenu treba kreirati ručno kreiranjem svakog detalja stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Sadrži vreme | Zastavica **Da**/**Ne** označava da li će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude. Vrednost **Ne** označava da vremenske transakcije ili troškovi rada na izabranom projektu neće biti uključeni u procenu ove stavke ponude. Vrednost **Da** označava da će vremenske transakcije ili troškovi rada na izabranom projektu biti uključeni u procenu ove stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Sadrži trošak | Zastavica **Da**/**Ne** označava da li će cene troškova na izabranom projektu biti uključene u procenu ove stavke ponude. Vrednost **Ne** označava da cena troška neće biti uključena u procenu ove stavke ponude. Vrednost **Da** označava da će cena troška biti uključena u procenu ove stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Sadrži nadoknadu | Zastavica **Da**/**Ne** označava da li će naknade na izabranom projektu biti uključene u procenu ove stavke ponude. Vrednost **Ne** označava da naknade neće biti uključene u procenu ove stavke ponude. Vrednost **Da** označava da će naknade biti uključene u procenu ove stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Ponuđeni iznos | Ovo je iznos koji će biti naveden klijentu za sve radove predviđene u ovoj stavci ponude zasnovane na projektu. U ponudi kreiranoj iz mogućnosti za poslovanje, ova vrednost se kopira iz polja **Budžet klijenta** u stavci mogućnosti za poslovanje. Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa na detaljima stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Procenjeni porez | To polje može da uređuje korisnik da bi dodao procenjeni iznos poreza u stavku ponude. Kada stavka ponude zasnovana na projektu sadrži detalje o stavci, ovo polje je zaključano za uređivanje i rezimirano je iz iznosa poreza na detaljima stavke ponude. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Ponuđeni oporezovani iznos | Ovo polje je oporezovani iznos stavke ponude i samo je za čitanje. Iznos u ovom polju se izračunava kao *Ponuđeni iznos + porez*. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Ograničenje koje ne sme da se prekorači | Ovo polje je moguće uređivati i dostupno je samo u stavkama ponude zasnovanim na projektu čiji način obračuna je **Vreme i materijal**. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |
| Budžet klijenta | Ovo polje može da se uređuje i kopira se iz odgovarajućeg polja stavke mogućnosti za poslovanje ako je ponuda kreirana iz mogućnosti za poslovanje. | Ovo polje se kopira u predmet ugovora o projektu koji se kreira iz ove stavke ponude kada se ponuda ostvari. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Pravila za validaciju za polja na kartici Opšti podaci stavki ponude zasnovanih na projektu

**1. pravilo**: Određena klasa transakcija na izabranom projektu može se uključiti samo u jednu stavku ponude na osnovu projekta.

**2. pravilo**: Ako mogućnost za poslovanje ima više ponuda, mogu postojati stavke ponude iz različitih ponuda koje se odnose na isti projekat i uključuju istu klasu transakcije.

**3. pravilo**: Ako ponude ne pripadaju istoj mogućnosti za poslovanje, ne mogu da uključuju isti projekat i klasu transakcije.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Mogućnost za poslovanje</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Ponuda</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Stavka ponude</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
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
                    <strong>Umetanje</strong>
                </p>
                <p>
                    <strong>naknada</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Važi / Ne važi</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Razlog</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 1. Vreme, troškovi i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje pravila br. 1. Vreme i naknade za projekat P1 uključeni su u stavke ponude QL1 i QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Važeći </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Vreme i naknade za projekat P1 su uključeni u QL1.
Troškovi za projekat P1 uključeni su u QL2.
Nema preklapanja u onome što je uključeno u svaku stavku ponude, tako da je to važeće.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" rowspan="2" valign="top">
                <p>
Ne važi </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Kršenje gorenavedenog pravila br. 1 </p>
                <p>
Q1 uključuje vreme, troškove i naknade za ceo projekat P1.
                </p>
                <p>
QL2 uključuje vreme, troškove i naknade za ceo projekat P1 i preklapa se sa onim što je uključeno u Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Važeći </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na osnovu pravila br. 2, Q1 i Q2 su dve ponude u istoj mogućnosti za poslovanje, tako da obe mogu proceniti iste komponente projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 na Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Važeći </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Na osnovu pravila br. 3, Q1 i Q2 su dve ponude u različitim mogućnostima za poslovanje, tako da one ne mogu proceniti komponente istog projekta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
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
            <td width="54" valign="top">
                <p>
Ne važi </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
