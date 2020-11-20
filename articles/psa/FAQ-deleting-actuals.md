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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127175"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="94e3f-103">Zašto ne mogu da izbrišem zapise iz entiteta stvarnih vrednosti?</span><span class="sxs-lookup"><span data-stu-id="94e3f-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="94e3f-104">Project Service Automation (PSA) ne dopušta vam brisanje stvarnih vrednosti jer one služe kao izvor istine za transakcije koje imaju finansijske implikacije na dolazne sisteme, kao što je glavna knjiga.</span><span class="sxs-lookup"><span data-stu-id="94e3f-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="94e3f-105">Ako bi se stvarne vrednosti mogle izbrisati, mogao bi se dovesti u pitanje integritet transakcija finansijskog izveštavanja.</span><span class="sxs-lookup"><span data-stu-id="94e3f-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="94e3f-106">Da bi uspostavili evidenciju nadgledanja, klijenti bi trebalo da koriste dnevnike za kreiranje transakcija kompenzacije.</span><span class="sxs-lookup"><span data-stu-id="94e3f-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

