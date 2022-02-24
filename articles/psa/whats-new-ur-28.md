---
title: Šta je novo ili promenjeno u izdanju 28 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 28 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150640"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Šta je novo ili promenjeno u izdanju 28 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene u izdanju ispravke 28 za Project Service Automation verzije 3. Ova verzija ima broj verzije V3.10.46.32 i postala je opšte dostupna putem samostalne ispravke u januaru 2021.

## <a name="update-release-28"></a>Izdanje ispravke 28

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Korisnici mogu da koriste **Masovno uređivanje** za ažuriranje zapisa vremena koji su odobreni i poslati.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- U slučajevima kada se GUID zadatka tumači kao broj, zadaci se ne mogu otvoriti za uređivanje pomoću opcije **Uredi zadatak** u traci na stranici **Strukturna analiza posla**.

**Sales**

Popravljeni su sledeći problemi:

- Izuzetak prazne reference se generiše kada se poziva dodatna komponenta **GetEstimatesForProject**.
- **Označi kao spremno za fakturisanje** u mreži kontrolnih tačaka samo delimično ažurira atribute, osim atributa **InvoiceStatus**, koji se ažurira.

