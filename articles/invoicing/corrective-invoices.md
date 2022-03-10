---
title: Kreiranje korektivnih faktura zasnovanih na projektu
description: Ova tema pruža informacije o korektivnim fakturama u usluzi Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006217"
---
# <a name="create-corrective-project-based-invoices"></a>Kreiranje korektivnih faktura zasnovanih na projektu 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Potvrđena faktura projekta može se ispraviti tako da obrađuje promene ili kredite prema dogovoru sa klijentom i menadžerom projekta.

Da biste izvršili izmene na potvrđenoj fakturi, otvorite potvrđenu fakturu i izaberite **Ispravite ovu fakturu**. 

> [!NOTE]
> Ovaj izbor nije dostupan ukoliko se ne potvrdi faktura projekta.

Iz potvrđene fakture kreira se nova radna verzija fakture. Svi detalji linije fakture iz prethodno potvrđene fakture kopiraju se u novu radnu verziju. Slede neke ključne tačke koje će vam pomoći da razumete više o detaljima stavki na novoj ispravljenoj fakturi:

- Sve količine su ažurirane na nulu. To pretpostavlja da su sve fakturisane stavke u potpunosti zadužene. Ako je potrebno, ove količine možete ručno ažurirati tako da odražavaju količinu koja se fakturiše, a ne količinu koja se zadužuje. Na osnovu količine koju unesete, aplikacija izračunava zaduženu količinu. Ovaj iznos se ogleda u stvarnim troškovima koji se zadužuju kada se potvrdi ispravljena faktura. Ako menjate iznos poreza, morate uneti tačan iznos poreza, a ne iznos poreza koji se zadužuje.
- Ispravke kontrolnih tačaka uvek se obrađuju kao puna zaduženja.
- Iznosi obustave ili avansa mogu se ispraviti ako je klijentu fakturisan netačan iznos.
- Sravnjenja obustava i avansa mogu se ispraviti ako je korišćen netačan iznos za stavnjenje troškova na prethodno potvrđenoj fakturi.

> [!IMPORTANT]
> Detalji stavke fakture koje predstavljaju ispravke za druge već fakturisane troškove sadrže polje **Ispravka** podešeno na **Da**. Fakture koje imaju ispravljene detalje o liniji fakture imaju polje **Ima ispravke** koje je takođe postavljeno na **Da**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Trenutno stanje kreirano na potvrdi korektivne fakture

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
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]