---
title: Trenutno stanje
description: Ova tema pruža informacije o tome kako se radi sa stvarnim podacima u usluzi Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581301"
---
# <a name="actuals"></a>Trenutno stanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Trenutno stanje predstavlja pregledani i odobreni finansijski i vremenski raspored projekta. One se kreiraju kada se odobre stavke vremena, troškova i korišćenja materijala, stavke naloga i fakture.

> [!IMPORTANT]
> Stvarne stvari ne bi trebalo uređivati ili brisati iz sistema. U suprotnom, finansijski integritet i bilo kakva integracija sa drugim finansijskim i računovodstvenim sistemima mogla bi da bude nepovoljno pogođena. Microsoft Dynamics 365 Project Operations vam omogućava da koristite reverziju i zamenu stvarnih stvari za uređivanje stvarnih stvari na različitim tačkama životnog ciklusa poslovnog procesa vaših projekata.

## <a name="recording-actuals-based-on-project-events"></a>Evidentiranje stvarnih vrednosti na osnovu događaja u projektu

Operacije projekta zapisuje finansijske transakcije do kojih dolazi tokom životnog ciklusa angažovanja projekta kao stvarne. Stvaranje stvarnih stvari na različitim događajima u životnom ciklusu varira, u zavisnosti od toga da li angažovanje projekta koristi model naplate vremena i materijala ili model naplate fiksne cene, kao i da li je u fazi pretpristupne prodaje ili je u internom projektu.

Sledeće teme sadrže objašnjenja o uticaju na tabelu "Stvarne stvari" na različite događaje za različite varijacije:

- [Stvarni uticaj u vremenu i angažovanju materijala](ActualsonTM.md)
- [Stvarni uticaj na angažovanje fiksne cene](ActualonFP.md)
- [Stvarni uticaj u pred-prodajnoj fazi angažovanja](ActualonPreSales.md)
- [Stvarni uticaj na interni projekat](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
