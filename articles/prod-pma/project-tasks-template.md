---
title: Sinhronizovanje projektnih zadataka direktno iz usluge Project Service Automation sa uslugom Finance and Operations
description: Ova tema opisuje predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka direktno iz usluge Microsoft Dynamics 365 Project Service Automation u Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083562"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizovanje projektnih zadataka direktno iz usluge Project Service Automation sa uslugom Finance and Operations

[!include[banner](../includes/banner.md)]

Ova tema opisuje predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka direktno iz usluge Dynamics 365 Project Service Automation u Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Ako koristite Enterprise Edition 7.3.0, kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti. Ako morate da resetujete računovodstvene distribucije, preporučili smo da instalirate i KB 4131710.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok podataka iz usluge Project Service Automation u Finance

Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predložak za integraciju koji je dostupan sa funkcijom Integracija podataka omogućava tok podataka o projektnim zadacima iz usluge Project Service Automation u Finance.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Predložak i zadatak

Da biste pristupili predlošku, u Microsoft Power Apps centru administracije izaberite **Projekti** , a zatim u gornjem desnom uglu izaberite **Novi projekat** za odabir javnih obrazaca.

Sledeći predložak i osnovni zadatak koji se koriste za sinhronizaciju projektnih zadataka iz usluge Project Service Automation u Finance:

- **Naziv predloška u Integraciji podataka:** Projektni zadaci (iz PSA u Fin and Ops)
- **Naziv zadatka u projektu:** Projektni zadaci

Da bi moglo da dođe do sinhronizacije projektnih zadataka, morate sinhronizovati ugovore o projektu i projekte.

## <a name="entity-set"></a>Skup entiteta

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Projektni zadaci              | Entitet integracije za projektni zadatak |

## <a name="entity-flow"></a>Tok entiteta

Projektnim zadacima se upravlja u usluzi Project Service Automation i oni se sinhronizuju sa uslugom Finance kao aktivnosti projekta.

## <a name="prerequisites-and-mapping-setup"></a>Preduslovi i podešavanje mapiranja

Da bi moglo da dođe do sinhronizacije projektnih zadataka, morate sinhronizovati ugovore o projektu i projekte.

## <a name="power-query"></a>Power Query

Morate koristiti Microsoft Power Query za Excel za filtriranje podataka ako je ispunjen ovaj uslov:

- U projektnom zadatku imate zapise specifične za resurse.

Ako morate da koristite Power Query, sledite ove smernice:

- Predložak projektnih zadataka (iz PSA u Fin and Ops) ima podrazumevani filter koji iz projektnog zadatka isključuje zapise specifične za resurse postavljanjem filtera na **IsLineTask** na **Netačno**. Ako kreirate sopstveni obrazac, morate dodati ovaj filter.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u integraciji podataka. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje predložaka](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]