---
title: Ispravka računovodstva na radnim verzijama predloga faktura za projekat
description: Ova tema objašnjava kako da prilagodite računovodstvene informacije u radnoj verziji predloga fakture.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251267"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ispravka računovodstva na radnim verzijama predloga faktura za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

*Operativne detalje* za fakture projekata vodi menadžer projekta na predračunu. Ovi detalji uključuju odluku o radnom vremenu, troškovima, materijalima ili kontrolnim tačkama koje se moraju fakturisati, cenama i primeni iznosa avansa i akontacija. Kada potvrdite originalni predračun, možete prilagoditi operativne detalje kreiranjem i potvrđivanjem [korektivnog predračuna](../proforma-invoicing/corrective-invoices.md).

*Računovodstveni detalji* za fakture projekata se održavaju u dokumentu fakture prema kupcu. Ovi detalji uključuju obračun poreza na promet i finansijske dimenzije koje se primenjuju na fakturi. Ova tema pruža detalje o tome kako se ovi računovodstveni detalji mogu prilagoditi u radnoj verziji predloga fakture projekta.

## <a name="adjust-sales-tax"></a>Prilagođeni porez na promet

Podrazumevane grupe za obračun poreza na promet i grupe poreza na promet stavki mogu se prilagoditi direktno na dokument predloga fakture. Da biste prilagodili te grupe, izaberite **Uredi**, a zatim u svaki red predloga za fakturu projekta unesite novu vrednost u polje **Grupa poreza na promet** ili **Grupa poreza na promet stavke**.

## <a name="adjust-financial-dimensions"></a>Prilagođeni finansijski aspekti

Finansijski aspekti se ne mogu direktno uređivati na stavci predloga fakture projekta. Umesto toga, sledite ove korake za prilagođavanje finansijskih aspekata na predlogu fakture projekta.

1. Na predlogu fakture projekta, izaberite **Izbriši sve** da uklonite redove predloga fakture projekta.

    > [!NOTE]
    > Dugme **Izbriši sve** je dostupno samo nakon što administrator sistema omogući funkciju **Izbrišite redove predloga fakture kada Project Operations koristite za scenarije zasnovane na resursima / bez zaliha** u radnom prostoru **Upravljanje funkcijama**.

2. Prilagođavanje finansijskih aspekata:

    - **Transakcije na računu (kontrolne tačke obračuna):** Idite na **Svi projekti** \> **Upravljanje** \> **Transakcije na računu** i izaberite kontrolnu tačku koja zahteva prilagođavanje. Zatim na kartici **Finansijski aspekti** ažurirajte vrednosti po potrebi.
    - **Vreme, troškovi i materijalne transakcije:** Na stranici **Objavljene transakcije projekata** izaberite **Prilagođavanje računovodstva** da biste ažurirali finansijske aspekte.

3. Kada završite prilagođavanje vrednosti finansijskih aspekata, idite na **Upravljanje projektima i računovodstvo** \> **Periodično** \> **Project Operations integracija** i izaberite **Uvoz iz pripremne tabele** da pokrenete periodični proces. Taj proces koristi ažurirane vrednosti finansijskih aspekata za ponovno kreiranje stavki predloga fakture projekta. Ažurirane vrednosti se zatim koriste u knjizi analitike projekta i glavnoj knjizi kada se knjiži faktura projekta.
