---
title: Potvrda predračuna za projekat
description: Ova tema pruža informacije o potvrđivanju predračuna za projekat u usluzi Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 276f54936ad9fd72fdc7e85196b43463572e6d3e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600299"
---
# <a name="confirm-a-proforma-project-invoice"></a>Potvrda predračuna za projekat 

_**Odnosi se na:** Jednostavna primena – od pogodbe do profakture_


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
Stvarna nenaplaćena prodaja negativnog iznosa obustave ili avansa, koja će se koristiti za sravnjenje.
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
Novi nenaplaćeni stvarni iznos prodaje koji je nenaplativ za preostale sate i iznos nakon odbijanja ispravljenih cifara na detalju linije uređene fakture, storniranje stvarnog iznosa prodaje i ekvivalentan stvarni naplaćeni iznos prodaje.
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
Naplaćeni stvarni iznos prodaje za količinu i iznos na originalnom odobrenju za troškove </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Fakturisanje predmeta ugovora zasnovanog na proizvodu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Naplaćeni stvarni iznos prodaje za liniju proizvoda sa količinom i iznosom koji potiču iz predmeta ugovora zasnovanog na proizvodu.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
