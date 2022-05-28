---
title: Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Izdanje 39, V3
description: Ovaj tema navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: 1d198f9ad9144f5cc2f533fa9603e1f1a181c8b6
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588753"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Izdanje 39, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj tema navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 39, V3. Ova verzija ima broj verzije V3.10.60.170 i opšte je dostupna putem samo-ispravke u januaru 2022. godine.

## <a name="update-release-39"></a>Izdanje ispravke 39

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Opšte**

- Napravljeno je nekoliko poboljšanja na mapi lokacije za arapsko prevođenje.

**Upravljanje projektima**

- Do greške dolazi kada promenite menadžera projekta na projektu u korisnika koji je već član tima na projektu.

**Prodaja**

- Vlasnik cenovnik ugovora **projekta je** netačan kada se cenovnik automatski kreira. 
- Efekat datuma cenovnka nije ispoštovan kada se cenovnik primeni na parametar projekta.
- Jedinica za ugovaranje možda nema ispravnu podrazumevanu vrednost prilikom uređivanja dve odvojene ponude.
