---
title: Šta je novo ili promenjeno u izdanju 41 ispravke Project Service Automation verzije 3
description: U ovom članku navedene su funkcije i ispravke koje su dostupne u izdanju 41 ispravke usluge Microsoft Dynamics 365 Project Service Automation verzije 3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930565"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Šta je novo ili promenjeno u izdanju 41 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovom članku date su funkcije koje su nove ili su promenjene u rešenju Project Service Automation u verziji 3, izdanje ispravke 41. Ova verzija ima broj verzije V3.10.62.162 i opšte je dostupna putem samo-ispravke u martu 2022. godine.

## <a name="update-release-41"></a>Izdanje ispravke 41

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Upravljanje projektima**
- Kada pokušate da kreirate projekat iz predloška zasnovanog na projektu kreiranom iz programskog dodatka za računare, prikazuje se sledeća greška: „Provera valjanosti polja planiranog rada dodele resursa: Datum završetka svakog isečka vremena dodele resursa ne sme biti pre datuma početka“.

**Vreme i trošak**
- Kada pokušate da izbrišete stavku vremena, prikazuje se sledeća poruka o grešci: „Došlo je do neočekivane greške iz ISV koda“.

**Prodaja**
- Kada kreirate fakturu za kontrolnu tačku sa fiksnom cenom, polja **Opis** i **Spoljni opis** se ne popunjavaju. 
