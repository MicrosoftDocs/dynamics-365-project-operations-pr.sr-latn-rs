---
title: Definisanje kalendara projekata
description: Ova tema pruža informacije o tome kako primeniti šablon kalendara na projekat za praćenje rasporeda projekata.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 181032b27ee67591a3bb40ab080477c51c1e34a46e9aac20039e4e5df3a5ab1d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000953"
---
# <a name="define-project-calendars"></a>Definisanje kalendara projekata

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima/bez zaliha, jednostavna primena – od pogodbe do profakture_

Da biste kreirali i upravljali projektom, na njega morate primeniti šablon kalendara. Predložak kalendara definiše sledeće atribute projekta:

- Radno vreme, uključujući vreme početka i završetka
- Radni dani
- Izuzeci iz kalendara kao što su neradni dani

Šablon kalendara koji se primenjuje na projekat je kopija šablona kalendara definisanog u podešavanjima vaše organizacije.

> [!NOTE]
> Ako promenite šablon kalendara, te promene se neće preneti na radno vreme projekta. Da biste promenili radno vreme projekta, mora se primeniti novi obrazac.

Da biste kreirali šablon kalendara za svoju organizaciju, postoje dva ključna zahteva:

- Definišite željeno radno vreme šablona pomoću novog ili postojećeg resursa koji se može rezervisati.
- Napravite novi šablon kalendara i povežite ga sa resursom koji možete rezervirati.

**Definišite radno vreme šablona**

1. Idite na **Resursi** \> **Resursi**.
2. Napravite novi resurs za referencu u predlošku kalendara ili odaberite postojeći.
3. Izaberite karticu resursa **Radno vreme** i dovršite uputstva u [Postavite radno vreme za resurs](/dynamics365/field-service/set-work-hours-resource.md) za konfigurisanje pravila kalendara.

**Kreirajte novi predložak kalendara**

1. Idite na **Podešavanja** \> **Šablon kalendara**.
2. Izaberite **Novo** i unesite ime, opis i resurs šablona.

> [!NOTE]
> Kada se na resurs navodi šablon kalendara, kopija kalendara resursa pridružuje se šablonu kalendara. Ako promenite radno vreme kopiranog šablona, te promene se neće preneti na radno vreme kalendara.

Sada možete povezati radni predložak sa predloškom kalendara projekta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

