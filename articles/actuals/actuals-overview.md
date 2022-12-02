---
title: Trenutno stanje
description: Ovaj članak pruža informacije o tome kako se radi sa stvarnim podacima u usluzi Microsoft Dynamics 365 Project Operations.
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

Trenutno stanje predstavlja pregledani i odobreni finansijski i vremenski raspored projekta. Kreiraju se kada se odobravaju vreme, trošak, kao i stavke korišćenja materijala, stavke dnevnika i fakture odobravaju.

> [!IMPORTANT]
> Stvarne vrednosti ne bi trebalo uređivati niti brisati iz sistema. U suprotnom, to bi moglo imati negativan uticaj na finansijski integritet i bilo kakvu integraciju sa drugim finansijskim i računovodstvenim sistemima. Microsoft Dynamics 365 Project Operations vam omogućava da koristite preokretanje i zamenu stvarnih vrednosti za uređivanje stvarnih vrednosti tokom različitih tačaka u životnom ciklusu poslovnog procesa u vašim projektima..

## <a name="recording-actuals-based-on-project-events"></a>Evidentiranje stvarnih vrednosti na osnovu događaja u projektu

Project Operations beleži finansijske transakcije koje se dešavaju tokom životnog ciklusa angažovanja na projekta kao stvarne vrednosti. Kreiranje stvarnih vrednosti na različitim događajima u životnom ciklusu varira, u zavisnosti od toga da li angažovanje na projektu koristi model naplate prema vremenu i materijalu ili model naplate po fiksnoj ceni, kao i da li je u fazi pretpristupne prodaje ili je u internom projektu.

Sledeći članci objašnjavaju uticaj na tabelu „Stvarne vrednosti“ na različitim događajima za različite varijacije:

- [Uticaj stvarnih vrednosti u angažovanju u pogledu vremena i materijala](ActualsonTM.md)
- [Uticaj stvarnih vrednosti na angažovanje po fiksnoj ceni](ActualonFP.md)
- [Uticaj stvarnih vrednosti u pretprodajnoj fazi angažovanja](ActualonPreSales.md)
- [Uticaj stvarnih vrednosti za interni projekat](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
