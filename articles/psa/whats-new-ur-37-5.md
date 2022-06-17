---
title: Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Izdanje 37.5, V3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 37.5, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/15/2021
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
ms.openlocfilehash: 46782c4c430ad5d78f2ed1936ae71b42327af9a9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915304"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-375-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Izdanje 37.5, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 37.5, V3. Ova verzija ima broj V3.10.58.130 i opšte je dostupna kroz samostalnu ispravku u novembru 2021.

## <a name="update-release-375"></a>Izdanje ispravke 37.5

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Upravljanje resursima**
- Duplirane rezervacije se kreiraju kada ažurirate postojeće rezervacije, a proporcionalno **je** izabrano za metod **povećanja časova ili** metod **smanjenja časova**.
