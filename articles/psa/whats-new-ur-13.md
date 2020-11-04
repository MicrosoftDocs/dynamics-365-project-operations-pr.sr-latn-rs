---
title: Šta je novo ili promenjeno u izdanju 13 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4083540"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation izdanje ispravke 13, u verziji 3
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
     - Ispravljeno: dodatna dugmad za **Nova mogućnost za poslovanje** , **Ponuda** , **Stavka porudžbine** i **Dodaj proizvod** su vidljiva u komandama za mogućnosti za poslovanje, ponude, proizvode porudžbine i podformi redova zasnovanih na projektu.


