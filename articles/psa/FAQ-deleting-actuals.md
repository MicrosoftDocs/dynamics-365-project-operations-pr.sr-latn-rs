---
title: Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?
description: Ova tema pruža informacije o tome zašto ne možete obrisati zapise iz entiteta stvarnih vrednosti.
author: JPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
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
ms.openlocfilehash: e3122c5d9495b3ff9a683f477e719ce0c228a84d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286085"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne dopušta vam brisanje stvarnih vrednosti jer one služe kao izvor istine za transakcije koje imaju finansijske implikacije na dolazne sisteme, kao što je glavna knjiga. Ako bi se stvarne vrednosti mogle izbrisati, mogao bi se dovesti u pitanje integritet transakcija finansijskog izveštavanja. Da bi uspostavili evidenciju nadgledanja, klijenti bi trebalo da koriste dnevnike za kreiranje transakcija kompenzacije.



[!INCLUDE[footer-include](../includes/footer-banner.md)]