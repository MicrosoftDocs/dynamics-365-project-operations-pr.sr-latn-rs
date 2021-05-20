---
title: Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3
description: U ovoj temi su navedene funkcije i ispravke koje su dostupne u izdanju ispravke 29 za Project Service Automation verzije 3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 2ac47974b9cc8386c7446136faf48724de73efce
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sr-Latn-RS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948673"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Šta je novo ili promenjeno u izdanju 29 ispravke Project Service Automation verzije 3

[!include [banner](../includes/psa-now-project-operations.md)]

Zadovoljstvo nam je da objavimo najnovije ažuriranje za aplikaciju Project Service Automation za Dynamics 365. Ovo izdanje uključuje neka važna poboljšanja u kvalitetu, performansama i upotrebljivosti. Ovo izdanje je kompatibilno sa uslugom Dynamics 365 9.x. Da biste ažurirali ovo izdanje, posetite stranicu sa rešenjima centra za administraciju za Dynamics 365 online kako biste instalirali ispravku. Za još informacija pogledajte članak [Instaliranje, ispravka ili uklanjanje željenog rešenja](/power-platform/admin/install-remove-preferred-solution).

U ovoj temi su navedene funkcije i ispravke koje su nove ili promenjene u izdanju ispravke 29 za Project Service Automation verzije 3. Ova verzija ima broj verzije V3.10.47.7 i generalno je dostupna putem samostalnog ažuriranja u februaru 2021.

## <a name="update-release-29"></a>Izdanje ispravke 29

### <a name="bug-fixes"></a>Ispravke grešaka

**Vreme i trošak**

Popravljeni su sledeći problemi:

- Korisnici ne mogu da vide radno vreme zabeleženo neradnim danima u mreži za unos vremena.
- Odobreni unosi troškova mogu se uređivati na mreži.

**Upravljanje projektima**

Popravljeni su sledeći problemi:

- Nedostaje logika validacije da bi se osiguralo da sati angažovanja za dodelu resursa ne mogu biti negativni.
- Prilagođena radnja, **AssignResourcesForTask** ažurira sva polja, a ne samo promenjena.
- Kada kopirate projekat u okruženju sa dodatnim komponentama ili tokovima posla koji su registrovani u događaju **CreateProject**, atribut **msdyn_bulkgenerationstatus** se ne ažurira ako je **CopyWBSToProject** neuspešan.
- Kada proširite kalendar projekta, radni dani se ne sortiraju u rastućem redosledu, što dovodi do neuspeha ažuriranja nekih projektnih zadataka.
- Promena menadžera projekta na postojećem projektu pokreće podrazumevanu logiku organizacione jedinice.

**Prodaja**

Popravljeni su sledeći problemi:

- Kartica **Izvršenje ugovora** na stranici **Ugovor** bez upozorenja ne uspeva tokom inicijalizacije kada nema linija ugovora.