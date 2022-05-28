---
title: Kreiranje predloška za radne sate
description: Ova tema opisuje kako da kreirate predloške za radne sate u aplikaciji Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598965"
---
# <a name="create-a-work-hours-template-project-service"></a>Kreiranje predloška radnih sati (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Izaberite karticu resursa **Radno vreme** i dovršite uputstva u [Postavite radno vreme za resurs](/dynamics365/field-service/set-work-hours-resource) za konfigurisanje pravila kalendara.

**Kreirajte novi predložak kalendara**

1. Idite na **Podešavanja** \> **Šablon kalendara**.
2. Izaberite **Novo** i unesite ime, opis i resurs šablona.


> [!NOTE]
> Kada se na resurs navodi šablon kalendara, kopija kalendara resursa pridružuje se šablonu kalendara. Ako promenite radno vreme kopiranog šablona, te promene se neće preneti na radno vreme kalendara.


### <a name="see-also"></a>Takođe pogledajte  
 [Podešavanje resursa](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
