---
title: Šta je novo ili promenjeno u ažuriranju automatskog ažuriranja usluge projekta Release 41, V3
description: Ovaj tema navodi funkcije i ispravke koje su dostupne u izdanju Microsoft Dynamics 365 Project Service Automation Update Release 41, V3.
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580979"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Šta je novo ili promenjeno u ažuriranju automatskog ažuriranja usluge projekta Release 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da najavimo najnoviju ispravku za aplikaciju Microsoft Dynamics 365 Project Service Automation. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Kompatibilna je sa sistemom Dynamics 365 9.x. Da biste se ažurirali na ovo izdanje, posetite stranicu centra administracije za Dynamics 365 mrežna rešenja i instalirajte ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

Ovaj tema navodi funkcije i ispravke koje su nove ili promenjene za ispravku za automatizaciju usluge projekta Release 41, V3. Ova verzija ima broj verzije V3.10.62.162 i opšte je dostupna putem samo-ispravke u martu 2022. godine.

## <a name="update-release-41"></a>Izdanje ispravke 41

### <a name="bug-fixes"></a>Ispravke grešaka

Popravljeni su sledeći problemi.

**Upravljanje projektima**
- Kada pokušate da kreirate projekat od predloška zasnovanog na projektu kreiranom iz programskog dodatka na radnoj površini, prikazuje se sledeća greška: "Provera valjanosti polja planiranog rada dodele resursa: Datum završetka svakog isečaka vremena dodele resursa ne sme biti raniji od datuma početka".

**Vreme i trošak**
- Kada pokušate da izbrišete stavku vremena, sledeća poruka o grešci prikazuje: "Došlo je do neočekivane greške iz ISV koda".

**Prodaja**
- Kada kreirate fakturu za prekretnicu fiksne cene, polja **Opis** **i Spoljni** opis se ne popunjavaju. 
