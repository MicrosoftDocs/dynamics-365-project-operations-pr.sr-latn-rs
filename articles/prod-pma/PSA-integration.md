---
title: Pregled usluge Project Service Automation
description: Ovaj tema pruža informacije o rešenju Dynamics 365 Project Service Automation za Dynamics 365 Finance integracije.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b8588e664f140ca1b0dd740d27fe6a5137da595
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685579"
---
# <a name="project-service-automation-overview"></a>Pregled usluge Project Service Automation

[!include[banner](../includes/banner.md)]


Rešenje za automatizaciju usluge projekta za finansiranje integracije koristi funkciju integracije podataka za sinhronizaciju podataka u Dynamics 365 Finance i putem Dynamics 365 Project Service Automation Common Data Service. Predlošci integracije koji su dostupni sa funkcijom Integracija podataka omogućavaju tok projekata, ugovore o projektu, predmete ugovora o projektu, kontrolne tačke predmeta ugovora o projektu, projektne zadatke, kategorije transakcija troškova, procene sati i procene troškova iz usluge Project Service Automation u Finance.

> [!NOTE]
> - Ako koristite verziju 7.3.0, morate instalirati KB 4074835. Tada ćete moći da integrišete projekte sa fiksnom cenom.
> - Ako koristite verziju 7.3.0, a transakcije naknada prenosite iz usluge Project Service Automation, morate instalirati KB 4345320 da biste te naknade uključili u fakturu projekta.
> - Ako koristite verziju 8.0, moći ćete da koristite integraciju projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti.
> - Ako koristite verziju 8.0.1 ili noviju, moći ćete da sinhronizujete aktuelne podatke.

Da biste mogli da integrišete Project Service Automation Finance, morate konfigurisati parametre integracije usluge Project Service Automation. Za više informacija, pogledajte: [Integrisanje parametara usluge Project Service Automation](PSA-parameters.md).

Ovo rešenje za integraciju omogućava direktnu sinhronizaciju u sledećim scenarijima:

- Održavajte ugovore o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Kreirajte projekte u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Održavajte predmete ugovora o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Održavajte kontrolne tačke predmeta ugovora o projektu u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Održavajte projektne zadatke u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Održavajte kategorije transakcija troškova u usluzi Finance i sinhronizujte ih direktno iz usluge Finance u Project Service Automation.
- Kreirajte procene časova projekta u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Kreirajte procene troškova projekta u usluzi Project Service Automation i sinhronizujte ih direktno iz usluge Project Service Automation u Finance.
- Kreirajte aktuelne podatke o vremenu, troškovima i naknadama u usluzi Project Service Automation i kreirajte projektne transakcije u dnevniku Project Service Automation integracije tako da mogu biti proknjiženi u usluzi Finance.

## <a name="data-synchronization"></a>Sinhronizacija podataka

Sledeća ilustracija prikazuje kako se podaci sinhronizuju kao deo integracije između usluga Project Service Automation i Finance.

> [!NOTE]
> Trenutno nisu dostupni svi predlošci. Predlošci će biti objavljeni po završetku.

[![Integracija usluge Project Service Automation sa uslugom Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Sistemski zahtevi za Finance

Da biste koristili rešenje za integraciju usluge Project Service Automation u Finance, morate instalirati Enterprise Edition 7.3 sa ispravkom platforme 12 ili novijom.

## <a name="system-requirements-for-project-service-automation"></a>Sistemski zahtevi za Project Service Automation

Da biste koristili rešenje za integraciju usluge Project Service Automation u Finance, morate instalirati sledeće komponente:

- Dynamics 365 Project Service Automation verzija 9.0.0.0 ili novija
- Moguće rešenje za gotovinu za Dynamics 365 Sales, verzija 1.14.0.0 (v14) ili novija
- Rešenje Project Service Automation u Finance za Dynamics 365 Project Service Automation verzija 1.0.0.0 ili novija

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Instaliranje rešenja za integraciju usluge Project Service Automation u Finance u vašoj instanci usluge Project Service Automation

Preuzmite rešenje za integraciju Project Service Automation u Finance iz [Microsoft centra za preuzimanje](https://www.microsoft.com/download/details.aspx?id=57016) i sledite uputstva koja ste dobili uz rešenje.


[!INCLUDE[footer-include](../includes/footer-banner.md)]