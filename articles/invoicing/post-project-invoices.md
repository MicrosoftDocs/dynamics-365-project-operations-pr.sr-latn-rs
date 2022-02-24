---
title: Pregled procesa fakturisanja
description: Ova tema pruža pregled procesa fakturisanja u usluzi Project Operations za scenarije zasnovane na resursima/bez zaliha.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089295"
---
# <a name="invoicing-process-overview"></a>Pregled procesa fakturisanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Project Operations za scenarije zasnovane na resursima/bez zaliha nudi sveobuhvatne mogućnosti prilagođene da odgovaraju potrebama i menadžera projekta i službenika/računovođe projekta za potraživanja. Za postupak fakturisanja, menadžer projekta upravlja zaostalim naplatama za projekat, a službenik/računovođa projekta za potraživanja kreira usaglašen i tačan dokument fakture za klijenta.

![Dijagram toka fakturisanja](./media/invoicing-flow.png)

Predmet ugovora za projekat definiše način naplate za povezane projektne transakcije. Kada menadžer projekta odobri transakcije vremena i troškova, sistem evidentira transakcije u entitetu **Stvarne vrednosti projekta** i šalje informacije u modul **Upravljanje projektima i računovodstvo** u usluzi Dynamics 365 Finance. Računovođa projekta zatim pregledava i objavljuje evidenciju pomoću [Project Operations dnevnika integracije](../project-accounting/project-operations-integration-journal.md). Ovaj dnevnik sadrži važne računovodstvene detalje za stvarne podatke o projektu, kao što su naplata, grupa za porez na promet, grupa za porez na promet stavki na računu i finansijski aspekti.

Menadžer projekta može pregledati nenaplaćene prodajne transakcije koristeći način naplate vremena i materijala u delu [Preostala naplata vremena i materijala](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) i način naplate sa fiksnom cenom u delu [Kontrolne tačke sa fiksnom cenom](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Ovi prikazi vam omogućavaju da filtrirate i odaberete transakcije koje treba da budu uključene u sledeći ciklus naplate, a zatim ih označite kao **Spremno za fakturisanje**.

Možete [ručno da kreirate profakturu](../proforma-invoicing/create-manual-proforma-invoice.md) ili da koristite [periodični proces](../proforma-invoicing/configure-automated-invoice-creation.md). Menadžer projekta može da [prilagodi radnu verziju profakture](../proforma-invoicing/manage-proforma-invoice.md) po potrebi, a zatim da je potvrdi.

Potvrđena profaktura se šalje u modul **Upravljanje projektima i računovodstvo** u usluzi Finance. Računovođa projekta formatira i ažurira predlog fakture projekta, a zatim knjiži i štampa dokument. Proknjižene fakture projekata evidentiraju se u glavnoj knjizi, kao i u potknjigama za klijenta i projekat.
