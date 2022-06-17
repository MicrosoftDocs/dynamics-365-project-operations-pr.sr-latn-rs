---
title: Trenutno stanje
description: Ovaj članak pruža informacije o radu sa stvarnim podacima korporacije Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924815"
---
# <a name="actuals"></a>Trenutno stanje

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Trenutno stanje predstavlja pregledani i odobreni finansijski i vremenski raspored projekta. One se kreiraju kada se odobre stavke vremena, troškova i korišćenja materijala, stavke naloga i fakture.

> [!IMPORTANT]
> Stvarne stvari ne bi trebalo uređivati ili brisati iz sistema. U suprotnom, finansijski integritet i bilo kakva integracija sa drugim finansijskim i računovodstvenim sistemima mogla bi da bude nepovoljno pogođena. Microsoft Dynamics 365 Project Operations vam omogućava da koristite reverziju i zamenu stvarnih stvari za uređivanje stvarnih stvari na različitim tačkama životnog ciklusa poslovnog procesa vaših projekata.

## <a name="recording-actuals-based-on-project-events"></a>Evidentiranje stvarnih vrednosti na osnovu događaja u projektu

Operacije projekta zapisuje finansijske transakcije do kojih dolazi tokom životnog ciklusa angažovanja projekta kao stvarne. Stvaranje stvarnih stvari na različitim događajima u životnom ciklusu varira, u zavisnosti od toga da li angažovanje projekta koristi model naplate vremena i materijala ili model naplate fiksne cene, kao i da li je u fazi pretpristupne prodaje ili je u internom projektu.

Sledeći članci sadrže objašnjenja o uticaju na tabelu "Stvarne stvari" na različite događaje za različite varijacije:

- [Stvarni uticaj u vremenu i angažovanju materijala](ActualsonTM.md)
- [Stvarni uticaj na angažovanje fiksne cene](ActualonFP.md)
- [Stvarni uticaj u pred-prodajnoj fazi angažovanja](ActualonPreSales.md)
- [Stvarni uticaj na interni projekat](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
