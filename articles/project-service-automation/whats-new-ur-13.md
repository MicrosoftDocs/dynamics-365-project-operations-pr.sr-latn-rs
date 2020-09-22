---
title: Šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755165"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation u verziji 3, izdanje ispravke 13
Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 13. Ova verzija ima broj verzije V3.10.3.18 i dostupna je prema sledećem planu:

- **Opšta dostupnost (samo-ispravka):** novembar 2019. godine
- **automatska ispravka:** decembar 2019. godine


## <a name="update-release-13"></a>Izdanje ispravke 13 

### <a name="bug-fixes"></a>Ispravke grešaka

- Vreme i trošak

     - Ispravljeno: funkcija pretrage na stranici **Odobrenje troškova** ne radi prilikom pretraživanja prema svrsi troškova.

- Upravljanje resursima

     - Ispravljeno: brojevi u sravnjenju su ispravljeni kako bi bili poravnati udesno.
     - Ispravljeno: nije moguće dodeliti imenovane resurse zadacima putem kartice **Raspored**.

- Upravljanje projektima

     - Ispravljeno: Izuzetak za referencu na vrednost koje nema prilikom dodeljivanja člana tima kada za **TransactionType** nedostaju informacije o podešavanju za entitete **Unit** i **DefaultGroup**.

- Sales

     - Ispravljeno: duplirani zapisi tipa transakcije vraćaju grešku kada se kreiraju zapisi cene uloge.
     - Ispravljeno: dodatna dugmad za **Nova mogućnost za poslovanje**, **Ponuda**, **Stavka porudžbine** i **Dodaj proizvod** su vidljiva u komandama za mogućnosti za poslovanje, ponude, proizvode porudžbine i podformi redova zasnovanih na projektu.


