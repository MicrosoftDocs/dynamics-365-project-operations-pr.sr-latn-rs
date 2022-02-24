---
title: Korektivne fakture za projekat
description: Ova tema pruža informacije o tome kako da kreirate i potvrdite korektivne fakture u usluzi Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866608"
---
# <a name="corrective-project-invoices"></a>Korektivne fakture za projekat

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_

Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.

Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**. 

> [!NOTE]
> Ovaj izbor nije dostupan ukoliko se ne potvrdi faktura projekta.

Iz potvrđene fakture kreira se nova radna verzija fakture. Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju. Slede neke od ključnih tačaka koje treba razumeti u vezi sa detaljima linije na novoj ispravljenoj fakturi:

- Sve količine su ažurirane na nulu. Aplikacija pretpostavlja da su sve fakturisane stavke u potpunosti zadužene. Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje. Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu. Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura. Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.
- Prethodno potvrđeni predmeti ugovora zasnovani na proizvodu se ne kopiraju. Obrada ispravki na fakturi projekta zasnovanog na proizvodu nije podržana.
- Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.
- Iznosi obustave ili avansa mogu se ispraviti ako je klijentu fakturisan netačan iznos.
- Sravnjenja obustava i avansa mogu se ispraviti ako je korišćen netačan iznos za stavnjenje troškova na prethodno potvrđenoj fakturi.

> [!IMPORTANT]
> Podaci o liniji fakture koji predstavljaju ispravke drugih već fakturisanih troškova imaju polje **Ispravka** podešeno na **Da**. Fakture koje imaju ispravljene detalje o liniji fakture imaju polje **Ima ispravke** koje je takođe postavljeno na **Da**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Trenutno stanje kreirano kada je potvrđena korektivna faktura

Sledeća tabela navodi stvarne podatke koji se kreiraju kada se potvrdi faktura sa ispravkom.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Stvarni podaci kreirani prilikom potvrde</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrdite ispravku fakturisanog avansa ili obustave.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje. Ovaj iznos je pozitivan jer ima za cilj da poništi negativ nastao prilikom fakturisanja obustave ili avansa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni iznos stornirane naplaćene prodaje kreira se za iznos na obustavi ili avansu da bi se poništila prvobitna naplaćena prodaja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Kreira se novi fakturisani stvarni trošak prodaje za ispravljeni iznos ili ispravljenoj liniji fakture na osnovu obustave ili avansa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarna nenaplaćena prodaja negativnog iznosa ispravljene linije fakture na osnovu obustave ili avansa, koja će se koristiti za sravnjenje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Potvrda ispravke prethodno sravnjene obustave ili avansa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za obustavu ili avans koji je kreiran za sravnjenje. Ovaj iznos je pozitivan i ima za cilj da poništi negativan iznos nastao prilikom prethodnog sravnjenja.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni iznos stornirane naplaćene prodaje za iznos na prethodnoj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi naplaćeni stvarni trošak prodaje za ispravljeni iznos obustave koji se primenjuje na ispravljenu fakturu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarna nenaplaćena prodaja sa negativnim iznosom sa ispravljene preostale obustave ili avansa, koja će se koristiti za sravnjenje na kasnijim fakturama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje punog kredita prethodno fakturisane vremenske transakcije.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje za sate i iznos na originalnom detalju linije fakture za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje delimičnog kredita za vremensku transakciju.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos fakturisan na originalnom detalju linije fakture za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje punog kredita prethodno fakturisane transakcije troškova.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje delimičnog kredita prethodno fakturisane transakcije troškova.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za trošak.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije ispravljene fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje punog kredita prethodno fakturisane materijalne transakcije.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova stvarna vrednost nenaplaćene prodaje za količinu i iznos na detaljima stavki originalne fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje delimičnog kredita za transakciju materijala.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za fakturisanu količinu i iznos na detaljima stavki originalne fakture za materijal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nova nefakturisana stvarna prodaja koja se naplaćuje za količinu i iznos na izmenjenom detalju stavke fakture, storniranje ove stavke i ekvivalentni stvarni iznos naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije fakture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje punog kredita prethodno fakturisane transakcije naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje za količinu i iznos na originalnom detalju linije fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje delimičnog kredita prethodno fakturisane transakcije naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za količinu i fakturisani iznos na originalnom detalju linije fakture za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene korektivne fakture, storniranje ove stavke i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturisanje punog kredita prethodno fakturisane kontrolne tačke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje naplaćene prodaje za sate i iznos na originalnom detalju linije fakture za kontrolnu tačku.
                </p>
                <p>
Status fakture na kontrolnoj tački se ažurira iz <b>Proknjižena faktura za klijenta</b> u <b>Spremno za fakturisanje</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturisanje delimičnog kredita prethodno fakturisane kontrolne tačke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepodržano </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Krediti i ispravke prethodno fakturisanog predmeta ugovora zasnovanog na proizvodu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Nepodržano </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
