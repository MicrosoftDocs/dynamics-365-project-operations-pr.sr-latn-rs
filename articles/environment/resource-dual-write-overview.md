---
title: Project Operations integracija dvostrukog upisivanja
description: Ova tema pruža pregled Project Operations integraciji dvostrukog upisivanja.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: b65c40e8aaa9524c1c634738dadd23f21e86e2ec095c47bc849467c8806addbc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007928"
---
# <a name="project-operations-dual-write-integration-overview"></a>Pregled Project Operations integracije dvostrukog upisivanja

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Project Operations koristi [mogućnosti dvostrukog upisivanja](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) za sinhronizaciju podataka u Microsoft Dataverse i Dynamics 365 Finance.

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