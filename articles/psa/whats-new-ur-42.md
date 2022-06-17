---
title: Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 42, V3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 42, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: e9911531e4acbd78db416f554c8d85c4f1fee1cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912732"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije usluge projekta Izdanje 42, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 42, V3. Broj izrade ove verzije je V3.10.73.61 i uglavnom je dostupna putem samostalnog ažuriranja u aprilu 2022. godine.

## <a name="update-release-42"></a>Izdanje ispravke 42

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Vreme i trošak**

- Kada je vremenski list odbijen, korisnik koji ga je odbacio je netačno identifikovan kao **Sistem**.
- Kada se stavke vremena uvezu, nedostaje **vrednost "Kategorija** resursa".
- Osobe koje vrše odobravanje projekta mogu da odobre prosleđene projekte kada njihove dozvole nisu posebno podešene na "Može **da odobri"**.

**Prodaja**

- Kada se stvarne datoteke evidentiraju na zadacima koji nisu osnovnog nivoa, stvarni troškovi se nepravilno agregiraju.
