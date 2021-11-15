---
title: Deinstaliranje programa Dynamics 365 Project Operations
description: Ova tema pruža informacije o načinu deinstaliranja usluge Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783660"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Deinstaliranje programa Dynamics 365 Project Operations 

_**Odnosi se na:** Project Operations za scenarije zasnovane na resursima / bez zaliha_

Da biste deinstalirali uslugu Dynamics 365 Project Operations, mora vam biti dodeljena uloga administratora.

1. Idite na stavku **Podešavanja** > **Rešenja**.

    ![Stranica Podešavanja.](./media/uninstall-proj-ops-solutions.png)
  
2. Uklonite rešenja tačnom redosledom kojim su navedena u sledećoj tabeli. 

    | Korak | Naziv rešenja                                    | Beleška                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 2 | ProjectOperations_Anchor                           | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 5 | ProjectService                                     | Nema dodatnih beleški.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Nema dodatnih beleški.                                                                         |
    | 7 | ProjectServiceCore                                 | Nema dodatnih beleški.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 9 | FieldServiceCommon                                 | Potrebno za dvostruko pisanje sa uslugom Dynamics 365 Finance ili Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Potrebno za dvostruko pisanje sa uslugom Dynamics 365 Finance ili Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Obavezno za Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Obavezno za Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Obavezno za Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Obavezno za Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Obavezno za Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Obavezno za Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Obavezno za Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 19 | Dynamics365Notes                                   | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 21 | DualWriteCore                                      | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 23 | Dynamics365AssetManagement                         | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 26 | HCMCommon                                          | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 28 | Izvođač                                              | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 29 | Dynamics365Company                                 | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 30 | CurrencyExchangeRates                              | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
    | 31 | AssetCommon                                        | Ako ga ne nađete, preskočite ovo rešenje.                                                            |
