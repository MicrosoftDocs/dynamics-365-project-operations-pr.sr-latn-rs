---
title: Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Release 45, V3
description: Ovaj članak navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169186"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Šta je novo ili promenjeno u ažuriranju automatizacije projektne usluge Release 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj članak navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 45, V3. Ova verzija ima broj V3.10.76.168 i obično je dostupna putem samostalnog ažuriranja u julu 2022.

## <a name="update-release-45"></a>Izdanje ispravke 45

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Prodaja**

- Korisnici ne mogu uspešno da kreiraju fakture nakon što pokušaju da kreiraju fakturu bez neželjene prodaje, ako takođe pregledaju istu instancu stranice i ne osvežavaju je.

**Vreme i trošak**

- Kada je savremeno odobravanje omogućeno i opozvano odobrenje projekta odobreno, faza zapisa se nepravilno ažurira u opoziv **zahteva odobrenog**.
- Kada su savremena odobrenja omogućena, a Tokovi u oblaku neaktivni, proces odobravanja nije uspešan, a korisnici koji prosleđuju ili odobravaju nisu obavešteni.
