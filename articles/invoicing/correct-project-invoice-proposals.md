---
title: Ispravka računovodstva na radnim verzijama predloga faktura za projekat
description: Ova tema objašnjava kako da prilagodite računovodstvene informacije u radnoj verziji predloga fakture.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bf0a3d6b97880920b133cb3b30389adf0c83111c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575091"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Ispravka računovodstva na radnim verzijama predloga faktura za projekat

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

*Operativne detalje* za fakture projekata vodi menadžer projekta na predračunu. Ovi detalji uključuju odluku o radnom vremenu, troškovima, materijalima ili kontrolnim tačkama koje se moraju fakturisati, cenama i primeni iznosa avansa i akontacija. Kada potvrdite originalni predračun, možete prilagoditi operativne detalje kreiranjem i potvrđivanjem [korektivnog predračuna](../proforma-invoicing/corrective-invoices.md).

*Računovodstveni detalji* za fakture projekata se održavaju u dokumentu fakture prema kupcu. Ovi detalji uključuju obračun poreza na promet i finansijske dimenzije koje se primenjuju na fakturi. Ova tema pruža detalje o tome kako se ovi računovodstveni detalji mogu prilagoditi u radnoj verziji predloga fakture projekta.

## <a name="adjust-sales-tax"></a>Prilagođeni porez na promet

Podrazumevane grupe za obračun poreza na promet i grupe poreza na promet stavki mogu se prilagoditi direktno na dokument predloga fakture. Da biste prilagodili te grupe, izaberite **Uredi**, a zatim u svaki red predloga za fakturu projekta unesite novu vrednost u polje **Grupa poreza na promet** ili **Grupa poreza na promet stavke**.

## <a name="adjust-financial-dimensions"></a>Prilagođeni finansijski aspekti

### <a name="header-dimensions"></a>Dimenzije zaglavlja

Podrazumevano, finansijske dimenzije fakture su izvedene iz zapisa neželjenih transakcija projekta koji se fakturiše. Međutim, postavke sistema vam omogućava da koristite finansijske dimenzije u zaglavlju predloga faktura projekta za knjiženje salda kupaca. Da biste omogućili ovu funkcionalnost, na kartici **"** **·** **Finansije" na stranici "Upravljanje projektima i računovodstvenim parametrima" izaberite stavku Dozvoli ažuriranje dimenzija** projekta za potraživanja.

Finansijske dimenzije u zaglavljima faktura se mogu uređivati pre knjiženja fakture. Na stranici **Predlog fakture projekta** prebacite se u prikaz **zaglavlja**, a zatim uredite vrednosti na kartici **Finansijske dimenzije**.

Prikaz **zaglavlja** je dostupan tek kada administrator sistema omogući korišćenje predloga fakture **projekta i obrazaca naloga faktura sa funkcijom prikaza zaglavlja** i redova u **radnom prostoru za upravljanje** funkcijama. Ova funkcija zahteva ispravku finansija 10.0.25 ili noviju.

### <a name="line-dimensions"></a>Dimenzije reda

Finansijski aspekti se ne mogu direktno uređivati na stavci predloga fakture projekta. Umesto toga, sledite ove korake za prilagođavanje finansijskih aspekata na predlogu fakture projekta.

1. Na predlogu fakture projekta, izaberite **Izbriši sve** da uklonite redove predloga fakture projekta.

    Dugme **Izbriši sve** je dostupno samo nakon što administrator sistema omogući funkciju **Izbrišite redove predloga fakture kada Project Operations koristite za scenarije zasnovane na resursima / bez zaliha** u radnom prostoru **Upravljanje funkcijama**.

2. Prilagođavanje finansijskih aspekata:

    - **Transakcije na računu (kontrolne tačke obračuna):** Idite na **Svi projekti** \> **Upravljanje** \> **Transakcije na računu** i izaberite kontrolnu tačku koja zahteva prilagođavanje. Zatim na kartici **Finansijski aspekti** ažurirajte vrednosti po potrebi.
    - **Vreme, troškovi i materijalne transakcije:** Na stranici **Objavljene transakcije projekata** izaberite **Prilagođavanje računovodstva** da biste ažurirali finansijske aspekte.

3. Kada završite prilagođavanje vrednosti finansijskih aspekata, idite na **Upravljanje projektima i računovodstvo** \> **Periodično** \> **Project Operations integracija** i izaberite **Uvoz iz pripremne tabele** da pokrenete periodični proces. Taj proces koristi ažurirane vrednosti finansijskih aspekata za ponovno kreiranje stavki predloga fakture projekta. Ažurirane vrednosti se zatim koriste u knjizi analitike projekta i glavnoj knjizi kada se knjiži faktura projekta.
