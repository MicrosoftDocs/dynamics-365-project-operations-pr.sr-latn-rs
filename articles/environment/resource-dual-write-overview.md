---
title: Project Operations integracija dvostrukog upisivanja
description: Ova tema pruža pregled Project Operations integraciji dvostrukog upisivanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9b57b8bab9a6821e71a16b191804af21ae5d0b5a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582773"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled Project Operations integracije dvostrukog upisivanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Operacije projekta koriste [mogućnosti dvostrukog pisanja za](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) sinhronizaciju podataka preko Microsoft Dataverse i Dynamics 365 Finance.

Sledeća ilustracija pokazuje kako se podaci sinhronizuju kao deo ove integracije između Dataverse i Finance.

![Pregled Project Operations tokova podataka.](./media/ProjectOperationsFlows.jpg)

Project Operations u Dataverse pruža moderan korisnički interfejs (UI) i jednostavnu proširivost bez kodiranja/sa malo kodiranja pomoću Power Platform mogućnosti. Menadžeri projekata, menadžeri resursa, članovi projektnog tima i osobe koje rade sa klijentima obavljaju svoje aktivnosti u Project Operations u Dataverse.

Project Operations u Finance pruža podršku projektnom računovodstvu i priznavanju prihoda. Project Operations se uključuju u finansijski okvir u Finance za obračun poreza na promet, kurseve valuta, izveštavanje o finansijskoj dimenziji i još mnogo toga. Iskustva računovođa na projektu uglavnom se temelje na Finance.

Project Operations integracija sastoji se od sledeće integracije komponenata:


- [Project Operations podešavanje i integracija podataka o konfiguraciji](resource-dual-write-setup-integration.md) 
- [Procene i stvarne vrednosti u projektu](resource-dual-write-estimates-actuals.md)
- [Fakture projekta](resource-dual-write-project-invoice.md)
- [Upravljanje troškovima](resource-dual-write-expense.md)
- [Faktura prodavca](resource-dual-write-vendor-invoice.md)
