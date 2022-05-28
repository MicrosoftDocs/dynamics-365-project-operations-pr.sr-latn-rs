---
title: Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?
description: Ova tema pruža informacije o tome zašto ne možete obrisati zapise iz entiteta stvarnih vrednosti.
author: JPBurrows
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ff2c951905324d5d05722f399057c03d22f1a1c9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584429"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Project Service Automation (PSA) ne dopušta vam brisanje stvarnih vrednosti jer one služe kao izvor istine za transakcije koje imaju finansijske implikacije na dolazne sisteme, kao što je glavna knjiga. Ako bi se stvarne vrednosti mogle izbrisati, mogao bi se dovesti u pitanje integritet transakcija finansijskog izveštavanja. Da bi uspostavili evidenciju nadgledanja, klijenti bi trebalo da koriste dnevnike za kreiranje transakcija kompenzacije.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
