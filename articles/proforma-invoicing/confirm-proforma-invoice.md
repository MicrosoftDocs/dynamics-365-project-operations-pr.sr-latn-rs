---
title: Potvrda predračuna zasnovanog na projektu
description: Ova tema pruža informacije o potvrđivanju predračuna zasnovanog na projektu.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012153"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Potvrda predračuna zasnovanog na projektu

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Nakon potvrde predračuna, status fakture projekta se ažurira na **Potvrđeno**. Kada se faktura potvrdi, postaje samo za čitanje. Ubuduće se faktura može ispraviti samo ako postoje ispravke ili krediti koje je pokrenuo klijenti.

U sledećoj tabeli su navedeni stvarni podaci koje je kreirao sistem. Ovi stvarni podaci se kreiraju kada se izvrše određene radnje na radnoj verziji fakture projekta pre nego što se ona potvrdi.

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
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje avansa ili odbitka </p>
            </td>
            <td width="408" valign="top">
                <p>
Fakturisani stvarni iznos prodaje, <strong>Odbitak</strong> kreira se za iznos na avansu ili obustavi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni iznos nenaplaćene prodaje sa negativnim iznosom obustave ili avansa koji će se koristiti za sravnjenje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Nakon potpunog sravnjenja obustave ili avansa na fakturi.
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
Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Nakon delimičnog sravnjenja obustave ili avansa na fakturi.
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
Stvarni iznos naplaćene prodaje za iznos na ovoj fakturi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Negativna stvarna nenaplaćena prodaja preostalog iznosa obustave ili avansa, koja će se koristiti za sravnjenje na budućim fakturama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje vremenske transakcije bez ikakvih izmena na radnoj verziji fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naplaćeni stvarni iznos prodaje za sate i iznos na originalnom odobrenju za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje vremenske transakcije koja je uređena da bi se smanjila količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi stvarni iznos nenaplaćene prodaje koji se ne naplaćuje za preostale sate i iznos nakon odbijanja ispravljenih podataka na uređenom detalju stavke fakture, storniranja stvarne prodaje i ekvivalentni stvarni iznos naplaćene prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje vremenske transakcije koja je uređena da bi se povećala količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za sate i iznos na originalnom odobrenju za vreme.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za sate i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje transakcije troškova bez ikakvih izmena na radnoj verziji fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje transakcije troškova koja je uređena da bi se smanjila količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje transakcije troškova koja je uređena da bi se povećala količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju za troškove.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje transakcije materijala bez ikakvih izmena u radnoj verziji fakture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Stvarni iznos naplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Fakturisanje materijalne transakcije koja je uređena da bi se smanjila količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju vremena.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostalu količinu i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje transakcije materijala koja je uređena da bi se povećala količina.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za količinu i iznos na originalnom odobrenju korišćenja materijala.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Novi nenaplaćeni stvarni iznos prodaje koji je naplativ za količinu i iznos na detalju linije uređene fakture, storniranje nenaplaćenog stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Fakturisanje naknade.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Storniranje nenaplaćene prodaje za iznos naknade u originalnoj stavci u glavnoj knjizi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Naplaćeni stvarni iznos prodaje za količinu i iznos u originalnoj stavci u glavnoj knjizi za naknadu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Fakturisanje kontrolne tačke.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Naplaćeni stvarni iznos prodaje za iznos kontrolne tačke na originalnoj kontrolnoj tački u predmetu ugovora.
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
