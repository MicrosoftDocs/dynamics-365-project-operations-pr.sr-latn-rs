---
title: Prosleđivanje zahteva za resurs
description: Ova tema pruža informacije o prosleđivanju zahteva za resurs projekta.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755211"
---
# <a name="submit-a-resource-request"></a>Prosleđivanje zahteva za resurs

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Generisanu potrebu za resursom možete proslediti kao zahtev za resurs. Zahtev se zatim šalje menadžeru resursa radi ispunjavanja.

1. U aplikaciji Project Service Automation (PSA), na stranici **Projekti** kliknite na karticu **Tim** da biste videli listu resursa koji se mogu rezervisati. 
2. Sa liste izaberite generički resurs koji ima potrebu za resursom, a zatim kliknite na **Prosledi zahtev**.

![Prosleđivanje zahteva za resurs](media/RM-how-to-18.png)

Status zahteva generičkog člana tima će se promeniti u **Prosleđen**.

Kada menadžer resursa ispuni zahtev, generički resurs će biti zamenjen imenovanim resursom ako menadžer resursa ispuni zahtev rezervisanjem imenovanog resursa. U suprotnom, generički resurs će ostati u timu i status zahteva će se promeniti u **Zahteva pregled** ako je menadžer resursa predložio imenovani resurs.
