---
title: Prosleđivanje zahteva za resurs
description: Ova tema pruža informacije o prosleđivanju zahteva za resurs projekta.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013188"
---
# <a name="submitting-a-resource-request"></a>Prosleđivanje zahteva za resurs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Generisanu potrebu za resursom možete proslediti kao zahtev za resurs. Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.

1. U aplikaciji Project Service Automation (PSA), na stranici **Projekti** kliknite na karticu **Tim** da biste videli listu resursa koji se mogu rezervisati. 
2. Sa liste izaberite generički resurs koji ima potrebu za resursom, a zatim kliknite na **Prosledi zahtev**.

![Prosleđivanje zahteva za resurs](media/RM-how-to-18.png)

Status zahteva generičkog člana tima će se promeniti u **Prosleđen**.

Kada menadžer resursa ispuni zahtev, generički resurs će biti zamenjen imenovanim resursom ako menadžer resursa ispuni zahtev rezervisanjem imenovanog resursa. U suprotnom, generički resurs će ostati u timu i status zahteva će se promeniti u **Zahteva pregled** ako je menadžer resursa predložio imenovani resurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]