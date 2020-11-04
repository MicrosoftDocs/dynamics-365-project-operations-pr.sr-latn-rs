---
title: Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?
description: Ova tema pruža informacije o tome zašto ne možete obrisati zapise iz entiteta stvarnih vrednosti.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083706"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c76e9-103">Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?</span><span class="sxs-lookup"><span data-stu-id="c76e9-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c76e9-104">Project Service Automation (PSA) ne dopušta vam brisanje stvarnih vrednosti jer one služe kao izvor istine za transakcije koje imaju finansijske implikacije na dolazne sisteme, kao što je glavna knjiga.</span><span class="sxs-lookup"><span data-stu-id="c76e9-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c76e9-105">Ako bi se stvarne vrednosti mogle izbrisati, mogao bi se dovesti u pitanje integritet transakcija finansijskog izveštavanja.</span><span class="sxs-lookup"><span data-stu-id="c76e9-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c76e9-106">Da bi uspostavili evidenciju nadgledanja, klijenti bi trebalo da koriste dnevnike za kreiranje transakcija kompenzacije.</span><span class="sxs-lookup"><span data-stu-id="c76e9-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

