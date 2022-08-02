---
title: Sinhronizuj projektne zadatke direktno iz automatizacije projektnih usluga u finansije i operacije
description: Ovaj članak opisuje predložak i osnovni zadatak koji se koristi za sinhronizaciju projektnog zadatka direktno iz Microsoft Dynamics 365 Project Service Automation Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ed559fcd9e0e666f68e7d9f4f1fca91417fe4970
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028378"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Sinhronizuj projektne zadatke direktno iz automatizacije projektnih usluga u finansije i operacije

[!include[banner](../includes/banner.md)]

Ovaj članak opisuje predložak i osnovni zadatak koji se koristi za sinhronizaciju projektnog zadatka direktno iz Dynamics 365 Project Service Automation Dynamics 365 Finance.

> [!NOTE]
> - Integracija projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i zaključavanje funkcionalnosti dostupni su u verziji 8.0.
> - Ako koristite Enterprise Edition 7.3.0, kada instalirate KB 4132657 i KB 4132660, moći ćete da koristite predloške za integrisanje projektnih zadataka, kategorije transakcija troškova, procene sati, procene troškova i stvarnih podataka, kao i da konfigurišite zaključavanje funkcionalnosti. Ako morate da resetujete računovodstvene distribucije, preporučili smo da instalirate i KB 4131710.
> - Integracija stvarnih podataka dostupna je u verziji 8.0.1 ili novijoj.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok podataka iz usluge Project Service Automation u Finance

Rešenje za integraciju iz usluge Project Service Automation u Finance koristi funkciju integracije podataka za sinhronizaciju podataka u svim instancama usluga Project Service Automation i Finance. Predložak za integraciju koji je dostupan sa funkcijom Integracija podataka omogućava tok podataka o projektnim zadacima iz usluge Project Service Automation u Finance.

Sledeća ilustracija prikazuje kako se podaci sinhronizuju između usluga Project Service Automation i Finance.

[![Tok podataka za integraciju usluge Project Service Automation sa uslugom Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Predložak i zadatak

Da biste pristupili predlošku, u Microsoft Power Apps centru administracije izaberite **Projekti**, a zatim u gornjem desnom uglu izaberite **Novi projekat** za odabir javnih obrazaca.

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

Microsoft za Excel morate da Power Query koristite za filtriranje podataka ako je ovaj uslov ispunjen:

- U projektnom zadatku imate zapise specifične za resurse.

Ako morate da koristite Power Query, sledite ovo uputstvo:

- Predložak projektnih zadataka (iz PSA u Fin and Ops) ima podrazumevani filter koji iz projektnog zadatka isključuje zapise specifične za resurse postavljanjem filtera na **IsLineTask** na **Netačno**. Ako kreirate sopstveni obrazac, morate dodati ovaj filter.

## <a name="template-mapping-in-data-integration"></a>Mapiranje predložaka u usluzi Data Integration

Sledeća ilustracija prikazuje primer mapiranja zadataka predloška u integraciji podataka. Mapiranje prikazuje informacije o terenu koje će se sinhronizovati iz usluge Project Service Automation u Finance.

[![Mapiranje predložaka.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]