---
title: Šta je novo ili promenjeno u izdanju 47 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 47 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/14/2022
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
ms.openlocfilehash: 08e8fa9c41bdd77d93e4d5207266115022fba1b2
ms.sourcegitcommit: 498a5d5a33c47cab788fac4215fc47662042155a
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 09/14/2022
ms.locfileid: "9477288"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-47-v3"></a>Šta je novo ili promenjeno u izdanju 47 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 45. Ova verzija ima broj verzije 3.10.78.8 i opšte je dostupna putem samostalnog ažuriranja u julu 2022.

## <a name="update-release-47"></a>Izdanje ispravke 47

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Upravljanje resursima**
- Provera valjanosti je ažurirana da bi se osiguralo da korisnici ne mogu da pokreću izuzetak bez reference kada pokušavaju da kreiraju člana projektnog tima bez **Resursa koji je moguće rezervisati**.
