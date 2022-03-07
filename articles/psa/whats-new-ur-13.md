---
title: Šta je novo ili promenjeno u izdanju 13 ispravke Project Service Automation verzije 3
description: U ovoj temi date su informacije o tome šta je novo u izdanju ispravke 13 za Project Service Automation u verziji 3.
author: ruhercul
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
ms.openlocfilehash: 3a20cf32e578bc818f3ef6ed916784c32b559c3342162bcb7857f5e9cc520d9c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006712"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation izdanje ispravke 13, u verziji 3

[!include [banner](../includes/psa-now-project-operations.md)]

Sa zadovoljstvo najavljujemo najnoviju ispravku za aplikaciju Dynamics 365 Project Service Automation (PSA). Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite centar za administraciju za Dynamics 365 online i idite do stranice sa rešenjima kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

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
     - Ispravljeno: Dodatna dugmad za stavke **Nova mogućnost za poslovanje**, **Ponuda**, **Stavka porudžbine** i **Dodavanje proizvoda** su vidljiva u komandama za mogućnosti za poslovanje, ponude, naručivanje proizvoda i podforme za stavke zasnovane na projektu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]